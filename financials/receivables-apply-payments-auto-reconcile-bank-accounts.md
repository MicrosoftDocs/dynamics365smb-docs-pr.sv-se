---
title: "Uppgifter för att stämma av bankkonton och koppla betalningar till relaterade poster | Microsoft Docs"
description: "Beskriver uppgifter för att stämma av din bank, kundreskontra och leverantörsreskontra, bokföra inbetalningar eller kostnader och tillämpa betalningar automatiskt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f828fce295b15db9e50034a51e1531b29b064c85
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="apply-payments-automatically-and-reconcile-bank-accounts"></a>Koppla utbetalningar automatiskt och stämma av bankkonton
Du måste regelbundet stämma av din bank, kundfordringar och konto för kundreskontra genom att koppla betalningar som är registrerade i banken till deras motsvarande obetalda fakturor och kreditnotor eller andra öppna transaktioner i [!INCLUDE[d365fin](includes/d365fin_long_md.md)].  

Du kan utföra denna aktivitet i fönstret **Betalningsavstämningsjournal** genom att importera ett kontoutdrag eller feed för att snabbt registrera utbetalningarna. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på matchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra automatiska kopplingar, innan du bokför journalen. Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen. Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.  

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera tjänsten Envestnet Yodlee bankfeed och sedan länka dina bankkonton till relaterade onlinebankkonton. Mer information finns i [Så här konfigurerar du tjänsten Envestnet Yodlee bankfeeder](bank-how-setup-bank-statement-service.md).  

Du kan alternativt använda funktionen för bankdatakonvertering om du vill få en bankutdragsfil i något format konverterad till en dataström som du kan importera till [!INCLUDE[d365fin](includes/d365fin_long_md.md)]. Mer information finns i [Så här konfigurerar du bankdatakonverteringstjänsten](bank-how-setup-bank-data-conversion-service.md).  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Om du vill | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner genom att importera ett kontoutdrag och stämma av bankkonton när alla betalningar är kopplade. |[Så här stämmer du av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md) |
| Koppla betalningar manuellt genom att visa detaljerad information om matchade data och förslag om att öppna kandidattransaktioner att koppla betalningar till. |[Så här granskar och kopplar du betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md) |
| Lös betalningar som inte kan kopplas automatiskt till deras relaterade öppna transaktioner. Till exempel för att beloppen skiljer sig eller för att en relaterad transaktion inte finns. |[Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koppla text på betalningar till specifika kund-, leverantörs- eller redovisningskonton för att alltid bokföra återkommande inbetalningar eller kostnader på dessa konton när det inte finns dokument att applicera dem på. |[Så här mappar du text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

