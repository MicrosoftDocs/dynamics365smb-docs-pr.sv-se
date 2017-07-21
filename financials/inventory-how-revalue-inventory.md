---
title: "Skapa ny värdetransaktioner för artiklarna i lagret | Microsoft Docs"
description: "Beskriver hur du uppskattar eller skriver av värdetransaktionerna av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1935f53db068047921e44109cd4b23bbb51f0890
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-revalue-inventory"></a>Så här omvärderar du lager
Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.

## <a name="to-revalue-inventory"></a>Omvärdera lager
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Omvärderingsjournal** och välj sedan relaterad länk.
2. Välj åtgärden **Beräkna lagervärde**.
3. I fönstret **Beräkna lagervärde** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj **OK**.
5. På varje rad i fönstret **Omvärderingsjournal** i fältet **Styckkostnad (omvärderad)** anger du den nya styckkostnaden. Du kan alternativt ange det nya totalbeloppet i fältet **Lagervärde (omvärderad)**.

    Relevanta fält uppdateras automatiskt. Lägg märke till att den faktiska förändringen av lagervärdet för den aktuella artikeltransaktionen visas i fältet **Belopp**. Detta belopp utgör skillnaden mellan värdena i fälten **Lagervärde (beräknat)** och **Lagervärde (omvärderat)**.
6. När du har slutfört alla rader i omvärderingsjournalen väljer du åtgärden **Bokför**.

Nya värdetransaktioner skapas nu för att visa omvärderingarna som du har bokfört. Du kan se de nya värdena på respektive artikelkort.

## <a name="see-also"></a>Se även
[Lagersaldo](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

