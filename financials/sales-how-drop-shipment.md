---
title: "Skapa en försäljningsorder som är kopplad till en inköpsorder för en direktleverans | Microsoft Docs"
description: "Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="0d7b8-103">Så här utför du direktleveranser</span><span class="sxs-lookup"><span data-stu-id="0d7b8-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="0d7b8-104">Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="0d7b8-105">När en försäljningsorder är markerad för direktleverans, och du skapar en inköpsorder där du anger kunden i fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="0d7b8-106">kan du länka de två dokumenten och därmed instruera leverantören att leverera direkt till kunden.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="0d7b8-107">Så här skapar du försäljningsorder för direktleveranser</span><span class="sxs-lookup"><span data-stu-id="0d7b8-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="0d7b8-108">För att förbereda en direktleverans skapar du en försäljningsorder för en artikel som vanligt, förutom att du måste ange på försäljningsraden att försäljningen kräver direktleverans.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="0d7b8-109">Skapa en försäljningsorder för en artikel.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-109">Create a sales order for an item.</span></span> <span data-ttu-id="0d7b8-110">Mer information finns i [Så här säljer du produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="0d7b8-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="0d7b8-111">På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="0d7b8-112">Använd funktionen **Välj kolumner** om fältet inte visas.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="0d7b8-113">Mer information finns i [Användaranpassning](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="0d7b8-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="0d7b8-114">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="0d7b8-115">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="0d7b8-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="0d7b8-116">Så här skapar du inköpsorder för direktleverans</span><span class="sxs-lookup"><span data-stu-id="0d7b8-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="0d7b8-117">Om du vill förbereda en direktleverans för den artikel som ska säljas kan du skapa en inköpsorder som vanligt förutom att du måste ange på inköpsordern att den ska levereras till din kund och inte till dig själv.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="0d7b8-118">Skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-118">Create a purchase order.</span></span> <span data-ttu-id="0d7b8-119">Fyll inte i några fält på raderna.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="0d7b8-120">Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="0d7b8-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="0d7b8-121">I fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="0d7b8-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="0d7b8-122">markerar du kunden som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="0d7b8-123">Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="0d7b8-124">I fönstret **Försäljningslista** väljer du den försäljningsorder som du förberedde i avsnittet "Så här skapar du försäljningsorder för direktleveranser".</span><span class="sxs-lookup"><span data-stu-id="0d7b8-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="0d7b8-125">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-125">Choose the **OK** button.</span></span>

<span data-ttu-id="0d7b8-126">Radinformationen från försäljningsordern infogas på inköpsorderraden.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="0d7b8-127">Du kan nu instruera leverantören att leverera artiklarna till kunden, till exempel genom att e-posta inköpsordern som en PDF.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="0d7b8-128">Om du vill se den länkade inköpsordern från försäljningsordern</span><span class="sxs-lookup"><span data-stu-id="0d7b8-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="0d7b8-129">Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="0d7b8-130">Så här bokför du en direktutleverans</span><span class="sxs-lookup"><span data-stu-id="0d7b8-130">To post a drop shipment</span></span>
<span data-ttu-id="0d7b8-131">När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="0d7b8-132">Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="0d7b8-133">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d7b8-134">Öppna den försäljningsorder som du skapade i avsnittet "Att skapa en försäljningsorder för en direktleverans" .</span><span class="sxs-lookup"><span data-stu-id="0d7b8-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="0d7b8-135">I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="0d7b8-136">Välj åtgärden **Bokför** eller **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="0d7b8-137">Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.</span><span class="sxs-lookup"><span data-stu-id="0d7b8-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d7b8-138">Se även</span><span class="sxs-lookup"><span data-stu-id="0d7b8-138">See Also</span></span>
<span data-ttu-id="0d7b8-139">[Så här skapar du specialorder](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="0d7b8-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="0d7b8-140">Så här säljer du produkter</span><span class="sxs-lookup"><span data-stu-id="0d7b8-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="0d7b8-141">Så här registrerar du inköp</span><span class="sxs-lookup"><span data-stu-id="0d7b8-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="0d7b8-142">Försäljning</span><span class="sxs-lookup"><span data-stu-id="0d7b8-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0d7b8-143">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="0d7b8-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0d7b8-144">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d7b8-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

