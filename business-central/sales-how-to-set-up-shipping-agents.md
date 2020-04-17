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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d6a4bac4d540a65cc164029b23b063c8c9dbc1fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192666"
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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
