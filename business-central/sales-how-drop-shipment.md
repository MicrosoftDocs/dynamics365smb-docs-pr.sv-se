---
title: Koppla en försäljningsorder till en inköpsorder för direktleverans | Microsoft Docs
description: Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "929365"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="64a95-103">Skapa direktleveranser</span><span class="sxs-lookup"><span data-stu-id="64a95-103">Make Drop Shipments</span></span>
<span data-ttu-id="64a95-104">Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.</span><span class="sxs-lookup"><span data-stu-id="64a95-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="64a95-105">När en försäljningsorder är markerad för direktleverans, och du skapar en inköpsorder där du anger kunden i fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="64a95-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="64a95-106">kan du länka de två dokumenten och därmed instruera leverantören att leverera direkt till kunden.</span><span class="sxs-lookup"><span data-stu-id="64a95-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="64a95-107">Så här skapar du försäljningsorder för direktleveranser</span><span class="sxs-lookup"><span data-stu-id="64a95-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="64a95-108">För att förbereda en direktleverans skapar du en försäljningsorder för en artikel som vanligt, förutom att du måste ange på försäljningsraden att försäljningen kräver direktleverans.</span><span class="sxs-lookup"><span data-stu-id="64a95-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="64a95-109">Skapa en försäljningsorder för en artikel.</span><span class="sxs-lookup"><span data-stu-id="64a95-109">Create a sales order for an item.</span></span> <span data-ttu-id="64a95-110">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="64a95-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="64a95-111">På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**.</span><span class="sxs-lookup"><span data-stu-id="64a95-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="64a95-112">Använda funktionen **Välj kolumner** om fältet inte visas.</span><span class="sxs-lookup"><span data-stu-id="64a95-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="64a95-113">Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="64a95-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="64a95-114">Så här skapar du inköpsorder för direktleverans</span><span class="sxs-lookup"><span data-stu-id="64a95-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="64a95-115">Om du vill förbereda en direktleverans för den artikel som ska säljas kan du skapa en inköpsorder som vanligt förutom att du måste ange på inköpsordern att den ska levereras till din kund och inte till dig själv.</span><span class="sxs-lookup"><span data-stu-id="64a95-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="64a95-116">Skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="64a95-116">Create a purchase order.</span></span> <span data-ttu-id="64a95-117">Fyll inte i några fält på raderna.</span><span class="sxs-lookup"><span data-stu-id="64a95-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="64a95-118">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="64a95-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="64a95-119">I fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="64a95-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="64a95-120">markerar du kunden som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="64a95-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="64a95-121">Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.</span><span class="sxs-lookup"><span data-stu-id="64a95-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="64a95-122">På sidan **Försäljningslista** väljer du den försäljningsorder som du förberedde i [Så här skapar du försäljningsorder för direktleveranser](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="64a95-122">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="64a95-123">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a95-123">Choose the **OK** button.</span></span>

<span data-ttu-id="64a95-124">Radinformationen från försäljningsordern infogas på inköpsorderraden.</span><span class="sxs-lookup"><span data-stu-id="64a95-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="64a95-125">Du kan nu instruera leverantören att leverera artiklarna till kunden, till exempel genom att e-posta inköpsordern som en PDF.</span><span class="sxs-lookup"><span data-stu-id="64a95-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="64a95-126">Om du vill se den länkade inköpsordern från försäljningsordern</span><span class="sxs-lookup"><span data-stu-id="64a95-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="64a95-127">Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="64a95-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="64a95-128">Så här bokför du en direktutleverans</span><span class="sxs-lookup"><span data-stu-id="64a95-128">To post a drop shipment</span></span>
<span data-ttu-id="64a95-129">När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad.</span><span class="sxs-lookup"><span data-stu-id="64a95-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="64a95-130">Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="64a95-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="64a95-131">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64a95-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="64a95-132">Öppna den försäljningsorder som du skapade i [Att skapa en försäljningsorder för en direktleverans]() .</span><span class="sxs-lookup"><span data-stu-id="64a95-132">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="64a95-133">I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="64a95-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="64a95-134">Välj åtgärden **Bokför** eller **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="64a95-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="64a95-135">Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.</span><span class="sxs-lookup"><span data-stu-id="64a95-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="64a95-136">Se även</span><span class="sxs-lookup"><span data-stu-id="64a95-136">See Also</span></span>
[<span data-ttu-id="64a95-137">Skapa specialorder</span><span class="sxs-lookup"><span data-stu-id="64a95-137">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="64a95-138">Köpa artiklar för en försäljning</span><span class="sxs-lookup"><span data-stu-id="64a95-138">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="64a95-139">Sälja produkter</span><span class="sxs-lookup"><span data-stu-id="64a95-139">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="64a95-140">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="64a95-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="64a95-141">Försäljning</span><span class="sxs-lookup"><span data-stu-id="64a95-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="64a95-142">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="64a95-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="64a95-143">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64a95-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
