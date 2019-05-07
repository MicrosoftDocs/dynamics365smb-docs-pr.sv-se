---
title: Designdetaljer - Begreppet motkonto i korthet | Microsoft Docs
description: Efterfrågan anges av ett företags kunder. Tillgång är det som företag kan skapa och ta bort för att fastställa saldo. Planeringssystemet börjar med den icke-härledda efterfrågan och spårar sedan tillbaka till tillgången.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8684389c75299dc57a2056041b50ebde37a0bea1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "941309"
---
# <a name="design-details-the-concept-of-balancing-in-brief"></a><span data-ttu-id="e4076-105">Designdetaljer: Begreppet motkonto i korthet</span><span class="sxs-lookup"><span data-stu-id="e4076-105">Design Details: The Concept of Balancing in Brief</span></span>
<span data-ttu-id="e4076-106">Efterfrågan anges av ett företags kunder.</span><span class="sxs-lookup"><span data-stu-id="e4076-106">Demand is given by a company’s customers.</span></span> <span data-ttu-id="e4076-107">Tillgång är det som företag kan skapa och ta bort för att fastställa saldo.</span><span class="sxs-lookup"><span data-stu-id="e4076-107">Supply is what the company can create and remove to establish balance.</span></span> <span data-ttu-id="e4076-108">Planeringssystemet börjar med den icke-härledda efterfrågan och spårar sedan tillbaka till tillgången.</span><span class="sxs-lookup"><span data-stu-id="e4076-108">The planning system starts with the independent demand and then tracks backwards to the supply.</span></span>  

 <span data-ttu-id="e4076-109">Lagerprofilerna används för att innehålla information om efterfrågan och tillgång, antal och tidsplan.</span><span class="sxs-lookup"><span data-stu-id="e4076-109">The inventory profiles are used to contain information about the demands and supplies, quantities, and timing.</span></span> <span data-ttu-id="e4076-110">Dessa profiler utgör grunden för de två sidorna av den balanserande skalan.</span><span class="sxs-lookup"><span data-stu-id="e4076-110">These profiles essentially make up the two sides of the balancing scale.</span></span>  

 <span data-ttu-id="e4076-111">Syftet med planläggningsmekanismen är att balansera efterfrågan och tillgång för en artikel för att se till att tillgång matchar efterfrågan på ett genomförbart sätt som definieras av planläggningsparametrar och regler.</span><span class="sxs-lookup"><span data-stu-id="e4076-111">The objective of the planning mechanism is to counterbalance the demand and supply of an item to ensure that supply will match demand in a feasible way as defined by the planning parameters and rules.</span></span>  

 <span data-ttu-id="e4076-112">![Översikt över balansering av tillgång och efterfrågan](media/nav_app_supply_planning_2_balancing.png "Översikt över balansering av tillgång och efterfrågan")</span><span class="sxs-lookup"><span data-stu-id="e4076-112">![Overview of supply-demand balancing](media/nav_app_supply_planning_2_balancing.png "Overview of supply-demand balancing")</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4076-113">Se även</span><span class="sxs-lookup"><span data-stu-id="e4076-113">See Also</span></span>  
 <span data-ttu-id="e4076-114">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="e4076-114">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="e4076-115">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="e4076-115">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="e4076-116">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="e4076-116">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
