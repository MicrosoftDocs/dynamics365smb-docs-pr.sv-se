---
title: "Översikt över uppgifter för hantering av betalningar till leverantörer | Microsoft Docs"
description: "Innehåller information om hur du hanterar betalningar till leverantörer och fordringsägare, inklusive bokför betalningsraderna och få en översikt över saldot som förfaller."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/26/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 6b912e8f54fd0e3fb4ac4a1eee3c376c209ffe65
ms.contentlocale: sv-se
ms.lasthandoff: 04/26/2018

---
# <a name="making-payments"></a>Göra betalningar
När du gör betalningar till leverantörer eller återbetalningar till anställda bokför du relaterade betalningsraderna i fönstret **Betalningsjournal**. Du kan använda funktionen **Betalningsförslag för lev.** för att söka efter leveratörsbetalningar som förfaller till betalning. Du kan även använda rapporten **Lev.saldo - ålderssammandrag** för att få en översikt över leverantörsbetalningar som förfaller till betalning.

Från utbetalningsjournalen kan du skriva ut datorcheckar eller registrera när checkar skrivs. När **Datorcheck** har valts i fältet **Bankbetalningstyp** i utbetalningsjournalen måste alla rader som representerar checkarna skrivas ut innan betalningsjournalen kan bokföras.

När du bokför betalningar, exporterar du dem till en bank-fil för överföring till din bank för bearbetning.

När betalningarna har utförts på din bank, måste du koppla dem till deras tillhörande öppna leverantörs- eller personaltransaktioner. Du kan göra detta manuellt eller genom att importera en bankutdragsfil och att koppla betalningarna automatiskt. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
|Förstå grundläggande funktioner i fönstret **Betalningsjournal** som är baserat på redovisningsjournalen för att bokföra betalningar till leverantörer eller medarbetare.|[Arbeta med redovisningsjournaler](ui-work-general-journals.md)|
|Bokför betalningar till leverantörer och återbetalningar till kunder och om du vill koppla betalningar till relaterade obetalda fakturor/kreditnotor stänga dem som betalda.|[Registrera betalningar och återbetalningar](payables-how-post-payments-refunds.md)|
| Använd en funktion i **Betalningsjournal** för att föreslå leverantörsbetalningar enligt valda villkor, till exempel förfallodatum, rabattvalbarhet och din likviditeten. |[Betalningsförslag för lev.](payables-how-suggest-vendor-payments.md) |
| Utfärda checkar för leverantörsbetalningar eller kundåterbetalningar, antingen som utskrifter eller som datorcheckar. Makulera checkar, före eller efter bokföring. |[Gör checkbetalning](payables-how-work-checks.md) |
|Gör elektroniska betalningar genom att exportera betalningar till en bankfil som du skickar till din bank för bearbetning, inklusive EFT (elektronisk överföring) i Nordamerika. |[Gör elektroniska betalningar](payables-how-export-payments-bank-file.md)|
|Göra elektroniska betalningar i enlighet med EU:s kreditöverföringsstandard SEPA.|[Göra betalningar med tjänsten för bankdatakonvertering eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Betala leverantören kontant eller med check och bokför betalningen när du bokför fakturan. |[Betala inköpsfakturor snabbt](finance-how-to-settle-purchase-invoices-promptly.md) |
|Återbetala anställda för privata utgifter under affärsaktiviteter genom att göra betalningen till dennes bankkonto.|[Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)|
| Se till att banken bara godkänner validerade checkar och belopp genom att skicka en fil som innehåller information om leverantör, check ch betalning. |[Exportera en Positive Pay-fil](finance-how-positive-pay.md) |

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

