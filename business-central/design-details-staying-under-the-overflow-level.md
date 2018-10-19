---
title: "Designdetaljer - Hålla sig under överflödesnivån | Microsoft Docs"
description: "När du använder Maximalt antal och Fast orderkvantitet fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten. Det betyder att planeringssystemet kan föreslå överflödig efterfrågan när negativ efterfrågan eller positiva tillförseländringar uppstår utanför den angivna tidsenheten."
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
ms.openlocfilehash: e532893b1823ef84256403fb7bf5ef9fabd59f2e
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="937ae-104">Designdetaljer: Hålla sig under överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="937ae-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="937ae-105">När du använder policyer för Maximalt antal och Fast orderkvantitet fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="937ae-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="937ae-106">Det betyder att planeringssystemet kan föreslå överflödig efterfrågan när negativ efterfrågan eller positiva tillförseländringar uppstår utanför den angivna tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="937ae-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="937ae-107">Om det av denna anledning föreslås en överflödig leverans, beräknar planeringssystemet vilket antal utleveransen ska minskar till (eller tas bort) för att undvika den överflödiga utleveransen.</span><span class="sxs-lookup"><span data-stu-id="937ae-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="937ae-108">Denna mängd kallas ”Överflödesnivå”.</span><span class="sxs-lookup"><span data-stu-id="937ae-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="937ae-109">Överflödet kommuniceras som en planeringsrad med åtgärden **Ändra antal (minska)** eller **Avbryta** eller Annullera och följande varningsmeddelande:</span><span class="sxs-lookup"><span data-stu-id="937ae-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="937ae-110">*Observera! Det planerade lagret [xx] är större än överflödesnivån [xx] på förfallodatumet [xx].*</span><span class="sxs-lookup"><span data-stu-id="937ae-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="937ae-111">![Lagrets överflödesnivå](media/supplyplanning_2_overflow1_new.png "Lagrets överflödesnivå")</span><span class="sxs-lookup"><span data-stu-id="937ae-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "Inventory overflow level")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="937ae-112">Beräknar överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="937ae-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="937ae-113">Överflödesnivån beräknas på olika sätt beroende på planeringsinställningen.</span><span class="sxs-lookup"><span data-stu-id="937ae-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="937ae-114">Partiformningsmetoden Maximalt antal</span><span class="sxs-lookup"><span data-stu-id="937ae-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="937ae-115">Överflödesnivå = beställningsgräns</span><span class="sxs-lookup"><span data-stu-id="937ae-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="937ae-116">Om en lägsta partistorlek finns kommer den läggas till enligt följande: Överflödesnivå = maximalt lager + minsta partistorlek.</span><span class="sxs-lookup"><span data-stu-id="937ae-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="937ae-117">Partiformningsmetoden Fast orderkvantitet</span><span class="sxs-lookup"><span data-stu-id="937ae-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="937ae-118">Överflödesnivå = Beställningsantal + beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="937ae-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="937ae-119">Om den minsta partistorleken är större än beställningspunkten, kommer den att ersätta enligt följande: Överflödesnivå= Beställningsantal + minsta partistorlek</span><span class="sxs-lookup"><span data-stu-id="937ae-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="937ae-120">Partistorleksmultipel</span><span class="sxs-lookup"><span data-stu-id="937ae-120">Order Multiple</span></span>  
<span data-ttu-id="937ae-121">Om en ordermultipel finns justerar den överflödesnivån för partiformningsmetoderna Maximalt antal och Orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="937ae-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="937ae-122">Skapa planeringsraden med överflödesvarning</span><span class="sxs-lookup"><span data-stu-id="937ae-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="937ae-123">När en befintlig leverans gör att det planerade lagret blir högre än överflödesnivån vid slutet av en tidsenhet, skapas en planeringsrad.</span><span class="sxs-lookup"><span data-stu-id="937ae-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="937ae-124">För att varna för den potentiella överflödiga leveransen har planeringsraden ett varningsmeddelande, fältet **Acceptera åtgärdsmeddelande** markeras inte och åtgärdsmeddelandet är antingen Avbryt eller Ändra antal.</span><span class="sxs-lookup"><span data-stu-id="937ae-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="937ae-125">Beräknar antal för planeringsraden</span><span class="sxs-lookup"><span data-stu-id="937ae-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="937ae-126">Planeringsradantal = antal för aktuell efterfrågan – (planerat lager – överflödesnivå)</span><span class="sxs-lookup"><span data-stu-id="937ae-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="937ae-127">Som med alla varningsrader ignoreras all största/minsta partistorlek eller partistorleksmultipel.</span><span class="sxs-lookup"><span data-stu-id="937ae-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="937ae-128">Definiera typen av åtgärdsmeddelande</span><span class="sxs-lookup"><span data-stu-id="937ae-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="937ae-129">Om planeringsradantalet är större än 0 är åtgärdsmeddelandet Ändra antal</span><span class="sxs-lookup"><span data-stu-id="937ae-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="937ae-130">Om planeringsradantalet är lika med eller mindre än 0 är åtgärdsmeddelandet Avbryt</span><span class="sxs-lookup"><span data-stu-id="937ae-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="937ae-131">Skapar varningsmeddelandet</span><span class="sxs-lookup"><span data-stu-id="937ae-131">Composing the Warning Message</span></span>  
<span data-ttu-id="937ae-132">I händelse av överflöde visar fönstret **Ej spårade planeringselement** ett varningsmeddelande med följande information:</span><span class="sxs-lookup"><span data-stu-id="937ae-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="937ae-133">Den planerade lagernivån som utlöste varningen</span><span class="sxs-lookup"><span data-stu-id="937ae-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="937ae-134">Den beräknade överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="937ae-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="937ae-135">Förfallodatumet för tillgångshändelsen.</span><span class="sxs-lookup"><span data-stu-id="937ae-135">The due date of the supply event.</span></span>  

<span data-ttu-id="937ae-136">Exempel: "Det planerade lagret 120 är större än överflödesnivå 60 i 28-01-11”</span><span class="sxs-lookup"><span data-stu-id="937ae-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="937ae-137">Scenario</span><span class="sxs-lookup"><span data-stu-id="937ae-137">Scenario</span></span>  
<span data-ttu-id="937ae-138">I det här scenariot ändrar en kund en försäljningsorder från 70 till 40 stycken mellan två planeringskörningar.</span><span class="sxs-lookup"><span data-stu-id="937ae-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="937ae-139">Överflödesfunktionen går in för att minska inköpet som föreslogs för den initiala försäljningsantalet.</span><span class="sxs-lookup"><span data-stu-id="937ae-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="937ae-140">Inställningar för artiklar</span><span class="sxs-lookup"><span data-stu-id="937ae-140">Item setup</span></span>  

|<span data-ttu-id="937ae-141">Partiformningsmetod</span><span class="sxs-lookup"><span data-stu-id="937ae-141">Reordering Policy</span></span>|<span data-ttu-id="937ae-142">Maximalt antal</span><span class="sxs-lookup"><span data-stu-id="937ae-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="937ae-143">Max. partistorlek</span><span class="sxs-lookup"><span data-stu-id="937ae-143">Maximum Order Quantity</span></span>|<span data-ttu-id="937ae-144">100</span><span class="sxs-lookup"><span data-stu-id="937ae-144">100</span></span>|  
|<span data-ttu-id="937ae-145">Beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="937ae-145">Reorder Point</span></span>|<span data-ttu-id="937ae-146">50</span><span class="sxs-lookup"><span data-stu-id="937ae-146">50</span></span>|  
|<span data-ttu-id="937ae-147">Lager</span><span class="sxs-lookup"><span data-stu-id="937ae-147">Inventory</span></span>|<span data-ttu-id="937ae-148">80</span><span class="sxs-lookup"><span data-stu-id="937ae-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="937ae-149">Läge före försäljningsminskning</span><span class="sxs-lookup"><span data-stu-id="937ae-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="937ae-150">Händelse</span><span class="sxs-lookup"><span data-stu-id="937ae-150">Event</span></span>|<span data-ttu-id="937ae-151">Ändra antal</span><span class="sxs-lookup"><span data-stu-id="937ae-151">Change Qty.</span></span>|<span data-ttu-id="937ae-152">Planerat lager</span><span class="sxs-lookup"><span data-stu-id="937ae-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="937ae-153">Dag ett</span><span class="sxs-lookup"><span data-stu-id="937ae-153">Day one</span></span>|<span data-ttu-id="937ae-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="937ae-154">None</span></span>|<span data-ttu-id="937ae-155">80</span><span class="sxs-lookup"><span data-stu-id="937ae-155">80</span></span>|  
|<span data-ttu-id="937ae-156">Försäljning</span><span class="sxs-lookup"><span data-stu-id="937ae-156">Sale</span></span>|<span data-ttu-id="937ae-157">-70</span><span class="sxs-lookup"><span data-stu-id="937ae-157">-70</span></span>|<span data-ttu-id="937ae-158">10</span><span class="sxs-lookup"><span data-stu-id="937ae-158">10</span></span>|  
|<span data-ttu-id="937ae-159">Slut på tidsenheten</span><span class="sxs-lookup"><span data-stu-id="937ae-159">End of time bucket</span></span>|<span data-ttu-id="937ae-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="937ae-160">None</span></span>|<span data-ttu-id="937ae-161">10</span><span class="sxs-lookup"><span data-stu-id="937ae-161">10</span></span>|  
|<span data-ttu-id="937ae-162">Föreslå ny inköpsorder</span><span class="sxs-lookup"><span data-stu-id="937ae-162">Suggest new purchase order</span></span>|<span data-ttu-id="937ae-163">+90</span><span class="sxs-lookup"><span data-stu-id="937ae-163">+90</span></span>|<span data-ttu-id="937ae-164">100</span><span class="sxs-lookup"><span data-stu-id="937ae-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="937ae-165">Läge efter försäljningsminskning</span><span class="sxs-lookup"><span data-stu-id="937ae-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="937ae-166">Ändra</span><span class="sxs-lookup"><span data-stu-id="937ae-166">Change</span></span>|<span data-ttu-id="937ae-167">Ändra antal</span><span class="sxs-lookup"><span data-stu-id="937ae-167">Change Qty.</span></span>|<span data-ttu-id="937ae-168">Planerat lager</span><span class="sxs-lookup"><span data-stu-id="937ae-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="937ae-169">Dag ett</span><span class="sxs-lookup"><span data-stu-id="937ae-169">Day one</span></span>|<span data-ttu-id="937ae-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="937ae-170">None</span></span>|<span data-ttu-id="937ae-171">80</span><span class="sxs-lookup"><span data-stu-id="937ae-171">80</span></span>|  
|<span data-ttu-id="937ae-172">Försäljning</span><span class="sxs-lookup"><span data-stu-id="937ae-172">Sale</span></span>|<span data-ttu-id="937ae-173">-40</span><span class="sxs-lookup"><span data-stu-id="937ae-173">-40</span></span>|<span data-ttu-id="937ae-174">40</span><span class="sxs-lookup"><span data-stu-id="937ae-174">40</span></span>|  
|<span data-ttu-id="937ae-175">Inköp</span><span class="sxs-lookup"><span data-stu-id="937ae-175">Purchase</span></span>|<span data-ttu-id="937ae-176">+90</span><span class="sxs-lookup"><span data-stu-id="937ae-176">+90</span></span>|<span data-ttu-id="937ae-177">130</span><span class="sxs-lookup"><span data-stu-id="937ae-177">130</span></span>|  
|<span data-ttu-id="937ae-178">Slut på tidsenheten</span><span class="sxs-lookup"><span data-stu-id="937ae-178">End of time bucket</span></span>|<span data-ttu-id="937ae-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="937ae-179">None</span></span>|<span data-ttu-id="937ae-180">130</span><span class="sxs-lookup"><span data-stu-id="937ae-180">130</span></span>|  
|<span data-ttu-id="937ae-181">Föreslås för att minska inköpet</span><span class="sxs-lookup"><span data-stu-id="937ae-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="937ae-182">order från 90 till 60</span><span class="sxs-lookup"><span data-stu-id="937ae-182">order from 90 to 60</span></span>|<span data-ttu-id="937ae-183">-30</span><span class="sxs-lookup"><span data-stu-id="937ae-183">-30</span></span>|<span data-ttu-id="937ae-184">100</span><span class="sxs-lookup"><span data-stu-id="937ae-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="937ae-185">Uppdaterar planeringsrader</span><span class="sxs-lookup"><span data-stu-id="937ae-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="937ae-186">En planeringsrad (varning) skapas för att minska inköpet med 30 från 90 till 60 för att hålla det planerade lagret på 100 enligt överflödesnivån.</span><span class="sxs-lookup"><span data-stu-id="937ae-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="937ae-187">![Planera enligt avvikelsenivån](media/nav_app_supply_planning_2_overflow2.png "Planera enligt avvikelsenivån")</span><span class="sxs-lookup"><span data-stu-id="937ae-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "Plan according to overflow level")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="937ae-188">Utan funktionen Överflöde skapas ingen varning om den planerade lagernivån är högre än beställningsgränsen.</span><span class="sxs-lookup"><span data-stu-id="937ae-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="937ae-189">Det kan orsaka en överflödig leverans av 30.</span><span class="sxs-lookup"><span data-stu-id="937ae-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="937ae-190">Se även</span><span class="sxs-lookup"><span data-stu-id="937ae-190">See Also</span></span>  
<span data-ttu-id="937ae-191">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="937ae-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="937ae-192">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="937ae-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="937ae-193">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="937ae-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="937ae-194">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="937ae-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

