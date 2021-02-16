---
title: Ställa in Financialsprocesser | Microsoft Docs
description: Få mer information om uppgifterna för att ställa in Finance i ditt företag som passar alla behov av redovisning, granskning eller bokföring.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b18d4406f77594486104e2348487a3380cca0af4
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024468"
---
# <a name="setting-up-finance"></a>Ställa in ekonomi
Innan du kan börja driva ditt företag måste du ange regler och standardvärden för hur du vill hantera finansprocesser för det företaget. Du börjar med att skapa det viktigaste för företagets redovisningsposter – kontoplanen. Därefter skapar du bokföringsmallar, som gör det effektivare att tilldela standardredovisningskonton till kunder, leverantörer och artiklar.

Vissa ekonomiinställningar kan göras automatiskt med assisterade konfigurationsguider, och vissa måste göras manuellt. Mer information finns i [Komma igång med att göra affärer](ui-get-ready-business.md).

Med hjälp av dimensioner kan du lägga till olika typer av information för respektive transaktion. Du kan konfigurera ditt företags grundläggande dimensioner, till exempel projekt och avdelningar. Senare kan du lägga till fler dimensioner efter behov, och du kan skapa tillfälliga dimensioner som ska användas under en begränsad tidsperiod, till exempel i samband med en försäljningskampanj. Mer information finns i [Arbeta med](finance-dimensions.md).

Många av inställningsuppgifterna måste genomföras innan du kan börja registrera ekonomiska transaktioner, men du kan ändra de flesta inställningar vid en senare tidpunkt. Vissa uppgifter är valfria, till exempel behöver du bara ställa in koncerninterna bokningar och konsolideringar om du arbetar med flera företag. Andra uppgifter, som att ange vilken period som bokföringen kan göras under, kanske måste upprepas regelbundet.  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
| Ange hur du vill att kunderna ska betala och hur du vill betala leverantörerna. |[Konfigurera betalsätt](finance-payment-methods.md) |
| Ange betalningsvillkor för att hantera förfallodatum och beräkna eventuella kassarabatter.|[Ställa in betalningsvillkor](finance-payment-terms.md) |
| Ange bokföringsmallar mappar enheter som t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. |[Ställa in bokföringsmallar](finance-posting-groups.md)|
|Skapa kontouppställningar och definiera kategorier för att definiera innehållet i ekonomiska tabeller och rapporter som rapporterna balansräkning och resultaträkning.|[Förbereda ekonomiska rapporter, kontouppställningar och kategorier](bi-how-work-account-schedule.md)|
|Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet.|[Arbeta med betalningstoleranser och kassarabattstoleranser](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Ställa in räkenskapsperioder. |[Arbeta med bokföringsperioder och räkenskapsår](finance-accounting-periods-and-fiscal-years.md) |
|Ange villkor för betalningspåminnelse för att hjälpa dig att få in förfallna betalningar.|[Konfigurera påminnelsevillkor och nivåer](finance-setup-reminders.md)|
| Definiera hur du rapporterar belopp för moms som du har lagrat för försäljning till skattemyndigheterna. |[Ställa in moms](finance-setup-vat.md)|
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
|Se till att en transaktion i en redovisningsjournal allokeras till flera olika konton när journalen bokförs, antingen efter kvantitet, procent eller belopp.|[Så här använder du fördelningsnycklar i redovisningsjournaler](ui-how-use-allocation-keys-general-journals.md)|
|Ställ in ursprungskoder och uppföljningskoder som kan användas för att spåra granskningshistorik|[Ställa in ursprungskoder och orsakskoder för granskningshistorik](finance-setup-trail-codes.md)|
|Ange standardrapporter som ska användas för olika dokumenttyper.|[Rapportval i Business Central](across-report-selections.md)|

> [!TIP]
> Beroende på vilken geografisk plats det är kan vissa sidor innehålla fält som inte beskrivs i artiklarna som anges här eftersom de gäller lokala funktioner eller anpassningar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
