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
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a>Gör utbetalningar
När du gör betalningar till leverantörer, bokför du relaterade betalningsraderna i fönstret **Betalningsjournal**. Du kan använda funktionen **Betalningsförslag för lev.** för att söka efter betalningar som förfaller till betalning. Du kan även använda rapporten **Lev.saldo - ålderssammandrag** för att få en översikt över betalningar som förfaller till betalning.

Från utbetalningsjournalen kan du skriva ut datorcheckar eller registrera när checkar skrivs. När **Datorcheck** har valts i fältet **Bankbetalningstyp** i utbetalningsjournalen måste alla rader som representerar checkarna skrivas ut innan betalningsjournalen kan bokföras.

När du bokför betalningar, exporterar du dem till en bank-fil för överföring till din bank för bearbetning.

När betalningarna har utförts på din bank, måste du koppla dem till deras tillhörande öppna leverantörsreskontratransaktioner. Du kan göra detta manuellt eller genom att importera en bankutdragsfil och att koppla betalningarna automatiskt. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| Använd en funktion för att föreslå leverantörsbetalningar enligt valda kriterier, till exempel förfallodatum, rabattvalbarhet och din likviditeten. |[Så här använder du betalningsförslag för leverantörer](payables-how-suggest-vendor-payments.md) |
| Utfärda checkar för utbetalningar, antingen som utskrifter eller som datorcheckar. Makulera checkar, före eller efter bokföring. |[Så här arbetar du med checkar](payables-how-work-checks.md) |
| Se till att banken bara godkänner validerade checkar och belopp genom att skicka en fil som innehåller information om leverantör, check ch betalning. |[Så här exporterar du en Positive Pay-fil](finance-how-positive-pay.md) |
|Exportera betalningar från fönstret **Betalningsjournal** till en bankfil som du skickar till din bank för bearbetning, inklusive EFT (elektronisk överföring) i Nordamerika. |[Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

