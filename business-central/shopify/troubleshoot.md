---
title: Felsöka synkroniseringen mellan Shopify och Business Central
description: Lår dig vad du ska göra om något går fel under synkroniseringen av data mellan Shopify och Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization" />Felsöka synkroniseringen mellan Shopify och Business Central

Det kan hända att du behöver felsöka problem när du synkroniserar data mellan Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)]. På den här sidan beskrivs åtgärder för att felsöka vanliga scenarier.

## <a name="run-tasks-in-the-foreground" />Kör uppgifter i förgrund

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill felsöka och öppna sidan **Shopify-butikskort**.
3. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.

När synkroniseringsåtgärden utlöses, körs uppgiften i förgrunden. Om ett fel inträffar visas en feldialogruta med länken **Kopiera Detaljer**. Använd den här länken om du vill kopiera information till en textredigerare för vidare analys.

## <a name="logs" />Loggar

Om en synkroniseringsuppgift misslyckas kan du aktivera **Logg aktiverad** på sidan **Shopify butikskort** för att aktivera loggning. Du kan sedan utlösa synkroniseringsuppgift och granska loggar manuellt.

### <a name="to-enable-logging" />Så här aktiverar du loggning

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill felsöka och öppna sidan **Shopify-butikskort**.
3. Slå på brytaren **Logg aktiverad**.

### <a name="to-review-logs" />Att granska loggar

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-loggposter** och väljer sedan relaterad länk.
2. Välj den berörda loggposten och öppna sidan **Shopify-loggpost**.
3. Kontrollera värden för begäran, statuskod och beskrivning och svar. Du kan hämta värdena för begäran och svar som filer i ett text format.

Senare, kom ihåg att stänga av loggning för att undvika negativ effekt på prestanda och ökning av databasstorlek.

Från sidan **Shopify-loggposter** kan du utlösa borttagning av alla loggposter eller transaktioner som är äldre än sju dagar.

## <a name="data-capture" />Datainsamling

Oavsett om **Logg aktiverad** är aktiverad eller inte loggas alltid Shopify svar. Du kan kontrollera eller hämta loggarna från sidan **Datainsamlingslista**.

Välj åtgärden **Hämtade Shopify-data** på en av följande sidor:

- **Shopify-order**
- **Shopify-orderuppfyllelse**
- **Leveranskostnader för Shopify-order**
- **Shopify-ordertransaktioner**
- **Shopify-utbetalningar**
- **Shopify-betalningstransaktioner**
- **Shopify-transaktioner**

## <a name="reset-sync" />Återställ synkronisering

För optimala prestanda importerar kopplingen endast kunder, produkter och order som har skapats eller ändrats sedan den senaste synkroniseringen. På sidan **Shopify-butikskortet** finns funktioner för att ändra datum och tid för den senaste synkroniseringen eller för att återställa den helt. Med den här funktionen ser du till att alla data synkroniseras och inte bara de ändringar som gjorts sedan den senaste synkroniseringen utfördes.

Den här funktionen kan endast användas för synkronisering från Shopify till [!INCLUDE[prod_short](../includes/prod_short.md)]. Den kan vara användbar om du behöver återställa borttagna data, såsom produkter, kunder eller borttagna ordrar.

## <a name="request-the-access-token" />Kräv åtkomsttoken

Om [!INCLUDE[prod_short](../includes/prod_short.md)] inte kan ansluta till ditt Shopify konto kan du prova att återställa åtkomsttoken från Shopify. Du kan behöva begära en ny token om ändringar gjorts i säkerhetsnycklar eller nödvändiga behörigheter (programomfattningarna).

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik som du vill hämta åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas att logga in på ditt Shopify-konto.

Växlas **Har AccessKey** kommer att aktiveras.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment" />Kontrollera och aktivera behörigheter för att göra HTTP-begäranden i en miljö utan produktions miljön

Anslutningstillägget kräver Shopify behörighet att göra HTTP-begäranden för att det ska fungera korrekt. Vid testning i en miljö för begränsat läge är HTTP-begäranden förbjudna för alla tillägg.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tilläggshantering** och väljer sedan relaterad länk.
2. Välj tillägget **Shopify Connector**.
3. På sidan **Konfigurera** väljer du åtgärden **Tilläggsinställningar**.
4. Kontrollera att växlingsknappen **Tillåt HTTPClient-begäranden** är aktiverat.

## <a name="rotate-the-shopify-access-token" />Rotera Shopify åtkomsttoken

I följande procedurer beskrivs hur du roterar den åtkomsttoken som används av Shopify Connector för att komma åt din Shopify onlinebutik.

### <a name="in-shopify" />I Shopify

1. Gå till **Shopify administratör** i din [appar](https://www.shopify.com/admin/apps).
2. Välj **Ta bort** i raden med **Dynamics 365 Business Central**-appen.
3. Välj **Ta bort** i meddelandet.

### <a name="in-includeprodshortincludesprodshortmd" />I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butiker** och väljer sedan relaterad länk.
2. Välj den butik som du vill rotera åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas till det, loggar du in på ditt Shopify-konto, granskar sekretess och behörigheter och trycker sedan på knappen **Installera app**.

## <a name="known-issues" />Kända problem

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store" />Fel: försäljningshuvudet finns inte. Identifieringsfält och värden: dokumenttyp='Quote',No.='YOUR SHOPIFY STORE'

För att beräkna priser skapar Shopify anslutningsprogram ett tillfälligt försäljningsdokument (offert) för tillfällig kund (butikskod) och använder standardprisberäkningslogiken. Om ett tillägg från en annan tillverkare prenumererar på händelser i ett temporärt försäljningsdokument kanske inte huvudet är tillgängligt. Du bör kontakta tilläggets leverantör. Be dem att ändra sin kod och söka efter tillfälliga poster. I vissa fall behöver de bara lägga till `IsTemporary` metoden på rätt plats. Om du vill veta mer om `IsTemporary`, gå till [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Du kan kontrollera att problemet orsakas av ett tredje parts tillägg genom att använda länken **Kopiera information till Urklipp** i felmeddelandet och kopiera innehållet till textredigerare. Informationen innehåller en **Al-anropsstack** där den översta raden är den rad där fel uppstod. Följande exempel visar en AL-anropsstack.

AL-anropsstack:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Kom ihåg informationen om resursen AL-anropsstacken till med tilläggets leverantör.

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty" />Fel: gen. Rörelsebokföringsmallen måste ha ett värde i kund: 'YOUR SHOPIFY STORE'. Den kan inte vara noll eller tom

På sidan **Shopify butikskort**, fyll i fältet **Kod för kundmall** med den mall som har **Rörelsebokföringsmall** ifyllt. Kundmallen används för att skapa kunder och för att beräkna försäljningspriser på försäljningsdokument.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it" />Fel: Import av data till din Shopify butik har inte aktiverats. Gå till butikskortet för att aktivera det

På sidan **Shopify butikskort** aktivera växlingsknappen **Tillåt synkronisering till Shopify**. Denna inställning är avsedd att skydda onlinebutiken från att hämta demodata från [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="error-oauth-error-invalidrequest-could-not-find-shopify-api-application-with-apikey" />Fel: Oauth error invalid_request: Det gick inte att hitta Shopify API-programmet med api_key

Det verkar som du använder [bädda in appen](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), där klientens URL har formatet: `https://[application name].bc.dynamics.com`. Shopify anslutningen fungerar inte för inbäddade appar. För mer information, se [Vilka Microsoft-produkter är Shopify-anslutningen tillgängliga för?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx" />Fel: Internt fel. Det verkar som om ett fel har inträffat hos oss. Begärande-ID: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Kontakta Shopify-supporten inom sju dagar efter det här felet och ange begärande-ID. Om du vill veta mer går du till [Supportalternativ för Shopify](shopify-faq.md#shopify).

## <a name="see-also" />Se även

[Kom igång med kopplingen för Shopify](get-started.md)
