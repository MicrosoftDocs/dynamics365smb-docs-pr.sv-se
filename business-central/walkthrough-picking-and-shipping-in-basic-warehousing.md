---
title: Plockning och leverans i grundläggande lagerkonfiguration | Microsoft Docs
description: I Business Central kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktioner beroende på lagerkomplexitetsnivå.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96a837eaded2cf9be5e1fabb4d7f81415a171f96
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393455"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="8f0c4-103">Genomgång: Plockning och leverans i grundläggande lagerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8f0c4-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="8f0c4-104">I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="8f0c4-105">Metod</span><span class="sxs-lookup"><span data-stu-id="8f0c4-105">Method</span></span>|<span data-ttu-id="8f0c4-106">inkommande behandling</span><span class="sxs-lookup"><span data-stu-id="8f0c4-106">Inbound process</span></span>|<span data-ttu-id="8f0c4-107">Lagerställen</span><span class="sxs-lookup"><span data-stu-id="8f0c4-107">Bins</span></span>|<span data-ttu-id="8f0c4-108">Plockningar</span><span class="sxs-lookup"><span data-stu-id="8f0c4-108">Picks</span></span>|<span data-ttu-id="8f0c4-109">Utleveranser</span><span class="sxs-lookup"><span data-stu-id="8f0c4-109">Shipments</span></span>|<span data-ttu-id="8f0c4-110">Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="8f0c4-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="8f0c4-111">A</span><span class="sxs-lookup"><span data-stu-id="8f0c4-111">A</span></span>|<span data-ttu-id="8f0c4-112">Bokföra plockning och utleverans från orderraden</span><span class="sxs-lookup"><span data-stu-id="8f0c4-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="8f0c4-113">INTER</span><span class="sxs-lookup"><span data-stu-id="8f0c4-113">X</span></span>|||<span data-ttu-id="8f0c4-114">2</span><span class="sxs-lookup"><span data-stu-id="8f0c4-114">2</span></span>|  
|<span data-ttu-id="8f0c4-115">B</span><span class="sxs-lookup"><span data-stu-id="8f0c4-115">B</span></span>|<span data-ttu-id="8f0c4-116">Bokföra plockning och utleverans från ett lagerplockningdokument</span><span class="sxs-lookup"><span data-stu-id="8f0c4-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="8f0c4-117">X</span><span class="sxs-lookup"><span data-stu-id="8f0c4-117">X</span></span>||<span data-ttu-id="8f0c4-118">3</span><span class="sxs-lookup"><span data-stu-id="8f0c4-118">3</span></span>|  
|<span data-ttu-id="8f0c4-119">L</span><span class="sxs-lookup"><span data-stu-id="8f0c4-119">C</span></span>|<span data-ttu-id="8f0c4-120">Bokföra plockning och utleverans från ett distributionslagerutleveransdokument</span><span class="sxs-lookup"><span data-stu-id="8f0c4-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="8f0c4-121">X</span><span class="sxs-lookup"><span data-stu-id="8f0c4-121">X</span></span>|<span data-ttu-id="8f0c4-122">6-4-5</span><span class="sxs-lookup"><span data-stu-id="8f0c4-122">4/5/6</span></span>|  
|<span data-ttu-id="8f0c4-123">D</span><span class="sxs-lookup"><span data-stu-id="8f0c4-123">D</span></span>|<span data-ttu-id="8f0c4-124">Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument</span><span class="sxs-lookup"><span data-stu-id="8f0c4-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="8f0c4-125">INTER</span><span class="sxs-lookup"><span data-stu-id="8f0c4-125">X</span></span>|<span data-ttu-id="8f0c4-126">INTER</span><span class="sxs-lookup"><span data-stu-id="8f0c4-126">X</span></span>|<span data-ttu-id="8f0c4-127">6-4-5</span><span class="sxs-lookup"><span data-stu-id="8f0c4-127">4/5/6</span></span>|  

<span data-ttu-id="8f0c4-128">Mer information finns i [Designdetaljer: utgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="8f0c4-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="8f0c4-129">Efterföljande genomgången visar metod B i föregående tabellen.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a><span data-ttu-id="8f0c4-130">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="8f0c4-130">About This Walkthrough</span></span>

<span data-ttu-id="8f0c4-131">För grundläggande lagerkonfigurationer där lagerstället har konfigurerats att kräva plockningsbearbetning men inte leveransbearbetning, använder du sidan **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina utgående källdokument.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="8f0c4-132">Det utgående källdokumentet kan vara en försäljningsorder, inköpsreturorder, utgående överföringsorder eller produktionsorder med komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="8f0c4-133">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="8f0c4-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="8f0c4-134">Lägger upp lagerstället SILVER för lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="8f0c4-135">Skapa en försäljningsorder för kund 10000 på 30 högtalare.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="8f0c4-136">Släppa försäljningsordern för lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="8f0c4-137">Skapa en lagerplockning som baseras på ett släppt källdokument.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="8f0c4-138">Registrering av lagerrörelsen från lagret och samtidigt bokföra försäljningsutleveransen för källförsäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a><span data-ttu-id="8f0c4-139">Roller</span><span class="sxs-lookup"><span data-stu-id="8f0c4-139">Roles</span></span>

<span data-ttu-id="8f0c4-140">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:</span><span class="sxs-lookup"><span data-stu-id="8f0c4-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="8f0c4-141">Dist.lagerchef</span><span class="sxs-lookup"><span data-stu-id="8f0c4-141">Warehouse Manager</span></span>  
- <span data-ttu-id="8f0c4-142">Orderhandläggare</span><span class="sxs-lookup"><span data-stu-id="8f0c4-142">Order Processor</span></span>  
- <span data-ttu-id="8f0c4-143">Lagerarbetare</span><span class="sxs-lookup"><span data-stu-id="8f0c4-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="8f0c4-144">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="8f0c4-144">Prerequisites</span></span>

<span data-ttu-id="8f0c4-145">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="8f0c4-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="8f0c4-146">För [!INCLUDE[prod_short](includes/prod_short.md)] online är detta ett företag som bygger på den **Avancerade utvärderingen av utvärdering – fullständiga exempeldata** i en begränsad miljö.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-146">For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="8f0c4-147">För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, CRONUS International Ltd. installerat.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-147">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="8f0c4-148">Gör dig själv till distributionslageranvändare på lagerstället SILVER med följande steg:</span><span class="sxs-lookup"><span data-stu-id="8f0c4-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="8f0c4-149">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="8f0c4-150">Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="8f0c4-151">Ange SILVER i fältet **Lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="8f0c4-152">Välj fältet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="8f0c4-153">Gör artikeln LS-81 tillgänglig på platsen SILVER, genom att följa nedanstående steg:</span><span class="sxs-lookup"><span data-stu-id="8f0c4-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="8f0c4-154">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager artikeljournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="8f0c4-155">Öppna standardjournalen och skapa sedan två artikeljournalrader med följande information om arbetsdatumet (23 januari).</span><span class="sxs-lookup"><span data-stu-id="8f0c4-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="8f0c4-156">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="8f0c4-156">Entry Type</span></span>|<span data-ttu-id="8f0c4-157">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="8f0c4-157">Item Number</span></span>|<span data-ttu-id="8f0c4-158">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="8f0c4-158">Location Code</span></span>|<span data-ttu-id="8f0c4-159">Lagerställeskod</span><span class="sxs-lookup"><span data-stu-id="8f0c4-159">Bin Code</span></span>|<span data-ttu-id="8f0c4-160">Antal</span><span class="sxs-lookup"><span data-stu-id="8f0c4-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="8f0c4-161">Positiv antalsjust.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-161">Positive Adjmt.</span></span>|<span data-ttu-id="8f0c4-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="8f0c4-162">LS-81</span></span>|<span data-ttu-id="8f0c4-163">SILVER</span><span class="sxs-lookup"><span data-stu-id="8f0c4-163">SILVER</span></span>|<span data-ttu-id="8f0c4-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="8f0c4-164">S-01-0001</span></span>|<span data-ttu-id="8f0c4-165">20</span><span class="sxs-lookup"><span data-stu-id="8f0c4-165">20</span></span>|  
        |<span data-ttu-id="8f0c4-166">Positiv antalsjust.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-166">Positive Adjmt.</span></span>|<span data-ttu-id="8f0c4-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="8f0c4-167">LS-81</span></span>|<span data-ttu-id="8f0c4-168">SILVER</span><span class="sxs-lookup"><span data-stu-id="8f0c4-168">SILVER</span></span>|<span data-ttu-id="8f0c4-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="8f0c4-169">S-01-0002</span></span>|<span data-ttu-id="8f0c4-170">20</span><span class="sxs-lookup"><span data-stu-id="8f0c4-170">20</span></span>|  

  3. <span data-ttu-id="8f0c4-171">Välj åtgärden **Bokföra** och sedan knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="8f0c4-172">Situation</span><span class="sxs-lookup"><span data-stu-id="8f0c4-172">Story</span></span>

<span data-ttu-id="8f0c4-173">Ellen, lagerchefen i CRONUS, ställer in lagret SILVER för grundläggande plockning där lagerarbetare behandlar utgående beställningar var för sig.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="8f0c4-174">Susan, orderhandläggaren, skapar en försäljningsorder för 30 enheter av artikeln LS-81 att levereras till kund 10000 från SILVERLAGRET.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="8f0c4-175">Anders, lagerarbetaren, måste kontrollera att leveransen förbereds och levereras till kunden.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="8f0c4-176">Anders hanterar alla uppgifter som är involverade på sidan **Lagerplockning** som automatiskt pekar på lagerställena där LS-81 lagras.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="8f0c4-177">Lägger upp lagerstället</span><span class="sxs-lookup"><span data-stu-id="8f0c4-177">Setting Up the Location</span></span>

<span data-ttu-id="8f0c4-178">Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-178">The setup of the **Location Card** page defines the company's warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="8f0c4-179">Så här lägger du upp lagerställen</span><span class="sxs-lookup"><span data-stu-id="8f0c4-179">To set up the location</span></span>

1. <span data-ttu-id="8f0c4-180">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f0c4-181">Öppna lagerställekortet SILVER.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="8f0c4-182">Markera fältet **Kräver plockning** på kryssrutan **Dist.lager**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="8f0c4-183">Skapar försäljningsreturordern</span><span class="sxs-lookup"><span data-stu-id="8f0c4-183">Creating the Sales Order</span></span>

<span data-ttu-id="8f0c4-184">Försäljningsorder är den vanligaste typen för utgående källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="8f0c4-185">Så här skapar du försäljningsreturordern</span><span class="sxs-lookup"><span data-stu-id="8f0c4-185">To create the sales order</span></span>

1. <span data-ttu-id="8f0c4-186">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f0c4-187">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="8f0c4-188">Skapa en försäljningsorder för kund 10000 på arbetsdatumet (23 januari) med följande försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="8f0c4-189">Artikel</span><span class="sxs-lookup"><span data-stu-id="8f0c4-189">Item</span></span>|<span data-ttu-id="8f0c4-190">Lagerställekod</span><span class="sxs-lookup"><span data-stu-id="8f0c4-190">Location Code</span></span>|<span data-ttu-id="8f0c4-191">Antal</span><span class="sxs-lookup"><span data-stu-id="8f0c4-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="8f0c4-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="8f0c4-192">LS_81</span></span>|<span data-ttu-id="8f0c4-193">SILVER</span><span class="sxs-lookup"><span data-stu-id="8f0c4-193">SILVER</span></span>|<span data-ttu-id="8f0c4-194">30</span><span class="sxs-lookup"><span data-stu-id="8f0c4-194">30</span></span>|  

     <span data-ttu-id="8f0c4-195">Fortsätt med att meddela lagret att försäljningsordern är klar för lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="8f0c4-196">Välj åtgärden **Släppa**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="8f0c4-197">Anders fortsätter att plocka och leverera de sålda artiklarna.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="8f0c4-198">Plocka och leverera artiklar</span><span class="sxs-lookup"><span data-stu-id="8f0c4-198">Picking and Shipping Items</span></span>

<span data-ttu-id="8f0c4-199">På sidan **Lagerplockning** kan du hantera alla utgående distributionslageraktiviteter för ett särskilt källdokument, t.ex en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="8f0c4-200">Plocka och utleverera artiklar så här</span><span class="sxs-lookup"><span data-stu-id="8f0c4-200">To pick and ship items</span></span>

1. <span data-ttu-id="8f0c4-201">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerplockning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f0c4-202">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="8f0c4-203">Kontrollera att fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="8f0c4-203">Make sure that the **No.**</span></span> <span data-ttu-id="8f0c4-204">fälten på snabbfliken **Allmänt** fylls i.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="8f0c4-205">Välj fältet **Källdokument** och sedan **Försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="8f0c4-206">Välj fältet **Ursprungsnr.**, markera raden för försäljningen till kund 10000 och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="8f0c4-207">Välj alternativt åtgärden **Hämta källdokument** och välj sedan försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="8f0c4-208">Välj åtgärden **Fyll i auto. ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="8f0c4-209">Alternativt, ange 10 respektive 20 i fältet **Ant. att hantera** på de två lagerplockningsraderna.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="8f0c4-210">Välj åtgärden **bokför**, välj **leverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="8f0c4-211">De 30 högtalarna har nu registrerats som plockade från lagerställen S-01-0001 och S-01-0002, och en negativ artikeltransaktion skapas som återspeglar den bokförda leveransen.</span><span class="sxs-lookup"><span data-stu-id="8f0c4-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f0c4-212">Se även</span><span class="sxs-lookup"><span data-stu-id="8f0c4-212">See Also</span></span>

[<span data-ttu-id="8f0c4-213">Plocka artiklar med lagerplockning</span><span class="sxs-lookup"><span data-stu-id="8f0c4-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="8f0c4-214">Plocka artiklar för utleverans från dist.lager</span><span class="sxs-lookup"><span data-stu-id="8f0c4-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="8f0c4-215">Ställa in grundläggande dist.lager med verksamhetsområden</span><span class="sxs-lookup"><span data-stu-id="8f0c4-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="8f0c4-216">Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="8f0c4-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="8f0c4-217">Plocka för produktion eller montering</span><span class="sxs-lookup"><span data-stu-id="8f0c4-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="8f0c4-218">Flytta artiklar ad hoc i grundläggande lagerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="8f0c4-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="8f0c4-219">Designdetaljer: utgående distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="8f0c4-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="8f0c4-220">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="8f0c4-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="8f0c4-221">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f0c4-221">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]