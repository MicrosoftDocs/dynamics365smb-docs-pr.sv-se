---
title: "Så här skapar du speditörer | Microsoft Docs"
description: "Du kan lägga upp en kod för och ange information om var och en av dina speditörer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 49ed631f56730bce647dfe9fc75be2c2fc6b9359
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-shipping-agents"></a>Så här konfigurerar du speditörer
Du kan lägga upp en kod för och ange information om var och en av dina speditörer.  

Om du anger en Internet-adress för speditören och denne tillhandahåller godsupplysningstjänster på Internet kan du använda den automatiska funktionen för godsupplysning. Mer information finns i [Så här spårar du paket](sales-how-track-packages.md).

När du anger speditörer på dina försäljningsorder kan du också ange vilken typ av service varje speditör erbjuder.  
Du kan ange obegränsat antal tjänster för varje speditör, samt ange leveranstid för varje service.  

När en speditörsservice har kopplats till en försäljningsorderrad inkluderas leveranstiden för tjänsten i orderlöftesberäkningen för den raden. Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Så här lägger du upp en speditör  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Speditörer** och välj sedan relaterad länk.  
2.  Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Välj åtgärden **Speditörsservice**.
4. I **Speditörsservice** fyller du i fälten efter behov.

> [!NOTE]  
>  Om du tar bort en speditör på orderraden tas även speditörsservicekoden bort. Därefter omberäknas innehållet i fält som delvis baserats på speditörsservicen.  

## <a name="see-also"></a>Se även
[Spåra paket](sales-how-track-packages.md)    
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

