---
title: Konfigurera finansiella processer
description: 'Få mer information om uppgifterna för att ställa in Finance i ditt företag som passar alla behov av redovisning, granskning eller bokföring.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: edupont
---
# <a name="setting-up-finance"></a>Ställa in ekonomi

Innan du kan börja driva ditt företag måste du ange hur du vill hantera finansprocesser för företaget. Först skapar du det viktigaste för företagets redovisningsposter: kontoplanen. Därefter skapar du bokföringsmallar, som gör det effektivare att tilldela standardredovisningskonton till kunder, leverantörer och artiklar.

Vissa ekonomiinställningar kan göras automatiskt med assisterade konfigurationsguider, och vissa måste göras manuellt. Lär dig mer på [Gör dig redo att göra affärer](ui-get-ready-business.md). Sidan **Redovisningsinställningar** anger du hur du ska hantera företagets många olika bokföringsprocesser. Du kan till exempel använda denna sida för att ange uppgifter om avrundning av fakturabelopp, valutakoden för basvalutan, adressformat och om du vill använda en alternativ rapporteringsvaluta. Mer information finns på [Förstå redovisningen och kontoplanen](finance-general-ledger.md).  

Med hjälp av dimensioner kan du lägga till olika typer av information för respektive transaktion. Du kan skapa företagets grundläggande dimensioner, till exempel *Projekt* och *Avdelningar*. Senare kan du lägga till fler dimensioner när du behöver dem. Du kan t.ex. ange att temporära dimensioner ska användas under en begränsad tidsperiod, till exempel under en försäljningskampanj. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

Många av inställningsuppgifterna måste genomföras innan du kan börja registrera ekonomiska transaktioner, men du kan ändra de flesta inställningar efter behov. Det finns även valfria inställningsuppgifter. Till exempel behöver du bara ställa in koncerninterna bokningar och konsolideringar om du arbetar med flera företag. Andra inställningsuppgifter, som att ange vilken period som bokföringen kan göras under, kanske måste upprepas regelbundet.  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
|Visa eller redigera den lista med redovisningskonton som alla redovisningstransaktioner bokförs på|[Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md)|
| Ange hur du vill att kunderna ska betala och hur du vill betala leverantörerna. |[Konfigurera betalsätt](finance-payment-methods.md) |
| Ange betalningsvillkor för att hantera förfallodatum och beräkna eventuella kassarabatter.|[Ställa in betalningsvillkor](finance-payment-terms.md) |
| Ange bokföringsmallar mappar enheter som t. ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. |[Konfigurera bokföringsmallar](finance-posting-groups.md)|
|Skapa ekonomiska rapporter och definiera kontokategorier som definierar innehållet i ekonomiska tabeller och rapporter, som rapporterna Balansräkning och Resultaträkning.|[Förbereda Financial Reporting med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)|
|Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet.|[Arbeta med betalningstoleranser och kassarabattstoleranser](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Ställa in räkenskapsperioder. |[Arbeta med bokföringsperioder och räkenskapsår](finance-accounting-periods-and-fiscal-years.md) |
|Ange fakturavillkor som påminner kunderna om att betala.|[Konfigurera påminnelsevillkor och nivåer](finance-setup-reminders.md)|
| Definiera hur du rapporterar belopp för moms som du har lagrat för försäljning till skattemyndigheterna. |[Ställa in moms](finance-setup-vat.md)|
|Förbereda att hantera orealiserad moms i samband med kontantbaserade redovisningsmetoder.|[Ställa in orealiserad moms för kontantbaserad redovisning](finance-setup-unrealized-vat.md)|
|Definiera utländska valutor som du handlar med eller rapporterar transaktioner i.|[Konfigurera valutor](finance-set-up-currencies.md)|
| Ange funktioner för försäljning och inköp till att hantera betalningar i utländsk valuta.|[Aktivera koppling av kundreskontratransaktioner till olika valutor](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definiera ett eller fler ytterligare belopp så att beloppen rapporteras automatiskt i både lokal valuta (BVA) och en ytterligare rapporteringsvaluta för varje redovisningstransaktion och för andra transaktioner.|[Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md)|
|Ändra med jämna mellanrum alternativa valutavärden för fluktuerande växelkurser.|[Uppdatera valutakurser](finance-how-update-currencies.md)|
|Definiera flera räntesatser som används för olika perioder för försenade betalningar i handelstransaktioner.|[Ställ in flera räntesatser](finance-how-to-set-up-multiple-interest-rates.md)|
|Ordna så att belopp avrundas automatiskt när fakturor skapas.|[Ställa in överavrundning](finance-set-up-invoice-rounding.md)|
| Lägga till nya konton i den befintliga kontoplanen. |[Ställa in kontoplanen](finance-setup-chart-accounts.md) |
| Ställa in business intelligence (BI)-diagram för att analysera betalningen. |[Ställa in analys för kassaflöde](finance-setup-cash-flow-analyses.md) |
|Aktivera fakturering av en kund som inte har angetts i systemet.|[Så här skapar du Kontantkunder](finance-how-to-set-up-cash-customers.md)|
| Ställa in Intrastat-rapporten och skicka rapporten till en myndighet. | [Skapa och rapportera Intrastat](finance-how-setup-report-intrastat.md)|
|Se till att en journaltransaktion allokeras mellan olika konton, som kvantitet, procent eller belopp, när du bokför den i journalen.|[Så här använder du fördelningsnycklar i redovisningsjournaler](ui-how-use-allocation-keys-general-journals.md)|
|Ställ in ursprungskoder och uppföljningskoder för att spåra granskningshistorik.|[Ställa in ursprungskoder och orsakskoder för granskningshistorik](finance-setup-trail-codes.md)|
|Ange standardrapporter som ska användas för olika dokumenttyper.|[Rapportval i Business Central](across-report-selections.md)|

> [!TIP]
> Beroende på ditt geografiska läge kan vissa Business Central-sidor innehålla fält som inte beskrivs i artiklarna som anges ovan, eftersom de gäller lokala funktioner eller anpassningar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
