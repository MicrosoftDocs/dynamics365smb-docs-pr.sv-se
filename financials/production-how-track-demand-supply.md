---
title: "Hur du spårar relationer mellan tillgång och efterfrågan | Microsoft Docs"
description: "Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 511381e4f6d469ff16714a30fde60d3e238ad975
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-track-relations-between-demand-and-supply"></a><span data-ttu-id="1a716-103">Hur du spårar relationer mellan tillgång och efterfrågan</span><span class="sxs-lookup"><span data-stu-id="1a716-103">How to: Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="1a716-104">Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.</span><span class="sxs-lookup"><span data-stu-id="1a716-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="1a716-105">Planeringsförslaget omfattar också stödinformation för planeringen, till exempel enheter som inte finns på order som hjälper planeraren att ta fram en optimal leveransplan.</span><span class="sxs-lookup"><span data-stu-id="1a716-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="1a716-106">Mer information finns i avsnittet Planeringselement, inte spårat.</span><span class="sxs-lookup"><span data-stu-id="1a716-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="1a716-107">Så här spårar du länkade artiklar</span><span class="sxs-lookup"><span data-stu-id="1a716-107">To track linked items</span></span>
<span data-ttu-id="1a716-108">Orderspårningen visar hur försäljningsorder, produktionsorder och inköpsorder är relaterade till produktionsordern genom planerings- och reservationssystem.</span><span class="sxs-lookup"><span data-stu-id="1a716-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="1a716-109">Nedan beskrivs hur du spårar länkade artiklar på en fast planerad produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="1a716-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="1a716-110">Momentet är liknande för alla andra ordertyper och från planeringsförslagsraderna.</span><span class="sxs-lookup"><span data-stu-id="1a716-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="1a716-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1a716-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a716-112">Öppna relevant fast planerad produktionsorder i listan.</span><span class="sxs-lookup"><span data-stu-id="1a716-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="1a716-113">På snabbfliken **Rader** väljer du åtgärden **Funktioner** och sedan åtgärden **Orderspårning**.</span><span class="sxs-lookup"><span data-stu-id="1a716-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="1a716-114">På raderna i fönstret **Orderspårning** visas de dokument som är relaterade till den aktuella produktionsorderraden.</span><span class="sxs-lookup"><span data-stu-id="1a716-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="1a716-115">Ej spårade planeringselement</span><span class="sxs-lookup"><span data-stu-id="1a716-115">Untracked Planning Elements</span></span>
<span data-ttu-id="1a716-116">Fönstret **Ej spårade planeringselement** öppnas när du väljer fönstret **ej spårat antal** i fönstret **orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="1a716-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="1a716-117">Den har två syften:</span><span class="sxs-lookup"><span data-stu-id="1a716-117">It serves two purposes:</span></span>

1. <span data-ttu-id="1a716-118">Den innehåller information om ej spårade kvantiteter, som visas när användaren vill se ej spårade kvantiteter från fönstret Orderspårning .</span><span class="sxs-lookup"><span data-stu-id="1a716-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="1a716-119">Den innehåller varningsmeddelanden som visas när användaren klickar på en **varningsikon** i fönstret **planeringsförslag**.</span><span class="sxs-lookup"><span data-stu-id="1a716-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="1a716-120">Fönstret innehåller poster som redogör för en överskottskvantitet i orderspårningsnätverket.</span><span class="sxs-lookup"><span data-stu-id="1a716-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="1a716-121">Dessa poster skapas under planeringen och förklarar var den ej spårade överskottskvantiteten på orderspårningsraderna kommer ifrån.</span><span class="sxs-lookup"><span data-stu-id="1a716-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="1a716-122">Överskottet som inte har spårats kan komma från:</span><span class="sxs-lookup"><span data-stu-id="1a716-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="1a716-123">Produktionsprognos</span><span class="sxs-lookup"><span data-stu-id="1a716-123">Production forecast</span></span>
- <span data-ttu-id="1a716-124">Avropsorder</span><span class="sxs-lookup"><span data-stu-id="1a716-124">Blanket orders</span></span>
- <span data-ttu-id="1a716-125">Säkerhetslager</span><span class="sxs-lookup"><span data-stu-id="1a716-125">Safety stock quantity</span></span>
- <span data-ttu-id="1a716-126">Beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="1a716-126">Reorder point</span></span>
- <span data-ttu-id="1a716-127">Beställningsgräns</span><span class="sxs-lookup"><span data-stu-id="1a716-127">Maximum inventory</span></span>
- <span data-ttu-id="1a716-128">Beställningsantal</span><span class="sxs-lookup"><span data-stu-id="1a716-128">Reorder quantity</span></span>
- <span data-ttu-id="1a716-129">Max. partistorlek</span><span class="sxs-lookup"><span data-stu-id="1a716-129">Maximum order quantity</span></span>
- <span data-ttu-id="1a716-130">Min. partistorlek</span><span class="sxs-lookup"><span data-stu-id="1a716-130">Minimum order quantity</span></span>
- <span data-ttu-id="1a716-131">Partistorleksmultipel</span><span class="sxs-lookup"><span data-stu-id="1a716-131">Order multiple</span></span>
- <span data-ttu-id="1a716-132">Dämpare (% partistorlek)</span><span class="sxs-lookup"><span data-stu-id="1a716-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="1a716-133">Se även</span><span class="sxs-lookup"><span data-stu-id="1a716-133">See Also</span></span>  
<span data-ttu-id="1a716-134">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="1a716-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="1a716-135">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="1a716-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1a716-136">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1a716-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1a716-137">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="1a716-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1a716-138">Inköp</span><span class="sxs-lookup"><span data-stu-id="1a716-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="1a716-139">Designdetaljer: Reservation, spårning och åtgärdsmeddelanden</span><span class="sxs-lookup"><span data-stu-id="1a716-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="1a716-140">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="1a716-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="1a716-141">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="1a716-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="1a716-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a716-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
