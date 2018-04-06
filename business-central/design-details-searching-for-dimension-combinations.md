---
title: "Designdetaljer - Söka efter dimensionskombinationer | Microsoft Docs"
description: "När du stänger ett fönster efter att ha redigerat en uppsättning dimensioner utvärderar Business Central huruvida den redigerade uppsättningen dimensioner finns. Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 416fe8425d2b21f1f1f72b2f159bb6a863bc1d8b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="8a1a3-104">Designdetaljer: Söka efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="8a1a3-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="8a1a3-105">När du stänger ett fönster när du har redigerat en uppsättning med dimensioner utvärderar [!INCLUDE[d365fin](includes/d365fin_md.md)] om den redigerade uppsättningen med dimensioner finns.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-105">When you close a window after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="8a1a3-106">Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="8a1a3-107">Bygga sökträd</span><span class="sxs-lookup"><span data-stu-id="8a1a3-107">Building Search Tree</span></span>  
 <span data-ttu-id="8a1a3-108">Tabell 481 **Trädnod för dimensionsuppsättning** används när [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning redan finns i tabell 480 **Dimensionsuppsättnings transaktion**.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="8a1a3-109">Utvärderingen utförs av rekursivt genomgång av sökträdet från toppnivån nummer 0.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="8a1a3-110">Den översta nivån 0 representerar en dimension utan dimensionsuppsättningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="8a1a3-111">De underordnade uppsättningarna till denna dimensionsuppsättning representerar dimensionsuppsättningar med endast en dimensionsuppsättningstransaktion.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="8a1a3-112">De underordnade uppsättningarna till dessa dimensionsuppsättningar representerar dimensionsuppsättningar med två underordnade, och så vidare.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="8a1a3-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a1a3-113">Example 1</span></span>  
 <span data-ttu-id="8a1a3-114">Följande diagram representerar ett sökträd med sex dimensionsuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="8a1a3-115">Endast den särskiljande dimensionsuppsättningstransaktionen visas i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="8a1a3-116">![Dimension trädstrukturen](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")</span><span class="sxs-lookup"><span data-stu-id="8a1a3-116">![Dimension tree structure](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")</span></span>  

 <span data-ttu-id="8a1a3-117">Följande tabell beskrivs en fullständig lista över dimensionsuppsättningstransaktioner som utgör varje dimensionsuppsättning.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="8a1a3-118">Dimensionsuppsättningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-118">Dimension Sets</span></span>|<span data-ttu-id="8a1a3-119">Dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="8a1a3-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="8a1a3-120">Frågesvar 0</span><span class="sxs-lookup"><span data-stu-id="8a1a3-120">Set 0</span></span>|<span data-ttu-id="8a1a3-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a1a3-121">None</span></span>|  
|<span data-ttu-id="8a1a3-122">Frågesvar 1</span><span class="sxs-lookup"><span data-stu-id="8a1a3-122">Set 1</span></span>|<span data-ttu-id="8a1a3-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="8a1a3-123">AREA 30</span></span>|  
|<span data-ttu-id="8a1a3-124">Frågesvar 2</span><span class="sxs-lookup"><span data-stu-id="8a1a3-124">Set 2</span></span>|<span data-ttu-id="8a1a3-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="8a1a3-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="8a1a3-126">Frågesvar 3</span><span class="sxs-lookup"><span data-stu-id="8a1a3-126">Set 3</span></span>|<span data-ttu-id="8a1a3-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="8a1a3-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="8a1a3-128">Frågesvar 4</span><span class="sxs-lookup"><span data-stu-id="8a1a3-128">Set 4</span></span>|<span data-ttu-id="8a1a3-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="8a1a3-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="8a1a3-130">Frågesvar 5</span><span class="sxs-lookup"><span data-stu-id="8a1a3-130">Set 5</span></span>|<span data-ttu-id="8a1a3-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="8a1a3-131">AREA 40</span></span>|  
|<span data-ttu-id="8a1a3-132">Frågesvar 6</span><span class="sxs-lookup"><span data-stu-id="8a1a3-132">Set 6</span></span>|<span data-ttu-id="8a1a3-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="8a1a3-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="8a1a3-134">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8a1a3-134">Example 2</span></span>  
 <span data-ttu-id="8a1a3-135">I det här exemplet visas hur [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning som består av dimensionsuppsättningstransaktionerna AREA 40, DEPT PROD finns.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="8a1a3-136">Först [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdateras även tabellen **Trädnod för dimensionsuppsättning** för att se till att sökträdet ser ut som på bilden.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="8a1a3-137">På så sätt blir dimensionsuppsättning 7 underordnad dimensionsuppsättning 5.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="8a1a3-138">![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")</span><span class="sxs-lookup"><span data-stu-id="8a1a3-138">![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="8a1a3-139">Hitta dimensionsuppsättnings-ID</span><span class="sxs-lookup"><span data-stu-id="8a1a3-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="8a1a3-140">På en begreppsmässig nivå kombineras **Överordnat ID**, **Dimension**, och **Dimensionsvärde**,  i sökträdet, och används som primärnyckel eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] korsar trädet i samma ordning som dimensionstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="8a1a3-141">Funktionen GET (record) används för att söka efter dimensionuppsättnings-ID.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="8a1a3-142">Följande kodexempel visar hur du hittar dimensionsuppsättning-ID när det finns tre dimensionsvärden.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 <span data-ttu-id="8a1a3-143">För att bevara möjligheten för [!INCLUDE[d365fin](includes/d365fin_md.md)] byta namn på en dimension och ett dimensionsvärde utökas tabellen 348 **Dimensionsvärde** med heltalsfältet **Dimensionsvärde-ID**.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename a dimension and dimension value, table 348 **Dimension Value** is extended with an integer field of **Dimension Value ID**.</span></span> <span data-ttu-id="8a1a3-144">Den här tabellen omvandlar fältparen **Dimension** och **Dimensionsvärde** till ett heltalsvärde.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-144">This table converts the field pair **Dimension** and **Dimension Value** to an integer value.</span></span> <span data-ttu-id="8a1a3-145">När du byter namn på dimensionen och dimensionsvärdet ändras inte heltalsvärdet.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="8a1a3-146">Se även</span><span class="sxs-lookup"><span data-stu-id="8a1a3-146">See Also</span></span>  
 <span data-ttu-id="8a1a3-147">[HÄMTA funktionen (post)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="8a1a3-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="8a1a3-148">[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="8a1a3-149">[Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="8a1a3-150">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-150">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 <span data-ttu-id="8a1a3-151">[Designdetaljer: Kodenhet 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-151">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
 [<span data-ttu-id="8a1a3-152">Designdetaljer: Kodexempel på ändrade mönster i ändringar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-152">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

