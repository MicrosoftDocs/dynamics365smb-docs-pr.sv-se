---
title: "Designdetaljer - Övervaka den planerade lagernivån och beställningspunkten | Microsoft Docs"
description: "Lär dig hur lagerplanering skiljer mellan planerat lager och planerade tillgängliga lagernivåer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a0e64d96389739c67a9e9f548958fac12e3aca2a
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a><span data-ttu-id="760f7-103">Designdetaljer: Övervaka den planerade lagernivån och beställningspunkten</span><span class="sxs-lookup"><span data-stu-id="760f7-103">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>
<span data-ttu-id="760f7-104">Lager är en typ av tillgång, men för lagerplanering skiljer planeringssystemet mellan två lagernivåer:</span><span class="sxs-lookup"><span data-stu-id="760f7-104">Inventory is a type of supply, but for inventory planning, the planning system distinguishes between two inventory levels:</span></span>  

* <span data-ttu-id="760f7-105">Planerat lager</span><span class="sxs-lookup"><span data-stu-id="760f7-105">Projected inventory</span></span>  
* <span data-ttu-id="760f7-106">Planerat tillgängligt lager</span><span class="sxs-lookup"><span data-stu-id="760f7-106">Projected available inventory</span></span>  

## <a name="projected-inventory"></a><span data-ttu-id="760f7-107">Planerat lager</span><span class="sxs-lookup"><span data-stu-id="760f7-107">Projected Inventory</span></span>  
<span data-ttu-id="760f7-108">Från början är planerat lager antalet i bruttolager, inklusive tidigare tillgång och efterfrågan även om den inte är bokförd, när planeringsprocessen startas</span><span class="sxs-lookup"><span data-stu-id="760f7-108">Initially, projected inventory is the quantity of gross inventory, including supply and demand in the past even if not posted, when starting the planning process.</span></span> <span data-ttu-id="760f7-109">I framtiden blir det en rörlig planerad lagernivå som underhålls av bruttoantal från framtida tillgång och efterfrågan, eftersom de introduceras längs tidslinjen (reserverade eller fördelade på andra sätt).</span><span class="sxs-lookup"><span data-stu-id="760f7-109">In the future, this becomes a moving projected inventory level that is maintained by gross quantities from future supply and demand because those are introduced along the time line (whether reserved or in other ways allocated).</span></span>  

<span data-ttu-id="760f7-110">Det planerade lagret används i planeringssystemet för att övervaka beställningspunkt och för att bestämma beställningsantal när du använder partiformningsmetoden Maximalt antal.</span><span class="sxs-lookup"><span data-stu-id="760f7-110">The projected inventory is used by the planning system to monitor the reorder point and to determine the reorder quantity when using the Maximum Qty. reordering policy.</span></span>  

## <a name="projected-available-inventory"></a><span data-ttu-id="760f7-111">Planerat tillgängligt lager</span><span class="sxs-lookup"><span data-stu-id="760f7-111">Projected Available Inventory</span></span>  
<span data-ttu-id="760f7-112">Det planerade tillgängliga lagret är en del av det planerade lagret som vid en viss tidpunkt är tillgängligt för att uppfylla behov.</span><span class="sxs-lookup"><span data-stu-id="760f7-112">The projected available inventory is the part of the projected inventory that at a given point in time is available to fulfill demand.</span></span> <span data-ttu-id="760f7-113">Det planerade tillgängliga lagret används av planeringsmotorn när du övervakar säkerhetslagernivån.</span><span class="sxs-lookup"><span data-stu-id="760f7-113">The projected available inventory is used by the planning engine when monitoring the safety stock level.</span></span>  

<span data-ttu-id="760f7-114">Det planerade tillgängliga lagret används i planeringssystemet för att övervaka säkerhetslagernivån, eftersom säkerhetslagret alltid måste vara tillgänglig för att uppfylla oväntad efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="760f7-114">The projected available inventory is used by the planning system to monitor the safety stock level, since the safety stock must always be available to serve unexpected demand.</span></span>  

## <a name="time-buckets"></a><span data-ttu-id="760f7-115">Tidsenheter</span><span class="sxs-lookup"><span data-stu-id="760f7-115">Time Buckets</span></span>  
<span data-ttu-id="760f7-116">Om du vill ha en noggrann styrning planerat lager är det avgörande att identifiera när beställningspunkten överstigs och att beräkna rätt partistorlek när du använder partiformningsmetoden Maximalt antal.</span><span class="sxs-lookup"><span data-stu-id="760f7-116">Having a tight control of the projected inventory is crucial to detect when the reorder point is reached or crossed and to calculate the right order quantity when using the Maximum Qty. reordering policy.</span></span>  

<span data-ttu-id="760f7-117">Som angavs tidigare beräknas den planerade lagernivån i början av planeringsperioden.</span><span class="sxs-lookup"><span data-stu-id="760f7-117">As stated earlier, the projected inventory level is calculated at the start of the planning period.</span></span> <span data-ttu-id="760f7-118">Det är en bruttonivå som inte beaktar reservationer och liknande fördelningar.</span><span class="sxs-lookup"><span data-stu-id="760f7-118">It is a gross level that does not consider reservations and similar allocations.</span></span> <span data-ttu-id="760f7-119">För att övervaka den här lagernivån under planeringsföljden övervakar systemet de samlade ändringarna över en tidsperiod, en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="760f7-119">To monitor this inventory level during the planning sequence, the system monitors the aggregated changes over a period of time, a time bucket.</span></span> <span data-ttu-id="760f7-120">Systemet ser till att tidsenheten är minst en dag, eftersom det är mest den exakta tidsenheten för en efterfrågan- eller tillgångshändelse.</span><span class="sxs-lookup"><span data-stu-id="760f7-120">The system ensures that the time bucket is at least one day since it is the most precise unit of time for a demand or supply event.</span></span>  

## <a name="determining-the-projected-inventory-level"></a><span data-ttu-id="760f7-121">Fastställa den planerade lagernivån</span><span class="sxs-lookup"><span data-stu-id="760f7-121">Determining the Projected Inventory Level</span></span>  
<span data-ttu-id="760f7-122">Följande sekvens beskriver hur den planerade lagernivån fastställs:</span><span class="sxs-lookup"><span data-stu-id="760f7-122">The following sequence describes how the projected inventory level is determined:</span></span>  

* <span data-ttu-id="760f7-123">När en tillförselhändelse, t.ex. en inköpsorder har planerats fullständigt kommer det att öka det planerade lagret på förfallodatumet.</span><span class="sxs-lookup"><span data-stu-id="760f7-123">When a supply event, such as a purchase order has been totally planned, it will increase the projected inventory on its due date.</span></span>  
* <span data-ttu-id="760f7-124">När en begäranhändelse har blivit fullständigt uppfylld kommer den inte att minska det planerade lagret direkt.</span><span class="sxs-lookup"><span data-stu-id="760f7-124">When a demand event has been fully satisfied, it will not decrease the projected inventory right away.</span></span> <span data-ttu-id="760f7-125">I stället bokförs en minska-påminnelse, vilket är en intern post som innehåller datumet och antalet som läggs till i det planerade lagret.</span><span class="sxs-lookup"><span data-stu-id="760f7-125">Instead, it posts a decrease reminder, which is an internal record that holds the date and quantity of the contribution to the projected inventory.</span></span>  
* <span data-ttu-id="760f7-126">När en efterföljande tillförselhändelse planeras och placeras på tidslinjen, utforskas de bokförda minska-påminnelserna en och en fram tills det planerade datumet för leveransen, medan det planerade lagret uppdateras.</span><span class="sxs-lookup"><span data-stu-id="760f7-126">When a subsequent supply event is planned and placed on the time line, the posted decrease reminders are investigated one by one up until the planned date of the supply while updating the projected inventory.</span></span> <span data-ttu-id="760f7-127">Under processen kan beställningspunktsnivån för den interna ökningspåminnelsen ha nåtts eller passerats.</span><span class="sxs-lookup"><span data-stu-id="760f7-127">During this process, the reorder point level of the internal increase reminder may be reached or crossed.</span></span>  
* <span data-ttu-id="760f7-128">Om en ny leveransorder introduceras kontrollerar systemet om den har angetts före den aktuella tillgången.</span><span class="sxs-lookup"><span data-stu-id="760f7-128">If a new supply order is introduced, the system checks if it is entered before the current supply.</span></span> <span data-ttu-id="760f7-129">Om det är det, blir den nya tillgången aktuell tillgång och balanseringsproceduren börjar om.</span><span class="sxs-lookup"><span data-stu-id="760f7-129">If it is, the new supply becomes current supply and the balancing procedure starts over.</span></span>  

<span data-ttu-id="760f7-130">Följande visar en grafisk illustration av den här principen:</span><span class="sxs-lookup"><span data-stu-id="760f7-130">The following shows a graphical illustration of this principle:</span></span>  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. <span data-ttu-id="760f7-131">Tillgång **Sa** of 4 (fast) stänger Efterfrågan **Da** of -3.</span><span class="sxs-lookup"><span data-stu-id="760f7-131">Supply **Sa** of 4 (fixed) closes Demand **Da** of -3.</span></span>  
2. <span data-ttu-id="760f7-132">CloseDemand: Skapa en minska-påminnelse på -3 (visas inte).</span><span class="sxs-lookup"><span data-stu-id="760f7-132">CloseDemand: Create a decrease reminder of -3 (not shown).</span></span>  
3. <span data-ttu-id="760f7-133">Tillgång **Sa** har stängts med ett överskott på 1 (inget mer behov finns).</span><span class="sxs-lookup"><span data-stu-id="760f7-133">Supply **Sa** is closed with a surplus of 1 (no more demand exists).</span></span>  

     <span data-ttu-id="760f7-134">Det här ökar den planerade lagernivån till +4, medan det planerade **tillgängliga** lagret blir -1.</span><span class="sxs-lookup"><span data-stu-id="760f7-134">This increases the projected inventory level to +4, while the projected **available** inventory becomes -1.</span></span>  

4. <span data-ttu-id="760f7-135">Nästa tillgång **Sb** av 2 (en annan order) redan har placerats på tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="760f7-135">The next supply **Sb** of 2 (another order) has already been placed on the timeline.</span></span>  
5. <span data-ttu-id="760f7-136">Systemet kontrollerar om det finns någon minska-påminnelse som föregår **Sb** (det finns det inte, så ingen åtgärd vidtas).</span><span class="sxs-lookup"><span data-stu-id="760f7-136">System checks if there is any decrease reminder preceding **Sb** (there is not, so no action is taken).</span></span>  
6. <span data-ttu-id="760f7-137">Systemet stänger tillgång **Sb** (ingen mer efterfrågan finns)—antingen A: genom att minska den till 0 (annullera) eller B: genom att låta den vara som den är.</span><span class="sxs-lookup"><span data-stu-id="760f7-137">System closes supply **Sb** (no more demand exists)—either A: by reducing it to 0 (cancel) or B: by leaving as is.</span></span>  

     <span data-ttu-id="760f7-138">Ökar den planerade lagernivån (A: +0 => +4 or B: +2 = +6).</span><span class="sxs-lookup"><span data-stu-id="760f7-138">This increases the projected inventory level (A: +0 => +4 or B: +2 = +6).</span></span>  

7. <span data-ttu-id="760f7-139">System gör en sista kontroll: Finns det någon minska-påminnelse?</span><span class="sxs-lookup"><span data-stu-id="760f7-139">System makes a final check: Is there any decrease reminder?</span></span> <span data-ttu-id="760f7-140">Ja, det finns ett på datumet för **Da**.</span><span class="sxs-lookup"><span data-stu-id="760f7-140">Yes, there is one on the date of **Da**.</span></span>  
8. <span data-ttu-id="760f7-141">Programmet lägger till minska-påminnelsen på -3 påminnelse till den planerade lagernivån, antingen A: +4 -3 = 1 eller B: +6 -3 = +3.</span><span class="sxs-lookup"><span data-stu-id="760f7-141">System adds the decrease reminder of -3 reminder to the projected inventory level, either A: +4 -3 = 1 or B: +6 -3 = +3.</span></span>  
9. <span data-ttu-id="760f7-142">I händelse av A skapas automatiskt framåtplanerad order som startar på datumet **Da**.</span><span class="sxs-lookup"><span data-stu-id="760f7-142">In case of A, the system creates a forward-scheduled order starting on date **Da**.</span></span>  

     <span data-ttu-id="760f7-143">I händelse av B når vi beställningspunkten och en ny order skapas.</span><span class="sxs-lookup"><span data-stu-id="760f7-143">In case of B, the reorder point is reached and a new order is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="760f7-144">Se även</span><span class="sxs-lookup"><span data-stu-id="760f7-144">See Also</span></span>  
<span data-ttu-id="760f7-145">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="760f7-145">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="760f7-146">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="760f7-146">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="760f7-147">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="760f7-147">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="760f7-148">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="760f7-148">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

