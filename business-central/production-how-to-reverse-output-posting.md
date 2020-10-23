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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b33b0642d8cee6e26edeeece47c8fceb72c2bfa1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921573"
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
