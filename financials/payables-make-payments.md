---
title: "Översikt över uppgifter för hantering av betalningar till leverantörer | Microsoft Docs"
description: "Innehåller information om hur du hanterar betalningar till leverantörer och fordringsägare, inklusive bokför betalningsraderna och få en översikt över saldot som förfaller."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00792adb8b4c7deccee262982cd532423884c8f5
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="making-payments"></a>Göra betalningar
När du gör betalningar till leverantörer eller återbetalningar till anställda bokför du relaterade betalningsraderna i fönstret **Betalningsjournal**. Du kan använda funktionen **Betalningsförslag för lev.** för att söka efter leveratörsbetalningar som förfaller till betalning. Du kan även använda rapporten **Lev.saldo - ålderssammandrag** för att få en översikt över leverantörsbetalningar som förfaller till betalning.

Från utbetalningsjournalen kan du skriva ut datorcheckar eller registrera när checkar skrivs. När **Datorcheck** har valts i fältet **Bankbetalningstyp** i utbetalningsjournalen måste alla rader som representerar checkarna skrivas ut innan betalningsjournalen kan bokföras.

När du bokför betalningar, exporterar du dem till en bank-fil för överföring till din bank för bearbetning.

När betalningarna har utförts på din bank, måste du koppla dem till deras tillhörande öppna leverantörs- eller personaltransaktioner. Du kan göra detta manuellt eller genom att importera en bankutdragsfil och att koppla betalningarna automatiskt. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
|Använd fönstret **Betalningsjournal** som är baserat på redovisningsjournalen för att bokföra betalningar till leverantörer eller medarbetare.|[Arbeta med redovisningsjournaler](ui-work-general-journals.md)|
| Använd en funktion för att föreslå leverantörsbetalningar enligt valda kriterier, till exempel förfallodatum, rabattvalbarhet och din likviditeten. |[Så här använder du betalningsförslag för leverantörer](payables-how-suggest-vendor-payments.md) |
|Återbetala anställda för privata utgifter under affärsaktiviteter genom att göra betalningen till dennes bankkonto.|[Så här: skapa och återbetala anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)|
| Utfärda checkar för leverantörsbetalningar, antingen som utskrifter eller som datorcheckar. Makulera checkar, före eller efter bokföring. |[Så här arbetar du med checkar](payables-how-work-checks.md) |
| Betala leverantören kontant eller med check och bokför betalningen när du bokför fakturan. |[Så här gör du för att snabbt betala inköpsfakturor](finance-how-to-settle-purchase-invoices-promptly.md) |
| Se till att banken bara godkänner validerade checkar och belopp genom att skicka en fil som innehåller information om leverantör, check ch betalning. |[Så här exporterar du en Positive Pay-fil](finance-how-positive-pay.md) |
|Exportera betalningar från fönstret **Betalningsjournal** till en bankfil som du skickar till din bank för bearbetning, inklusive EFT (elektronisk överföring) i Nordamerika. |[Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

