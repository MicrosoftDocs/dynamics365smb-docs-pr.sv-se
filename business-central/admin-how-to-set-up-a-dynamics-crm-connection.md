---
title: Ansluta till Common Data Service | Microsoft Docs
description: Du kan integrera andra appar med Business Central via Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/24/2020
ms.author: bholtorf
ms.openlocfilehash: e6ee18367ad229ab56d694d0bbac23e1959b1a5f
ms.sourcegitcommit: edad0d0b129e916c2cfdfa9c4f8d9d83513f4fd1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/24/2020
ms.locfileid: "3619416"
---
# <a name="connect-to-common-data-service"></a>Anslut till Common Data Service

I det här avsnittet beskrivs hur du upprättar en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Vanligtvis skapar företag anslutningen för att integrera och synkronisera data med en annan Dynamics 365-affärsapp, till exempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Innan du börjar

Det finns lite information du bör ha tillhanda innan du skapar anslutningen:  

* Webbadressen (URL) till den [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljö du vill ansluta till. Om du använder den assisterade konfigurationsguiden **Inställningar för CDS-anslutning** för att skapa anslutningen kommer vi att upptäcka dina miljöer, men du kan också ange URL:en till en annan miljö i din klientorganisation.  
* Användarnamn och lösenord för ett konto som har administratörsbehörigheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

> [!Note]
> Här beskrivs proceduren för onlineversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Om du använder Business Central lokal och inte använder Azure Active Directory-kontot för att ansluta till [!INCLUDE [cds_long_md](includes/cds_long_md.md)], måste du också ange användarnamn och lösenord för ett användarkonto för integreringen. Detta kontot kallas "integreringsanvändar"-kontot. Om du använder ett Azure Active Directory-konto krävs eller visas inte integrationens användarkonto. Integrationsanvändaren ställs in automatiskt och kräver ingen licens.

## <a name="set-up-a-connection-to-cds_long_md"></a>Ställ in en anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

För alla autentiseringstyper förutom Office 365-autentisering kan du ställa in anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på sidan **Inställningar för CDS-anslutning**. För Office 365-autentisering rekommenderar vi att du använder den assisterade konfigurationsguiden **Inställningar för Common Data Service-anslutning**. Guiden gör det enklare att konfigurera anslutningen och specificera avancerade funktioner, till exempel ägarskapsmodell och initial synkronisering.  

> [!IMPORTANT]
> Under installationen av anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ombeds administratören att ge följande behörigheter till registrerad Azure-tillämpning [!INCLUDE[d365fin](includes/d365fin_md.md)] som heter integration för [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * **Åtkomst [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som du** behöver [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du, för administratörens räkning, automatiskt skapa icke-interaktiva [!INCLUDE[d365fin](includes/d365fin_md.md)] integrationsprogramanvändare, tilldela användaren säkerhetsroller och distribuera [!INCLUDE[d365fin](includes/d365fin_md.md)] bas-CD-lösning för integrering till [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Den här behörigheten används endast en gång vid upprättandet av anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Ha fullständig åtkomst till Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** behörighet krävs så att automatiskt skapade [!INCLUDE[d365fin](includes/d365fin_md.md)] integrationsprogramanvändare kan komma åt [!INCLUDE[d365fin](includes/d365fin_md.md)] data som ska synkroniseras.  
> * **Logga in och läsa din profil** behörighet krävs för att verifiera användarloggning i själva verket har säkerhetsrollen systemadministratör tilldelad i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Genom att ge tillstånd till organisationen, är det administratören som omnämns det registrerade Azure-programmet som kallas [!INCLUDE[d365fin](includes/d365fin_md.md)] integration för [!INCLUDE[cds_long_md](includes/cds_long_md.md)] att synkronisera data med hjälp av automatiskt skapade [!INCLUDE[d365fin](includes/d365fin_md.md)] användarensreferenser för integrationsprogram.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Så här använder den assisterade konfigurationsguiden Inställningar för Common Data Service-anslutning

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Assisterad konfiguration** och välj sedan relaterad länk.
2. Välj **ställa in Common Data Service-anslutning** för att starta guiden för assisterad konfiguration.
3. Fyll i fälten om det behövs.

### <a name="to-create-or-maintain-the-connection-manually"></a>Om du vill skapa eller hantera anslutningen manuellt

I följande procedur beskrivs hur du konfigurerar anslutningen manuellt på sidan **Inställningar för CDS-anslutning**. Detta är sidan där du hanterar inställningar för integrering.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för CDS-anslutning** och välj sedan tillhörande länk.
2. Ange följande information om anslutningen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Fält|Beskrivning|
    |-----|-----|
    |**Miljö-URL**|Om du äger miljöerna i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] kommer vi att upptäcka dem när du kör installationsguiden. Om du vill ansluta till en annan miljö i en annan klientorganisation, kan du ange administratörsbehörighet för miljön så att vi upptäcker dem. |
    |**Aktiv**|Starta använda integreringen Om du inte aktiverar anslutningen nu sparas anslutningsinställningarna, men användarna kan inte få åtkomst till data i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gå tillbaka till sidan och aktivera anslutningen senare.  |

3. I fältet **Ägarskapsmodlel** väljer du om du vill att en gruppenhet i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ska äga nya transaktioner, eller om en eller flera specifika användare ska göra det. Om du väljer **Person** måste du ange varje enskild användare. Om du väljer **Team** visas den förvalda affärsenheten "BCI Company" i fältet **Kopplad affärsenhet**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Ange följande avancerade inställningar.

    |Fält|Beskrivning|
    |-----|-----|
    |**[!INCLUDE[d365fin](includes/d365fin_md.md)] Användare måste mappa till CDS-användare**|Om du använder modellen för personägarskap anger du om [!INCLUDE[d365fin](includes/d365fin_md.md)]-användarkonton måste ha matchande användarkonton i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. **Office 365 E-postadress för autentisering** av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användaren måste vara samma som **Primär e-postadress** för [!INCLUDE[crm_md](includes/crm_md.md)]-användaren.<br /><br /> Om du anger värdet till **Ja** kommer [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som inte har något matchande [!INCLUDE[crm_md](includes/crm_md.md)]-användarkonto inte ha [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationskapaciteter i användargränssnittet. Åtkomst till [!INCLUDE[crm_md](includes/crm_md.md)]-data direkt från [!INCLUDE[d365fin](includes/d365fin_md.md)] utförs på [!INCLUDE[crm_md](includes/crm_md.md)]-användarkontots vägnar.<br /><br /> Om du anger värdet till **Nej** kommer alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare ha [!INCLUDE[crm_md](includes/crm_md.md)]--integrationskapaciteter i användargränssnittet. Åtkomst till [!INCLUDE[crm_md](includes/crm_md.md)]-data gör på [!INCLUDE[crm_md](includes/crm_md.md)]-anslutningens (integration) vägnar.|
    |**Nuvarande Business Central-säljare mappas till en användare**|Anger om användarkontot är mappat till ett konto i [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Kontrollera anslutningsinställningarna genom att välja **Anslutning** och sedan **Testa anslutning**.  

    > [!NOTE]  
    > Om datakrypteringen inte har aktiverats i [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer du att tillfrågas om du vill aktivera den. Välj **Ja** och ange den obligatoriska informationen om du vill aktivera datakryptering. Annars väljer du **Nej**. Du kan aktivera datakryptering senare. Mer information finns i [kryptering av data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i Hjälp för utvecklare och administration.  

5. Om [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkroniseringen inte redan har ställts in får en fråga om du vill använda standardsynkroniseringskonfigurationen. Beroende på om du vill bokföra poster justerade i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)], välj **Ja** eller **Nej**.

## <a name="show-me-the-process"></a>Visa det här tillvägagångssättet

Följande video visar vilka steg du tar för att ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Ansluta lokala versioner

Om du vill ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] lokalt till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] måste du ange viss information på **Common Data Service anslutningsinställningar**.

Om du vill ansluta med ett Azure Active Directory (Azure AD)-konto måste du registrera ett program i Azure AD och ange program-ID, nyckelvalvhemlighet och URL för omdirigering som ska användas. URL-adressen för omdirigering fylls i förväg och bör användas för de flesta installationer. Du måste ställa in installationen för att använda HTTPS. Mer information finns i [Konfigurera SSL för att skydda anslutningen till Business Central webbklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Om du konfigurerar servern så att den har en annan startsida kan du alltid ändra URL-adressen. Klientens hemlighet kommer att sparas som en krypterad sträng i databasen.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Så här registrerar du ett program i Azure AD för att ansluta från Business Central till Common Data Service

Följande åtgärder förutsätter att du använder Azure AD för att hantera identiteter och åtkomst. Mer information om hur du registrerar ett program i Azure AD finns i [snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Om du inte använder Azure AD, se [använda en annan identitets- och åtkomsthanteringstjänst](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. I Azure Portal, under **Hantera** i navigeringsrutan välj **autentisering**.  
2. Under **omdirigerings-URL**, lägger du till den omdirigerings-URL som föreslås på sidan **Inställningar för Common Data Service-anslutning** i [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Under **Hantera**, välj **API-behörigheter**.
4. Under **konfigurerade behörigheter** väljer du **Lägg till en behörighet** och lägger sedan till delegerade behörigheter på fliken **Microsoft API:er** på följande sätt:
    * För Business Central lägger du till **Financials.ReadWrite.All** behörighet.
    * För Dynamics CRM lägg till behörigheter **user_impersonation**.  

    > [!NOTE]
    > Namnet på Dynamics CRM API kan ändras.

5. Under **Hantera**, välj **Certifikat och hemligheter** och skapa sedan en ny hemlighet för ditt program. Du kommer att använda hemligheten i [!INCLUDE[d365fin](includes/d365fin_md.md)] i fältet **klienthemlighet** på sidan **inställningar för Common Data Service-anslutning**, eller lagra i en skyddad lagringsenhet och tillhandahålla den i en händelseprenumerant enligt beskrivningen ovan.
6. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Det här är klient-ID:t för ditt program. Du måste ange den på sidan **inställningar för Common Data Service-anslutning** i fältet **klient-ID** eller lagra den på ett säkert lagringsutrymme och tillhandahålla den i en händelseprenumeration.
7. I [!INCLUDE[d365fin](includes/d365fin_md.md)], på sidan **inställningar av Common Data Service-anslutning** i fältet **Miljö-URL** anger du URL för din [!INCLUDE[cds_long_md](includes/cds_long_md.md)] miljö.
8. För att aktivera anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)], aktivera växlingen **Aktiverad**.
9. Logga in med ditt administratörskonto för Azure Active Directory (det här kontot måste ha en giltig licens för [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och vara administratör i din [!INCLUDE[cds_long_md](includes/cds_long_md.md)] miljö). När du har loggat in kommer du att uppmanas att tillåta att ditt registrerade program loggar in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på ditt företags vägnar. Du måste ange ett medgivande för att slutföra installationen.

   > [!NOTE]
   > Om du inte uppmanas att logga in med ditt administratörskonto beror det förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Använda en annan identitets- och åtkomsthanteringstjänst

Om du inte använder Azure Active Directory för att hantera identiteter och åtkomst behöver du en viss hjälp från en utvecklare. Om du hellre vill lagra program-ID och hemlighet på en annan plats kan du lämna fälten klient-ID och klienthemlighet tomma och skriva ett tillägg för att hämta ID och hemlighet från platsen. Du kan tillhandahålla hemligheten vid körning genom att prenumerera på händelserna OnGetCDSConnectionClientId och OnGetCDSConnectionClientSecret i codeunit 7201 "CD-integrering impl."

### <a name="to-disconnect-from-cds_long_md"></a>Koppla bort från [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för CDS-anslutning** och välj sedan tillhörande länk.
2. På sidan **Inställnignar för CDS-anslutning** stänger du av brytaren **Aktiverad**.  

## <a name="see-also"></a>Se även

[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  
