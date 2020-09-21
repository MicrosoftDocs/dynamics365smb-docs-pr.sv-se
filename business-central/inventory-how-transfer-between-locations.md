---
title: Så här överför du artiklar mellan olika distributionslagerplatser | Microsoft Docs
description: Beskriver hur du flytta lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fcd88d3fc8c933863bd79ab8b3405b68a3e1f1e1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778017"
---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="1a667-103">Överföra lager mellan olika lagerställen</span><span class="sxs-lookup"><span data-stu-id="1a667-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="1a667-104">Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="1a667-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="1a667-105">Du kan även använda artikelgrupperingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="1a667-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="1a667-106">Med överföringsorder kan du leverera en utgående överföring från ett lagerställe och ta emot den ankommande överföringen på det andra lagerstället.</span><span class="sxs-lookup"><span data-stu-id="1a667-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="1a667-107">Detta gör det möjligt att administrera relevanta lageraktiviteter, och ger en större trygghet att lagerkvantiteterna uppdateras på rätt sätt.</span><span class="sxs-lookup"><span data-stu-id="1a667-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="1a667-108">Med grupperingsjournalen fyller du helt enkelt i fälten **Lagerställeskod** och **Ny Lagerställeskod**.</span><span class="sxs-lookup"><span data-stu-id="1a667-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="1a667-109">När du bokför journalen, justeras artikeltransaktionerna på berörda lägerställen.</span><span class="sxs-lookup"><span data-stu-id="1a667-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="1a667-110">På så sätt administreras inga lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="1a667-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1a667-111">Om du har artiklar i lagret utan lagerställekod, till exempel från en tid när du bara hade ett lage, kan du inte överföra objekten med överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="1a667-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="1a667-112">I stället måste du använda grupperingsjournalen för att gruppera artiklar från en tom lagerställekod till en faktisk lagerställekod.</span><span class="sxs-lookup"><span data-stu-id="1a667-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="1a667-113">Mer information finns i steg 3 i [Att överföra artiklar med artikelgrupperingsjournalen](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span><span class="sxs-lookup"><span data-stu-id="1a667-113">For more information, see step 3 in [To transfer items with the item reclassification journal](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span></span>

<span data-ttu-id="1a667-114">Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in.</span><span class="sxs-lookup"><span data-stu-id="1a667-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="1a667-115">Mer information finns i [Ange platser](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="1a667-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="1a667-116">För att överföra artiklar med en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="1a667-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="1a667-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Överföringsorder** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="1a667-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a667-118">I huvudet på sidan **Överföringsorder** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="1a667-118">On the header of the **Transfer Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="1a667-119">Om du har fyllt i fälten **Transitkod**, **Speditörkod** och **Speditör servicekod** på sidan **Överföringsflödespec.** när du lade upp överföringsflödet, fylls motsvarande fält i automatiskt på överföringsordern.</span><span class="sxs-lookup"><span data-stu-id="1a667-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields on the **Trans. Route Spec.** page when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="1a667-120">När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.</span><span class="sxs-lookup"><span data-stu-id="1a667-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

3. <span data-ttu-id="1a667-121">Om du vill fylla i raderna anger du dem manuellt eller väljer ett av följande alternativ under åtgärdsfönstret **funktioner**:</span><span class="sxs-lookup"><span data-stu-id="1a667-121">To fill in the lines, either enter them manually or choose one of the following options on the under the **Functions** action:</span></span>
    - <span data-ttu-id="1a667-122">Välj åtgärden **Hämta lagerplatsinnehåll** om du vill välja befintliga artiklar från en viss lagerplats på lagerstället.</span><span class="sxs-lookup"><span data-stu-id="1a667-122">Choose the **Get Bin Content** action to select existing items from a specific bin at the location.</span></span>
    - <span data-ttu-id="1a667-123">Välj **Hämta inleveransrader** för att välja artiklar som precis har anlänt till det lagerställe där överföringen sker.</span><span class="sxs-lookup"><span data-stu-id="1a667-123">Choose the **Get Receipt Lines** to select items that have just arrived at the transfer-from location.</span></span>   

    <span data-ttu-id="1a667-124">Som lagerarbetare på utleveranslagerstället fortsätter du med att leverera artiklarna.</span><span class="sxs-lookup"><span data-stu-id="1a667-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
4. <span data-ttu-id="1a667-125">Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="1a667-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="1a667-126">Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med angivet överföringsflöde.</span><span class="sxs-lookup"><span data-stu-id="1a667-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="1a667-127">Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna.</span><span class="sxs-lookup"><span data-stu-id="1a667-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span> <span data-ttu-id="1a667-128">Överföringsorderraderna är desamma som när de levereras och kan inte redigeras.</span><span class="sxs-lookup"><span data-stu-id="1a667-128">The transfer order lines are the same as when shipped and cannot be edited.</span></span>
5. <span data-ttu-id="1a667-129">Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="1a667-129">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="1a667-130">Så här överför du artiklar med artikelgrupperingsjournalen</span><span class="sxs-lookup"><span data-stu-id="1a667-130">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="1a667-131">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelgrupperingsjournaler** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="1a667-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a667-132">På sidan **Artikelgrupp.journal** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="1a667-132">On the **Item Reclass. Journal** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="1a667-133">I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.</span><span class="sxs-lookup"><span data-stu-id="1a667-133">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="1a667-134">För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod**.</span><span class="sxs-lookup"><span data-stu-id="1a667-134">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="1a667-135">I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.</span><span class="sxs-lookup"><span data-stu-id="1a667-135">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="1a667-136">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="1a667-136">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a667-137">Se även</span><span class="sxs-lookup"><span data-stu-id="1a667-137">See Also</span></span>
[<span data-ttu-id="1a667-138">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="1a667-138">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1a667-139">Konfigurera platser</span><span class="sxs-lookup"><span data-stu-id="1a667-139">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="1a667-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a667-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1a667-141">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="1a667-141">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="1a667-142">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="1a667-142">General Business Functionality</span></span>](ui-across-business-areas.md)
