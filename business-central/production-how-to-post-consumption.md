---
title: 'Så här: batch-bokföra förbrukning | Microsoft Docs'
description: Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ad21fa7f0a18b3549bdab19c07e0065d5fb684dd
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759173"
---
# <a name="batch-post-production-consumption"></a>Batch-bokföra produktionsförbrukning
Om bokföringsmetoden är **Manuell** måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.

Du kan också ställa in systemet att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder. Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Om du vill bokföra förbrukning för produktion av en eller flera rader  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **förbrukningsjournal** och välj sedan relaterad länk.  
2.  Fyll i fälten med data om produktionsorden och om förbrukningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Om distributionslagret där komponenterna lagras har konfigurerats till att använda lagerställen men inte kräva bearbetning av plockning, kopplar du en lagerställeskod till journalraden för att ange var artiklarna ska tas från i distributionslagret. Mer information finns i [Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).  
3.  Välj åtgärden **Bokför** om du vill bokföra förbrukningen. De associerade artikeltransaktionerna misnkas.

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]