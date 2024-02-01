---
title: Batch-bokför förbrukning
description: 'Om bokföringsmetoden är Manuell, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournal.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="batch-post-production-consumption"></a>Batch-bokföra produktionsförbrukning

Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.  

> [!NOTE]
> Om du har markerat fältet **Begär plockning** på lagerställekortet för att ange att lagerstället kräver bearbetning av lagerplockning, behöver du inte använda det här batch-jobbet. [!INCLUDE[prod_short](includes/prod_short.md)] hanterar förbrukningen när du bokför lagerplockning. Mer information finns i [Plocka för produktion i grundläggande distributionslagerkonfigurationer](warehouse-how-to-pick-for-production.md).  

Du kan också ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder. Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Om du vill bokföra förbrukning för produktion av en eller flera rader

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **förbrukningsjournal** och väljer sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och om förbrukningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Använd åtgärden **Beräkna förbrukning** för att generera journalrader från produktionsorder baserat på faktiskt utflöde (den mängd färdiga varor som du har rapporterat) eller på förväntat utflöde (den mängd färdiga varor som förväntas produceras).

    > [!NOTE]
    > Om du har konfigurerat platskortet för att kräva bearbetning av lagerplockning kan endast kvantiteter som redan plockas genom en lageraktivitet anges i fältet **Antal** på sidan **Förbrukningsjournal** inte någon beräknad kvantitet.. Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Välj åtgärden **Bokför** om du vill bokföra förbrukningen. De relaterade varulagret minskas.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a>Se även

[Produktion](production-manage-manufacturing.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
