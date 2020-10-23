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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c8fb1026c871efc1ce61b26e587399f91bdf718f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910911"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="7b805-104">Designdetaljer: Söka efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="7b805-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="7b805-105">När du stänger en sida när du har redigerat en uppsättning med dimensioner utvärderar [!INCLUDE[d365fin](includes/d365fin_md.md)] om den redigerade uppsättningen med dimensioner finns.</span><span class="sxs-lookup"><span data-stu-id="7b805-105">When you close a page after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="7b805-106">Om uppsättningen inte finns skapas en ny uppsättning och dimensionskombinationens ID returneras.</span><span class="sxs-lookup"><span data-stu-id="7b805-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="7b805-107">Bygga sökträd</span><span class="sxs-lookup"><span data-stu-id="7b805-107">Building Search Tree</span></span>  
 <span data-ttu-id="7b805-108">Tabell 481 **Trädnod för dimensionsuppsättning** används när [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning redan finns i tabell 480 **Dimensionsuppsättnings transaktion**.</span><span class="sxs-lookup"><span data-stu-id="7b805-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="7b805-109">Utvärderingen utförs av rekursivt genomgång av sökträdet från toppnivån nummer 0.</span><span class="sxs-lookup"><span data-stu-id="7b805-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="7b805-110">Den översta nivån 0 representerar en dimension utan dimensionsuppsättningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7b805-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="7b805-111">De underordnade uppsättningarna till denna dimensionsuppsättning representerar dimensionsuppsättningar med endast en dimensionsuppsättningstransaktion.</span><span class="sxs-lookup"><span data-stu-id="7b805-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="7b805-112">De underordnade uppsättningarna till dessa dimensionsuppsättningar representerar dimensionsuppsättningar med två underordnade, och så vidare.</span><span class="sxs-lookup"><span data-stu-id="7b805-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="7b805-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b805-113">Example 1</span></span>  
 <span data-ttu-id="7b805-114">Följande diagram representerar ett sökträd med sex dimensionsuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="7b805-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="7b805-115">Endast den särskiljande dimensionsuppsättningstransaktionen visas i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="7b805-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="7b805-116">![Exempel på en dimensionsträdsstruktur](media/nav2013_dimension_tree.png "Exempel på en dimensionsträdsstruktur")</span><span class="sxs-lookup"><span data-stu-id="7b805-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="7b805-117">Följande tabell beskrivs en fullständig lista över dimensionsuppsättningstransaktioner som utgör varje dimensionsuppsättning.</span><span class="sxs-lookup"><span data-stu-id="7b805-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="7b805-118">Dimensionsuppsättningar</span><span class="sxs-lookup"><span data-stu-id="7b805-118">Dimension Sets</span></span>|<span data-ttu-id="7b805-119">Dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="7b805-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="7b805-120">Frågesvar 0</span><span class="sxs-lookup"><span data-stu-id="7b805-120">Set 0</span></span>|<span data-ttu-id="7b805-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="7b805-121">None</span></span>|  
|<span data-ttu-id="7b805-122">Frågesvar 1</span><span class="sxs-lookup"><span data-stu-id="7b805-122">Set 1</span></span>|<span data-ttu-id="7b805-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="7b805-123">AREA 30</span></span>|  
|<span data-ttu-id="7b805-124">Frågesvar 2</span><span class="sxs-lookup"><span data-stu-id="7b805-124">Set 2</span></span>|<span data-ttu-id="7b805-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="7b805-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="7b805-126">Frågesvar 3</span><span class="sxs-lookup"><span data-stu-id="7b805-126">Set 3</span></span>|<span data-ttu-id="7b805-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="7b805-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="7b805-128">Frågesvar 4</span><span class="sxs-lookup"><span data-stu-id="7b805-128">Set 4</span></span>|<span data-ttu-id="7b805-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="7b805-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="7b805-130">Frågesvar 5</span><span class="sxs-lookup"><span data-stu-id="7b805-130">Set 5</span></span>|<span data-ttu-id="7b805-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="7b805-131">AREA 40</span></span>|  
|<span data-ttu-id="7b805-132">Frågesvar 6</span><span class="sxs-lookup"><span data-stu-id="7b805-132">Set 6</span></span>|<span data-ttu-id="7b805-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="7b805-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="7b805-134">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7b805-134">Example 2</span></span>  
 <span data-ttu-id="7b805-135">I det här exemplet visas hur [!INCLUDE[d365fin](includes/d365fin_md.md)] utvärderar om en dimensionsuppsättning som består av dimensionsuppsättningstransaktionerna AREA 40, DEPT PROD finns.</span><span class="sxs-lookup"><span data-stu-id="7b805-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="7b805-136">Först [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdateras även tabellen **Trädnod för dimensionsuppsättning** för att se till att sökträdet ser ut som på bilden.</span><span class="sxs-lookup"><span data-stu-id="7b805-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="7b805-137">På så sätt blir dimensionsuppsättning 7 underordnad dimensionsuppsättning 5.</span><span class="sxs-lookup"><span data-stu-id="7b805-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="7b805-138">![Exempel på en dimensionsträdsstruktur i NAV 2013](media/nav2013_dimension_tree_example2.png "Exempel på en dimensionsträdsstruktur i NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="7b805-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="7b805-139">Hitta dimensionsuppsättnings-ID</span><span class="sxs-lookup"><span data-stu-id="7b805-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="7b805-140">På en begreppsmässig nivå kombineras **Överordnat ID**, **Dimension**, och **Dimensionsvärde**,  i sökträdet, och används som primärnyckel eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] korsar trädet i samma ordning som dimensionstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="7b805-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="7b805-141">Funktionen GET (record) används för att söka efter dimensionuppsättnings-ID.</span><span class="sxs-lookup"><span data-stu-id="7b805-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="7b805-142">Följande kodexempel visar hur du hittar dimensionsuppsättning-ID när det finns tre dimensionsvärden.</span><span class="sxs-lookup"><span data-stu-id="7b805-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="7b805-143">För att bevara möjligheten för [!INCLUDE[d365fin](includes/d365fin_md.md)] byta namn på en dimension och ett dimensionsvärde utökas tabellen 349 **Dimensionsvärde** med heltalsfältet **Dimensionsvärde-ID**.</span><span class="sxs-lookup"><span data-stu-id="7b805-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="7b805-144">Den här tabellen omvandlar fältparen **Dimension** och **Dimensionsvärde** till ett heltalsvärde.</span><span class="sxs-lookup"><span data-stu-id="7b805-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="7b805-145">När du byter namn på dimensionen och dimensionsvärdet ändras inte heltalsvärdet.</span><span class="sxs-lookup"><span data-stu-id="7b805-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="7b805-146">Se även</span><span class="sxs-lookup"><span data-stu-id="7b805-146">See Also</span></span>  
 <span data-ttu-id="7b805-147">[HÄMTA funktionen (post)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="7b805-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="7b805-148">[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7b805-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="7b805-149">[Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="7b805-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="7b805-150">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="7b805-150">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
