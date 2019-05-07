---
title: Designdetaljer - Söka efter dimensionskombinationer | Microsoft Docs
description: När du stänger en sida efter att ha redigerat en uppsättning dimensioner utvärderar Business Central huruvida den redigerade uppsättningen dimensioner finns. Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: cde720526fdad4c9e4352f08f649d6bd3fc51540
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "912369"
---
# <a name="design-details-searching-for-dimension-combinations"></a>Designdetaljer: Söka efter dimensionskombinationer
När du stänger en sida när du har redigerat en uppsättning med dimensioner utvärderar [!INCLUDE[d365fin](includes/d365fin_md.md)] om den redigerade uppsättningen med dimensioner finns. Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras.  

## <a name="building-search-tree"></a>Bygga sökträd  
 Tabell 481 **Trädnod för dimensionsuppsättning** används när [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning redan finns i tabell 480 **Dimensionsuppsättnings transaktion**. Utvärderingen utförs av rekursivt genomgång av sökträdet från toppnivån nummer 0. Den översta nivån 0 representerar en dimension utan dimensionsuppsättningstransaktioner. De underordnade uppsättningarna till denna dimensionsuppsättning representerar dimensionsuppsättningar med endast en dimensionsuppsättningstransaktion. De underordnade uppsättningarna till dessa dimensionsuppsättningar representerar dimensionsuppsättningar med två underordnade, och så vidare.  

### <a name="example-1"></a>Exempel 1  
 Följande diagram representerar ett sökträd med sex dimensionsuppsättningar. Endast den särskiljande dimensionsuppsättningstransaktionen visas i diagrammet.  

 ![Exempel på dimensionsträdstruktur](media/nav2013_dimension_tree.png "Exempel på dimensionsträdstruktur")  

 Följande tabell beskrivs en fullständig lista över dimensionsuppsättningstransaktioner som utgör varje dimensionsuppsättning.  

|Dimensionsuppsättningar|Dimensionsuppsättningstransaktioner|  
|--------------------|---------------------------|  
|Frågesvar 0|Ingen|  
|Frågesvar 1|AREA 30|  
|Frågesvar 2|AREA 30, DEPT ADM|  
|Frågesvar 3|AREA 30, DEPT PROD|  
|Frågesvar 4|AREA 30, DEPT ADM, PROJ VW|  
|Frågesvar 5|AREA 40|  
|Frågesvar 6|AREA 40, PROJ VW|  

### <a name="example-2"></a>Exempel 2  
 I det här exemplet visas hur [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning som består av dimensionsuppsättningstransaktionerna AREA 40, DEPT PROD finns.  

 Först [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdateras även tabellen **Trädnod för dimensionsuppsättning** för att se till att sökträdet ser ut som på bilden. På så sätt blir dimensionsuppsättning 7 underordnad dimensionsuppsättning 5.  

 ![Exempel på dimensionsträdstruktur i NAV 2013](media/nav2013_dimension_tree_example2.png "Exempel på dimensionsträdstruktur i NAV 2013")  

### <a name="finding-dimension-set-id"></a>Hitta dimensionsuppsättnings-ID  
 På en begreppsmässig nivå kombineras **Överordnat ID**, **Dimension**, och **Dimensionsvärde**,  i sökträdet, och används som primärnyckel eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] korsar trädet i samma ordning som dimensionstransaktionerna. Funktionen GET (record) används för att söka efter dimensionuppsättnings-ID. Följande kodexempel visar hur du hittar dimensionsuppsättning-ID när det finns tre dimensionsvärden.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

För att bevara möjligheten för [!INCLUDE[d365fin](includes/d365fin_md.md)] byta namn på en dimension och ett dimensionsvärde utökas tabellen 349 **Dimensionsvärde** med heltalsfältet **Dimensionsvärde-ID**. Den här tabellen omvandlar fältparen **Dimension** och **Dimensionsvärde** till ett heltalsvärde. När du byter namn på dimensionen och dimensionsvärdet ändras inte heltalsvärdet.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Se även  
 [HÄMTA funktionen (post)](/dynamics-nav/GET-Function--Record-)    
 [Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md)   
 [Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
 [Designdetaljer: Kodenhet 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
 [Designdetaljer: Kodexempel på ändrade mönster i ändringar](design-details-code-examples-of-changed-patterns-in-modifications.md)
