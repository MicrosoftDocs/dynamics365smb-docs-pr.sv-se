---
title: "Ställa in Financialsprocesser | Microsoft Docs"
description: "Få mer information om uppgifterna för att ställa in Finance i ditt företag som passar alla behov av redovisning, granskning eller bokföring."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 377e7f8eb3cb78adf68e3f4167a215d8f027f972
ms.contentlocale: sv-se
ms.lasthandoff: 12/19/2018

---
# <a name="setting-up-finance"></a>Ställa in ekonomi
För att komma igång snabbare innehåller [!INCLUDE[d365fin](includes/d365fin_md.md)] standardkonfigurationer för de flesta ekonomiska processer. Om du behöver ändra konfigurationen så att de passar din verksamhet kan du fortsätta direkt. Från Rollcenter kan du exempelvis använda en assisterad konfigurationsguide som hjälper dig att konfigurera momssatsen för din plats.  

Det finns dock några saker som du måste konfigurera själv. Om du till exempel vill använda dimensioner som grund för business intelligence.  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| Välj hur du betalar leverantörerna. |[Definiera betalningssätt](finance-payment-methods.md) |
| Ange bokföringsmallar mappar enheter som t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. |[Ställa in bokföringsmallar](finance-posting-groups.md)|
|Skapa kontouppställningar och definiera kategorier för att definiera innehållet i ekonomiska tabeller och rapporter som rapporterna balansräkning och resultaträkning.|[Förbereda ekonomiska rapporter, kontouppställningar och kategorier](bi-how-work-account-schedule.md)|
|Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet.|[Arbeta med betalningstoleranser och kassarabattstoleranser](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Ställa in räkenskapsperioder. |[Så här öppnar du ett nytt räkenskapsår:](finance-how-open-new-fiscal-year.md) |
| Definiera hur du rapporterar belopp för moms som du har lagrat för försäljning till skattemyndigheterna. |[Förbereda beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)|
|Förbereda att hantera orealiserad moms i samband med kontantbaserade redovisningsmetoder.|[Ställa in orealiserad moms för kontantbaserad redovisning](finance-setup-unrealized-vat.md)|
| Ange funktioner för försäljning och inköp till att hantera betalningar i utländsk valuta.|[Aktivera koppling av kundreskontratransaktioner till olika valutor](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definiera ett eller fler ytterligare belopp så att beloppen rapporteras automatiskt i både BVA och en alternativ rapporteringsvaluta för varje redovisningstransaktion och för andra transaktioner.|[Ställa in en alternativ rapporteringsvaluta.](finance-how-setup-additional-currencies.md)|
|Ändra med jämna mellanrum alternativa valutavärden för fluktuerande växelkurser.|[Uppdatera valutakurser](finance-how-update-currencies.md)|
|Definiera flera räntesatser som används för olika perioder för försenade betalningar i handelstransaktioner.|[Ställ in flera räntesatser](finance-how-to-set-up-multiple-interest-rates.md)|
|Förbered automatisk avrundning av fakturabelopp när du skapar fakturor.|[Ställa in överavrundning](finance-set-up-invoice-rounding.md)|
| Lägga till nya konton i den befintliga kontoplanen. |[Ställa in kontoplanen](finance-setup-chart-accounts.md) |
| Ställa in business intelligence (BI)-diagram för att analysera betalningen. |[Ställa in analysvy för kassaflöde](finance-setup-cash-flow-analyses.md) |
|Aktivera fakturering av en kund som inte har angetts i systemet.|[Så här skapar du Kontantkunder](finance-how-to-set-up-cash-customers.md)|
| Ställa in Intrastat-rapporten och skicka rapporten till en myndighet | [Skapa och rapportera Intrastat](finance-how-setup-report-intrastat.md)|
|Förbered rapporten Konsoliderad råbalans för rollcentret Redovisare för en ekonomisk översikt över flera företag.|[Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md)|
|Se till att en transaktion i en redovisningsjournal allokeras till flera olika konton när journalen bokförs, antingen efter kvantitet, procent eller belopp.|[Så här använder du fördelningsnycklar i redovisningsjournaler](ui-how-use-allocation-keys-general-journals.md)|

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

