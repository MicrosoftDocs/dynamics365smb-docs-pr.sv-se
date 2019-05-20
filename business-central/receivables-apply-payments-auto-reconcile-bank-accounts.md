---
title: Stämma av bankkonton och utför betalningar | Microsoft Docs
description: Beskriver uppgifter för att stämma av din bank, kundreskontra och leverantörsreskontra, bokföra inbetalningar eller kostnader och tillämpa betalningar automatiskt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 124b3e82a38af375128353d977cc250aa9f94cf8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251406"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Koppla utbetalningar automatiskt och stämma av bankkonton
Du måste regelbundet stämma av din bank, kundfordringar och konto för kundreskontra genom att koppla betalningar som är registrerade i banken till deras motsvarande obetalda fakturor och kreditnotor eller andra öppna transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du kan utföra denna aktivitet på sidan **Betalningsavstämningsjournal** genom att importera ett kontoutdrag eller feed för att snabbt registrera utbetalningarna. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på matchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra automatiska kopplingar, innan du bokför journalen. Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen. Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.

Du kan också stämma av bankkonton utan att samtidigt utföra betalningar. Du utför detta arbete på sidan **Bankkontoavstämning**. Mer information finns i [Stämma av bankkonto separat](bank-how-reconcile-bank-accounts-separately.md).   

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera Envestnet Yodlee Bank Feeds-tjänsten och sedan länka dina bankkonton till relaterade onlinebankkonton. Mer information finns i [Konfigurera du Envestnet Yodlee Bank Feeds-tjänsten](bank-how-setup-bank-statement-service.md).  

Du kan alternativt använda funktionen för bankdatakonvertering om du vill få en bankutdragsfil i något format konverterad till en dataström som du kan importera till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Konfigurera bankdatakonverteringstjänsten](bank-how-setup-bank-data-conversion-service.md).  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Om du vill | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner genom att importera ett kontoutdrag och stämma av bankkonton när alla betalningar är kopplade. |[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md) |
| Koppla betalningar manuellt genom att visa detaljerad information om matchade data och förslag om att öppna kandidattransaktioner att koppla betalningar till. |[Så här granskar och kopplar du betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md) |
| Lös betalningar som inte kan kopplas automatiskt till deras relaterade öppna transaktioner. Till exempel för att beloppen skiljer sig eller för att en relaterad transaktion inte finns. |[Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koppla text på betalningar till specifika kund-, leverantörs- eller redovisningskonton för att alltid bokföra återkommande inbetalningar eller kostnader på dessa konton när det inte finns dokument att applicera dem på. |[Så här mappar du text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
