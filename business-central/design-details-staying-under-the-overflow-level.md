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
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2fc2ef2528a1edc85c0a7694c1afc5bec7a0065a
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="0dbf9-104">Designdetaljer: Hålla sig under överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="0dbf9-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="0dbf9-105">När du använder policyer för Maximalt antal och Fast orderkvantitet fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="0dbf9-106">Det betyder att planeringssystemet kan föreslå överflödig efterfrågan när negativ efterfrågan eller positiva tillförseländringar uppstår utanför den angivna tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="0dbf9-107">Om det av denna anledning föreslås en överflödig leverans, beräknar planeringssystemet vilket antal utleveransen ska minskar till (eller tas bort) för att undvika den överflödiga utleveransen.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="0dbf9-108">Denna mängd kallas ”Överflödesnivå”.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="0dbf9-109">Överflödet kommuniceras som en planeringsrad med åtgärden **Ändra antal (minska)** eller **Avbryta** eller Annullera och följande varningsmeddelande:</span><span class="sxs-lookup"><span data-stu-id="0dbf9-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="0dbf9-110">*Observera! Det planerade lagret [xx] är större än överflödesnivån [xx] på förfallodatumet [xx].*</span><span class="sxs-lookup"><span data-stu-id="0dbf9-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="0dbf9-111">![Lagrets överflödesnivå](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span><span class="sxs-lookup"><span data-stu-id="0dbf9-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="0dbf9-112">Beräknar överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="0dbf9-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="0dbf9-113">Överflödesnivån beräknas på olika sätt beroende på planeringsinställningen.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="0dbf9-114">Partiformningsmetoden Maximalt antal</span><span class="sxs-lookup"><span data-stu-id="0dbf9-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="0dbf9-115">Överflödesnivå = beställningsgräns</span><span class="sxs-lookup"><span data-stu-id="0dbf9-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dbf9-116">Om en lägsta partistorlek finns kommer den läggas till enligt följande: Överflödesnivå = maximalt lager + minsta partistorlek.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="0dbf9-117">Partiformningsmetoden Fast orderkvantitet</span><span class="sxs-lookup"><span data-stu-id="0dbf9-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="0dbf9-118">Överflödesnivå = Beställningsantal + beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="0dbf9-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dbf9-119">Om den minsta partistorleken är större än beställningspunkten, kommer den att ersätta enligt följande: Överflödesnivå= Beställningsantal + minsta partistorlek</span><span class="sxs-lookup"><span data-stu-id="0dbf9-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="0dbf9-120">Partistorleksmultipel</span><span class="sxs-lookup"><span data-stu-id="0dbf9-120">Order Multiple</span></span>  
<span data-ttu-id="0dbf9-121">Om en ordermultipel finns justerar den överflödesnivån för partiformningsmetoderna Maximalt antal och Orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="0dbf9-122">Skapa planeringsraden med överflödesvarning</span><span class="sxs-lookup"><span data-stu-id="0dbf9-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="0dbf9-123">När en befintlig leverans gör att det planerade lagret blir högre än överflödesnivån vid slutet av en tidsenhet, skapas en planeringsrad.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="0dbf9-124">För att varna för den potentiella överflödiga leveransen har planeringsraden ett varningsmeddelande, fältet **Acceptera åtgärdsmeddelande** markeras inte och åtgärdsmeddelandet är antingen Avbryt eller Ändra antal.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="0dbf9-125">Beräknar antal för planeringsraden</span><span class="sxs-lookup"><span data-stu-id="0dbf9-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="0dbf9-126">Planeringsradantal = antal för aktuell efterfrågan – (planerat lager – överflödesnivå)</span><span class="sxs-lookup"><span data-stu-id="0dbf9-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dbf9-127">Som med alla varningsrader ignoreras all största/minsta partistorlek eller partistorleksmultipel.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="0dbf9-128">Definiera typen av åtgärdsmeddelande</span><span class="sxs-lookup"><span data-stu-id="0dbf9-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="0dbf9-129">Om planeringsradantalet är större än 0 är åtgärdsmeddelandet Ändra antal</span><span class="sxs-lookup"><span data-stu-id="0dbf9-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="0dbf9-130">Om planeringsradantalet är lika med eller mindre än 0 är åtgärdsmeddelandet Avbryt</span><span class="sxs-lookup"><span data-stu-id="0dbf9-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="0dbf9-131">Skapar varningsmeddelandet</span><span class="sxs-lookup"><span data-stu-id="0dbf9-131">Composing the Warning Message</span></span>  
<span data-ttu-id="0dbf9-132">I händelse av överflöde visar fönstret **Ej spårade planeringselement** ett varningsmeddelande med följande information:</span><span class="sxs-lookup"><span data-stu-id="0dbf9-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="0dbf9-133">Den planerade lagernivån som utlöste varningen</span><span class="sxs-lookup"><span data-stu-id="0dbf9-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="0dbf9-134">Den beräknade överflödesnivån</span><span class="sxs-lookup"><span data-stu-id="0dbf9-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="0dbf9-135">Förfallodatumet för tillgångshändelsen.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-135">The due date of the supply event.</span></span>  

<span data-ttu-id="0dbf9-136">Exempel: "Det planerade lagret 120 är större än överflödesnivå 60 i 28-01-11”</span><span class="sxs-lookup"><span data-stu-id="0dbf9-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="0dbf9-137">Scenario</span><span class="sxs-lookup"><span data-stu-id="0dbf9-137">Scenario</span></span>  
<span data-ttu-id="0dbf9-138">I det här scenariot ändrar en kund en försäljningsorder från 70 till 40 stycken mellan två planeringskörningar.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="0dbf9-139">Överflödesfunktionen går in för att minska inköpet som föreslogs för den initiala försäljningsantalet.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="0dbf9-140">Inställningar för artiklar</span><span class="sxs-lookup"><span data-stu-id="0dbf9-140">Item setup</span></span>  

|<span data-ttu-id="0dbf9-141">Partiformningsmetod</span><span class="sxs-lookup"><span data-stu-id="0dbf9-141">Reordering Policy</span></span>|<span data-ttu-id="0dbf9-142">Maximalt antal</span><span class="sxs-lookup"><span data-stu-id="0dbf9-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="0dbf9-143">Max. partistorlek</span><span class="sxs-lookup"><span data-stu-id="0dbf9-143">Maximum Order Quantity</span></span>|<span data-ttu-id="0dbf9-144">100</span><span class="sxs-lookup"><span data-stu-id="0dbf9-144">100</span></span>|  
|<span data-ttu-id="0dbf9-145">Beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="0dbf9-145">Reorder Point</span></span>|<span data-ttu-id="0dbf9-146">50</span><span class="sxs-lookup"><span data-stu-id="0dbf9-146">50</span></span>|  
|<span data-ttu-id="0dbf9-147">Lager</span><span class="sxs-lookup"><span data-stu-id="0dbf9-147">Inventory</span></span>|<span data-ttu-id="0dbf9-148">80</span><span class="sxs-lookup"><span data-stu-id="0dbf9-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="0dbf9-149">Läge före försäljningsminskning</span><span class="sxs-lookup"><span data-stu-id="0dbf9-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="0dbf9-150">Händelse</span><span class="sxs-lookup"><span data-stu-id="0dbf9-150">Event</span></span>|<span data-ttu-id="0dbf9-151">Ändra antal</span><span class="sxs-lookup"><span data-stu-id="0dbf9-151">Change Qty.</span></span>|<span data-ttu-id="0dbf9-152">Planerat lager</span><span class="sxs-lookup"><span data-stu-id="0dbf9-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="0dbf9-153">Dag ett</span><span class="sxs-lookup"><span data-stu-id="0dbf9-153">Day one</span></span>|<span data-ttu-id="0dbf9-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="0dbf9-154">None</span></span>|<span data-ttu-id="0dbf9-155">80</span><span class="sxs-lookup"><span data-stu-id="0dbf9-155">80</span></span>|  
|<span data-ttu-id="0dbf9-156">Försäljning</span><span class="sxs-lookup"><span data-stu-id="0dbf9-156">Sale</span></span>|<span data-ttu-id="0dbf9-157">-70</span><span class="sxs-lookup"><span data-stu-id="0dbf9-157">-70</span></span>|<span data-ttu-id="0dbf9-158">10</span><span class="sxs-lookup"><span data-stu-id="0dbf9-158">10</span></span>|  
|<span data-ttu-id="0dbf9-159">Slut på tidsenheten</span><span class="sxs-lookup"><span data-stu-id="0dbf9-159">End of time bucket</span></span>|<span data-ttu-id="0dbf9-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="0dbf9-160">None</span></span>|<span data-ttu-id="0dbf9-161">10</span><span class="sxs-lookup"><span data-stu-id="0dbf9-161">10</span></span>|  
|<span data-ttu-id="0dbf9-162">Föreslå ny inköpsorder</span><span class="sxs-lookup"><span data-stu-id="0dbf9-162">Suggest new purchase order</span></span>|<span data-ttu-id="0dbf9-163">+90</span><span class="sxs-lookup"><span data-stu-id="0dbf9-163">+90</span></span>|<span data-ttu-id="0dbf9-164">100</span><span class="sxs-lookup"><span data-stu-id="0dbf9-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="0dbf9-165">Läge efter försäljningsminskning</span><span class="sxs-lookup"><span data-stu-id="0dbf9-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="0dbf9-166">Ändra</span><span class="sxs-lookup"><span data-stu-id="0dbf9-166">Change</span></span>|<span data-ttu-id="0dbf9-167">Ändra antal</span><span class="sxs-lookup"><span data-stu-id="0dbf9-167">Change Qty.</span></span>|<span data-ttu-id="0dbf9-168">Planerat lager</span><span class="sxs-lookup"><span data-stu-id="0dbf9-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="0dbf9-169">Dag ett</span><span class="sxs-lookup"><span data-stu-id="0dbf9-169">Day one</span></span>|<span data-ttu-id="0dbf9-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="0dbf9-170">None</span></span>|<span data-ttu-id="0dbf9-171">80</span><span class="sxs-lookup"><span data-stu-id="0dbf9-171">80</span></span>|  
|<span data-ttu-id="0dbf9-172">Försäljning</span><span class="sxs-lookup"><span data-stu-id="0dbf9-172">Sale</span></span>|<span data-ttu-id="0dbf9-173">-40</span><span class="sxs-lookup"><span data-stu-id="0dbf9-173">-40</span></span>|<span data-ttu-id="0dbf9-174">40</span><span class="sxs-lookup"><span data-stu-id="0dbf9-174">40</span></span>|  
|<span data-ttu-id="0dbf9-175">Inköp</span><span class="sxs-lookup"><span data-stu-id="0dbf9-175">Purchase</span></span>|<span data-ttu-id="0dbf9-176">+90</span><span class="sxs-lookup"><span data-stu-id="0dbf9-176">+90</span></span>|<span data-ttu-id="0dbf9-177">130</span><span class="sxs-lookup"><span data-stu-id="0dbf9-177">130</span></span>|  
|<span data-ttu-id="0dbf9-178">Slut på tidsenheten</span><span class="sxs-lookup"><span data-stu-id="0dbf9-178">End of time bucket</span></span>|<span data-ttu-id="0dbf9-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="0dbf9-179">None</span></span>|<span data-ttu-id="0dbf9-180">130</span><span class="sxs-lookup"><span data-stu-id="0dbf9-180">130</span></span>|  
|<span data-ttu-id="0dbf9-181">Föreslås för att minska inköpet</span><span class="sxs-lookup"><span data-stu-id="0dbf9-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="0dbf9-182">order från 90 till 60</span><span class="sxs-lookup"><span data-stu-id="0dbf9-182">order from 90 to 60</span></span>|<span data-ttu-id="0dbf9-183">-30</span><span class="sxs-lookup"><span data-stu-id="0dbf9-183">-30</span></span>|<span data-ttu-id="0dbf9-184">100</span><span class="sxs-lookup"><span data-stu-id="0dbf9-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="0dbf9-185">Uppdaterar planeringsrader</span><span class="sxs-lookup"><span data-stu-id="0dbf9-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="0dbf9-186">En planeringsrad (varning) skapas för att minska inköpet med 30 från 90 till 60 för att hålla det planerade lagret på 100 enligt överflödesnivån.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="0dbf9-187">![Planera enligt överflödesnivån](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span><span class="sxs-lookup"><span data-stu-id="0dbf9-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dbf9-188">Utan funktionen Överflöde skapas ingen varning om den planerade lagernivån är högre än beställningsgränsen.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="0dbf9-189">Det kan orsaka en överflödig leverans av 30.</span><span class="sxs-lookup"><span data-stu-id="0dbf9-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0dbf9-190">Se även</span><span class="sxs-lookup"><span data-stu-id="0dbf9-190">See Also</span></span>  
<span data-ttu-id="0dbf9-191">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0dbf9-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="0dbf9-192">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="0dbf9-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="0dbf9-193">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0dbf9-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="0dbf9-194">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="0dbf9-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
