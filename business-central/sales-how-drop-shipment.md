---
title: "Koppla en försäljningsorder till en inköpsorder för direktleverans | Microsoft Docs"
description: "Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4840cde44374f17dcbd2befb167bfdf6110fe6fe
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="make-drop-shipments"></a><span data-ttu-id="5449b-103">Skapa direktleveranser</span><span class="sxs-lookup"><span data-stu-id="5449b-103">Make Drop Shipments</span></span>
<span data-ttu-id="5449b-104">Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.</span><span class="sxs-lookup"><span data-stu-id="5449b-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="5449b-105">När en försäljningsorder är markerad för direktleverans, och du skapar en inköpsorder där du anger kunden i fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="5449b-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="5449b-106">kan du länka de två dokumenten och därmed instruera leverantören att leverera direkt till kunden.</span><span class="sxs-lookup"><span data-stu-id="5449b-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="5449b-107">Så här skapar du försäljningsorder för direktleveranser</span><span class="sxs-lookup"><span data-stu-id="5449b-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="5449b-108">För att förbereda en direktleverans skapar du en försäljningsorder för en artikel som vanligt, förutom att du måste ange på försäljningsraden att försäljningen kräver direktleverans.</span><span class="sxs-lookup"><span data-stu-id="5449b-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="5449b-109">Skapa en försäljningsorder för en artikel.</span><span class="sxs-lookup"><span data-stu-id="5449b-109">Create a sales order for an item.</span></span> <span data-ttu-id="5449b-110">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="5449b-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="5449b-111">På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**.</span><span class="sxs-lookup"><span data-stu-id="5449b-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="5449b-112">Använda funktionen **Välj kolumner** om fältet inte visas.</span><span class="sxs-lookup"><span data-stu-id="5449b-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="5449b-113">Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="5449b-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="5449b-114">Så här skapar du inköpsorder för direktleverans</span><span class="sxs-lookup"><span data-stu-id="5449b-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="5449b-115">Om du vill förbereda en direktleverans för den artikel som ska säljas kan du skapa en inköpsorder som vanligt förutom att du måste ange på inköpsordern att den ska levereras till din kund och inte till dig själv.</span><span class="sxs-lookup"><span data-stu-id="5449b-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="5449b-116">Skapa en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="5449b-116">Create a purchase order.</span></span> <span data-ttu-id="5449b-117">Fyll inte i några fält på raderna.</span><span class="sxs-lookup"><span data-stu-id="5449b-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="5449b-118">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="5449b-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="5449b-119">I fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="5449b-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="5449b-120">markerar du kunden som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="5449b-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="5449b-121">Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.</span><span class="sxs-lookup"><span data-stu-id="5449b-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="5449b-122">I fönstret **Försäljningslista** väljer du den försäljningsorder som du förberedde i avsnittet "Så här skapar du försäljningsorder för direktleveranser".</span><span class="sxs-lookup"><span data-stu-id="5449b-122">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="5449b-123">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="5449b-123">Choose the **OK** button.</span></span>

<span data-ttu-id="5449b-124">Radinformationen från försäljningsordern infogas på inköpsorderraden.</span><span class="sxs-lookup"><span data-stu-id="5449b-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="5449b-125">Du kan nu instruera leverantören att leverera artiklarna till kunden, till exempel genom att e-posta inköpsordern som en PDF.</span><span class="sxs-lookup"><span data-stu-id="5449b-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="5449b-126">Om du vill se den länkade inköpsordern från försäljningsordern</span><span class="sxs-lookup"><span data-stu-id="5449b-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="5449b-127">Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="5449b-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="5449b-128">Så här bokför du en direktutleverans</span><span class="sxs-lookup"><span data-stu-id="5449b-128">To post a drop shipment</span></span>
<span data-ttu-id="5449b-129">När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad.</span><span class="sxs-lookup"><span data-stu-id="5449b-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="5449b-130">Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="5449b-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="5449b-131">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5449b-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5449b-132">Öppna den försäljningsorder som du skapade i avsnittet "Att skapa en försäljningsorder för en direktleverans" .</span><span class="sxs-lookup"><span data-stu-id="5449b-132">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="5449b-133">I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="5449b-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="5449b-134">Välj åtgärden **Bokför** eller **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="5449b-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="5449b-135">Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.</span><span class="sxs-lookup"><span data-stu-id="5449b-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="5449b-136">Se även</span><span class="sxs-lookup"><span data-stu-id="5449b-136">See Also</span></span>
<span data-ttu-id="5449b-137">[Skapa specialorder](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="5449b-137">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="5449b-138">Sälja produkter</span><span class="sxs-lookup"><span data-stu-id="5449b-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="5449b-139">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="5449b-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="5449b-140">Försäljning</span><span class="sxs-lookup"><span data-stu-id="5449b-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5449b-141">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="5449b-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5449b-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5449b-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

