---
title: "Så här överför du artiklar mellan olika distributionslagerplatser | Microsoft Docs"
description: "Beskriver hur du flytta lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41804dc183f9fa05ec1599db34c2b4f76a790a72
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="e8b1e-103">Så här överför du lager mellan olika lagerställen</span><span class="sxs-lookup"><span data-stu-id="e8b1e-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="e8b1e-104">Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="e8b1e-105">Du kan även använda artikelgrupperingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="e8b1e-106">Med överföringsorder kan du leverera en utgående överföring från ett lagerställe och ta emot den ankommande överföringen på det andra lagerstället.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="e8b1e-107">Detta gör det möjligt att administrera relevanta lageraktiviteter, och ger en större trygghet att lagerkvantiteterna uppdateras på rätt sätt.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="e8b1e-108">Med grupperingsjournalen fyller du helt enkelt i fälten **Lagerställeskod** och **Ny Lagerställeskod**.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="e8b1e-109">När du bokför journalen, justeras artikeltransaktionerna på berörda lägerställen.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="e8b1e-110">På så sätt administreras inga lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e8b1e-111">Om du har artiklar i lagret utan lagerställekod, till exempel från en tid när du bara hade ett lage, kan du inte överföra objekten med överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="e8b1e-112">I stället måste du använda grupperingsjournalen för att gruppera artiklar från en tom lagerställekod till en faktisk lagerställekod.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="e8b1e-113">Mer information finns i steg 3 i avsnittet "Att överföra artiklar med artikelgrupperingsjournalen".</span><span class="sxs-lookup"><span data-stu-id="e8b1e-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="e8b1e-114">Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="e8b1e-115">Mer information finns i [Så här skapar du lägerställen](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="e8b1e-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="e8b1e-116">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="e8b1e-117">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="e8b1e-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="e8b1e-118">För att överföra artiklar med en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="e8b1e-119">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Överföringsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="e8b1e-120">I fönstret **Överföringsorder** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="e8b1e-121">Om du har fyllt i fälten **Transitkod**, **Speditörkod** och **Speditör servicekod** i fönstret **Överföringsflödespec.** när du lade upp överföringsflödet, fylls motsvarande fält i automatiskt på överföringsordern.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="e8b1e-122">När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-122">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="e8b1e-123">Som lagerarbetare på utleveranslagerstället fortsätter du med att leverera artiklarna.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-123">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="e8b1e-124">Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-124">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="e8b1e-125">Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med angivet överföringsflöde.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-125">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="e8b1e-126">Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-126">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="e8b1e-127">Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-127">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="e8b1e-128">Så här överför du artiklar med artikelgrupperingsjournalen</span><span class="sxs-lookup"><span data-stu-id="e8b1e-128">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="e8b1e-129">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e8b1e-130">I fönstret **Artikelgrupp.journal** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-130">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e8b1e-131">I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-131">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="e8b1e-132">För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-132">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="e8b1e-133">I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-133">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="e8b1e-134">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-134">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8b1e-135">Se även</span><span class="sxs-lookup"><span data-stu-id="e8b1e-135">See Also</span></span>
[<span data-ttu-id="e8b1e-136">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="e8b1e-136">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e8b1e-137">Så här skapar du lagerställen</span><span class="sxs-lookup"><span data-stu-id="e8b1e-137">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
  
<span data-ttu-id="e8b1e-138">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8b1e-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="e8b1e-139">[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="e8b1e-139">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="e8b1e-140">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="e8b1e-140">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
