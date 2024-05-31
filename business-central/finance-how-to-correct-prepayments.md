---
title: Korrigera förskottsbetalningar
description: Du kan korrigera en order efter att du har bokfört en förskottsfaktura för ordern och lägger till nya rader i en order efter att ha utfärdat en förskottsbetalning.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '44, 48, 42, 50, 52, 9305, 9307'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="correct-prepayments"></a>Korrigera förskottsbetalningar

Du kan korrigera en order efter att du har bokfört en förskottsfaktura för den. Du kan lägga till nya rader på en order efter att du har skickat ut en förskottsbetalning, och sedan kan du bokföra en ny förskottsfaktura. Du kan däremot inte ta bort en rad från en order efter en förskottsbetalning har fakturerats för raden.  

> [!TIP]
> Om du har bokfört en förskottsfaktura för en försäljningsfaktura som du sedan korrigerar eller avbryter, måste du även korrigera eller avbryta förskottsbetalningen.

## <a name="to-correct-a-prepayment"></a>Så här korrigerar du en förskottsbetalning

I följande procedur beskrivs hur du skapar en kreditnota för förskottsbetalning för att annullera alla fakturerade förskottsbetalningar för en order.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Öppna den aktuella försäljningsordern.
3. Välj åtgärden **Förskottsbetalning** och välj sedan åtgärden **Bokför kreditnota för förskottsbetalning** eller åtgärden **Bokför och skriv ut kreditnota för förskottsbetalning**.  
4. På sidan **Försäljningskreditnota** fortsätter du att korrigera de aktuella transaktionerna för varje försäljningskreditnota. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Om du vill minska antalet i fältet **Radbelopp** måste du först öka procentandelen för förskottsbetalning på raden så att värdet i fältet **Radbelopp, förskottsbetalning** inte blir lägre än värdet i fältet **Fakturabelopp, förskottsbetalning**.

5. För att göra en förskottsfaktura för eventuella nya rader i försäljningsmeddelandet väljer du åtgärden **Förskottsbetalning** och väljer sedan åtgärden **Bokför förskottsfaktura** eller åtgärden **Bokför och skriv ut faktura på förskottsbet.**.  
6. Om du vill utfärda en ytterligare förskottsfaktura på minst en rad och bokför sedan förskottsfakturan. En ny faktura skapas för skillnaden mellan förskottsbetalningsbeloppen som fakturerats och de nya förskottsbetalningsbeloppen.  

## <a name="see-also"></a>Se även

[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Genomgång: Konfigurera och fakturera förskottsbetalning för försäljning](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
