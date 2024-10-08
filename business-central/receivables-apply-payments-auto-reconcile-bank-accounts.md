---
title: Stämma av bankkonton koppla betalningar
description: 'Beskriver uppgifter för att stämma av din bank, kundreskontra och leverantörsreskontra, bokföra inbetalningar eller kostnader och tillämpa betalningar automatiskt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
---

# <a name="apply-payments-automatically-and-reconciling-bank-accounts"></a>Koppla betalningar automatiskt och stämma av bankkonton
Du måste regelbundet stämma av dina bankkonton, kundfordringskonton och konton för leverantörsreskontra genom att koppla betalningar som är registrerade i banken till dessas motsvarande öppna (obetalda) fakturor och kreditnotor eller andra öppna transaktioner i [!INCLUDE[prod_short](includes/prod_short.md)].  

Du kan utföra denna aktivitet på sidan **Betalningsavstämningsjournal** genom att till exempel importera ett kontoutdrag eller en feed för att snabbt registrera utbetalningarna. Betalningarna används för att öppna leverantörs- eller kundreskontratransaktioner baserat på matchningar mellan betalningstexten och transaktionsinformation. Du kan granska och ändra automatiska kopplingar, innan du bokför journalen. Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen. Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.

På sidan **Betalningskopplingsregler** kan du sätta upp prioriterade regler som styr hur betalningstext automatiskt matchas med inmatningsinformation.

Du kan också stämma av bankkonton utan att samtidigt utföra betalningar. Du utför detta arbete på sidan **Bankkontoavstämning**. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera Envestnet Yodlee Bank Feeds-tjänsten och sedan länka dina bankkonton till relaterade onlinebankkonton. Mer information finns [i konfigurera bankfeedstjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan också importera bankutdragsfiler i komma- eller semikolonavgränsat format (.CSV). Använd **Konfigurera importformat för en kontoutdragsfil** assisterad installation för att definiera importformat för kontoutdrag och bifoga formatet till ett bankkonto. Du kan sedan använda dessa format när du importerar bankutdrag på sidan **Bankkontoavstämning**.

Du kan alternativt använda tillägget AMC Banking 365 Fundamentals om du vill konvertera en kontoutdrags i valfritt format till en dataström som du kan importera till [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns [i använda tillägget AMC banking 365 fundamentals](ui-extensions-amc-banking.md).  

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.  

| Till | Gå till |
| --- | --- |
| Koppla betalningar för att öppna kund- eller leverantörsreskontratransaktioner genom att importera ett kontoutdrag och stämma av bankkonton när alla betalningar är kopplade. |[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md) |
| Koppla betalningar manuellt genom att visa detaljerad information om matchade data och förslag om att öppna kandidattransaktioner att koppla betalningar till. |[Så här granskar och kopplar du betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md) |
| Lös betalningar som inte kan kopplas automatiskt till deras relaterade öppna transaktioner. Till exempel för att beloppen skiljer sig eller för att en relaterad transaktion inte finns. |[Stämma av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koppla text på betalningar till specifika kund-, leverantörs- eller redovisningskonton för att alltid bokföra återkommande inbetalningar eller kostnader på dessa konton när det inte finns dokument att applicera dem på. |[Så här mappar du text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Ange reglerna som styr hur betalningar/banktransaktioner automatiskt ska kopplas till sina relaterade öppna transaktioner när du använder funktionen **Koppla automatiskt** på sidan **Betalningsavstämningsjournal**.|[Konfigurera regler för automatisk koppling av betalningar](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-also"></a>Se även
[Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
