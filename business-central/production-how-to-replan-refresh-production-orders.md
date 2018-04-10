---
title: Omplanera eller uppdatera produktionsorder direkt | Microsoft Docs
description: "Produktionsorderraderna innehåller de artiklar som ska produceras i produktionsordern."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 356c8e6d87fd54be3be376ec4320d3a9aa26d834
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="replan-or-refresh-production-orders-directly"></a><span data-ttu-id="e79cd-103">Omplanera eller uppdatera produktionsorder direkt</span><span class="sxs-lookup"><span data-stu-id="e79cd-103">Replan or Refresh Production Orders Directly</span></span>
<span data-ttu-id="e79cd-104">Funktionen **Omplanera** på produktionsorder används vanligtvis när du har lagt till eller ändrat komponenter som utgör underliggande produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e79cd-104">The **Replan** function on production orders is typically used after you have added or changed components that constitute underlying production orders.</span></span> <span data-ttu-id="e79cd-105">Funktionen beräknar de ändringar som gjorts på komponent- och verksamhetsföljdsrader, och artiklar på lägre produktionsstrukturnivåer beaktas. Detta innebär att nya produktionsorder kan skapas för dessa artiklar.</span><span class="sxs-lookup"><span data-stu-id="e79cd-105">The function calculates changes made to components and routings lines, and it includes items on lower production BOM levels for which it may generate new production orders.</span></span>  

<span data-ttu-id="e79cd-106">Funktionen Omplanera utgår ifrån de ändringar som du har gjort på komponent- och verksamhetsföljdsrader, och beräknar och planerar för eventuella nya behov för produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="e79cd-106">Based on the changes you have made to the components and routing lines, the Replan function calculates and plans for any new demand for the production order.</span></span>  

<span data-ttu-id="e79cd-107">Funktioen **uppdatera** för produktionsorder används vanligtvis när du har gjort något av följande:</span><span class="sxs-lookup"><span data-stu-id="e79cd-107">The **Refresh** function on production orders is typically used after you have done one of the following:</span></span>

- <span data-ttu-id="e79cd-108">Skapat ett produktionsorderhuvud manuellt för att beräkna och skapa radinformation för första gången.</span><span class="sxs-lookup"><span data-stu-id="e79cd-108">Created a production order header manually to calculate and create line data for the first time.</span></span>
- <span data-ttu-id="e79cd-109">Gjort ändringar i produktionsorderhuvudet för att beräkna om all radinformation.</span><span class="sxs-lookup"><span data-stu-id="e79cd-109">Made changes to the production order header to recalculate all the line data.</span></span>

<span data-ttu-id="e79cd-110">Uppdateringsfunktionen beräknar de ändringar som gjorts i ett produktionsorderhuvud, och produktionsstrukturnivåer beaktas inte.</span><span class="sxs-lookup"><span data-stu-id="e79cd-110">The Refresh function calculates changes made to a production order header and does not involve production BOM levels.</span></span> <span data-ttu-id="e79cd-111">Funktionen beräknar och initialiserar värdena på komponent- och verksamhetsföljdsrader utifrån de standarduppgifter som har angetts i den tilldelade produktionsstrukturen och verksamhetsföljden, och enligt den orderkvantitet och förfallodatum som har angetts i produktionsorderhuvudet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-111">The function calculates and initiates the values of the component lines and routing lines based on the master data defined in the assigned production BOM and routing, according to the order quantity and due date on the production order’s header.</span></span>

<span data-ttu-id="e79cd-112">Du kan antingen infoga produktionsorderraderna manuellt eller använda en funktion som beräknar produktionsorderraderna från huvudet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-112">You can either insert the production order lines manually or use the function that calculates the production order lines from the header.</span></span>  

> [!NOTE]
> <span data-ttu-id="e79cd-113">Om du använder funktionen Uppdatera för att omberäkna produktionsorderraderna kommer de gamla produktionsorderraderna tas bort och nya beräknas.</span><span class="sxs-lookup"><span data-stu-id="e79cd-113">If you use the Refresh function to recalculate production order lines, the old production order lines are deleted and new lines are calculated.</span></span>  

## <a name="to-replan-a-production-order"></a><span data-ttu-id="e79cd-114">Så här planerar du om en produktionsorder</span><span class="sxs-lookup"><span data-stu-id="e79cd-114">To replan a production order</span></span>  
1.  <span data-ttu-id="e79cd-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Fasta planerade prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e79cd-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e79cd-116">Öppna den produktionsorder som du vill omplanera.</span><span class="sxs-lookup"><span data-stu-id="e79cd-116">Open the production order you want to replan.</span></span>  
3.  <span data-ttu-id="e79cd-117">På snabbfliken **Rader** väljer du åtgärden **Rader** och väljer sedan åtgärden **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="e79cd-117">On the **Lines** FastTab, choose the **Lines** action, and then choose the **Components** action.</span></span>  
4.  <span data-ttu-id="e79cd-118">Lägg till en komponent som är en producerad artikel eller halvfabrikat.</span><span class="sxs-lookup"><span data-stu-id="e79cd-118">Add a component, which is a produced item or subassembly.</span></span>  
5.  <span data-ttu-id="e79cd-119">Från produktionsordern väljer du åtgärden **Omplanera**.</span><span class="sxs-lookup"><span data-stu-id="e79cd-119">From the production order, choose the **Replan** action.</span></span>  

    <span data-ttu-id="e79cd-120">I fönstret **Omplanera produktionsorder** anger du vad som ska omplaneras och hur:</span><span class="sxs-lookup"><span data-stu-id="e79cd-120">In the **Replan Production Order** window, proceed to define how and what to replan.</span></span>  
6.  <span data-ttu-id="e79cd-121">I fältet **Planeringsriktning**, välj ett av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="e79cd-121">In the **Scheduling Direction** field, select one of the following options.</span></span>  

    |<span data-ttu-id="e79cd-122">Alternativ</span><span class="sxs-lookup"><span data-stu-id="e79cd-122">Option</span></span>|<span data-ttu-id="e79cd-123">Description</span><span class="sxs-lookup"><span data-stu-id="e79cd-123">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="e79cd-124">**Tillbaka**</span><span class="sxs-lookup"><span data-stu-id="e79cd-124">**Back**</span></span>|<span data-ttu-id="e79cd-125">Beräknar verksamhetssekvensen baklänges från det tidigaste möjliga slutdatumet, som definieras genom förfallodatumet och/eller andra planerade ordrar, till det senaste möjliga startdatumet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-125">Calculates the operation sequence backwards from the earliest possible ending date, defined by due date and/or other scheduled orders, to the latest possible starting date.</span></span> <span data-ttu-id="e79cd-126">**Obs!**  Det här är standardalternativet, som fungerar i de flesta situationer.</span><span class="sxs-lookup"><span data-stu-id="e79cd-126">**Note:**  This default option is relevant in the majority of situations.</span></span>|  
    |<span data-ttu-id="e79cd-127">**Framåt**</span><span class="sxs-lookup"><span data-stu-id="e79cd-127">**Forward**</span></span>|<span data-ttu-id="e79cd-128">Beräknar verksamhetssekvensen framåt från det senaste möjliga startdatumet, som definieras genom förfallodatumet och/eller andra planerade ordrar, till det tidigaste möjliga slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-128">Calculates the operation sequence forward from the earliest latest possible starting date, defined by due date and/or other scheduled orders, to the earliest possible ending date.</span></span> <span data-ttu-id="e79cd-129">**Obs!**  Detta alternativ fungerar endast för snabborder.</span><span class="sxs-lookup"><span data-stu-id="e79cd-129">**Note:**  This option is only relevant for expedite orders.</span></span>|  

7.  <span data-ttu-id="e79cd-130">I fältet **Planera** anger du om produktionsbehov för producerade artiklar i produktionsstrukturen ska beräknas:</span><span class="sxs-lookup"><span data-stu-id="e79cd-130">In the **Plan** field, select whether to calculate production requirements for produced items on the production BOM, as follows.</span></span>  

    |<span data-ttu-id="e79cd-131">Alternativ</span><span class="sxs-lookup"><span data-stu-id="e79cd-131">Option</span></span>|<span data-ttu-id="e79cd-132">Description</span><span class="sxs-lookup"><span data-stu-id="e79cd-132">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="e79cd-133">**Inga nivåer**</span><span class="sxs-lookup"><span data-stu-id="e79cd-133">**No Levels**</span></span>|<span data-ttu-id="e79cd-134">Produktion på lägre nivåer beaktas inte.</span><span class="sxs-lookup"><span data-stu-id="e79cd-134">Do not consider lower level production.</span></span> <span data-ttu-id="e79cd-135">Detta innebär att endast artikelns plan uppdateras (som vid en uppdatering).</span><span class="sxs-lookup"><span data-stu-id="e79cd-135">This only updates the item’s schedule, like refresh.</span></span>|  
    |<span data-ttu-id="e79cd-136">**En nivå**</span><span class="sxs-lookup"><span data-stu-id="e79cd-136">**One Level**</span></span>|<span data-ttu-id="e79cd-137">Planera för produktionsbehov på en nivå.</span><span class="sxs-lookup"><span data-stu-id="e79cd-137">Plan for first-level production demand.</span></span> <span data-ttu-id="e79cd-138">Produktionsorder kan skapas på första nivån.</span><span class="sxs-lookup"><span data-stu-id="e79cd-138">First-level production orders may be created.</span></span>|  
    |<span data-ttu-id="e79cd-139">**Alla nivåer**</span><span class="sxs-lookup"><span data-stu-id="e79cd-139">**All Levels**</span></span>|<span data-ttu-id="e79cd-140">Planera för produktionsbehov på alla nivåer.</span><span class="sxs-lookup"><span data-stu-id="e79cd-140">Plan for all-level production demand.</span></span> <span data-ttu-id="e79cd-141">Produktionsorder kan skapas på alla nivåer.</span><span class="sxs-lookup"><span data-stu-id="e79cd-141">All-level production orders may be created.</span></span>|  

8.  <span data-ttu-id="e79cd-142">Välj **En nivå** och klicka på **OK** om du vill omplanera produktionsordern samt beräkna och skapa en ny underliggande produktionsorder för det nya halvfabrikatet, om det inte är helt tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="e79cd-142">Select **One Level**, and choose the **OK** button to replan the production order, and calculate and create a new underlying production order for the introduced subassembly, if it is not fully available.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e79cd-143">De ändringar som genomförs via funktionen **Omplanering** ändrar förmodligen kapacitetsbehovet i produktionsordern, och du kan därför behöva planera om operationer när du har uppdaterat.</span><span class="sxs-lookup"><span data-stu-id="e79cd-143">Changes implemented with the **Replan** function are very likely to change the capacity need of the production order and you may therefore have to reschedule operations afterwards.</span></span>  

## <a name="to-refresh-a-production-order"></a><span data-ttu-id="e79cd-144">Så här uppdaterar du en produktionsorder</span><span class="sxs-lookup"><span data-stu-id="e79cd-144">To refresh a production order</span></span>  
<span data-ttu-id="e79cd-145">Om du har ändrat produktionsorderrader, komponenter eller verksamhetsföljdrader måste du också uppdatera informationen i produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="e79cd-145">If you have amended production order lines, components, or routing lines, you must also refresh the information on the production order.</span></span> <span data-ttu-id="e79cd-146">I följande procedur beräknas komponenterna för en fast planerad produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e79cd-146">In the following procedure, the components are calculated for a firm planned production order.</span></span> <span data-ttu-id="e79cd-147">Momenten är liknande för verksamhetsföljdsrader.</span><span class="sxs-lookup"><span data-stu-id="e79cd-147">The steps are similar for routing lines.</span></span>

1.  <span data-ttu-id="e79cd-148">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e79cd-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e79cd-149">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e79cd-149">Choose the **New** action.</span></span> <span data-ttu-id="e79cd-150">För mer information, se [Skapa produktionsorder](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="e79cd-150">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>  
3.  <span data-ttu-id="e79cd-151">Välj åtgärden **Uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="e79cd-151">Choose the **Refresh** action.</span></span>
4. <span data-ttu-id="e79cd-152">Du kan välja en av följande alternativ i fönstret **Uppdatera produktionsorder**:</span><span class="sxs-lookup"><span data-stu-id="e79cd-152">In the **Refresh Production Order** window, select one of the following options:</span></span>

    |<span data-ttu-id="e79cd-153">Alternativ</span><span class="sxs-lookup"><span data-stu-id="e79cd-153">Option</span></span>|<span data-ttu-id="e79cd-154">Description</span><span class="sxs-lookup"><span data-stu-id="e79cd-154">Description</span></span>|  
    |----------------------------------|---------------|---------------------------------------|  
    |<span data-ttu-id="e79cd-155">**Planeringsriktning**</span><span class="sxs-lookup"><span data-stu-id="e79cd-155">**Scheduling Direction**</span></span>|<span data-ttu-id="e79cd-156">**Framåt**</span><span class="sxs-lookup"><span data-stu-id="e79cd-156">**Forward**</span></span>|<span data-ttu-id="e79cd-157">Planeringen börjar vid startdatumet och fortsätter framåt till slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-157">Scheduling starts from the starting date and proceeds forward to the finishing date.</span></span> <span data-ttu-id="e79cd-158">Du måste fylla i startdatumet om du vill använda det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-158">You must fill in the starting date to use this option.</span></span>|  
    ||<span data-ttu-id="e79cd-159">**Bakåt**</span><span class="sxs-lookup"><span data-stu-id="e79cd-159">**Backward**</span></span>|<span data-ttu-id="e79cd-160">Planeringen börjar vid slutdatumet och fortsätter bakåt till startdatumet.</span><span class="sxs-lookup"><span data-stu-id="e79cd-160">Scheduling starts from the ending date and proceeds backward to the starting date.</span></span>|  
    |<span data-ttu-id="e79cd-161">**Beräkna**</span><span class="sxs-lookup"><span data-stu-id="e79cd-161">**Calculate**</span></span>|<span data-ttu-id="e79cd-162">**Rader**</span><span class="sxs-lookup"><span data-stu-id="e79cd-162">**Lines**</span></span>|<span data-ttu-id="e79cd-163">Markera det här fältet om du vill beräkna produktionsorderrader.</span><span class="sxs-lookup"><span data-stu-id="e79cd-163">Select this field to calculate the production order lines.</span></span>|  
    ||<span data-ttu-id="e79cd-164">**Operationsföljder**</span><span class="sxs-lookup"><span data-stu-id="e79cd-164">**Routings**</span></span>|<span data-ttu-id="e79cd-165">Det här fältet påverkar inte beräkningen av produktionsrader.</span><span class="sxs-lookup"><span data-stu-id="e79cd-165">This field has no influence on calculating the production lines.</span></span>|  
    ||<span data-ttu-id="e79cd-166">**Komponentbehov**</span><span class="sxs-lookup"><span data-stu-id="e79cd-166">**Component Need**</span></span>|<span data-ttu-id="e79cd-167">Det här fältet påverkar inte beräkningen av produktionsrader.</span><span class="sxs-lookup"><span data-stu-id="e79cd-167">This field has no influence on calculating the production lines.</span></span>|  
    |<span data-ttu-id="e79cd-168">**Dist.lager**</span><span class="sxs-lookup"><span data-stu-id="e79cd-168">**Warehouse**</span></span>|<span data-ttu-id="e79cd-169">**Skapa ingående rekvisition**</span><span class="sxs-lookup"><span data-stu-id="e79cd-169">**Create Inbound Request**</span></span>|<span data-ttu-id="e79cd-170">Det här fältet påverkar inte beräkningen av produktionsrader.</span><span class="sxs-lookup"><span data-stu-id="e79cd-170">This field has no influence on calculating the production lines.</span></span>|  

5. <span data-ttu-id="e79cd-171">Klicka på knappen **OK** för att bekräfta ditt val.</span><span class="sxs-lookup"><span data-stu-id="e79cd-171">Choose the **OK** button to confirm your selection.</span></span> <span data-ttu-id="e79cd-172">Nu har produktionsorderraderna beräknats.</span><span class="sxs-lookup"><span data-stu-id="e79cd-172">Now the production order lines are calculated.</span></span>

> [!NOTE]  
>  <span data-ttu-id="e79cd-173">När du beräknar produktionsorderkomponenter tas tidigare gjorda ändringar i komponenterna bort.</span><span class="sxs-lookup"><span data-stu-id="e79cd-173">Calculating production order components deletes previous changes in the components.</span></span>

## <a name="see-also"></a><span data-ttu-id="e79cd-174">Se även</span><span class="sxs-lookup"><span data-stu-id="e79cd-174">See Also</span></span>  
[<span data-ttu-id="e79cd-175">Planerad</span><span class="sxs-lookup"><span data-stu-id="e79cd-175">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="e79cd-176">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="e79cd-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e79cd-177">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e79cd-177">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="e79cd-178">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="e79cd-178">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e79cd-179">Inköp</span><span class="sxs-lookup"><span data-stu-id="e79cd-179">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e79cd-180">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e79cd-180">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="e79cd-181">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="e79cd-181">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="e79cd-182">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e79cd-182">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
