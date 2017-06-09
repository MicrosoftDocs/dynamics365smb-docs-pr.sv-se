---
title: "Hantera leverantörsskulder | Microsoft Docs"
description: "Hantera Leverantörsreskontra"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 92b16c52589a07661d9ff080e9ef8a0f6be633f7
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


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

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

