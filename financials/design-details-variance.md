---
title: Designdetaljer - Varians | Microsoft Docs
description: "Varians definieras som skillnaden mellan den faktiska kostnaden och standardkostnaden, enligt beskrivningen i följande formel."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04faa28799288e272da93c60cbb90fa19fd190f0
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

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

 ![Köpa avvikelseberäkning](media/design_details_inventory_costing_11_purchase_variance.png "design_details_inventory_costing_11_purchase_variance")  

## <a name="determining-the-standard-cost"></a>Fastställa standardkostnaden  
 Standardkostnaden används när du beräknar avvikelse och beloppet som ska kapitaliseras. Eftersom standardkostnaden kan ändras med tiden på grund av manuell uppdateringsberäkning måste du ha en tidpunkt då standardkostnaden är fast för avvikelseberäkning. Det här är punkten där lagerökningen faktureras. För producerade eller monterade artiklar punkten, är den punkt när standardkostnaden fastställs den punkt när kostnaden justeras.  

 Följande tabell visar hur olika kostnadsandelar beräknas för tillverkade och monterade artiklar när du använder funktionen Beräkna standardkostnad.  

|Kostnadsandel|Inköpt artikel|Producerad/monterad artikel|  
|----------------|--------------------|------------------------------|  
|**Standardkostnad**||En-nivå materialkostnad + En-nivå kapacitetskostnad + En-nivå underleverantörkost. + En-nivå kap.overheadkost. + En-nivå mat.overheadkost.|  
|**En-nivå materialkostnad**|Styckkostnad|![Formel 1](media/design_details_inventory_costing_11_equation_1.png "design_details_inventory_costing_11_equation_1")|  
|**En-nivå kapacitetskostnad**|Ej tillämpbart|![Formel 2](media/design_details_inventory_costing_11_equation_2.png "design_details_inventory_costing_11_equation_2")|  
|**En-nivå underleverantörkost.**|Ej tillämpbart|![Formel 3](media/design_details_inventory_costing_11_equation_3.png "design_details_inventory_costing_11_equation_3")|  
|**En-nivå kap.overheadkost.**|Ej tillämpbart|![Formel 4](media/design_details_inventory_costing_11_equation_4.png "design_details_inventory_costing_11_equation_4")|  
|**En-nivå mat.overheadkost.**|Ej tillämpbart|(En-nivå materialkostnad + En-nivå kapacitetskostnad + En-nivå underlev.kost.) * Indirekt kostnad % / 100 + Omkostnader|  
|**Uppsum. materialkost.**|Styckkostnad|![Formel 5](media/design_details_inventory_costing_11_equation_5.png "design_details_inventory_costing_11_equation_5")|  
|**Uppsum. kapacitetskost.**|Ej tillämpbart|![Formel 6](media/design_details_inventory_costing_11_equation_6.png "design_details_inventory_costing_11_equation_6")|  
|**Uppsummerad utlegokostnad**|Ej tillämpbart|![Formel 7](media/design_details_inventory_costing_11_equation_7.png "design_details_inventory_costing_11_equation_7")|  
|**Uppsum. kap.overh.kostnad**|Ej tillämpbart|![Formel 8](media/design_details_inventory_costing_11_equation_8.png "design_details_inventory_costing_11_equation_8")|  
|**Uppsum. tillverk.overh.kost**|Ej tillämpbart|![Formel 9](media/design_details_inventory_costing_11_equation_9.png "design_details_inventory_costing_11_equation_9")|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: värderingsprinciper](design-details-costing-methods.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

