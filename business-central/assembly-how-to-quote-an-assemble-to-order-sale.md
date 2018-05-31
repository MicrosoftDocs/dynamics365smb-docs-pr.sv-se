---
title: "Så här skapar du en offert för montering mot kundorder-försäljning | Microsoft Docs"
description: "Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4bc9199b879c23115082b07a81d6da5a0b46e60d
ms.openlocfilehash: 74f59840f2c881619910457366f38f0fa354abff
ms.contentlocale: sv-se
ms.lasthandoff: 05/31/2018

---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="34579-103">Skapa en försäljning för montering mot kundorder</span><span class="sxs-lookup"><span data-stu-id="34579-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="34579-104">Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="34579-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="34579-105">Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="34579-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="34579-106">När du säljer någon annan typ av artikel kan du också skapa en försäljningsoffert för en anpassad monteringsartikel innan du omvandlar den till en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="34579-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="34579-107">Den här processen involverar flera extra steg i jämförelse med att skapa en vanlig försäljningsoffert. Den använder en variation av en kopplad monteringsorder, dvs. en monteringsoffert.</span><span class="sxs-lookup"><span data-stu-id="34579-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="34579-108">Precis som på alla typer av offerter används inte antalet på monteringsoffertar för tillgänglighet, planering eller reservationer.</span><span class="sxs-lookup"><span data-stu-id="34579-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="34579-109">Så här skapar du en försäljningsoffert för en artikel för montering mot kundorder</span><span class="sxs-lookup"><span data-stu-id="34579-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="34579-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsoffert** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="34579-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="34579-111">Skapa en försäljningsoffertrad med en rad för en monteringsartikel.</span><span class="sxs-lookup"><span data-stu-id="34579-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="34579-112">Mer information finns i [Skapa erbjudanden](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="34579-112">For more information, see [Make Offers](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="34579-113">I fältet **Antal att montera mot kundorder** anger du hela antalet.</span><span class="sxs-lookup"><span data-stu-id="34579-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="34579-114">Du bör inte erbjuda ett delantal i offerten.</span><span class="sxs-lookup"><span data-stu-id="34579-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="34579-115">Därför måste du ange samma antal som du angett i fältet **Antal** på försäljningsoffertraden.</span><span class="sxs-lookup"><span data-stu-id="34579-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="34579-116">På snabbfliken **Rader** väljer du **Rad**, **Montering mot kundorder** och sedan **Montering mot kundorderrader**.</span><span class="sxs-lookup"><span data-stu-id="34579-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="34579-117">Alternativt kan du välja fältet **Antal att montera mot kundorder** på raden.</span><span class="sxs-lookup"><span data-stu-id="34579-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="34579-118">I fönstret **Montering mot kundorderrader** granskar eller ändrar du monteringsorderrader enligt den offert som kunden begär.</span><span class="sxs-lookup"><span data-stu-id="34579-118">In the **Assemble-to-Order Lines** window, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="34579-119">Om du vill ha mer information kan du välja åtgärden **Visa dokument** för att öppna hela avropsordern för offerten.</span><span class="sxs-lookup"><span data-stu-id="34579-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="34579-120">Du kan inte ändra innehållet i de flesta fält, och du kan inte bokföra.</span><span class="sxs-lookup"><span data-stu-id="34579-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="34579-121">När du har justerat monteringsorderraderna enligt offerten stänger du fönstret **Montering mot kundorderrader** så att du kommer tillbaka till fönstret **Försäljningsoffert**.</span><span class="sxs-lookup"><span data-stu-id="34579-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** window to return to the **Sales Quote** window.</span></span>  
7.  <span data-ttu-id="34579-122">Om kunden accepterar offerten skapar du en försäljningsorder för den offererade monteringsartikeln.</span><span class="sxs-lookup"><span data-stu-id="34579-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="34579-123">Mer information finns i [Skapa erbjudanden](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="34579-123">For more information, see [Make Offers](sales-how-make-offers.md).</span></span> <span data-ttu-id="34579-124">Den länkade monteringsofferten och eventuella anpassningar är kopplad till den nya försäljningsordern så att artikelmontering eller -försäljning kan förberedas.</span><span class="sxs-lookup"><span data-stu-id="34579-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34579-125">Se även</span><span class="sxs-lookup"><span data-stu-id="34579-125">See Also</span></span>  
[<span data-ttu-id="34579-126">Monteringshantering</span><span class="sxs-lookup"><span data-stu-id="34579-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="34579-127">Arbeta med strukturer</span><span class="sxs-lookup"><span data-stu-id="34579-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="34579-128">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="34579-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="34579-129">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="34579-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="34579-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34579-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

