---
title: Anslut till Microsoft Dataverse
description: Du kan integrera andra appar med Business Central via Microsoft Dataverse. Den här artikeln innehåller tips och trick för hur du konfigurerar anslutningarna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/26/2021
ms.author: bholtorf
ms.openlocfilehash: 00034e8f1be2f88074fb33b53a1c048f81f69ede
ms.sourcegitcommit: 57e8ab70d70849752567eecf29529efe2dcdf3af
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941669"
---
# <a name="connect-to-microsoft-dataverse"></a>Anslut till Microsoft Dataverse

[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

I det här avsnittet beskrivs hur du upprättar en anslutning mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Vanligtvis skapar företag anslutningen för att integrera och synkronisera data med en annan Dynamics 365-affärsapp, till exempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Innan du börjar

Det finns lite information du bör ha tillhanda innan du skapar anslutningen:  

* Webbadressen (URL) till den [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljö du vill ansluta till. Om du använder den **assisterade konfigurationsguiden för Dataverse** för att skapa anslutningen kommer vi att upptäcka dina miljöer, men du kan också ange URL:en till en annan miljö i din klientorganisation.  
* Användarnamn och lösenord för ett konto som har administratörsbehörigheter i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Om du har en lokal [!INCLUDE[prod_short](includes/prod_short.md)], 2020 års utgivningscykel 1, version 16.5, läs då artikeln [Vissa kända problem](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Du måste slutföra den beskrivna lösningen innan du kan skapa anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* Företagets lokala valuta i [!INCLUDE[prod_short](includes/prod_short.md)] måste vara samma som bastransaktionsvalutan i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. När en bastransaktion har angetts i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] kan den inte ändras. Mer information finns i [entiteten Transaktionsvaluta (valuta)](/powerapps/developer/data-platform/transaction-currency-currency-entity). Detta innebär att alla [!INCLUDE[prod_short](includes/prod_short.md)]-företag som du ansluter till en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-organisation måste använda samma valuta.

> [!IMPORTANT]
> Din [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljö får inte vara i administrationsläge. Administrationsläget gör att anslutningen misslyckas eftersom integreringsanvändarkontot för anslutningen inte har administratörsbehörighet. Mer information finns i [Administrationsläge](/power-platform/admin/admin-mode).

> [!Note]
> Här beskrivs proceduren för onlineversionen av [!INCLUDE[prod_short](includes/prod_short.md)].
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt och inte använder Azure Active Directory-kontot för att ansluta till [!INCLUDE [cds_long_md](includes/cds_long_md.md)], måste du också ange användarnamn och lösenord för ett användarkonto för integreringen. Detta kontot kallas "integreringsanvändar"-kontot. Om du använder ett Azure Active Directory-konto krävs eller visas inte integrationens användarkonto. Integrationsanvändaren ställs in automatiskt och kräver ingen licens.

## <a name="set-up-a-connection-to-cds_long_md"></a>Ställ in en anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

För alla andra autentiseringstyper än Microsoft 365-autentisering konfigurerar du din anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på sidan **Konfiguration av anslutning till Dataverse**. För Microsoft 365-autentisering rekommenderar vi att du använder den assisterade konfigurationsguiden **Konfiguration av anslutning till Dataverse**. Guiden gör det enklare att konfigurera anslutningen och specificera avancerade funktioner, till exempel ägarskapsmodell och initial synkronisering.  

> [!IMPORTANT]
> Under installationen av anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ombeds administratören att ge följande behörigheter till en registrerad Azure-tillämpning kallad [!INCLUDE[prod_short](includes/prod_short.md)]-integration för [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * Behörigheten **Öppna [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som dig själv** krävs, varför [!INCLUDE[prod_short](includes/prod_short.md)] för administratörens räkning automatiskt kan skapa icke-interaktiva, icke-licensierade [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogramanvändare, tilldela användaren säkerhetsroller samt distribuera [!INCLUDE[prod_short](includes/prod_short.md)]-integreringslösningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Den här behörigheten används endast en gång vid upprättandet av anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Ha fullständig åtkomst till Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** behörighet krävs så att automatiskt skapade [!INCLUDE[prod_short](includes/prod_short.md)] integrationsprogramanvändare kan komma åt [!INCLUDE[prod_short](includes/prod_short.md)] data som ska synkroniseras.  
> * **Logga in och läsa din profil** behörighet krävs för att verifiera användarloggning i själva verket har säkerhetsrollen systemadministratör tilldelad i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Genom att ge tillstånd till organisationen, är det administratören som omnämns det registrerade Azure-programmet som kallas [!INCLUDE[prod_short](includes/prod_short.md)] integration för [!INCLUDE[cds_long_md](includes/cds_long_md.md)] att synkronisera data med hjälp av automatiskt skapade [!INCLUDE[prod_short](includes/prod_short.md)] användarensreferenser för integrationsprogram.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Så här använder du den assisterade guiden Konfiguration av anslutning till Dataverse
Guiden Konfiguration av anslutning till Dataverse kan göra det enklare att ansluta programmen, och kan till och med hjälpa dig att köra en första synkronisering. Om du väljer att köra inledande synkronisering kommer [!INCLUDE[prod_short](includes/prod_short.md)] att granska data i båda program rekommendationer för hur man tar sig an en inledande synkronisering. Rekommendationerna beskrivs i tabellen nedan.

|Rekommendation  |Beskrivning  |
|---------|---------|
|**Fullständig synkronisering**|Data finns bara i [!INCLUDE[prod_short](includes/prod_short.md)], eller bara i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Rekommendationen är att synkronisera alla data från tjänsten som har den till den andra tjänsten.|
|**Ingen synkronisering**|Data finns i båda programmen, och att köra en fullständig synkronisering skulle duplicera datan. Rekommendationen är att koppla poster.|
|**Beroendet inte uppfyllt**|Data finns i båda programmen, men det går inte att synkronisera raden eller tabellen eftersom dessa är beroende av en rad eller en tabell som har rekommendationen Ingen synkronisering. Om kunder exempelvis inte kan synkroniseras kan data för kontakter som är beroende av kunddatan inte heller synkroniseras.|

> [!IMPORTANT]
> Vanligtvis använder du bara fullständig synkronisering när du integrerar programmen för första gången, och endast ett program innehåller data. Fullständig synkronisering kan vara användbar i en demonstrationsmiljö eftersom den automatiskt skapar och kopplar poster i respektive program, vilket gör det möjligt att snabbare börja arbeta med synkroniserade data. Du bör dock bara köra fullständig synkronisering om du vill ha en rad i [!INCLUDE[prod_short](includes/prod_short.md)] för respektive rad i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] för registermappningarna. Annars kan resultatet bli dubblettposter.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Assisterad konfiguration** och välj sedan relaterad länk.
2. Välj **Skapa en anslutning till Microsoft Dataverse** för att starta den assisterade konfigurationsguiden.
3. Fyll i fälten om det behövs.

> [!NOTE]
> Om du inte uppmanas att logga in med ditt administratörskonto beror det förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Om du vill skapa eller hantera anslutningen manuellt

I följande procedur beskrivs hur du konfigurerar anslutningen manuellt på sidan **Konfiguration av anslutning till Dataverse**. Detta är sidan där du hanterar inställningar för integrering.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Anslutningsinställningar för Dataverse** och välj sedan tillhörande länk.
2. Ange följande information om anslutningen från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Fält|Beskrivning|
    |-----|-----|
    |**Miljö-URL**|Om du äger miljöerna i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] kommer vi att upptäcka dem när du kör installationsguiden. Om du vill ansluta till en annan miljö i en annan klientorganisation, kan du ange administratörsbehörighet för miljön så att vi upptäcker dem. |
    |**Aktiv**|Starta använda integreringen Om du inte aktiverar anslutningen nu sparas anslutningsinställningarna, men användarna kan inte få åtkomst till data i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] från [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan gå tillbaka till sidan och aktivera anslutningen senare.  |

3. I fältet **Ägarskapsmodlel** väljer du om du vill att en grupptabell i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ska äga nya transaktioner, eller om en eller flera specifika användare ska göra det. Om du väljer **Person** måste du ange varje enskild användare. Om du väljer **Team** visas den förvalda affärsenheten i fältet **Kopplad affärsenhet**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|
4. Kontrollera anslutningsinställningarna genom att välja **Anslutning** och sedan **Testa anslutning**.  

    > [!NOTE]  
    > Om datakrypteringen inte har aktiverats i [!INCLUDE[prod_short](includes/prod_short.md)] kommer du att tillfrågas om du vill aktivera den. Välj **Ja** och ange den obligatoriska informationen om du vill aktivera datakryptering. Annars väljer du **Nej**. Du kan aktivera datakryptering senare. Mer information finns i [kryptering av data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i Hjälp för utvecklare och administration.  
5. Om [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkroniseringen inte redan har ställts in får en fråga om du vill använda standardsynkroniseringskonfigurationen. Beroende på om du vill bokföra poster justerade i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)], välj **Ja** eller **Nej**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="connecting-on-premises-versions"></a>Ansluta lokala versioner

Om du vill ansluta [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] måste du ange viss information på **Dataverse anslutningsinställningar**.

Om du vill ansluta med ett Azure Active Directory (Azure AD)-konto måste du registrera ett program i Azure AD och ange program-ID, nyckelvalvhemlighet och URL för omdirigering som ska användas. URL-adressen för omdirigering fylls i förväg och bör användas för de flesta installationer. Du måste ställa in installationen för att använda HTTPS. Mer information finns i [Konfigurera SSL för att skydda anslutningen till Business Central webbklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Om du konfigurerar servern så att den har en annan startsida kan du alltid ändra URL-adressen. Klientens hemlighet kommer att sparas som en krypterad sträng i databasen. 

### <a name="prerequisites"></a>Förutsättningar

Dataverse måste använda någon av följande autentiseringstyper:

* Office 365 (äldre)

  > [!IMPORTANT]
  > Från och med april 2022 kommer Office 365 (äldre) inte längre att stödjas. Mer information finns i [Viktiga ändringar (utfasningar) som kommer i Power Apps, Power Automate och kundengagemangsappar](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).
* Office365 (modern, OAuth2-klienthemlighetsbaserad)
* OAuth

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Så här registrerar du ett program i Azure AD för att ansluta från Business Central till Dataverse

Följande åtgärder förutsätter att du använder Azure AD för att hantera identiteter och åtkomst. Mer information om hur du registrerar ett program i Azure AD finns i [snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Om du inte använder Azure AD, se [använda en annan identitets- och åtkomsthanteringstjänst](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. I Azure Portal, under **Hantera** i navigeringsrutan välj **autentisering**.  
2. Under **omdirigerings-URL**, lägger du till den omdirigerings-URL som föreslås på sidan **Inställningar för Dataverse-anslutning** i [!INCLUDE[prod_short](includes/prod_short.md)].
3. Under **Hantera**, välj **API-behörigheter**.
4. Under **konfigurerade behörigheter** väljer du **Lägg till en behörighet** och lägger sedan till delegerade behörigheter på fliken **Microsoft API:er** på följande sätt:
    * För Business Central lägger du till **Financials.ReadWrite.All** behörighet.
    * För Dynamics CRM lägg till behörigheter **user_impersonation**.  

    > [!NOTE]
    > Namnet på Dynamics CRM API kan ändras.

5. Under **Hantera**, välj **Certifikat och hemligheter** och skapa sedan en ny hemlighet för ditt program. Du kommer att använda hemligheten i [!INCLUDE[prod_short](includes/prod_short.md)] i fältet **klienthemlighet** på sidan **inställningar för Dataverse-anslutning**, eller lagra i en skyddad lagringsenhet och tillhandahålla den i en händelseprenumerant enligt beskrivningen ovan.
6. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Det här är klient-ID:t för ditt program. Du måste ange den på sidan **inställningar för Dataverse-anslutning** i fältet **klient-ID** eller lagra den på ett säkert lagringsutrymme och tillhandahålla den i en händelseprenumeration.
7. I [!INCLUDE[prod_short](includes/prod_short.md)], på sidan **inställningar av Dataverse-anslutning** i fältet **Miljö-URL** anger du URL för din [!INCLUDE[cds_long_md](includes/cds_long_md.md)] miljö.
8. För att aktivera anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)], aktivera växlingen **Aktiverad**.
9. Logga in med ditt administratörskonto för Azure Active Directory (det här kontot måste ha en giltig licens för [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och vara administratör i din [!INCLUDE[cds_long_md](includes/cds_long_md.md)] miljö). När du har loggat in kommer du att uppmanas att tillåta att ditt registrerade program loggar in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på ditt företags vägnar. Du måste ange ett medgivande för att slutföra installationen.

   > [!NOTE]
   > Om du inte uppmanas att logga in med ditt administratörskonto beror det förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Använda en annan identitets- och åtkomsthanteringstjänst

Om du inte använder Azure Active Directory för att hantera identiteter och åtkomst behöver du en viss hjälp från en utvecklare. Om du hellre vill lagra program-ID och hemlighet på en annan plats kan du lämna fälten klient-ID och klienthemlighet tomma och skriva ett tillägg för att hämta ID och hemlighet från platsen. Du kan tillhandahålla hemligheten vid körning genom att prenumerera på `OnGetCDSConnectionClientId`- och `OnGetCDSConnectionClientSecret`-händelserna i codeunit 7201 `CDS Integration Impl.`.

### <a name="to-disconnect-from-cds_long_md"></a>Koppla bort från [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Anslutningsinställningar för Dataverse** och välj sedan tillhörande länk.
2. På sidan **Konfiguration av anslutning till Dataverse** stänger du av reglaget **Aktiverad**.  

## <a name="see-also"></a>Se även

[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]