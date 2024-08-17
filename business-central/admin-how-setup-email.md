---
title: Skapa ett e-postkonto i Business Central
description: Beskriver hur du ansluter e-postkonton till Business Central så att du kan skicka avgående meddelanden utan att behöva öppna någon annan app.
author: brentholtorf
ms.author: bholtorf
ms.topic: get-started
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 06/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-email"></a>Konfigurera e-post

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Personer på företag skickar information och dokument, till exempel försäljnings- och inköpsorder och fakturor, via e-post varje dag. Administratörer kan ansluta ett eller flera e-postkonton till [!INCLUDE[prod_short](includes/prod_short.md)], så att du kan skicka dokument utan att behöva öppna någon e-postapp. Du kan skapa varje meddelande individuellt med grundläggande formateringsverktyg, till exempel teckensnitt, format, färger och så vidare, och bifoga filer på upp till 100 MB. Administratörer kan dessutom skapa rapportlayouter som endast innehåller nyckelinformation från dokument. Läs mer på [Skicka dokument via e-post](ui-how-send-documents-email.md).

E-postfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)] gäller endast för avgående meddelanden. Det går inte att ta emot svar – det vill säga, det finns ingen "Inkorg"-sida.

> [!NOTE]
> Du kan bara e-postfunktioner för [!INCLUDE[prod_short](includes/prod_short.md)] online endast med Exchange Online. Vi stöder inte hybridscenarier, till exempel att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] online till en lokal version av Exchange.
>
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du skapa en app-registrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal innan du kan konfigurera e-post. App-registreringen gör det möjligt för [!INCLUDE[prod_short](includes/prod_short.md)] att auktorisera och autentisera med din e-postleverantör. Lär dig mer på [Konfigurera e-post för Business Central lokalt](admin-how-setup-email.md#set-up-email-for-business-central-on-premises). I [!INCLUDE[prod_short](includes/prod_short.md)] online hanterar vi detta åt dig.

## <a name="requirements"></a>Krav

Det finns några krav för att konfigurera och använda e-postfunktionerna.

* För att kunna konfigurera e-post måste du ha behörighetsinställningen **E-POSTKONFIGURATION**. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).
* Alla som ska använda e-postfunktionerna måste vara helt licensierade [!INCLUDE [prod_short](includes/prod_short.md)]. Delegerade administratörer och gästanvändare kan t. ex. inte använda klientorganisationens e-postkonto.

## <a name="add-email-accounts"></a>Lägg till e-postkonton

Du lägger till e-postkonton via tillägg som möjliggör att konton från olika providrar ansluter till [!INCLUDE[prod_short](includes/prod_short.md)]. Med standardtilläggen kan du använda konton från Microsoft Exchange Online. Det kan emellertid finnas andra tillägg som du kan använda för att ansluta konton från andra leverantörer, till exempel Gmail.

Du kan ange fördefinierade affärsscenarier där kontot ska användas för att skicka e-post. Du kan t. ex. ange att alla användare skickar försäljnings dokument från ett visst konto och inköpsdokument från ett annat. Läs mer på [Tilldela scenarier för e-post till e-postkonton](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

I följande tabell beskrivs de e-posttillägg som är tillgängliga som standard.

|Tillägg  |Beskrivning  |Exempel på när du kan använda  |
|---------|---------|---------|
|**Microsoft 365 anslutningsprogram**|Alla skickar e-post från en delad postlåda i Exchange Online.|När alla meddelanden kommer från samma avdelning, t. ex. genom att din försäljningsorganisation skickar meddelanden från ett sales@cronus.com-konto. Detta alternativ kräver att du skapar en delad postlåda i administrationscentret för Microsoft 365. Mer information finns i [Delade postlådor](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Aktuell anslutningsprogram för användare**|Alla skickar e-post från det konto som de använde för att logga in på [!INCLUDE[prod_short](includes/prod_short.md)].|Tillåt kommunikation från enskilda konton.|
|**SMTP Connector**|Använd SMTP-protokoll för att skicka e-post.|Tillåt kommunikation via din SMTP-e-postserver. |

Tilläggen **Microsoft 365 anslutningsprogram** och **anslutningsprogram för aktuell användare** använder de konton som du har angett för användare i administrationscentret för Microsoft 365 för din Microsoft 365-prenumeration. Användarna måste ha en giltig licens för Exchange Online för att kunna skicka e-post med hjälp av tilläggen. Dessutom, i sandbox-miljöer, inkluderar dessa tillägg **Outlook REST API** kräver att **Tillåt HttpClient-begäranden** är aktiverad. Om du vill kontrollera om den är aktiverad för dessa tillägg, gå till sidan för **tilläggshantering**, välj tillägget och välj sedan alternativet **Konfigurera**.

Externa användare, exempelvis utsedda administratörer och externa revisorer, kan inte använda dessa tillägg för att skicka e-postmeddelanden från [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Om du använder tjänst-till-tjänst-autentisering (S2S) Microsoft 365 och nuvarande användaranslutningsprogram kan inte autentisera användaren när de skickar ett försäljnings- eller köpdokument via e-post. När någon skickar ett dokument visas följande felmeddelande:
>
> "Du har inte behörighet att komma åt den här resursen: https:\//graph.microsoft.com/.default. Kontakta systemadministratören."
>
> Problemet orsakas av de bundna åtgärderna på dokument-API:erna som skickar e-post. Om du vill veta mer om bundna åtgärder går du till [bundna åtgärder](/dynamics365/business-central/dev-itpro/api-reference/v2.0/resources/dynamics_salesinvoice#bound-actions). 
>
> Om du vill använda S2S-autentisering och e-postfunktionerna använder du alternativet SMTP-anslutning.
<br><br>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="use-smtp"></a>Använd SMTP

Om du vill använda SMTP-protokollet för att skicka e-post från [!INCLUDE[prod_short](includes/prod_short.md)] kan du använda SMTP-anslutningstillägget. När du skapar ett konto som använder SMTP är fältet **Sändartyp** av stor vikt. Om du väljer **Specifik användare** kommer e-postmeddelanden att skickas med hjälp av namn och annan information från det konto som du konfigurerar. Om du däremot väljer **Aktuell användare** skickas e-postmeddelanden från det e-postkonto som anges för respektive användares konto. Aktuell användare liknar Skicka som-funktionen. För mer information, se [Använda en adress för ersättningsavsändare i avgående e-postmeddelanden](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Om du vill använda OAuth för SMTP måste alla användare finnas i samma Microsoft Entra-klientorganisation. 
> 
> Du måste skapa en programregistrering i Azure-portalen och sedan köra **Konfigurera guiden för assisterad Microsoft Entra ID-konfiguration** i [!INCLUDE[prod_short](includes/prod_short.md)] för att ansluta till Microsoft Entra ID. Mer information finns i [Skapa en programregistrering för Business Central i Azure-portalen](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online avvecklar grundläggande autentisering för SMTP. KLientorganisationer som för närvarande använder SMTP-autentisering påverkas inte av ändringen. Vi rekommenderar dock starkt att du använder den senaste versionen av [!INCLUDE [prod_short](includes/prod_short.md)] och konfigurerar OAuth 2.0-autentisering för SMTP. Vi kommer inte att lägga till certifikatbaserad autentisering i tidigare versioner av [!INCLUDE [prod_short](includes/prod_short.md)], till exempel version 14. Om du inte kan konfigurera OAuth 2.0-autentisering uppmuntrar vi dig att utforska alternativ från tredje part om du vill använda e-post från SMTP i tidigare versioner.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="use-the-set-up-email-assisted-setup-guide"></a>Använd Konfigurera guiden för assisterad konfiguration för e-post

Med den assisterade konfigurationsguiden för **Konfigurera e-post** kan du snabbt komma igång med e-post.

> [!NOTE]
> Du måste ha ett standardkonto för e-post, även om du bara lägger till ett enda konto. Standardkontot kommer att användas för alla e-postscenarier som inte har tilldelats något konto. Läs mer på [Tilldela scenarier för e-post till e-postkonton](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurera e-postkonton** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Tilldela e-postscenarier till e-postkonton

E-postscenarier är processer som involverar att skicka ett dokument. Exempelvis en försäljnings- eller inköpsorder eller en anmälan, till exempel en inbjudan till en extern revisor. Specifika e-postkonton kan användas för specifika scenarier. Du kan t. ex. ange att alla användare alltid ska skicka försäljningsdokument från ett konto, inköpsdokument från ett annat, samt lager- eller produktionsdokument från ett tredje konto. Du kan tilldela, tilldela om och ta bort scenarier när du vill. Ett scenario kan bara tilldelas ett e-postkonto åt gången. Standardkontot kommer att användas för alla e-postscenarier som inte har tilldelats något konto.

På sidan **Tilldelning av e-postscenario** kan du välja åtgärden **Konfigurera standardbilagor** för att lägga till bifogade filer till e-postscenarier. De bifogade filerna är alltid tillgängliga när du skriver ett e-postmeddelande för ett dokument som är relaterat till scenariot. Varje e-postscenario kan ha en eller flera bifogade standardbilagor. Standardbilagor läggs automatiskt till i e-postmeddelanden för e-postscenariot. När du t.ex. skickar en försäljningsorder med e-post, läggs standardbilagan som anges för försäljningsorderscenariot till. Standardbilagor visas i avsnittet **Bifogadefiler** längst ned på sidan **Skriv ett e-postmeddelande**. Du kan manuellt lägga till bifogade filer som inte är standard i e-postmeddelandet.

<!--
## <a name="to-set-up-email"></a>To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a>Konfigurera visningspolicyer

Du kan kontrollera vilka e-postmeddelanden som en användare kan nå på sidorna Utkorg för e-post och Skickad e-post.

På sidan **Visningspolicyer för användar-e-post** väljer du en användare och därefter ett av följande alternativ i fältet **Visningspolicy för e-post**:

* **Visa egna e-postmeddelanden** – Användaren kan bara visa sina egna e-postmeddelanden.
* **Visa alla e-postmeddelanden** – Användaren kan visa alla e-postmeddelanden, inklusive e-postmeddelanden som har skickats av andra användare.
* **Se om tillgång till alla relaterade poster** – Denna vypolicy används om ingen annan policy anges. Användaren kan visa e-postmeddelanden som andra användare har skickat om användaren har åtkomst till posten som har skickats och alla relaterade poster. Exempelvis skickar användare A en bokförd försäljningsfaktura till en kund. Användare B kan se e-postmeddelandet om denne har tillgång till både fakturan och kunden.
* **Visa om åtkomst till relaterade poster** – Användaren kan visa e-postmeddelanden som har skickats av andra personer om användaren har åtkomst till minst en post som är relaterad till posten som har skickats. Exempelvis skickar användare A en bokförd försäljningsfaktura till en kund. Användare B kan se e-postmeddelandet om denne har tillgång till antingen fakturan eller kunden.

> [!NOTE]
> Om du lämnar fältet **Användar-ID** tomt och sedan väljer åtgärden **Visningspolicy för e-post** gäller visningspolicyn för alla användare.

## <a name="specify-how-many-messages-an-account-can-send-per-minute"></a>Ange hur många meddelanden ett konto får skicka per minut

Vissa e-postleverantörer (ISP) begränsar antalet e-postmeddelanden som ett e-postkonto kan skicka samtidigt eller inom en viss tidsperiod, eller både och. Denna praxis kallad *e-poststrypning* hjälper internetleverantören till att styra trafiken på sina servrar och förhindra skräppost. Om ett e-postkonto överskrider gränsen kan det hända att internetleverantören spärrar meddelandena. Du kan kontrollera att antalet meddelanden som du skickar från [!INCLUDE [prod_short](includes/prod_short.md)] följer internetleverantörens gräns genom att ange gränsen för vart och ett av dina e-postkonton.

Standardgränsen för kontotyperna Microsoft 365 och Aktuell användare är 30, vilket motsvarar den gräns som anges av Exchange Online.

Du kan ange gränsen på två sätt:

* När du använder guiden Konfigurera assisterad konfiguration för e-post för att skapa ett nytt konto anger du gränsen i fältet **Gräns per minut**.
* För befintliga e-postkonton anger du gränsen i fältet **Gräns för e-post** på kontot.

## <a name="set-up-reusable-email-texts-and-layouts"></a>Konfigurera återanvändbara texter och layouter för e-post

Du kan använda rapporter för att inkludera nyckelinformation från försäljnings-, inköps- och tjänstedokument i texter för e-post. Med rapportlayout definieras stilen och innehållet i e-postmeddelandet. Innehållet kan till exempel omfatta text som t. ex. hälsningar eller instruktioner som föregår dokumentinformationen. I den här proceduren beskrivs hur du ställer in rapporten **Försäljning – Faktura** för bokförda försäljningsfakturor, men processen liknar den för andra rapporter.

> [!NOTE]
> Om du vill använda layouten för att skapa innehåll för e-postmeddelanden måste du använda Word-filtyp för layouten.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Rapporturval – försäljning** och väljer sedan relaterad länk.
2. På sidan **Rapportval, försäljning** i fältet **Användning** väljer du **Faktura**.
3. På en ny rad i fältet **Rappport-ID** väljer du t. ex. standardrapport 1306.
4. Markera kryssrutan **Använd för e-postbrödtext**.
5. Välj fältet **Beskrivning av layouten på brödtext i e-post** och välj sedan en layout från listan.
6. Om du vill visa eller redigera den layout som e-mailets brödtext baseras på väljer du layout på sidan **Anpassade rapportlayouter** och väljer sedan åtgärden **Uppdatera layout**. Om du anpassar layouten använder du åtgärden **Importera layout** för att överföra den nya layouten.
    > [!NOTE]
    > Om du vill anpassa en layout för standardrapporter, till exempel 1306, måste du göra en kopia av rapporten. [!INCLUDE [prod_short](includes/prod_short.md)] hjälper dig att skapa en kopia när du importerar en anpassad layout för en standardrapport. Namnet på den nya anpassade rapportlayouten kommer att föregås av "kopia av".
7. Om du vill att kunderna ska använda en betalningstjänst, till exempel PayPal, måste du ställa in tjänsten. Därefter infogas PayPal-informationen och -länken i e-postmeddelandet. Mer information finns i [Så här aktiverar du kundbetalningar via PayPal](sales-how-enable-payment-service-extensions.md).
8. Välj knappen **OK**.

Nu när du till exempel väljer åtgärden **Skicka** på sidan **Bokförd försäljningsfaktura** kommer e-postbrödtexten att innehålla information om dokumentet i rapport 1306 som föregås av utformad standardtext enligt den rapportlayout du valde i steg 5.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Använda en adress för ersättningsavsändare för avgående e-postmeddelanden

Om du använder tillägget SMTP-anslutning kan du använda kan du använda funktionerna **Skicka som** eller **Skicka åt** från Microsoft Exchange för ändra avsändaradressen på avgående meddelanden. [!INCLUDE[prod_short](includes/prod_short.md)] använder SMTP-kontot för att autentisera till Exchange, men kommer antingen att ersätta avsändarens adress med den som du anger eller ändra den med "åt".

När du skapar ett konto och vill använda funktionerna Skicka som eller Skicka åt från Exchange, i fältet **Typ av avsändare** väljer du **Specifik användare**.

Du kan också välja **Aktuell användare** för att tillåta att användare skickar meddelanden via SMTP-anslutning. Meddelandet kommer att skickas från det e-postkonto som angetts i fältet kontakt e-post på användar kortet för den användare som de är inloggade på. Det fungerar emellertid som det ska när du skickar som-funktion och kommer att skickas från det konto som anges i SMTP-anslutningens inställningar.

Nedan följer exempel på hur Skicka som och Skicka åt används i [!INCLUDE[prod_short](includes/prod_short.md)]:

* Du kanske vill att inköps- eller försäljningsorder som du skickar till leverantörer och kunder ska se ut att komma från adressen _noreply@yourcompanyname.com_.
* När arbetsflödet skickar en godkännandeförfrågan via e-post med hjälp av e-postadressen till beställaren.

> [!Note]
> Du kan bara använda ett konto för att ersätta avsändaradresser. Det innebär att du inte kan ha en ersättningsadress för att inköpsprocesser, och en annan för försäljningsprocesser.

<!--
### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a>Konfigurera dokumentutskicksprofiler

Du kan spara tid genom att ange en önskad metod för att skicka försäljningsdokument för respektive kund. Om du gör detta behöver du inte välja ett alternativ för sändning, till exempel om du vill skicka dokumentet via e-post eller ett elektroniskt dokument, varje gång du skickar ett dokument. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

## <a name="optional-set-up-email-logging-in-exchange-online"></a>Tillval: Konfigurera e-postloggning i Exchange Online

Få ut mer av kommunikationen mellan säljare och befintliga eller potentiella kunder. Du kan spåra e-postutbyten och sedan göra dem till de möjligheter som kan åtgärdas. Lär dig mer på [Spåra utbyten av e-postmeddelanden mellan säljare och kontakter](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="optional-monitor-email-usage-and-troubleshoot-email-failures-with-telemetry"></a>Tillval: övervaka e-postanvändning och felsök e-postfel med telemetri

Administratörer kan växla till funktionen telemetri i [!INCLUDE[prod_short](includes/prod_short.md)] för att hämta data om användning och fel i olika funktioner i systemet. För e-post loggar vi in följande åtgärder:

- Ett e-postmeddelande har skickats  
- Ett försök att skicka ett e-postmeddelande misslyckades   
- Autentisering till en SMTP-server lyckades/misslyckades  
- Anslutning till en SMTP-server lyckades/misslyckades  

Du kan använda dessa data för att övervaka e-postanvändning och felsöka e-postfel. Mer information finns i [Analysera e-posttelemetri (administrationsinnehåll)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace).  

## <a name="set-up-email-for-business-central-on-premises"></a>Konfigurera e-post för Business Central lokalt

[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan integreras med tjänster som baseras på Microsoft Azure. Du kan till exempel använda Cortana Intelligence för smartare kassaflödesprognoser, Power BI för att visualisera verksamheten och Exchange Online för att skicka e-post. Integreringen med dessa tjänster baseras på en programregistrering i Microsoft Entra ID. Programregistreringen tillhandahåller autentisering och autentiseringstjänster för kommunikation. Om du vill använda e-postfunktionerna i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du registrera [!INCLUDE[prod_short](includes/prod_short.md)] som en app i Azure-portalen och sedan ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till programregistreringen. Följande avsnitt beskriver hur du gör detta.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Skapa en programregistrering för Business Central i Azure-portalen

Stegen för att registrera [!INCLUDE[prod_short](includes/prod_short.md)] i Azure portal beskrivs i [Registrera ett program i Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Om du vill använda e-postfunktioner måste din programregistrering använda en konfiguration för flera innehavare.

De inställningar som är specifika för e-postfunktionen är de delegerade behörigheter som du ger din programregistrering. Följande register anger minimibehörigheterna.

|API/behörighetsnamn  |Typ  |Beskrivning  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegerades|Logga in och läs användarprofilen.         |
|Microsoft Graph / Mail.ReadWrite |Delegerades|Skriv e-postmeddelanden.         |
|Microsoft Graph / Mail.Send|Delegerades|Skicka e-postmeddelanden.         |
|Microsoft Graph / offline_access|Delegerades|Behåll medgivande för dataåtkomst.|
|Microsoft Graph / Mail.Send.Shared|Delegerades|Delad postlåda|

Om du använder SMTP-anslutning och vill använda OAuth 2.0 för autentisering, är behörigheterna något annorlunda. Följande register anger behörigheterna.

|API/behörighetsnamn  |Typ  |Beskrivning  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Delegerades|Behåll medgivande för dataåtkomst.|
|Microsoft Graph / openid|Delegerades|Logga in användare.|
|Microsoft Graph / User.Read |Delegerades|Logga in och läs användarprofilen.         |
|Microsoft Graph / SMTP.Send|Delegerades|Skicka e-postmeddelanden från postlådor med SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Delegerades|Logga in och läs användarprofilen.         |

Notera följande information när du skapar din appregistrering. Du kommer att behöva den för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till din app-registrering.
 
* Program-ID (klient)
* Omdirigerings-URI (valfritt)
* Klienthemlighet

Lär dig mer om allmänna riktlinjer om hur du registrerar ett program i [Snabbstart: Registrera ett program med Microsofts identitetsplattform](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Om du har problem med att använda SMTP-protokoll för att skicka e-post efter att du har anslutit [!INCLUDE[prod_short](includes/prod_short.md)] till din programregistrering kan det bero på att SMTP-autentisering inte har aktiverats för klientorganisationen. Vi rekommenderar att du använder e-postkopplingarna från Microsoft 365 och Aktuell användare i stället, eftersom de använder Microsoft Graph Mail API:er. Om du måste använda SMTP-protokoll kan du emellertid aktivera SMTP AUTH. Mer information finns i [Aktivera eller inaktivera autentiserad klient-SMTP-sändning (SMTP-autentisering) i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect--to-your-app-registration"></a>Anslut [!INCLUDE[prod_short](includes/prod_short.md)] till din app-registrering

När du har registrerat ditt program i Azure portal går du till [!INCLUDE[prod_short](includes/prod_short.md)] och använder sidan **Registrering för e-postprogram för Microsoft Entra ID** för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till den.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Registrering för e-postprogram för Microsoft Entra ID** och väljer sedan tillhörande länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Om du ansluter för första gången kan du också köra den assisterade konfigurationsguiden **Konfigurera e-post**. I det här fallet innehåller guiden också registreringssidan för e-postprogram för Microsoft Entra ID där du kan lägga till information för att ansluta till din programregistrering. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Microsoft Entra ID, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant)** or **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Microsoft Entra ID, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-also"></a>Se även

[Delade postlådor i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som din företagsinkorg i Outlook](admin-outlook.md)  
[Få [!INCLUDE[prod_short](includes/prod_short.md)] på min mobila enhet](install-mobile-app.md)   
[Få [!INCLUDE[prod_short](includes/prod_short.md)] på min mobila enhet](install-mobile-app.md)   
[Analysera e-posttelemetri (administrationsinnehåll)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
