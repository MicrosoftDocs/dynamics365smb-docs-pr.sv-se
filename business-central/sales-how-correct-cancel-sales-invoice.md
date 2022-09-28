---
title: Korrigera eller annullera en bokförd försäljningsfaktura
description: Detta ämne beskriver hur du korrigerar, raderar, eller annullerar en bokförd försäljningsfaktura och kopplar en försäljningskreditnota.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 95cf36a9f48b3452bcc28e049c12ae310c58e2ee
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531033"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Korrigera eller makulera obetalda försäljningsfakturor

Du kan korrigera eller annullera en obetald bokförd försäljningsfaktura, förutsatt att den inte har levererats helt. Detta är användbart om du begår ett fel, eller om kunden begär ett ändring innan utleveransen har slutförts. I alla andra fall rekommenderar vi att du skapar en korrigerande försäljningskreditnota direkt. Mer information finns i [Så här skapar du en försäljningskreditnota från en bokförd försäljningsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> När en bokförd försäljningsfaktura har betalts helt eller delvis, kan du inte rätta eller annullera den från själva den bokförda försäljningsfakturan. I stället måste du manuellt skapa en försäljningskreditnota för att makulera försäljningen och för att ersätta kunden, alternaivt hanterat med en försäljningsreturorder. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).

Skillnaden mellan att annullera och att korrigera en bokförd försäljningsfaktura som inte har betalats eller levererats beskrivs i följande tabell.

| Åtgärd | Beskrivning |
| --- | --- |
| **Annullera** |Den bokförda försäljningsfakturan avbryts. En korrigerande försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. På den ursprungligen bokförda försäljningsfakturan har kryssrutorna **Annulerad** och **Betalad** markerats. |
| **Korrigera** |Den bokförda försäljningsfakturan annulleras. En ny försäljningsfaktura med samma information skapas, såvida inte den bokförda försäljningsordern har bokförts från en försäljningsorder. I så fall föreslår vi att du avbryter den bokförda försäljningsfakturan istället och sedan utför korrigeringen samt fortsätter försäljningsprocessen från den ursprungliga försäljningsordern. <br/><br/>Den nya försäljningsfakturan har ett annat antal än den ursprungliga försäljningsfakturan. En korrigerande försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. På den ursprungligen bokförda försäljningsfakturan har kryssrutorna **Annulerad** och **Betalad** markerats. |

När du uppdaterar eller avbryter en bokförd försäljningsfaktura gäller den korrigerande försäljningskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga försäljningsfakturan bokfördes. Det återför den bokförda försäljningsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av försäljningskreditnota för din verifieringskedja.  

> [!TIP]
> Om du har bokfört en förskottsfaktura för en försäljningsfaktura som du sedan korrigerar eller avbryter, måste du även korrigera eller avbryta förskottsbetalningen. Mer information finns i [Korrigera Förskottsbetalningar](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice"></a>Avbryta en bokförd försäljningsfaktura

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokförda försäljningsfakturor** och väljer sedan relaterad länk.  
2. Markera den bokförda försäljningsfakturan som du vill annullera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte avbryta den bokförda försäljningsfakturan, eftersom den redan har korrigerats eller annullerats.
3. På sidan **Bokförd försäljningsfaktura** väljer du åtgärden **Annullera**.

    En försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. Fältet **Avbruten** på den först bokförda försäljningsfakturan ändras till **Ja**.
4. Välj åtgärden **Visa korrigerande kreditnota** för att visa de bokförda försäljningskreditnotorna som annullerar den ursprungliga bokförda försäljningsfakturan.

### <a name="partial-invoice-posting-also-supported"></a>Delfakturabokföring stöds också

Om annulleringen är knuten till en delfakturabokföring uppdateras den ursprungliga försäljningsorderraden så att den återspeglar det annullerade fakturerade antalet. Fälten **Ant. att fakturera** och **Antal fakturerat** på den relaterade försäljningsorderraden återställs till värdena före delbokföringen.

## <a name="to-correct-a-posted-sales-invoice"></a>Korrigera en bokförd försäljningsfaktura

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokförda försäljningsfakturor** och väljer sedan relaterad länk.  
2. Markera den bokförda försäljningsfakturan som du vill korrigera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte rätta den bokförda försäljningsfakturan, eftersom den redan har korrigerats eller annullerats.
3. På sidan **Bokförd försäljningsfaktura** väljer du åtgärden **korrigera**.  

    > [!NOTE]
    > Om försäljningsfakturan bokfördes från en försäljningsorder rekommenderar vi att du *annullerar* försäljningsfakturan och sedan bearbetar korrigeringen från den ursprungliga försäljningsordern. Om den ursprungliga försäljningsordern har tagits bort, till exempel om den har levererats helt, kan du skapa en ny försäljningsorder genom att använda åtgärden **Kopiera dokument**. Mer information finns i [Så här skapar du en försäljningskreditnota genom att kopiera en bokförd försäljningsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. En ny försäljningsfaktura med samma information skapas där du kan göra rättningen. Fältet **Avbruten** på den först bokförda försäljningsfakturan ändras till **Ja**.

    En försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan.
5. Välj åtgärden **Visa korrigerande kreditnota** för att visa de bokförda försäljningskreditnotorna som annullerar den ursprungliga bokförda försäljningsfakturan.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
