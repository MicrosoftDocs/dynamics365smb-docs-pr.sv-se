---
title: Hantera kundreskontra | Microsoft Docs
description: Hantera kundreskontra
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 62d59546331a5faa5ecb7aea0f9bb8dedea719f9
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="managing-receivables"></a>Hantera kundreskontra
En vanlig steg i alla finansiella takter är att stämma av bankkonton, som kräver att du kopplar betalningar till kund- eller leverantörsreskontratransaktioner för att stänga försäljningsfakturor och inköpskreditnotor.  

I [!INCLUDE[d365fin](includes/d365fin_md.md)], är ett av de snabbaste sätten att registrera betalningar från fönstret **Betalningsavstämningsjournal** genom att importera en bankutdragsfil feed. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på datamatchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra matchningrana innan du bokför journalen och avsluta bankkontotransaktioner för transaktioner när du bokför journalen. Bankkontot avstäms när alla utbetalningar kopplas.

Det finns dock andra praktiska ställen för att tillämpa betalningar och stämma av bankkonton:  

* Fönstret **Bankkontoavstämningar** låter dig kontrollera transaktionerna. Mer information finns i [Så här stämmer du av bankkonton separat](bank-how-reconcile-bank-accounts-separately.md).  
* Fönstret **Betalningsregistrering** där du kan tillämpa och manuellt kontrollera betalningar som tas emot som kontanter, check eller banktransaktion mot en skapad lista över obetalda försäljningsdokument. Observera att den här funktionen endast är tillgänglig för försäljningsdokument.  
* Fönstret **Inbetalningsjournal** där du kan manuellt bokföra kvitton till relevant redovisning, kund eller annat konto, genom att ange en betalningsrad Du kan antingen använda kvittot eller återbetalningen till en eller flera öppna transaktioner, innan du bokför inbetalningsjournalen, eller från kundtransaktionerna.  

En annan del i hanteringen av kundfordringar är att kräva in utestående saldon inklusive dröjsmålsränta och skicka betalningspåminnelser. [!INCLUDE[d365fin](includes/d365fin_md.md)] erbjuder sätt att göra detta också. Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Om du vill | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner baserade på en importerat kontoutdragsfil eller feed och stämma av bankkonton när alla betalningar är kopplade. |[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Koppla utbetalningar till öppna kundreskontratransaktioner som baseras på manuell inmatning i en lista över obetalda försäljningsdokument. |[Så här stämmer du av kundutbetalningar manuellt från en lista med obetalda försäljningsdokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bokföring av inbetalningar eller återbetalningar för kunder i inbetalningsjournalen och koppla till kundreskontratransaktioner, antingen från journalen eller från bokförda transaktioner. |[Så här stämmer du av kundbetalningar rabatter manuellt](receivables-how-apply-sales-transactions-manually.md) |
| påminna kunder om förfallna belopp, beräkna dröjsmålsränta och hantera kundreskontra. |[Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md) |

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

