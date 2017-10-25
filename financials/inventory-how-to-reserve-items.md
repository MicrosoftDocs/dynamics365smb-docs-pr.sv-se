---
title: "Så här reserverar du artiklar | Microsoft Docs"
description: "Du kan reservera artiklar för försäljningsorder, inköpsorder och produktionsorder. Du kan reservera artiklar i lager eller ankommande på öppna dokumentrader."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b03209b5681c264f7d788d3d731d32b60f1709b6
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reserve-items"></a><span data-ttu-id="0f394-104">Så här reserverar du artiklar</span><span class="sxs-lookup"><span data-stu-id="0f394-104">How to: Reserve Items</span></span>
<span data-ttu-id="0f394-105">Reservera artiklar för försäljningsorder, inköpsorder, serviceorder, monteringsorder eller produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-105">You can reserve items for sales orders, purchase orders, service orders, assembly orders, and production orders.</span></span> <span data-ttu-id="0f394-106">Du kan reservera artiklar i lager eller ankommande på öppna dokument eller journalrader.</span><span class="sxs-lookup"><span data-stu-id="0f394-106">You can reserve items on inventory or inbound on open document or journal lines.</span></span> <span data-ttu-id="0f394-107">Du utför arbetet i fönstret **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="0f394-107">You perform the work in the **Reservation** window.</span></span>

<span data-ttu-id="0f394-108">Varje rad i fönstret **Reservation** som du öppnar för att reservera artiklar visar information om en viss typ av rad (försäljning, inköp, journal) eller lagerpost.</span><span class="sxs-lookup"><span data-stu-id="0f394-108">Each line in the **Reservation** window, which you open to reserve items, displays information about one type of line (sales, purchase, journal) or inventory entry.</span></span> <span data-ttu-id="0f394-109">Raderna beskriver hur många artiklar som är disponibla för reservation för varje radtyp eller post.</span><span class="sxs-lookup"><span data-stu-id="0f394-109">The lines describe how many items are available to be reserved from each type of line or entry.</span></span>

## <a name="to-reserve-items-for-sales"></a><span data-ttu-id="0f394-110">Så här reserverar du artiklar för försäljning</span><span class="sxs-lookup"><span data-stu-id="0f394-110">To reserve items for sales</span></span>
<span data-ttu-id="0f394-111">Nedan beskrivs hur du reserverar artiklar från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-111">The following describes how to reserve items from a sales order.</span></span> <span data-ttu-id="0f394-112">Momentet är liknande för inköp, service och monteringsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-112">The steps are similar for purchase, service, and assembly orders.</span></span>  
1.  <span data-ttu-id="0f394-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0f394-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0f394-114">På en föräljningsorder, på snabbfliken **Rader** väljer du åtgärden **Reservera**.</span><span class="sxs-lookup"><span data-stu-id="0f394-114">On a sales order, on the **Lines** FastTab, choose the **Reserve** action.</span></span> <span data-ttu-id="0f394-115">Fönstret **Reservation** öppnas.</span><span class="sxs-lookup"><span data-stu-id="0f394-115">The **Reservation** window opens.</span></span>  
3. <span data-ttu-id="0f394-116">Välj den rad som du vill reservera artiklarna från.</span><span class="sxs-lookup"><span data-stu-id="0f394-116">Select the line that you want to reserve the items from.</span></span>  
4. <span data-ttu-id="0f394-117">Välj något av följande åtgärder:</span><span class="sxs-lookup"><span data-stu-id="0f394-117">Choose one of the following actions.</span></span>  

    |<span data-ttu-id="0f394-118">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0f394-118">**Function**</span></span>|<span data-ttu-id="0f394-119">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="0f394-119">**Description**</span></span>|
    |------------------|---------------------|  
    |<span data-ttu-id="0f394-120">**Reservera auto.**</span><span class="sxs-lookup"><span data-stu-id="0f394-120">**Auto Reserve**</span></span>|<span data-ttu-id="0f394-121">Om du vill reservera artiklar automatiskt i fönstret **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="0f394-121">To automatically reserve items in the **Reservation** window.</span></span>|  
    |<span data-ttu-id="0f394-122">**Reservera från aktuell rad**</span><span class="sxs-lookup"><span data-stu-id="0f394-122">**Reserve from Current Line**</span></span>|<span data-ttu-id="0f394-123">För reservering av artiklar från den rad du har markerat i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="0f394-123">To reserve the items from the document on the line you have selected.</span></span>|  
    |<span data-ttu-id="0f394-124">**Avbeställ reservation från aktuell rad**</span><span class="sxs-lookup"><span data-stu-id="0f394-124">**Cancel Reservation from Current Line**</span></span>|<span data-ttu-id="0f394-125">För att avbeställa reservation av artiklar från den rad du har markerat i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="0f394-125">To cancel reservation of the items from the document on the line you have selected.</span></span>|

> [!NOTE]  
>  <span data-ttu-id="0f394-126">Om artikelspårningsrader finns för försäljningsordern används en särskild procedur.</span><span class="sxs-lookup"><span data-stu-id="0f394-126">If item tracking lines exist for the sales order, the reservation system will take you through special steps.</span></span> <span data-ttu-id="0f394-127">Mer information finns i avsnittet "Att reservera ett specifikt parti- eller serienummer".</span><span class="sxs-lookup"><span data-stu-id="0f394-127">For more information, see the "To reserve a specific serial or lot number" section.</span></span>  

## <a name="to-reserve-an-item-for-a-production-order-line"></a><span data-ttu-id="0f394-128">Så här reserverar du artiklar för produktionsorderrader</span><span class="sxs-lookup"><span data-stu-id="0f394-128">To reserve an item for a production order line</span></span>  
<span data-ttu-id="0f394-129">Om du vill kan du reservera artiklar för produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-129">You can reserve items for production orders.</span></span> <span data-ttu-id="0f394-130">Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.</span><span class="sxs-lookup"><span data-stu-id="0f394-130">You have to distinguish between production order lines, meaning the parent item, and production order components.</span></span>

<span data-ttu-id="0f394-131">I det följande procedur används en fast planerad produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-131">In the following procedure, a firm planned production order is used.</span></span>   
1. <span data-ttu-id="0f394-132">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0f394-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0f394-133">Öppna den fast planerade produktionsorder som du vill reservera överordnade artiklar för.</span><span class="sxs-lookup"><span data-stu-id="0f394-133">Open the firm planned production order you want to reserve parent items for.</span></span>  
3. <span data-ttu-id="0f394-134">Markera relevant produktionsorderrad.</span><span class="sxs-lookup"><span data-stu-id="0f394-134">Select the relevant production order line.</span></span>  
4. <span data-ttu-id="0f394-135">På snabbfliken **rader** i fältet **Reservera.**</span><span class="sxs-lookup"><span data-stu-id="0f394-135">On the **Lines** FastTab, choose the **Reserve** action.</span></span>
5. <span data-ttu-id="0f394-136">I fönstret **Reservation** väljer du raden **Försäljningsrad, Order** och sedan åtgärden **Reservera från aktuell rad**.</span><span class="sxs-lookup"><span data-stu-id="0f394-136">In the **Reservation** window, select the **Sales Line, Order** line, and then choose the **Reserve from Current Line** action.</span></span>  

<span data-ttu-id="0f394-137">Det antal som du angett på raden för den fast planerade produktionsorden har nu reserverats.</span><span class="sxs-lookup"><span data-stu-id="0f394-137">The quantity you entered in the firm planned production order line is now reserved.</span></span>

## <a name="to-reserve-items-for-production-order-components"></a><span data-ttu-id="0f394-138">Så här reserverar du artiklar för produktionsorderkomponenter</span><span class="sxs-lookup"><span data-stu-id="0f394-138">To reserve items for production order components</span></span>  
<span data-ttu-id="0f394-139">Om du vill kan du reservera artiklar för produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-139">You can reserve items for production orders.</span></span> <span data-ttu-id="0f394-140">Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.</span><span class="sxs-lookup"><span data-stu-id="0f394-140">You have to distinguish between production order lines, meaning the parent item, and production order components.</span></span>

<span data-ttu-id="0f394-141">I det följande procedur används en fast planerad produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-141">In the following procedure, a firm planned production order is used.</span></span>    
1. <span data-ttu-id="0f394-142">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0f394-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0f394-143">Öppna den fast planerade produktionsorder som du vill reservera komponentartiklar för.</span><span class="sxs-lookup"><span data-stu-id="0f394-143">Open the firm planned production order you want to reserve component items for.</span></span>  
3. <span data-ttu-id="0f394-144">Markera relevant produktionsorderrad.</span><span class="sxs-lookup"><span data-stu-id="0f394-144">Select the relevant production order line.</span></span>  
4. <span data-ttu-id="0f394-145">Välj **Rad**och sedan **Koppla trans.** på snabbfliken **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="0f394-145">On the **Lines** FastTab, choose **Line**, and then choose **Components**.</span></span>  
5. <span data-ttu-id="0f394-146">Välj relevant komponentrad.</span><span class="sxs-lookup"><span data-stu-id="0f394-146">Select the relevant component line.</span></span>  
6. <span data-ttu-id="0f394-147">På snabbfliken **rader** i fältet **Reservera.**</span><span class="sxs-lookup"><span data-stu-id="0f394-147">Choose On the **Lines** FastTab, choose the **Reserve** action.</span></span>  
7. <span data-ttu-id="0f394-148">I fönstret **Reservation** väljer du raden **Reservera från aktuell rad**.</span><span class="sxs-lookup"><span data-stu-id="0f394-148">In the **Reservation** window, select a line, and then choose the **Reserve from Current Line** action.</span></span>  

<span data-ttu-id="0f394-149">Det antal som du angett på raden för den fast planerade produktionskomponentraden har nu reserverats.</span><span class="sxs-lookup"><span data-stu-id="0f394-149">The quantity you entered in the firm planned production component line is now reserved.</span></span>

## <a name="to-change-a-reservation"></a><span data-ttu-id="0f394-150">Så här ändrar du en reservation</span><span class="sxs-lookup"><span data-stu-id="0f394-150">To change a reservation</span></span>  
<span data-ttu-id="0f394-151">Någon gång kan du behöva ändra en artikelreservation.</span><span class="sxs-lookup"><span data-stu-id="0f394-151">Sometimes, you may want to change an item reservation.</span></span>   
1. <span data-ttu-id="0f394-152">Från dokumentraden som du har reserverats från snabbfliken **rader** väljer du åtgärden **reservera**.</span><span class="sxs-lookup"><span data-stu-id="0f394-152">From the document line that you have reserved from, on the **Lines** FastTab, choose the **Reserve** action.</span></span>  
2. <span data-ttu-id="0f394-153">I fönstret **Reservation** väljer du åtgärden **Reservationstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="0f394-153">In the **Reservation** window, choose the **Reservation Entries** action.</span></span>
3. <span data-ttu-id="0f394-154">Fönstret **Reservationstransaktioner** uppdaterar fältet **antal** på den rad som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="0f394-154">The **Reservation Entries** window, update the **Quantity** field on the line you want to change.</span></span>
4. <span data-ttu-id="0f394-155">Bekräfta meddelandet som visas, genom att välja **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="0f394-155">Confirm the subsequent message, by choosing the **OK** button.</span></span>

## <a name="to-cancel-a-reservation"></a><span data-ttu-id="0f394-156">Så här avbeställer du en reservation</span><span class="sxs-lookup"><span data-stu-id="0f394-156">To cancel a reservation</span></span>  
<span data-ttu-id="0f394-157">Någon gång kan du behöva avbeställa en artikelreservation.</span><span class="sxs-lookup"><span data-stu-id="0f394-157">Sometimes, you may want to cancel an item reservation.</span></span>   
1. <span data-ttu-id="0f394-158">Från dokumentraden som du vill avbryta en reservervation från på snabbfliken **rader** väljer du åtgärden **reservera**.</span><span class="sxs-lookup"><span data-stu-id="0f394-158">From the document line that you want to cancel a reservation from, on the **Lines** FastTab, choose the **Reserve** action.</span></span>  
2. <span data-ttu-id="0f394-159">I fönstret **Reservation** väljer du åtgärden **Reservationstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="0f394-159">In the **Reservation** window, choose **Reservation Entries** action.</span></span>  
3.  <span data-ttu-id="0f394-160">I fönstret **Reservationstransaktioner** väljer du åtgärden **Avbryt reservation**.</span><span class="sxs-lookup"><span data-stu-id="0f394-160">In the **Reservation Entries** window, choose the **Cancel Reservation** action.</span></span>  
4.  <span data-ttu-id="0f394-161">Bekräfta meddelandet som visas, genom att välja **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="0f394-161">Confirm the subsequent message, by choosing the **OK** button.</span></span>  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a><span data-ttu-id="0f394-162">Om du vill reservera ett visst serie- eller partinummer</span><span class="sxs-lookup"><span data-stu-id="0f394-162">To reserve a specific serial or lot number</span></span>  
<span data-ttu-id="0f394-163">Från utgående dokument för spårade artiklar t.ex. försäljningsorder eller produktionskomponentlistor kan du reservera specifika serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="0f394-163">From outbound documents for item-tracked items, such as sales orders or production component lists, you can reserve specific serial or lot numbers.</span></span> <span data-ttu-id="0f394-164">Detta kan vara användbart till exempel om du behöver produktionskomponenter från ett visst parti för att kontrollera överensstämmelse med tidigare produktionsbatcher eller därför att en kund har begärt ett specifikt serienummer.</span><span class="sxs-lookup"><span data-stu-id="0f394-164">This may be relevant, for example, if you need production components from a specific lot to ensure consistency with earlier production batches, or because a customer has requested a specific serial number.</span></span> <span data-ttu-id="0f394-165">Mer information finns i [Så här arbetar du med serienummer och partinummer](inventory-how-work-item-tracking.md).</span><span class="sxs-lookup"><span data-stu-id="0f394-165">For more information, see [How to: Work with Serial and Lot Numbers](inventory-how-work-item-tracking.md).</span></span>

<span data-ttu-id="0f394-166">Detta kallas för en specifik reservation, eftersom du reserverar från antalet av artikeln X som tillhör parti X. Om du enbart reserverar från antal av artikeln X, är det en helt vanlig, icke-specifik reservation.</span><span class="sxs-lookup"><span data-stu-id="0f394-166">This is referred to as a specific reservation, because you reserve from the quantity of  Item X that belongs to Lot X. If you simply reserve from quantities of Item X, then it is a normal, non-specific, reservation.</span></span> <span data-ttu-id="0f394-167">Mer information finns i  [Designdetaljer: Artikelspårning och reservationer](design-details-item-tracking-and-reservations.md).</span><span class="sxs-lookup"><span data-stu-id="0f394-167">For more information, see [Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md).</span></span>

<span data-ttu-id="0f394-168">Följande procedur är baserad på en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="0f394-168">The following procedure is based on a sales order.</span></span>    
1. <span data-ttu-id="0f394-169">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0f394-169">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then select the related link.</span></span>  
2. <span data-ttu-id="0f394-170">Skapa försäljningsorderrader för en artikelspårad artikel.</span><span class="sxs-lookup"><span data-stu-id="0f394-170">Create a sales order line for an item-tracked item.</span></span>  
3. <span data-ttu-id="0f394-171">Fortsätt med att tilldela serie- och partinummer på försäljningsorderraden.</span><span class="sxs-lookup"><span data-stu-id="0f394-171">Assign serial and lot numbers to the sales order line.</span></span> <span data-ttu-id="0f394-172">Mer information finns i [Så här arbetar du med serienummer och partinummer](inventory-how-work-item-tracking.md).</span><span class="sxs-lookup"><span data-stu-id="0f394-172">For more information, see [How to: Work with Serial and Lot Numbers](inventory-how-work-item-tracking.md).</span></span>
4. <span data-ttu-id="0f394-173">På försäljningsorderraden väljer du åtgärden **Reservera**.</span><span class="sxs-lookup"><span data-stu-id="0f394-173">On the sales order line, choose the **Reserve** action.</span></span>  
5. <span data-ttu-id="0f394-174">Välj knappen **Ja** för att reservera specifika serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="0f394-174">Choose the **Yes** button to reserve specific serial or lot numbers.</span></span>  
6. <span data-ttu-id="0f394-175">I fönstret **Artikelspårningslista**, välj serie- och partinummerkombinationen som du precis har tilldelats.</span><span class="sxs-lookup"><span data-stu-id="0f394-175">In the   **Item Tracking List** window, select the serial and lot number combination that you have just assigned.</span></span>  
7. <span data-ttu-id="0f394-176">Välj knappen **OK** för att öppna fönstret **Reservation** där endast lager med det angivna artikelspårningsnumret visas.</span><span class="sxs-lookup"><span data-stu-id="0f394-176">Choose the **OK** button to open the **Reservation** window showing only supply with the specified item tracking number.</span></span> <span data-ttu-id="0f394-177">Om det finns icke-specifika reservationer för något av artikelspårningsnumren som har angetts på den här raden, informeras du om den kvantitet som redan har reserverats.</span><span class="sxs-lookup"><span data-stu-id="0f394-177">If there are any non-specific reservations on any of the item tracking numbers that you have specified for this line, you are informed of the quantity that has already been reserved.</span></span>  
8. <span data-ttu-id="0f394-178">Välj antingen **Reservera auto** eller åtgärden **Reservera från aktuell rad** för att skapa reservationen med de specifika artikelspårningsnumren.</span><span class="sxs-lookup"><span data-stu-id="0f394-178">Choose either the **Auto Reserve** or the **Reserve from Current Line** action to create the reservation on the specific item tracking numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f394-179">Se även</span><span class="sxs-lookup"><span data-stu-id="0f394-179">See Also</span></span>
[<span data-ttu-id="0f394-180">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="0f394-180">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0f394-181">Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden</span><span class="sxs-lookup"><span data-stu-id="0f394-181">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="0f394-182">Designdetaljer: Artikelspårning och reservationer</span><span class="sxs-lookup"><span data-stu-id="0f394-182">Design Details - Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="0f394-183">Så här arbetar du med serienummer och partinummer</span><span class="sxs-lookup"><span data-stu-id="0f394-183">How to: Work with Serial and Lot Numbers</span></span>](inventory-how-work-item-tracking.md)  
<span data-ttu-id="0f394-184">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0f394-184">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
