---
title: "Definiera och fördela kostnader | Microsoft Docs"
description: "Kostnadsfördelning flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare. Du kan definiera valfritt antal fördelningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ed219b252c17fe18aadefabce7ddd280790ffcc0
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="bd2a7-104">Definiera och fördela kostnader</span><span class="sxs-lookup"><span data-stu-id="bd2a7-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="bd2a7-105">Kostnadsfördelning flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="bd2a7-106">Du kan definiera valfritt antal fördelningar.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="bd2a7-107">Varje fördelning består av:</span><span class="sxs-lookup"><span data-stu-id="bd2a7-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="bd2a7-108">En fördelningskälla.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-108">An allocation source.</span></span>  
-   <span data-ttu-id="bd2a7-109">Ett eller flera fördelningsmål.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-109">One or more allocation targets.</span></span>  

<span data-ttu-id="bd2a7-110">Fördelningskällan bestämmer vilka kostnader som måste fördelas, och fördelningsmålen bestämmer var kostnader måste fördelas.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="bd2a7-111">Till exempel kan en fördelningskälla vara kostnaderna för kostnadstypen Uppvärmning.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="bd2a7-112">Du tilldelar alla uppvärmningskostnader till tre kostnadsställen: Seminarium, Produktion och Försäljning.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="bd2a7-113">Dessa kostnadsställen är dina fördelningsmål.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="bd2a7-114">För varje fördelningskälla definierar du en fördelningsnivå, en giltighetsperiod och en variant som grupp-id.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="bd2a7-115">Du kan använda ett batch-jobb för att definiera filter för att välja fördelningsdefinitioner och sedan köra kostnadsfördelningar automatiskt.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="bd2a7-116">För varje fördelningsmål definierar du en fördelningsbas.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="bd2a7-117">Fördelningsbasen kan antingen vara statisk eller dynamisk.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="bd2a7-118">Statisk fördelning är baserad på ett visst värde, till exempel kvadratmetrar eller en fastställd fördelningskvot, till exempel 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="bd2a7-119">Dynamiska fördelningsbaser beror på värden som kan ändras, t.ex hur många anställda i ett kostnadsställe eller försäljningsintäkten för en kostnadsbärare under en viss tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="bd2a7-120">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="bd2a7-121">Till</span><span class="sxs-lookup"><span data-stu-id="bd2a7-121">To</span></span>|<span data-ttu-id="bd2a7-122">Gå till</span><span class="sxs-lookup"><span data-stu-id="bd2a7-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="bd2a7-123">Skapa fördelningskälla och dess mål.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="bd2a7-124">Skapa fördelningskälla och mål</span><span class="sxs-lookup"><span data-stu-id="bd2a7-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="bd2a7-125">Skapa olika filter för dynamiska fördelningsbaser.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="bd2a7-126">Skapa filter för dynamiska fördelningsbaser</span><span class="sxs-lookup"><span data-stu-id="bd2a7-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="bd2a7-127">Visa ett exempel på hur du definierar en fast distribution.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="bd2a7-128">Scenarioexempel: Definiera fast distribution beräknad på fördelningskvot</span><span class="sxs-lookup"><span data-stu-id="bd2a7-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="bd2a7-129">Visa ett exempel på hur du definierar en dynamisk distribution.</span><span class="sxs-lookup"><span data-stu-id="bd2a7-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="bd2a7-130">Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar</span><span class="sxs-lookup"><span data-stu-id="bd2a7-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="bd2a7-131">Se även</span><span class="sxs-lookup"><span data-stu-id="bd2a7-131">See Also</span></span>  
 <span data-ttu-id="bd2a7-132">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="bd2a7-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="bd2a7-133">[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="bd2a7-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="bd2a7-134">[Redovisa kostnader](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="bd2a7-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="bd2a7-135">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="bd2a7-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="bd2a7-136">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="bd2a7-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

