---
title: Så här skapar du speditörer | Microsoft Docs
description: Du kan lägga upp en kod för och ange information om var och en av dina speditörer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd27caed8be1e7231f98964890fafed66c7bbbb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748224"
---
# <a name="set-up-shipping-agents"></a>Så här konfigurerar du speditörer
Du kan lägga upp en kod för och ange information om var och en av dina speditörer.  

Om du anger en Internet-adress för speditören och denne tillhandahåller godsupplysningstjänster på Internet kan du använda den automatiska funktionen för godsupplysning. Mer information finns i [Så här spårar du paket](sales-how-track-packages.md).

När du anger speditörer på dina försäljningsorder kan du också ange vilken typ av service varje speditör erbjuder.  
Du kan ange obegränsat antal tjänster för varje speditör, samt ange leveranstid för varje service.  

När en speditörsservice har kopplats till en försäljningsorderrad inkluderas leveranstiden för tjänsten i orderlöftesberäkningen för den raden. Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Så här lägger du upp en speditör  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **speditör** och välj sedan relaterad länk.  
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