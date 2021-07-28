---
title: Designdetaljer – Varians | Microsoft Docs
description: Varians definieras som skillnaden mellan den faktiska kostnaden och standardkostnaden, enligt beskrivningen i följande formel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 3b6ec6cbd2ebef6ff2cd44a49284821485d63f6f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439566"
---
# <a name="design-details-variance"></a>Designdetaljer: Varians
Varians definieras som skillnaden mellan den faktiska kostnaden och standardkostnaden, enligt beskrivningen i följande formel.  

 faktisk kostnad – standardkostnad = varians  

 Om den faktiska kostnaden ändra, till exempel eftersom du bokför en artikelomkostnad på ett senare datum, kommer variansen att uppdateras därefter.  

> [!NOTE]  
>  Omvärderingen påverkar inte avvikelseberäkningen, eftersom omvärderingen endast ändrar lagervärdet.  

## <a name="example"></a>Exempel  
 Följande exempel visar hur avvikelser beräknas för inköpta artiklar. Det baseras på följande scenario:  

1.  Användaren köper en artikel för BVA 90,00, men standardkostnaden är BVA 100,00. Inköpsvariansen är -10,00 BVA.  
2.  BVA 10,00 krediteras på inköpsvarianskontot.  
3.  Användaren bokför en artikelomkostnad på BVA 20,00. På så sätt ökas den faktiska kostnaden till 110,00 BVA, och värdet för inköpsvariansen blir 10,00 BVA.  
4.  BVA 20,00 krediteras på inköpsvarianskontot. På så sätt blir nettoinköpsvariansen 10,00 BVA.  
5.  Användaren omvärderar artikeln från BVA 100,00 till BVA 70,00. Det påverkar inte avvikelseberäkningen,bara lagervärdet.  

 Följande tabell visar de resulterande värdetransaktionerna.  

 ![Beräkning av inköpsvarians.](media/design_details_inventory_costing_11_purchase_variance.png "Beräkning av inköpsvarians")  

## <a name="determining-the-standard-cost"></a>Fastställa standardkostnaden  
 Standardkostnaden används när du beräknar avvikelse och beloppet som ska kapitaliseras. Eftersom standardkostnaden kan ändras med tiden på grund av manuell uppdateringsberäkning måste du ha en tidpunkt då standardkostnaden är fast för avvikelseberäkning. Det här är punkten där lagerökningen faktureras. För producerade eller monterade artiklar punkten, är den punkt när standardkostnaden fastställs den punkt när kostnaden justeras.  

 Följande tabell visar hur olika kostnadsandelar beräknas för tillverkade och monterade artiklar när du använder funktionen Beräkna standardkostnad.  

|Kostnadsandel|Inköpt artikel|Producerad/monterad artikel|  
|----------------|--------------------|------------------------------|  
|**Standardkostnad**||En-nivå materialkostnad + En-nivå kapacitetskostnad + En-nivå underleverantörkost. + En-nivå kap.overheadkost. + En-nivå mat.overheadkost.|  
|**En-nivå materialkostnad**|Styckkostnad|![Ekvation 1.](media/design_details_inventory_costing_11_equation_1.png "Ekvation 1")|  
|**En-nivå kapacitetskostnad**|Ej tillämpbart|![Ekvation 2.](media/design_details_inventory_costing_11_equation_2.png "Ekvation 2")|  
|**En-nivå underleverantörkost.**|Ej tillämpbart|![Ekvation 3.](media/design_details_inventory_costing_11_equation_3.png "Ekvation 3")|  
|**En-nivå kap.overheadkost.**|Ej tillämpbart|![Ekvation 4.](media/design_details_inventory_costing_11_equation_4.png "Ekvation 4")|  
|**En-nivå mat.overheadkost.**|Ej tillämpbart|(En-nivå materialkostnad + En-nivå kapacitetskostnad + En-nivå underlev.kost.) * Indirekt kostnad % / 100 + Omkostnader|  
|**Uppsum. materialkost.**|Styckkostnad|![Ekvation 5.](media/design_details_inventory_costing_11_equation_5.png "Ekvation 5")|  
|**Uppsum. kapacitetskost.**|Ej tillämpbart|![Ekvation 6.](media/design_details_inventory_costing_11_equation_6.png "Ekvation 6")|  
|**Uppsummerad utlegokostnad**|Ej tillämpbart|![Ekvation 7.](media/design_details_inventory_costing_11_equation_7.png "Ekvation 7")|  
|**Uppsum. kap.overh.kostnad**|Ej tillämpbart|![Ekvation 8.](media/design_details_inventory_costing_11_equation_8.png "Ekvation 8")|  
|**Uppsum. tillverk.overh.kost**|Ej tillämpbart|![Ekvation 9.](media/design_details_inventory_costing_11_equation_9.png "Ekvation 9")|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: värderingsprinciper](design-details-costing-methods.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]