---
title: Så här återför du en utflödesbokföring | Microsoft Docs
description: Det finns tillfällen när bokföring av utflöde måste återföras. Ett exempel på detta är om det inträffar ett informationsregistreringsfel och ett felaktigt utflödesbelopp bokförs i en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2cdda8a01d6391f97bfae5600ce35d2ab989ae54
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877855"
---
# <a name="reverse-output-posting"></a>Återföra bokföring av utflöde
Det finns tillfällen när bokföring av utflöde måste återföras. Ett exempel på detta är om det inträffar ett informationsregistreringsfel och ett felaktigt utflödesbelopp bokförs i en produktionsorder.  

## <a name="to-reverse-an-output-posting"></a>Så här återför du en utflödesbokföring  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk. Välj din batch.  
2. Fyll i fälten om det behövs. Mer information finns i [Batch-bokför utflöde och körtider](production-how-to-post-output-quantity.md).
3.  I fältet **Kopplas till löpnr** väljer du den tillhörande artikeltransaktionen. Kapaciteten och artikeltransaktionerna återförs.  
4. Bokför återföringen genom att bokföra journalen.  

Transaktionerna i utflödesjournalen bokförs som en positiv justering i artikeltransaktionen.  

## <a name="see-also"></a>Se även  
 [Produktion](production-manage-manufacturing.md)    
 [Ställa in Produktion](production-configure-production-processes.md)  
 [Planerad](production-planning.md)      
 [Lager](inventory-manage-inventory.md)  
 [Inköp](purchasing-manage-purchasing.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
