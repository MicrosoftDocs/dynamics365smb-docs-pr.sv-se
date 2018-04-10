---
title: "Skapa filter för dynamiska fördelningsbaser | Microsoft Docs"
description: "Den dynamiska fördelningsmetoden bygger på värden som kan ändras. Till exempel antalet anställda i ett kostnadsställe eller artiklar som säljs på en kostnadsbärare för en viss tidsperiod. Det finns nio fördefinierade fördelningsbaser och tolv dynamiska datumintervall. Du kan ange olika filter baserade på fördelningsbasen."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: 5ca8e7008c2bfe4a9abeb9d9b7b467a38e2c1971
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a><span data-ttu-id="e8051-106">Skapa filter för dynamiska fördelningsbaser</span><span class="sxs-lookup"><span data-stu-id="e8051-106">Setting Filters for Dynamic Allocation Bases</span></span>
<span data-ttu-id="e8051-107">Den dynamiska fördelningsmetoden bygger på värden som kan ändras.</span><span class="sxs-lookup"><span data-stu-id="e8051-107">The dynamic allocation method is based on changeable values.</span></span> <span data-ttu-id="e8051-108">Till exempel antalet anställda i ett kostnadsställe eller artiklar som säljs på en kostnadsbärare för en viss tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="e8051-108">For example, the number of employees in a cost center or the items sold of a cost object in a specific time period.</span></span> <span data-ttu-id="e8051-109">Det finns nio fördefinierade fördelningsbaser och tolv dynamiska datumintervall.</span><span class="sxs-lookup"><span data-stu-id="e8051-109">There are nine pre-defined allocation bases and twelve dynamic date ranges.</span></span> <span data-ttu-id="e8051-110">Du kan ange olika filter baserade på fördelningsbasen.</span><span class="sxs-lookup"><span data-stu-id="e8051-110">You set different filters based on the allocation base.</span></span>  

## <a name="setting-filters-for-dynamic-allocation-bases"></a><span data-ttu-id="e8051-111">Skapa filter för dynamiska fördelningsbaser</span><span class="sxs-lookup"><span data-stu-id="e8051-111">Setting Filters for Dynamic Allocation Bases</span></span>  
 <span data-ttu-id="e8051-112">Följande tabell visar vilka filter är möjliga för olika fördelningsbaser och vilka värden som gäller i fälten **Nummerfilter** och **Gruppfilter**.</span><span class="sxs-lookup"><span data-stu-id="e8051-112">The following table shows which filters are possible for different allocation bases and which values are valid in the **No. Filter** and **Group Filter** fields.</span></span> <span data-ttu-id="e8051-113">Tryck på F1 i fälten **Kod för datumfilter** om du vill läsa detaljerad beskrivningar.</span><span class="sxs-lookup"><span data-stu-id="e8051-113">Press F1 in the **Date Filter Code** field to read detailed descriptions.</span></span>  

|<span data-ttu-id="e8051-114">**Bas**</span><span class="sxs-lookup"><span data-stu-id="e8051-114">**Base**</span></span>|<span data-ttu-id="e8051-115">**Nummerfilter**</span><span class="sxs-lookup"><span data-stu-id="e8051-115">**No. Filter**</span></span>|<span data-ttu-id="e8051-116">**Kod för datumfilter**</span><span class="sxs-lookup"><span data-stu-id="e8051-116">**Date Filter Code**</span></span>|<span data-ttu-id="e8051-117">**Filter för kostnadsställe**</span><span class="sxs-lookup"><span data-stu-id="e8051-117">**Cost Center Filter**</span></span>|<span data-ttu-id="e8051-118">**Filter för kostnadsbärare**</span><span class="sxs-lookup"><span data-stu-id="e8051-118">**Cost Object Filter**</span></span>|<span data-ttu-id="e8051-119">**Gruppfilter**</span><span class="sxs-lookup"><span data-stu-id="e8051-119">**Group Filter**</span></span>|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|<span data-ttu-id="e8051-120">Redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="e8051-120">G/L Entries</span></span>|<span data-ttu-id="e8051-121">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="e8051-121">G/L Account</span></span>|<span data-ttu-id="e8051-122">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-122">Yes</span></span>|<span data-ttu-id="e8051-123">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-123">Yes</span></span>|<span data-ttu-id="e8051-124">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-124">Yes</span></span>|<span data-ttu-id="e8051-125">Inte tillämpligt</span><span class="sxs-lookup"><span data-stu-id="e8051-125">N/A</span></span>|  
|<span data-ttu-id="e8051-126">Redov.budgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="e8051-126">G/L Budget Entries</span></span>|<span data-ttu-id="e8051-127">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="e8051-127">G/L Account</span></span>|<span data-ttu-id="e8051-128">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-128">Yes</span></span>|<span data-ttu-id="e8051-129">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-129">Yes</span></span>|<span data-ttu-id="e8051-130">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-130">Yes</span></span>|<span data-ttu-id="e8051-131">Redov.budgetnamn</span><span class="sxs-lookup"><span data-stu-id="e8051-131">G/L Budget Name</span></span>|  
|<span data-ttu-id="e8051-132">Kostnadstypstransaktioner</span><span class="sxs-lookup"><span data-stu-id="e8051-132">Cost Type Entries</span></span>|<span data-ttu-id="e8051-133">Kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="e8051-133">Cost Type</span></span>|<span data-ttu-id="e8051-134">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-134">Yes</span></span>|<span data-ttu-id="e8051-135">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-135">Yes</span></span>|<span data-ttu-id="e8051-136">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-136">Yes</span></span>|<span data-ttu-id="e8051-137">Inte tillämpligt</span><span class="sxs-lookup"><span data-stu-id="e8051-137">N/A</span></span>|  
|<span data-ttu-id="e8051-138">Kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="e8051-138">Cost Budget Entries</span></span>|<span data-ttu-id="e8051-139">Kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="e8051-139">Cost Type</span></span>|<span data-ttu-id="e8051-140">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-140">Yes</span></span>|<span data-ttu-id="e8051-141">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-141">Yes</span></span>|<span data-ttu-id="e8051-142">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-142">Yes</span></span>|<span data-ttu-id="e8051-143">Budgetnamn</span><span class="sxs-lookup"><span data-stu-id="e8051-143">Budget Name</span></span>|  
|<span data-ttu-id="e8051-144">Antal anställda</span><span class="sxs-lookup"><span data-stu-id="e8051-144">No of Employees</span></span>|<span data-ttu-id="e8051-145">Inte tillämpligt</span><span class="sxs-lookup"><span data-stu-id="e8051-145">N/A</span></span>|<span data-ttu-id="e8051-146">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-146">Yes</span></span>|<span data-ttu-id="e8051-147">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-147">Yes</span></span>|<span data-ttu-id="e8051-148">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-148">Yes</span></span>|<span data-ttu-id="e8051-149">Inte tillämpligt</span><span class="sxs-lookup"><span data-stu-id="e8051-149">N/A</span></span>|  
|<span data-ttu-id="e8051-150">Sålda artiklar (antal)</span><span class="sxs-lookup"><span data-stu-id="e8051-150">Items Sold (Qty)</span></span>|<span data-ttu-id="e8051-151">Artikelnr</span><span class="sxs-lookup"><span data-stu-id="e8051-151">Item No.</span></span>|<span data-ttu-id="e8051-152">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-152">Yes</span></span>|<span data-ttu-id="e8051-153">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-153">Yes</span></span>|<span data-ttu-id="e8051-154">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-154">Yes</span></span>|<span data-ttu-id="e8051-155">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="e8051-155">Inventory Posting Group</span></span>|  
|<span data-ttu-id="e8051-156">Inköpta artiklar (antal)</span><span class="sxs-lookup"><span data-stu-id="e8051-156">Items Purchased (Qty)</span></span>|<span data-ttu-id="e8051-157">Artikelnr</span><span class="sxs-lookup"><span data-stu-id="e8051-157">Item No.</span></span>|<span data-ttu-id="e8051-158">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-158">Yes</span></span>|<span data-ttu-id="e8051-159">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-159">Yes</span></span>|<span data-ttu-id="e8051-160">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-160">Yes</span></span>|<span data-ttu-id="e8051-161">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="e8051-161">Inventory Posting Group</span></span>|  
|<span data-ttu-id="e8051-162">Sålda artiklar (belopp)</span><span class="sxs-lookup"><span data-stu-id="e8051-162">Items Sold (Amount)</span></span>|<span data-ttu-id="e8051-163">Artikelnr</span><span class="sxs-lookup"><span data-stu-id="e8051-163">Item No.</span></span>|<span data-ttu-id="e8051-164">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-164">Yes</span></span>|<span data-ttu-id="e8051-165">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-165">Yes</span></span>|<span data-ttu-id="e8051-166">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-166">Yes</span></span>|<span data-ttu-id="e8051-167">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="e8051-167">Inventory Posting Group</span></span>|  
|<span data-ttu-id="e8051-168">Inköpta artiklar (belopp)</span><span class="sxs-lookup"><span data-stu-id="e8051-168">Items Purchased (Amount)</span></span>|<span data-ttu-id="e8051-169">Artikelnr</span><span class="sxs-lookup"><span data-stu-id="e8051-169">Item No.</span></span>|<span data-ttu-id="e8051-170">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-170">Yes</span></span>|<span data-ttu-id="e8051-171">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-171">Yes</span></span>|<span data-ttu-id="e8051-172">Ja</span><span class="sxs-lookup"><span data-stu-id="e8051-172">Yes</span></span>|<span data-ttu-id="e8051-173">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="e8051-173">Inventory Posting Group</span></span>|  

## <a name="see-also"></a><span data-ttu-id="e8051-174">Se även</span><span class="sxs-lookup"><span data-stu-id="e8051-174">See Also</span></span>  
 <span data-ttu-id="e8051-175">[Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="e8051-175">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
 <span data-ttu-id="e8051-176">[Skapa fördelningskälla och mål](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="e8051-176">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 [<span data-ttu-id="e8051-177">Definiera och fördela kostnader</span><span class="sxs-lookup"><span data-stu-id="e8051-177">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)
