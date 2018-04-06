---
title: "Designdetaljer - Planeringsfördelningstabell | Microsoft Docs"
description: "Det här avsnittet innehåller information om vad som händer när du ändrar hur du planerar för en artikel."
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
ms.openlocfilehash: 3e412c6fe82b3ee5640329c523b19d68f849f93a
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="694f1-103">Designdetaljer: Planeringsfördelningstabell</span><span class="sxs-lookup"><span data-stu-id="694f1-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="694f1-104">Alla artiklar ska planeras för, men det finns ingen anledning att beräkna en plan för en artikel om det inte har skett någon ändring i efterfråge- eller tillgångsmönstret sedan senaste gången som en plan beräknades.</span><span class="sxs-lookup"><span data-stu-id="694f1-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  
  
<span data-ttu-id="694f1-105">Om användaren har angett en ny försäljningsorder eller har ändrat en befintlig finns det anledning att beräkna om planen.</span><span class="sxs-lookup"><span data-stu-id="694f1-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="694f1-106">Andra anledningar är en ändring i prognos eller önskat antal i säkerhetslagret.</span><span class="sxs-lookup"><span data-stu-id="694f1-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="694f1-107">När du ändrar en struktur genom att lägga till eller ta bort en komponent indikerar det troligtvis en ändring, men endast för komponentartikeln.</span><span class="sxs-lookup"><span data-stu-id="694f1-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  
  
<span data-ttu-id="694f1-108">För flera lagerställen sker fördelningen på nivån med kombinationen av artikel per lagerställe.</span><span class="sxs-lookup"><span data-stu-id="694f1-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="694f1-109">Om till exempel en försäljningsorder har skapats vid endast ett lagerställe, kommer programmet att tilldela artikeln vid det specifika lagerstället för planeringen.</span><span class="sxs-lookup"><span data-stu-id="694f1-109">If, for example, a sales order has been created at only one location, the program will assign the item at that specific location for planning.</span></span>  
  
<span data-ttu-id="694f1-110">Anledningen för att välja artikel för planeringen är en fråga om systemprestanda.</span><span class="sxs-lookup"><span data-stu-id="694f1-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="694f1-111">Om ingen ändring i en artikels efterfrågans-/tillgångsmönster har skett kommer planeringssystemet inte att föreslå några åtgärder som ska vidtas.</span><span class="sxs-lookup"><span data-stu-id="694f1-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="694f1-112">Utan planeringsfördelningen måste systemet utföra beräkningarna för alla artiklar för att avgöra vad som ska planeras för, och det skulle dränera systemresurser.</span><span class="sxs-lookup"><span data-stu-id="694f1-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  
  
<span data-ttu-id="694f1-113">Tabellen **Planeringsfördelning** övervakar behovs- och försörjningshändelser och tilldelar lämpliga artiklar för planeringen.</span><span class="sxs-lookup"><span data-stu-id="694f1-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="694f1-114">Följande händelser övervakas:</span><span class="sxs-lookup"><span data-stu-id="694f1-114">The following events are monitored:</span></span>  
  
* <span data-ttu-id="694f1-115">En ny försäljningsorder, prognos, komponent, inköpsorder, produktionsorder, monteringsorder eller överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="694f1-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="694f1-116">Ändring av artikel, antal, lagerställe, variant eller datum på en försäljningsorder, prognos, komponent, inköpsorder, produktionsorder, monteringsorder eller överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="694f1-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="694f1-117">Annullering av en försäljningsorder, prognos, komponent, inköpsorder, produktionsorder, monteringsorder eller överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="694f1-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="694f1-118">Förbrukning av artiklar annat än planerade.</span><span class="sxs-lookup"><span data-stu-id="694f1-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="694f1-119">Utflöde av andra artiklar än planerade.</span><span class="sxs-lookup"><span data-stu-id="694f1-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="694f1-120">Oplanerade ändringar i lagret.</span><span class="sxs-lookup"><span data-stu-id="694f1-120">Unplanned changes in inventory.</span></span>  
  
<span data-ttu-id="694f1-121">För dessa direkta efterfrågan/tillgång-förflyttningar underhåller orderspårnings- och åtgärdsmeddelandesystemet tabellen Planeringsfördelning och anger en planeringsorsak som ett åtgärdsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="694f1-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  
  
<span data-ttu-id="694f1-122">Följande ändringar av huvuddata kan också orsaka en planeringsobalans:</span><span class="sxs-lookup"><span data-stu-id="694f1-122">The following changes in master data can also cause a planning imbalance:</span></span>  
  
* <span data-ttu-id="694f1-123">Ändring av status till Certifierat i produktionsstrukturhuvudet (för alla artiklar som använder huvudet).</span><span class="sxs-lookup"><span data-stu-id="694f1-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="694f1-124">Tagit bort rad (underordnat objekt).</span><span class="sxs-lookup"><span data-stu-id="694f1-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="694f1-125">Ändring av status till Certifierat i verksamhetsföljdhuvudet (för alla artiklar som använder verksamhetsföljden).</span><span class="sxs-lookup"><span data-stu-id="694f1-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="694f1-126">Ändringar i följande artikelkortfält.</span><span class="sxs-lookup"><span data-stu-id="694f1-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="694f1-127">Säkerhetslager eller säkerhetsledtid.</span><span class="sxs-lookup"><span data-stu-id="694f1-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="694f1-128">Ledtidsberäkning.</span><span class="sxs-lookup"><span data-stu-id="694f1-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="694f1-129">Beställningspunkt.</span><span class="sxs-lookup"><span data-stu-id="694f1-129">Reorder Point.</span></span>  
* <span data-ttu-id="694f1-130">Produktionstrukturnr. (och alla underordnade till gammal strukturreferens).</span><span class="sxs-lookup"><span data-stu-id="694f1-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="694f1-131">Operationsföljdsnr</span><span class="sxs-lookup"><span data-stu-id="694f1-131">Routing No.</span></span>  
* <span data-ttu-id="694f1-132">Partiformningsmetod.</span><span class="sxs-lookup"><span data-stu-id="694f1-132">Reordering Policy.</span></span>  
  
<span data-ttu-id="694f1-133">I de här fallen underhåller en ny funktion, Planera fördelningshantering, tabellen och ange planeringsanledningen som Nettoförändring.</span><span class="sxs-lookup"><span data-stu-id="694f1-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  
  
<span data-ttu-id="694f1-134">Följande ändringar orsakar ingen planeringsfördelning:</span><span class="sxs-lookup"><span data-stu-id="694f1-134">The following changes do not cause a planning assignment:</span></span>  
  
* <span data-ttu-id="694f1-135">Kalendrar</span><span class="sxs-lookup"><span data-stu-id="694f1-135">Calendars</span></span>  
* <span data-ttu-id="694f1-136">Andra planeringsparametrar på artikelkortet</span><span class="sxs-lookup"><span data-stu-id="694f1-136">Other planning parameters on the item card</span></span>  
  
<span data-ttu-id="694f1-137">När att prod.program eller ett nettobehov beräknas gäller inga begränsningar:</span><span class="sxs-lookup"><span data-stu-id="694f1-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  
  
* <span data-ttu-id="694f1-138">Prod.program: Planeringssystemet kontrollerar att artikeln har en produktionsprognos eller en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="694f1-138">MPS: The planning system checks that the item carries a production forecast or a sales order.</span></span> <span data-ttu-id="694f1-139">Om inte, ingår artikeln inte i planen.</span><span class="sxs-lookup"><span data-stu-id="694f1-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="694f1-140">Nettobehov: Om planeringssystemet identifierar att artikeln fylls på av en nettoplaneringsrad eller nettoleveransorder ska artikeln inte användas i planeringen.</span><span class="sxs-lookup"><span data-stu-id="694f1-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="694f1-141">Dock inkluderas all efterfrågan från relevanta komponenter.</span><span class="sxs-lookup"><span data-stu-id="694f1-141">However, any demand from relevant components is included.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="694f1-142">Se även</span><span class="sxs-lookup"><span data-stu-id="694f1-142">See Also</span></span>  
<span data-ttu-id="694f1-143">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="694f1-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="694f1-144">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="694f1-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="694f1-145">[Designdetaljer: Överföringar i planering](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="694f1-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="694f1-146">Designdetaljer: Planeringsparametrar</span><span class="sxs-lookup"><span data-stu-id="694f1-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  

