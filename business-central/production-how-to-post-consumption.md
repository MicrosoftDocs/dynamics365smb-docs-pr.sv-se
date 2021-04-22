---
title: Batch-bokför förbrukning
description: Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787908"
---
# <a name="batch-post-production-consumption"></a>Batch-bokföra produktionsförbrukning

Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.  

>[!NOTE]
> Om du har markerat fältet **Begär plockning** på lagerställekortet för att ange att lagerstället kräver bearbetning av lagerplockning, behöver du inte använda det här batch-jobbet. [!INCLUDE[prod_short](includes/prod_short.md)] hanterar förbrukningen när du bokför lagerplockning. Mer information finns i [Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations). 

Du kan också ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder. Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Om du vill bokföra förbrukning för produktion av en eller flera rader

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **förbrukningsjournal** och välj sedan relaterad länk.  
2.  Fyll i fälten med data om produktionsorden och om förbrukningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Använd åtgärden **Beräkna förbrukning** för att generera journalrader från produktionsorder baserat på faktiskt utflöde (den mängd färdiga varor som du har rapporterat) eller på förväntat utflöde (den mängd färdiga varor som förväntas produceras).

    > [!NOTE]
    > Om du har konfigurerat platskortet för att kräva bearbetning av lagerplockning kan endast kvantiteter som redan plockas genom en lageraktivitet anges i fältet **Antal** på sidan **Förbrukningsjournal** inte någon beräknad kvantitet.. Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3.  Välj åtgärden **Bokför** om du vill bokföra förbrukningen. De relaterade varulagret minskas.



## <a name="see-also"></a>Se även

[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
