---
title: 'Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer | Microsoft Docs'
description: I Business Central kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktioner beroende på lagerkomplexitetsnivå.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b119883babf1f44ff78482c4849faff72c1ec257
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918444"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="5e9f0-103">Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="5e9f0-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

<span data-ttu-id="5e9f0-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="5e9f0-105">Metod</span><span class="sxs-lookup"><span data-stu-id="5e9f0-105">Method</span></span>|<span data-ttu-id="5e9f0-106">Ankommande behandling</span><span class="sxs-lookup"><span data-stu-id="5e9f0-106">Inbound process</span></span>|<span data-ttu-id="5e9f0-107">Lagerplatser</span><span class="sxs-lookup"><span data-stu-id="5e9f0-107">Bins</span></span>|<span data-ttu-id="5e9f0-108">Inleveranser</span><span class="sxs-lookup"><span data-stu-id="5e9f0-108">Receipts</span></span>|<span data-ttu-id="5e9f0-109">Artikelinförslar</span><span class="sxs-lookup"><span data-stu-id="5e9f0-109">Put-aways</span></span>|<span data-ttu-id="5e9f0-110">Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="5e9f0-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="5e9f0-111">A</span><span class="sxs-lookup"><span data-stu-id="5e9f0-111">A</span></span>|<span data-ttu-id="5e9f0-112">Bokföra inleverans och lagerinförsel från orderraden</span><span class="sxs-lookup"><span data-stu-id="5e9f0-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="5e9f0-113">INTER</span><span class="sxs-lookup"><span data-stu-id="5e9f0-113">X</span></span>|||<span data-ttu-id="5e9f0-114">2</span><span class="sxs-lookup"><span data-stu-id="5e9f0-114">2</span></span>|  
|<span data-ttu-id="5e9f0-115">B</span><span class="sxs-lookup"><span data-stu-id="5e9f0-115">B</span></span>|<span data-ttu-id="5e9f0-116">Bokföra inleverans och lagerinförsel från ett lagerinförseldokument</span><span class="sxs-lookup"><span data-stu-id="5e9f0-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="5e9f0-117">X</span><span class="sxs-lookup"><span data-stu-id="5e9f0-117">X</span></span>|<span data-ttu-id="5e9f0-118">3</span><span class="sxs-lookup"><span data-stu-id="5e9f0-118">3</span></span>|  
|<span data-ttu-id="5e9f0-119">L</span><span class="sxs-lookup"><span data-stu-id="5e9f0-119">C</span></span>|<span data-ttu-id="5e9f0-120">Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument</span><span class="sxs-lookup"><span data-stu-id="5e9f0-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="5e9f0-121">X</span><span class="sxs-lookup"><span data-stu-id="5e9f0-121">X</span></span>||<span data-ttu-id="5e9f0-122">6-4-5</span><span class="sxs-lookup"><span data-stu-id="5e9f0-122">4/5/6</span></span>|  
|<span data-ttu-id="5e9f0-123">D</span><span class="sxs-lookup"><span data-stu-id="5e9f0-123">D</span></span>|<span data-ttu-id="5e9f0-124">Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument</span><span class="sxs-lookup"><span data-stu-id="5e9f0-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="5e9f0-125">INTER</span><span class="sxs-lookup"><span data-stu-id="5e9f0-125">X</span></span>|<span data-ttu-id="5e9f0-126">INTER</span><span class="sxs-lookup"><span data-stu-id="5e9f0-126">X</span></span>|<span data-ttu-id="5e9f0-127">6-4-5</span><span class="sxs-lookup"><span data-stu-id="5e9f0-127">4/5/6</span></span>|  

<span data-ttu-id="5e9f0-128">Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="5e9f0-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="5e9f0-129">Efterföljande genomgången visar metod B i föregående tabellen.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="5e9f0-130">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="5e9f0-130">About This Walkthrough</span></span>  
<span data-ttu-id="5e9f0-131">För grundläggande lagerkonfiguration där lagerstället har konfigurerats att kräva artikelinförselbearbetning men inte mottagningsbearbetning, använder du sidan **Lagerinförsel** för att registrera och bokföra artikelinförsel- och mottagningsinformation för dina ankommande källdokument.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="5e9f0-132">Det ankommande källdokumentet kan vara en inköpsorder, försäljningsreturorder, ankommande överföringsorder eller produktionsorder vars utflöde är klart för artikelinförsel.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="5e9f0-133">Även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="5e9f0-134">I den här genomgången tas följande uppgifter upp.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="5e9f0-135">Lägger upp lagerstället SILVER för lagerinförsel.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="5e9f0-136">Lägger upp lagerstället SILVER för lagerplatshantering.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="5e9f0-137">Definierar en standardlagerplats för artikeln LS-81.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="5e9f0-138">(LS-75 redan inställd i CRONUS.)</span><span class="sxs-lookup"><span data-stu-id="5e9f0-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="5e9f0-139">Skapa en inköpsorder för leverantör 10000 på 40 högtalare.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="5e9f0-140">Kontrollera att införsel-lagerplatserna förinställs av inställningarna.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="5e9f0-141">Släppa inköpsordern för lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="5e9f0-142">Skapa en lagerinförsel som baseras på ett släppt källdokument.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="5e9f0-143">Kontrollera att införsel-lagerplatserna hämtas från inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="5e9f0-144">Registrering av lagerrörelsen till lagret och samtidigt bokföra inköpsinleveransen för källinköpsorder.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="5e9f0-145">Roller</span><span class="sxs-lookup"><span data-stu-id="5e9f0-145">Roles</span></span>  
<span data-ttu-id="5e9f0-146">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="5e9f0-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="5e9f0-147">Dist.lagerchef</span><span class="sxs-lookup"><span data-stu-id="5e9f0-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="5e9f0-148">Inköpsagent</span><span class="sxs-lookup"><span data-stu-id="5e9f0-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="5e9f0-149">Lagerarbetare</span><span class="sxs-lookup"><span data-stu-id="5e9f0-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="5e9f0-150">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="5e9f0-150">Prerequisites</span></span>  
<span data-ttu-id="5e9f0-151">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="5e9f0-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="5e9f0-152">CRONUS Sverige Ab installerad.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="5e9f0-153">Gör dig själv till distributionslageranvändare på lagerstället SILVER med följande steg:</span><span class="sxs-lookup"><span data-stu-id="5e9f0-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="5e9f0-154">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="5e9f0-155">Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-155">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="5e9f0-156">Ange SILVER i fältet **Lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="5e9f0-157">Välj fältet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="5e9f0-158">Situation</span><span class="sxs-lookup"><span data-stu-id="5e9f0-158">Story</span></span>  
<span data-ttu-id="5e9f0-159">Alicia, inköpsagenten i CRONUS, skapar en inköpsorder för 10 enheter av artikeln LS-75 och 30 enheter av artikeln LS-81 från leverantör 10000 som ska levereras till distributionslagret SILVER.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="5e9f0-160">När leveransen inlevereras till lagret placerar Anders, lagerarbetaren, artiklarna i standardlagerplatser som definieras för artiklarna.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="5e9f0-161">När Anders bokför artikelinförseln, bokförs artiklarna som inlevererade till lagret och som tillgängligt för försäljning eller andra behov.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="5e9f0-162">Lägger upp lagerstället</span><span class="sxs-lookup"><span data-stu-id="5e9f0-162">Setting up the Location</span></span>  
 <span data-ttu-id="5e9f0-163">Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-163">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="5e9f0-164">Så här lägger du upp lagerställen</span><span class="sxs-lookup"><span data-stu-id="5e9f0-164">To set up the location</span></span>  

1.  <span data-ttu-id="5e9f0-165">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-165">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e9f0-166">Öppna lagerställekortet SILVER.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="5e9f0-167">Markera kryssrutan **Begär artikelinförsel**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="5e9f0-168">Fortsätt med att lägga upp en standardlagerplats för de två artikelnumren för att styra var de ska föras in.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="5e9f0-169">Välj åtgärden **Lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="5e9f0-170">Markera den första raden för lagerplatsinnehållet S-01-0001, och välj sedan åtgärden **innehåll**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="5e9f0-171">Lägg märke till att på sidan **Lagerplatsinnehåll** har artikeln LS-75 redan lagts upp som innehåll i lagerplatsen S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-171">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="5e9f0-172">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="5e9f0-173">Markera fälten **Fast** och **Standard**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="5e9f0-174">I fältet **Verifikationsnr.** anger du LS-81.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="5e9f0-175">Skapar inköpsordern</span><span class="sxs-lookup"><span data-stu-id="5e9f0-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="5e9f0-176">Inköpsorder är den vanligaste typen för inkommande källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="5e9f0-177">Skapa inköpsordern</span><span class="sxs-lookup"><span data-stu-id="5e9f0-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="5e9f0-178">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-178">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e9f0-179">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5e9f0-180">Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="5e9f0-181">Artikel</span><span class="sxs-lookup"><span data-stu-id="5e9f0-181">Item</span></span>|<span data-ttu-id="5e9f0-182">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="5e9f0-182">Location code</span></span>|<span data-ttu-id="5e9f0-183">Lagerplatskod</span><span class="sxs-lookup"><span data-stu-id="5e9f0-183">Bin code</span></span>|<span data-ttu-id="5e9f0-184">Antal</span><span class="sxs-lookup"><span data-stu-id="5e9f0-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="5e9f0-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="5e9f0-185">LS_75</span></span>|<span data-ttu-id="5e9f0-186">SILVER</span><span class="sxs-lookup"><span data-stu-id="5e9f0-186">SILVER</span></span>|<span data-ttu-id="5e9f0-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="5e9f0-187">S-01-0001</span></span>|<span data-ttu-id="5e9f0-188">10</span><span class="sxs-lookup"><span data-stu-id="5e9f0-188">10</span></span>|  
    |<span data-ttu-id="5e9f0-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="5e9f0-189">LS-81</span></span>|<span data-ttu-id="5e9f0-190">SILVER</span><span class="sxs-lookup"><span data-stu-id="5e9f0-190">SILVER</span></span>|<span data-ttu-id="5e9f0-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="5e9f0-191">S-01-0001</span></span>|<span data-ttu-id="5e9f0-192">30</span><span class="sxs-lookup"><span data-stu-id="5e9f0-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="5e9f0-193">Lagerplatskod anges automatiskt i överensstämmelse med inställningar som du har utfört i avsnittet ”Skapa lagerplatsen”.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="5e9f0-194">Fortsätt med att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="5e9f0-195">Välj åtgärden **Släppa**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="5e9f0-196">Leverans av högtalare från leverantör 10000 har anlänt till SILVERLAGRET, och Anders fortsätter att föra in dem.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="5e9f0-197">Ta emot och föra in artiklar i lagret</span><span class="sxs-lookup"><span data-stu-id="5e9f0-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="5e9f0-198">På sidan **Lagerinförsel** kan du hantera alla ingående distributionslageraktiviteter för ett särskilt källdokument, t.ex en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-198">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="5e9f0-199">Så här tar du emot och för in artiklar</span><span class="sxs-lookup"><span data-stu-id="5e9f0-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="5e9f0-200">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lager, artikelinförsel** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-200">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e9f0-201">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5e9f0-202">Välj fältet **Källdokument** och sedan **Inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="5e9f0-203">Välj fältet **Källnr.** markera raden för köpet från leverantör 10000 och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="5e9f0-204">Välj alternativt åtgärden **Hämta källdokument** och välj sedan inköpsordern.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-204">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="5e9f0-205">Välj åtgärden **Fyll i auto. ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="5e9f0-206">Alternativt, ange 10 respektive 30 i fältet **Ant. att hantera** på de två lagerinförselraderna.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="5e9f0-207">Välj åtgärden **bokför**, välj åtgärden **inleverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="5e9f0-208">De 40 högtalarna har nu registrerats som införda på lagerplatser S-01-0001 och en positiv artikeltransaktion skapas som återspeglar den bokförda inköpsinleveransraden.</span><span class="sxs-lookup"><span data-stu-id="5e9f0-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e9f0-209">Se även</span><span class="sxs-lookup"><span data-stu-id="5e9f0-209">See Also</span></span>  
 <span data-ttu-id="5e9f0-210">[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="5e9f0-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="5e9f0-211">[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="5e9f0-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="5e9f0-212">[Flytta komponenter till ett verksamhetsområde i en grundläggande lagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="5e9f0-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="5e9f0-213">[Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="5e9f0-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="5e9f0-214">[Flytta artiklar ad hoc i grundläggande lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="5e9f0-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="5e9f0-215">[Designdetaljer: Ankommande distributionslagerflöde](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="5e9f0-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="5e9f0-216">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="5e9f0-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="5e9f0-217">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e9f0-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
