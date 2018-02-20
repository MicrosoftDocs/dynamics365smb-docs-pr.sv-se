---
title: "Genomgång - Planera leveranser manuellt | Microsoft Docs"
description: "Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan. Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: de00ca393b5d2c28292ae3deba743ce3447b6145
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="e1624-104">Genomgång: Planera leveranser manuellt</span><span class="sxs-lookup"><span data-stu-id="e1624-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="e1624-105">Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="e1624-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="e1624-106">Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="e1624-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="e1624-107">I den här genomgången använder du fönstret **Orderplanering**, som är ett enkelt leveransplaneringsverktyg som bygger på manuellt beslutsfattande snarare än parameterbaserad automatisk planering.</span><span class="sxs-lookup"><span data-stu-id="e1624-107">In this walkthrough you will use the **Order Planning** window, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="e1624-108">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="e1624-108">About This Walkthrough</span></span>  
 <span data-ttu-id="e1624-109">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="e1624-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="e1624-110">Planera en inköpsorder för komponenter till produktionen.</span><span class="sxs-lookup"><span data-stu-id="e1624-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="e1624-111">Planera en överföringsorder för att uppfylla försäljningsbehov.</span><span class="sxs-lookup"><span data-stu-id="e1624-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="e1624-112">Planera en produktionsorder för en artikel med flera nivåer.</span><span class="sxs-lookup"><span data-stu-id="e1624-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="e1624-113">Roller</span><span class="sxs-lookup"><span data-stu-id="e1624-113">Roles</span></span>  
 <span data-ttu-id="e1624-114">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="e1624-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="e1624-115">Produktionsplanerare</span><span class="sxs-lookup"><span data-stu-id="e1624-115">Production Planner</span></span>  
-   <span data-ttu-id="e1624-116">Inköpsagent</span><span class="sxs-lookup"><span data-stu-id="e1624-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="e1624-117">Försäljningsorderhandläggare</span><span class="sxs-lookup"><span data-stu-id="e1624-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="e1624-118">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="e1624-118">Prerequisites</span></span>  
 <span data-ttu-id="e1624-119">Innan du påbörjar genomgången måste du installera [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e1624-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e1624-120">Följande ändringar måste göras i databasen:</span><span class="sxs-lookup"><span data-stu-id="e1624-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="e1624-121">Ta bort alla befintliga försäljningsorder på cyklar.</span><span class="sxs-lookup"><span data-stu-id="e1624-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="e1624-122">Skapa en försäljningsorder på tio cyklar på lagerstället BLÅ.</span><span class="sxs-lookup"><span data-stu-id="e1624-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="e1624-123">Ta bort alla planerade och fast planerade produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="e1624-124">Ta inte bort påbörjade order med transaktioner som redan har bokförts.</span><span class="sxs-lookup"><span data-stu-id="e1624-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="e1624-125">En regel är att de data som föreslås i genomgången ska användas eftersom dessa data har alla nödvändiga poster.</span><span class="sxs-lookup"><span data-stu-id="e1624-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="e1624-126">Situation</span><span class="sxs-lookup"><span data-stu-id="e1624-126">Story</span></span>  
 <span data-ttu-id="e1624-127">Eduardo är produktionsplanerare på ett litet tillverkande företag och håller på att planera produktions- och inköpsorder för att uppfylla behov.</span><span class="sxs-lookup"><span data-stu-id="e1624-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="e1624-128">Eftersom produkternas produktstrukturer har få nivåer och orderflödet är relativt lågt använder Eduardo fönstret **Orderplanering** för att manuellt skapa leveransorder, en produktnivå i taget.</span><span class="sxs-lookup"><span data-stu-id="e1624-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** window to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="e1624-129">I en mer komplex produktionsmiljö används planeringsförslaget för att planera leveranser baserat på parametrar som omplaneringsperiod, säkerhetsledtid, beställningspunkt och batch-beräkningar av den sammanställda efterfrågan på alla produktnivåer.</span><span class="sxs-lookup"><span data-stu-id="e1624-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="e1624-130">Ställa in exempeldata</span><span class="sxs-lookup"><span data-stu-id="e1624-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="e1624-131">Standarddemonstrationsföretaget CRONUS har för närvarande en stor mängd oplanerad efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="e1624-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="e1624-132">Under de olika planeringsaktiviteterna i den här genomgången måste du avvika från det realistiska verksamhetsflödet genom att ignorera efterfrågan med tidiga förfallodatum och i stället använda efterfrågan med senare förfallodatum.</span><span class="sxs-lookup"><span data-stu-id="e1624-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-window"></a><span data-ttu-id="e1624-133">Använda fönstret Orderplanering</span><span class="sxs-lookup"><span data-stu-id="e1624-133">Using the Order Planning Window</span></span>  
 <span data-ttu-id="e1624-134">Fönstret **Orderplanering** kan öppnas från flera olika ställen på menyn **Avdelningar** i navigeringsrutan:</span><span class="sxs-lookup"><span data-stu-id="e1624-134">The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:</span></span>  

-   <span data-ttu-id="e1624-135">Produktion, Planering</span><span class="sxs-lookup"><span data-stu-id="e1624-135">Manufacturing, Planning</span></span>  
-   <span data-ttu-id="e1624-136">Försäljning och marknadsföring, Orderbearbetning</span><span class="sxs-lookup"><span data-stu-id="e1624-136">Sales & Marketing, Order Processing</span></span>  
-   <span data-ttu-id="e1624-137">Inköp, Planering</span><span class="sxs-lookup"><span data-stu-id="e1624-137">Purchase, Planning</span></span>  
-   <span data-ttu-id="e1624-138">Du kan dessutom öppna fönstret för en specifik produktionsorder genom att välja **Planering** på fliken **Analysera** i gruppen **Order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-138">In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.</span></span>  

### <a name="to-use-the-order-planning-window"></a><span data-ttu-id="e1624-139">Så här använder du fönstret Orderplanering</span><span class="sxs-lookup"><span data-stu-id="e1624-139">To use the Order Planning window</span></span>  

1.  <span data-ttu-id="e1624-140">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Orderplanering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e1624-140">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="e1624-141">När fönstret **Orderplanering** har öppnats måste en plan beräknas för att visa den nya efterfrågan sedan den senaste beräkningen.</span><span class="sxs-lookup"><span data-stu-id="e1624-141">When the **Order Planning** window first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="e1624-142">Välj åtgärden **Beräkna plan**.</span><span class="sxs-lookup"><span data-stu-id="e1624-142">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="e1624-143">Planeringssystemet analyserar alla ny behov som har tillkommit, exempelvis ny försäljning, förändrad försäljning och produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-143">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="e1624-144">Den kvantitet som behövs för respektive efterfrågerad beräknas utifrån den totala tillgången.</span><span class="sxs-lookup"><span data-stu-id="e1624-144">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="e1624-145">Beräkningen görs per order.</span><span class="sxs-lookup"><span data-stu-id="e1624-145">This calculation is performed order-by-order.</span></span> <span data-ttu-id="e1624-146">Det betyder att den order som innehåller efterfrågan med det tidigaste förfallodatumet eller utleveransdatumet beräknas först.</span><span class="sxs-lookup"><span data-stu-id="e1624-146">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="e1624-147">Därefter beräknas ytterligare efterfrågerader i samma ordning, oavsett förfallodatum eller utleveransdatum.</span><span class="sxs-lookup"><span data-stu-id="e1624-147">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="e1624-148">Se till att fönstret **Orderplanering** är maximerat och att kolumnfälten har lagom storlek för att alla standardfältnamn ska synas.</span><span class="sxs-lookup"><span data-stu-id="e1624-148">Be sure that the **Order Planning** window is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="e1624-149">När beräkningen är slutförd visas alla ej uppfyllda behov i fönstret som reducerade orderrader sorterade efter behovsdatum.</span><span class="sxs-lookup"><span data-stu-id="e1624-149">When the calculation is completed, the window displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="e1624-150">Lägg märke till att CRONUS har flera order med ej uppfyllda behov.</span><span class="sxs-lookup"><span data-stu-id="e1624-150">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="e1624-151">Varje planeringsrad i fetstil motsvarar en order, försäljningsorder eller produktionsorder, inklusive minst en orderrad med otillräcklig tillgång.</span><span class="sxs-lookup"><span data-stu-id="e1624-151">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="e1624-152">I fältet **Visa behov som** väljer du filtret **Alla behov**.</span><span class="sxs-lookup"><span data-stu-id="e1624-152">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="e1624-153">I fältet **Behovstyp** kan du välja vilka ordertyper som du vill visa.</span><span class="sxs-lookup"><span data-stu-id="e1624-153">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="e1624-154">Order som inte har några problem med tillgången visas inte.</span><span class="sxs-lookup"><span data-stu-id="e1624-154">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="e1624-155">Om det inte finns några order när en plan beräknas visas ett meddelande och inga planeringsrader visas.</span><span class="sxs-lookup"><span data-stu-id="e1624-155">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="e1624-156">Planera en inköpsorder för att uppfylla behov av komponenter</span><span class="sxs-lookup"><span data-stu-id="e1624-156">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="e1624-157">I den här proceduren skapar du en inköpsorder på komponenter som behövs för produktionen.</span><span class="sxs-lookup"><span data-stu-id="e1624-157">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="e1624-158">Så här planerar du en inköpsorder för att uppfylla komponentbehovet i produktionen</span><span class="sxs-lookup"><span data-stu-id="e1624-158">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="e1624-159">Expandera den första raden (välj +-symbolen).</span><span class="sxs-lookup"><span data-stu-id="e1624-159">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="e1624-160">Välj den första behovsraden med artikel **LSU-15**, och välj sedan åtgärden **visa dokument**.</span><span class="sxs-lookup"><span data-stu-id="e1624-160">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="e1624-161">Stäng produktionsordern och återgå till fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="e1624-161">Close the opened production order to return to the **Order Planning** window.</span></span>  
4.  <span data-ttu-id="e1624-162">I fältet **Återanskaffningssystem** väljer du **Inköp**.</span><span class="sxs-lookup"><span data-stu-id="e1624-162">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="e1624-163">Standardvärdet är från artikelkortet, eller lagerställeenhetskortet, men det går att ändra till något av följande tre alternativ:</span><span class="sxs-lookup"><span data-stu-id="e1624-163">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="e1624-164">**Inköp** – Om du vill skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-164">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="e1624-165">**Överföring** – Om du vill skapa en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-165">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="e1624-166">**Prod.order** – Om du vill skapa en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-166">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="e1624-167">I fältet **Leverera från** måste du välja något av följande alternativ enligt det återanskaffningssystem som du har markerat:</span><span class="sxs-lookup"><span data-stu-id="e1624-167">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="e1624-168">**Leverantör** – För inköp</span><span class="sxs-lookup"><span data-stu-id="e1624-168">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="e1624-169">**Lagerställe** – för överföringar</span><span class="sxs-lookup"><span data-stu-id="e1624-169">**Location** – For transfers</span></span>  

     <span data-ttu-id="e1624-170">Om inte fältet fylls i visas ett felmeddelande när du försöker skapa leveransorderna.</span><span class="sxs-lookup"><span data-stu-id="e1624-170">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e1624-171">Om komponenterna har ett standardleverantörsnummer på artikelkorten är raderna förinställda.</span><span class="sxs-lookup"><span data-stu-id="e1624-171">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="e1624-172">Välj fältet **Leverera från**.</span><span class="sxs-lookup"><span data-stu-id="e1624-172">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="e1624-173">I fönstret **Artikelns leverantörskatalog** väljer du åtgärden **Ny** och sedan leverantör **30000**.</span><span class="sxs-lookup"><span data-stu-id="e1624-173">In the **Item Vendor Catalogue** window, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="e1624-174">Välj knappen **OK** om du vill återvända till fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="e1624-174">Choose the **OK** button to return to the **Order Planning** window.</span></span>  
9. <span data-ttu-id="e1624-175">Kopiera leverantörsnummer **30000** till de andra raderna för högtalarkomponenterna på den här produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="e1624-175">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="e1624-176">Du är nu redo att skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-176">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="e1624-177">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-177">Choose the **Make Orders** action.</span></span> <span data-ttu-id="e1624-178">Fönstret **Skapa leveransorder** öppnas.</span><span class="sxs-lookup"><span data-stu-id="e1624-178">The **Make Supply Orders** window opens.</span></span>  
11. <span data-ttu-id="e1624-179">På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-179">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="e1624-180">På snabbfliken **Alternativ**, i fältet **Skapa inköpsorder**, väljer du alternativet **Skapa inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="e1624-180">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="e1624-181">Välj knappen **OK** för att skapa inköpsorder för alla komponenterna på ordern.</span><span class="sxs-lookup"><span data-stu-id="e1624-181">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="e1624-182">Inköpsorder skapas och sparas som de sista orderna i listan över inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-182">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="e1624-183">Planera en överföringsorder för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="e1624-183">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="e1624-184">I den här proceduren planerar du för behov från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-184">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="e1624-185">Behovsraderna motsvarar försäljningsrader och inte komponentrader som vid efterfrågan från produktion.</span><span class="sxs-lookup"><span data-stu-id="e1624-185">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="e1624-186">Så här planerar du en överföringsorder för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="e1624-186">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="e1624-187">Flytta markören till planeringsraden för order **2008**.</span><span class="sxs-lookup"><span data-stu-id="e1624-187">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="e1624-188">Expandera raden och flytta markören till behovsraden.</span><span class="sxs-lookup"><span data-stu-id="e1624-188">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="e1624-189">Försäljningsorder **2008** avser tio högtalare, artikel **LS-120** som har beställts av John Haddock Insurance Co.</span><span class="sxs-lookup"><span data-stu-id="e1624-189">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="e1624-190">Artikelns definierade återanskaffningssystem och standardleverantör visas.</span><span class="sxs-lookup"><span data-stu-id="e1624-190">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e1624-191">Längst ned i fönstret finns fyra informationsfält.</span><span class="sxs-lookup"><span data-stu-id="e1624-191">At the bottom of the window, there are four information fields.</span></span> <span data-ttu-id="e1624-192">I fältet **Tidigast disponibelt den** syns det att de tio delar som behövs kommer att vara disponibla, genom en ankommande leveransorder, nio dagar senare än det aktuella förfallodatumet.</span><span class="sxs-lookup"><span data-stu-id="e1624-192">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="e1624-193">Om det är för sent för kunden innehåller fältet **Disponibelt för överföring** tretton enheter av samma artikel på ett annat lagerställe.</span><span class="sxs-lookup"><span data-stu-id="e1624-193">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="e1624-194">Det betyder att du behöver planera för artikeltillgången.</span><span class="sxs-lookup"><span data-stu-id="e1624-194">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="e1624-195">Välj fältet **Disponibelt för överföring** för att öppna fönstret **Hämta alternativ leverans**.</span><span class="sxs-lookup"><span data-stu-id="e1624-195">Choose the **Available for Transfer** field to open the **Get Alternative Supply** window.</span></span>  
4.  <span data-ttu-id="e1624-196">Välj knappen **OK** för att boka de tio artiklar som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="e1624-196">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e1624-197">På behovsraden har det föreslagna inköpet bytts ut mot en överföring från lagerstället GRÖN.</span><span class="sxs-lookup"><span data-stu-id="e1624-197">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="e1624-198">Med funktionen **Skapa order** skapas en överföringsorder från GRÖN till det lagerställe där behovet finns.</span><span class="sxs-lookup"><span data-stu-id="e1624-198">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="e1624-199">Fältet **Ersättningar finns** fungerar på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="e1624-199">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="e1624-200">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-200">Choose the **Make Orders** action.</span></span> <span data-ttu-id="e1624-201">Fönstret **Skapa leveransorder** öppnas.</span><span class="sxs-lookup"><span data-stu-id="e1624-201">The **Make Supply Orders** window opens.</span></span>  
6.  <span data-ttu-id="e1624-202">På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-202">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="e1624-203">På snabbfliken **Alternativ**, i fältet **Skapa överföringsorder**, väljer du alternativet **Skapa överföringsorder**.</span><span class="sxs-lookup"><span data-stu-id="e1624-203">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="e1624-204">Välj knappen **OK** för att skapa överföringsordern som gör att försäljningsordern kan uppfyllas.</span><span class="sxs-lookup"><span data-stu-id="e1624-204">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="e1624-205">Överföringsordern skapas och sparas i listan som den sista ordern i listan över öppna överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-205">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="e1624-206">Planera en produktionsorder med flera nivåer för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="e1624-206">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="e1624-207">I den här proceduren planerar du att uppfylla försäljningsbehovet av en tillverkad artikel med flera produktnivåer som var och en ger upphov till beroende produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="e1624-207">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="e1624-208">Så här planerar du produktion i flera nivåer för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="e1624-208">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="e1624-209">Markera planeringsraden med försäljningsbehov för order **1001** som skapades tidigare under förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="e1624-209">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="e1624-210">Det här behovet är en försäljningsrad, men artikeln har ett definierat återanskaffningssystem, **Prod.order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-210">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="e1624-211">Fortsätt genom att lägga till en extra klocka i varje cykels komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="e1624-211">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="e1624-212">I fönstret **Komponenter** väljer du åtgärden **Planeringskomponenter**.</span><span class="sxs-lookup"><span data-stu-id="e1624-212">Choose the **Components** action to open the **Planning Components** window.</span></span>  
3.  <span data-ttu-id="e1624-213">På raden för klockan (Bell) ändrar du fältet **Antal per** från **1** till **2**.</span><span class="sxs-lookup"><span data-stu-id="e1624-213">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="e1624-214">I fönstret **Orderplanering** kan du överväga planeringsalternativen.</span><span class="sxs-lookup"><span data-stu-id="e1624-214">In the **Order Planning** window, consider your planning alternatives.</span></span> <span data-ttu-id="e1624-215">I det här fallet har du inga alternativ, ingen överföring, ersättning eller sen leverans.</span><span class="sxs-lookup"><span data-stu-id="e1624-215">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="e1624-216">Du måste skapa den föreslagna leveransordern, en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-216">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="e1624-217">Välj åtgärden **Skapa order** för att skapa produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="e1624-217">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="e1624-218">I fönstret **Orderplanering** kan du lägga märke till att planeringsraden för försäljningsordern **1001** inte längre finns och att det ursprungliga försäljningsbehovet är uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="e1624-218">In the **Order Planning** window, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="e1624-219">Stäng fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="e1624-219">Close the **Order Planning** window.</span></span>  

     <span data-ttu-id="e1624-220">Nu kan du välja att stanna kvar i den här vyn och slutföra alla planeringsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e1624-220">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="e1624-221">Istället ska du nu ikläda dig rollen som produktionsplanerare genom att gå till produktionsordern som du skapade, och öppna fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="e1624-221">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** window.</span></span>  

 <span data-ttu-id="e1624-222">Som produktionsplanerare måste du planera en särskild produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e1624-222">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="e1624-223">Så här planerar du en särskild produktionsorder</span><span class="sxs-lookup"><span data-stu-id="e1624-223">To plan a specific production order</span></span>  

1.  <span data-ttu-id="e1624-224">Öppna produktionsordern **101001** på tio cyklar som du precis har skapat med funktionen **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-224">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="e1624-225">Öppna fönstret **Prod.order - komponenter** för att kontrollera att den extra klockan återges i produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="e1624-225">Open the **Prod. Order Components** window to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="e1624-226">Välj åtgärden **Planerad**.</span><span class="sxs-lookup"><span data-stu-id="e1624-226">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="e1624-227">Fönstret **Orderplanering** öppnas i en vy som är alltid filtrerad efter specifika produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="e1624-227">The **Order Planning** window opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="e1624-228">Det går inte att göra ändringar i fönstret.</span><span class="sxs-lookup"><span data-stu-id="e1624-228">Sales demand is not displayed.</span></span> <span data-ttu-id="e1624-229">Du måste beräkna en plan innan du kan se ytterligare behov.</span><span class="sxs-lookup"><span data-stu-id="e1624-229">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="e1624-230">Välj åtgärden **Beräkna plan**.</span><span class="sxs-lookup"><span data-stu-id="e1624-230">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="e1624-231">Lägg märke till att fyra nya produktionsorder visas som oplanerat produktionsbehov härlett från order **101001**.</span><span class="sxs-lookup"><span data-stu-id="e1624-231">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="e1624-232">De nya raderna representerar nytt produktionsbehov från de delprodukter som måste skapas för att producera ordern.</span><span class="sxs-lookup"><span data-stu-id="e1624-232">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="e1624-233">Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för produktionsordrarna.</span><span class="sxs-lookup"><span data-stu-id="e1624-233">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="e1624-234">Om du vill ha mer information om behovsraderna kan du lägga till fälten **Efterfrågekvantitet** och **Disponibelt efterfrågat antal** i din vy.</span><span class="sxs-lookup"><span data-stu-id="e1624-234">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="e1624-235">Nu måste du leverera tio enheter av varje komponent.</span><span class="sxs-lookup"><span data-stu-id="e1624-235">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="e1624-236">Lägg märke till att fyra av behovsraderna har återanskaffningssystemet Prod.order.</span><span class="sxs-lookup"><span data-stu-id="e1624-236">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="e1624-237">Dessa fyra delprodukter representerar cykelns andra produktnivå.</span><span class="sxs-lookup"><span data-stu-id="e1624-237">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="e1624-238">Standardinställningarna för återanskaffning är redan ifyllda och du kan fortsätta med att skapa order.</span><span class="sxs-lookup"><span data-stu-id="e1624-238">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="e1624-239">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-239">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="e1624-240">Innan du klickar på **OK** bör du notera texten på snabbfliken **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="e1624-240">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="e1624-241">Den här texten är viktig eftersom du vet att cykeln har flera producerade komponenter, delmontage, i sin produktstruktur som kan behövas när du skapar produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="e1624-241">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="e1624-242">I fönstret **Skapa leveransorder**, i fältet **Skapa order för**, väljer du alternativet **Alla rader** och väljer sedan **OK** för att skapa produktionsorder för den andra produktnivån.</span><span class="sxs-lookup"><span data-stu-id="e1624-242">In the **Make Supply Order** window, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="e1624-243">Lägg märke till att produktionsbehovet på högsta nivån för produktionsorder 101001 inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="e1624-243">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="e1624-244">Det innebär att det ursprungliga produktionsbehovet av delprodukterna har åtgärdats genom planeringen.</span><span class="sxs-lookup"><span data-stu-id="e1624-244">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="e1624-245">I fönstret **Orderplanering** kan du beräkna en plan igen för att planera för cykelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="e1624-245">In the **Order Planning** window, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="e1624-246">Välj åtgärden **Beräkna plan** för att beräkna planen på nytt enligt instruktionerna i den inbäddade hjälptexten.</span><span class="sxs-lookup"><span data-stu-id="e1624-246">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="e1624-247">De två nya raderna representerar ytterligare produktionsbehov härlett från de delprodukter som planerades i föregående steg.</span><span class="sxs-lookup"><span data-stu-id="e1624-247">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="e1624-248">Vi rekommenderar att du skapar två produktionsorder för att leverera hjulnaven, en för 10 framnav och en för 10 baknav.</span><span class="sxs-lookup"><span data-stu-id="e1624-248">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="e1624-249">Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för de två produktionsordrarna.</span><span class="sxs-lookup"><span data-stu-id="e1624-249">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="e1624-250">Den föreslagna leveransplanen anger att totalt fyra inköpsorder kommer att skapas för komponenterna.</span><span class="sxs-lookup"><span data-stu-id="e1624-250">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="e1624-251">Du bestämmer dig för att skapa de föreslagna orderna.</span><span class="sxs-lookup"><span data-stu-id="e1624-251">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="e1624-252">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="e1624-252">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="e1624-253">I fältet **Skapa order för**, markera alternativet **Alla rader** och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1624-253">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="e1624-254">Kontrollera om det finns ytterligare behov för produktion av den överordnade artikeln, cykeln, som säljs på försäljningsorder 1001.</span><span class="sxs-lookup"><span data-stu-id="e1624-254">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="e1624-255">Välj åtgärden **Beräkna plan**.</span><span class="sxs-lookup"><span data-stu-id="e1624-255">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="e1624-256">Meddelandet tyder på att alla artiklar som behövs nu är levererade.</span><span class="sxs-lookup"><span data-stu-id="e1624-256">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="e1624-257">Kontrollera de fast planerade produktionsorder som skapas.</span><span class="sxs-lookup"><span data-stu-id="e1624-257">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="e1624-258">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Fasta planerade prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e1624-258">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="e1624-259">Stäng fönstret **Fasta planerade prod.order** för att se hur starttider och sluttider för enskilda order har planerats enligt produktstrukturen.</span><span class="sxs-lookup"><span data-stu-id="e1624-259">In the **Firm Planned Prod. Orders** window review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="e1624-260">Komponenterna på den lägsta nivån tillverkas först.</span><span class="sxs-lookup"><span data-stu-id="e1624-260">The lowest-level components are produced first.</span></span> <span data-ttu-id="e1624-261">Därför måste du planera order i flera nivåer, vilket framgår av den här planeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="e1624-261">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1624-262">Se även</span><span class="sxs-lookup"><span data-stu-id="e1624-262">See Also</span></span>  
 <span data-ttu-id="e1624-263">[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="e1624-263">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="e1624-264">Genomgång: Planera leveranser automatiskt</span><span class="sxs-lookup"><span data-stu-id="e1624-264">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)

