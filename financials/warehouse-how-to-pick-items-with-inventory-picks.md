---
title: "Så här plockar du artiklar med Lagerplockning | Microsoft Docs"
description: "Om det lagerställe som du vill plocka från har konfigurerats så att plockbehandling krävs men inte leveransbearbetning, använder du lagerplockningsdokument för att registrera och bokföra plocknings- och leveransinformation för dina källdokument."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ba8c1649094c9606766c4f4e88df5beed9400e53
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-items-with-inventory-picks"></a><span data-ttu-id="247cb-103">Så här plockar du artiklar med Lagerplockning</span><span class="sxs-lookup"><span data-stu-id="247cb-103">How to: Pick Items with Inventory Picks</span></span>
<span data-ttu-id="247cb-104">När det lagerställe som du vill plocka från har konfigurerats så att plockbehandling krävs men inte leveransbearbetning, använder du fönstret **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina källdokument.</span><span class="sxs-lookup"><span data-stu-id="247cb-104">When your location is set up to require pick processing but not shipment processing, you use the **Inventory Pick** window to record and post picking and shipping information for your source documents.</span></span> <span data-ttu-id="247cb-105">Det avgående källdokumentet kan vara en försäljningsorder, en utgående överföringsorder eller en produktionsorder vars komponenter är klara att plockas.</span><span class="sxs-lookup"><span data-stu-id="247cb-105">The outbound source document can be a sales order, a purchase return order, an outbound transfer order, or a production order whose components are ready to be picked.</span></span>

> [!NOTE]  
> <span data-ttu-id="247cb-106">Komponenter för monteringsorder kan inte plockas eller bokföras med lagerplockningar.</span><span class="sxs-lookup"><span data-stu-id="247cb-106">Components for assembly orders cannot be picked or posted with inventory picks.</span></span> <span data-ttu-id="247cb-107">Med **lagerförflyttning** fönstret.</span><span class="sxs-lookup"><span data-stu-id="247cb-107">Instead, use the **Inventory Movement** window.</span></span> <span data-ttu-id="247cb-108">För mer informatio, se [Så här: Flytta komponenter till ett operationsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="247cb-108">For more information, see [How to: Move Components to an Operation Area in Basic Warehousing](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

>  <span data-ttu-id="247cb-109">Om plockning- och leveransförsäljningsradantal läggs till i order ska du följa vissa regler när du skapar lagerplockningsraderna.</span><span class="sxs-lookup"><span data-stu-id="247cb-109">When picking and shipping sales line quantities that are assembled to the order, you must follow certain rules when creating the inventory pick lines.</span></span> <span data-ttu-id="247cb-110">Mer information finns i avsnittet ”hantera artiklar för montering mot kundorder i lagerplockningar” i .</span><span class="sxs-lookup"><span data-stu-id="247cb-110">For more information, see the “Handling Assemble-to-Order Items in Inventory Picks” section.</span></span>  

<span data-ttu-id="247cb-111">Du kan skapa en lagerartikelplockning på tre sätt:</span><span class="sxs-lookup"><span data-stu-id="247cb-111">You can create an inventory pick in three ways:</span></span>  

- <span data-ttu-id="247cb-112">Skapa plockningen i två steg genom att först begära en lagerplockning genom att släppa källdokument.</span><span class="sxs-lookup"><span data-stu-id="247cb-112">Create the pick in two steps by first requesting an inventory pick by releasing the source document.</span></span> <span data-ttu-id="247cb-113">Det signalerar till distributionslagret att källdokumentet är klart för plockning.</span><span class="sxs-lookup"><span data-stu-id="247cb-113">This signals to the warehouse that the source document is ready for picking.</span></span> <span data-ttu-id="247cb-114">Lagerplockning kan sedan skapas från fönstret **Lagerplockning** baserat på källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="247cb-114">The inventory pick can then be created in the **Inventory Pick** window based on the source document.</span></span>  
- <span data-ttu-id="247cb-115">Skapa lagerplockningen direkt från själva källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="247cb-115">Create the inventory pick directly from the source document itself.</span></span>  
- <span data-ttu-id="247cb-116">Du kan skapa lagerplockningar för flera källdokument samtidigt med hjälp av batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="247cb-116">You can create inventory picks for several source documents at the same time by using the batch job.</span></span>  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a><span data-ttu-id="247cb-117">Så här begär du en lagerplockning genom att släppa källdokumentet</span><span class="sxs-lookup"><span data-stu-id="247cb-117">To request an inventory pick by releasing the source document</span></span>  
<span data-ttu-id="247cb-118">För försäljningsorder, inköpsreturorder och avgående överföringsorder skapar du distributionslagerkravet genom att släppa ordern.</span><span class="sxs-lookup"><span data-stu-id="247cb-118">For sales orders, purchase return orders, and outbound transfer orders, you create the warehouse request by releasing the order.</span></span> <span data-ttu-id="247cb-119">Nedan beskrivs hur du gör detta från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="247cb-119">The following describes how to do this from a sales order.</span></span>

1.  <span data-ttu-id="247cb-120">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="247cb-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="247cb-121">Markera den försäljningsorder som du vill släppa och välj sedan åtgärden **Släpp**.</span><span class="sxs-lookup"><span data-stu-id="247cb-121">Select the sales order that you want to release, and then choose the **Release** action.</span></span>

<span data-ttu-id="247cb-122">Om det gäller produktionsorder skapar du automatisktdistributionslagerkravet för plockningen av komponenterna som kallas *bokföring*, när produktionsorderns status ändras till **Släppt** eller när den släppta produktionsordern skapas.</span><span class="sxs-lookup"><span data-stu-id="247cb-122">For production orders, you automatically create the warehouse request for the picking of components, called *flushing*, when the production order status is changed to **Released** or when the released production order is created.</span></span> <span data-ttu-id="247cb-123">Mer information finnsi [Så här: Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="247cb-123">For more information, see [How to: Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>

<span data-ttu-id="247cb-124">När distributionslagerkravet har skapats kan någon som arbetar i distributionslagret och plockar artiklar se att källdokumentet är klart att plockas, och kan då skapa ett nytt plockningsdokument från distributionslagerkravet.</span><span class="sxs-lookup"><span data-stu-id="247cb-124">After the warehouse request has been created, a warehouse employee assigned to picking items can see that the source document is ready to be picked and can create a new pick document based on the warehouse request.</span></span>  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a><span data-ttu-id="247cb-125">Så här skapar du en lagerplockning från källdokumentet:</span><span class="sxs-lookup"><span data-stu-id="247cb-125">To create an inventory pick based on the source document</span></span>
<span data-ttu-id="247cb-126">Nu när begäran har skapats kan lagerpersonalen skapa en ny lagerplockning baserat på släppta källdokument.</span><span class="sxs-lookup"><span data-stu-id="247cb-126">Now that the request is created, the warehouse employee can create a new inventory pick based on the released source document.</span></span>
1.  <span data-ttu-id="247cb-127">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerplockningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="247cb-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="247cb-128">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="247cb-128">Choose the **New** action.</span></span>  
3. <span data-ttu-id="247cb-129">I fältet **Källdokument** markerar du den typ av källdokument som du plockar för.</span><span class="sxs-lookup"><span data-stu-id="247cb-129">In the **Source Document** field, select the type of source document you are picking for.</span></span>  
4. <span data-ttu-id="247cb-130">I fältet **Ursprungsnr** markerar du källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="247cb-130">In the **Source No.** field, select the source document.</span></span>  
5. <span data-ttu-id="247cb-131">Välj åtgärden **Hämta källdokument** för att välja från en lista över avgående källdokument som är klara för plockning för på lagerstället.</span><span class="sxs-lookup"><span data-stu-id="247cb-131">Alternatively, choose the **Get Source Document** action to select the document from a list of outbound source documents that are ready for picking at the location.</span></span>  
6. <span data-ttu-id="247cb-132">Välj **OK** för att fylla plockrader enligt det valda källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="247cb-132">Choose the **OK** button to fill the pick lines according to the selected source document.</span></span>  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a><span data-ttu-id="247cb-133">Så här skapar du en lagerplockning från källdokumentet</span><span class="sxs-lookup"><span data-stu-id="247cb-133">To create an inventory pick from the source document</span></span>  
1.  <span data-ttu-id="247cb-134">I källdokumentet, som kan vara en försäljningsorder, inköpsreturorder, avgående överföringsorder eller en produktionsorder, klickar du på åtgärden **Skapa lagerartikelinförsel/plocka**.</span><span class="sxs-lookup"><span data-stu-id="247cb-134">In the source document, which can be a sales order, purchase return order, outbound transfer order, or production order, choose the **Create Inventory Put-away/Pick** action.</span></span>
2.  <span data-ttu-id="247cb-135">Markera kryssrutan **Skapa lagerplockning**.</span><span class="sxs-lookup"><span data-stu-id="247cb-135">Select the **Create Invt. Pick** check box.</span></span>  
3.  <span data-ttu-id="247cb-136">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="247cb-136">Choose the **OK** button.</span></span> <span data-ttu-id="247cb-137">En ny lagerplockning skapas.</span><span class="sxs-lookup"><span data-stu-id="247cb-137">A new inventory pick will be created.</span></span>

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a><span data-ttu-id="247cb-138">Så här skapar du flera lagerplockningar med batch-jobbet</span><span class="sxs-lookup"><span data-stu-id="247cb-138">To create multiple inventory picks with a batch job</span></span>  
1.  <span data-ttu-id="247cb-139">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Skapa lagerinförsel/plockning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="247cb-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Invt. Put-away / Pick**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="247cb-140">På snabbfliken **Dist.lagerkrav** använder du fälten **Ursprungsnr** och **Källdokument** om du vill filtrera efter vissa typer av dokument eller intervall med dokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="247cb-140">On the **Warehouse Request** FastTab, use the **Source Document** and **Source No.** fields to filter on certain types of documents  or ranges of document numbers.</span></span> <span data-ttu-id="247cb-141">Du kan till exempel skapa plockningar för enbart försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="247cb-141">For example, you can create picks only for sales orders.</span></span>  
3. <span data-ttu-id="247cb-142">Välj fältet **Skapa lagerinförsel** på kryssrutan **Skapa lagerplockning**.</span><span class="sxs-lookup"><span data-stu-id="247cb-142">On the **Options** FastTab, select the **Create Invt. Pick** check box.</span></span>
4. <span data-ttu-id="247cb-143">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="247cb-143">Choose the **OK** button.</span></span> <span data-ttu-id="247cb-144">De specifika lagerplockningarna jar skapats.</span><span class="sxs-lookup"><span data-stu-id="247cb-144">The specified inventory picks are created.</span></span>

> [!NOTE]  
>  <span data-ttu-id="247cb-145">Om plockning- och leveransförsäljningsradantal läggs till i order ska du följa vissa regler när du skapar lagerplockningsraderna.</span><span class="sxs-lookup"><span data-stu-id="247cb-145">If picking and shipping sales line quantities that are assembled to the order you should follow certain rules when creating the inventory pick lines.</span></span> <span data-ttu-id="247cb-146">Mer information finns i avsnittet ”hantera artiklar för montering mot kundorder i lagerplockningar” i .</span><span class="sxs-lookup"><span data-stu-id="247cb-146">For more information, see the “Handling Assemble-to-Order Items in Inventory Picks” section.</span></span>  
>   
>  <span data-ttu-id="247cb-147">I grundläggande lagerkonfiguration plockas artiklar för montering mot försäljningsorder från den kopplade försäljningsordern som förklaras i det här avsnittet.</span><span class="sxs-lookup"><span data-stu-id="247cb-147">In basic warehouse configurations, items that are assembled to sales orders are picked from the related sales order, as explained in this topic.</span></span> <span data-ttu-id="247cb-148">Mer information finns i avsnittet ”hantera artiklar för montering mot kundorder i lagerplockningar” i Lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="247cb-148">For more information, see “Handling Assemble-to-Order Items in Inventory Picks” in Inventory Pick.</span></span>  

## <a name="to-record-the-inventory-picks"></a><span data-ttu-id="247cb-149">När du vill registrera lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="247cb-149">To record the inventory picks</span></span>  
1.  <span data-ttu-id="247cb-150">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerplockning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="247cb-150">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Pick**, and then choose the related link.</span></span>  
2. <span data-ttu-id="247cb-151">I fältet **Lagerplatskod** på plockningsraderna, är lagerplatsen som artiklarna måste plockas från antyder per artiklarna standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="247cb-151">In the **Bin Code** field on the pick lines, the bin that the items must be picked from is suggesting per the item's default bin.</span></span> <span data-ttu-id="247cb-152">Du kan ändra lagerplatsen i det här fönstret om det behövs.</span><span class="sxs-lookup"><span data-stu-id="247cb-152">You can change the bin in this window if necessary.</span></span>  
3. <span data-ttu-id="247cb-153">Utför plockningen och ange information för den faktiska kvantiteten som förts in i fältet **Ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="247cb-153">Perform the pick and enter the information for the actual quantity put away in the **Qty. to Handle** field.</span></span>

    <span data-ttu-id="247cb-154">Om det är nödvändigt att plocka artiklar för en rad på flera lagerplatser, t.ex. eftersom de inte finns på den utsedda lagerplatsen, använder du funktionen **Dela rad**, på snabbfliken **Rader**.</span><span class="sxs-lookup"><span data-stu-id="247cb-154">If it is necessary to pick the items for one line from more than one bin, for example because they are not available in the designated bin, then use the **Split Line** function on the **Lines** FastTab.</span></span> <span data-ttu-id="247cb-155">Mer information om hur du delar upp rader finns i [så här: dela dist.lageraktivitet rader](warehouse-how-to-split-warehouse-activity-lines.md).</span><span class="sxs-lookup"><span data-stu-id="247cb-155">For more information about splitting lines, see [How to: Split Warehouse Activity Lines](warehouse-how-to-split-warehouse-activity-lines.md).</span></span>  
4. <span data-ttu-id="247cb-156">När du har utfört plockningen, väljer du åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="247cb-156">When you have performed the pick, choose the **Post** action.</span></span>    

<span data-ttu-id="247cb-157">Vid bokföringsprocessen bokförs leverans av de källdokumentrader som har plockats, eller om det gäller produktionsorder bokförs förbrukningen vid bokföringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="247cb-157">The posting process will post the shipment of the source document lines that have been picked, or in the case of production orders, the posting process will post the consumption.</span></span> <span data-ttu-id="247cb-158">Om lagerstället använder lagerplatser kommer bokföringen även att skapa distributionslagertransaktioner för att bokföra ändringar i antalet lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="247cb-158">If the location uses bins, the posting will also create warehouse entries to post the bin quantity changes.</span></span>  

## <a name="to-delete-inventory-pick-lines"></a><span data-ttu-id="247cb-159">Ta bort lagerplockningsrader</span><span class="sxs-lookup"><span data-stu-id="247cb-159">To delete inventory pick lines</span></span>  
<span data-ttu-id="247cb-160">Om artiklar i lagerplockningen inte är tillgängliga, kan du ta bort de lagerplockningsrader när du har bokfört dem och har sedan ta bort dokumentet lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="247cb-160">If items on the inventory pick are not available, then you can delete those inventory pick lines after posting and then delete the inventory pick document.</span></span> <span data-ttu-id="247cb-161">Källdokumentet, till exempel en försäljningsorder eller en produktionsorder, har sedan återstående artiklar som ska plockas som kan erhållas via en ny lagerplockning senare när artiklarna blir tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="247cb-161">The source document, such as a sales order or a production order, will have remaining items to be picked, which can be obtained through a new inventory pick later when the items become available.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="247cb-162">Den här processen är inte möjlig, om serienr/partinr angetts i källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="247cb-162">This process is not possible if serial/lot numbers are specified on the source document.</span></span> <span data-ttu-id="247cb-163">Till exempel om en försäljningsorderrad innehåller en serienr/partinr, då det artikelspårning specifikation tas bort om en lagerplockningsrad för serienr/partinr tas bort.</span><span class="sxs-lookup"><span data-stu-id="247cb-163">For example, if a sales order line contains a serial/lot number, then that item tracking specification will be deleted if an inventory pick line for the serial/lot number is deleted.</span></span>  
>   
>  <span data-ttu-id="247cb-164">Om lagerplockningsrader har serienr/partinr som inte är tillgängliga, måste du inte ta bort de aktuella raderna.</span><span class="sxs-lookup"><span data-stu-id="247cb-164">If inventory pick lines have serial/lot numbers that are not available, you must not delete the lines in question.</span></span> <span data-ttu-id="247cb-165">I stället måste ändra fältet **Ant. att hantera** till noll, bokföra faktisk plockning och sedan bort lagerplockningsdokument.</span><span class="sxs-lookup"><span data-stu-id="247cb-165">Instead, you must change the **Qty. to Handle** field to zero, post the actual picks, and then delete the inventory pick document.</span></span> <span data-ttu-id="247cb-166">Det garanterar att lagerplockningsraderna för de serienr/partinr kan återskapas från senare försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="247cb-166">This ensures that the inventory pick lines for those serial/lot numbers can be recreated from the sales order later.</span></span>  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a><span data-ttu-id="247cb-167">Hantering av artikel för montering mot kundorder i lagerplockningar</span><span class="sxs-lookup"><span data-stu-id="247cb-167">Handling Assemble-to-Order Items with Inventory Picks</span></span>
<span data-ttu-id="247cb-168">Fönstret **Lagerplockning** används också för att plocka och leverera för försäljning där artiklar måste vara församlade, innan de kan levereras.</span><span class="sxs-lookup"><span data-stu-id="247cb-168">The **Inventory Pick** window is also used to pick and ship for sales where items must be assembled before they can be shipped.</span></span> <span data-ttu-id="247cb-169">Mer information finns i [så här: sälja artiklar monterde mot order](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="247cb-169">For more information, see [How to: Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>

<span data-ttu-id="247cb-170">Artiklar som ska levereras, inte fysiskt finns i en lagerplats, förrän de är bokförda och församlade som utflöde på en lagerplats i monteringsområdet.</span><span class="sxs-lookup"><span data-stu-id="247cb-170">Items to be shipped are not physically present in a bin until they are assembled and posted as output to a bin in the assembly area.</span></span> <span data-ttu-id="247cb-171">Det innebär att plocka artiklar för montering mot kundorder för utleverans följer ett speciellt flöde.</span><span class="sxs-lookup"><span data-stu-id="247cb-171">This means that picking assemble-to-order items for shipment follows a special flow.</span></span> <span data-ttu-id="247cb-172">Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen.</span><span class="sxs-lookup"><span data-stu-id="247cb-172">From a bin, warehouse workers take the assembly items to the shipping dock and then post the inventory pick.</span></span> <span data-ttu-id="247cb-173">Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.</span><span class="sxs-lookup"><span data-stu-id="247cb-173">The posted inventory pick then posts the assembly output, the component consumption, and the sales shipment.</span></span>

<span data-ttu-id="247cb-174">Du kan lägga upp [!INCLUDE[d365fin](includes/d365fin_md.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas.</span><span class="sxs-lookup"><span data-stu-id="247cb-174">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] to automatically create an inventory movement when the inventory pick for the assembly item is created.</span></span> <span data-ttu-id="247cb-175">Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** i fönstret **Monteringsinställningar**</span><span class="sxs-lookup"><span data-stu-id="247cb-175">To enable this, you must select the **Create Movements Automatically** field in the **Assembly Setup** window.</span></span> <span data-ttu-id="247cb-176">För mer informatio, se [Så här: Flytta komponenter till ett operationsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="247cb-176">For more information, see [How to: Move Components to an Operation Area in Basic Warehousing](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

<span data-ttu-id="247cb-177">Lagerplockningsrader för försäljningsartiklar skapas på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder.</span><span class="sxs-lookup"><span data-stu-id="247cb-177">Inventory pick lines for sales items are created in different ways depending on whether none, some, or all of the sales line quantities are assembled to order.</span></span>

<span data-ttu-id="247cb-178">I vanliga lagerförsäljningar, när du använder lagerplockningar för att bokföra utleveransen av lagerantal, skapas en lagerplockrad eller flera om artikeln ligger i olika lagerplatser för varje försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="247cb-178">In regular sales where you use inventory picks to post shipment of inventory quantities, one inventory pick line, or several if the item is placed in different bins, is created for each sales order line.</span></span> <span data-ttu-id="247cb-179">Denna plockningsrad baseras på antalet i **Ant. att utleverera**.</span><span class="sxs-lookup"><span data-stu-id="247cb-179">This pick line is based on the quantity in the **Qty. to Ship** field.</span></span>

<span data-ttu-id="247cb-180">I montering mot kundorder försäljning, där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antal.</span><span class="sxs-lookup"><span data-stu-id="247cb-180">In assemble-to-order sales where the full quantity on the sales order line is assembled to order, one inventory pick line is created for that quantity.</span></span> <span data-ttu-id="247cb-181">Detta innebär att värdet i fältet Antal att montera är lika med värdet i fältet **Antal att leverera**.</span><span class="sxs-lookup"><span data-stu-id="247cb-181">This means that the value in the Quantity to Assemble field is the same as the value in the **Qty. to Ship** field.</span></span> <span data-ttu-id="247cb-182">Fältet **montering mot kundorder** är markerat på raden.</span><span class="sxs-lookup"><span data-stu-id="247cb-182">The **Assemble to Order** field is selected on the line.</span></span>

<span data-ttu-id="247cb-183">Om ett monteringsutflöde har angetts för lagerstället, när värdet i fältet **Lagerpl.kod för mont. mot lev.** eller värdet i **Från monteringsplats - kod** i den ordern infogas i fältet **Lagerplatskod** på lagerplockningsraden.</span><span class="sxs-lookup"><span data-stu-id="247cb-183">If an assembly output flow is set up for the location, then the value in the **Asm.-to-Order Shpt. Bin Code** field or the value in the **From-Assembly Bin Code** field, in that order, is inserted in the **Bin Code** field on the inventory pick line.</span></span>

<span data-ttu-id="247cb-184">Om ingen lagerplatskod anges på försäljningsorderraden, och ingen monteringsutflöde har angetts för lagerstället, är **Lagerplatskod** på lagerplockningsraden tomt.</span><span class="sxs-lookup"><span data-stu-id="247cb-184">If no bin code is specified on the sales order line, and no assembly output flow is set up for the location, then the **Bin Code** field on the inventory pick line is empty.</span></span> <span data-ttu-id="247cb-185">Lagerarbetaren måste öppna **Lagerplatsinnehåll**och markera den lagerplats där monteringsartiklarna är församlade.</span><span class="sxs-lookup"><span data-stu-id="247cb-185">The warehouse worker must open the **Bin Contents** window and select the bin where the assembly items are assembled.</span></span>

<span data-ttu-id="247cb-186">I alla scenarier där en del av antalet måste först vara församlad och ett annat ska plockas från lagret, skapas ett minimum på två lagerplockningsrader.</span><span class="sxs-lookup"><span data-stu-id="247cb-186">In combination scenarios, where a part of the quantity must first be assembled and another must be picked from inventory, a minimum of two inventory pick lines are created.</span></span> <span data-ttu-id="247cb-187">En plockningsrad är för antal för montering mot kundorder.</span><span class="sxs-lookup"><span data-stu-id="247cb-187">One pick line is for the assemble-to-order quantity.</span></span> <span data-ttu-id="247cb-188">Den andra plockningsraden beror på vilka lagerplatser som kan uppfylla det återstående antalet från lagret.</span><span class="sxs-lookup"><span data-stu-id="247cb-188">The other pick line depends on which bins can fulfill the remaining quantity from inventory.</span></span> <span data-ttu-id="247cb-189">Lagerplatskoder på de två raderna är ifyllt olika sätt, som beskrivs för de två olika försäljningstyperna.</span><span class="sxs-lookup"><span data-stu-id="247cb-189">Bin codes on the two lines are filled in different ways as described for the two different sales types respectively.</span></span> <span data-ttu-id="247cb-190">Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="247cb-190">For more information, see the “Combination Scenarios” section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="247cb-191">Se även</span><span class="sxs-lookup"><span data-stu-id="247cb-191">See Also</span></span>  
[<span data-ttu-id="247cb-192">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="247cb-192">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="247cb-193">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="247cb-193">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="247cb-194">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="247cb-194">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="247cb-195">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="247cb-195">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="247cb-196">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="247cb-196">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="247cb-197">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="247cb-197">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
