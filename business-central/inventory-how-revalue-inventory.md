---
title: Skapa ny värdetransaktioner för artiklarna i lagret | Microsoft Docs
description: Beskriver hur du uppskattar eller skriver av värdetransaktionerna av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.search.forms: 5803,
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: edad8dcc23a204f4dcfabfa43a9c83918f63f416
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511552"
---
# <a name="revalue-inventory"></a>Omvärdera lager
Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.

## <a name="to-revalue-inventory"></a>Omvärdera lager
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **omvärderingsjournalen** och väljer sedan relaterad länk.
2. Välj åtgärden **Beräkna lagervärde**.
3. På sidan **Beräkna lagervärde** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj knappen **OK**.
5. På varje rad på sidan **Omvärderingsjournal** i fältet **Styckkostnad (omvärderad)** anger du den nya styckkostnaden. Du kan alternativt ange det nya totalbeloppet i fältet **Lagervärde (omvärderad)**.

    Relevanta fält uppdateras automatiskt. Lägg märke till att den faktiska förändringen av lagervärdet för den aktuella artikeltransaktionen visas i fältet **Belopp**. Detta belopp utgör skillnaden mellan värdena i fälten **Lagervärde (beräknat)** och **Lagervärde (omvärderat)**.
6. När du har slutfört alla rader i omvärderingsjournalen väljer du åtgärden **Bokför**.

Nya värdetransaktioner skapas nu för att visa omvärderingarna som du har bokfört. Du kan se de nya värdena på respektive artikelkort.

## <a name="see-also"></a>Se även
[Designdetaljer: Omvärdering](design-details-revaluation.md)  
[Lager](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]