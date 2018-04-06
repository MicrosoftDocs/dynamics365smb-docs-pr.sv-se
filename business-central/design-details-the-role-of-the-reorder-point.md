---
title: "Designdetaljer - Beställningspunktens roll | Microsoft Docs"
description: "Det här avsnittet beskriver vikten av att ställa in en beställningspunkt, så att du vet när du ska beställa flera lager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a64d71ca9f163793c959126da09ffa4ef281b5e0
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="3b022-103">Designdetaljer: Beställningspunktens roll</span><span class="sxs-lookup"><span data-stu-id="3b022-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="3b022-104">Förutom allmän balansering av efterfrågan och tillgång måste planeringssystemet också övervaka lagernivåer för de påverkade artiklarna för att respektera de definierade partiformningsmetoderna.</span><span class="sxs-lookup"><span data-stu-id="3b022-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  
  
<span data-ttu-id="3b022-105">En beställningspunkt representerar efterfrågan under ledtid.</span><span class="sxs-lookup"><span data-stu-id="3b022-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="3b022-106">När det planerade lagret hamnar under lagernivån som definieras av beställningspunkten är det dags att beställa ytterligare antal.</span><span class="sxs-lookup"><span data-stu-id="3b022-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="3b022-107">Under tiden förväntas lagret minska gradvis och eventuellt nå noll (eller säkerhetslagernivån), tills återanskaffning anländer.</span><span class="sxs-lookup"><span data-stu-id="3b022-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  
  
<span data-ttu-id="3b022-108">Planeringssystemet föreslår en framåtplanerad leveransorder när planerat lager hamnar under beställningspunkten.</span><span class="sxs-lookup"><span data-stu-id="3b022-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  
  
<span data-ttu-id="3b022-109">Beställningspunkten beskriver en viss lagernivå.</span><span class="sxs-lookup"><span data-stu-id="3b022-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="3b022-110">Lagernivåer kan förändras markant under tidsenheten, och därför måste planeringssystemet ständigt övervaka det planerade tillgängliga lagret.</span><span class="sxs-lookup"><span data-stu-id="3b022-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b022-111">Se även</span><span class="sxs-lookup"><span data-stu-id="3b022-111">See Also</span></span>  
<span data-ttu-id="3b022-112">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3b022-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="3b022-113">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="3b022-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="3b022-114">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3b022-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="3b022-115">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="3b022-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
