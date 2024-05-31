---
title: Analyser av anläggningstillgångar
description: 'Lär dig hur du samlar in, analyserar och delar data om anläggningstillgångar för Business Intelligence.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analyser av anläggningstillgångar

Företag med anläggningstillgångar samlar in mycket data om dem under den dagliga verksamheten. Denna data stöder värdefull Business Intelligence (BI) för de som hanterar anläggningstillgångar:

- Anskaffningar av tillgångar
- Avskrivning av tillgångar
- Försäkring och underhåll
- Budgetar för tillgångar

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller många funktioner som hjälper dig att samla in, analysera och dela data om organisationens anläggningstillgångar:

- Ekonomisk rapportering (för finansiella rapporter och KPI:er för konton för anläggningstillgångar)
- Ad hoc-analys på listor
- Ad-hoc-analys av data i Excel (med öppna i Excel)
- Inbyggda analysverktyg för anläggningstillgångar
- Inbyggda rapporter om anläggningstillgångar

> [!NOTE]
> Analyser för anläggningstillgångar är lite annorlunda än andra områden. Du måste analysera data som redan finns, till exempel tillgångsförvärv, avskrivning och försäkring, men även data om framtida (projicerade) data, till exempel avskrivningar och tillbakadragna tillgångar. För den senare typen av analys,har [!INCLUDE[prod_short](includes/prod_short.md)] inbyggda rapporter som kan beräkna dessa siffror.

Varje funktion har sina fördelar och nackdelar, beroende på typ av dataanalys och användarens roll. För mer informations, se [Översikt över analys, Business Intelligence och rapportering](reports-bi-reporting.md).

I den här artikeln beskrivs hur du använder de här analysfunktionerna för att få insikter om anläggningstillgångarna.

## Analysbehov inom tillgångshantering

När du tänker på analysbehoven vid i tillgångshantering att använda en personbaserad modell som beskriver deras analysbehov på hög nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration av olika profiler för analys" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

När det gäller data har människor i olika roller olika behov och de använder data på olika sätt. Till exempel interagerar personer inom kapitalförvaltning och ekonomi med data på ett annat sätt än personer inom försäljning.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration av hur olika profiler har olika analysbehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Roll              | Dataaggregering  | Vanliga sätt att använda data                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO/COO/VD                 | Prestandadata  | KPI:er <br> Instrumentpaneler <br> Ekonomiska rapporter           |
|Tillgångshantering/kontrollant   | Trender, sammanfattningar | Inbyggda ledningsrapporter <br> Ad hoc-analys      | 
|Bokföringsansvarig                      | Detaljerad data     | Inbyggda operativa rapporter <br> Uppgiftsdata på skärmen |

## KPI:er för tillgångshantering

En KPI (Key Performance Indicator) är ett mätbart värde som visar hur effektivt du uppfyller dina mål. Inom tillgångshantering använder människor ofta följande nyckeltal för att övervaka deras organisations användning av tillgångar:

- Omsättning i förhållande till tillgångarna
- Avkastning på tillgångar

## Använd ekonomisk rapportering för att göra finansiella rapporter och KPI:er relaterad till anläggningstillgångar

Funktionen **Ekonomiska rapporter** ger dig insikter i ekonomiska data som visas på din kontoplan. Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. När det gäller tillgångshantering kan du skapa ekonomiska rapporter på de redovisningskonton som du använder för att spåra bokföring av anläggningstillgångar.

Dimensioner spelar en viktig roll i Business Intelligence. En dimension är data som du kan lägga till en transaktion som en parameter. Med dimensioner kan du gruppera transaktioner med liknande egenskaper, till exempel kunder, produkter och säljare, och enkelt hämta dessa grupper för analys. Bland annat kan du använda dimensioner när du definierar analysvyer och när du skapar ekonomiska rapporter. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

Läs mer om ekonomiska rapporter i [Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md).

## Ekonomisk rapportering över affärsenheter eller juridiska personer (relaterat till anläggningstillgångar)

Vissa organisationer använder [!INCLUDE [prod_short](includes/prod_short.md)] i flera affärsenheter eller juridiska enheter. Andra använder [!INCLUDE [prod_short](includes/prod_short.md)] i dotterbolag som rapporterar till överordnade organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] ger revisorer verktyg som hjälper dem att överföra redovisningstransaktioner från två eller flera företag (dotterbolag) till ett konsoliderat företag. Särskilt för tillgångshantering kanske du vill konsolidera redovisningstransaktioner för dina anläggningstillgångskonton för att kunna spåra anläggningstillgångs-KPI:er över affärsenheter eller juridiska personer.

Mer information finns i [Företagskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analys av data för anläggningstillgångar

Ibland behöver du bara kontrollera om siffrorna lägger till korrekt eller snabbt bekräfta en siffra. Följande funktioner är bra för ad hoc-analyser:

- Dataanalys för huvudbokens listsidor
- Öppna i Excel

Med funktionen Dataanalys kan du öppna nästan alla listsidor, till exempel sidor för **Redovisningstransaktioner** eller **Anläggningstillgångstransaktionerna**, ange analysläge och sedan Gruppera, Filtrera och Pivotera data efter önskemål.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Exempel på hur du gör dataanalyser på sidan redovisning för anläggningstillgångar för att se tillgångens värde." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

På samma sätt kan du använda åtgärden **Öppna i Excel** för att öppna en listsida för transaktioner, eventuellt filtrera listan till en delmängd av data och sedan använda Excel för att arbeta med data. Du kan till exempel använda funktioner som Analysera data, What-If-analys eller Prognosblad.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Om du konfigurerar OneDrive för systemfunktioner öppnas Excel-arbetsboken i webbläsaren med hjälp av Excel för webben. 

Mer information om hur du gör ad hoc-analyser av redovisning av anläggningstillgångar finns i [Ad hoc-analys av data för anläggningstillgångar](ad-hoc-analysis-fa.md).


## Inbyggda rapporter för anläggningstillgångar

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller flera inbyggda rapporter, spårningsfunktioner och verktyg som hjälper revisorer eller controllers som redovisar anläggningstillgångar.

Om du vill ha en översikt över tillgängliga rapporter väljer du **Alla rapporter** i den övre rutan på startsidan. Denna åtgärd öppnar sidan Rollutforskaren, som är filtrerad efter funktionerna i alternativet **Rapport och analys**. Om du vill söka efter rapporter relaterade anläggningstillgångar anger du **Sök** i fältet **Sök**. Läs mer i [Söka efter rapporter med Rollutforskaren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Exempel på rapporter om rollcentret Ekonomi." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Mer information om rapporter som är relevanta för anläggningstillgångar finns i [Inbyggda anläggningstillgångsrapporter](fa-reports.md).

## Analyser för anläggningstillgångar

[!INCLUDE [prod_short](includes/prod_short.md)] har flera sidor som ger dig översikt över anläggningstillgångar och uppgifter att göra. Här är några exempel på hur du kan komma igång:

- [Beräkna avskrivningar, bokföra avskrivningar och analysera avskrivningar.](fa-how-depreciate-amortize.md)
- [Övervaka underhållskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Bevaka försäkringsskydd](fa-how-insure.md#to-monitor-insurance-coverage)
- [Visa ändrade värden för avskrivningsregler](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Visa avyttringstransaktioner](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Visa planerade avyttringsvärden](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### Visa redovisningstransaktioner för anläggningstillgångar och saldon från sidan Kontoplan

På sidan Kontoplan visas alla redovisningskonton med aggregerade siffror i redovisningen. Från den här sidan kan du göra saker som:  

- Visa rapporter som visar transaktioner och saldon.  
- Granska en lista med bokföringsmallar för det kontot.
- Visa separata debet- och kreditsaldon för ett enskilt konto.

För anläggningstillgångar kan du skapa en vy på sidan Kontoplan som bara visar tillgångskonton, eller kanske bara de tillgångskonton du använder för att bokföra anläggningstillgångar.

:::image type="content" source="media/chart-of-accounts-page-fa.png" alt-text="Exempel på hur sidan Kontoplan visar ekonomiska insikter" lightbox="media/chart-of-accounts-page-fa.png":::

För mer information, gå till [Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Analysera data efter dimensioner (relaterade till anläggningstillgångar)

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis journaler för anläggningstillgångar. Dimensioner kan till exempel indikera avdelningen eller platsen en post kom från.  

I stället för att skapa separata redovisningskonton för varje avdelning eller plats kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad struktur för kontoplan.

Läs mer i [Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)

## Se även

[Hantera ekonomisk rapportering mellan affärsenheter eller juridiska personer](finance-consolidated-company-reporting.md)  
[Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)  
[Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Ad hoc-analys av data för anläggningstillgångar](ad-hoc-analysis-fa.md)   
[Inbyggda rapporter om anläggningstillgångar](fa-reports.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
