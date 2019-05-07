---
title: Skapa ny värdetransaktioner för artiklarna i lagret | Microsoft Docs
description: Beskriver hur du uppskattar eller skriver av värdetransaktionerna av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 602381b34a057120cc53deca4dd293f939777dc5
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2019
ms.locfileid: "939017"
---
# <a name="revalue-inventory"></a>Omvärdera lager
Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.

## <a name="to-revalue-inventory"></a>Omvärdera lager
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Omvärderingsjournal** och välj sedan relaterad länk.
2. Välj åtgärden **Beräkna lagervärde**.
3. På sidan **Beräkna lagervärde** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj knappen **OK**.
5. På varje rad på sidan **Omvärderingsjournal** i fältet **Styckkostnad (omvärderad)** anger du den nya styckkostnaden. Du kan alternativt ange det nya totalbeloppet i fältet **Lagervärde (omvärderad)**.

    Relevanta fält uppdateras automatiskt. Lägg märke till att den faktiska förändringen av lagervärdet för den aktuella artikeltransaktionen visas i fältet **Belopp**. Detta belopp utgör skillnaden mellan värdena i fälten **Lagervärde (beräknat)** och **Lagervärde (omvärderat)**.
6. När du har slutfört alla rader i omvärderingsjournalen väljer du åtgärden **Bokför**.

Nya värdetransaktioner skapas nu för att visa omvärderingarna som du har bokfört. Du kan se de nya värdena på respektive artikelkort.

## <a name="see-also"></a>Se även
[Designdetaljer: Omvärdering](design-details-revaluation.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
