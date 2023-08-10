---
title: Översikt över uppgifter för hantering av betalningar till leverantörer
description: 'Innehåller information om hur du hanterar betalningar till leverantörer och fordringsägare, inklusive bokför betalningsraderna och få en översikt över saldot som förfaller.'
author: edupont04
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="making-payments"></a>Göra betalningar

När du gör betalningar till leverantörer eller kunder eller återbetalningar till anställda bokför du relaterade betalningsraderna på sidan **Betalningsjournal**. Betalningsjournalen är en redovisningsjournal som är optimerad för betalningar och innehåller flera kraftfulla funktioner, till exempel funktionen **Betalningsförslag för lev.** som söker efter leverantörsbetalningar som har förfallit, och rapporten **Leverantör – Ålderssammandrag** som visar en översikt över förfallna leverantörsbetalningar.  

Du kan starta processen med att göra betalningen från listor, kort och transaktioner för leverantörer, kunder och anställda. Var och en av dessa sidor har en knapp som startar betalningsflödet och hjälper dig att fylla i utbetalningsjournalen.  

Från utbetalningsjournalen kan du skriva ut datorcheckar eller registrera när checkar skrivs. När **Datorcheck** har valts i fältet **Bankbetalningstyp** i utbetalningsjournalen måste alla rader som representerar checkarna skrivas ut innan betalningsjournalen kan bokföras.

När du bokför betalningar, exporterar du dem till en bank-fil för överföring till din bank för bearbetning.

När betalningarna har utförts på din bank, måste du koppla dem till deras tillhörande öppna leverantörs- eller personaltransaktioner. Du kan göra detta manuellt eller genom att importera en bankutdragsfil och att koppla betalningarna automatiskt. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
|Förstå grundläggande funktioner på sidan **Betalningsjournal** som är baserat på redovisningsjournalen för att bokföra betalningar till leverantörer eller medarbetare.|[Arbeta med redovisningsjournaler](ui-work-general-journals.md)|
|Bokför betalningar till leverantörer eller anställda och återbetalningar till kunder och om du vill koppla betalningar till relaterade obetalda fakturor/kreditnotor stänga dem som betalda.|[Registrera betalningar och återbetalningar](payables-how-post-payments-refunds.md)|
| Använd en funktion på sidan **Betalningsjournal** för att föreslå leverantörsbetalningar enligt valda villkor, till exempel förfallodatum, rabattvalbarhet och din likviditeten. |[Betalningsförslag för lev.](payables-how-suggest-vendor-payments.md) |
| Utfärda checkar för leverantörsbetalningar eller kundåterbetalningar, antingen som utskrifter eller som datorcheckar. Makulera checkar, före eller efter bokföring. |[Gör checkbetalning](payables-how-work-checks.md) |
|Göra elektroniska betalningar i enlighet med EU:s kreditöverföringsstandard SEPA.|[Gör betalningar med tillägget AMC Banking 365 Fundamentals eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Betala leverantören kontant eller med check och bokför betalningen när du bokför fakturan. |[Betala inköpsfakturor snabbt](finance-how-to-settle-purchase-invoices-promptly.md) |
| Se till att banken bara godkänner validerade checkar och belopp genom att skicka en fil som innehåller information om leverantör, check ch betalning. |[Exportera en Positive Pay-fil](finance-how-positive-pay.md) |

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
