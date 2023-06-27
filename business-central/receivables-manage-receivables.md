---
title: Översikt över uppgifter för hantering av kundreskontra
description: Detta ämne innehåller information om hur du hanterar kundreskontra och kopplar betalningar till kund- eller leverantörstransaktioner.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer payment, debtor, balance due, AR'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="managing-receivables" />Hantera kundreskontra

En vanlig steg i alla finansiella takter är att stämma av bankkonton, som kräver att du kopplar inkommande betalningar till kund- eller leverantörsreskontratransaktioner för att stänga försäljningsfakturor och inköpskreditnotor när de betalas.

Även om de flesta kunder i B2B-miljöer betalar ett tag efter leverans lämnar bokförda försäljningsfakturor öppna för kundreskontraavdelningen att stänga (koppla) när betalningen tas emot, vissa försäljningsfakturor kan betalas direkt, till exempel med PayPal. Sådana fakturor tillämpas omedelbart som betalda när de bokförs och därför visas de inte som betalningar som ska behandlas i KR. Mer information finns i t. ex. [Fakturera försäljning](sales-how-invoice-sales.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] är ett av de snabbaste sätten att registrera betalningar från sidan **Betalningsavstämningsjournal** genom att importera en kontoutdragsfil feed. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på datamatchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra matchningrana innan du bokför journalen och avsluta bankkontotransaktioner för transaktioner när du bokför journalen. Bankkontot avstäms när alla utbetalningar kopplas.

Det finns andra sidor där du kan koppla betalningar eller stämma av bankkonton:

* Sidan **Bankkontoavstämningar**, där du stämmer av bankkonton genom att matcha importerade bankutdragsrader med dina systembankkontotransaktioner. Här kan du stämma av checkbetalningar. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md). Här kan du inte använda betalningar.
* Sidan **Betalningsregistrering** där du kan tillämpa och manuellt kontrollera checkbetalningar som tas emot som kontanter, check eller banktransaktion mot en skapad lista över obetalda försäljningsdokument. Observera att den här funktionen endast är tillgänglig för försäljningsdokument. Du kan inte använda utgående betalningar här, och du kan inte stämma av bankkonton.
* Sidan **Inbetalningsjournal** där du kan manuellt bokföra kvitton till relevant redovisning, kund eller annat konto, genom att ange en betalningsrad. Du kan antingen använda kvittot eller återbetalningen till en eller flera öppna transaktioner, innan du bokför inbetalningsjournalen, eller från kundtransaktionerna. Här kan du inte stämma av bankkonton.

Sidan **Betalningsavstämningsjournal** använder automatisk matchningslogik som du kan ställa in på sidan **Regler för betalningskoppling**. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md).  

Andra aspekter av hanteringen av kundfordringar är att kräva in utestående saldon, inklusive ränta och betalningspåminnelser och att konfigurera bankkonton så att kundernas betalningarna dras från kontot automatiskt.

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Om du vill | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner baserade på en importerat kontoutdragsfil eller feed och stämma av bankkonton när alla betalningar är kopplade. |[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Tillämpa betalningar för att öppna kundreskontratransaktioner utifrån en lista över obetalda försäljningsdokument på sidan **Betalningsregistrering**. |[Så här stämmer du av kundutbetalningar från en lista med obetalda försäljningsdokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bokföring av inbetalningar eller återbetalningar för kunder i inbetalningsjournalen och koppla till kundreskontratransaktioner, antingen från journalen eller från bokförda transaktioner. |[Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner](receivables-how-apply-sales-transactions-manually.md) |
| påminna kunder om förfallna belopp, beräkna dröjsmålsränta och hantera kundreskontra. |[Kräva in utestående saldon](receivables-collect-outstanding-balances.md) |
|Med kundens samtycke kan du endast samla in betalningar direkt från kundens bankkonto i valutan Euro.|[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)|
|Spärra en kund som förs in i dokument eller från bokföring, till exempel på grund av att ett insolvensförfarande.|[Spärra kunder](receivables-how-block-customers.md)|
|Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet.|[Arbeta med betalningstoleranser och kassarabattstoleranser](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Förutsäga när betalningar görs sent för försäljningsdokument. | [Tillägget för prediktion om sen betalning](ui-extensions-late-payment-prediction.md) |

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also" />Se även
[Försäljning](sales-manage-sales.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
