---
title: Designdetaljer - Balansera efterfrågan och tillgång | Microsoft Docs
description: Efterfrågan är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder. Dessutom tillåter programmet mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: ad6684bb1fefe10fc965c3c8a7780c6aa8a9d685
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807935"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="0dc13-104">Designdetaljer: Efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="0dc13-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="0dc13-105">Efterfrågan är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="0dc13-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="0dc13-106">Dessutom tillåter programmet mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer.</span><span class="sxs-lookup"><span data-stu-id="0dc13-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="0dc13-107">Tillgång är den term som vanligtvis används för alla typer av positivt eller ankommande antal, t.ex. inköpsöverföringar, monteringsöverföringar, produktionsöverföringar och ankommande överföringar.</span><span class="sxs-lookup"><span data-stu-id="0dc13-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="0dc13-108">Dessutom kan en försäljningsretur också representera tillgång.</span><span class="sxs-lookup"><span data-stu-id="0dc13-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="0dc13-109">För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.</span><span class="sxs-lookup"><span data-stu-id="0dc13-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="0dc13-110">En profil innehåller efterfråganshändelser och den andra innehåller motsvarande tillgångshändelser.</span><span class="sxs-lookup"><span data-stu-id="0dc13-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="0dc13-111">Varje händelse representerar en ordernätverksenhet, till exempel en försäljningsorderrad, en artikeltransaktion eller en produktionsorderrad.</span><span class="sxs-lookup"><span data-stu-id="0dc13-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="0dc13-112">När lagerprofiler laddas balanseras de olika uppsättningarna med efterfrågan-tillgång för att skapa ut en tillförselplan som uppfyller de angivna målen.</span><span class="sxs-lookup"><span data-stu-id="0dc13-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="0dc13-113">Planeringsparametrar och lagernivåer är andra typer av efterfrågan och tillgång, som genomgår integrerad motkontering för att fylla på lagerartiklar.</span><span class="sxs-lookup"><span data-stu-id="0dc13-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="0dc13-114">Mer information finns i [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0dc13-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0dc13-115">Se även</span><span class="sxs-lookup"><span data-stu-id="0dc13-115">See Also</span></span>  
 <span data-ttu-id="0dc13-116">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="0dc13-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="0dc13-117">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="0dc13-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="0dc13-118">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="0dc13-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
