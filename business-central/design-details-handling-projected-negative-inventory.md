---
title: Designdetaljer - Hantera planerat negativt lagersaldo | Microsoft Docs
description: "Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln. När beställningspunkten har passerats är det dags att beställa mer. Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot. Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå."
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
ms.openlocfilehash: 25a2017fd91f09a9d7725c68ffaa0df48a041294
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="a272d-106">Designdetaljer: Hantera planerat negativt lagersaldo</span><span class="sxs-lookup"><span data-stu-id="a272d-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="a272d-107">Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln.</span><span class="sxs-lookup"><span data-stu-id="a272d-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="a272d-108">När beställningspunkten har passerats är det dags att beställa mer.</span><span class="sxs-lookup"><span data-stu-id="a272d-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="a272d-109">Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot.</span><span class="sxs-lookup"><span data-stu-id="a272d-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="a272d-110">Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå.</span><span class="sxs-lookup"><span data-stu-id="a272d-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="a272d-111">Därför anser planeringssystemet att det är ett nödläge om en framtida efterfrågan inte kan uppfyllas från det planerade lagret, eller uttryckt på ett annat sätt, att det planerade lagret blir negativt.</span><span class="sxs-lookup"><span data-stu-id="a272d-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="a272d-112">Systemet hanterar ett sådant undantag genom att föreslå en ny leveransorder för att uppfylla en del av behovet som inte kan uppfyllas av lager eller annan tillgång.</span><span class="sxs-lookup"><span data-stu-id="a272d-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="a272d-113">Orderstorleken för den nya leveransordern beaktar inte maximalt lager eller beställningsantal och beaktar inte heller ordermodifierarna Maximal partistorlek, Minsta partistorlek och Partistorleksmultipel.</span><span class="sxs-lookup"><span data-stu-id="a272d-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="a272d-114">I stället motsvarar det den exakta bristen.</span><span class="sxs-lookup"><span data-stu-id="a272d-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="a272d-115">Planeringsraden för den här typen av leveransorder ska innehålla en nödvarningsikon och ytterligare information finns i fältet för att informera användaren om situationen.</span><span class="sxs-lookup"><span data-stu-id="a272d-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="a272d-116">I följande illustration representerar D en nödleveransorder för att justera för ett negativt lagersaldo.</span><span class="sxs-lookup"><span data-stu-id="a272d-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="a272d-117">![Förslag på nödplanering för att undvika negativt lagersaldo](media/nav_app_supply_planning_2_negative_inventory.png "Förslag på nödplanering för att undvika negativt lagersaldo")</span><span class="sxs-lookup"><span data-stu-id="a272d-117">![Emergency planning suggestion to avoid negative inventory](media/nav_app_supply_planning_2_negative_inventory.png "Emergency planning suggestion to avoid negative inventory")</span></span>  

1.  <span data-ttu-id="a272d-118">Tillgång **A**, initialt planerat lager, är nedanför beställningspunkt.</span><span class="sxs-lookup"><span data-stu-id="a272d-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  
2.  <span data-ttu-id="a272d-119">En ny framåtplanerad tillgång skapas (**C**).</span><span class="sxs-lookup"><span data-stu-id="a272d-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="a272d-120">(Antal = Beställningsgräns – Planerad lagernivå)</span><span class="sxs-lookup"><span data-stu-id="a272d-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  
3.  <span data-ttu-id="a272d-121">Tillgång **A** är stängd efter efterfrågan **B**, som inte täcks helt.</span><span class="sxs-lookup"><span data-stu-id="a272d-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="a272d-122">(Behov **B** kan försöka schemalägga Tillgång C, men det kommer inte att hända enligt följande tidsenhetsbegreppet.)</span><span class="sxs-lookup"><span data-stu-id="a272d-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  
4.  <span data-ttu-id="a272d-123">Ny leverans (**D**) skapas för att täcka det återstående antalet i efterfrågan **B**.</span><span class="sxs-lookup"><span data-stu-id="a272d-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  
5.  <span data-ttu-id="a272d-124">Efterfrågan **B** är stängd (och skapar en betalningspåminnelse till det planerade lagret).</span><span class="sxs-lookup"><span data-stu-id="a272d-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  
6.  <span data-ttu-id="a272d-125">Den nya tillgången **D** stängs.</span><span class="sxs-lookup"><span data-stu-id="a272d-125">The new supply **D** is closed.</span></span>  
7.  <span data-ttu-id="a272d-126">Planerat lager kontrolleras; beställningspunkten har inte passerats.</span><span class="sxs-lookup"><span data-stu-id="a272d-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  
8.  <span data-ttu-id="a272d-127">Tillgång **C** är stängd (ingen mer efterfrågan finns).</span><span class="sxs-lookup"><span data-stu-id="a272d-127">Supply **C** is closed (no more demand exists).</span></span>  
9. <span data-ttu-id="a272d-128">Sista kontroll: Inga utestående lagernivåpåminnelser finns.</span><span class="sxs-lookup"><span data-stu-id="a272d-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a272d-129">Moment 4 återspeglar hur godkännandesystemet på tidigare versioner än Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="a272d-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="a272d-130">Detta slutför beskrivningen av centrala principer för lagerplanering baserat på partiformningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="a272d-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="a272d-131">Följande avsnitt beskriver egenskaperna för de fyra partiformningsmetoderna som stöds.</span><span class="sxs-lookup"><span data-stu-id="a272d-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a272d-132">Se även</span><span class="sxs-lookup"><span data-stu-id="a272d-132">See Also</span></span>  
 <span data-ttu-id="a272d-133">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a272d-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="a272d-134">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="a272d-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="a272d-135">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a272d-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="a272d-136">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="a272d-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

