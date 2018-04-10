---
title: "Köpa artiklar till försäljning genom att skapa inköpsfakturor | Microsoft Docs"
description: "Om du vill köpa produkter från en försäljningsfaktura skapar du en inköpsfaktura för en leverantör."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: d5ae63043a6f296de22f71c401a5686f970ad3a0
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="09c96-103">Köpa artiklar för en försäljning</span><span class="sxs-lookup"><span data-stu-id="09c96-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="09c96-104">Du kan använda funktioner snabbt skapa inköpsdokument för saknade artikelkvantiteter som krävs av försäljningen från försäljningsorder och fakturor.</span><span class="sxs-lookup"><span data-stu-id="09c96-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="09c96-105">Du kan använda två olika funktioner beroende på dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="09c96-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="09c96-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="09c96-106">Function</span></span>|<span data-ttu-id="09c96-107">Description</span><span class="sxs-lookup"><span data-stu-id="09c96-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="09c96-108">**Skapa inköpsorder**</span><span class="sxs-lookup"><span data-stu-id="09c96-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="09c96-109">Från en försäljningsorder skapar den här funktionen en inköpsorder för varje leverantör av artiklar som levererar artiklarna på försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="09c96-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="09c96-110">Du kan redigera inköpskvantiteten innan du skapar inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="09c96-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="09c96-111">Endast ej tillgängligt antal föreslås.</span><span class="sxs-lookup"><span data-stu-id="09c96-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="09c96-112">**Skapa inköpsfaktura**</span><span class="sxs-lookup"><span data-stu-id="09c96-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="09c96-113">Från en försäljningsorder och en försäljningsfaktura skapar funktionen en inköpsfaktura för en vald leverantör för alla eller markerade områden i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="09c96-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="09c96-114">Hela försäljningskvantiteten föreslås.</span><span class="sxs-lookup"><span data-stu-id="09c96-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="09c96-115">Så här skapar du inköpsorder för en eller flera serviceorder från en försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="09c96-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="09c96-116">Om du vill skapa en inköpsorder för varje artikelkvantitet som inte är tillgängliga på försäljningsordern, använd funktion **skapa inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="09c96-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="09c96-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="09c96-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="09c96-118">Öppna en försäljningsorder som du vill köpa in artiklar för.</span><span class="sxs-lookup"><span data-stu-id="09c96-118">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="09c96-119">Välj åtgärden **Skapa inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="09c96-119">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="09c96-120">Fönstret **skapa inköpsorder** öppnas med en rad för varje annan artikeln på försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="09c96-120">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="09c96-121">Rader för helt tillgängligt antal och inte tillgängligt antal (nedtonade) visas som standard.</span><span class="sxs-lookup"><span data-stu-id="09c96-121">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="09c96-122">Du kan välja åtgärden **Visa tillgängliga** för att bara visa rader för ej tillgängligt antal.</span><span class="sxs-lookup"><span data-stu-id="09c96-122">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="09c96-123">Fältet **antal att köpa** innehåller otillgängliga försäljningskvantiteten som standard.</span><span class="sxs-lookup"><span data-stu-id="09c96-123">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="09c96-124">Om du vill köpa en annan kvantitet än inte tillgängligt försäljningsantal, redigera värdet i fältet **antal att köpa**.</span><span class="sxs-lookup"><span data-stu-id="09c96-124">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="09c96-125">Du kan också ändra fältet **antal att köpa** på nedtonade rader även om de representerar helt tillgängligt antal.</span><span class="sxs-lookup"><span data-stu-id="09c96-125">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="09c96-126">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c96-126">Choose the **OK** button.</span></span>

    <span data-ttu-id="09c96-127">En inköpsorder skapas för varje leverantör som levererar artiklarna på försäljningsordern, inklusive kvantitetsändring som du gjorde i fönstret **skapa inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="09c96-127">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="09c96-128">Fortsätt att behandla inköpsorder, till exempel genom att redigera eller lägga till inköpsorderrader.</span><span class="sxs-lookup"><span data-stu-id="09c96-128">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="09c96-129">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="09c96-129">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="09c96-130">Så här skapar du en försäljningsorder från en försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="09c96-130">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="09c96-131">Om du vill skapa en enda inköpsorder för en eller flera rader i ett försäljningsdokument väljer du först vilken leverantör som du köper från med funktionen **skapa inköpsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="09c96-131">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="09c96-132">Den här funktionen skapar en inköpsfaktura för antalet exakt i det valda försäljningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="09c96-132">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="09c96-133">Om du vill ändra antalet inköp, måste du redigera journalen skapas.</span><span class="sxs-lookup"><span data-stu-id="09c96-133">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="09c96-134">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="09c96-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="09c96-135">Öppna en försäljningfaktura som du vill köpa in artiklar för.</span><span class="sxs-lookup"><span data-stu-id="09c96-135">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="09c96-136">Markera en eller flera försäljningsfakturarader som du vill använda i inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="09c96-136">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="09c96-137">För att använda alla försäljningsfakturarader väljer du antingen all rader eller inga rader alls.</span><span class="sxs-lookup"><span data-stu-id="09c96-137">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="09c96-138">Välj åtgärden **Skapa inköpsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="09c96-138">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="09c96-139">Välj antingen **Alla rader** eller **Valda rader** och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c96-139">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="09c96-140">Välj leverantören som du vill köpa alla artiklr frpn i listan över leverantörer som kommer att leverera artiklarna eller tjänsterna och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c96-140">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="09c96-141">En inköpsfaktura skapas som har en, flera eller alla rader på försäljningsfakturan.</span><span class="sxs-lookup"><span data-stu-id="09c96-141">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="09c96-142">Fortsätt att behandla inköpsfakturan, till exempel genom att redigera eller lägga till inköpsfakturarader.</span><span class="sxs-lookup"><span data-stu-id="09c96-142">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="09c96-143">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="09c96-143">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="09c96-144">Se även</span><span class="sxs-lookup"><span data-stu-id="09c96-144">See Also</span></span>
[<span data-ttu-id="09c96-145">Inköp</span><span class="sxs-lookup"><span data-stu-id="09c96-145">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="09c96-146">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="09c96-146">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="09c96-147">Fakturaförsäljning</span><span class="sxs-lookup"><span data-stu-id="09c96-147">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="09c96-148">Registrera nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="09c96-148">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="09c96-149">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="09c96-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

