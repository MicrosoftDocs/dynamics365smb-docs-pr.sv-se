---
title: "Designdetaljer - Söka efter dimensionskombinationer | Microsoft Docs"
description: "När du stänger ett fönster när du har redigerat en uppsättning med dimensioner utvärderar [!INCLUDE[d365fin](includes/d365fin_md.md)] om den redigerade uppsättningen med dimensioner finns. Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras."
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
ms.openlocfilehash: 9e36a8a1a5eeede5023da32bcb40a06042173fb4
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-searching-for-dimension-combinations"></a>Designdetaljer: Söka efter dimensionskombinationer
När du stänger ett fönster när du har redigerat en uppsättning med dimensioner utvärderar [!INCLUDE[d365fin](includes/d365fin_md.md)] om den redigerade uppsättningen med dimensioner finns. Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras.  

## <a name="building-search-tree"></a>Bygga sökträd  
 Tabell 481 **Trädnod för dimensionsuppsättning** används när [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning redan finns i tabell 480 **Dimensionsuppsättnings transaktion**. Utvärderingen utförs av rekursivt genomgång av sökträdet från toppnivån nummer 0. Den översta nivån 0 representerar en dimension utan dimensionsuppsättningstransaktioner. De underordnade uppsättningarna till denna dimensionsuppsättning representerar dimensionsuppsättningar med endast en dimensionsuppsättningstransaktion. De underordnade uppsättningarna till dessa dimensionsuppsättningar representerar dimensionsuppsättningar med två underordnade, och så vidare.  

### <a name="example-1"></a>Exempel 1  
 Följande diagram representerar ett sökträd med sex dimensionsuppsättningar. Endast den särskiljande dimensionsuppsättningstransaktionen visas i diagrammet.  

 ![Dimension trädstrukturen](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")  

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

 ![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")  

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

 För att bevara möjligheten för [!INCLUDE[d365fin](includes/d365fin_md.md)] byta namn på en dimension och ett dimensionsvärde utökas tabellen 348 **Dimensionsvärde** med heltalsfältet **Dimensionsvärde-ID**. Den här tabellen omvandlar fältparen **Dimension** och **Dimensionsvärde** till ett heltalsvärde. När du byter namn på dimensionen och dimensionsvärdet ändras inte heltalsvärdet.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Se även  
 [HÄMTA funktionen (post)](https://msdn.microsoft.com/en-us/library/dd301056.aspx)    
 [Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md)   
 [Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
 [Designdetaljer: Kodenhet 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
 [Designdetaljer: Kodexempel på ändrade mönster i ändringar](design-details-code-examples-of-changed-patterns-in-modifications.md)

