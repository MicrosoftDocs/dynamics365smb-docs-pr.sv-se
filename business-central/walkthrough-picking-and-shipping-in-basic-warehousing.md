---
title: Plockning och leverans i grundläggande distributionslagerkonfiguration
description: I Business Central kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktioner beroende på lagerkomplexitetsnivå.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214659"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="d1e44-103">Genomgång: Plockning och leverans i grundläggande lagerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e44-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="d1e44-104">I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.</span><span class="sxs-lookup"><span data-stu-id="d1e44-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="d1e44-105">Metod</span><span class="sxs-lookup"><span data-stu-id="d1e44-105">Method</span></span>|<span data-ttu-id="d1e44-106">inkommande behandling</span><span class="sxs-lookup"><span data-stu-id="d1e44-106">Inbound process</span></span>|<span data-ttu-id="d1e44-107">Lagerställen</span><span class="sxs-lookup"><span data-stu-id="d1e44-107">Bins</span></span>|<span data-ttu-id="d1e44-108">Plockningar</span><span class="sxs-lookup"><span data-stu-id="d1e44-108">Picks</span></span>|<span data-ttu-id="d1e44-109">Utleveranser</span><span class="sxs-lookup"><span data-stu-id="d1e44-109">Shipments</span></span>|<span data-ttu-id="d1e44-110">Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="d1e44-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="d1e44-111">A</span><span class="sxs-lookup"><span data-stu-id="d1e44-111">A</span></span>|<span data-ttu-id="d1e44-112">Bokföra plockning och utleverans från orderraden</span><span class="sxs-lookup"><span data-stu-id="d1e44-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="d1e44-113">INTER</span><span class="sxs-lookup"><span data-stu-id="d1e44-113">X</span></span>|||<span data-ttu-id="d1e44-114">2</span><span class="sxs-lookup"><span data-stu-id="d1e44-114">2</span></span>|  
|<span data-ttu-id="d1e44-115">B</span><span class="sxs-lookup"><span data-stu-id="d1e44-115">B</span></span>|<span data-ttu-id="d1e44-116">Bokföra plockning och utleverans från ett lagerplockningdokument</span><span class="sxs-lookup"><span data-stu-id="d1e44-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="d1e44-117">X</span><span class="sxs-lookup"><span data-stu-id="d1e44-117">X</span></span>||<span data-ttu-id="d1e44-118">3</span><span class="sxs-lookup"><span data-stu-id="d1e44-118">3</span></span>|  
|<span data-ttu-id="d1e44-119">L</span><span class="sxs-lookup"><span data-stu-id="d1e44-119">C</span></span>|<span data-ttu-id="d1e44-120">Bokföra plockning och utleverans från ett distributionslagerutleveransdokument</span><span class="sxs-lookup"><span data-stu-id="d1e44-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="d1e44-121">X</span><span class="sxs-lookup"><span data-stu-id="d1e44-121">X</span></span>|<span data-ttu-id="d1e44-122">6-4-5</span><span class="sxs-lookup"><span data-stu-id="d1e44-122">4/5/6</span></span>|  
|<span data-ttu-id="d1e44-123">D</span><span class="sxs-lookup"><span data-stu-id="d1e44-123">D</span></span>|<span data-ttu-id="d1e44-124">Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument</span><span class="sxs-lookup"><span data-stu-id="d1e44-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="d1e44-125">INTER</span><span class="sxs-lookup"><span data-stu-id="d1e44-125">X</span></span>|<span data-ttu-id="d1e44-126">INTER</span><span class="sxs-lookup"><span data-stu-id="d1e44-126">X</span></span>|<span data-ttu-id="d1e44-127">6-4-5</span><span class="sxs-lookup"><span data-stu-id="d1e44-127">4/5/6</span></span>|  

<span data-ttu-id="d1e44-128">Mer information finns i [Designdetaljer: utgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="d1e44-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="d1e44-129">Efterföljande genomgången visar metod B i föregående tabellen.</span><span class="sxs-lookup"><span data-stu-id="d1e44-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="d1e44-130">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="d1e44-130">About This Walkthrough</span></span>

<span data-ttu-id="d1e44-131">För grundläggande lagerkonfigurationer där lagerstället har konfigurerats att kräva plockningsbearbetning men inte leveransbearbetning, använder du sidan **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina utgående källdokument.</span><span class="sxs-lookup"><span data-stu-id="d1e44-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="d1e44-132">Det utgående källdokumentet kan vara en försäljningsorder, inköpsreturorder, utgående överföringsorder eller produktionsorder med komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="d1e44-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="d1e44-133">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="d1e44-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="d1e44-134">Lägger upp lagerstället SYD för lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="d1e44-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="d1e44-135">Skapa en försäljningsorder för kund 10000 på 30 Amsterdam-lampor.</span><span class="sxs-lookup"><span data-stu-id="d1e44-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="d1e44-136">Släppa försäljningsordern för lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="d1e44-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="d1e44-137">Skapa en lagerplockning som baseras på ett släppt källdokument.</span><span class="sxs-lookup"><span data-stu-id="d1e44-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="d1e44-138">Registrering av lagerrörelsen från lagret och samtidigt bokföra försäljningsutleveransen för källförsäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="d1e44-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="d1e44-139">Roller</span><span class="sxs-lookup"><span data-stu-id="d1e44-139">Roles</span></span>

<span data-ttu-id="d1e44-140">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="d1e44-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="d1e44-141">Dist.lagerchef</span><span class="sxs-lookup"><span data-stu-id="d1e44-141">Warehouse Manager</span></span>  
- <span data-ttu-id="d1e44-142">Orderhandläggare</span><span class="sxs-lookup"><span data-stu-id="d1e44-142">Order Processor</span></span>  
- <span data-ttu-id="d1e44-143">Lagerarbetare</span><span class="sxs-lookup"><span data-stu-id="d1e44-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="d1e44-144">Situation</span><span class="sxs-lookup"><span data-stu-id="d1e44-144">Story</span></span>

<span data-ttu-id="d1e44-145">Ellen, lagerchefen i CRONUS, ställer in lagret SYD för grundläggande plockning där lagerarbetare behandlar utgående beställningar var för sig.</span><span class="sxs-lookup"><span data-stu-id="d1e44-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="d1e44-146">Susan, orderhandläggaren, skapar en försäljningsorder för 30 enheter av artikeln 1928-S att levereras till kund 10000 från distributionslagret SYD.</span><span class="sxs-lookup"><span data-stu-id="d1e44-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="d1e44-147">Anders, lagerarbetaren, måste kontrollera att leveransen förbereds och levereras till kunden.</span><span class="sxs-lookup"><span data-stu-id="d1e44-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="d1e44-148">Anders hanterar alla uppgifter som är involverade på sidan **Lagerplockning** som automatiskt pekar på lagerställena där 1928-S lagras.</span><span class="sxs-lookup"><span data-stu-id="d1e44-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="d1e44-149">Ställer in lagerplatskoder</span><span class="sxs-lookup"><span data-stu-id="d1e44-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="d1e44-150">När du har skapat ett lagerställe måste du lägga till två lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="d1e44-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="d1e44-151">Ställa in lagerplatskoder</span><span class="sxs-lookup"><span data-stu-id="d1e44-151">To setup the bin codes</span></span>

1. <span data-ttu-id="d1e44-152">Välj åtgärden **Lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="d1e44-153">Skapa två lagerplatser med koderna *S-01-0001* och *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="d1e44-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="d1e44-154">Skapa en distributionslagerarbetare på lagerstället SYD</span><span class="sxs-lookup"><span data-stu-id="d1e44-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="d1e44-155">För att kunna använda den här funktionen måste du lägga till dig själv till lagerstället som distributionslagerarbetare.</span><span class="sxs-lookup"><span data-stu-id="d1e44-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="d1e44-156">Så här skapar du en distributionslagerarbetare</span><span class="sxs-lookup"><span data-stu-id="d1e44-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="d1e44-157">Välj ikonen ![Glödlampa som öppnar funktionen Berätta först](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="d1e44-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="d1e44-158">Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Distributionslagerarbetare**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="d1e44-159">I fältet **Lagerställekod** väljer du SYD.</span><span class="sxs-lookup"><span data-stu-id="d1e44-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="d1e44-160">Välj fältet **Standard** och sedan knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="d1e44-161">Göra punkt 1928-S tillgänglig</span><span class="sxs-lookup"><span data-stu-id="d1e44-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="d1e44-162">Gör artikeln 1928-S tillgänglig på lagerstället SYD, genom att följa nedanstående steg:</span><span class="sxs-lookup"><span data-stu-id="d1e44-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="d1e44-163">Välj ikonen ![Glödlampa som öppnar funktionen Berätta andra](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikeljournaler** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="d1e44-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="d1e44-164">Öppna standardjournalen och skapa sedan två artikeljournalrader med följande information om arbetsdatumet (23 januari).</span><span class="sxs-lookup"><span data-stu-id="d1e44-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="d1e44-165">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="d1e44-165">Entry Type</span></span>|<span data-ttu-id="d1e44-166">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d1e44-166">Item Number</span></span>|<span data-ttu-id="d1e44-167">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="d1e44-167">Location Code</span></span>|<span data-ttu-id="d1e44-168">Lagerställeskod</span><span class="sxs-lookup"><span data-stu-id="d1e44-168">Bin Code</span></span>|<span data-ttu-id="d1e44-169">Antal</span><span class="sxs-lookup"><span data-stu-id="d1e44-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="d1e44-170">Positiv antalsjust.</span><span class="sxs-lookup"><span data-stu-id="d1e44-170">Positive Adjmt.</span></span>|<span data-ttu-id="d1e44-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="d1e44-171">1928-S</span></span>|<span data-ttu-id="d1e44-172">SYD</span><span class="sxs-lookup"><span data-stu-id="d1e44-172">SOUTH</span></span>|<span data-ttu-id="d1e44-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="d1e44-173">S-01-0001</span></span>|<span data-ttu-id="d1e44-174">20</span><span class="sxs-lookup"><span data-stu-id="d1e44-174">20</span></span>|  
        |<span data-ttu-id="d1e44-175">Positiv antalsjust.</span><span class="sxs-lookup"><span data-stu-id="d1e44-175">Positive Adjmt.</span></span>|<span data-ttu-id="d1e44-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="d1e44-176">1928-S</span></span>|<span data-ttu-id="d1e44-177">SYD</span><span class="sxs-lookup"><span data-stu-id="d1e44-177">SOUTH</span></span>|<span data-ttu-id="d1e44-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="d1e44-178">S-01-0002</span></span>|<span data-ttu-id="d1e44-179">20</span><span class="sxs-lookup"><span data-stu-id="d1e44-179">20</span></span>|  

        <span data-ttu-id="d1e44-180">Som standard är fältet **Lagerplatskod** på försäljningsraderna dolt, så du måste visa det.</span><span class="sxs-lookup"><span data-stu-id="d1e44-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="d1e44-181">För att göra detta måste du anpassa sidan.</span><span class="sxs-lookup"><span data-stu-id="d1e44-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="d1e44-182">Mer information finns i [Så här börjar du anpassa en sida genom den anpassningsbanderollen](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="d1e44-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="d1e44-183">Välj **Åtgärder**, sedan **Bokföring** och sedan väljer du **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="d1e44-184">Tryck på knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="d1e44-185">Skapar försäljningsreturordern</span><span class="sxs-lookup"><span data-stu-id="d1e44-185">Creating the Sales Order</span></span>

<span data-ttu-id="d1e44-186">Försäljningsorder är den vanligaste typen för utgående källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="d1e44-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="d1e44-187">Så här skapar du försäljningsreturordern</span><span class="sxs-lookup"><span data-stu-id="d1e44-187">To create the sales order</span></span>

1. <span data-ttu-id="d1e44-188">Välj ikonen ![Glödlampa som öppnar funktionen Berätta tredje](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d1e44-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1e44-189">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="d1e44-190">Skapa en försäljningsorder för kund 10000 på arbetsdatumet (23 januari) med följande försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="d1e44-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="d1e44-191">Artikel</span><span class="sxs-lookup"><span data-stu-id="d1e44-191">Item</span></span>|<span data-ttu-id="d1e44-192">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="d1e44-192">Location Code</span></span>|<span data-ttu-id="d1e44-193">Antal</span><span class="sxs-lookup"><span data-stu-id="d1e44-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="d1e44-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="d1e44-194">1928-S</span></span>|<span data-ttu-id="d1e44-195">SYD</span><span class="sxs-lookup"><span data-stu-id="d1e44-195">SOUTH</span></span>|<span data-ttu-id="d1e44-196">30</span><span class="sxs-lookup"><span data-stu-id="d1e44-196">30</span></span>|  

     <span data-ttu-id="d1e44-197">Fortsätt med att meddela lagret att försäljningsordern är klar för lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="d1e44-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="d1e44-198">Välj åtgärden **Släppa**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="d1e44-199">Anders fortsätter att plocka och leverera de sålda artiklarna.</span><span class="sxs-lookup"><span data-stu-id="d1e44-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="d1e44-200">Plocka och leverera artiklar</span><span class="sxs-lookup"><span data-stu-id="d1e44-200">Picking and Shipping Items</span></span>

<span data-ttu-id="d1e44-201">På sidan **Lagerplockning** kan du hantera alla utgående distributionslageraktiviteter för ett särskilt källdokument, t.ex en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="d1e44-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="d1e44-202">Plocka och utleverera artiklar så här</span><span class="sxs-lookup"><span data-stu-id="d1e44-202">To pick and ship items</span></span>

1. <span data-ttu-id="d1e44-203">Välj ikonen ![Glödlampa som öppnar funktionen Berätta fjärde](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerplockning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d1e44-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1e44-204">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="d1e44-205">Kontrollera att fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="d1e44-205">Make sure that the **No.**</span></span> <span data-ttu-id="d1e44-206">fälten på snabbfliken **Allmänt** fylls i.</span><span class="sxs-lookup"><span data-stu-id="d1e44-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="d1e44-207">Välj fältet **Källdokument** och sedan **Försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="d1e44-208">Välj fältet **Ursprungsnr.**, markera raden för försäljningen till kund 10000 och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="d1e44-209">Välj alternativt åtgärden **Hämta källdokument** och välj sedan försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="d1e44-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="d1e44-210">Välj åtgärden **Fyll i auto. ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="d1e44-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="d1e44-211">Alternativt, ange 10 respektive 20 i fältet **Ant. att hantera** på de två lagerplockningsraderna.</span><span class="sxs-lookup"><span data-stu-id="d1e44-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="d1e44-212">Välj åtgärden **bokför**, välj **leverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="d1e44-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="d1e44-213">De 30 Amsterdam-lamporna har nu registrerats som plockade från lagerställen S-01-0001 och S-01-0002, och en negativ artikeltransaktion skapas som återspeglar den bokförda leveransen.</span><span class="sxs-lookup"><span data-stu-id="d1e44-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1e44-214">Se även</span><span class="sxs-lookup"><span data-stu-id="d1e44-214">See Also</span></span>

[<span data-ttu-id="d1e44-215">Plocka artiklar med lagerplockning</span><span class="sxs-lookup"><span data-stu-id="d1e44-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="d1e44-216">Plocka artiklar för utleverans från dist.lager</span><span class="sxs-lookup"><span data-stu-id="d1e44-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="d1e44-217">Ställa in grundläggande dist.lager med verksamhetsområden</span><span class="sxs-lookup"><span data-stu-id="d1e44-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="d1e44-218">Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="d1e44-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="d1e44-219">Plocka för produktion eller montering</span><span class="sxs-lookup"><span data-stu-id="d1e44-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="d1e44-220">Flytta artiklar ad hoc i grundläggande lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="d1e44-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="d1e44-221">Designdetaljer: utgående distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="d1e44-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="d1e44-222">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="d1e44-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="d1e44-223">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1e44-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
