---
title: Analys vid inköp
description: Business Central innehåller många funktioner som hjälper dig att samla in och dela värdefull försäljningsdata för business intelligence och beslutsfattande inom inköpsorganisationen.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analys vid inköp

Företag samlar in massor av data under dagliga aktiviteter som stödjer business intelligence (BI) för inköpschefer:

- Inköpsofferter
- Inköpsorder
- Inköpsfakturor

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller många funktioner som hjälper dig att samla in, analysera och dela organisationens inköpsdata:

- Ad hoc-analys på listor
- Ad-hoc-analys av data i Excel (med öppna i Excel)
- Inbyggda försäljningsrapporter

Var och en av dessa funktioner har fördelar och nackdelar, beroende på typ av dataanalys och användarens roll. För mer informations, se [Översikt över analys, Business Intelligence och rapportering](reports-bi-reporting.md).

Den här artikeln beskriver hur du kan använda dessa analysfunktioner för att få köpinsikter.

## Analysbehov inom inköp

När du tänker på analysbehoven vid inköp kan det hjälpa att använda en personbaserad modell som beskriver olika analysbehov på hög nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration av olika profiler för analys" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Människor i olika roller har olika behov när det gäller data och de använder data på olika sätt. Till exempel interagerar personer inom kapitalförvaltning och ekonomi med data på ett annat sätt än personer inom försäljning.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration av hur olika profiler har olika analysbehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Roll              | Dataaggregering  | Vanliga sätt att använda data                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO/CSO/CFO/CEO    | Prestandadata  | KPI:er <br> Instrumentpaneler <br> Ekonomiska rapporter           |
|Inköpschef      | Trender, sammanfattningar | Inbyggda ledningsrapporter <br> Ad hoc-analys      | 
|Inköpsansvarig/Inköpsagent | Detaljerad data     | Inbyggda operativa rapporter <br> Uppgiftsdata på skärmen |

<!-- 
## Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## Använd ekonomisk rapportering för att göra finansiella rapporter och KPI:er (relaterad till inköp)

Funktionen **Ekonomiska rapporter** ger dig insikter i ekonomiska data som visas på din kontoplan. Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. När det gäller inköp kan du skapa ekonomiska rapporter på de redovisningskonton som du använder för att spåra inköpsbokföringar.

Dimensioner spelar en viktig roll i Business Intelligence. En dimension är data som du kan lägga till en transaktion som en parameter. Med dimensioner kan du gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner och produkter och enkelt hämta dessa grupper för analys. Bland annat kan använder du dimensioner när du definierar analysvyer och när du skapar ekonomiska rapporter. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

Läs mer om ekonomiska rapporter i [Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md).

## Ekonomisk rapportering över affärsenheter eller juridiska personer (relaterat till inköp)

Vissa organisationer använder [!INCLUDE [prod_short](includes/prod_short.md)] i flera affärsenheter eller juridiska enheter. Andra använder [!INCLUDE [prod_short](includes/prod_short.md)] i dotterbolag som rapporterar till överordnade organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] ger revisorer verktyg som hjälper dem att överföra redovisningstransaktioner från två eller flera företag (dotterbolag) till ett konsoliderat företag. Särskilt för inköpshantering kanske du vill konsolidera redovisningstransaktioner för dina inköpskonton för att spåra försäljnings-KPI:er över affärsenheter eller juridiska personer.

Mer information finns i [Företagskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analys av inköpsdata

Ibland behöver du bara kontrollera om siffrorna lägger till korrekt eller snabbt bekräfta en siffra. Följande funktioner är bra för ad hoc-analyser:

- Dataanalys för huvudbokens listsidor
- Öppna i Excel

Med funktionen **Dataanalys** kan du öppna nästan alla listsidor, till exempel **Inköpsorder**, **Bokförda inköpsfakturor**, **Leverantörstransaktioner** eller **Redovisningstransaktioner**, ange analysläge och sedan Gruppera, Filtrera och Pivotera data efter önskemål.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Exempel på hur du gör dataanalyser på sidan Redovisningstransaktioner." lightbox="media/data-analysis-vendor-ledger-entries.png":::

På samma sätt kan du använda åtgärden **Öppna i Excel** för att öppna en listsida, filtrera listan till en delmängd av data och sedan använda Excel för att arbeta med data. Du kan till exempel använda funktioner som Analysera data, What-If-analys eller Prognosblad.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Exempel på hur du gör dataanalyser på Redovisningstransaktioner med hjälp av Excel." lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Om du konfigurerar OneDrive för systemfunktioner öppnas Excel-arbetsboken i webbläsaren.

Mer information om hur du gör ad hoc-analyser av inköpsdata finns i [Ad hoc-analys av inköpsdata](ad-hoc-analysis-purchasing.md).

## Inbyggda rapporter för inköp

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller flera inbyggda rapporter, spårningsfunktioner och verktyg som hjälper inköpsorganisationer att rapportera om sina data.

Om du vill ha en översikt över tillgängliga rapporter väljer du **Alla rapporter** i den övre rutan på startsidan. Denna åtgärd öppnar rollutforskaren, som är filtrerad efter funktionerna i alternativet **Rapport och analys**. Läs mer i [Söka efter rapporter med Rollutforskaren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Exempel på rapporter om rollcentret XXX." lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Mer information om rapporter som är relevanta för inköp finns i [Inbyggda inköpsrapporter](purchase-reports.md).

## Inköpsanalys på skärmen

[!INCLUDE [prod_short](includes/prod_short.md)] har flera sidor som ger dig inköpsöversikter och uppgifter att göra. Här är ett exempel på hur du kan komma igång:

- [Beräkna datum för inköp](purchasing-date-calculation-for-purchases.md)

### Visa inköpsrelaterade redovisningstransaktioner och saldon från sidan Kontoplan

På sidan Kontoplan visas alla redovisningskonton med aggregerade siffror på det som bokförs i redovisningen. Från den här sidan kan du göra saker som:  

- Visa rapporter som visar transaktioner och saldon.  
- Granska en lista med bokföringsmallar för det kontot.
- Visa separata debet- och kreditsaldon för ett enskilt konto.

För inköp kan du skapa en vy på sidan Kontoplan som bara visar de konton som du använder för att bokföra inköpstransaktioner.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Exempel på hur sidan Kontoplan visar ekonomiska insikter" lightbox="media/chart-of-accounts-page.png":::

För mer information, gå till [Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Analysera data efter dimensioner (relaterade till inköp)

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis inköpsorder. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

I stället för att skapa separata redovisningskonton för varje avdelning eller plats kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad struktur för kontoplan.

Läs mer i [Analysera data efter dimensioner](bi-how-analyze-data-dimension.md).

## Se även

[Företagskonsolidering](finance-consolidated-company-reporting.md)  
[Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)  
[Hantera ekonomisk rapportering mellan affärsenheter eller juridiska personer](finance-consolidated-company-reporting.md)  
[Ad hoc-analys av inköpsdata](ad-hoc-analysis-purchasing.md)  
[Inbyggda inköpsrapporter](purchase-reports.md)  
[Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]