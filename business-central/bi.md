---
title: Ekonomisk analys
description: 'Business Central hjälper dig att samla in, analysera och dela företagsdata för business intelligence.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ekonomisk analys

Företag samlar in en enorm mängd data under dagliga aktiviteter som stöder värdefull Business Intelligence (BI) för beslutsfattare:

- Försäljningssiffror
- Inköp
- Driftkostnader
- Löner
- Budgetar

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller många funktioner som hjälper dig att samla in, analysera och dela organisationens ekonomidata:

- Ekonomisk rapportering (för ekonomiska och KPI:er)
- Ad hoc-analys på listor
- Ad-hoc-analys av data i Excel (med öppna i Excel)
- Inbyggda ekonomiska rapporter

Var och en av dessa funktioner har sina egna fördelar och nackdelar, beroende på typ av dataanalys och användarens roll. För mer informations, se [Översikt över analys, Business Intelligence och rapportering](reports-bi-reporting.md).

Den här artikeln beskriver hur du kan använda dessa analysfunktioner för att ge ekonomiska insikter.

## Analysbehov inom ekonomi

När man tänker på analysbehov inom ekonomi kan det hjälpa att använda en mental modell baserad på profiler beskrivna på en övergripande nivå och deras olika analytiska behov.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration av olika profiler för analys" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Människor i olika roller har olika behov när det gäller data och de använder data på olika sätt. Människor inom ekonomi interagerar till exempel med data på ett annat sätt än de inom försäljning.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration av hur olika profiler har olika analysbehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Roll              | Dataaggregering  | Vanliga sätt att använda data                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO/VD          | Prestandadata  | KPI:er <br> Instrumentpaneler <br> Ekonomiska rapporter           |
|Ekonomihantering | Trender, sammanfattningar | Inbyggda ledningsrapporter <br> Ad hoc-analys      | 
|Bokföringsansvarig         | Detaljerad data     | Inbyggda operativa rapporter <br> Uppgiftsdata på skärmen |

## KPI:er för ekonomi

En KPI (Key Performance Indicator) är ett mätbart värde som visar hur effektivt du uppfyller dina mål. Inom ekonomi använder människor ofta följande KPI:er för att övervaka organisationens ekonomiska hälsa:

- Bruttovinstmarginal
- Nettovinstmarginal
- Rörelsekapital
- Kassalikviditet/balanslikviditet
- Finansiell hävstång, även känd som multiplikator för eget kapital
- Skuldsättningsgrad
- Omsättning i förhållande till tillgångarna
- Avkastning på eget kapital
- Avkastning på tillgångar

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Använda ekonomisk rapportering för att göra finansiella rapporter och KPI:er

Funktionen **Ekonomiska rapporter** ger dig insikter i ekonomiska data som visas på din kontoplan. Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. Resultaten visas i diagram och rapporter på startsidan, till exempel diagram för kassaflöde och resultaträknings- och balansräkningsrapporter.

Dimensioner spelar en viktig roll i Business Intelligence. En dimension är data som du kan lägga till en transaktion som en parameter. Med hjälp av dimensioner kan du gruppera poster med liknande egenskaper så att de blir enklare att analysera. Till exempel kunder, regioner, produkter och säljare. Bland annat kan använder du dimensioner när du definierar analysvyer och när du skapar ekonomiska rapporter. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

> [!TIP]
> Som ett snabbt sätt att analysera transaktionsdata kan du filtrera summorna i kontoplanen och alla posterna på sidor för **Transaktioner** per dimension. Sök efter åtgärden **Ange dimensionsfilter**.  

I följande tabell beskrivs en serie uppgifter i ekonomiska rapporter med länkar till de artiklar där de beskrivs.  

| Till | Gå till |
| --- | --- |
| Skapa nya ekonomiska rapporter för att ange finansiella rapporter för att rapportera eller för att visa som diagram.| [Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)|
| Använda statistiska konton för att komplettera information i ekonomiska rapporter. Med statistiska konton kan du lägga till mått som bygger på icke-transaktionella data. Du kan lägga till icke-transaktionsrelaterade data som nummerbaserade enheter, till exempel personalstyrka, kvadratmeter eller antal kunder med förfallna konton. | [Analysera data med statistiska konton](bi-use-statistical-accounts.md) |
| Lär dig hur du ställer in en ny ekonomisk rapport med hjälp av exempel. | [Genomgång: Använda ekonomisk rapportering för att utföra kassaflödesprognoser](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analysera din ekonomiska kapacitet, genom att ställa in KPI:er baserat på ekonomiska rapporter, som du sedan publicerar som webbtjänster. De publicerade KPI:erna för ekonomiska rapporter kan visas på en webbplats eller importeras till Microsoft Excel med hjälp av OData-webbtjänster. |[Skapa och publicera KPI-webbtjänster som baseras på ekonomiska rapporter](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Skapa vyer för att analysera data med dimensioner.|[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)|
| skapa nya analysrapporter för försäljning, inköp och lager, och skapa analysmallar. |[Skapa analysrapporter](bi-how-create-analysis-views-reports.md)|

## Ekonomiska rapportering mellan affärsenheter eller juridiska personer

Vissa organisationer använder [!INCLUDE [prod_short](includes/prod_short.md)] i flera affärsenheter eller juridiska enheter. Andra använder [!INCLUDE [prod_short](includes/prod_short.md)] i dotterbolag som ska rapportera till överordnade organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] ger revisorer verktyg som hjälper dem att överföra redovisningstransaktioner från två eller flera företag (dotterbolag) till ett konsoliderat företag.  

Mer information finns i [Företagskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analys av ekonomiska data

Ibland behöver du bara kontrollera om siffrorna lägger till korrekt eller snabbt bekräfta en siffra. Följande funktioner är bra för ad hoc-analyser:

- Dataanalys för huvudbokens listsidor
- Öppna i Excel

Med funktionen Dataanalys kan du nästan öppna en listsida, till exempel Redovisningstransaktioner, Anläggningstillgångstransaktioner, Checktransaktioner eller Bankkontotransaktioner, gå in i analysläge och sedan Gruppera, Filtrera och Pivotera data efter önskemål.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Exempel på hur du gör dataanalyser på sidan Redovisningstransaktioner." lightbox="media/data-analysis-gl-entries.png":::

På samma sätt kan du använda åtgärden **Öppna i Excel** för att öppna en listsida för transaktioner, eventuellt filtrera listan till en delmängd av data och sedan använda Excel för att arbeta med data. Du kan till exempel använda funktioner som Analysera data, What-If-analys eller Prognosblad.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Exempel på hur du gör dataanalyser på Redovisningstransaktioner med hjälp av Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Om du konfigurerar OneDrive för systemfunktioner öppnas Excel-arbetsboken i webbläsaren med hjälp av Excel för webben. 


Mer information om hur du gör ad hoc-analyser av redovisningar finns i [Ad hoc-analys av ekonomiska data](ad-hoc-analysis-finance.md). 

## Inbyggda rapporter för ekonomi

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller flera inbyggda rapporter, spårningsfunktioner och verktyg som hjälper revisorer eller controllers som ansvarar för rapportering till ekonomiavdelningen.

Om du vill ha en översikt över tillgängliga rapporter väljer du **Alla rapporter** i den övre rutan på startsidan. Denna åtgärd öppnar rollutforskaren, som är filtrerad efter funktionerna i alternativet **Rapport och analys**. Läs mer i [Söka efter rapporter med Rollutforskaren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Exempel på rapporter om rollcentret Ekonomi." lightbox="media/report-explorer-finance.png":::

Inbyggda rapporter finns i två varianter:

- Designad för utskrift (pdf).
- Designad för analys i Excel.

Mer information finns i dessa översikter för rapporter som är relevanta för ekonomi.

- [Inbyggda Excel-rapporter för ekonomi](finance-analyze-excel.md)
- [Inbyggda viktiga ekonomiska rapporter](finance-reports.md)
- [Inbyggda rapporter om anläggningstillgångar](fa-reports.md)
- [Inbygga rapporter om kundfordringar](receivables-reports.md)
- [Inbygga rapporter om leverantörsskulder](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Uppgiftssidor för ekonomi på skärmen

[!INCLUDE [prod_short](includes/prod_short.md)] har flera sidor som ger dig ekonomiska översikter och uppgifter att göra.

### Visa redovisningstransaktioner och saldon från sidan Kontoplan

På sidan Kontoplan visas alla redovisningskonton med aggregerade siffror på det som bokförs i redovisningen. Från den här sidan kan du göra saker som:  

- Visa rapporter som visar transaktioner och saldon.  
- Granska en lista med bokföringsmallar för det kontot.
- Visa separatea debet- och kreditsaldon för ett enskilt konto.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Exempel på hur sidan Kontoplan visar ekonomiska insikter" lightbox="media/chart-of-accounts-page.png":::

För mer information, gå till [Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Visa faktiska belopp i jämförelse med budgeterade belopp för alla konton och för flera perioder

Som en del av att samla in, analysera och dela dina företagsdata, kan du visa faktiska belopp och budgeterade belopp för alla konton och för flera perioder. Du kan göra denna jämförelse på sidan **kontoplan** genom att välja åtgärden **Redovisningssaldo/Budget**.

För mer information, gå till [Analysera faktiska belopp kontra budgeterade belopp](bi-how-analyze-actual-versus-budget.md).

### Analysera data efter dimensioner

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis försäljningsorder. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

I stället för att skapa separata redovisningskonton för varje avdelning och projekt kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad struktur för kontoplan.

Inom ekonomisk analys är en dimension data som du lägger till en redovisningstransaktion som en sorts markör. Dessa data används för att gruppera redovisningstransaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare, och enkelt hämta dessa grupper för analys. Du kan använda dimensioner på transaktioner i journaler, dokument och budgetar. Mer information finns i [Analysera data efter dimension](bi-how-analyze-data-dimension.md)

### Analysera kassaflöden

På startsidan Revisor under **finansiell prestanda**, erbjuder diagrammen kontantcykel, kassaflöde, och inkomster och utgifter olika sätt att analysera kassaflöde:

- Granska siffrorna för en period med hjälp av skjutreglaget för tidslinje.
- Filtrera diagrammet genom att välja källan i förklaringen.
- Ändra längden på perioden, eller gå till föregående eller nästa period, genom att välja alternativ i listrutan finansiell prestanda.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Exempel på hur kassaflödesbilderna ser ut i rollcentret Revisor" lightbox="media/cashflow-accountant-rolecentre.png":::

Om du vill undersöka prognosen, förutom prognostransaktioner, kan du också titta på kassaflödeskalkylbladet. Du kan t.ex se hur prognosen:

- Hanterar bekräftade försäljningar och inköp.
- Subtraherar leverantörsreskontra och lägger till kundreskontra.
- Hoppar över dubbla försäljningsorder och inköpsorder.

För mer information, gå till [Analysera kassaflödet i företaget](finance-analyze-cash-flow.md).

## Se även

[Hantera ekonomisk rapportering mellan affärsenheter eller juridiska personer](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)  
[Ad hoc-analys av ekonomiska data](ad-hoc-analysis-finance.md)   
[Förstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Inbyggda ekonomiska Excel-rapporter](finance-analyze-excel.md)  
[Inbyggda viktiga ekonomiska rapporter](finance-reports.md)  
[Inbyggda rapporter om anläggningstillgångar](fa-reports.md)  
[Inbygga rapporter om kundfordringar](receivables-reports.md)  
[Inbygga rapporter om leverantörsskulder](payables-reports.md)  
[Översikt över ekonomi](finance.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)   
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
