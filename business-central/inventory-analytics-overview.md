---
title: Lageranalys
description: Business Central innehåller många funktioner som hjälper dig att samla in och dela värdefull data om ditt lager för business intelligence och beslutsfattande inom organisationen.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Lageranalys

Företag samlar in massor av data under dagliga aktiviteter som stödjer business intelligence (BI) för lagerchefer:

- Leverans av varor när försäljningsorder är uppfyllda.
- Inleveranser av artiklar när inköpsorder är uppfyllda.
- Flytta artiklar mellan lagerställen.

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller många funktioner som hjälper dig att samla in, analysera och dela organisationens lagerdata:

- Ad hoc-analys på listor
- Ad-hoc-analys av data i Excel (med öppna i Excel)
- Inbyggda lageranalysverktyg
- Inbyggda lagerrapporter

Var och en av dessa funktioner har sina fördelar och nackdelar, beroende på typ av dataanalys och användarens roll. För mer informations, se [Översikt över analys, Business Intelligence och rapportering](reports-bi-reporting.md).

Den här artikeln beskriver hur du kan använda dessa analysfunktioner för ditt lager.

## Analysbehov inom lager

När du tänker på analysbehoven vid i lagerhantering att använda en personbaserad modell som beskriver olika analysbehov på hög nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration av olika profiler för analys" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Människor i olika roller har olika behov när det gäller data och de använder data på olika sätt. Till exempel interagerar personer inom kapitalförvaltning och ekonomi med data på ett annat sätt än personer inom försäljning.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration av hur olika profiler har olika analysbehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Roll              | Dataaggregering  | Vanliga sätt att använda data                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO/CFO/VD    | Prestandadata  | KPI:er, instrumentpaneler, ekonomiska rapporter           |
|Lagerchef  | Trender, sammanfattningar | Inbyggda ledningsrapporter, ad hoc-analys      | 
|Lagerarbetare   | Detaljerad data     | Inbyggda driftrapporter, uppgiftsdata på skärmen |

<!-- 
## Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Använd ekonomisk rapportering för att göra finansiella rapporter och KPI:er relaterade till lager

Funktionen **Ekonomiska rapporter** ger dig insikter i ekonomiska data som visas på din kontoplan. Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. När det gäller lagerhantering kan du skapa ekonomiska rapporter på de redovisningskonton som du använder för att spåra bokföring av lager.

Dimensioner spelar en viktig roll i Business Intelligence. En dimension är data som du lägger till i en transaktion som en parameter. Med dimensioner kan du gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare. Bland annat kan använder du dimensioner när du definierar analysvyer och när du skapar ekonomiska rapporter. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

Läs mer om ekonomiska rapporter i [Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md).

## Ekonomisk rapportering över affärsenheter eller juridiska personer (relaterat till lager)

Vissa organisationer använder [!INCLUDE [prod_short](includes/prod_short.md)] i flera affärsenheter eller juridiska enheter. Andra använder [!INCLUDE [prod_short](includes/prod_short.md)] i dotterbolag som rapporterar till överordnade organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] ger revisorer verktyg som hjälper dem att överföra redovisningstransaktioner från två eller flera företag (dotterbolag) till ett konsoliderat företag. Särskilt för lagerhantering kanske du vill konsolidera redovisningstransaktioner för dina lagerkonton för att kunna spåra försäljnings-KPI:er över affärsenheter eller juridiska personer.

Mer information finns i [Företagskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analys av lagerdata

Ibland behöver du bara kontrollera om siffrorna lägger till korrekt eller snabbt bekräfta en siffra. Följande funktioner är bra för ad hoc-analyser:

- Dataanalys för huvudbokens listsidor
- Öppna i Excel

Med funktionen Dataanalys kan du öppna nästan alla listsidor, till exempel sidor för **Artikeltransaktioner**, ange analysläge och sedan gruppera, filtrera och pivotera data efter önskemål.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Exempel på hur du gör dataanalyser av gammalt lager på sidan Artikeltransaktioner." lightbox="media/data-analysis-inventory-dead-stock.png":::

På samma sätt kan du använda åtgärden **Öppna i Excel** för att öppna en listsida, eventuellt filtrera listan till en delmängd av data och sedan använda Excel för att arbeta med data. Du kan till exempel använda funktioner som Analysera data, What-If-analys eller Prognosblad.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Om du konfigurerar OneDrive för systemfunktioner öppnas Excel-arbetsboken i webbläsaren.

Mer information om hur du gör ad hoc-analyser av lagerdata finns i [Ad hoc-analys av lagerdata](ad-hoc-analysis-inventory.md).

## Inbyggda rapporter för lager

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller flera inbyggda rapporter, spårningsfunktioner och verktyg som hjälper lagerorganisationer att rapportera om sina data.

Om du vill ha en översikt över tillgängliga rapporter väljer du **Alla rapporter** på startsidan. Denna åtgärd öppnar rapportutforskaren, som är filtrerad efter funktionerna i alternativet **Rapport och analys**. Under rubriken **Försäljning och marknadsföring** välj **Utforska**. Läs mer i [Söka efter rapporter med Rollutforskaren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Exempel på rapporter om rollcentret för försäljning." lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Mer information om rapporter som är relevanta för lager finns i [Inbyggda lager- och lagerställerapporter](inventory-WMS-reports.md).

## Lageranalys på skärmen

[!INCLUDE [prod_short](includes/prod_short.md)] har flera sidor som ger dig lageröversikter och uppgifter att göra. Här är några exempel på hur du kan komma igång:

- [Visa artikeldisposition](inventory-how-availability-overview.md)
- [Spåra artiklar med serie-, parti- eller paketnummer](inventory-how-work-item-tracking.md)
- [Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)
- [Granska avstämningen mellan inventeringen och redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Visa direktutlevererade artiklar i utleveranser eller plockningsförslag](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Försäljningsmodulen innehåller även analyssidor relaterade till lager:

- [Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)
- [Beräkning av leveransdatum för försäljningsorder](sales-date-calculation-for-sales.md)
- [Spåra paket](sales-how-track-packages.md)

### Visa lagersrelaterade redovisningstransaktioner och saldon från sidan Kontoplan

På sidan **Kontoplan** visas alla redovisningskonton med aggregerade siffror på det som bokförs i redovisningen. Från den här sidan kan du göra saker som:  

- Visa rapporter som visar transaktioner och saldon.  
- Granska en lista med bokföringsmallar för det kontot.
- Visa separata debet- och kreditsaldon för ett enskilt konto.

För lagerhantering kan du skapa en vy på sidan Kontoplan som bara visar de konton som du använder för att bokföra lagertransaktioner.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Exempel på hur sidan Kontoplan visar ekonomiska insikter" lightbox="media/chart-of-accounts-page.png":::

För mer information, gå till [Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Analysera lagerdata efter dimensioner

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis försäljningsorder. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

I stället för att skapa separata redovisningskonton för varje avdelning eller plats kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad struktur för kontoplan.

Läs mer i [Analysera data efter dimensioner](bi-how-analyze-data-dimension.md).

## Se även

[Företagskonsolidering](finance-consolidated-company-reporting.md)   
[Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)  
[Hantera ekonomisk rapportering mellan affärsenheter eller juridiska personer](finance-consolidated-company-reporting.md)  
[Ad hoc-analys av lagerdata](ad-hoc-analysis-inventory.md)  
[Inbyggt lager och distributionslagerrapporter](inventory-WMS-reports.md)  
[Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)   
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
