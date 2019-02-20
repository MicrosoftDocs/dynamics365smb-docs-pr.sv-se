---
title: "Så här skapar du monteringsorder för avrop | Microsoft Docs"
description: "Om fältet **Återanskaffningssystem** på artikelkortet innehåller **Montering** så är standard metoden för att tillhandahålla artikeln att sammanställa den av definierade komponenter, eventuellt med en angiven resurs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 12/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5801fcc1284edfe1b8578518c084455c336d5a40
ms.openlocfilehash: 8796ccf6ce73ded327fad35573a2268e249fb7a7
ms.contentlocale: sv-se
ms.lasthandoff: 12/27/2018

---
# <a name="create-blanket-assembly-orders"></a><span data-ttu-id="80308-103">Skapa monteringsorder för avrop</span><span class="sxs-lookup"><span data-stu-id="80308-103">Create Blanket Assembly Orders</span></span>
<span data-ttu-id="80308-104">Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="80308-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="80308-105">Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="80308-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

 <span data-ttu-id="80308-106">Som med alla typer av artiklar kan du också skapa avropsförsäljningsorder för anpassade monteringsartiklar före periodens skapande av faktiska försäljningsorder enligt avropsorderavtalet.</span><span class="sxs-lookup"><span data-stu-id="80308-106">As with any other type of item, you can also create blanket sales orders for customized assembly items before periodically making the actual sales orders according to the blanket order agreement.</span></span> <span data-ttu-id="80308-107">Den här processen involverar flera extra steg i jämförelse med att skapa en vanlig avropsförsäljningsorder. Den använder en variation av en kopplad monteringsorder, dvs. en monteringsorder för avrop.</span><span class="sxs-lookup"><span data-stu-id="80308-107">This process involves several extra steps when you compare it to creating a regular blanket sales order, and it uses a variation of a linked assembly order, which is a blanket assembly order.</span></span>

> [!NOTE]  
>  <span data-ttu-id="80308-108">Som för alla avropsorder är antalet i monteringsavropsorder endast prognoser och kan inte användas förrän de konverterats till faktiska monteringsorder.</span><span class="sxs-lookup"><span data-stu-id="80308-108">Like all blanket orders, quantities on assembly blanket orders are only forecasts and are not operational until they are converted to actual assembly orders.</span></span> <span data-ttu-id="80308-109">Därför är orderfunktioner som dispositionsberäkning, reservation och artikelspårning inte aktiva för monteringsorder för avrop.</span><span class="sxs-lookup"><span data-stu-id="80308-109">Therefore, order functionality, such as availability calculation, reservation, and item tracking, is not active on blanket assembly orders.</span></span>  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><span data-ttu-id="80308-110">Så här skapar du en monteringsorder för avrop för montering\-mot\-kundorder</span><span class="sxs-lookup"><span data-stu-id="80308-110">To create a blanket assembly order for an assemble\-to\-order item</span></span>  
1. <span data-ttu-id="80308-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Förs.avropsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="80308-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="80308-112">Skapa en ny avropsorder med en rad för en monteringsartikel.</span><span class="sxs-lookup"><span data-stu-id="80308-112">Create a new blanket sales order with one line for an assembly item.</span></span> <span data-ttu-id="80308-113">Mer information finns i [Skapa försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="80308-113">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>  
3. <span data-ttu-id="80308-114">I fältet **Antal att montera mot kundorder** på monteringsorderraden anger du det totala antalet.</span><span class="sxs-lookup"><span data-stu-id="80308-114">In the **Qty. to Assemble to Order** field on the blanket assembly order line, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="80308-115">Du bör inte skapa avropsorderavtal för delvisa antal.</span><span class="sxs-lookup"><span data-stu-id="80308-115">You should not create blanket order agreements for a partial quantity.</span></span> <span data-ttu-id="80308-116">Därför måste du ange samma antal som du angett i fältet **Antal** på avropsorderraden.</span><span class="sxs-lookup"><span data-stu-id="80308-116">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the blanket sales order line.</span></span>  

4. <span data-ttu-id="80308-117">Välj åtgärden **Montering mot kundorder** och välj sedan åtgärden **Montering mot kundorderrader**.</span><span class="sxs-lookup"><span data-stu-id="80308-117">Choose the **Assemble to Order** action, and then choose the **Assemble-to-Order Lines** action.</span></span> <span data-ttu-id="80308-118">Alternativt kan du välja fältet **Antal att montera mot kundorder** på raden.</span><span class="sxs-lookup"><span data-stu-id="80308-118">Alternatively, choose the **Qty. to Assemble to Order)** field on the line.</span></span>  
5. <span data-ttu-id="80308-119">På sidan **Montering mot kundorderrader** granskar eller ändrar du monteringsorderrader enligt avropsorderavtalet som du har gjort med kunden.</span><span class="sxs-lookup"><span data-stu-id="80308-119">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the blanket order agreement that you have made with the customer.</span></span> <span data-ttu-id="80308-120">Om du vill ha mer information kan du välja åtgärden **Visa dokument** för att öppna hela avropsförsäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="80308-120">If you want to view more information, choose the **Show Document** action to open the complete blanket assembly order.</span></span> <span data-ttu-id="80308-121">Du kan inte ändra innehållet i de flesta fält, och du kan inte bokföra.</span><span class="sxs-lookup"><span data-stu-id="80308-121">You cannot change the contents of most fields, and you cannot post.</span></span>  
6. <span data-ttu-id="80308-122">När du har justerat monteringsorderraderna enligt avropsorderavtalet stänger du sidan **Montering mot kundorderrader** så att du kommer tillbaka till sidan **Förs.avropsorder**.</span><span class="sxs-lookup"><span data-stu-id="80308-122">When you have adjusted the assembly order lines according to the blanket order agreement, close the **Assemble-to-Order Lines** page to return to the **Blanket Sales Order** page.</span></span>  
7. <span data-ttu-id="80308-123">När kunden efterfrågar en försäljningsorder baserat på den överenskomna avropsordern, skapar du en försäljningsorder för den överenskomna monteringsartikeln eller artiklarna.</span><span class="sxs-lookup"><span data-stu-id="80308-123">When the customer requests to create a sales order based on the agreed blanket sales order, create a sales order for the agreed assembly item or items.</span></span> <span data-ttu-id="80308-124">Mer information finns i [Skapa försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="80308-124">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>

<span data-ttu-id="80308-125">Den länkade avropsmonteringsofferten och eventuella anpassningar är kopplade till den nya försäljningsordern så att artikelmontering eller -försäljning kan förberedas.</span><span class="sxs-lookup"><span data-stu-id="80308-125">The linked blanket assembly order and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="80308-126">Se även</span><span class="sxs-lookup"><span data-stu-id="80308-126">See Also</span></span>
[<span data-ttu-id="80308-127">Skapa försäljningsavropsorder</span><span class="sxs-lookup"><span data-stu-id="80308-127">Create Blanket Sales Orders</span></span>](sales-how-to-create-blanket-sales-orders.md)  
[<span data-ttu-id="80308-128">Monteringshantering</span><span class="sxs-lookup"><span data-stu-id="80308-128">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="80308-129">Arbeta med strukturer</span><span class="sxs-lookup"><span data-stu-id="80308-129">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="80308-130">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="80308-130">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="80308-131">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="80308-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="80308-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80308-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

