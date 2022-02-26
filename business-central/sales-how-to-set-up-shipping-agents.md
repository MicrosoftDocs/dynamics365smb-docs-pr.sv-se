---
title: Så här lägger du upp speditörer
description: Lär dig hur du lägger upp en kod för var och en av dina speditörer och anger beskrivande information om var och en av dem och de tjänster de tillhandahåller.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 1e74be125909db7f7d1c4301a33da1b12648e70a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440234"
---
# <a name="set-up-shipping-agents"></a>Så här konfigurerar du speditörer
Du kan lägga upp en kod för och ange information om var och en av dina speditörer.  

Om du anger en Internet-adress för speditören och denne tillhandahåller godsupplysningstjänster på Internet kan du använda den automatiska funktionen för godsupplysning. Mer information finns i [Så här spårar du paket](sales-how-track-packages.md).

När du anger speditörer på dina försäljningsorder kan du också ange vilken typ av service varje speditör erbjuder.  
Du kan ange obegränsat antal tjänster för varje speditör, samt ange leveranstid för varje service.  

När en speditörsservice har kopplats till en försäljningsorderrad inkluderas leveranstiden för tjänsten i orderlöftesberäkningen för den raden. Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Så här lägger du upp en speditör  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **speditörer** och väljer sedan relaterad länk.  
2.  Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Välj åtgärden **Speditörsservice**.
4. I **Speditörsservice** fyller du i fälten efter behov.

> [!NOTE]  
>  Om du tar bort en speditör på orderraden tas även speditörsservicekoden bort. Därefter omberäknas innehållet i fält som delvis baserats på speditörsservicen.  

## <a name="see-also"></a>Se även
[Så här definierar du leveransmetoder](sales-how-set-up-shipment-methods.md)  
[Spåra paket](sales-how-track-packages.md)    
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]