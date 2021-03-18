---
title: Designdetaljer – Kostnadskomponenter | Microsoft Docs
description: Kostnadkomponenter är olika typer av kostnader som utgör värdet på en lagerökning eller lagerminskning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bf47da0a1ef2b4c8469f0311c04e14ef85e568a0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386980"
---
# <a name="design-details-cost-components"></a>Designdetaljer: Kostnadskomponenter
Kostnadkomponenter är olika typer av kostnader som utgör värdet på en lagerökning eller lagerminskning.  

 Följande tabell innehåller de olika kostnadskomponenterna och eventuella underordnade kostnadskomponenter som de består av.  

|Kostnadskomponent|Underordnad kostnadkomponent|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Direkt kostnad|Styckkostnad (direkt inköpspris)|Kostnad som kan spåras till en kostnadsbärare.|  
|Direkt kostnad|Fraktkostnad (artikelomkostnad)|Kostnad som kan spåras till en kostnadsbärare.|  
|Direkt kostnad|Försäkringskostnad (artikelomkostnad)|Kostnad som kan spåras till en kostnadsbärare.|  
|Indirekt kostnad||Kostnad som inte kan spåras till en kostnadsbärare.|  
|Varians|Inköpsvarians|Skillnaden mellan faktiska kostnader och standardkostnader, som endast bokförs för artiklar med värderingsprincipen **Standard**.|  
|Varians|Materialvarians|Skillnaden mellan faktiska kostnader och standardkostnader, som endast bokförs för artiklar med värderingsprincipen **Standard**.|  
|Varians|Kapacitetsvarians|Skillnaden mellan faktiska kostnader och standardkostnader, som endast bokförs för artiklar med värderingsprincipen **Standard**.|  
|Varians|Legotillverkning varians|Skillnaden mellan faktiska kostnader och standardkostnader, som endast bokförs för artiklar med värderingsprincipen **Standard**.|  
|Varians|Kapacitetsomkostnadsvarians|Skillnaden mellan faktiska kostnader och standardkostnader, som endast bokförs för artiklar med värderingsprincipen **Standard**.|  
|Varians|Produktionsomkostnadsvarians|Skillnaden mellan faktiska kostnader och standardkostnader, som endast bokförs för artiklar med värderingsprincipen **Standard**.|  
|Omvärdering||En avskrivning eller uppskrivning av det aktuella lagervärdet.|  
|Avrundning||Rester som orsakas av sättet som värderingen av lager minskar beräknas.|  

> [!NOTE]  
>  Frakt- och försäkringskostnader är artikelomkostnader som kan läggas till i en artikels kostnad när som helst. När du kör batchjobbet **Justera kost. – artikeltrans** uppdateras värdet på alla relaterade lagerminskningar därefter.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Varians](design-details-variance.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]