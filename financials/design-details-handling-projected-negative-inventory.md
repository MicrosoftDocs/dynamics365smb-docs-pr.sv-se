---
title: Designdetaljer - Hantera planerat negativt lagersaldo | Microsoft Docs
description: "Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln. När beställningspunkten har passerats är det dags att beställa mer. Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot. Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå."
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
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="8789f-106">Designdetaljer: Hantera planerat negativt lagersaldo</span><span class="sxs-lookup"><span data-stu-id="8789f-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="8789f-107">Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln.</span><span class="sxs-lookup"><span data-stu-id="8789f-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="8789f-108">När beställningspunkten har passerats är det dags att beställa mer.</span><span class="sxs-lookup"><span data-stu-id="8789f-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="8789f-109">Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot.</span><span class="sxs-lookup"><span data-stu-id="8789f-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="8789f-110">Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå.</span><span class="sxs-lookup"><span data-stu-id="8789f-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="8789f-111">Därför anser planeringssystemet att det är ett nödläge om en framtida efterfrågan inte kan uppfyllas från det planerade lagret, eller uttryckt på ett annat sätt, att det planerade lagret blir negativt.</span><span class="sxs-lookup"><span data-stu-id="8789f-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="8789f-112">Systemet hanterar ett sådant undantag genom att föreslå en ny leveransorder för att uppfylla en del av behovet som inte kan uppfyllas av lager eller annan tillgång.</span><span class="sxs-lookup"><span data-stu-id="8789f-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="8789f-113">Orderstorleken för den nya leveransordern beaktar inte maximalt lager eller beställningsantal och beaktar inte heller ordermodifierarna Maximal partistorlek, Minsta partistorlek och Partistorleksmultipel.</span><span class="sxs-lookup"><span data-stu-id="8789f-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="8789f-114">I stället motsvarar det den exakta bristen.</span><span class="sxs-lookup"><span data-stu-id="8789f-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="8789f-115">Planeringsraden för den här typen av leveransorder ska innehålla en nödvarningsikon och ytterligare information finns i fältet för att informera användaren om situationen.</span><span class="sxs-lookup"><span data-stu-id="8789f-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="8789f-116">I följande illustration representerar D en nödleveransorder för att justera för ett negativt lagersaldo.</span><span class="sxs-lookup"><span data-stu-id="8789f-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  <span data-ttu-id="8789f-117">Tillgång **A**, initialt planerat lager, är nedanför beställningspunkt.</span><span class="sxs-lookup"><span data-stu-id="8789f-117">Supply **A**, initial projected inventory, is below reorder point.</span></span>  

2.  <span data-ttu-id="8789f-118">En ny framåtplanerad tillgång skapas (**C**).</span><span class="sxs-lookup"><span data-stu-id="8789f-118">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="8789f-119">(Antal = Beställningsgräns – Planerad lagernivå)</span><span class="sxs-lookup"><span data-stu-id="8789f-119">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  

3.  <span data-ttu-id="8789f-120">Tillgång **A** är stängd efter efterfrågan **B**, som inte täcks helt.</span><span class="sxs-lookup"><span data-stu-id="8789f-120">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="8789f-121">(Behov **B** kan försöka schemalägga Tillgång C, men det kommer inte att hända enligt följande tidsenhetsbegreppet.)</span><span class="sxs-lookup"><span data-stu-id="8789f-121">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  

4.  <span data-ttu-id="8789f-122">Ny leverans (**D**) skapas för att täcka det återstående antalet i efterfrågan **B**.</span><span class="sxs-lookup"><span data-stu-id="8789f-122">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  

5.  <span data-ttu-id="8789f-123">Efterfrågan **B** är stängd (och skapar en betalningspåminnelse till det planerade lagret).</span><span class="sxs-lookup"><span data-stu-id="8789f-123">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  

6.  <span data-ttu-id="8789f-124">Den nya tillgången **D** stängs.</span><span class="sxs-lookup"><span data-stu-id="8789f-124">The new supply **D** is closed.</span></span>  

7.  <span data-ttu-id="8789f-125">Planerat lager kontrolleras; beställningspunkten har inte passerats.</span><span class="sxs-lookup"><span data-stu-id="8789f-125">Projected Inventory is checked; reorder point has not been crossed.</span></span>  

8.  <span data-ttu-id="8789f-126">Tillgång **C** är stängd (ingen mer efterfrågan finns).</span><span class="sxs-lookup"><span data-stu-id="8789f-126">Supply **C** is closed (no more demand exists).</span></span>  

9. <span data-ttu-id="8789f-127">Sista kontroll: Inga utestående lagernivåpåminnelser finns.</span><span class="sxs-lookup"><span data-stu-id="8789f-127">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8789f-128">Moment 4 återspeglar hur godkännandesystemet på tidigare versioner än Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="8789f-128">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="8789f-129">Detta slutför beskrivningen av centrala principer för lagerplanering baserat på partiformningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="8789f-129">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="8789f-130">Följande avsnitt beskriver egenskaperna för de fyra partiformningsmetoderna som stöds.</span><span class="sxs-lookup"><span data-stu-id="8789f-130">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8789f-131">Se även</span><span class="sxs-lookup"><span data-stu-id="8789f-131">See Also</span></span>  
 <span data-ttu-id="8789f-132">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="8789f-132">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="8789f-133">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="8789f-133">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="8789f-134">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="8789f-134">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="8789f-135">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="8789f-135">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

