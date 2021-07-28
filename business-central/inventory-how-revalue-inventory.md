---
title: Skapa ny värdetransaktioner för artiklarna i lagret | Microsoft Docs
description: Beskriver hur du uppskattar eller skriver av värdetransaktionerna av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 01710b23c56634b91b86f3f1c6e6c87415a787c6
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435603"
---
# <a name="revalue-inventory"></a>Omvärdera lager
Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.

## <a name="to-revalue-inventory"></a>Omvärdera lager
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **omvärderingsjournalen** och väljer sedan relaterad länk.
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