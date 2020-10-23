---
title: Korrigera eller annullera bokförda försäljningsfakturor | Microsoft Docs
description: Beskriver hur du korrigerar, raderar, eller annullerar en bokförd försäljningsfaktura och kopplar en försäljningskreditnota.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3803ce840569d1b1668db64879e68395ee6f3a65
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926303"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Korrigera eller makulera obetalda försäljningsfakturor

Du kan korrigera eller annullera en bokförd försäljningsfaktura. Det är användbart om du gör ett fel, eller om kunden begär ett ändring.

> [!NOTE]  
> När en bokförd försäljningsfaktura har betalts helt eller delvis, kan du inte rätta eller annullera den från själva den bokförda försäljningsfakturan. I stället måste du manuellt skapa en försäljningskreditnota för att makulera försäljningen och för att ersätta kunden, alternaivt hanterat med en försäljningsreturorder. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).

På sidan **Bokförd försäljningsfaktura** kan du välja åtgärden **Korrigera** eller **Avbryt** för att utföra de åtgärder som beskrivs i följande tabell.

| Åtgärd | Beskrivning |
| --- | --- |
| **Korrigera** |Den bokförda försäljningsfakturan avbryts. En ny försäljningsfaktura med samma information skapas. Du kan göra rättningen och sedan fortsätta försäljningsprocessen. Den nya försäljningsfakturan har ett annat antal än den ursprungliga försäljningsfakturan. En korrigerande försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. På den först bokförda försäljningsfakturan är kryssrutorna Avbruten och Betalad markerade. |
| **Annullera** |Den bokförda försäljningsfakturan avbryts. En korrigerande försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. På den först bokförda försäljningsfakturan är kryssrutorna Avbruten och Betalad markerade. |

När du uppdaterar eller avbryter en bokförd försäljningsfaktura gäller den korrigerande försäljningskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga försäljningsfakturan bokfördes. Det återför den bokförda försäljningsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av försäljningskreditnota för din verifieringskedja.  

> [!TIP]
> Om du har bokfört en förskottsfaktura för en försäljningsfaktura som du sedan korrigerar eller avbryter, måste du även korrigera eller avbryta förskottsbetalningen. Mer information finns i [Korrigera Förskottsbetalningar](finance-how-to-correct-prepayments.md).

## <a name="to-correct-a-posted-sales-invoice"></a>Korrigera en bokförd försäljningsfaktura

1. Välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda försäljningsfakturor** och välj sedan relaterad länk.  
2. Markera den bokförda försäljningsfakturan som du vill korrigera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte rätta den bokförda försäljningsfakturan, eftersom den redan har korrigerats eller annullerats.
3. På sidan **Bokförd försäljningsfaktura** väljer du åtgärden **korrigera**.  
4. En ny försäljningsfaktura med samma information skapas där du kan göra rättningen. Fältet **Avbruten** på den först bokförda försäljningsfakturan ändras till **Ja**.

    En försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan.
5. Välj åtgärden **Visa korrigerande kreditnota** för att visa de bokförda försäljningskreditnotorna som annullerar den ursprungliga bokförda försäljningsfakturan.

## <a name="to-cancel-a-posted-sales-invoice"></a>Avbryta en bokförd försäljningsfaktura

1. Välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda försäljningsfakturor** och välj sedan relaterad länk.  
2. Markera den bokförda försäljningsfakturan som du vill annullera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte avbryta den bokförda försäljningsfakturan, eftersom den redan har korrigerats eller annullerats.
3. På sidan **Bokförd försäljningsfaktura** väljer du åtgärden **Annullera**.

    En försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. Fältet **Avbruten** på den först bokförda försäljningsfakturan ändras till **Ja**.
4. Välj åtgärden **Visa korrigerande kreditnota** för att visa de bokförda försäljningskreditnotorna som annullerar den ursprungliga bokförda försäljningsfakturan.

### <a name="partial-invoice-posting-also-supported"></a>Delfakturabokföring stöds också

Om annulleringen är knuten till en delfakturabokföring uppdateras den ursprungliga försäljningsorderraden så att den återspeglar det annullerade fakturerade antalet. Fälten **Ant. att fakturera** och **Antal fakturerat** på den relaterade försäljningsorderraden återställs till värdena före delbokföringen.

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
