---
title: Hur du spårar relationer mellan tillgång och efterfrågan | Microsoft Docs
description: Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ba774a7f7ba93c132e10e19f61b7df9cf825e7a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383231"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="8c654-103">Spåra relationer mellan tillgång och efterfrågan</span><span class="sxs-lookup"><span data-stu-id="8c654-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="8c654-104">Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.</span><span class="sxs-lookup"><span data-stu-id="8c654-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="8c654-105">Planeringsförslaget omfattar också stödinformation för planeringen, till exempel enheter som inte finns på order som hjälper planeraren att ta fram en optimal leveransplan.</span><span class="sxs-lookup"><span data-stu-id="8c654-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="8c654-106">Mer information finns i [Planeringselement, inte spårat](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="8c654-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="8c654-107">Så här spårar du länkade artiklar</span><span class="sxs-lookup"><span data-stu-id="8c654-107">To track linked items</span></span>
<span data-ttu-id="8c654-108">Orderspårningen visar hur försäljningsorder, produktionsorder och inköpsorder är relaterade till produktionsordern genom planerings- och reservationssystem.</span><span class="sxs-lookup"><span data-stu-id="8c654-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="8c654-109">Nedan beskrivs hur du spårar länkade artiklar på en fast planerad produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="8c654-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="8c654-110">Momentet är liknande för alla andra ordertyper och från planeringsförslagsraderna.</span><span class="sxs-lookup"><span data-stu-id="8c654-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="8c654-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8c654-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c654-112">Öppna relevant fast planerad produktionsorder i listan.</span><span class="sxs-lookup"><span data-stu-id="8c654-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="8c654-113">På snabbfliken **Rader** väljer du åtgärden **Funktioner** och sedan åtgärden **Orderspårning**.</span><span class="sxs-lookup"><span data-stu-id="8c654-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="8c654-114">På raderna i fönstret **Orderspårning** visas de dokument som är relaterade till den aktuella produktionsorderraden.</span><span class="sxs-lookup"><span data-stu-id="8c654-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="8c654-115">Ej spårade planeringselement</span><span class="sxs-lookup"><span data-stu-id="8c654-115">Untracked Planning Elements</span></span>
<span data-ttu-id="8c654-116">Sidan **Ej spårade planeringselement** öppnas när du väljer sidan **ej spårat antal** på sidan **orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="8c654-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="8c654-117">Den har två syften:</span><span class="sxs-lookup"><span data-stu-id="8c654-117">It serves two purposes:</span></span>

1. <span data-ttu-id="8c654-118">Den innehåller information om ej spårade kvantiteter, som visas när användaren vill se ej spårade kvantiteter från sidan Orderspårning .</span><span class="sxs-lookup"><span data-stu-id="8c654-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="8c654-119">Den innehåller varningsmeddelanden som visas när användaren klickar på en **varningsikon** på sidan **planeringsförslag**.</span><span class="sxs-lookup"><span data-stu-id="8c654-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="8c654-120">Sidan innehåller poster som redogör för en överskottskvantitet i orderspårningsnätverket.</span><span class="sxs-lookup"><span data-stu-id="8c654-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="8c654-121">Dessa poster skapas under planeringen och förklarar var den ej spårade överskottskvantiteten på orderspårningsraderna kommer ifrån.</span><span class="sxs-lookup"><span data-stu-id="8c654-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="8c654-122">Överskottet som inte har spårats kan komma från:</span><span class="sxs-lookup"><span data-stu-id="8c654-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="8c654-123">Produktionsprognos</span><span class="sxs-lookup"><span data-stu-id="8c654-123">Production forecast</span></span>
- <span data-ttu-id="8c654-124">Avropsorder</span><span class="sxs-lookup"><span data-stu-id="8c654-124">Blanket orders</span></span>
- <span data-ttu-id="8c654-125">Säkerhetslager</span><span class="sxs-lookup"><span data-stu-id="8c654-125">Safety stock quantity</span></span>
- <span data-ttu-id="8c654-126">Beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="8c654-126">Reorder point</span></span>
- <span data-ttu-id="8c654-127">Beställningsgräns</span><span class="sxs-lookup"><span data-stu-id="8c654-127">Maximum inventory</span></span>
- <span data-ttu-id="8c654-128">Beställningsantal</span><span class="sxs-lookup"><span data-stu-id="8c654-128">Reorder quantity</span></span>
- <span data-ttu-id="8c654-129">Max. partistorlek</span><span class="sxs-lookup"><span data-stu-id="8c654-129">Maximum order quantity</span></span>
- <span data-ttu-id="8c654-130">Min. partistorlek</span><span class="sxs-lookup"><span data-stu-id="8c654-130">Minimum order quantity</span></span>
- <span data-ttu-id="8c654-131">Partistorleksmultipel</span><span class="sxs-lookup"><span data-stu-id="8c654-131">Order multiple</span></span>
- <span data-ttu-id="8c654-132">Dämpare (% partistorlek)</span><span class="sxs-lookup"><span data-stu-id="8c654-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="8c654-133">Se även</span><span class="sxs-lookup"><span data-stu-id="8c654-133">See Also</span></span>  
<span data-ttu-id="8c654-134">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="8c654-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="8c654-135">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="8c654-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="8c654-136">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="8c654-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="8c654-137">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="8c654-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8c654-138">Inköp</span><span class="sxs-lookup"><span data-stu-id="8c654-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="8c654-139">Designdetaljer: Reservation, spårning och åtgärdsmeddelanden</span><span class="sxs-lookup"><span data-stu-id="8c654-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="8c654-140">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="8c654-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="8c654-141">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="8c654-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="8c654-142">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c654-142">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]