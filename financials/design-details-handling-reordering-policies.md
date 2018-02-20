---
title: Designdetaljer - Hantera partiformningsmetoder | Microsoft Docs
description: "Översikt över aktiviteter för att definiera en ombeställningsmetod inom leveransplanering."
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
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="5da0b-103">Designdetaljer: Hantera partiformningsmetoder</span><span class="sxs-lookup"><span data-stu-id="5da0b-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="5da0b-104">För att en artikel ska ingå i leveransplanering måste en ombeställningsmetod definieras.</span><span class="sxs-lookup"><span data-stu-id="5da0b-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="5da0b-105">Följande fyra partiformningsmetoder finns:</span><span class="sxs-lookup"><span data-stu-id="5da0b-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="5da0b-106">Fast orderkvantitet</span><span class="sxs-lookup"><span data-stu-id="5da0b-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="5da0b-107">Maximalt antal</span><span class="sxs-lookup"><span data-stu-id="5da0b-107">Maximum Qty.</span></span>  
* <span data-ttu-id="5da0b-108">Order</span><span class="sxs-lookup"><span data-stu-id="5da0b-108">Order</span></span>  
* <span data-ttu-id="5da0b-109">Parti-för-parti</span><span class="sxs-lookup"><span data-stu-id="5da0b-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="5da0b-110">Metoderna Fast orderkvantitet och Maximalt antal avser lagerplanering.</span><span class="sxs-lookup"><span data-stu-id="5da0b-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="5da0b-111">Även om lagerplaneringen är tekniskt enklare än motkonteringen, måste de här metoderna finnas samtidigt som steg-för-steg-motkontering av tillgångs- och orderspårning.</span><span class="sxs-lookup"><span data-stu-id="5da0b-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="5da0b-112">För att kontrollera integrering mellan de två och ge insyn i den komplicerade planeringslogiken finns strikta principer för hur partiformningsmetoder hanteras.</span><span class="sxs-lookup"><span data-stu-id="5da0b-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5da0b-113">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="5da0b-113">In This Section</span></span>  
[<span data-ttu-id="5da0b-114">Designdetaljer: Beställningspunktens roll</span><span class="sxs-lookup"><span data-stu-id="5da0b-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="5da0b-115">Designdetaljer: Övervaka den planerade lagernivån och beställningspunkten</span><span class="sxs-lookup"><span data-stu-id="5da0b-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="5da0b-116">Designdetaljer: Tidsenhetens roll</span><span class="sxs-lookup"><span data-stu-id="5da0b-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="5da0b-117">Designdetaljer: Hålla sig under överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="5da0b-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="5da0b-118">Designdetaljer: Hantera planerat negativt lagersaldo</span><span class="sxs-lookup"><span data-stu-id="5da0b-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="5da0b-119">Designdetaljer: Partiformningsmetoder</span><span class="sxs-lookup"><span data-stu-id="5da0b-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="5da0b-120">Se även</span><span class="sxs-lookup"><span data-stu-id="5da0b-120">See Also</span></span>  
<span data-ttu-id="5da0b-121">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="5da0b-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="5da0b-122">[Designdetaljer: Planeringstilldelningstabell](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="5da0b-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="5da0b-123">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="5da0b-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="5da0b-124">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="5da0b-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="5da0b-125">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="5da0b-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
