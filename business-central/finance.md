---
title: Ekonomihantering (innehåller video)
description: 'Läs om hur Business Central stöder dina behov av ekonomisk förvaltning, redovisning, revision samt bokföring.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '1151, 1166, 9027, 9004'
ms.date: 02/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ekonomihantering

[!INCLUDE[prod_short](includes/prod_short.md)] inkluderar standardkonfigurationen för de flesta finansiella processer, men du kan ändra den så att den passar dina behov. Läs mer i [Ställa in finanser](finance-setup-finance.md).

Standardinställningkonfigurationen innehåller en kontoplan och standardbokföringsmallar som gör det effektivare att tilldela standardredovisningskonton till kunder, leverantörer och artiklar.  

Följande avsnitt beskriver en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

## Ta en videorundtur

I detta videoklipp beskrivs några av huvudfunktionerna för att hantera finanser. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

## Kom igång med ekonomifunktioner

Innan du kan börja driva ditt företag måste du ange hur du vill hantera företagets finansprocesser.

|Till...| Gå till |
|---|---|
| Ändra standardkonfigurationen för [!INCLUDE[prod_short](includes/prod_short.md)] för de flesta finansiella processer så att den passar dina behov. | [Ställa in Finance](finance-setup-finance.md) | 
| Läs om redovisningen och kontoplanen. |[Så här fungerar i redovisningen och kontoplanen](finance-general-ledger.md) |

## Bokföring

I det här avsnittet beskrivs några av de redovisningsverktyg som du använder för att registrera ekonomiska transaktioner så att de uppfyller dina krav på registrering, rapportering och chefsfinansiering.

| Till... | Gå till |
| --- | --- |
| Lägga till dimensioner för rikare business intelligence. |[Arbeta med dimensioner](finance-dimensions.md) |
|Lär dig använda ytterligare valutor och uppdatera valutakurser automatiskt. |[Uppdatera valutakurser](finance-how-update-currencies.md)|
| Allokera intäkter och kostnader till andra perioder än när transaktionerna faktiskt bokfördes. |[Periodisera intäkter och kostnader](finance-how-defer-revenue-expenses.md)|
|fördela en transaktion i en redovisningsjournal på olika konton när du bokför journalen. |[Fördela kostnader och intäkter](year-allocate-costs-income.md) |
| Tilldela extra kostnader, till exempel frakt- och fysisk hantering som förekommer vid handel med artiklar. På så sätt återspeglas kostnaden i lagervärdering. |[Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md) |
| Lär dig mer om tillgängliga alternativ för att automatiskt skicka prenumerationsfakturor till kunder och registrera återkommande intäkter. |[Arbeta med återkommande intäkter](finance-recurring-invoicing.md)|
|Bokföra kostnader för anställda för arbetsrelaterade aktiviteter och göra återbetalningar direkt till medarbetarbankkonton.|[Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)|

## Moms och skatter

Det är enkelt att arbeta med moms i [!INCLUDE[prod_short](includes/prod_short.md)] och du kan antingen använda en manuell eller automatisk inställning. I de här artiklarna finns information om hur du uppfyller lands-/regionspecifika bestämmelser.

| Till... | Gå till |
| --- | --- |
|Beräkna moms (VAT) för försäljnings- och inköpstransaktioner så att du kan rapportera beloppen till skattemyndigheterna.|[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)|
|Förbereda en rapport över moms från försäljning och skicka rapporten till en skattemyndighet inom Europeiska unionen (EU). | [Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)|
|Manuellt omvandla servicekontrakt för att ändra deras momssats.|[Omvandla servicekontrakt som innehåller momsbelopp](service-how-to-convert-service-contracts.md)|

## Hantera leverantörsreskontra och kundreskontra

Kärnan i finansiering centreras kring att hantera leverantörsreskontra och kundreskontra, registrera transaktioner, avstämma bankkonton, betala leverantörer, ta emot kundbetalningar, ersätta anställda för utlägg och så vidare. Det här avsnittet innehåller länkar till de grundläggande begreppen.

| Till... | Gå till |
| --- | --- |
| Koppla inkommande utbetalningar, stämma av bankkonton under betalningskoppling och kräva in utestående saldon. |[Hantera kundreskontra](receivables-manage-receivables.md) |
| Göra utbetalningar, koppla utgående betalningar och arbeta med checkar. |[Hantera Leverantörsreskontra](payables-manage-payables.md) |
|Be kunderna skicka betalning innan du levererar till dem eller skicka betalning till dina leverantörer innan de levererar till dig.|[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)|
| Stämma av och överföra pengar mellan bankkonton. |[Jämka bankkonton](bank-manage-bank-accounts.md) |

## Hantera flera företag

[!INCLUDE [prod_short](includes/prod_short.md)] ger små och medelstora företag en affärshanteringslösning som är lätt att använda och som upprätthålls till en låg ägandekostnad.

| Till... | Gå till |
| --- | --- |
|Ställa in koncerninterna partners och bearbeta transaktioner, manuellt eller automatiskt mellan juridiska personer inom samma företag.|[Hantera koncerninterna transaktioner](intercompany-manage.md)|
|Kombinera redovisningstransaktioner från flera företag i ett enda virtuellt konsoliderat företag för ekonomisk analys.|[Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md)|
| Samarbeta närmare med närstående företag som du har tillgång till och få information om KPI-data. | [Hantera arbete i flera företag med företagsnavet](company-hub.md)|

## Periodslutsrapportering och relaterade uppgifter

I slutet av varje bokföringsperiod eller i slutet av räkenskapsåret finns det ett antal administrativa uppgifter att utföra. Du vill till exempel se till att alla dokument och journaler är bokförda, se till att valutadata är uppdaterade, avsluta böckerna och så vidare. De faktiska uppgifterna beror på ditt företag.

| Till... | Gå till |
| --- | --- |
|Hantera lager- och produktionskostnader, och rapportera och stämma av kostnader med redovisningen.|[Hantera lagerkostnader](finance-manage-inventory-costs.md)|
| Importera löntransaktioner från ditt lönesystem till redovisningen. |[Importera lönetransaktioner](finance-how-import-payroll-transactions.md)|
|För mer information om hur du använder rollcentret Revisor, kontakta en extern revisor och använd företagsnavet för att hantera konton för flera klienter.|[Revisorlösningar i Business Central ](finance-accounting.md)| 

## Företagsledningens bokföring

Som Business Manager eller kontrollant är det viktigt att du kan förbereda och analysera de affärsdata du behöver för att fatta välgrundade beslut. Artiklarna i följande tabell hjälper dig att förbereda data. Mer information om analyser finns i [Business Intelligence och rapporteringsöversikt](reports-bi-reporting.md).

| Till... | Gå till |
| --- | --- |
|Analysera kostnaderna för att driva ditt företag genom att fördela faktiska budgeterade kostnader för drift, avdelningar, produkter och projekt till kostnadscenter.|[Redovisa kostnader](finance-manage-cost-accounting.md)|
| Övervaka kassaflödet till och från ditt företag. |[Analysera transaktioner i företaget](finance-analyze-cash-flow.md) |
|Följ en heltäckande process som beskriver hur du använder ekonomiska rapporter för att göra kassaflödesprognoser.|[Genomgång: Utföra kassaflödesprognoser genom att använda ekonomiska rapporter](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md)|
| Arbeta med finansiella rapporter och översikter i Microsoft Excel. |[Analysera finansiella rapporter i Excel](finance-analyze-excel.md) |

## Gratis e-inlärningsmoduler

Vill du lära dig mer om [!INCLUDE[prod_short](includes/prod_short.md)] i din egen takt? 

[!INCLUDE[footer-include](includes/footer-banner.md)]

## Se även

[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med modulen Försäljning](sales-manage-sales.md)  
[Arbeta med modulen Inköp](purchasing-manage-purchasing.md)  
[Stänga räkenskapsperioder](year-close-years-periods.md)  
[Hantera projekt](projects-manage-projects.md)  
[Importera data från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]