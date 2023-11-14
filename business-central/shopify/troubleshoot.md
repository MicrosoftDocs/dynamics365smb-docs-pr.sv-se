---
title: Felsöka synkroniseringen mellan Shopify och Business Central
description: Lår dig vad du ska göra om något går fel under synkroniseringen av data mellan Shopify och Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# Felsöka synkroniseringen mellan Shopify och Business Central

Det kan hända att du behöver felsöka problem när du synkroniserar data mellan Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)]. På den här sidan beskrivs åtgärder för att felsöka vanliga scenarier.

## Kör uppgifter i förgrund

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill felsöka och öppna sidan **Shopify-butikskort**.
3. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.

När synkroniseringsåtgärden utlöses körs numera uppgiften i förgrunden. Om ett fel inträffar visas en feldialogruta med länken **Kopiera Detaljer**. Använd den här länken om du vill kopiera information till en textredigerare för vidare analys.

## Loggar

Loggningsfunktionerna kan göra det enklare att identifiera varför ett fel inträffade. På sidan **Shopify-butikskort**, i fältet **Loggningsläge**, kan du ange den detaljnivå du vill överföra gällande fel. Fältet erbjuder följande alternativ:

- **Inaktiverat** – Logga inte information om fel.
- **Endast fel** – Logga endast felmeddelandet utan begäran/svar-paren. Denna inställning är den förvalda inställningen för nya butiker.
- **Alla** - Logga begäran/svarsparen för alla transaktioner, inklusive de som lyckades.

> [!NOTE]
> Kontinuerliga loggningsfel kan komma att göra [!INCLUDE [prod_short](../includes/prod_short.md)] långsammare. Du kan undvika detta genom att aktivera loggning när du har hittat ett fel i synkroniseringen. Du kan utlösa synkroniseringen manuellt igen och sedan granska loggen för att ta reda på vad som gick fel.

### Hantera loggpostsdata

För att hålla databasens storlek under kontroll ingår loggposter i en kvarhållningsprincip för data kallad **Shpfy Loggpost**. Med kvarhållandepolicyer kan du ange hur länge du vill lagra olika typer av data. Som standard sparas Shopify-loggposter i en månad. Mer information om kvarhållningsprinciper i [Definiera kvarhållningsprincip](../admin-data-retention-policies.md).

På sidan **Shopify-loggposter** kan du ta bort alla loggposter eller bara de poster som är äldre än sju dagar.

### Att granska loggar

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-loggposter** och väljer sedan relaterad länk.
2. Välj den berörda loggposten och öppna sidan **Shopify-loggpost**.
3. Kontrollera värden för begäran, statuskod och beskrivning och svar.

> [!TIP]
> Om du måste kontakta Shopify-supporten för att få hjälp med felsökning noterar du informationen i fältet **Begärande-ID**. Den informationen kan hjälpa till att lösa problemet snabbare.

Du kan hämta värdena för begäran och svar som filer i ett text format.

Överväg att stänga av loggningsfunktionen om du vill undvika inverkan på prestanda och din databas.

## Datainsamling

Oavsett om loggning är aktiverad eller inte loggas alltid vissa Shopify-svar. Du kan kontrollera eller hämta loggarna från sidan **Datainsamlingslista**.

Välj åtgärden **Hämtade Shopify-data** på en av följande sidor:

- **Shopify-order**
- **Shopify orderrad**
- **Shopify uppfyllelser**
- **Leveranskostnader för Shopify-order**
- **Shopify-ordertransaktioner**
- **Shopify retur**
- **Shopify returrad**
- **Shopify återbetalning**
- **Shopify återbetalningsrad**
- **Shopify-utbetalningar**
- **Shopify-betalningstransaktioner**
- **Shopify-transaktioner**

## Återställ synkronisering

För optimala prestanda importerar kopplingen endast kunder, produkter och order som har skapats eller ändrats sedan den senaste synkroniseringen. På sidan **Shopify-butikskortet** finns funktioner för att ändra datum och tid för den senaste synkroniseringen eller för att återställa den helt. Med den här funktionen ser du till att alla data synkroniseras och inte bara de ändringar som gjorts sedan den senaste synkroniseringen utfördes.

Den här funktionen kan endast användas för synkronisering från Shopify till [!INCLUDE[prod_short](../includes/prod_short.md)]. Den kan vara användbar om du behöver återställa borttagna data, såsom produkter, kunder eller borttagna order.

## Kräv åtkomsttoken

Om [!INCLUDE[prod_short](../includes/prod_short.md)] inte kan ansluta till ditt Shopify konto kan du prova att återställa åtkomsttoken från Shopify. Du kan behöva begära en ny token om ändringar gjorts i säkerhetsnycklar eller nödvändiga behörigheter (programomfattningarna).

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik som du vill hämta åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas att logga in på ditt Shopify-konto.

Växlingsknappen **Har AccessKey** är aktiverad.

## Kontrollera och aktivera behörigheter för att göra HTTP-begäranden i en miljö utan produktions miljön

Anslutningstillägget kräver Shopify behörighet att göra HTTP-begäranden för att det ska fungera korrekt. När du kör tester i en miljö för begränsat läge är HTTP-begäranden förbjudna för alla tillägg.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tilläggshantering** och väljer sedan relaterad länk.
2. Välj tillägget **Shopify Connector**.
3. På sidan **Konfigurera** väljer du åtgärden **Tilläggsinställningar**.
4. Kontrollera att växlingsknappen **Tillåt HTTPClient-begäranden** är aktiverat.

## Rotera Shopify åtkomsttoken

I följande procedurer beskrivs hur du roterar den åtkomsttoken som används av Shopify Connector för att komma åt din Shopify onlinebutik.

### I Shopify

1. Gå till **Shopify administratör** i din [appar](https://www.shopify.com/admin/apps).
2. Välj **Ta bort** i raden med **Dynamics 365 Business Central**-appen.
3. Välj **Ta bort** i meddelandet.

### I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butiker** och väljer sedan relaterad länk.
2. Välj den butik som du vill rotera åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas till det, loggar du in på ditt Shopify-konto, granskar sekretess och behörigheter och trycker sedan på knappen **Installera app**.

## Kända problem

### Fel: försäljningshuvudet finns inte. Identifieringsfält och värden: dokumenttyp='Quote',No.='YOUR SHOPIFY STORE'

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

### Fel: gen. Rörelsebokföringsmallen måste ha ett värde i kund: 'YOUR SHOPIFY STORE'. Den kan inte vara noll eller tom

På sidan **Shopify butikskort**, fyll i fältet **Kod för kundmall** med den mall som har **Rörelsebokföringsmall** ifyllt. Kundmallen används för att skapa kunder och för att beräkna försäljningspriser på försäljningsdokument.

### Fel: Import av data till din Shopify butik har inte aktiverats. Gå till butikskortet för att aktivera det

På sidan **Shopify butikskort** aktivera växlingsknappen **Tillåt synkronisering till Shopify**. Denna inställning är avsedd att skydda onlinebutiken från att hämta demodata från [!INCLUDE[prod_short](../includes/prod_short.md)].

### Fel: Oauth error invalid_request: Det gick inte att hitta Shopify API-programmet med api_key

Det verkar som du använder [bädda in appen](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), där klientens URL har formatet: `https://[application name].bc.dynamics.com`. Shopify anslutningen fungerar inte för inbäddade appar. För mer information, se [Vilka Microsoft-produkter är Shopify-anslutningen tillgängliga för?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Fel: Internt fel. Det verkar som om ett fel har inträffat hos oss. Begärande-ID: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Kontakta Shopify-supporten inom sju dagar efter detta felet uppstått och ange begärande-ID. Om du vill veta mer går du till [Supportalternativ för Shopify](shopify-faq.md#shopify).

### Fel: Oauth-fel invalid_request: Ditt konto har inte behörighet att bevilja den begärda åtkomsten för den här appen. 

Det verkar som om användare som begär åtkomst inte har rättigheter att hantera appar (möjlighet att hantera och installera appar och kanaler, samt eventuellt godkänna appavgifter). Du kanske kan lösa problemet genom att installera appen som kontoägare. Du kan också kontrollera **Appbehörigheten** för användaren i inställningarna [**Användare och behörigheter**](https://www.shopify.com/admin/settings/account) i din **Shopify administratören**.  

### [{"meddelande":"Åtkomst nekad för fältet FÄLT.","platser":[{"rad":0,"kolumn":0}],"sökväg":["sökväg"],"tillägg":{"kod":"ÅTKOMST_NEKAD","dokumentation":https://shopify.dev/api/usage/access-scopes}}]

Begär en ny token eftersom den uppdaterade versionen av anslutningsprogrammet kräver fler behörigheter (programomfattningar). För mer information gå till to [Begäran om åtkomsttoken](#request-the-access-token).

## Se även

[Kom igång med kopplingen för Shopify](get-started.md)
