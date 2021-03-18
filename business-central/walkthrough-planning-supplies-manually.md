---
title: Genomgång – Planera leveranser manuellt | Microsoft Docs
description: Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan. Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 604a783f292b04c2609b8415d6b2ec6287f5cfcb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379808"
---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="10c89-104">Genomgång: Planera leveranser manuellt</span><span class="sxs-lookup"><span data-stu-id="10c89-104">Walkthrough: Planning Supplies Manually</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

<span data-ttu-id="10c89-105">Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="10c89-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="10c89-106">Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="10c89-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="10c89-107">I den här genomgången använder du sidan **Orderplanering**, som är ett enkelt leveransplaneringsverktyg som bygger på manuellt beslutsfattande snarare än parameterbaserad automatisk planering.</span><span class="sxs-lookup"><span data-stu-id="10c89-107">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="10c89-108">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="10c89-108">About This Walkthrough</span></span>  
 <span data-ttu-id="10c89-109">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="10c89-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="10c89-110">Planera en inköpsorder för komponenter till produktionen.</span><span class="sxs-lookup"><span data-stu-id="10c89-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="10c89-111">Planera en överföringsorder för att uppfylla försäljningsbehov.</span><span class="sxs-lookup"><span data-stu-id="10c89-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="10c89-112">Planera en produktionsorder för en artikel med flera nivåer.</span><span class="sxs-lookup"><span data-stu-id="10c89-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="10c89-113">Roller</span><span class="sxs-lookup"><span data-stu-id="10c89-113">Roles</span></span>  
 <span data-ttu-id="10c89-114">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="10c89-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="10c89-115">Produktionsplanerare</span><span class="sxs-lookup"><span data-stu-id="10c89-115">Production Planner</span></span>  
-   <span data-ttu-id="10c89-116">Inköpsagent</span><span class="sxs-lookup"><span data-stu-id="10c89-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="10c89-117">Försäljningsorderhandläggare</span><span class="sxs-lookup"><span data-stu-id="10c89-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="10c89-118">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="10c89-118">Prerequisites</span></span>  
 <span data-ttu-id="10c89-119">Innan du påbörjar genomgången måste du installera [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="10c89-119">Before you begin this walkthrough, you must install the [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="10c89-120">Följande ändringar måste göras i databasen:</span><span class="sxs-lookup"><span data-stu-id="10c89-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="10c89-121">Ta bort alla befintliga försäljningsorder på cyklar.</span><span class="sxs-lookup"><span data-stu-id="10c89-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="10c89-122">Skapa en försäljningsorder för tio cyklar på lagerstället ÖST.</span><span class="sxs-lookup"><span data-stu-id="10c89-122">Create one sales order for 10 bicycles at EAST location.</span></span>  
-   <span data-ttu-id="10c89-123">Ta bort alla planerade och fast planerade produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="10c89-124">Ta inte bort påbörjade order med transaktioner som redan har bokförts.</span><span class="sxs-lookup"><span data-stu-id="10c89-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="10c89-125">En regel är att de data som föreslås i genomgången ska användas eftersom dessa data har alla nödvändiga poster.</span><span class="sxs-lookup"><span data-stu-id="10c89-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="10c89-126">Situation</span><span class="sxs-lookup"><span data-stu-id="10c89-126">Story</span></span>  
 <span data-ttu-id="10c89-127">Eduardo är produktionsplanerare på ett litet tillverkande företag och håller på att planera produktions- och inköpsorder för att uppfylla behov.</span><span class="sxs-lookup"><span data-stu-id="10c89-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="10c89-128">Eftersom produkternas produktstrukturer har få nivåer och orderflödet är relativt lågt använder Eduardo sidan **Orderplanering** för att manuellt skapa leveransorder, en produktnivå i taget.</span><span class="sxs-lookup"><span data-stu-id="10c89-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="10c89-129">I en mer komplex produktionsmiljö används planeringsförslaget för att planera leveranser baserat på parametrar som omplaneringsperiod, säkerhetsledtid, beställningspunkt och batch-beräkningar av den sammanställda efterfrågan på alla produktnivåer.</span><span class="sxs-lookup"><span data-stu-id="10c89-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="10c89-130">Ställa in exempeldata</span><span class="sxs-lookup"><span data-stu-id="10c89-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="10c89-131">Standarddemonstrationsföretaget CRONUS har för närvarande en stor mängd oplanerad efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="10c89-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="10c89-132">Under de olika planeringsaktiviteterna i den här genomgången måste du avvika från det realistiska verksamhetsflödet genom att ignorera efterfrågan med tidiga förfallodatum och i stället använda efterfrågan med senare förfallodatum.</span><span class="sxs-lookup"><span data-stu-id="10c89-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="10c89-133">Använda sidan Orderplanering</span><span class="sxs-lookup"><span data-stu-id="10c89-133">Using the Order Planning Page</span></span>  

<span data-ttu-id="10c89-134">Du kommer åt sidan **Orderplanering** från flera olika platser:</span><span class="sxs-lookup"><span data-stu-id="10c89-134">The **Order Planning** page can be accessed from several different locations:</span></span>  

-   <span data-ttu-id="10c89-135">Produktion, Planering</span><span class="sxs-lookup"><span data-stu-id="10c89-135">Manufacturing, Planning</span></span>  
-   <span data-ttu-id="10c89-136">Försäljning och marknadsföring, Orderbearbetning</span><span class="sxs-lookup"><span data-stu-id="10c89-136">Sales & Marketing, Order Processing</span></span>  
-   <span data-ttu-id="10c89-137">Inköp, Planering</span><span class="sxs-lookup"><span data-stu-id="10c89-137">Purchase, Planning</span></span>  
-   <span data-ttu-id="10c89-138">Du kan dessutom öppna den här sidan för en viss produktionsorder genom att välja åtgärden **Planering**.</span><span class="sxs-lookup"><span data-stu-id="10c89-138">In addition, you can open this page for a specific production order by choosing the **Planning** action.</span></span>

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="10c89-139">Så här använder du sidan Orderplanering</span><span class="sxs-lookup"><span data-stu-id="10c89-139">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="10c89-140">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Orderplanering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="10c89-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="10c89-141">När sidan **Orderplanering** har öppnats måste en plan beräknas för att visa den nya efterfrågan sedan den senaste beräkningen.</span><span class="sxs-lookup"><span data-stu-id="10c89-141">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="10c89-142">Välj åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="10c89-142">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="10c89-143">Planeringssystemet analyserar alla ny behov som har tillkommit, exempelvis ny försäljning, förändrad försäljning och produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-143">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="10c89-144">Den kvantitet som behövs för respektive efterfrågerad beräknas utifrån den totala tillgången.</span><span class="sxs-lookup"><span data-stu-id="10c89-144">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="10c89-145">Beräkningen görs per order.</span><span class="sxs-lookup"><span data-stu-id="10c89-145">This calculation is performed order-by-order.</span></span> <span data-ttu-id="10c89-146">Det betyder att den order som innehåller efterfrågan med det tidigaste förfallodatumet eller utleveransdatumet beräknas först.</span><span class="sxs-lookup"><span data-stu-id="10c89-146">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="10c89-147">Därefter beräknas ytterligare efterfrågerader i samma ordning, oavsett förfallodatum eller utleveransdatum.</span><span class="sxs-lookup"><span data-stu-id="10c89-147">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="10c89-148">Se till att sidan **Orderplanering** är maximerad och att kolumnfälten har lagom storlek för att alla standardfältnamn ska synas.</span><span class="sxs-lookup"><span data-stu-id="10c89-148">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="10c89-149">När beräkningen är slutförd visas alla ej uppfyllda behov i sidan som reducerade orderrader sorterade efter behovsdatum.</span><span class="sxs-lookup"><span data-stu-id="10c89-149">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="10c89-150">Lägg märke till att CRONUS har flera order med ej uppfyllda behov.</span><span class="sxs-lookup"><span data-stu-id="10c89-150">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="10c89-151">Varje planeringsrad i fetstil motsvarar en order, försäljningsorder eller produktionsorder, inklusive minst en orderrad med otillräcklig tillgång.</span><span class="sxs-lookup"><span data-stu-id="10c89-151">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="10c89-152">I fältet **Visa behov som** väljer du filtret **Alla behov**.</span><span class="sxs-lookup"><span data-stu-id="10c89-152">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="10c89-153">I fältet **Behovstyp** kan du välja vilka ordertyper som du vill visa.</span><span class="sxs-lookup"><span data-stu-id="10c89-153">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="10c89-154">Order som inte har några problem med tillgången visas inte.</span><span class="sxs-lookup"><span data-stu-id="10c89-154">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="10c89-155">Om det inte finns några order när en plan beräknas visas ett meddelande och inga planeringsrader visas.</span><span class="sxs-lookup"><span data-stu-id="10c89-155">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="10c89-156">Planera en inköpsorder för att uppfylla behov av komponenter</span><span class="sxs-lookup"><span data-stu-id="10c89-156">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="10c89-157">I den här proceduren skapar du en inköpsorder på komponenter som behövs för produktionen.</span><span class="sxs-lookup"><span data-stu-id="10c89-157">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="10c89-158">Så här planerar du en inköpsorder för att uppfylla komponentbehovet i produktionen</span><span class="sxs-lookup"><span data-stu-id="10c89-158">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="10c89-159">Expandera den första raden (välj +-symbolen).</span><span class="sxs-lookup"><span data-stu-id="10c89-159">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="10c89-160">Välj den första behovsraden med artikel **LSU-15**, och välj sedan åtgärden **visa dokument**.</span><span class="sxs-lookup"><span data-stu-id="10c89-160">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="10c89-161">Stäng produktionsordern och återgå till sidan **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="10c89-161">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="10c89-162">I fältet **Återanskaffningssystem** väljer du **Inköp**.</span><span class="sxs-lookup"><span data-stu-id="10c89-162">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="10c89-163">Standardvärdet är från artikelkortet, eller lagerställeenhetskortet, men det går att ändra till något av följande tre alternativ:</span><span class="sxs-lookup"><span data-stu-id="10c89-163">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="10c89-164">**Inköp** – Om du vill skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-164">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="10c89-165">**Överföring** – Om du vill skapa en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-165">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="10c89-166">**Prod.order** – Om du vill skapa en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-166">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="10c89-167">I fältet **Leverera från** måste du välja något av följande alternativ enligt det återanskaffningssystem som du har markerat:</span><span class="sxs-lookup"><span data-stu-id="10c89-167">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="10c89-168">**Leverantör** – För inköp</span><span class="sxs-lookup"><span data-stu-id="10c89-168">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="10c89-169">**Lagerställe** – för överföringar</span><span class="sxs-lookup"><span data-stu-id="10c89-169">**Location** – For transfers</span></span>  

     <span data-ttu-id="10c89-170">Om inte fältet fylls i visas ett felmeddelande när du försöker skapa leveransorderna.</span><span class="sxs-lookup"><span data-stu-id="10c89-170">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="10c89-171">Om komponenterna har ett standardleverantörsnummer på artikelkorten är raderna förinställda.</span><span class="sxs-lookup"><span data-stu-id="10c89-171">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="10c89-172">Välj fältet **Leverera från**.</span><span class="sxs-lookup"><span data-stu-id="10c89-172">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="10c89-173">På sidan **Artikelns leverantörskatalog** väljer du åtgärden **Ny** och sedan leverantör **30000**.</span><span class="sxs-lookup"><span data-stu-id="10c89-173">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="10c89-174">Välj knappen **OK** om du vill återvända till sidan **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="10c89-174">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="10c89-175">Kopiera leverantörsnummer **30000** till de andra raderna för högtalarkomponenterna på den här produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="10c89-175">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="10c89-176">Du är nu redo att skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-176">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="10c89-177">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-177">Choose the **Make Orders** action.</span></span> <span data-ttu-id="10c89-178">Sidan **Skapa leveransorder** öppnas.</span><span class="sxs-lookup"><span data-stu-id="10c89-178">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="10c89-179">På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-179">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="10c89-180">På snabbfliken **Alternativ**, i fältet **Skapa inköpsorder**, väljer du alternativet **Skapa inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="10c89-180">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="10c89-181">Välj knappen **OK** för att skapa inköpsorder för alla komponenterna på ordern.</span><span class="sxs-lookup"><span data-stu-id="10c89-181">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="10c89-182">Inköpsorder skapas och sparas som de sista orderna i listan över inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-182">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="10c89-183">Planera en överföringsorder för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="10c89-183">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="10c89-184">I den här proceduren planerar du för behov från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-184">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="10c89-185">Behovsraderna motsvarar försäljningsrader och inte komponentrader som vid efterfrågan från produktion.</span><span class="sxs-lookup"><span data-stu-id="10c89-185">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="10c89-186">Så här planerar du en överföringsorder för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="10c89-186">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="10c89-187">Flytta markören till planeringsraden för order **2008**.</span><span class="sxs-lookup"><span data-stu-id="10c89-187">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="10c89-188">Expandera raden och flytta markören till behovsraden.</span><span class="sxs-lookup"><span data-stu-id="10c89-188">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="10c89-189">Försäljningsorder **2008** avser tio högtalare, artikel **LS-120** som har beställts av John Haddock Insurance Co.</span><span class="sxs-lookup"><span data-stu-id="10c89-189">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="10c89-190">Artikelns definierade återanskaffningssystem och standardleverantör visas.</span><span class="sxs-lookup"><span data-stu-id="10c89-190">The item's defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="10c89-191">Längst ned på sidan finns fyra informationsfält.</span><span class="sxs-lookup"><span data-stu-id="10c89-191">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="10c89-192">I fältet **Tidigast disponibelt den** syns det att de tio delar som behövs kommer att vara disponibla, genom en inkommande leveransorder, nio dagar senare än det aktuella förfallodatumet.</span><span class="sxs-lookup"><span data-stu-id="10c89-192">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="10c89-193">Om det är för sent för kunden innehåller fältet **Disponibelt för överföring** tretton enheter av samma artikel på ett annat lagerställe.</span><span class="sxs-lookup"><span data-stu-id="10c89-193">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="10c89-194">Det betyder att du behöver planera för artikeltillgången.</span><span class="sxs-lookup"><span data-stu-id="10c89-194">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="10c89-195">Välj fältet **Disponibelt för överföring** för att öppna sidan **Hämta alternativ leverans**.</span><span class="sxs-lookup"><span data-stu-id="10c89-195">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="10c89-196">Välj knappen **OK** för att boka de tio artiklar som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="10c89-196">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="10c89-197">På behovsraden har det föreslagna inköpet bytts ut mot en överföring från lagerställe PRIMÄR.</span><span class="sxs-lookup"><span data-stu-id="10c89-197">In the demand line, the suggested purchase has been exchanged with a transfer from MAIN location.</span></span> <span data-ttu-id="10c89-198">Med funktionen **Skapa order** skapas en överföringsorder från PRIMÄR till det lagerställe där behovet finns.</span><span class="sxs-lookup"><span data-stu-id="10c89-198">The **Make Orders** function creates a transfer order from MAIN to the demanded location.</span></span> <span data-ttu-id="10c89-199">Fältet **Ersättningar finns** fungerar på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="10c89-199">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="10c89-200">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-200">Choose the **Make Orders** action.</span></span> <span data-ttu-id="10c89-201">Sidan **Skapa leveransorder** öppnas.</span><span class="sxs-lookup"><span data-stu-id="10c89-201">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="10c89-202">På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-202">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="10c89-203">På snabbfliken **Alternativ**, i fältet **Skapa överföringsorder**, väljer du alternativet **Skapa överföringsorder**.</span><span class="sxs-lookup"><span data-stu-id="10c89-203">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="10c89-204">Välj knappen **OK** för att skapa överföringsordern som gör att försäljningsordern kan uppfyllas.</span><span class="sxs-lookup"><span data-stu-id="10c89-204">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="10c89-205">Överföringsordern skapas och sparas i listan som den sista ordern i listan över öppna överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-205">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="10c89-206">Planera en produktionsorder med flera nivåer för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="10c89-206">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="10c89-207">I den här proceduren planerar du att uppfylla försäljningsbehovet av en tillverkad artikel med flera produktnivåer som var och en ger upphov till beroende produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="10c89-207">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="10c89-208">Så här planerar du produktion i flera nivåer för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="10c89-208">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="10c89-209">Markera planeringsraden med försäljningsbehov för order **1001** som skapades tidigare under förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="10c89-209">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="10c89-210">Det här behovet är en försäljningsrad, men artikeln har ett definierat återanskaffningssystem, **Prod.order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-210">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="10c89-211">Fortsätt genom att lägga till en extra klocka i varje cykels komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="10c89-211">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="10c89-212">På sidan **Komponenter** väljer du åtgärden **Planeringskomponenter**.</span><span class="sxs-lookup"><span data-stu-id="10c89-212">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="10c89-213">På raden för klockan (Bell) ändrar du fältet **Antal per** från **1** till **2**.</span><span class="sxs-lookup"><span data-stu-id="10c89-213">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="10c89-214">På sidan **Orderplanering** kan du överväga planeringsalternativen.</span><span class="sxs-lookup"><span data-stu-id="10c89-214">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="10c89-215">I det här fallet har du inga alternativ, ingen överföring, ersättning eller sen leverans.</span><span class="sxs-lookup"><span data-stu-id="10c89-215">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="10c89-216">Du måste skapa den föreslagna leveransordern, en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-216">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="10c89-217">Välj åtgärden **Skapa order** för att skapa produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="10c89-217">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="10c89-218">På sidan **Orderplanering** kan du lägga märke till att planeringsraden för försäljningsordern **1001** inte längre finns och att det ursprungliga försäljningsbehovet är uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="10c89-218">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="10c89-219">Stäng sidan **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="10c89-219">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="10c89-220">Nu kan du välja att stanna kvar i den här vyn och slutföra alla planeringsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="10c89-220">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="10c89-221">Istället ska du nu ikläda dig rollen som produktionsplanerare genom att gå till produktionsordern som du skapade, och öppna sidan **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="10c89-221">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="10c89-222">Som produktionsplanerare måste du planera en särskild produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="10c89-222">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="10c89-223">Så här planerar du en särskild produktionsorder</span><span class="sxs-lookup"><span data-stu-id="10c89-223">To plan a specific production order</span></span>  

1.  <span data-ttu-id="10c89-224">Öppna produktionsordern **101001** på tio cyklar som du precis har skapat med funktionen **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-224">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="10c89-225">Öppna sidan **Prod.order – komponenter** för att kontrollera att den extra klockan återges i produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="10c89-225">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="10c89-226">Välj åtgärden **Planerad**.</span><span class="sxs-lookup"><span data-stu-id="10c89-226">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="10c89-227">Sidan **Orderplanering** öppnas i en vy som är alltid filtrerad efter specifika produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="10c89-227">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="10c89-228">Det går inte att göra ändringar i fönstret.</span><span class="sxs-lookup"><span data-stu-id="10c89-228">Sales demand is not displayed.</span></span> <span data-ttu-id="10c89-229">Du måste beräkna en plan innan du kan se ytterligare behov.</span><span class="sxs-lookup"><span data-stu-id="10c89-229">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="10c89-230">Välj åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="10c89-230">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="10c89-231">Lägg märke till att fyra nya produktionsorder visas som oplanerat produktionsbehov härlett från order **101001**.</span><span class="sxs-lookup"><span data-stu-id="10c89-231">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="10c89-232">De nya raderna representerar nytt produktionsbehov från de delprodukter som måste skapas för att producera ordern.</span><span class="sxs-lookup"><span data-stu-id="10c89-232">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="10c89-233">Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för produktionsordrarna.</span><span class="sxs-lookup"><span data-stu-id="10c89-233">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="10c89-234">Om du vill ha mer information om behovsraderna kan du lägga till fälten **Efterfrågekvantitet** och **Disponibelt efterfrågat antal** i din vy.</span><span class="sxs-lookup"><span data-stu-id="10c89-234">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="10c89-235">Nu måste du leverera tio enheter av varje komponent.</span><span class="sxs-lookup"><span data-stu-id="10c89-235">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="10c89-236">Lägg märke till att fyra av behovsraderna har återanskaffningssystemet Prod.order.</span><span class="sxs-lookup"><span data-stu-id="10c89-236">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="10c89-237">Dessa fyra delprodukter representerar cykelns andra produktnivå.</span><span class="sxs-lookup"><span data-stu-id="10c89-237">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="10c89-238">Standardinställningarna för återanskaffning är redan ifyllda och du kan fortsätta med att skapa order.</span><span class="sxs-lookup"><span data-stu-id="10c89-238">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="10c89-239">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-239">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="10c89-240">Innan du klickar på **OK** bör du notera texten på snabbfliken **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="10c89-240">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="10c89-241">Den här texten är viktig eftersom du vet att cykeln har flera producerade komponenter, delmontage, i sin produktstruktur som kan behövas när du skapar produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="10c89-241">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="10c89-242">På sidan **Skapa leveransorder**, i fältet **Skapa order för**, väljer du alternativet **Alla rader** och väljer sedan **OK** för att skapa produktionsorder för den andra produktnivån.</span><span class="sxs-lookup"><span data-stu-id="10c89-242">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="10c89-243">Lägg märke till att produktionsbehovet på högsta nivån för produktionsorder 101001 inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="10c89-243">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="10c89-244">Det innebär att det ursprungliga produktionsbehovet av delprodukterna har åtgärdats genom planeringen.</span><span class="sxs-lookup"><span data-stu-id="10c89-244">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="10c89-245">På sidan **Orderplanering** kan du beräkna en plan igen för att planera för cykelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="10c89-245">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="10c89-246">Välj åtgärden **Skapa inköpsförslag** för att Skapa inköpsförslagen på nytt enligt instruktionerna i den inbäddade hjälptexten.</span><span class="sxs-lookup"><span data-stu-id="10c89-246">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="10c89-247">De två nya raderna representerar ytterligare produktionsbehov härlett från de delprodukter som planerades i föregående steg.</span><span class="sxs-lookup"><span data-stu-id="10c89-247">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="10c89-248">Vi rekommenderar att du skapar två produktionsorder för att leverera hjulnaven, en för 10 framnav och en för 10 baknav.</span><span class="sxs-lookup"><span data-stu-id="10c89-248">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="10c89-249">Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för de två produktionsordrarna.</span><span class="sxs-lookup"><span data-stu-id="10c89-249">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="10c89-250">Den föreslagna leveransplanen anger att totalt fyra inköpsorder kommer att skapas för komponenterna.</span><span class="sxs-lookup"><span data-stu-id="10c89-250">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="10c89-251">Du bestämmer dig för att skapa de föreslagna orderna.</span><span class="sxs-lookup"><span data-stu-id="10c89-251">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="10c89-252">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="10c89-252">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="10c89-253">I fältet **Skapa order för**, markera alternativet **Alla rader** och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c89-253">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="10c89-254">Kontrollera om det finns ytterligare behov för produktion av den överordnade artikeln, cykeln, som säljs på försäljningsorder 1001.</span><span class="sxs-lookup"><span data-stu-id="10c89-254">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="10c89-255">Välj åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="10c89-255">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="10c89-256">Meddelandet tyder på att alla artiklar som behövs nu är levererade.</span><span class="sxs-lookup"><span data-stu-id="10c89-256">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="10c89-257">Kontrollera de fast planerade produktionsorder som skapas.</span><span class="sxs-lookup"><span data-stu-id="10c89-257">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="10c89-258">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="10c89-258">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="10c89-259">Stäng sidan **Fasta planerade prod.order** för att se hur starttider och sluttider för enskilda order har planerats enligt produktstrukturen.</span><span class="sxs-lookup"><span data-stu-id="10c89-259">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="10c89-260">Komponenterna på den lägsta nivån tillverkas först.</span><span class="sxs-lookup"><span data-stu-id="10c89-260">The lowest-level components are produced first.</span></span> <span data-ttu-id="10c89-261">Därför måste du planera order i flera nivåer, vilket framgår av den här planeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="10c89-261">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="10c89-262">Se även</span><span class="sxs-lookup"><span data-stu-id="10c89-262">See Also</span></span>  
 <span data-ttu-id="10c89-263">[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="10c89-263">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="10c89-264">Genomgång: Planera leveranser automatiskt</span><span class="sxs-lookup"><span data-stu-id="10c89-264">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]