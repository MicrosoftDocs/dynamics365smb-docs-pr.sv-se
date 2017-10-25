---
title: "Så här: Plocka för produktion i grundläggande distributionslagerkonfiguration | Microsoft Docs"
description: "När distributionslagrets lagerställe kräver plockningsbearbetning, men inte utleveransbearbetning, använder du fönstret **Lagerplockning** för att ordna och registrera plockning av komponenter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 35eb4fdb15eded48510a232ed26aa02b4f5700c2
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-for-production-or-assembly"></a><span data-ttu-id="4b5fb-103">Så här: Plocka för produktion eller montering</span><span class="sxs-lookup"><span data-stu-id="4b5fb-103">How to: Pick for Production or Assembly</span></span>
<span data-ttu-id="4b5fb-104">Hur du för in plockningskomponenter för produktions- eller monteringsorder beror på hur distributionslagret har ställts in som lagerställe.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-104">How you put away your pick components for production or assembly orders depends on how your warehouse is set up as a location.</span></span> <span data-ttu-id="4b5fb-105">Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-105">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="4b5fb-106">Igrundläggande lagerkonfigurationer där lagerställe kräver plockningsbearbetning, men inte utleveransbearbetning, använder du fönstret **Lagerplockning** för att ordna och registrera plockning av komponenter.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-106">In basic warehouse configurations where the location requires pick processing but not shipment processing, you use the **Inventory Pick** window to organize and record the picking of components.</span></span>  

<span data-ttu-id="4b5fb-107">I grundläggande distributionslagerkonfiguration måste du plocka för monteringsorder med fönstret **Lagertransport**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-107">In basic warehouse configurations, you must pick for assembly orders with the **Inventory Movement** window.</span></span> <span data-ttu-id="4b5fb-108">Mer information finns i avsnittet ”hantera artiklar för montering mot kundorder i lagerplockningar” i [Så här plockar du artiklar med Lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-108">For more information, see the "Handling Assemble-to-Order Item with Inventory Picks" section in [How to: Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>  

<span data-ttu-id="4b5fb-109">I avancerad distributionslagerkonfiguration, där lagerställen kräver både plockning och utleveranser, använder du **dist.lager plockning** för att få komponenter till produktions- eller monteringsordern.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-109">In advanced warehouse configurations where locations require both picks and shipments, you use the **Warehouse Pick** window to bring components to production or assembly orders.</span></span>

> [!NOTE]  
>  <span data-ttu-id="4b5fb-110">Lagerplockningar och lagerförflyttningar har följande viktiga skillnader:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-110">The following important differences exist between inventory picks and inventory movements:</span></span>  
>   
>  -   <span data-ttu-id="4b5fb-111">När du registrerar en lagerplockning för en intern operation, bokförs till exempel produktion, förbrukningen av markerade komponenterna samtidigt.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-111">When you register an inventory pick for an internal operation, such as production, the consumption of the picked components is posted at the same time.</span></span> <span data-ttu-id="4b5fb-112">När du registrerar en lagerförflyttning för en intern operation, registrerar du bara en fysisk transport av nödvändiga komponenter till en lagerplats i operationsområdet utan att bokföra förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-112">When you register an inventory movement for an internal operation, you only record the physical movement of the required components to a bin in the operation area without posting the consumption.</span></span>  
> -   <span data-ttu-id="4b5fb-113">Om du använder lagerplockningar definierar fältet **Lagerplatskod** på en produktionsorderkomponentrad lagerplatsen *ta* från vilken antalet komponenter minskas när konsumtionen bokförs.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-113">When you use inventory picks, the **Bin Code** field on a production order component line defines the *take* bin from where components are decreased when posting consumption.</span></span> <span data-ttu-id="4b5fb-114">Om du använder lagerförflyttningar definierar fältet **Lagerplatskod** på en produktionsorderkomponentrad, lagerplatsen *plats* i operationsområdet från vilken antalet lagerarbetare måste placera komponenter.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-114">When you use inventory movements, the **Bin Code** field on production order component lines defines the *place* bin in the operation area where the warehouse worker must place the components.</span></span>  

<span data-ttu-id="4b5fb-115">En systemvillkor för plockning eller flyttning av komponenter för källdokument, är att en avgående distributionslagerkrav finns för att meddela lagerområdet i komponentbehovet.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-115">A system precondition for picking, or moving, components for source documents is that an outbound warehouse request exists to notify the warehouse area of the component need.</span></span> <span data-ttu-id="4b5fb-116">Den avgående distributionslagerförfrågan skapas när produktionsorderns status ändras till Släppt eller när en släppt produktionsordern skapas.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-116">The outbound warehouse request is created whenever the production order status is changed to Released or when a released production order is created.</span></span>  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a><span data-ttu-id="4b5fb-117">Plocka komponenter i en grundläggande lagerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-117">To pick components in basic warehouse configurations</span></span>
<span data-ttu-id="4b5fb-118">I grundläggande distributionslagerkonfiguration, där det har angetts att lagerstället ska endast använda plockning samt leverans, kan du välja plockkomponenter i fönstret **Lagerplockning**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-118">In basic warehouse configurations where the location is set up to use picking only, you can pick components for production activities with the **Inventory Pick** window.</span></span> <span data-ttu-id="4b5fb-119">För mer information, se [så här: Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-119">For more information, see [How to: Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>

1.  <span data-ttu-id="4b5fb-120">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerplockningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4b5fb-121">Om du vill komma åt produktionsorderns komponenter väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-121">To access the production order components, choose the **Get Source Documents** action, and then select the released production order.</span></span>  
3.  <span data-ttu-id="4b5fb-122">Utför plockningen och registrera den verkliga plockningsinformationen i fältet **Plockat antal**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-122">Perform the pick, and then record the actual picking information in the **Qty. Picked** field.</span></span>  
4.  <span data-ttu-id="4b5fb-123">När raderna är färdiga att bokföras klickar du på **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-123">When the lines are ready for posting, choose the **Post** action.</span></span> <span data-ttu-id="4b5fb-124">Bokföringen skapar de nödvändiga distributionslagertransaktionerna och bokför förbrukningen av artiklarna.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-124">The posting creates the necessary warehouse entries and posts the consumption of the items.</span></span>  

<span data-ttu-id="4b5fb-125">Du kan också skapa en **lagerplockning** direkt från den släppta produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-125">You can also create an **Inventory Pick** directly from the released production order.</span></span> <span data-ttu-id="4b5fb-126">Välj **Skapa lagerartikelinförsel/Plocka**, välj **Skapa lagerplockning** och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-126">Choose the **Create Inventory Put-away/Pick** action, select the **Create Invt. Pick** check box, and then choose the **OK** button.</span></span>

<span data-ttu-id="4b5fb-127">Du kan också använda **Lagertransport**-fönstret för att flytta artiklar mellan lagerplatser ad hoc-, d.v.s till utan att referera till ett ursprungsdokument.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-127">Alternatively, you can use the **Inventory Movement** window to move items between bins ad hoc, meaning without reference to a source document.</span></span>
<span data-ttu-id="4b5fb-128">För mer information, se [Så här: Flytta komponenter till ett operationsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="4b5fb-128">For more information, see [How to: Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a><span data-ttu-id="4b5fb-129">Hantering av artikel för montering mot kundorder i lagerplockningar</span><span class="sxs-lookup"><span data-stu-id="4b5fb-129">Handling Assemble-to-Order Items with Inventory Picks</span></span>
<span data-ttu-id="4b5fb-130">Fönstret **Lagerplockning** används också för att plocka och leverera för försäljning där artiklar måste vara församlade, innan de kan levereras.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-130">The **Inventory Pick** window is also used to pick and ship for sales where items must be assembled before they can be shipped.</span></span> <span data-ttu-id="4b5fb-131">Mer information finns i [så här: sälja artiklar monterde mot order](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-131">For more information, see [How to: Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>

<span data-ttu-id="4b5fb-132">Artiklar som ska levereras, inte fysiskt finns i en lagerplats, förrän de är bokförda och församlade som utflöde på en lagerplats i monteringsområdet.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-132">Items to be shipped are not physically present in a bin until they are assembled and posted as output to a bin in the assembly area.</span></span> <span data-ttu-id="4b5fb-133">Det innebär att plocka artiklar för montering mot kundorder för utleverans följer ett speciellt flöde.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-133">This means that picking assemble-to-order items for shipment follows a special flow.</span></span> <span data-ttu-id="4b5fb-134">Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-134">From a bin, warehouse workers take the assembly items to the shipping dock and then post the inventory pick.</span></span> <span data-ttu-id="4b5fb-135">Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-135">The posted inventory pick then posts the assembly output, the component consumption, and the sales shipment.</span></span>

<span data-ttu-id="4b5fb-136">Du kan lägga upp [!INCLUDE[d365fin](includes/d365fin_md.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-136">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] to automatically create an inventory movement when the inventory pick for the assembly item is created.</span></span> <span data-ttu-id="4b5fb-137">Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** i fönstret **Monteringsinställningar**</span><span class="sxs-lookup"><span data-stu-id="4b5fb-137">To enable this, you must select the **Create Movements Automatically** field in the **Assembly Setup** window.</span></span> <span data-ttu-id="4b5fb-138">För mer informatio, se [Så här: Flytta komponenter till ett operationsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="4b5fb-138">For more information, see [How to: Move Components to an Operation Area in Basic Warehousing](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

<span data-ttu-id="4b5fb-139">Lagerplockningsrader för försäljningsartiklar skapas på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-139">Inventory pick lines for sales items are created in different ways depending on whether none, some, or all of the sales line quantities are assembled to order.</span></span>

<span data-ttu-id="4b5fb-140">I vanliga lagerförsäljningar, när du använder lagerplockningar för att bokföra utleveransen av lagerantal, skapas en lagerplockrad eller flera om artikeln ligger i olika lagerplatser för varje försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-140">In regular sales where you use inventory picks to post shipment of inventory quantities, one inventory pick line, or several if the item is placed in different bins, is created for each sales order line.</span></span> <span data-ttu-id="4b5fb-141">Denna plockningsrad baseras på antalet i **Ant. att utleverera**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-141">This pick line is based on the quantity in the **Qty. to Ship** field.</span></span>

<span data-ttu-id="4b5fb-142">I montering mot kundorder försäljning, där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antal.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-142">In assemble-to-order sales where the full quantity on the sales order line is assembled to order, one inventory pick line is created for that quantity.</span></span> <span data-ttu-id="4b5fb-143">Detta innebär att värdet i fältet Antal att montera är lika med värdet i fältet **Antal att leverera**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-143">This means that the value in the Quantity to Assemble field is the same as the value in the **Qty. to Ship** field.</span></span> <span data-ttu-id="4b5fb-144">Fältet **montering mot kundorder** är markerat på raden.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-144">The **Assemble to Order** field is selected on the line.</span></span>

<span data-ttu-id="4b5fb-145">Om ett monteringsutflöde har angetts för lagerstället, när värdet i fältet **Lagerpl.kod för mont. mot lev.** eller värdet i **Från monteringsplats - kod** i den ordern infogas i fältet **Lagerplatskod** på lagerplockningsraden.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-145">If an assembly output flow is set up for the location, then the value in the **Asm.-to-Order Shpt. Bin Code** field or the value in the **From-Assembly Bin Code** field, in that order, is inserted in the **Bin Code** field on the inventory pick line.</span></span>

<span data-ttu-id="4b5fb-146">Om ingen lagerplatskod anges på försäljningsorderraden, och ingen monteringsutflöde har angetts för lagerstället, är **Lagerplatskod** på lagerplockningsraden tomt.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-146">If no bin code is specified on the sales order line, and no assembly output flow is set up for the location, then the **Bin Code** field on the inventory pick line is empty.</span></span> <span data-ttu-id="4b5fb-147">Lagerarbetaren måste öppna **Lagerplatsinnehåll**och markera den lagerplats där monteringsartiklarna är församlade.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-147">The warehouse worker must open the **Bin Contents** window and select the bin where the assembly items are assembled.</span></span>

<span data-ttu-id="4b5fb-148">I alla scenarier där en del av antalet måste först vara församlad och ett annat ska plockas från lagret, skapas ett minimum på två lagerplockningsrader.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-148">In combination scenarios, where a part of the quantity must first be assembled and another must be picked from inventory, a minimum of two inventory pick lines are created.</span></span> <span data-ttu-id="4b5fb-149">En plockningsrad är för antal för montering mot kundorder.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-149">One pick line is for the assemble-to-order quantity.</span></span> <span data-ttu-id="4b5fb-150">Den andra plockningsraden beror på vilka lagerplatser som kan uppfylla det återstående antalet från lagret.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-150">The other pick line depends on which bins can fulfill the remaining quantity from inventory.</span></span> <span data-ttu-id="4b5fb-151">Lagerplatskoder på de två raderna är ifyllt olika sätt, som beskrivs för de två olika försäljningstyperna.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-151">Bin codes on the two lines are filled in different ways as described for the two different sales types respectively.</span></span> <span data-ttu-id="4b5fb-152">Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-152">For more information, see the “Combination Scenarios” section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a><span data-ttu-id="4b5fb-153">Plocka komponenter i en avancerad lagerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-153">To pick components in advanced warehouse configurations</span></span>
<span data-ttu-id="4b5fb-154">I avancerad distributionslagerkonfiguration, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktion- och monteringsaktiviteter med fönstret **Dist.lager plockning**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-154">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** window.</span></span> <span data-ttu-id="4b5fb-155">För mer information, se [så här: Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-155">For more information, see [How to: Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>

<span data-ttu-id="4b5fb-156">Du kan också använda **Transportförslag** fönstret för att flytta artiklar mellan lagerplatser ad hoc-, d.v.s till utan att referera till ett ursprungsdokument.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-156">Alternatively, you can use the **Movement Worksheet** window to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="4b5fb-157">För mer information, se [Så här: Flytta artiklar avancerad distributionslagerkonfiguration](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-157">For more information, see [How to: Move Items in Advanced Warehouse Configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="4b5fb-158">Du kan inte skapa ett dokument för dist.lager plockning från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-158">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="4b5fb-159">Du kan skapa dokumentet för dist.lager plockning med en pushmetod genom att välja **Skapa dist.lagerplockning** i källdokumentet, till exempel en släppt monteringsorder eller lagerutleverans.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-159">You can create the warehouse pick document in a push fashion by selecting the **Create Whse. Pick** action on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="4b5fb-160">För mer information, se [så här: Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-160">For more information, see [How to: Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="4b5fb-161">Du kan också skapa dokumentet för dist.lager plockning med en pullmetod med hjälp av **Plockningsförslag** fönstret för att undersöka plockningsförfrågningar, både för leverans och intern operation, och sedan skapa de nödvändiga dokumentet för dist.lager plockning.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-161">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** window to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="4b5fb-162">Nedan förklaras ett pull-scenario där du plockar komponenter för en släppt produktionsorder via **Plockningsförslag** fönstret.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-162">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** window.</span></span> <span data-ttu-id="4b5fb-163">Följande procedur gäller även för en monteringsorder.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-163">The procedure also applies to assembly orders.</span></span>  

<span data-ttu-id="4b5fb-164">För att skapa plockning för både pull- och pushscenarier, måste källdokumenten släppas.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-164">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="4b5fb-165">Släppa källdokumenten för intern operation på följande sätt.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-165">Release source documents for internal operations in the following ways.</span></span>  

 |<span data-ttu-id="4b5fb-166">Källdokument</span><span class="sxs-lookup"><span data-stu-id="4b5fb-166">Source Document</span></span>|<span data-ttu-id="4b5fb-167">Släppningsmetod</span><span class="sxs-lookup"><span data-stu-id="4b5fb-167">Release Method</span></span>|  
 |---------------------|--------------------|  
 |<span data-ttu-id="4b5fb-168">Produktionsorder</span><span class="sxs-lookup"><span data-stu-id="4b5fb-168">Production Order</span></span>|<span data-ttu-id="4b5fb-169">Ändra ordertyp till släppta produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-169">Change order type to released production order.</span></span>|  
 |<span data-ttu-id="4b5fb-170">Monteringsorder</span><span class="sxs-lookup"><span data-stu-id="4b5fb-170">Assembly Order</span></span>|<span data-ttu-id="4b5fb-171">Ändra status till släppt.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-171">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="4b5fb-172">Så här plockar du komponenter med hjälp av plockningsförslaget</span><span class="sxs-lookup"><span data-stu-id="4b5fb-172">To pick components using the pick worksheet</span></span>  

1.  <span data-ttu-id="4b5fb-173">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Plockningsförslag**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-173">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4b5fb-174">Välj åtgärden **Hämta dist.lager dokument** och välj sedan de komponentrader från den släppta produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-174">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="4b5fb-175">Analysera raderna, sortera dem för att garantera en effektiv plockningsrunda och kombinera dem med andra förslagsrader, om så behövs, för att minimera plockningstiden för den anställda.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-175">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="4b5fb-176">Välj åtgärden **Skapa plockning**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-176">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="4b5fb-177">Definiera hur du skapar dokument för dist.lager plockning och hur här fältet sorterar plockningsrader genom att fylla i **Skapa plockning** fönstret.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-177">Define how to create the warehouse pick documents and how to sort pick lines by filling fields in the **Create Pick** window.</span></span>  
6.  <span data-ttu-id="4b5fb-178">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-178">Choose the **OK** button.</span></span>

<span data-ttu-id="4b5fb-179">Dokumenten för dist.lager plockning skapas med plockningsrader för varje komponent som krävs i den intern operation.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-179">Warehouse pick documents are now created with pick lines for each component that is required in the internal operation.</span></span>

<span data-ttu-id="4b5fb-180">Om internt operationsområde, till exempel ett produktionslagerplats, har upprättats med en standardlagerplats för placering av komponenter som ska användas i operationen, infogas den lagerplatskoden i placeringsraderna på dokumentet för dist.lager plockning för att visa lagerarbetare var artiklarna ska placeras.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-180">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="4b5fb-181">Mer information finns i [så här: ställa in grundläggande dist.lager med operationsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-181">For more information, see [How to: Set Up Basic Warehouses with Operation Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="4b5fb-182">Fylla förbrukningslagerplatsen</span><span class="sxs-lookup"><span data-stu-id="4b5fb-182">Filling the Consumption Bin</span></span>
<span data-ttu-id="4b5fb-183">Diagrammet visar hur **Lagerplatskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-183">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="4b5fb-184">![Flödesschema för lagerplats](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="4b5fb-184">![Bin flow chart](media/binflow.png "BinFlow")</span></span>

## <a name="see-also"></a><span data-ttu-id="4b5fb-185">Se även</span><span class="sxs-lookup"><span data-stu-id="4b5fb-185">See Also</span></span>
[<span data-ttu-id="4b5fb-186">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="4b5fb-186">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="4b5fb-187">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="4b5fb-187">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4b5fb-188">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="4b5fb-188">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="4b5fb-189">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="4b5fb-189">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="4b5fb-190">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="4b5fb-190">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4b5fb-191">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4b5fb-191">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
