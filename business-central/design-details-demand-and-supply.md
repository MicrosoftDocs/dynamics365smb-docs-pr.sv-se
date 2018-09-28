---
title: "Designdetaljer - Balansera efterfrågan och tillgång | Microsoft Docs"
description: "Efterfrågan är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder. Dessutom tillåter programmet mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer."
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
ms.openlocfilehash: ad46c0a298ecd77f69375b7427193de464f6604c
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="920cd-104">Designdetaljer: Efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="920cd-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="920cd-105">Efterfrågan är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="920cd-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="920cd-106">Dessutom tillåter programmet mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer.</span><span class="sxs-lookup"><span data-stu-id="920cd-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
 <span data-ttu-id="920cd-107">Tillgång är den term som vanligtvis används för alla typer av positivt eller ankommande antal, t.ex. inköpsöverföringar, monteringsöverföringar, produktionsöverföringar och ankommande överföringar.</span><span class="sxs-lookup"><span data-stu-id="920cd-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="920cd-108">Dessutom kan en försäljningsretur också representera tillgång.</span><span class="sxs-lookup"><span data-stu-id="920cd-108">In addition, a sales return may also represent supply.</span></span>  
  
 <span data-ttu-id="920cd-109">För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.</span><span class="sxs-lookup"><span data-stu-id="920cd-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="920cd-110">En profil innehåller efterfråganshändelser och den andra innehåller motsvarande tillgångshändelser.</span><span class="sxs-lookup"><span data-stu-id="920cd-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="920cd-111">Varje händelse representerar en ordernätverksenhet, till exempel en försäljningsorderrad, en artikeltransaktion eller en produktionsorderrad.</span><span class="sxs-lookup"><span data-stu-id="920cd-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
 <span data-ttu-id="920cd-112">När lagerprofiler laddas balanseras de olika uppsättningarna med efterfrågan-tillgång för att skapa ut en tillförselplan som uppfyller de angivna målen.</span><span class="sxs-lookup"><span data-stu-id="920cd-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
 <span data-ttu-id="920cd-113">Planeringsparametrar och lagernivåer är andra typer av efterfrågan och tillgång, som genomgår integrerad motkontering för att fylla på lagerartiklar.</span><span class="sxs-lookup"><span data-stu-id="920cd-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="920cd-114">Mer information finns i [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="920cd-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="920cd-115">Se även</span><span class="sxs-lookup"><span data-stu-id="920cd-115">See Also</span></span>  
 <span data-ttu-id="920cd-116">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="920cd-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="920cd-117">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="920cd-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="920cd-118">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="920cd-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
