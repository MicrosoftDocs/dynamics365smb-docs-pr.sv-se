---
title: Anslut till Microsoft Dataverse (innehåller video)
description: Skapa en anslutning mellan Business Central och Dataverse. Företag skapar vanligtvis anslutningen för att integrera data med en annan Dynamics 365-affärsapp.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 7200, 7201
ms.date: 09/30/2021
ms.author: bholtorf
ms.openlocfilehash: f83764061bb341b0b9d6619a0c5d14cac6b664a9
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383837"
---
# <a name="connect-to-microsoft-dataverse"></a>Anslut till Microsoft Dataverse



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

För alla autentiseringstyper förutom Microsoft 365-autentisering kan du ställa in anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på sidan **Dataverse-anslutningsinställningar**. För Microsoft 365-autentisering rekommenderar vi att du använder guiden för assisterad konfiguration **Dataverse-anslutningsinställningar**. Guiden gör det enklare att konfigurera anslutningen och specificera avancerade funktioner, till exempel ägarskapsmodell och initial synkronisering.  

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

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Assisterad konfiguration** och väljer sedan relaterad länk.
2. Välj **Skapa en anslutning till Microsoft Dataverse** för att starta den assisterade konfigurationsguiden.
3. Fyll i fälten om det behövs.

> [!NOTE]
> Om du inte uppmanas att logga in med ditt administratörskonto beror det förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Om du vill skapa eller hantera anslutningen manuellt

I följande procedur beskrivs hur du konfigurerar anslutningen manuellt på sidan **Konfiguration av anslutning till Dataverse**. Detta är sidan där du hanterar inställningar för integrering.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av inställningen av Dataverse** och väljer sedan relaterad länk.
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
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Kontrollera anslutningsinställningarna genom att välja **Anslutning** och sedan **Testa anslutning**.  

    > [!NOTE]  
    > Om datakrypteringen inte har aktiverats i [!INCLUDE[prod_short](includes/prod_short.md)] kommer du att tillfrågas om du vill aktivera den. Välj **Ja** och ange den obligatoriska informationen om du vill aktivera datakryptering. Annars väljer du **Nej**. Du kan aktivera datakryptering senare. Mer information finns i [kryptering av data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i Hjälp för utvecklare och administration.  
5. Om [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkroniseringen inte redan har ställts in får en fråga om du vill använda standardsynkroniseringskonfigurationen. Beroende på om du vill bokföra poster justerade i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)], välj **Ja** eller **Nej**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Anpassa matchningsbaserad koppling

Från och med 2021 utgivningscykel 2 kan du skriva poster i [!INCLUDE [prod_short](includes/prod_short.md)] och [!INCLUDE [cds_long_md](includes/cds_long_md.md)] baserat på matchande kriterier som definierats av administratören.  

Algoritmen för matchande poster kan startas från följande platser i [!INCLUDE [prod_short](includes/prod_short.md)]:

* Lista sidor som visar poster som är synkroniserade med [!INCLUDE [cds_long_md](includes/cds_long_md.md)], till exempel sidorna kunder och artiklar.  

    Markera flera poster och välj sedan åtgärden **relaterad**, välj **Dataverse**, välj **koppling** och sedan **Matchbaserad koppling**.

    När den matchande kopplingsmetoden startas från en huvuddatalista schemaläggs ett kopplingsjobb direkt efter att du har valt kopplingskriteriet.  
* Sidan **Dataverse Fullständig synk.granskning**.  

    När hela synkroniseringsprocessen upptäcker att du har frikopplade poster båda i [!INCLUDE [prod_short](includes/prod_short.md)] och i [!INCLUDE [cds_long_md](includes/cds_long_md.md)], en länk **Välj kopplingskriterier** visas för relevant integrationstabell.  

    Du kan starta processen **Kör fullständig synkronisering** från sidorna **Dataverse Anslutningsinställningar** och **Dynamics 365 anslutningsinställning** och det kan initieras som ett steg i **Upprätta en anslutning till Dataverse** assisterad konfigurationsguide när du väljer att slutföra installationen och köra full synkronisering i slutet.  

    När den matchande kopplingsmetoden startas från sidan **Dataverse Fullständig synk.granskning** schemaläggs ett kopplingsjobb direkt efter att du har slutfört konfigurationen.  
* Listan **integreringstabellens mappningslista** list.  

    Välj en mappning, välj åtgärden **koppling** och välj sedan **Matchningsbaserad koppling**.

    När metoden matchningskoppling startas från en mappning för integrationstabellen, kommer ett kopplingsjobb att köras för alla icke-raderade poster i mappningen. Om den kördes för en uppsättning med valda poster från listan, körs den bara för de transaktioner som har valts.

I alla tre fallen öppnas sidan **Välj kopplingsvillkor** så att du kan definiera relevanta kopplingskriterier. Anpassa kopplingarna med följande uppgifter på den här sidan:

* Välj vilka fält som ska matcha [!INCLUDE [prod_short](includes/prod_short.md)] poster och [!INCLUDE [cds_long_md](includes/cds_long_md.md)] entiteter efter, och ange även om matchningen i fältet ska vara skiftlägeskänsliga eller inte.  

* Ange om du vill köra en synkronisering efter kopplingsposter och, om posten använder dubbelriktad mappning, även välja vad som ska hända om konflikter visas på sidan **Lös uppdateringskonflikter**.  

* Prioritera ordningen som posterna genomsöks i genom att ange en *matchningsprioritet* för relevanta mappningsfält. Matchningsprioriteterna gör att algoritmen söker efter en matchning i ett antal iterationer som definieras av värdena i fältet **Matcha prioritet** i stigande ordning. Ett tomt värde i fältet **Matcha prioritet** som prioritet 0, så fält med denna värdefyllning behandlas först.  

* Ange om du vill skapa en ny entitetsinstansen i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] om det inte går att hitta någon icke unik ej kopplad matchning med hjälp av matchningsvillkoret. Om du vill aktivera funktionen väljer du åtgärden **Skapa ny om det inte går att hitta någon matchning**.  

### <a name="view-the-results-of-the-coupling-job"></a>Visa resultatet av kopplingsjobbet

Om du vill visa resultatet av kopplings jobbet öppnar du sidan **Registermappningar för integrering**, väljer lämplig mappning, väljer **kopplingsåtgärd** och väljer sedan åtgärden **Logg över integrationskopplingsjobb**.  

Om det finns några poster som inte är kopplade till varandra kan du gå ned i värdet i kolumnen misslyckad, så öppnas en lista över fel som specificerar varför posterna inte kan kopplas.  

Misslyckad koppling inträffar ofta i följande fall:

* Inga matchningsvillkor har definierats

    Kör i så fall matchningsbaserad kopplingen igen, men tänk på att definiera kopplingskriterier.

* Ingen matchning hittades för ett antal poster, baserat på valda matchande fält

    Upprepa i så fall kopplingarna med andra matchande fält.

* Flera matchningar hittades för ett antal poster, baserat på valda matchande fält  

    Upprepa i så fall kopplingarna med andra matchande fält.

* En enskild matchning hittades, men motsvarande post är redan kopplad till en annan post i [!INCLUDE [prod_short](includes/prod_short.md)]  

    Upprepa i så fall kopplingarna med andra matchande fält eller undersök varför [!INCLUDE [cds_long_md](includes/cds_long_md.md)] entiteten är kopplad till den andra posten i [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> För att hjälpa dig att få en överblick över kopplingens framsteg, **Kopplad till Dataverse** visar om en specifik post är kopplad till en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] entitet eller inte. Du kan filtrera listan över poster som synkroniseras med [!INCLUDE [cds_long_md](includes/cds_long_md.md)] det här fältet.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Uppgradera anslutningar från Business Central Online till använda certifikatbaserad autentisering
> [!NOTE]
> Det här avsnittet är endast relevant för innehavaradministration i [!INCLUDE[prod_short](includes/prod_short.md)] online som Microsoft har. Online innehavaradministratörer som körs av ISV och lokala installationer påverkas inte.

I april, 2022, [!INCLUDE[cds_long_md](includes/cds_long_md.md)] är den Office365 autentiseringstypen (användarnamn/lösenord). Mer information finns i avsnittet [Avskrivning autentiseringstyp av Office 365](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Dessutom i mars 2022 avskriver [!INCLUDE[prod_short](includes/prod_short.md)] användning av klienthemlighetsbaserad tjänst-till-tjänst-autentisering för online-innehavare, och kräver att certifikatbaserad tjänst-till-tjänst-autentisering används för anslutningar till [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] onlineklienter som är värdbaserade hos internetföretag och lokala installationer kan fortsätta att använda klienthemlighet för autentisering vid anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

För att undvika störningar i integrationen _måste du uppgradera_ anslutningen så att den använder certifikatbaserad autentisering. Ãven om ändringen är schemalagd för mars 2022 rekommenderar vi starkt att du uppgraderar så snart som möjligt. Följande steg beskriver hur du uppgraderar till certifikatbaserad autentisering. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>För att uppgradera din Business Central online-anslutning för att använda certifikatbaserad autentisering

> [!NOTE]
> Certifikatbaserad autentisering finns i Business Central 2021 utgivningscykel 1 och senare. Om du använder en tidigare version måste du schemalägga en uppdatering till Business Central 2021 utgivningscykel 1 före mars, 2022. Mer information finns i [Schemalägg uppdateringar](/dynamics365/business-central/dev-itpro/administration/update-rollout-timeline#scheduling-updates). Kontakta partnern eller supporten om du får problem.

1. I [Business Central administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center) kontrollerar du att du använder Business Central utgivningscykel 1 för 2021 eller senare (version 18 eller senare).
2. Gör något av följande beroende på om du har integrerat med Dynamics 365 Sales:
   * Om du vill kan du öppna sidan **Microsoft Dynamics 365 anslutningsinställning**.
   * Om du vill kan du öppna sidan **Dataverse anslutningsinställning**.
3. Välj **anslutning** och sedan **Använd certifikatautentisering** för att uppgradera anslutningen till att använda certifikatbaserad autentisering.
4. Logga in med administratörsautentiseringsuppgifter för Dataverse. Inloggningen tar mindre än en minut.

> [!NOTE]
> Du måste upprepa dessa steg i varje [!INCLUDE[prod_short](includes/prod_short.md)]-miljö, inklusive både produktions- och miljöer i begränsat läge och i varje företag där du är ansluten till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

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

Följande åtgärder förutsätter att du använder Azure AD för att hantera identiteter och åtkomst. Mer information om hur du registrerar ett program i Azure AD finns i [snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

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

### <a name="to-disconnect-from-cds_long_md"></a>Koppla bort från [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av inställningen av Dataverse** och väljer sedan relaterad länk.
2. På sidan **Konfiguration av anslutning till Dataverse** stänger du av reglaget **Aktiverad**.  

## <a name="see-also"></a>Se även

[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
