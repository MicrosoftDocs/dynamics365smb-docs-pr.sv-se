---
title: "Genomgång - Planera leveranser manuellt | Microsoft Docs"
description: "Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan. Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2992c2a9cbd2142e69cfb59294791ec31ce4dcb1
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="ed353-104">Genomgång: Planera leveranser manuellt</span><span class="sxs-lookup"><span data-stu-id="ed353-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="ed353-105">Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="ed353-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="ed353-106">Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="ed353-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="ed353-107">I den här genomgången använder du fönstret **Orderplanering**, som är ett enkelt leveransplaneringsverktyg som bygger på manuellt beslutsfattande snarare än parameterbaserad automatisk planering.</span><span class="sxs-lookup"><span data-stu-id="ed353-107">In this walkthrough you will use the **Order Planning** window, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="ed353-108">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="ed353-108">About This Walkthrough</span></span>  
 <span data-ttu-id="ed353-109">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="ed353-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="ed353-110">Planera en inköpsorder för komponenter till produktionen.</span><span class="sxs-lookup"><span data-stu-id="ed353-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="ed353-111">Planera en överföringsorder för att uppfylla försäljningsbehov.</span><span class="sxs-lookup"><span data-stu-id="ed353-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="ed353-112">Planera en produktionsorder för en artikel med flera nivåer.</span><span class="sxs-lookup"><span data-stu-id="ed353-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="ed353-113">Roller</span><span class="sxs-lookup"><span data-stu-id="ed353-113">Roles</span></span>  
 <span data-ttu-id="ed353-114">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="ed353-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="ed353-115">Produktionsplanerare</span><span class="sxs-lookup"><span data-stu-id="ed353-115">Production Planner</span></span>  
-   <span data-ttu-id="ed353-116">Inköpsagent</span><span class="sxs-lookup"><span data-stu-id="ed353-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="ed353-117">Försäljningsorderhandläggare</span><span class="sxs-lookup"><span data-stu-id="ed353-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="ed353-118">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="ed353-118">Prerequisites</span></span>  
 <span data-ttu-id="ed353-119">Innan du påbörjar genomgången måste du installera [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed353-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ed353-120">Följande ändringar måste göras i databasen:</span><span class="sxs-lookup"><span data-stu-id="ed353-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="ed353-121">Ta bort alla befintliga försäljningsorder på cyklar.</span><span class="sxs-lookup"><span data-stu-id="ed353-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="ed353-122">Skapa en försäljningsorder på tio cyklar på lagerstället BLÅ.</span><span class="sxs-lookup"><span data-stu-id="ed353-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="ed353-123">Ta bort alla planerade och fast planerade produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="ed353-124">Ta inte bort påbörjade order med transaktioner som redan har bokförts.</span><span class="sxs-lookup"><span data-stu-id="ed353-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="ed353-125">En regel är att de data som föreslås i genomgången ska användas eftersom dessa data har alla nödvändiga poster.</span><span class="sxs-lookup"><span data-stu-id="ed353-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="ed353-126">Situation</span><span class="sxs-lookup"><span data-stu-id="ed353-126">Story</span></span>  
 <span data-ttu-id="ed353-127">Eduardo är produktionsplanerare på ett litet tillverkande företag och håller på att planera produktions- och inköpsorder för att uppfylla behov.</span><span class="sxs-lookup"><span data-stu-id="ed353-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="ed353-128">Eftersom produkternas produktstrukturer har få nivåer och orderflödet är relativt lågt använder Eduardo fönstret **Orderplanering** för att manuellt skapa leveransorder, en produktnivå i taget.</span><span class="sxs-lookup"><span data-stu-id="ed353-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** window to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="ed353-129">I en mer komplex produktionsmiljö används planeringsförslaget för att planera leveranser baserat på parametrar som omplaneringsperiod, säkerhetsledtid, beställningspunkt och batch-beräkningar av den sammanställda efterfrågan på alla produktnivåer.</span><span class="sxs-lookup"><span data-stu-id="ed353-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="ed353-130">Ställa in exempeldata</span><span class="sxs-lookup"><span data-stu-id="ed353-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="ed353-131">Standarddemonstrationsföretaget CRONUS har för närvarande en stor mängd oplanerad efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="ed353-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="ed353-132">Under de olika planeringsaktiviteterna i den här genomgången måste du avvika från det realistiska verksamhetsflödet genom att ignorera efterfrågan med tidiga förfallodatum och i stället använda efterfrågan med senare förfallodatum.</span><span class="sxs-lookup"><span data-stu-id="ed353-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-window"></a><span data-ttu-id="ed353-133">Använda fönstret Orderplanering</span><span class="sxs-lookup"><span data-stu-id="ed353-133">Using the Order Planning Window</span></span>  

<!-- 
The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-window"></a><span data-ttu-id="ed353-134">Så här använder du fönstret Orderplanering</span><span class="sxs-lookup"><span data-stu-id="ed353-134">To use the Order Planning window</span></span>  

1.  <span data-ttu-id="ed353-135">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Orderplanering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ed353-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="ed353-136">När fönstret **Orderplanering** har öppnats måste en plan beräknas för att visa den nya efterfrågan sedan den senaste beräkningen.</span><span class="sxs-lookup"><span data-stu-id="ed353-136">When the **Order Planning** window first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="ed353-137">Välj åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="ed353-137">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="ed353-138">Planeringssystemet analyserar alla ny behov som har tillkommit, exempelvis ny försäljning, förändrad försäljning och produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-138">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="ed353-139">Den kvantitet som behövs för respektive efterfrågerad beräknas utifrån den totala tillgången.</span><span class="sxs-lookup"><span data-stu-id="ed353-139">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="ed353-140">Beräkningen görs per order.</span><span class="sxs-lookup"><span data-stu-id="ed353-140">This calculation is performed order-by-order.</span></span> <span data-ttu-id="ed353-141">Det betyder att den order som innehåller efterfrågan med det tidigaste förfallodatumet eller utleveransdatumet beräknas först.</span><span class="sxs-lookup"><span data-stu-id="ed353-141">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="ed353-142">Därefter beräknas ytterligare efterfrågerader i samma ordning, oavsett förfallodatum eller utleveransdatum.</span><span class="sxs-lookup"><span data-stu-id="ed353-142">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="ed353-143">Se till att fönstret **Orderplanering** är maximerat och att kolumnfälten har lagom storlek för att alla standardfältnamn ska synas.</span><span class="sxs-lookup"><span data-stu-id="ed353-143">Be sure that the **Order Planning** window is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="ed353-144">När beräkningen är slutförd visas alla ej uppfyllda behov i fönstret som reducerade orderrader sorterade efter behovsdatum.</span><span class="sxs-lookup"><span data-stu-id="ed353-144">When the calculation is completed, the window displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="ed353-145">Lägg märke till att CRONUS har flera order med ej uppfyllda behov.</span><span class="sxs-lookup"><span data-stu-id="ed353-145">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="ed353-146">Varje planeringsrad i fetstil motsvarar en order, försäljningsorder eller produktionsorder, inklusive minst en orderrad med otillräcklig tillgång.</span><span class="sxs-lookup"><span data-stu-id="ed353-146">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="ed353-147">I fältet **Visa behov som** väljer du filtret **Alla behov**.</span><span class="sxs-lookup"><span data-stu-id="ed353-147">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="ed353-148">I fältet **Behovstyp** kan du välja vilka ordertyper som du vill visa.</span><span class="sxs-lookup"><span data-stu-id="ed353-148">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="ed353-149">Order som inte har några problem med tillgången visas inte.</span><span class="sxs-lookup"><span data-stu-id="ed353-149">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="ed353-150">Om det inte finns några order när en plan beräknas visas ett meddelande och inga planeringsrader visas.</span><span class="sxs-lookup"><span data-stu-id="ed353-150">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="ed353-151">Planera en inköpsorder för att uppfylla behov av komponenter</span><span class="sxs-lookup"><span data-stu-id="ed353-151">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="ed353-152">I den här proceduren skapar du en inköpsorder på komponenter som behövs för produktionen.</span><span class="sxs-lookup"><span data-stu-id="ed353-152">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="ed353-153">Så här planerar du en inköpsorder för att uppfylla komponentbehovet i produktionen</span><span class="sxs-lookup"><span data-stu-id="ed353-153">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="ed353-154">Expandera den första raden (välj +-symbolen).</span><span class="sxs-lookup"><span data-stu-id="ed353-154">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="ed353-155">Välj den första behovsraden med artikel **LSU-15**, och välj sedan åtgärden **visa dokument**.</span><span class="sxs-lookup"><span data-stu-id="ed353-155">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="ed353-156">Stäng produktionsordern och återgå till fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ed353-156">Close the opened production order to return to the **Order Planning** window.</span></span>  
4.  <span data-ttu-id="ed353-157">I fältet **Återanskaffningssystem** väljer du **Inköp**.</span><span class="sxs-lookup"><span data-stu-id="ed353-157">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="ed353-158">Standardvärdet är från artikelkortet, eller lagerställeenhetskortet, men det går att ändra till något av följande tre alternativ:</span><span class="sxs-lookup"><span data-stu-id="ed353-158">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="ed353-159">**Inköp** – Om du vill skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-159">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="ed353-160">**Överföring** – Om du vill skapa en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-160">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="ed353-161">**Prod.order** – Om du vill skapa en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-161">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="ed353-162">I fältet **Leverera från** måste du välja något av följande alternativ enligt det återanskaffningssystem som du har markerat:</span><span class="sxs-lookup"><span data-stu-id="ed353-162">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="ed353-163">**Leverantör** – För inköp</span><span class="sxs-lookup"><span data-stu-id="ed353-163">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="ed353-164">**Lagerställe** – för överföringar</span><span class="sxs-lookup"><span data-stu-id="ed353-164">**Location** – For transfers</span></span>  

     <span data-ttu-id="ed353-165">Om inte fältet fylls i visas ett felmeddelande när du försöker skapa leveransorderna.</span><span class="sxs-lookup"><span data-stu-id="ed353-165">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ed353-166">Om komponenterna har ett standardleverantörsnummer på artikelkorten är raderna förinställda.</span><span class="sxs-lookup"><span data-stu-id="ed353-166">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="ed353-167">Välj fältet **Leverera från**.</span><span class="sxs-lookup"><span data-stu-id="ed353-167">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="ed353-168">I fönstret **Artikelns leverantörskatalog** väljer du åtgärden **Ny** och sedan leverantör **30000**.</span><span class="sxs-lookup"><span data-stu-id="ed353-168">In the **Item Vendor Catalogue** window, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="ed353-169">Välj knappen **OK** om du vill återvända till fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ed353-169">Choose the **OK** button to return to the **Order Planning** window.</span></span>  
9. <span data-ttu-id="ed353-170">Kopiera leverantörsnummer **30000** till de andra raderna för högtalarkomponenterna på den här produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="ed353-170">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="ed353-171">Du är nu redo att skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-171">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="ed353-172">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-172">Choose the **Make Orders** action.</span></span> <span data-ttu-id="ed353-173">Fönstret **Skapa leveransorder** öppnas.</span><span class="sxs-lookup"><span data-stu-id="ed353-173">The **Make Supply Orders** window opens.</span></span>  
11. <span data-ttu-id="ed353-174">På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-174">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="ed353-175">På snabbfliken **Alternativ**, i fältet **Skapa inköpsorder**, väljer du alternativet **Skapa inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="ed353-175">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="ed353-176">Välj knappen **OK** för att skapa inköpsorder för alla komponenterna på ordern.</span><span class="sxs-lookup"><span data-stu-id="ed353-176">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="ed353-177">Inköpsorder skapas och sparas som de sista orderna i listan över inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-177">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="ed353-178">Planera en överföringsorder för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="ed353-178">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="ed353-179">I den här proceduren planerar du för behov från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-179">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="ed353-180">Behovsraderna motsvarar försäljningsrader och inte komponentrader som vid efterfrågan från produktion.</span><span class="sxs-lookup"><span data-stu-id="ed353-180">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="ed353-181">Så här planerar du en överföringsorder för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="ed353-181">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="ed353-182">Flytta markören till planeringsraden för order **2008**.</span><span class="sxs-lookup"><span data-stu-id="ed353-182">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="ed353-183">Expandera raden och flytta markören till behovsraden.</span><span class="sxs-lookup"><span data-stu-id="ed353-183">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="ed353-184">Försäljningsorder **2008** avser tio högtalare, artikel **LS-120** som har beställts av John Haddock Insurance Co.</span><span class="sxs-lookup"><span data-stu-id="ed353-184">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="ed353-185">Artikelns definierade återanskaffningssystem och standardleverantör visas.</span><span class="sxs-lookup"><span data-stu-id="ed353-185">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ed353-186">Längst ned i fönstret finns fyra informationsfält.</span><span class="sxs-lookup"><span data-stu-id="ed353-186">At the bottom of the window, there are four information fields.</span></span> <span data-ttu-id="ed353-187">I fältet **Tidigast disponibelt den** syns det att de tio delar som behövs kommer att vara disponibla, genom en ankommande leveransorder, nio dagar senare än det aktuella förfallodatumet.</span><span class="sxs-lookup"><span data-stu-id="ed353-187">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="ed353-188">Om det är för sent för kunden innehåller fältet **Disponibelt för överföring** tretton enheter av samma artikel på ett annat lagerställe.</span><span class="sxs-lookup"><span data-stu-id="ed353-188">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="ed353-189">Det betyder att du behöver planera för artikeltillgången.</span><span class="sxs-lookup"><span data-stu-id="ed353-189">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="ed353-190">Välj fältet **Disponibelt för överföring** för att öppna fönstret **Hämta alternativ leverans**.</span><span class="sxs-lookup"><span data-stu-id="ed353-190">Choose the **Available for Transfer** field to open the **Get Alternative Supply** window.</span></span>  
4.  <span data-ttu-id="ed353-191">Välj knappen **OK** för att boka de tio artiklar som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="ed353-191">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ed353-192">På behovsraden har det föreslagna inköpet bytts ut mot en överföring från lagerstället GRÖN.</span><span class="sxs-lookup"><span data-stu-id="ed353-192">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="ed353-193">Med funktionen **Skapa order** skapas en överföringsorder från GRÖN till det lagerställe där behovet finns.</span><span class="sxs-lookup"><span data-stu-id="ed353-193">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="ed353-194">Fältet **Ersättningar finns** fungerar på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="ed353-194">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="ed353-195">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-195">Choose the **Make Orders** action.</span></span> <span data-ttu-id="ed353-196">Fönstret **Skapa leveransorder** öppnas.</span><span class="sxs-lookup"><span data-stu-id="ed353-196">The **Make Supply Orders** window opens.</span></span>  
6.  <span data-ttu-id="ed353-197">På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-197">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="ed353-198">På snabbfliken **Alternativ**, i fältet **Skapa överföringsorder**, väljer du alternativet **Skapa överföringsorder**.</span><span class="sxs-lookup"><span data-stu-id="ed353-198">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="ed353-199">Välj knappen **OK** för att skapa överföringsordern som gör att försäljningsordern kan uppfyllas.</span><span class="sxs-lookup"><span data-stu-id="ed353-199">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="ed353-200">Överföringsordern skapas och sparas i listan som den sista ordern i listan över öppna överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-200">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="ed353-201">Planera en produktionsorder med flera nivåer för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="ed353-201">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="ed353-202">I den här proceduren planerar du att uppfylla försäljningsbehovet av en tillverkad artikel med flera produktnivåer som var och en ger upphov till beroende produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="ed353-202">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="ed353-203">Så här planerar du produktion i flera nivåer för att uppfylla försäljningsbehov</span><span class="sxs-lookup"><span data-stu-id="ed353-203">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="ed353-204">Markera planeringsraden med försäljningsbehov för order **1001** som skapades tidigare under förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="ed353-204">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="ed353-205">Det här behovet är en försäljningsrad, men artikeln har ett definierat återanskaffningssystem, **Prod.order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-205">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="ed353-206">Fortsätt genom att lägga till en extra klocka i varje cykels komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="ed353-206">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="ed353-207">I fönstret **Komponenter** väljer du åtgärden **Planeringskomponenter**.</span><span class="sxs-lookup"><span data-stu-id="ed353-207">Choose the **Components** action to open the **Planning Components** window.</span></span>  
3.  <span data-ttu-id="ed353-208">På raden för klockan (Bell) ändrar du fältet **Antal per** från **1** till **2**.</span><span class="sxs-lookup"><span data-stu-id="ed353-208">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="ed353-209">I fönstret **Orderplanering** kan du överväga planeringsalternativen.</span><span class="sxs-lookup"><span data-stu-id="ed353-209">In the **Order Planning** window, consider your planning alternatives.</span></span> <span data-ttu-id="ed353-210">I det här fallet har du inga alternativ, ingen överföring, ersättning eller sen leverans.</span><span class="sxs-lookup"><span data-stu-id="ed353-210">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="ed353-211">Du måste skapa den föreslagna leveransordern, en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-211">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="ed353-212">Välj åtgärden **Skapa order** för att skapa produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="ed353-212">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="ed353-213">I fönstret **Orderplanering** kan du lägga märke till att planeringsraden för försäljningsordern **1001** inte längre finns och att det ursprungliga försäljningsbehovet är uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="ed353-213">In the **Order Planning** window, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="ed353-214">Stäng fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ed353-214">Close the **Order Planning** window.</span></span>  

     <span data-ttu-id="ed353-215">Nu kan du välja att stanna kvar i den här vyn och slutföra alla planeringsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="ed353-215">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="ed353-216">Istället ska du nu ikläda dig rollen som produktionsplanerare genom att gå till produktionsordern som du skapade, och öppna fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ed353-216">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** window.</span></span>  

 <span data-ttu-id="ed353-217">Som produktionsplanerare måste du planera en särskild produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ed353-217">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="ed353-218">Så här planerar du en särskild produktionsorder</span><span class="sxs-lookup"><span data-stu-id="ed353-218">To plan a specific production order</span></span>  

1.  <span data-ttu-id="ed353-219">Öppna produktionsordern **101001** på tio cyklar som du precis har skapat med funktionen **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-219">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="ed353-220">Öppna fönstret **Prod.order - komponenter** för att kontrollera att den extra klockan återges i produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="ed353-220">Open the **Prod. Order Components** window to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="ed353-221">Välj åtgärden **Planerad**.</span><span class="sxs-lookup"><span data-stu-id="ed353-221">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="ed353-222">Fönstret **Orderplanering** öppnas i en vy som är alltid filtrerad efter specifika produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="ed353-222">The **Order Planning** window opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="ed353-223">Det går inte att göra ändringar i fönstret.</span><span class="sxs-lookup"><span data-stu-id="ed353-223">Sales demand is not displayed.</span></span> <span data-ttu-id="ed353-224">Du måste beräkna en plan innan du kan se ytterligare behov.</span><span class="sxs-lookup"><span data-stu-id="ed353-224">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="ed353-225">Välj åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="ed353-225">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="ed353-226">Lägg märke till att fyra nya produktionsorder visas som oplanerat produktionsbehov härlett från order **101001**.</span><span class="sxs-lookup"><span data-stu-id="ed353-226">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="ed353-227">De nya raderna representerar nytt produktionsbehov från de delprodukter som måste skapas för att producera ordern.</span><span class="sxs-lookup"><span data-stu-id="ed353-227">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="ed353-228">Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för produktionsordrarna.</span><span class="sxs-lookup"><span data-stu-id="ed353-228">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="ed353-229">Om du vill ha mer information om behovsraderna kan du lägga till fälten **Efterfrågekvantitet** och **Disponibelt efterfrågat antal** i din vy.</span><span class="sxs-lookup"><span data-stu-id="ed353-229">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="ed353-230">Nu måste du leverera tio enheter av varje komponent.</span><span class="sxs-lookup"><span data-stu-id="ed353-230">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="ed353-231">Lägg märke till att fyra av behovsraderna har återanskaffningssystemet Prod.order.</span><span class="sxs-lookup"><span data-stu-id="ed353-231">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="ed353-232">Dessa fyra delprodukter representerar cykelns andra produktnivå.</span><span class="sxs-lookup"><span data-stu-id="ed353-232">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="ed353-233">Standardinställningarna för återanskaffning är redan ifyllda och du kan fortsätta med att skapa order.</span><span class="sxs-lookup"><span data-stu-id="ed353-233">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="ed353-234">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-234">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="ed353-235">Innan du klickar på **OK** bör du notera texten på snabbfliken **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ed353-235">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="ed353-236">Den här texten är viktig eftersom du vet att cykeln har flera producerade komponenter, delmontage, i sin produktstruktur som kan behövas när du skapar produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="ed353-236">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="ed353-237">I fönstret **Skapa leveransorder**, i fältet **Skapa order för**, väljer du alternativet **Alla rader** och väljer sedan **OK** för att skapa produktionsorder för den andra produktnivån.</span><span class="sxs-lookup"><span data-stu-id="ed353-237">In the **Make Supply Order** window, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="ed353-238">Lägg märke till att produktionsbehovet på högsta nivån för produktionsorder 101001 inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="ed353-238">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="ed353-239">Det innebär att det ursprungliga produktionsbehovet av delprodukterna har åtgärdats genom planeringen.</span><span class="sxs-lookup"><span data-stu-id="ed353-239">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="ed353-240">I fönstret **Orderplanering** kan du beräkna en plan igen för att planera för cykelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="ed353-240">In the **Order Planning** window, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="ed353-241">Välj åtgärden **Skapa inköpsförslag** för att Skapa inköpsförslagen på nytt enligt instruktionerna i den inbäddade hjälptexten.</span><span class="sxs-lookup"><span data-stu-id="ed353-241">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="ed353-242">De två nya raderna representerar ytterligare produktionsbehov härlett från de delprodukter som planerades i föregående steg.</span><span class="sxs-lookup"><span data-stu-id="ed353-242">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="ed353-243">Vi rekommenderar att du skapar två produktionsorder för att leverera hjulnaven, en för 10 framnav och en för 10 baknav.</span><span class="sxs-lookup"><span data-stu-id="ed353-243">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="ed353-244">Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för de två produktionsordrarna.</span><span class="sxs-lookup"><span data-stu-id="ed353-244">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="ed353-245">Den föreslagna leveransplanen anger att totalt fyra inköpsorder kommer att skapas för komponenterna.</span><span class="sxs-lookup"><span data-stu-id="ed353-245">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="ed353-246">Du bestämmer dig för att skapa de föreslagna orderna.</span><span class="sxs-lookup"><span data-stu-id="ed353-246">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="ed353-247">Välj åtgärden **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="ed353-247">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="ed353-248">I fältet **Skapa order för**, markera alternativet **Alla rader** och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed353-248">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="ed353-249">Kontrollera om det finns ytterligare behov för produktion av den överordnade artikeln, cykeln, som säljs på försäljningsorder 1001.</span><span class="sxs-lookup"><span data-stu-id="ed353-249">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="ed353-250">Välj åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="ed353-250">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="ed353-251">Meddelandet tyder på att alla artiklar som behövs nu är levererade.</span><span class="sxs-lookup"><span data-stu-id="ed353-251">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="ed353-252">Kontrollera de fast planerade produktionsorder som skapas.</span><span class="sxs-lookup"><span data-stu-id="ed353-252">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="ed353-253">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Fasta planerade prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ed353-253">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="ed353-254">Stäng fönstret **Fasta planerade prod.order** för att se hur starttider och sluttider för enskilda order har planerats enligt produktstrukturen.</span><span class="sxs-lookup"><span data-stu-id="ed353-254">In the **Firm Planned Prod. Orders** window review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="ed353-255">Komponenterna på den lägsta nivån tillverkas först.</span><span class="sxs-lookup"><span data-stu-id="ed353-255">The lowest-level components are produced first.</span></span> <span data-ttu-id="ed353-256">Därför måste du planera order i flera nivåer, vilket framgår av den här planeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ed353-256">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed353-257">Se även</span><span class="sxs-lookup"><span data-stu-id="ed353-257">See Also</span></span>  
 <span data-ttu-id="ed353-258">[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="ed353-258">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="ed353-259">Genomgång: Planera leveranser automatiskt</span><span class="sxs-lookup"><span data-stu-id="ed353-259">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)
