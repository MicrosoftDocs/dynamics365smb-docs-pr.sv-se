---
title: Så här skapar du produktionsorder från försäljningsorder
description: Lär dig de olika sätten att skapa produktionsorder för producerade artiklar direkt från försäljningsorder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
ms.service: dynamics-365-business-central
---
# <a name="create-production-orders-from-sales-orders"></a>Så här skapar du produktionsorder från försäljningsorder

Du kan skapa produktionsorder för producerade artiklar direkt från försäljningsorder.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Så här skapar du produktionsorder från försäljningsorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Markera den försäljningsorder som du vill skapa en produktionsorder för.  
3. Välj åtgärden **Planerad**. På sidan **Försäljningsorderplanering** kan du visa dispositionen för artikeln.  
4. Välj åtgärden **Skapa prod.order**.  
5. Välj status och ordertyp.  
6. Tryck på knappen **Ja** för att skapa en eller flera produktionsorder för raderna som har **Prod.order** i fältet **Återanskaffningssystem**.

    > [!NOTE]  
    > Efterfrågerader som har **Prod.order** i fältet **Återanskaffningssystem**, motsvarar underliggande produktionsorder. När du har skapat dessa produktionsorder måste du komma ihåg att identifiera eventuella ouppfyllda komponentefterfrågan för dem. Använd sidan **Orderplanering** eller åtgärden **Omplanera** för att identifiera ouppfylld efterfrågan.
    >
    > När du skapar produktionsorder för försäljningsorder med sidan försäljningsorderplanering tillämpas order-till-order-länkar mellan efterfrågan och tillgång. När order-till-order-länkar finns tar inte planeringssystemet med kopplad tillgång eller lager i balanseringen. Om du vill ha mer information om balansering går du till [Order-till-order-länkar](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## <a name="order-type"></a>Ordertyp

I följande tabell beskrivs två sätt att skapa produktionsorder.

|Alternativ|Beskrivning|
|------|-----------|
|Artikelorder|En produktionsorder skapas för varje artikel som representeras av en rad i fönstret **Försäljningsorderplanering**.|
|Projektorder|En produktionsorder med flera rader skapas för varje artikel som representeras av en rad i fönstret **Försäljningsorderplanering**. När du använder projektorder innehåller fältet **Ursprungstyp** för produktionsordern **Försäljningshuvud**. Ordern innehåller en rad för varje försäljningsradartikel som måste produceras.|

## <a name="see-also"></a>Se även

[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
