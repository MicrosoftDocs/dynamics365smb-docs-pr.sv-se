---
title: Så här skapar du specialorder | Microsoft Docs
description: Du kan skapa en specialorder för en specifik katalogartikel som inte finns i lagret och som ska levereras till en specifik kund. Leverantören levererar artikeln till distributionslagret så att du sedan kan leverera den till kunden, som en enskild leverans eller tillsammans med andra artiklar på en annan order.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd22ee25cb472a827468c578ccdb8a7427490bc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383031"
---
# <a name="create-special-orders"></a><span data-ttu-id="2182a-104">Skapa specialorder</span><span class="sxs-lookup"><span data-stu-id="2182a-104">Create Special Orders</span></span>
<span data-ttu-id="2182a-105">Du kan skapa en specialorder för en specifik katalogartikel som inte finns i lagret och som ska levereras till en specifik kund.</span><span class="sxs-lookup"><span data-stu-id="2182a-105">You can create a special order for a specific catalog item to be shipped to a specific customer.</span></span> <span data-ttu-id="2182a-106">Leverantören levererar artikeln till distributionslagret så att du sedan kan leverera den till kunden, som en enskild leverans eller tillsammans med andra artiklar på en annan order.</span><span class="sxs-lookup"><span data-stu-id="2182a-106">Your vendor ships the item to your warehouse and you can then ship the item on to your customer either independently or together with other items on another order.</span></span>  

<span data-ttu-id="2182a-107">Specialorder anger att inköps- och försäljningsordern är länkade för att säkerställa att den specifika katalogartikeln plockas och levereras till kunden.</span><span class="sxs-lookup"><span data-stu-id="2182a-107">Special orders imply that the purchase and sales order are linked to ensure that the specific catalog item is picked and delivered to the customer.</span></span>  

<span data-ttu-id="2182a-108">Innan den här funktionen kan användas måste de kund-, leverantörs- och artikelkort som behövs för ordern läggas upp.</span><span class="sxs-lookup"><span data-stu-id="2182a-108">Before you can use this feature, you must first set up the customer, vendor, and item cards necessary for the order.</span></span>  

## <a name="to-create-a-special-order"></a><span data-ttu-id="2182a-109">Så här skapar du en specialorder</span><span class="sxs-lookup"><span data-stu-id="2182a-109">To create a special order</span></span>  
1.  <span data-ttu-id="2182a-110">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2182a-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2182a-111">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2182a-111">Choose the **New** action.</span></span> <span data-ttu-id="2182a-112">Skapa och fyll i  försäljningsorder för artikeln.</span><span class="sxs-lookup"><span data-stu-id="2182a-112">Create and fill in a  sales order for the item.</span></span> <span data-ttu-id="2182a-113">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="2182a-113">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3.  <span data-ttu-id="2182a-114">Fyll i försäljningsraden på snabbfliken **Rader** .</span><span class="sxs-lookup"><span data-stu-id="2182a-114">On the **Lines** FastTab, fill in the sales line.</span></span> <span data-ttu-id="2182a-115">I fältet **Inköpskod**, välj en inköpskod som har fältet **Specialorder** markerat.</span><span class="sxs-lookup"><span data-stu-id="2182a-115">In the **Purchasing Code** field, select a purchasing code that has the **Special Order** field selected.</span></span>

    <span data-ttu-id="2182a-116">Därefter måste du skapa en inköpsorder från ett inköpsförslag.</span><span class="sxs-lookup"><span data-stu-id="2182a-116">You must now create a purchase order from a requisition worksheet.</span></span>  
4. <span data-ttu-id="2182a-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rekvisitionskalkylark** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="2182a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requisition Worksheet**, and then choose the related link.</span></span>  
5. <span data-ttu-id="2182a-118">Välj åtgärden **Specialorder** och väljer sedan åtgärden **Hämta förs.order**.</span><span class="sxs-lookup"><span data-stu-id="2182a-118">Choose the **Special Order** action, and then choose the **Get Sales Orders** action.</span></span>  
6.  <span data-ttu-id="2182a-119">På sidan **Hämta förs.order** visar resultat där **Verifikationsnr** är numret på försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="2182a-119">On the **Get Sales Orders** page, show results where the **Document No.** is the sales order number.</span></span> <span data-ttu-id="2182a-120">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2182a-120">Choose the **OK** button.</span></span> <span data-ttu-id="2182a-121">En inköpskalkylarksrad skapas för artikeln.</span><span class="sxs-lookup"><span data-stu-id="2182a-121">A requisition worksheet line is created for the item.</span></span>  
7.  <span data-ttu-id="2182a-122">På inköpskalkylarksraden, i fältet **Åtgärdsmeddelande**, väljer du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2182a-122">On the requisition worksheet line, in the **Action Message** field, select **New**.</span></span>  
8.  <span data-ttu-id="2182a-123">På sidan **Inköpsförslag** väljer du åtgärden **Verkställ åtgärdsmeddelande**.</span><span class="sxs-lookup"><span data-stu-id="2182a-123">On the **Req. Worksheet** page, choose the **Carry Out Action Message** action.</span></span> <span data-ttu-id="2182a-124">Sidan **Skapa inköpsorder** visas.</span><span class="sxs-lookup"><span data-stu-id="2182a-124">The **Carry Out Action Msg. - Req.** page opens.</span></span> <span data-ttu-id="2182a-125">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2182a-125">Choose the **OK** button.</span></span>  

    <span data-ttu-id="2182a-126">Du får meddelande om att inköpsorderna har skapats.</span><span class="sxs-lookup"><span data-stu-id="2182a-126">A message appears telling you that the purchase orders have been created.</span></span> <span data-ttu-id="2182a-127">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2182a-127">Choost the **OK** button.</span></span>  

<span data-ttu-id="2182a-128">En inköpsorder som skapas som en specialorder för en försäljningsorder respekteras av planeringssystemet när behov och tillgång balanseras.</span><span class="sxs-lookup"><span data-stu-id="2182a-128">A purchase order created as a special order for a sales order is respected by the planning system as it balances demand and supply.</span></span> <span data-ttu-id="2182a-129">Det innebär att inköpsordern (tillgång) förblir länkad till försäljningsordern (behov) även om inköpsorden kan tillgodose ett annat, tidigare behov.</span><span class="sxs-lookup"><span data-stu-id="2182a-129">That is, the purchase order (supply) remains linked to the sales order (demand), even if that purchase order could supply another earlier demand.</span></span> <span data-ttu-id="2182a-130">Mer information finns i [Designdetaljer: Partiformningsmetoder](design-details-reservation-order-tracking-and-action-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="2182a-130">For more information, see [Design Details: Reordering Policies](design-details-reservation-order-tracking-and-action-messaging.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2182a-131">Du kan använda funktionen Specialorder om artikeln redan har reserverats.</span><span class="sxs-lookup"><span data-stu-id="2182a-131">You cannot use the special order functionality if the item is already reserved.</span></span> <span data-ttu-id="2182a-132">Därför, för artiklar som säljs på särskilda order, kontrollera att fältet **Reservera** på artikelkortet har angetts till **alltid**.</span><span class="sxs-lookup"><span data-stu-id="2182a-132">Therefore, for items that are sold on special orders, make sure the **Reserve** field on the item card is not set to **Always**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2182a-133">Se även</span><span class="sxs-lookup"><span data-stu-id="2182a-133">See Also</span></span>  
[<span data-ttu-id="2182a-134">Arbeta med katalogartiklar</span><span class="sxs-lookup"><span data-stu-id="2182a-134">Work with Catalog Items</span></span>](inventory-how-work-nonstock-items.md)  
[<span data-ttu-id="2182a-135">Försäljning</span><span class="sxs-lookup"><span data-stu-id="2182a-135">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="2182a-136">[Skapa direktleveranser](sales-how-drop-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="2182a-136">[Make Drop Shipments](sales-how-drop-shipment.md) </span></span>  
[<span data-ttu-id="2182a-137">Designdetaljer: Partiformningsmetoder</span><span class="sxs-lookup"><span data-stu-id="2182a-137">Design Details: Reordering Policies</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="2182a-138">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2182a-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]