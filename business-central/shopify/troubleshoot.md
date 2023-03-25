---
title: Felsöka synkroniseringen mellan Shopify och Business Central
description: Lår dig vad du ska göra om något går fel under synkroniseringen av data mellan Shopify och Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Felsöka synkroniseringen mellan Shopify och Business Central

Det kan hända att du behöver felsöka problem när du synkroniserar data mellan Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)]. På den här sidan beskrivs åtgärder för att felsöka vanliga scenarier som kan uppstå.

## Loggar

Om en synkroniseringsuppgift misslyckas kan du aktivera loggning genom att aktivera reglaget **Aktivera logg** på sidan **Shopify-butikskortet**. Du kan sedan utlösa synkroniseringsuppgift och granska loggar manuellt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-loggposter** och väljer sedan relaterad länk.
2. Välj den berörda loggposten och öppna sidan **Shopify-loggpost**.
3. Kontrollera värden för begäran, statuskod och beskrivning och svar.

Glöm inte att inaktivera loggning för att undvika negativ inverkan på prestanda och öka databasstorleken.

Från sidan **Shopify-loggposter** kan du utlösa borttagning av alla loggposter eller de som är äldre än sju dagar.

## Datainsamling

Oavsett inställningar för **Logg aktiverad** loggas alltid vissa svar från Shopify, som du kan inspektera eller ladda ner från sidan **Datainsamlingslista**.

Välj åtgärden **Hämtade Shopify-data** på en av följande sidor:

- **Shopify-order**
- **Shopify-orderuppfyllelse**
- **Leveranskostnader för Shopify-order**
- **Shopify-ordertransaktioner**
- **Shopify-utbetalningar**
- **Shopify-betalningstransaktioner**
- **Shopify-transaktioner**

## Återställ synkronisering

För optimala prestanda importerar kopplingen endast kunder, produkter och ordrar som har skapats eller ändrats sedan den senaste synkroniseringen. På sidan **Shopify-butikskortet** finns funktioner för att ändra datum och tid för den senaste synkroniseringen eller för att återställa den helt. Med den här funktionen ser du till att alla data synkroniseras och inte bara de ändringar som gjorts sedan den senaste synkroniseringen utfördes.

Den här funktionen kan endast användas för synkronisering från Shopify till [!INCLUDE[prod_short](../includes/prod_short.md)]. Den kan vara användbar om du behöver återställa borttagna data, såsom produkter, kunder eller borttagna ordrar.

## Kräv åtkomsttoken

Om [!INCLUDE[prod_short](../includes/prod_short.md)] inte kan ansluta till ditt Shopify konto kan du prova att återställa åtkomsttoken från Shopify. Denna begäran kan behövas om det finns en rotation för säkerhetsnycklar eller ändringar i begärda behörigheter (omfattningar).

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik som du vill hämta åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas att logga in på ditt Shopify-konto.

Växlas **Har AccessKey** kommer att aktiveras.

### Kontrol lera och aktivera behörigheter för att göra HTTP-begäranden när de körs i en miljö utan produktions miljön

Anslutnings tillägget kräver Shopify behörighet att göra HTTP-begäranden för att det ska fungera korrekt. Vid testning i en miljö för begränsat läge är HTTP-begäranden förbjudna för alla tillägg.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Tilläggshantering** och väljer sedan relaterad länk.
2. Välj tillägget **Shopify anslutningsprogram**.
3. På sidan **Konfigurera** väljer du åtgärden **Tilläggsinställningar**.
4. Kontrollera att växlingsknappen **Tillåt HTTPClient-begäranden** är aktiverat.

## Rotera Shopify åtkomsttoken

I följande procedurer beskrivs hur du roterar den åtkomsttoken som används av Shopify Connector för att komma åt din Shopify onlinebutik.

### I Shopify

1. Gå till **Shopify administratör** i din [appar](https://www.shopify.com/admin/apps).
2. Välj **Ta bort** i raden med **Dynamics 365 Business Central**-appen.
3. Välj **Ta bort** i meddelandet.

### I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik som du vill rotera åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas till det, loggar du in på ditt Shopify-konto, granskar sekretess och behörigheter och trycker sedan på knappen **Installera app**.

## Kända problem

### *Rörelsebokföringsmall* kan inte vara noll eller tom. Det måste finnas ett värde i fältet kund

På sidan **Shopify butikskort**, fyll i fältet **Kod för kundmall** med den mall som har **Rörelsebokföringsmall** ifyllt. Kundmallen används inte bara för att skapa kunder, utan även för beräkning av försäljningspris och när försäljningsdokument skapas.

### Import av data till din Shopify butik har inte aktiverats. Gå till butikskortet för att aktivera det

I fönstret **Shopify butikskort** aktivera växlingsknappen **Tillåt synkronisering till Shopify**. Denna växlingsknapp är avsedd att skydda onlinebutiken från att hämta demodata från [!INCLUDE[prod_short](../includes/prod_short.md)].

### Oauth fel invalid_request: det gick inte att hitta Shopify API-programmet med api_key

Det verkar som du använder [bädda in appen](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), där klientens URL har formatet: `https://[application name].bc.dynamics.com`. Shopify anslutningen fungerar inte för inbäddade appar. För mer information, se [Vilka Microsoft-produkter är Shopify-anslutningen tillgängliga för](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## Se även

[Kom igång med kopplingen för Shopify](get-started.md)
