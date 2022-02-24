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
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 85f7feccd0eefa7c709ce077a8b01b049fc675c8
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2954063"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Koppla utbetalningar automatiskt och stämma av bankkonton
Du måste regelbundet stämma av dina bankkonton, kundfordringskonton och konton för leverantörsreskontra genom att koppla betalningar som är registrerade i banken till dessas motsvarande öppna (obetalda) fakturor och kreditnotor eller andra öppna transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du kan utföra denna aktivitet på sidan **Betalningsavstämningsjournal** genom att till exempel importera ett kontoutdrag eller en feed för att snabbt registrera utbetalningarna. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på matchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra automatiska kopplingar, innan du bokför journalen. Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen. Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.

Logiken som styr hur betalningstexten matchas automatiskt med information om inmatning ställs in på sidan **Regler för betalningskoppling** som ett antal prioriterade regler som du kan redigera.

Du kan också stämma av bankkonton utan att samtidigt utföra betalningar. Du utför detta arbete på sidan **Bankkontoavstämning**. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).   

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera Envestnet Yodlee Bank Feeds-tjänsten och sedan länka dina bankkonton till relaterade onlinebankkonton. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

Du kan alternativt använda tillägget AMC Banking 365 Fundamentals om du vill få en bankutdragsfil i något format konverterad till en dataström som du kan importera till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Om du vill | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner genom att importera ett kontoutdrag och stämma av bankkonton när alla betalningar är kopplade. |[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md) |
| Koppla betalningar manuellt genom att visa detaljerad information om matchade data och förslag om att öppna kandidattransaktioner att koppla betalningar till. |[Så här granskar och kopplar du betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md) |
| Lös betalningar som inte kan kopplas automatiskt till deras relaterade öppna transaktioner. Till exempel för att beloppen skiljer sig eller för att en relaterad transaktion inte finns. |[Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koppla text på betalningar till specifika kund-, leverantörs- eller redovisningskonton för att alltid bokföra återkommande inbetalningar eller kostnader på dessa konton när det inte finns dokument att applicera dem på. |[Så här mappar du text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Ange reglerna som styr hur betalningar/banktransaktioner automatiskt ska kopplas till sina relaterade öppna transaktioner när du använder funktionen **Koppla automatiskt** på sidan **Betalningsavstämningsjournal**.|[Definiera regler för automatisk koppling av betalningar](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
