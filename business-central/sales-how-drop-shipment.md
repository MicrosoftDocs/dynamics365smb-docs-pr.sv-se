---
title: Koppla en försäljningsorder till en inköpsorder för direktleverans | Microsoft Docs
description: Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: beb78a3526b95af228ab313b67174633902e7bd7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778828"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="752d0-103">Skapa direktleveranser</span><span class="sxs-lookup"><span data-stu-id="752d0-103">Make Drop Shipments</span></span>

<span data-ttu-id="752d0-104">Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.</span><span class="sxs-lookup"><span data-stu-id="752d0-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="752d0-105">När en försäljningsorder har markerats för direktleverans och du skapar en inköpsorder som anger kunden i fältet **Leverans**, **Kundadress** kan du länka de två dokumenten för att instruera leverantören att leverera direkt till kunden.</span><span class="sxs-lookup"><span data-stu-id="752d0-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="752d0-106">Så här skapar du försäljningsorder för direktleveranser</span><span class="sxs-lookup"><span data-stu-id="752d0-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="752d0-107">För att förbereda en direktleverans skapar du en försäljningsorder för en artikel och anger på försäljningsraden att försäljningen kräver direktleverans.</span><span class="sxs-lookup"><span data-stu-id="752d0-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="752d0-108">Skapa en försäljningsorder för en artikel.</span><span class="sxs-lookup"><span data-stu-id="752d0-108">Create a sales order for an item.</span></span> <span data-ttu-id="752d0-109">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="752d0-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="752d0-110">På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**.</span><span class="sxs-lookup"><span data-stu-id="752d0-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="752d0-111">Använda funktionen **Välj kolumner** om fältet inte visas.</span><span class="sxs-lookup"><span data-stu-id="752d0-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="752d0-112">Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="752d0-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="752d0-113">Så här skapar du inköpsorder för direktleverans</span><span class="sxs-lookup"><span data-stu-id="752d0-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="752d0-114">När du förbereder en direktleverans anger du på inköpsordern att den måste levereras till kunden, inte till dig själv.</span><span class="sxs-lookup"><span data-stu-id="752d0-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="752d0-115">Skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="752d0-115">Create a purchase order.</span></span> <span data-ttu-id="752d0-116">Fyll inte i några fält på raderna.</span><span class="sxs-lookup"><span data-stu-id="752d0-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="752d0-117">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="752d0-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="752d0-118">Välj **Kundadress** i fältet **Leverans**.</span><span class="sxs-lookup"><span data-stu-id="752d0-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="752d0-119">I fältet **Kund** markerar du kunden som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="752d0-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="752d0-120">Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.</span><span class="sxs-lookup"><span data-stu-id="752d0-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="752d0-121">På sidan **Försäljningslista** väljer du den försäljningsorder som du förberedde i [Så här skapar du försäljningsorder för direktleveranser](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="752d0-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="752d0-122">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="752d0-122">Choose the **OK** button.</span></span>

<span data-ttu-id="752d0-123">Radinformationen från försäljningsordern infogas på inköpsorderraden.</span><span class="sxs-lookup"><span data-stu-id="752d0-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="752d0-124">Du kan nu instruera leverantören att leverera artiklarna till kunden, till exempel genom att e-posta inköpsordern som en PDF.</span><span class="sxs-lookup"><span data-stu-id="752d0-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="752d0-125">Så här skapar du flera inköpsorder för direktleveranser</span><span class="sxs-lookup"><span data-stu-id="752d0-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="752d0-126">Du kan också använda inköpskalkylarket för att skapa inköpsordern för leverantören.</span><span class="sxs-lookup"><span data-stu-id="752d0-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="752d0-127">Fördelen med att använda inköpskalkylarket är att du kan skapa inköpsorder för alla utestående direktleveranser, så att du inte behöver skapa var och en enskilt.</span><span class="sxs-lookup"><span data-stu-id="752d0-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="752d0-128">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpskalkylark** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="752d0-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="752d0-129">Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.</span><span class="sxs-lookup"><span data-stu-id="752d0-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="752d0-130">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="752d0-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="752d0-131">Granska inköpsorderraderna och i fältet **Leverantörsnr** väljer du leverantör som levererar erforderliga varor.</span><span class="sxs-lookup"><span data-stu-id="752d0-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="752d0-132">Välj åtgärden **Utför åtgärdsmeddelande** för att konvertera mottagna rader till en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="752d0-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="752d0-133">Om du vill se den länkade inköpsordern från försäljningsordern</span><span class="sxs-lookup"><span data-stu-id="752d0-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="752d0-134">Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="752d0-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="752d0-135">Så här bokför du en direktutleverans</span><span class="sxs-lookup"><span data-stu-id="752d0-135">To post a drop shipment</span></span>

<span data-ttu-id="752d0-136">När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad.</span><span class="sxs-lookup"><span data-stu-id="752d0-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="752d0-137">Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="752d0-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="752d0-138">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="752d0-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="752d0-139">Öppna den säljorder som du skapade i [För att skapa en säljorder för dropshipment](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="752d0-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="752d0-140">I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="752d0-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="752d0-141">Välj åtgärden **Bokför** eller **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="752d0-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="752d0-142">Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.</span><span class="sxs-lookup"><span data-stu-id="752d0-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="752d0-143">Se även</span><span class="sxs-lookup"><span data-stu-id="752d0-143">See Also</span></span>

[<span data-ttu-id="752d0-144">Skapa specialorder</span><span class="sxs-lookup"><span data-stu-id="752d0-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="752d0-145">Köpa artiklar för en försäljning</span><span class="sxs-lookup"><span data-stu-id="752d0-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="752d0-146">Sälja produkter</span><span class="sxs-lookup"><span data-stu-id="752d0-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="752d0-147">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="752d0-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="752d0-148">Försäljning</span><span class="sxs-lookup"><span data-stu-id="752d0-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="752d0-149">Lager</span><span class="sxs-lookup"><span data-stu-id="752d0-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="752d0-150">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="752d0-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]