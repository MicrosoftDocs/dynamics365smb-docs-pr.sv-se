---
title: "Översikt över uppgifter för hantering av leverantörsskulder | Microsoft Docs"
description: "Innehåller information om hur du hanterar leverantörsreskontra, till exempel betala fordringsägare eller koppla utgående betalningar till transaktioner för att stänga fakturor eller kreditnotor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Hantera Leverantörsreskontra
En stor del av hantering av leverantörsskulder är att betala leverantörer. Du kan använda funktioner för att lägga till betalningsrder för inköpsfakturor som förfaller till betalning i fönstret **Betalningsjournal**. För att skicka transaktioner till din bank kan du exportera flera betalningsjournalrader till en fil och sedan överför du filen till din bank. Du kan också göra betalningar med check som inkluderar att överföra checkar som elektronisk betalning.

En annan typisk aktivitet är att koppla utgående betalningar till deras relaterade på kund- eller leverantörsreskontratransaktioner för att avsluta de inköpsfakturorna eller inköpskreditnotorna som betalda. Du kan göra detta i fönstret **Betalningsavstämningsjournal** genom att importera ett kontoutdrag för att snabbt registrera utbetalningarna. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner genom att matcha betalningstexten och transaktionsinformation. Det finns olika sätt att visa och ändra matchningarna innan du bokför journalen. Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen. Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.

Du kan också koppla utgående betalningar manuellt i fönstret **Betalningsjournal** eller från relaterade leverantörsreskontraposterna.

I följande tabell beskrivs en serie uppgifter inom Leverantörsskulder med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| Generera förfallna leverantörsbetalningar som prioriteras enligt kassarabatter och förseningsavgifter. Exportera betalningarna till en bankfil, när du bokför, om du vill. |[Gör utbetalningar](payables-make-payments.md) |
| Koppla leverantörsbetalningar automatiskt till obetalda inköpsfakturor, genom att importera bankutdragsfil. |[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Koppla leverantörsbetalningar till obetalda inköpsfakturor manuellt. |[Så här stämmer du av leverantörsbetalningar manuellt](payables-how-apply-purchase-transactions-manually.md) |
|Säkerställa korrekt värdering av lager genom att tilldela extra artikelkostnader, som till exempel frakt, fysisk hantering, försäkring och transport som förekommer vid inköp.|[Så här: Använd artikelomkostnader till kontot för ytterligare kostnader](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Så här: Använd artikelomkostnader till kontot för ytterligare kostnader](payables-how-assign-item-charges.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

