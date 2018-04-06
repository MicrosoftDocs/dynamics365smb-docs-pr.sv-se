---
title: "Så här överför du artiklar mellan olika distributionslagerplatser | Microsoft Docs"
description: "Beskriver hur du flytta lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 6f83607606d79d894cbe8f154566b9fe7a65a94c
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="3feaf-103">Överföra lager mellan olika lagerställen</span><span class="sxs-lookup"><span data-stu-id="3feaf-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="3feaf-104">Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="3feaf-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="3feaf-105">Du kan även använda artikelgrupperingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="3feaf-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="3feaf-106">Med överföringsorder kan du leverera en utgående överföring från ett lagerställe och ta emot den ankommande överföringen på det andra lagerstället.</span><span class="sxs-lookup"><span data-stu-id="3feaf-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="3feaf-107">Detta gör det möjligt att administrera relevanta lageraktiviteter, och ger en större trygghet att lagerkvantiteterna uppdateras på rätt sätt.</span><span class="sxs-lookup"><span data-stu-id="3feaf-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="3feaf-108">Med grupperingsjournalen fyller du helt enkelt i fälten **Lagerställeskod** och **Ny Lagerställeskod**.</span><span class="sxs-lookup"><span data-stu-id="3feaf-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="3feaf-109">När du bokför journalen, justeras artikeltransaktionerna på berörda lägerställen.</span><span class="sxs-lookup"><span data-stu-id="3feaf-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="3feaf-110">På så sätt administreras inga lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="3feaf-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3feaf-111">Om du har artiklar i lagret utan lagerställekod, till exempel från en tid när du bara hade ett lage, kan du inte överföra objekten med överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="3feaf-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="3feaf-112">I stället måste du använda grupperingsjournalen för att gruppera artiklar från en tom lagerställekod till en faktisk lagerställekod.</span><span class="sxs-lookup"><span data-stu-id="3feaf-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="3feaf-113">Mer information finns i steg 3 i avsnittet "Att överföra artiklar med artikelgrupperingsjournalen".</span><span class="sxs-lookup"><span data-stu-id="3feaf-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="3feaf-114">Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in.</span><span class="sxs-lookup"><span data-stu-id="3feaf-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="3feaf-115">Mer information finns i [Ange platser](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="3feaf-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="3feaf-116">För att överföra artiklar med en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="3feaf-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="3feaf-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Överföringsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3feaf-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="3feaf-118">I fönstret **Överföringsorder** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="3feaf-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="3feaf-119">Om du har fyllt i fälten **Transitkod**, **Speditörkod** och **Speditör servicekod** i fönstret **Överföringsflödespec.** när du lade upp överföringsflödet, fylls motsvarande fält i automatiskt på överföringsordern.</span><span class="sxs-lookup"><span data-stu-id="3feaf-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="3feaf-120">När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.</span><span class="sxs-lookup"><span data-stu-id="3feaf-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="3feaf-121">Som lagerarbetare på utleveranslagerstället fortsätter du med att leverera artiklarna.</span><span class="sxs-lookup"><span data-stu-id="3feaf-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="3feaf-122">Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="3feaf-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="3feaf-123">Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med angivet överföringsflöde.</span><span class="sxs-lookup"><span data-stu-id="3feaf-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="3feaf-124">Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna.</span><span class="sxs-lookup"><span data-stu-id="3feaf-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="3feaf-125">Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="3feaf-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="3feaf-126">Så här överför du artiklar med artikelgrupperingsjournalen</span><span class="sxs-lookup"><span data-stu-id="3feaf-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="3feaf-127">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3feaf-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="3feaf-128">I fönstret **Artikelgrupp.journal** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="3feaf-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="3feaf-129">I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.</span><span class="sxs-lookup"><span data-stu-id="3feaf-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="3feaf-130">För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="3feaf-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="3feaf-131">I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.</span><span class="sxs-lookup"><span data-stu-id="3feaf-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="3feaf-132">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="3feaf-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="3feaf-133">Se även</span><span class="sxs-lookup"><span data-stu-id="3feaf-133">See Also</span></span>
[<span data-ttu-id="3feaf-134">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="3feaf-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3feaf-135">Konfigurera platser</span><span class="sxs-lookup"><span data-stu-id="3feaf-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="3feaf-136">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3feaf-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="3feaf-137">[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="3feaf-137">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="3feaf-138">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="3feaf-138">General Business Functionality</span></span>](ui-across-business-areas.md)

