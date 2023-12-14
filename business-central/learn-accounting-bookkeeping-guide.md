---
title: Redovisning och bokföring
description: I den här artikeln finns information som hjälper dig att använda Microsoft  Dynamics 365 Business Central för att utföra redovisning och bokföring på företaget på rätt sätt.
author: altotovi
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, bookkeeping'
ms.search.form: '16, 39, 108'
ms.date: 03/14/2023
ms.author: altotovi
---

# <a name="accounting-and-bookkeeping"></a>Redovisning och bokföring

Redovisning är en viktig funktion i alla ERP-lösningar (Enterprise Resource Planning) och även i de flesta företag. Redovisning representerar processen att bokföra och katalogisera ett företags ekonomiska transaktioner och sedan hämta, mäta, summera och visa resultaten med hjälp av olika rapporter som ofta krävs enligt lokal lagstiftning. Det främsta målet med den här metoden är att hjälpa företagets ledning med att förstå affärsverksamhetens ekonomi och bedöma resultatet av företagets ekonomiska aktiviteter.

Bokföring är en del av redovisningsförfarandet och avser regelbundet bokföra alla finansiella transaktioner i ett företag. [!INCLUDE[prod_short](includes/prod_short.md)] är ett ERP-system som innehåller integrerade verktyg som gör det enklare att göra bokföringar i systemet. Många åtgärder kan göras automatiskt.

Den här artikeln innehåller en översikt över bokföringsprocesser, inklusive regler, procedurer och andra riktlinjer i [!INCLUDE[prod_short](includes/prod_short.md)]. Innehållet i den här artikeln syftar till att hjälpa revisorer och bokföringsansvariga att slutföra sitt dagliga arbete med detta ERP-system. Om du vill ha ytterligare hjälp, infogas en sammanhangsbaserad assistent i [!INCLUDE[prod_short](includes/prod_short.md)]. Den här assistenten innehåller länkar till information som är kopplad till den aktuella sidan och instruktioner för hur du arbetar med den aktuella åtgärden. För att få åtkomst väljer du knappen [**Hjälp**](product-help-and-support.md) i det övre högra hörnet för att öppna fönstret **Hjälp**. Använd sedan länkarna i avsnitten **Om denna uppgift eller sida** och **Relaterade resurser från Microsoft Learn**.

I följande videoklipp beskrivs några av huvudfunktionerna för redovisning och bokföring.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

I följande tabell beskrivs en serie uppgifter och ge länkar till de artiklar där de beskrivs.

| Uppgift | Artikel |
|------|---------|
| Visa eller redigera den lista med redovisningskonton som alla redovisningstransaktioner bokförs till. | [Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md) |
| Ange hur dina kunder ska betala dig och hur du ska betala dina leverantörer. | [Konfigurera betalningssätt:](finance-payment-methods.md) |
| Ange betalningsvillkor för att hantera förfallodatum och beräkna eventuella kassarabatter. | [Konfigurera betalningsvillkor](finance-payment-terms.md) |
| Ange bokföringsmallar mappar enheter som (t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument) till redovisningskonton. | [Konfigurera bokföringsmallar](finance-posting-groups.md)|
| Skapa ekonomiska rapporter och definiera kontokategorier som definierar innehållet i ekonomiska tabeller och rapporter, som rapporterna **Balansräkning** och **Resultaträkning**. | [Förbereda Financial Reporting med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)|
| Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet. | [Arbeta med betalningstoleranser och kassarabattstoleranser](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Ställa in räkenskapsperioder. | [Arbeta med bokföringsperioder och räkenskapsår](finance-accounting-periods-and-fiscal-years.md) |
| Ange fakturavillkor som påminner kunderna om att betala. | [Konfigurera villkor och nivåer för betalningspåminnelser](finance-setup-reminders.md)|
| Definiera hur du rapporterar belopp för moms som du har lagrat för försäljning till skattemyndigheterna. | [Konfigurera moms](finance-setup-vat.md) |
| Bestämma hur du kommer att hantera orealiserad moms i samband med kontantbaserade redovisningsmetoder. | [Konfigurera orealiserad moms för kontantbaserad redovisning](finance-setup-unrealized-vat.md) |
| Definiera utländska valutor som du gör handlar med eller rapporterar transaktioner i. | [Konfigurera valutor](finance-set-up-currencies.md) |
| Ange funktioner för försäljning och inköp till att hantera betalningar i utländsk valuta. | [Aktivera koppling av kundreskontratransaktioner till olika valutor](finance-how-enable-application-ledger-entries-different-currencies.md) |
| Definiera ett eller fler ytterligare belopp så att beloppen rapporteras automatiskt i både lokal valuta (BVA) och en ytterligare rapporteringsvaluta för varje redovisningstransaktion och för andra transaktioner. | [Konfigurera en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md) |
| Ändra med jämna mellanrum alternativa valutavärden för fluktuerande växelkurser. | [Uppdatera valutakurser](finance-how-update-currencies.md)|
| Definiera flera räntesatser för olika perioder relaterade till försenade betalningar i handelstransaktioner. | [Konfigurera flera räntesatser](finance-how-to-set-up-multiple-interest-rates.md) |
| Ordna så att belopp avrundas automatiskt när fakturor skapas. | [Konfigurera fakturaavrundning](finance-set-up-invoice-rounding.md) |
| Lägga till nya konton i den befintliga kontoplanen (COA). | [Ställa in kontoplanen](finance-setup-chart-accounts.md) |
| Ställa in business intelligence (BI)-diagram för att analysera betalningen. | [Ställa in analys för kassaflöde](finance-setup-cash-flow-analyses.md) |
| Gör det möjligt för kunder som inte är konfigurerade i systemet att faktureras. | [Konfigurera kontantkunder](finance-how-to-set-up-cash-customers.md) |
| Ställa in Intrastat-rapporten och skicka rapporten till en myndighet. | [Skapa och rapportera Intrastat](finance-how-setup-report-intrastat.md) |
| Se till att en journaltransaktion allokeras mellan olika konton, som kvantitet, procent eller belopp, när du bokför den i journalen. | [Använda fördelningsnycklar i redovisningsjournaler](ui-how-use-allocation-keys-general-journals.md) |
| Ställ in ursprungskoder och uppföljningskoder för att spåra granskningshistorik. | [Ställa in ursprungskoder och orsakskoder för granskningshistorik](finance-setup-trail-codes.md) |
| Ange standardrapporter som ska användas för olika dokumenttyper. | [Rapportval i Business Central](across-report-selections.md) |
| Koppla inkommande utbetalningar, stämma av bankkonton under betalningskoppling och kräva in utestående saldon. | [Hantera kundreskontra](receivables-manage-receivables.md) |
| Göra utbetalningar, koppla utgående betalningar och arbeta med checkar. | [Hantera Leverantörsreskontra](payables-manage-payables.md) |
| Be kunderna skicka betalning innan du levererar till dem eller skicka betalning till dina leverantörer innan de levererar till dig. | [Fakturera förskottsbetalningar](finance-invoice-prepayments.md) |
| Stämma av och överföra pengar mellan bankkonton. | [Jämka bankkonton](bank-manage-bank-accounts.md) |
| Ställa in koncerninterna partners och bearbeta transaktioner, automatiskt eller manuellt mellan juridiska personer inom samma företag. | [Hantera koncerninterna transaktioner](intercompany-manage.md) |
| Analysera kostnaderna för att driva ditt företag genom att fördela faktiska budgeterade kostnader för drift, avdelningar, produkter och projekt till kostnadscenter. | [Redovisa kostnader](finance-manage-cost-accounting.md) |
| Hantera lager- och produktionskostnader, och rapportera och stämma av kostnader med redovisningen. | [Hantera lagerkostnader](finance-manage-inventory-costs.md) |
| Hantera och rapportera kassainflöden och kassautflöden. | [Kassaflöde, översikt]( finance-cash-flow-overview.md) |
| Övervaka kassaflödet till och från ditt företag. | [Analysera transaktioner i företaget](finance-analyze-cash-flow.md) |
| Följ en heltäckande process som använder ekonomiska rapporter för att göra kassaflödesprognoser. | [Utföra kassaflödesprognoser genom att använda ekonomiska rapporter](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Lär dig mer om huvudboken och COA. | [Så här fungerar i redovisningen och kontoplanen](finance-general-ledger.md) |
| Kombinera redovisningstransaktioner från flera företag i ett enda virtuellt konsoliderat företag för ekonomisk analys. | [Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md)|
| Lägga till dimensioner för rikare BI. | [Arbeta med dimensioner](finance-dimensions.md) |
| Skapa redovisningsbudgetar för att förutse olika ekonomiska aktiviteter och koppla dimensioner för BI-syften. | [Skapa redovisningsbudgetar](finance-how-create-budgets.md) |
| Registrera intäkter och utgifter direkt i redovisningen utan att bokföra dedikerade affärsdokument. | [Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md) |
| Återför transaktioner om du vill ångra bokförda värdetransaktioner i redovisningsjournal eller bokföringar på inköps- och försäljningsdokument. | [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md) |
| fördela en transaktion i en redovisningsjournal på olika konton när du bokför journalen. | [Fördela kostnader och intäkter](year-allocate-costs-income.md) |
| Tilldela extra kostnader, till exempel frakt- och fysisk hantering som förekommer vid handel med artiklar. På så sätt återspeglas kostnaden i lagervärdering. | [Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md) |
| Bokföra kostnader för anställda för arbetsrelaterade aktiviteter och göra återbetalningar direkt till medarbetarbankkonton. | [Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md) |
| Allokera intäkter och kostnader till andra perioder som skiljer sig från de perioder då transaktionerna faktiskt bokfördes. | [Periodisera intäkter och kostnader](finance-how-defer-revenue-expenses.md) |
| Lär dig mer om tillgängliga alternativ för att automatiskt skicka prenumerationsfakturor till kunder och registrera återkommande intäkter. | [Arbeta med återkommande intäkter](finance-recurring-invoicing.md) |
| Använd ytterligare valutor och uppdatera valutakurser automatiskt. | [Uppdatera valutakurser](finance-how-update-currencies.md) |
| Importera löntransaktioner från ditt lönesystem till redovisningen. | [Importera lönetransaktioner](finance-how-import-payroll-transactions.md) |
| Beräkna moms (VAT) för försäljnings- och inköpstransaktioner så att du kan rapportera beloppen till skattemyndigheterna. | [Arbeta med moms på försäljning och inköp](finance-work-with-vat.md) |
| Förbereda en rapport över moms från försäljning och skicka rapporten till en skattemyndighet inom Europeiska unionen (EU). | [Rapportera moms till skattemyndigheterna](finance-how-report-vat.md) |
| Manuellt omvandla servicekontrakt för att ändra deras momssats. | [Omvandla servicekontrakt som innehåller momsbelopp](service-how-to-convert-service-contracts.md) |
| Arbeta med finansiella rapporter och översikter i Microsoft Excel. | [Analysera finansiella rapporter i Excel](finance-analyze-excel.md) |
| Använd använder rollcentret Revisor, kontakta en extern revisor och använd företagsnavet för att hantera konton för flera klienter. | [Revisorlösningar i Business Central ](finance-accounting.md) |
| Ställ in Intrastat-rapportering för att tillhandahålla handel med andra EU-medlemmar enligt lokal lagstiftning. | [Konfigurera Intrastat-rapportering]( finance-how-setup-report-intrastat.md) |
| Fyll i, validera och skicka Intrastat-rapporten. | [Arbeta med Intrastat-rapporter]( finance-how-report-intrastat.md) |
| Ställ in, fyll i, validera och skicka rapporten tjänstdeklaration för handelstjänster över hela EU. | [Ställ in och använd tjänstdeklarationen]( finance-how-setup-use-service-declaration.md) |
| skapa anläggningstillgångar, tilldela avskrivningsmetoder, bokföra anskaffningar, återanskaffningsvärden och skriva ut listor över anläggningstillgångar. | [Skaffa anläggningstillgångar](fa-how-acquire.md) |
| Registrera servicebesök, bokföra underhållsarbete och övervaka underhållskostnader. | [Underhålla anläggningstillgångar](fa-how-maintain.md) |
| Uppdatera försäkringsinformation, bokföra anskaffningskostnader i försäkringsbrev, ändra försäkringsskydd, visa försäkringsstatistik och visa listor över försäkringsbrev. | [Försäkra anläggningstillgångar](fa-how-insure.md) |
| gruppera anläggningstillgångar, flytta anläggningstillgångar mellan olika lagerställen, dela upp eller slå ihop tillgångar. | [Överföra, dela eller kombinera anläggningstillgångar](fa-how-trans-split-combine.md) |
| justera värdet på anläggningstillgångar, bokföra avskrivning och bokföra nedskrivningsstransaktioner. | [Omvärdera anläggningstillgångar](fa-how-revalue.md) |
| Beräkna och bokföra avskrivningar och analysera avskrivningar i rapporter om anläggningstillgångar. | [Skriva av eller amortera anläggningstillgångar](fa-how-depreciate-amortize.md) |
| bokföra avyttringstransaktioner, visa avyttringstransaktioner och bokföra delvisa avyttringar. | [Avyttra eller ställa av anläggningstillgångar](fa-how-dispose-retire.md) |
| Hanter budgetar för anläggningstillgångar, budgeterar anskaffningskostnader, budgeterar avyttringar av anläggningstillgångar och budgeterar avskrivning. | [Hantera budgetar och anläggningstillgångar](fa-how-manage-budgets.md) |
| Konfigurera arbetsflödesanvändare för godkännande, anger hur användarna får meddelanden och skapa nya arbetsflöden. För att skapa nya arbetsflöden för scenarier som inte stöds, implementera de nödvändiga arbetsflödeselementen genom att anpassa programkoden. | [Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md) |
| Aktivera arbetsflöden för godkännande, agera på arbetsflödemeddelanden (t.ex. genom att begära och godkänna arbetsflödessteg) och arkivera and ta bort arbetsflöden. | [Använda arbetsflöden för godkännande](across-use-workflows.md) |
| Visa faktiska belopp i jämförelse med budgeterade belopp för alla konton och för flera perioder. | [Analysera faktiska belopp kontra budgeterade belopp](bi-how-analyze-actual-versus-budget.md) |
| Skapa nya ekonomiska rapporter för att ange finansiella rapporter för att rapportera eller för att visa som diagram. | [Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md) |
| Analysera din ekonomiska kapacitet, genom att ställa in KPI:er baserat på ekonomiska rapporter och publicera de KPI:er som webbtjänster. De publicerade KPI:erna för ekonomiska rapporter kan visas på en webbplats eller importeras till Excel med hjälp av OData-webbtjänster. | [Konfigurera och publicera KPI-webbtjänster som baseras på ekonomiska rapporter](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Skapa vyer för att analysera data med dimensioner. | [Analysera data efter dimensioner](bi-how-analyze-data-dimension.md) |
| skapa nya analysrapporter för försäljning, inköp och lager, och skapa analysmallar. | [Skapa analysrapporter](bi-how-create-analysis-views-reports.md) |
| Aktivera global ekonomisk rapportering som står till internationella organisationer i redovisning med standarden eXtensible Business Reporting Language (XBRL). | [Skapa rapporter med XBRL](bi-create-reports-with-xbrl.md) |
| Ändra åtkomstmetoden för databaser gällande rapporter, sidor av typen API och frågor för att minska belastningen och förbättra prestandan. | [Hantera åtkomstmetod för databas](admin-data-access-intent.md) |

## <a name="see-also"></a>Se även

[Ställa in Finance](finance-setup-finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Stänga räkenskapsperioder](year-close-years-periods.md)  
[Hantera projekt](projects-manage-projects.md)  
[Importera data från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
