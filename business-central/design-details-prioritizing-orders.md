---
title: Designdetaljer - Prioritera order | Microsoft Docs
description: "Mer information om hur du prioriterar för att täcka både krav för efterfrågan och tillgång."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 1d58a02bdfe4810d1116d20866d3b435bc7341bc
ms.contentlocale: sv-se
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="8ed14-103">Designdetaljer: Prioritera order</span><span class="sxs-lookup"><span data-stu-id="8ed14-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="8ed14-104">Inom en given lagerställeenhet representerar det begärda eller tillgängliga datumet den högsta prioriteten. Dagens efterfrågan ska hanteras före nästa veckas efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="8ed14-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="8ed14-105">Men utöver den här allmänna prioriteten föreslår planeringssystemet också vilken typ av efterfrågan som ska uppfyllas innan övrig efterfrågan uppfylls.</span><span class="sxs-lookup"><span data-stu-id="8ed14-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="8ed14-106">På samma sätt kommer det att föreslå vilken tillgångskälla som ska kopplas innan du kopplar andra tillgångskällor.</span><span class="sxs-lookup"><span data-stu-id="8ed14-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="8ed14-107">Det utförs i enlighet med orderprioriteter.</span><span class="sxs-lookup"><span data-stu-id="8ed14-107">This is done according to order priorities.</span></span>  

<span data-ttu-id="8ed14-108">Den laddade efterfrågan och tillgången bidrar till en profil för planerade lagret enligt följande prioriteter:</span><span class="sxs-lookup"><span data-stu-id="8ed14-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  

## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="8ed14-109">Prioriteter på efterfråganssidan</span><span class="sxs-lookup"><span data-stu-id="8ed14-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="8ed14-110">Redan levererat: Artikeltransaktion</span><span class="sxs-lookup"><span data-stu-id="8ed14-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="8ed14-111">Inköpsreturorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="8ed14-112">Reservationstransaktion</span><span class="sxs-lookup"><span data-stu-id="8ed14-112">Sales Order</span></span>  
4. <span data-ttu-id="8ed14-113">Tjänsteorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-113">Service Order</span></span>  
5. <span data-ttu-id="8ed14-114">Produktionskomponentbehov</span><span class="sxs-lookup"><span data-stu-id="8ed14-114">Production Component Need</span></span>  
6. <span data-ttu-id="8ed14-115">Monteringsorderrad</span><span class="sxs-lookup"><span data-stu-id="8ed14-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="8ed14-116">Avgående överföringsorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="8ed14-117">Avropsorder (som inte redan har förbrukats av motsvarande försäljningsorder)</span><span class="sxs-lookup"><span data-stu-id="8ed14-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="8ed14-118">Prognos (som inte redan har förbrukats av andra försäljningsorder)</span><span class="sxs-lookup"><span data-stu-id="8ed14-118">Forecast (that has not already been consumed by other sales orders)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8ed14-119">Köpreturer ingår vanligtvis inte i tillförselplanläggning; de ska alltid reserverats från partiet som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="8ed14-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="8ed14-120">Om de inte har reserverats spelar inköpsreturer en roll i dispositionen och är högt prioriterade för att undvika att planeringssystemet föreslår en leveransorder bara för att hantera en inköpsretur.</span><span class="sxs-lookup"><span data-stu-id="8ed14-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  

## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="8ed14-121">Prioriteter på tillgångssidan</span><span class="sxs-lookup"><span data-stu-id="8ed14-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="8ed14-122">Finns redan i lager: Artikeltransaktion (Planeringsflexibilitet = Ingen)</span><span class="sxs-lookup"><span data-stu-id="8ed14-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="8ed14-123">Försäljningsreturorder (planeringsflexibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="8ed14-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="8ed14-124">Ankommande överföringsorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="8ed14-125">Produktionsorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-125">Production Order</span></span>  
5. <span data-ttu-id="8ed14-126">Monteringsorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-126">Assembly Order</span></span>  
6. <span data-ttu-id="8ed14-127">Inköpsorder</span><span class="sxs-lookup"><span data-stu-id="8ed14-127">Purchase Order</span></span>  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="8ed14-128">Prioritet kopplad till status för efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="8ed14-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="8ed14-129">Förutom prioriteter som anges av typen av efterfrågan och tillgång, definierar ordrarnas aktuella status i körningsprocessen också en prioritet.</span><span class="sxs-lookup"><span data-stu-id="8ed14-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="8ed14-130">Till exempel har lageraktiviteter en inverkan, och status för försäljningar, köp, överföringar, montering och produktionsorder tas med i beräkningen:</span><span class="sxs-lookup"><span data-stu-id="8ed14-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  

1. <span data-ttu-id="8ed14-131">Hanteras delvis (planeringsflexibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="8ed14-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="8ed14-132">Redan pågående i distributionslagret (Planeringsflexibilitet = Ingen)</span><span class="sxs-lookup"><span data-stu-id="8ed14-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="8ed14-133">Släppt – alla ordertyper (Planeringsflexibilitet = Obegränsad)</span><span class="sxs-lookup"><span data-stu-id="8ed14-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="8ed14-134">Fast planerad produktionsorder (Planeringsflexibilitet = Obegränsad)</span><span class="sxs-lookup"><span data-stu-id="8ed14-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="8ed14-135">Planerad/öppen – alla ordertyper (Planeringsflexibilitet = Obegränsad)</span><span class="sxs-lookup"><span data-stu-id="8ed14-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8ed14-136">Se även</span><span class="sxs-lookup"><span data-stu-id="8ed14-136">See Also</span></span>  
<span data-ttu-id="8ed14-137">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="8ed14-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="8ed14-138">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="8ed14-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="8ed14-139">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="8ed14-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

