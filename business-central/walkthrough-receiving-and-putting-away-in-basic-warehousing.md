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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 31ac21dbba331748c9eef7bce199a5709147016b
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554650"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="484e6-103">Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="484e6-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

<span data-ttu-id="484e6-104">**Obs**! i den här genomgången måste utföras på ett demonstrationsföretag, med alternativet **Fullständig utvärdering - fullständig exempeldata** som är tillgängliga i begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="484e6-104">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="484e6-105">Mer information finns i [Skapa en miljö för begränsat lägel](across-how-create-sandbox-environment.md).</span><span class="sxs-lookup"><span data-stu-id="484e6-105">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="484e6-106">I [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.</span><span class="sxs-lookup"><span data-stu-id="484e6-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="484e6-107">Metod</span><span class="sxs-lookup"><span data-stu-id="484e6-107">Method</span></span>|<span data-ttu-id="484e6-108">Ankommande behandling</span><span class="sxs-lookup"><span data-stu-id="484e6-108">Inbound process</span></span>|<span data-ttu-id="484e6-109">Lagerplatser</span><span class="sxs-lookup"><span data-stu-id="484e6-109">Bins</span></span>|<span data-ttu-id="484e6-110">Inleveranser</span><span class="sxs-lookup"><span data-stu-id="484e6-110">Receipts</span></span>|<span data-ttu-id="484e6-111">Artikelinförslar</span><span class="sxs-lookup"><span data-stu-id="484e6-111">Put-aways</span></span>|<span data-ttu-id="484e6-112">Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="484e6-112">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="484e6-113">A</span><span class="sxs-lookup"><span data-stu-id="484e6-113">A</span></span>|<span data-ttu-id="484e6-114">Bokföra inleverans och lagerinförsel från orderraden</span><span class="sxs-lookup"><span data-stu-id="484e6-114">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="484e6-115">INTER</span><span class="sxs-lookup"><span data-stu-id="484e6-115">X</span></span>|||<span data-ttu-id="484e6-116">2</span><span class="sxs-lookup"><span data-stu-id="484e6-116">2</span></span>|  
|<span data-ttu-id="484e6-117">B</span><span class="sxs-lookup"><span data-stu-id="484e6-117">B</span></span>|<span data-ttu-id="484e6-118">Bokföra inleverans och lagerinförsel från ett lagerinförseldokument</span><span class="sxs-lookup"><span data-stu-id="484e6-118">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="484e6-119">X</span><span class="sxs-lookup"><span data-stu-id="484e6-119">X</span></span>|<span data-ttu-id="484e6-120">3</span><span class="sxs-lookup"><span data-stu-id="484e6-120">3</span></span>|  
|<span data-ttu-id="484e6-121">L</span><span class="sxs-lookup"><span data-stu-id="484e6-121">C</span></span>|<span data-ttu-id="484e6-122">Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument</span><span class="sxs-lookup"><span data-stu-id="484e6-122">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="484e6-123">X</span><span class="sxs-lookup"><span data-stu-id="484e6-123">X</span></span>||<span data-ttu-id="484e6-124">6-4-5</span><span class="sxs-lookup"><span data-stu-id="484e6-124">4/5/6</span></span>|  
|<span data-ttu-id="484e6-125">D</span><span class="sxs-lookup"><span data-stu-id="484e6-125">D</span></span>|<span data-ttu-id="484e6-126">Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument</span><span class="sxs-lookup"><span data-stu-id="484e6-126">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="484e6-127">INTER</span><span class="sxs-lookup"><span data-stu-id="484e6-127">X</span></span>|<span data-ttu-id="484e6-128">INTER</span><span class="sxs-lookup"><span data-stu-id="484e6-128">X</span></span>|<span data-ttu-id="484e6-129">6-4-5</span><span class="sxs-lookup"><span data-stu-id="484e6-129">4/5/6</span></span>|  

<span data-ttu-id="484e6-130">Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="484e6-130">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="484e6-131">Efterföljande genomgången visar metod B i föregående tabellen.</span><span class="sxs-lookup"><span data-stu-id="484e6-131">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="484e6-132">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="484e6-132">About This Walkthrough</span></span>  
<span data-ttu-id="484e6-133">För grundläggande lagerkonfiguration där lagerstället har konfigurerats att kräva artikelinförselbearbetning men inte mottagningsbearbetning, använder du sidan **Lagerinförsel** för att registrera och bokföra artikelinförsel- och mottagningsinformation för dina ankommande källdokument.</span><span class="sxs-lookup"><span data-stu-id="484e6-133">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="484e6-134">Det ankommande källdokumentet kan vara en inköpsorder, försäljningsreturorder, ankommande överföringsorder eller produktionsorder vars utflöde är klart för artikelinförsel.</span><span class="sxs-lookup"><span data-stu-id="484e6-134">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="484e6-135">Även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.</span><span class="sxs-lookup"><span data-stu-id="484e6-135">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="484e6-136">I den här genomgången tas följande uppgifter upp.</span><span class="sxs-lookup"><span data-stu-id="484e6-136">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="484e6-137">Lägger upp lagerstället SILVER för lagerinförsel.</span><span class="sxs-lookup"><span data-stu-id="484e6-137">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="484e6-138">Lägger upp lagerstället SILVER för lagerplatshantering.</span><span class="sxs-lookup"><span data-stu-id="484e6-138">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="484e6-139">Definierar en standardlagerplats för artikeln LS-81.</span><span class="sxs-lookup"><span data-stu-id="484e6-139">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="484e6-140">(LS-75 redan inställd i CRONUS.)</span><span class="sxs-lookup"><span data-stu-id="484e6-140">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="484e6-141">Skapa en inköpsorder för leverantör 10000 på 40 högtalare.</span><span class="sxs-lookup"><span data-stu-id="484e6-141">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="484e6-142">Kontrollera att införsel-lagerplatserna förinställs av inställningarna.</span><span class="sxs-lookup"><span data-stu-id="484e6-142">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="484e6-143">Släppa inköpsordern för lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="484e6-143">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="484e6-144">Skapa en lagerinförsel som baseras på ett släppt källdokument.</span><span class="sxs-lookup"><span data-stu-id="484e6-144">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="484e6-145">Kontrollera att införsel-lagerplatserna hämtas från inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="484e6-145">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="484e6-146">Registrering av lagerrörelsen till lagret och samtidigt bokföra inköpsinleveransen för källinköpsorder.</span><span class="sxs-lookup"><span data-stu-id="484e6-146">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="484e6-147">Roller</span><span class="sxs-lookup"><span data-stu-id="484e6-147">Roles</span></span>  
<span data-ttu-id="484e6-148">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="484e6-148">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="484e6-149">Dist.lagerchef</span><span class="sxs-lookup"><span data-stu-id="484e6-149">Warehouse Manager</span></span>  
-   <span data-ttu-id="484e6-150">Inköpsagent</span><span class="sxs-lookup"><span data-stu-id="484e6-150">Purchasing Agent</span></span>  
-   <span data-ttu-id="484e6-151">Lagerarbetare</span><span class="sxs-lookup"><span data-stu-id="484e6-151">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="484e6-152">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="484e6-152">Prerequisites</span></span>  
<span data-ttu-id="484e6-153">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="484e6-153">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="484e6-154">CRONUS Sverige Ab installerad.</span><span class="sxs-lookup"><span data-stu-id="484e6-154">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="484e6-155">Gör dig själv till distributionslageranvändare på lagerstället SILVER med följande steg:</span><span class="sxs-lookup"><span data-stu-id="484e6-155">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="484e6-156">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Dist.lager personal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="484e6-156">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="484e6-157">Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.</span><span class="sxs-lookup"><span data-stu-id="484e6-157">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="484e6-158">Ange SILVER i fältet **Lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="484e6-158">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="484e6-159">Välj fältet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="484e6-159">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="484e6-160">Situation</span><span class="sxs-lookup"><span data-stu-id="484e6-160">Story</span></span>  
<span data-ttu-id="484e6-161">Alicia, inköpsagenten i CRONUS, skapar en inköpsorder för 10 enheter av artikeln LS-75 och 30 enheter av artikeln LS-81 från leverantör 10000 som ska levereras till distributionslagret SILVER.</span><span class="sxs-lookup"><span data-stu-id="484e6-161">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="484e6-162">När leveransen inlevereras till lagret placerar Anders, lagerarbetaren, artiklarna i standardlagerplatser som definieras för artiklarna.</span><span class="sxs-lookup"><span data-stu-id="484e6-162">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="484e6-163">När Anders bokför artikelinförseln, bokförs artiklarna som inlevererade till lagret och som tillgängligt för försäljning eller andra behov.</span><span class="sxs-lookup"><span data-stu-id="484e6-163">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="484e6-164">Lägger upp lagerstället</span><span class="sxs-lookup"><span data-stu-id="484e6-164">Setting up the Location</span></span>  
 <span data-ttu-id="484e6-165">Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.</span><span class="sxs-lookup"><span data-stu-id="484e6-165">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="484e6-166">Så här lägger du upp lagerställen</span><span class="sxs-lookup"><span data-stu-id="484e6-166">To set up the location</span></span>  

1.  <span data-ttu-id="484e6-167">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Platser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="484e6-167">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="484e6-168">Öppna lagerställekortet SILVER.</span><span class="sxs-lookup"><span data-stu-id="484e6-168">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="484e6-169">Markera kryssrutan **Begär artikelinförsel**.</span><span class="sxs-lookup"><span data-stu-id="484e6-169">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="484e6-170">Fortsätt med att lägga upp en standardlagerplats för de två artikelnumren för att styra var de ska föras in.</span><span class="sxs-lookup"><span data-stu-id="484e6-170">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="484e6-171">Välj åtgärden **Lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="484e6-171">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="484e6-172">Markera den första raden för lagerplatsinnehållet S-01-0001, och välj sedan åtgärden **innehåll**.</span><span class="sxs-lookup"><span data-stu-id="484e6-172">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="484e6-173">Lägg märke till att på sidan **Lagerplatsinnehåll** har artikeln LS-75 redan lagts upp som innehåll i lagerplatsen S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="484e6-173">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="484e6-174">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="484e6-174">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="484e6-175">Markera fälten **Fast** och **Standard**.</span><span class="sxs-lookup"><span data-stu-id="484e6-175">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="484e6-176">I fältet **Verifikationsnr.** anger du LS-81.</span><span class="sxs-lookup"><span data-stu-id="484e6-176">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="484e6-177">Skapar inköpsordern</span><span class="sxs-lookup"><span data-stu-id="484e6-177">Creating the Purchase Order</span></span>  
<span data-ttu-id="484e6-178">Inköpsorder är den vanligaste typen för inkommande källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="484e6-178">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="484e6-179">Skapa inköpsordern</span><span class="sxs-lookup"><span data-stu-id="484e6-179">To create the purchase order</span></span>  

1.  <span data-ttu-id="484e6-180">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="484e6-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="484e6-181">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="484e6-181">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="484e6-182">Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.</span><span class="sxs-lookup"><span data-stu-id="484e6-182">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="484e6-183">Artikel</span><span class="sxs-lookup"><span data-stu-id="484e6-183">Item</span></span>|<span data-ttu-id="484e6-184">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="484e6-184">Location code</span></span>|<span data-ttu-id="484e6-185">Lagerplatskod</span><span class="sxs-lookup"><span data-stu-id="484e6-185">Bin code</span></span>|<span data-ttu-id="484e6-186">Antal</span><span class="sxs-lookup"><span data-stu-id="484e6-186">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="484e6-187">LS_75</span><span class="sxs-lookup"><span data-stu-id="484e6-187">LS_75</span></span>|<span data-ttu-id="484e6-188">SILVER</span><span class="sxs-lookup"><span data-stu-id="484e6-188">SILVER</span></span>|<span data-ttu-id="484e6-189">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="484e6-189">S-01-0001</span></span>|<span data-ttu-id="484e6-190">10</span><span class="sxs-lookup"><span data-stu-id="484e6-190">10</span></span>|  
    |<span data-ttu-id="484e6-191">LS-81</span><span class="sxs-lookup"><span data-stu-id="484e6-191">LS-81</span></span>|<span data-ttu-id="484e6-192">SILVER</span><span class="sxs-lookup"><span data-stu-id="484e6-192">SILVER</span></span>|<span data-ttu-id="484e6-193">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="484e6-193">S-01-0001</span></span>|<span data-ttu-id="484e6-194">30</span><span class="sxs-lookup"><span data-stu-id="484e6-194">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="484e6-195">Lagerplatskod anges automatiskt i överensstämmelse med inställningar som du har utfört i avsnittet ”Skapa lagerplatsen”.</span><span class="sxs-lookup"><span data-stu-id="484e6-195">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="484e6-196">Fortsätt med att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.</span><span class="sxs-lookup"><span data-stu-id="484e6-196">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="484e6-197">Välj åtgärden **Släppa**.</span><span class="sxs-lookup"><span data-stu-id="484e6-197">Choose the **Release** action.</span></span>  

    <span data-ttu-id="484e6-198">Leverans av högtalare från leverantör 10000 har anlänt till SILVERLAGRET, och Anders fortsätter att föra in dem.</span><span class="sxs-lookup"><span data-stu-id="484e6-198">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="484e6-199">Ta emot och föra in artiklar i lagret</span><span class="sxs-lookup"><span data-stu-id="484e6-199">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="484e6-200">På sidan **Lagerinförsel** kan du hantera alla ingående distributionslageraktiviteter för ett särskilt källdokument, t.ex en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="484e6-200">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="484e6-201">Så här tar du emot och för in artiklar</span><span class="sxs-lookup"><span data-stu-id="484e6-201">To receive and put the items away</span></span>  

1.  <span data-ttu-id="484e6-202">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerinförslar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="484e6-202">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="484e6-203">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="484e6-203">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="484e6-204">Välj fältet **Källdokument** och sedan **Inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="484e6-204">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="484e6-205">Välj fältet **Källnr.** markera raden för köpet från leverantör 10000 och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="484e6-205">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="484e6-206">Välj alternativt åtgärden **Hämta källdokument** och välj sedan inköpsordern.</span><span class="sxs-lookup"><span data-stu-id="484e6-206">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="484e6-207">Välj åtgärden **Fyll i auto. ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="484e6-207">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="484e6-208">Alternativt, ange 10 respektive 30 i fältet **Ant. att hantera** på de två lagerinförselraderna.</span><span class="sxs-lookup"><span data-stu-id="484e6-208">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="484e6-209">Välj åtgärden **bokför**, välj åtgärden **inleverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="484e6-209">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="484e6-210">De 40 högtalarna har nu registrerats som införda på lagerplatser S-01-0001 och en positiv artikeltransaktion skapas som återspeglar den bokförda inköpsinleveransraden.</span><span class="sxs-lookup"><span data-stu-id="484e6-210">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="484e6-211">Se även</span><span class="sxs-lookup"><span data-stu-id="484e6-211">See Also</span></span>  
 <span data-ttu-id="484e6-212">[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="484e6-212">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="484e6-213">[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="484e6-213">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="484e6-214">[Flytta komponenter till ett verksamhetsområde i en grundläggande lagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="484e6-214">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="484e6-215">[Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="484e6-215">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="484e6-216">[Flytta artiklar ad hoc i grundläggande lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="484e6-216">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="484e6-217">[Designdetaljer: Ankommande distributionslagerflöde](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="484e6-217">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="484e6-218">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="484e6-218">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="484e6-219">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="484e6-219">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
