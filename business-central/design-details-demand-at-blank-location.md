---
title: Designdetaljer - Balansera efterfrågan och tillgång | Microsoft Docs
description: Detta ämne introducerar begreppet etfterfrågan, som är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 8cf7ffe90ccaf32258b4a51fb12f93a8df8ba7eb
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807946"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="ded93-103">Designdetaljer: Efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="ded93-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="ded93-104">Efterfrågan är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ded93-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="ded93-105">Dessutom tillåter programmet mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer.</span><span class="sxs-lookup"><span data-stu-id="ded93-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="ded93-106">Tillgång är den term som vanligtvis används för alla typer av positivt eller ankommande antal, t.ex. inköpsöverföringar, monteringsöverföringar, produktionsöverföringar och ankommande överföringar.</span><span class="sxs-lookup"><span data-stu-id="ded93-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="ded93-107">Dessutom kan en försäljningsretur också representera tillgång.</span><span class="sxs-lookup"><span data-stu-id="ded93-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="ded93-108">För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.</span><span class="sxs-lookup"><span data-stu-id="ded93-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="ded93-109">En profil innehåller efterfråganshändelser och den andra innehåller motsvarande tillgångshändelser.</span><span class="sxs-lookup"><span data-stu-id="ded93-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="ded93-110">Varje händelse representerar en ordernätverksenhet, till exempel en försäljningsorderrad, en artikeltransaktion eller en produktionsorderrad.</span><span class="sxs-lookup"><span data-stu-id="ded93-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="ded93-111">När lagerprofiler laddas balanseras de olika uppsättningarna med efterfrågan-tillgång för att skapa ut en tillförselplan som uppfyller de angivna målen.</span><span class="sxs-lookup"><span data-stu-id="ded93-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="ded93-112">Planeringsparametrar och lagernivåer är andra typer av efterfrågan och tillgång, som genomgår integrerad motkontering för att fylla på lagerartiklar.</span><span class="sxs-lookup"><span data-stu-id="ded93-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="ded93-113">Mer information finns i [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ded93-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ded93-114">Se även</span><span class="sxs-lookup"><span data-stu-id="ded93-114">See Also</span></span>  
<span data-ttu-id="ded93-115">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="ded93-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="ded93-116">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="ded93-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="ded93-117">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="ded93-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)