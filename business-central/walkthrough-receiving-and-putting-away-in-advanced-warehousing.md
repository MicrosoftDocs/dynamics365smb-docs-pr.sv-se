---
title: "Inleverera och införa utflöde i avancerad lagerstyrning | Microsoft Docs"
description: "I Business Central kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktioner beroende på lagerkomplexitetsnivå."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3c1f7a6d08ac03da0d89bad464784b71249c36a2
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a><span data-ttu-id="26b0c-103">Genomgång: Inleverera och införa utflöde i avancerade lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="26b0c-103">Walkthrough: Receiving and Putting Away in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="26b0c-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.</span><span class="sxs-lookup"><span data-stu-id="26b0c-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="26b0c-105">Metod</span><span class="sxs-lookup"><span data-stu-id="26b0c-105">Method</span></span>|<span data-ttu-id="26b0c-106">Ankommande behandling</span><span class="sxs-lookup"><span data-stu-id="26b0c-106">Inbound process</span></span>|<span data-ttu-id="26b0c-107">Lagerplatser</span><span class="sxs-lookup"><span data-stu-id="26b0c-107">Bins</span></span>|<span data-ttu-id="26b0c-108">Inleveranser</span><span class="sxs-lookup"><span data-stu-id="26b0c-108">Receipts</span></span>|<span data-ttu-id="26b0c-109">Artikelinförslar</span><span class="sxs-lookup"><span data-stu-id="26b0c-109">Put-aways</span></span>|<span data-ttu-id="26b0c-110">Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="26b0c-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="26b0c-111">A</span><span class="sxs-lookup"><span data-stu-id="26b0c-111">A</span></span>|<span data-ttu-id="26b0c-112">Bokföra inleverans och lagerinförsel från orderraden</span><span class="sxs-lookup"><span data-stu-id="26b0c-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="26b0c-113">INTER</span><span class="sxs-lookup"><span data-stu-id="26b0c-113">X</span></span>|||<span data-ttu-id="26b0c-114">2</span><span class="sxs-lookup"><span data-stu-id="26b0c-114">2</span></span>|  
|<span data-ttu-id="26b0c-115">B</span><span class="sxs-lookup"><span data-stu-id="26b0c-115">B</span></span>|<span data-ttu-id="26b0c-116">Bokföra inleverans och lagerinförsel från ett lagerinförseldokument</span><span class="sxs-lookup"><span data-stu-id="26b0c-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="26b0c-117">X</span><span class="sxs-lookup"><span data-stu-id="26b0c-117">X</span></span>|<span data-ttu-id="26b0c-118">3</span><span class="sxs-lookup"><span data-stu-id="26b0c-118">3</span></span>|  
|<span data-ttu-id="26b0c-119">L</span><span class="sxs-lookup"><span data-stu-id="26b0c-119">C</span></span>|<span data-ttu-id="26b0c-120">Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument</span><span class="sxs-lookup"><span data-stu-id="26b0c-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="26b0c-121">X</span><span class="sxs-lookup"><span data-stu-id="26b0c-121">X</span></span>||<span data-ttu-id="26b0c-122">6-4-5</span><span class="sxs-lookup"><span data-stu-id="26b0c-122">4/5/6</span></span>|  
|<span data-ttu-id="26b0c-123">D</span><span class="sxs-lookup"><span data-stu-id="26b0c-123">D</span></span>|<span data-ttu-id="26b0c-124">Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument</span><span class="sxs-lookup"><span data-stu-id="26b0c-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="26b0c-125">INTER</span><span class="sxs-lookup"><span data-stu-id="26b0c-125">X</span></span>|<span data-ttu-id="26b0c-126">INTER</span><span class="sxs-lookup"><span data-stu-id="26b0c-126">X</span></span>|<span data-ttu-id="26b0c-127">6-4-5</span><span class="sxs-lookup"><span data-stu-id="26b0c-127">4/5/6</span></span>|  

<span data-ttu-id="26b0c-128">Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="26b0c-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="26b0c-129">Efterföljande genomgången visar metod D i föregående tabellen.</span><span class="sxs-lookup"><span data-stu-id="26b0c-129">The following walkthrough demonstrates method D in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="26b0c-130">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="26b0c-130">About This Walkthrough</span></span>  
<span data-ttu-id="26b0c-131">För avancerad lagerkonfigurationer där lagerstället har konfigurerats att kräva mottagningsbehandling, förutom artikelinförselbehandling, använder du fönstret **Dist.lager inleverans** för att registrera och bokföra kvittot med artiklar för flera ankommande order.</span><span class="sxs-lookup"><span data-stu-id="26b0c-131">In advanced warehouse configurations where your location is set up to require receiving processing in addition to put-away processing, you use the **Warehouse Receipt** window to record and post the receipt of items on multiple inbound orders.</span></span> <span data-ttu-id="26b0c-132">När lagerinleveransen bokförs, skapas en eller flera av artikelinförseldokument för att instruera lagerarbetare att ta det mottagna artikeln och placera dem på avsedda ställen enligt lagerplatsinställning eller i andra lagerplatser. Den specifika placering av artiklarna registreras, när lagerartikelinförseln är registrerade.</span><span class="sxs-lookup"><span data-stu-id="26b0c-132">When the warehouse receipt is posted, one or more warehouse put-away documents are created to instruct warehouse workers to take the received item and place them in designated places according to bin setup or in other bins. The specific placement of the items is recorded when the warehouse put-away is registered.</span></span> <span data-ttu-id="26b0c-133">Det ankommande källdokumentet kan vara en inköpsorder, försäljningsreturorder, ankommande överföringsorder eller montering eller produktionsorder vars utflöde är klart för artikelinförsel.</span><span class="sxs-lookup"><span data-stu-id="26b0c-133">The inbound source document can be a purchase order, sales return order, inbound transfer order, or assembly or production order with output that is ready to be put away.</span></span> <span data-ttu-id="26b0c-134">Om kvittot skapas från en ankommande beställning, kan mer än en ankommande källdokument hämtas för kvittot.</span><span class="sxs-lookup"><span data-stu-id="26b0c-134">If the receipt is created from an inbound order, more than one inbound source document can be retrieved for the receipt.</span></span> <span data-ttu-id="26b0c-135">Genom att använda den här metoden, kan du registrera många artiklar som inlevereras från olika inkommande beställningar med ett kvitto.</span><span class="sxs-lookup"><span data-stu-id="26b0c-135">By using this method you can register many items arriving from different inbound orders with one receipt.</span></span>  

<span data-ttu-id="26b0c-136">I den här genomgången tas följande uppgifter upp.</span><span class="sxs-lookup"><span data-stu-id="26b0c-136">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="26b0c-137">Ställa in VIT lagerställe för mottagning och införsel.</span><span class="sxs-lookup"><span data-stu-id="26b0c-137">Setting up WHITE location for receiving and putting away.</span></span>  
-   <span data-ttu-id="26b0c-138">Skapa och släppa två inköpsorder för fullständig lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="26b0c-138">Creating and releasing two purchase orders for full warehouse handling.</span></span>  
-   <span data-ttu-id="26b0c-139">Skapa och bokför ett distributionslagerinleveransdokument för åtskilliga inköpsorderrader från vissa leverantörer.</span><span class="sxs-lookup"><span data-stu-id="26b0c-139">Creating and posting a warehouse receipt document for multiple purchase order lines from specific vendors.</span></span>  
-   <span data-ttu-id="26b0c-140">Registrering av en lagerartikelinförsel för de inlevererade artiklarna.</span><span class="sxs-lookup"><span data-stu-id="26b0c-140">Registering a warehouse put-away for the received items.</span></span>  

## <a name="roles"></a><span data-ttu-id="26b0c-141">Roller</span><span class="sxs-lookup"><span data-stu-id="26b0c-141">Roles</span></span>  
<span data-ttu-id="26b0c-142">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="26b0c-142">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="26b0c-143">Dist.lagerchef</span><span class="sxs-lookup"><span data-stu-id="26b0c-143">Warehouse Manager</span></span>  
-   <span data-ttu-id="26b0c-144">Inköpsagent</span><span class="sxs-lookup"><span data-stu-id="26b0c-144">Purchasing Agent</span></span>  
-   <span data-ttu-id="26b0c-145">Mottagande personal</span><span class="sxs-lookup"><span data-stu-id="26b0c-145">Receiving Staff</span></span>  
-   <span data-ttu-id="26b0c-146">Lagerarbetare</span><span class="sxs-lookup"><span data-stu-id="26b0c-146">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="26b0c-147">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="26b0c-147">Prerequisites</span></span>  
<span data-ttu-id="26b0c-148">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="26b0c-148">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="26b0c-149">CRONUS Sverige AB installerad</span><span class="sxs-lookup"><span data-stu-id="26b0c-149">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="26b0c-150">Om du vill Ange dig själv som distributionslagerpersonal på lagerstället VIT följer du de här stegen:</span><span class="sxs-lookup"><span data-stu-id="26b0c-150">To make yourself a warehouse employee at WHITE location by following these steps:</span></span>  

1.  <span data-ttu-id="26b0c-151">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Dist.lager personal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26b0c-151">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26b0c-152">Välj fältet **Användar-ID** och välj ditt eget användarkonto i fönstret **Användare**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-152">Choose the **User ID** field, and select your own user account in the **Users** window.</span></span>  
3.  <span data-ttu-id="26b0c-153">Ange WHITE i fältet **Lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-153">In the **Location Code** field, enter WHITE.</span></span>  
4.  <span data-ttu-id="26b0c-154">Välj fältet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-154">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="26b0c-155">Situation</span><span class="sxs-lookup"><span data-stu-id="26b0c-155">Story</span></span>  
<span data-ttu-id="26b0c-156">Ellen, lagerchef på CRONUS skapar två inköpsorder för tillbehörsartiklar från leverantörerna 10000 och 20000 som ska levereras till distributionslagret VIT.</span><span class="sxs-lookup"><span data-stu-id="26b0c-156">Ellen, the warehouse manager at CRONUS International Ltd., creates two purchase orders for accessory items from vendors 10000 and 20000 to be delivered to WHITE warehouse.</span></span> <span data-ttu-id="26b0c-157">När leveranserna inlevereras till lagret använder Sammy, som är ansvarig för att ta emot artiklar från leverantörer 10000 och 20000, ett filter för att skapa inleveransrader för inköpsorder som inlevereras från de två leverantörerna.</span><span class="sxs-lookup"><span data-stu-id="26b0c-157">When the deliveries arrive at the warehouse, Sammy, who is responsible for receiving items from vendors 10000 and 20000, uses a filter to create receipt lines for purchase orders arriving from the two vendors.</span></span> <span data-ttu-id="26b0c-158">Sammy bokför artiklar som inlevererade till lagret i en lagerinleverans och artiklarna blir tillgängliga till försäljning eller andra behov.</span><span class="sxs-lookup"><span data-stu-id="26b0c-158">Sammy posts the items as received into inventory in one warehouse receipt and makes the items available for sale or other demand.</span></span> <span data-ttu-id="26b0c-159">Anders lagerarbetaren, tar artiklarna från mottagande lagerplatsen och för in dem.</span><span class="sxs-lookup"><span data-stu-id="26b0c-159">John, the warehouse worker, takes the items from the receiving bin and puts them away.</span></span> <span data-ttu-id="26b0c-160">Han flyttar alla enheter i sina standardlagerplatser, utom 40 av 100 inlevererade gångjärn, som han flyttar till monteringsavdelningen genom att dela, artikelinförselraden.</span><span class="sxs-lookup"><span data-stu-id="26b0c-160">He puts all units away in their default bins, except 40 out of 100 received hinges that he puts away in the assembly department by splitting the put-away line.</span></span> <span data-ttu-id="26b0c-161">När Anders registrerar artikelinförsel, uppdateras lagerplatsinnehållen, och artiklarna blir tillgängliga för plockning från lagret.</span><span class="sxs-lookup"><span data-stu-id="26b0c-161">When John registers the put-away, the bin contents are updated and the items are made available for picking from the warehouse.</span></span>  

## <a name="reviewing-the-white-location-setup"></a><span data-ttu-id="26b0c-162">Granska konfigurationen av VITA platsen</span><span class="sxs-lookup"><span data-stu-id="26b0c-162">Reviewing the WHITE Location Setup</span></span>  
<span data-ttu-id="26b0c-163">Inställningen av fönstret **Lagerställekort** definierar företagets lagerflöden.</span><span class="sxs-lookup"><span data-stu-id="26b0c-163">The setup of the **Location Card** window defines the company’s warehouse flows.</span></span>  

### <a name="to-review-the-location-setup"></a><span data-ttu-id="26b0c-164">Om du vill granska lagerställekonfigurationen</span><span class="sxs-lookup"><span data-stu-id="26b0c-164">To review the location setup</span></span>  

1.  <span data-ttu-id="26b0c-165">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26b0c-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26b0c-166">Öppna lagerställekortet VIT.</span><span class="sxs-lookup"><span data-stu-id="26b0c-166">Open the WHITE location card.</span></span>  
3.  <span data-ttu-id="26b0c-167">Observera på snabbfliken **Dist.lager** att kryssrutan **dirigerad artikelinförsel och plockning** är markerad.</span><span class="sxs-lookup"><span data-stu-id="26b0c-167">Note on the **Warehouse** FastTab that the **Directed Put-away and Pick** check box is selected.</span></span>  

    <span data-ttu-id="26b0c-168">Det betyder att lagerstället ställts in för den högsta komplexitetsnivån, reflekterat av faktumet att alla kryssrutor för lagerhantering på snabbfliken är markerade.</span><span class="sxs-lookup"><span data-stu-id="26b0c-168">This means that the location is set up for the highest complexity level, reflected by the fact that all warehouse handling check boxes on the FastTab are selected.</span></span>  

4.  <span data-ttu-id="26b0c-169">Observera att på snabbfliken **Lagerplatser** att lagerplatser anges i fälten **Inlevns lagerplatskod** och **Utlevns lagerplatskod**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-169">Note on the **Bins** FastTab that bins are specified in the **Receipt Bin Code** and the **Shipment Bin Code** fields.</span></span>  

<span data-ttu-id="26b0c-170">Det betyder att, när du skapar en distributionslagerinleverans, den här lagerplatskoden kopieras till huvudet på den distributionslagerinleveransdokument som standard, och till raderna i de resulterande distributionslagerartikelinförslar.</span><span class="sxs-lookup"><span data-stu-id="26b0c-170">This means that when you create a warehouse receipt, this bin code is copied to the header of the warehouse receipt document by default and to the lines of the resulting warehouse put-aways.</span></span>  

## <a name="creating-the-purchase-orders"></a><span data-ttu-id="26b0c-171">Skapa inköpsorder</span><span class="sxs-lookup"><span data-stu-id="26b0c-171">Creating the Purchase Orders</span></span>  
<span data-ttu-id="26b0c-172">Inköpsorder är den vanligaste typen för inkommande källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="26b0c-172">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-orders"></a><span data-ttu-id="26b0c-173">Så här Skapa inköpsorder</span><span class="sxs-lookup"><span data-stu-id="26b0c-173">To create the purchase orders</span></span>  

1.  <span data-ttu-id="26b0c-174">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26b0c-174">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26b0c-175">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-175">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="26b0c-176">Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.</span><span class="sxs-lookup"><span data-stu-id="26b0c-176">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="26b0c-177">Artikel</span><span class="sxs-lookup"><span data-stu-id="26b0c-177">Item</span></span>|<span data-ttu-id="26b0c-178">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="26b0c-178">Location code</span></span>|<span data-ttu-id="26b0c-179">Antal</span><span class="sxs-lookup"><span data-stu-id="26b0c-179">Quantity</span></span>|  
    |----------|-------------------|--------------|  
    |<span data-ttu-id="26b0c-180">70200</span><span class="sxs-lookup"><span data-stu-id="26b0c-180">70200</span></span>|<span data-ttu-id="26b0c-181">VIT</span><span class="sxs-lookup"><span data-stu-id="26b0c-181">WHITE</span></span>|<span data-ttu-id="26b0c-182">100 STYCK</span><span class="sxs-lookup"><span data-stu-id="26b0c-182">100 PCS</span></span>|  
    |<span data-ttu-id="26b0c-183">70201</span><span class="sxs-lookup"><span data-stu-id="26b0c-183">70201</span></span>|<span data-ttu-id="26b0c-184">VIT</span><span class="sxs-lookup"><span data-stu-id="26b0c-184">WHITE</span></span>|<span data-ttu-id="26b0c-185">50 STYCK</span><span class="sxs-lookup"><span data-stu-id="26b0c-185">50 PCS</span></span>|  

    <span data-ttu-id="26b0c-186">Fortsätt med att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.</span><span class="sxs-lookup"><span data-stu-id="26b0c-186">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="26b0c-187">Välj åtgärden **Släppa**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-187">Choose the **Release** action.</span></span>  

    <span data-ttu-id="26b0c-188">Fortsätt att skapa den andra inköpsordern.</span><span class="sxs-lookup"><span data-stu-id="26b0c-188">Proceed to create the second purchase order.</span></span>  

5.  <span data-ttu-id="26b0c-189">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-189">Choose the **New** action.</span></span>  
6.  <span data-ttu-id="26b0c-190">Skapa en inköpsorder för leverantör 20000 på arbetsdatumet med följande inköpsorderrader.</span><span class="sxs-lookup"><span data-stu-id="26b0c-190">Create a purchase order for vendor 20000 on the work date with the following purchase order lines.</span></span>  

    |<span data-ttu-id="26b0c-191">Artikel</span><span class="sxs-lookup"><span data-stu-id="26b0c-191">Item</span></span>|<span data-ttu-id="26b0c-192">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="26b0c-192">Location code</span></span>|<span data-ttu-id="26b0c-193">Antal</span><span class="sxs-lookup"><span data-stu-id="26b0c-193">Quantity</span></span>|  
    |----------|-------------------|--------------|  
    |<span data-ttu-id="26b0c-194">70100</span><span class="sxs-lookup"><span data-stu-id="26b0c-194">70100</span></span>|<span data-ttu-id="26b0c-195">VIT</span><span class="sxs-lookup"><span data-stu-id="26b0c-195">WHITE</span></span>|<span data-ttu-id="26b0c-196">10 CAN</span><span class="sxs-lookup"><span data-stu-id="26b0c-196">10 CAN</span></span>|  
    |<span data-ttu-id="26b0c-197">70101</span><span class="sxs-lookup"><span data-stu-id="26b0c-197">70101</span></span>|<span data-ttu-id="26b0c-198">VIT</span><span class="sxs-lookup"><span data-stu-id="26b0c-198">WHITE</span></span>|<span data-ttu-id="26b0c-199">12 CAN</span><span class="sxs-lookup"><span data-stu-id="26b0c-199">12 CAN</span></span>|  

    <span data-ttu-id="26b0c-200">Välj åtgärden **Släppa**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-200">Choose the **Release** action.</span></span>  

    <span data-ttu-id="26b0c-201">Leveranserna av artiklar från leverantörer 10000 och 20000 har anlänt till det VITA lagret, och Sammy börjar behandla inköpsleveranserna.</span><span class="sxs-lookup"><span data-stu-id="26b0c-201">The deliveries of items from vendors 10000 and 20000 have arrived at WHITE warehouse, and Sammy starts to process the purchase receipts.</span></span>  

## <a name="receiving-the-items"></a><span data-ttu-id="26b0c-202">Ta emot artiklarna</span><span class="sxs-lookup"><span data-stu-id="26b0c-202">Receiving the Items</span></span>  
<span data-ttu-id="26b0c-203">I fönstret **Dist.lager inleverans** kan du hantera flera inkommande order för källdokument, t.ex en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="26b0c-203">In the **Warehouse Receipt** window, you can manage multiple inbound orders for source documents, such as a purchase order.</span></span>  

### <a name="to-receive-the-items"></a><span data-ttu-id="26b0c-204">Så här inlevererar du artiklarna</span><span class="sxs-lookup"><span data-stu-id="26b0c-204">To receive the items</span></span>  
1.  <span data-ttu-id="26b0c-205">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Dist.lager inleverans**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26b0c-205">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26b0c-206">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-206">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="26b0c-207">Ange WHITE i fältet **Lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-207">In the **Location Code** field, enter WHITE.</span></span>  
4.  <span data-ttu-id="26b0c-208">Välj åtgärden **Filter för att hämta urspr.dok.**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-208">Choose the **Use Filters to Get Src. Docs.** action.</span></span>  
5.  <span data-ttu-id="26b0c-209">Ange **ACCESSORY** i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-209">In the **Code** field, enter **ACCESSORY**.</span></span>  
6.  <span data-ttu-id="26b0c-210">I fältet **Beskrivning** anger du **Leverantörer 10000 och 20000**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-210">In the **Description** field, enter **Vendors 10000 and 20000**.</span></span>  
7.  <span data-ttu-id="26b0c-211">Välj åtgärden **Ändra**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-211">Choose the **Modify** action.</span></span>  
8.  <span data-ttu-id="26b0c-212">På snabbfliken **inköp** i fältet **Inköpsleverantörsnrfilter** anger du **10000&#124;20000**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-212">On the **Purchase** FastTab, in the **Buy-from Vendor No. Filter** field, enter **10000&#124;20000**.</span></span>  
9. <span data-ttu-id="26b0c-213">Välj åtgärden **Kör**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-213">Choose the **Run** action.</span></span> <span data-ttu-id="26b0c-214">lagerinleveransen är fylld med fyra rader som representerar inköpsorderrader för de angivna leverantörerna.</span><span class="sxs-lookup"><span data-stu-id="26b0c-214">The warehouse receipt is filled with four lines representing purchase order lines for the specified vendors.</span></span> <span data-ttu-id="26b0c-215">Fältet **Ant. att inlevereras** är fyllt, eftersom du inte valde kryssrutan **Fyll inte i ant. att hantera** i fönstret **Filter att hämta ursprungsdok.**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-215">The **Qty. to Receive** field is filled because you did not select the **Do not Fill Qty. to Handle** check box in the **Filters to Get Source Docs.** window.</span></span>  
10. <span data-ttu-id="26b0c-216">Alternativt om du vill använda ett filter på det sätt som beskrivs tidigare i det avsnitt, välj åtgärden **Hämta källdokument** och välj sedan inköpsorder från leverantörerna i fråga.</span><span class="sxs-lookup"><span data-stu-id="26b0c-216">Optionally, if you want to use a filter as described earlier in this section, choose the **Get Source Document** action, and then select purchase orders from the vendors in question.</span></span>  
11. <span data-ttu-id="26b0c-217">Välj åtgärden **Bokföra inleverans** och sedan knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-217">Choose the **Post Receipt** action, and then choose the **Yes** button.</span></span>  

    <span data-ttu-id="26b0c-218">Positiva artikeltransaktioner skapas som återspeglar de bokförda inköpsleveranserna av utrustning från leverantörerna 10000 och 20000, och artiklar är klara att föras in i distributionslagret från den mottagande lagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="26b0c-218">Positive item ledger entries are created reflecting the posted purchase receipts of accessories from vendors 10000 and 20000, and the items are ready to be put away in the warehouse from the receiving bin.</span></span>  

## <a name="putting-the-items-away"></a><span data-ttu-id="26b0c-219">Föra in artiklar i lagret</span><span class="sxs-lookup"><span data-stu-id="26b0c-219">Putting the Items Away</span></span>  
<span data-ttu-id="26b0c-220">I fönstret **Dist.lager artikelinförsel** kan du hantera artikelinförslar för ett specifikt distributionslagerinleveransdokument som täcker flera källdokument.</span><span class="sxs-lookup"><span data-stu-id="26b0c-220">In the **Warehouse Put-away** window, you can manage put-aways for a specific warehouse receipt document covering multiple source documents.</span></span> <span data-ttu-id="26b0c-221">Som alla dist.lageraktivitetdokument representeras varje artikel på dist.lager artikelinförsel av en taganderad och en platsrad.</span><span class="sxs-lookup"><span data-stu-id="26b0c-221">Like all warehouse activity documents, each item on the warehouse put-away is represented by a Take line and a Place line.</span></span> <span data-ttu-id="26b0c-222">I följande procedur är lagerplatskoden på hämtningsraderna standardlagerplatsen för inleveranser vid lagerställe VIT, W-08-0001.</span><span class="sxs-lookup"><span data-stu-id="26b0c-222">In the following procedure, the bin code on the Take lines is the default receiving bin at WHITE location, W-08-0001.</span></span>  

### <a name="to-put-the-items-away"></a><span data-ttu-id="26b0c-223">Så här för du in artiklarna</span><span class="sxs-lookup"><span data-stu-id="26b0c-223">To put the items away</span></span>  
1.  <span data-ttu-id="26b0c-224">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artikelinförslar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26b0c-224">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Put-Aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26b0c-225">Välj det enda distributionslagerinförseldokumentet i listan, och sedan, på **Startsida** fliken, i **Hantera** grupp, välj **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-225">Select the only warehouse put-away document in the list, and then on the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

    <span data-ttu-id="26b0c-226">Distributionslagerinförseldokumentet öppnas med totalt åtta Ta- eller Placerarader för de fyra inköpsorderrader.</span><span class="sxs-lookup"><span data-stu-id="26b0c-226">The warehouse put-away document opens with a total of eight Take or Place lines for the four purchase order lines.</span></span>

    <span data-ttu-id="26b0c-227">Lagerarbetaren har fått informationen att 40 gångjärn behövs i monteringavdelningen, och han fortsätter att dela upp den enda placeraraden för lagerplatsen W-02-0001 i monteringavdelningen där han placerar den delen av de inlevererade gångjärnen.</span><span class="sxs-lookup"><span data-stu-id="26b0c-227">The warehouse worker is told that 40 hinges are needed in the assembly department, and he proceeds to split the single Place line to specify a second Place line for bin W-02-0001 in the assembly department where he places that part of the received hinges.</span></span>  

3.  <span data-ttu-id="26b0c-228">Välj den andra raden i fönstret **Dist.lager artikelinförsel** fönstret, raden Plats för artikel 70200.</span><span class="sxs-lookup"><span data-stu-id="26b0c-228">Select the second line in the **Warehouse Put-away** window, the Place line for item 70200.</span></span>  
4.  <span data-ttu-id="26b0c-229">I fältet **Antal att hantera** ändra värdet från 100 till 60.</span><span class="sxs-lookup"><span data-stu-id="26b0c-229">In the **Qty. to Handle** field, change the value from 100 to 60.</span></span>  
5.  <span data-ttu-id="26b0c-230">På snabbfliken **Rader** väljer du **Funktioner** och sedan **dela rad**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-230">On the **Lines** FastTab, choose **Functions**, and then choose **Split Line**.</span></span> <span data-ttu-id="26b0c-231">En ny rad infogas för artikel 70200 med 40 i fältet **Ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-231">A new line is inserted for item 70200 with 40 in **Qty. to Handle** field.</span></span>  
6.  <span data-ttu-id="26b0c-232">Ange W-02-0001 i fältet **lagerplatskod**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-232">In the **Bin Code** field, enter W-02-0001.</span></span> <span data-ttu-id="26b0c-233">Fältet **Zonkod** fylls i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="26b0c-233">The **Zone Code** field is automatically filled.</span></span>  

    <span data-ttu-id="26b0c-234">Fortsätt med att registrera artikelinförseln.</span><span class="sxs-lookup"><span data-stu-id="26b0c-234">Proceed to register the put-away.</span></span>  

7.  <span data-ttu-id="26b0c-235">Välj åtgärden **Registrera artikelinförsel** och sedan knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="26b0c-235">Choose the **Register Put-Away** action, and then choose the **Yes** button.</span></span>  

    <span data-ttu-id="26b0c-236">Mottagna tillbehör är nu införda i artikelns standardlagerplatser, och 40 gångjärn placeras i monteringavdelningen.</span><span class="sxs-lookup"><span data-stu-id="26b0c-236">The received accessories are now put-away in the items’ default bins, and 40 hinges are placed in the assembly department.</span></span> <span data-ttu-id="26b0c-237">De inlevererade artiklarna är nu tillgängliga för plockning till intern efterfrågan, till exempel monteringsorder eller till extern efterfrågan, till exempel försäljningsutleveranser.</span><span class="sxs-lookup"><span data-stu-id="26b0c-237">The received items are now available for picking to internal demand, such as assembly orders, or to external demand, such as sales shipments.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26b0c-238">Se även</span><span class="sxs-lookup"><span data-stu-id="26b0c-238">See Also</span></span>  
 <span data-ttu-id="26b0c-239">[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="26b0c-239">[Put Items Away with Warehouse Put-aways](warehouse-how-to-put-items-away-with-warehouse-put-aways.md) </span></span>  
 <span data-ttu-id="26b0c-240">[Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="26b0c-240">[Move Items in advanced warehouse configurations](warehouse-how-to-move-items-in-advanced-warehousing.md) </span></span>  
 <span data-ttu-id="26b0c-241">[Designdetaljer: Ankommande distributionslagerflöde](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="26b0c-241">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 <span data-ttu-id="26b0c-242">[Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer](walkthrough-receiving-and-putting-away-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="26b0c-242">[Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md) </span></span>  
 [<span data-ttu-id="26b0c-243">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="26b0c-243">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)
