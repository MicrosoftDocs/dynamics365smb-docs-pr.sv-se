---
title: Designdetaljer - Kostnadskomponenter | Microsoft Docs
description: Kostnadkomponenter är olika typer av kostnader som utgör värdet på en lagerökning eller lagerminskning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6cd1d8ef57a206bfa077d28c70e04c4032ead0fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307282"
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
>  Frakt- och försäkringskostnader är artikelomkostnader som kan läggas till i en artikels kostnad när som helst. När du kör batchjobbet **Justera kost. - artikeltrans** uppdateras värdet på alla relaterade lagerminskningar därefter.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Varians](design-details-variance.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
