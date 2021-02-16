---
title: Bokföra komponenter utifrån operationens utflöde | Microsoft Docs
description: För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**. Mer information finns i  Bokföringsmetod.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f7f6c0c4be56c5f7e25f44063923cfe02e03e4c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759298"
---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="e0df1-104">Bokföra komponenter utifrån verksamhetens utflöde</span><span class="sxs-lookup"><span data-stu-id="e0df1-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="e0df1-105">För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**.</span><span class="sxs-lookup"><span data-stu-id="e0df1-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="e0df1-106">Om du definierar verksamhetsföljdslänkkoder också utförs beräkning och bokföring när varje operation har slutförts, och antal, som faktiskt förbrukades i operationen, bokförs.</span><span class="sxs-lookup"><span data-stu-id="e0df1-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="e0df1-107">Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="e0df1-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="e0df1-108">Om t.ex. en produktionsorder för att kunna producera 800 meter kräver 8 kg av en komponent så, när du bokför 200 meter som utflöde, bokförs 2 kg automatiskt som förbrukning.</span><span class="sxs-lookup"><span data-stu-id="e0df1-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="e0df1-109">Den här funktionen är användbar för följande:</span><span class="sxs-lookup"><span data-stu-id="e0df1-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="e0df1-110">**Lagervärdering** – värdetransaktioner för förbrukning och utflöde har skapats parallellt, i takt med att produktionsordern fortskrider.</span><span class="sxs-lookup"><span data-stu-id="e0df1-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="e0df1-111">Utan verksamhetsföljdslänkkoder minskar lagervärdet när utflödet bokförs och ökar sedan vid en senare tidpunkt, när värdet för komponentförbrukning bokförs tillsammans med färdig produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e0df1-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="e0df1-112">**Lagerdispositionen** – med tidsfasad förbrukningsbokföring, är tillgängligheten till komponentartiklarna mer uppdaterad, vilket är viktigt för att underhålla det interna saldot mellan tillgång och efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="e0df1-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="e0df1-113">Utan verksamhetsföljdslänkkoder kan andra behov av komponenten tro att den är tillgänglig så länge det finns en väntande försenad förbrukningsbokföring.</span><span class="sxs-lookup"><span data-stu-id="e0df1-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="e0df1-114">**JIT** – med möjligheten att anpassa produkter till pågående kundförfrågningar kan du reducera kassation genom att se till att arbets- och systemändringar endast görs när det behövs.</span><span class="sxs-lookup"><span data-stu-id="e0df1-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="e0df1-115">Följande procedur visar hur kopplingskoder för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen.</span><span class="sxs-lookup"><span data-stu-id="e0df1-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="e0df1-116">Bokföra komponenter utifrån operationens utflöde</span><span class="sxs-lookup"><span data-stu-id="e0df1-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="e0df1-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e0df1-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e0df1-118">Välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="e0df1-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="e0df1-119">På snabbfliken **Återanskaffning**, i fältet **Bokföringsmetod**, markera **framåt**.</span><span class="sxs-lookup"><span data-stu-id="e0df1-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e0df1-120">Välj **Plocka + framåt** om komponenten ska användas på ett lagerställe som har skapats för dirigerad artikelinförsel och plockning.</span><span class="sxs-lookup"><span data-stu-id="e0df1-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="e0df1-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **verksamhetsföljder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e0df1-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="e0df1-122">Definiera verksamhetsföljdslänkkoder för varje operation som förbrukar komponenten.</span><span class="sxs-lookup"><span data-stu-id="e0df1-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="e0df1-123">Mer information finns i [Skapa verksamhetsföljder ](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="e0df1-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="e0df1-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Prod.struktur** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e0df1-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="e0df1-125">Definiera verksamhetsföljdslänkkoder från varje instans av komponenten till operationen där den förbrukas.</span><span class="sxs-lookup"><span data-stu-id="e0df1-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="e0df1-126">Komponenten måste ha en verksamhetsföljdlänk till den sista operationen i verksamhetsföljden.</span><span class="sxs-lookup"><span data-stu-id="e0df1-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0df1-127">Se även</span><span class="sxs-lookup"><span data-stu-id="e0df1-127">See Also</span></span>  
[<span data-ttu-id="e0df1-128">Skapa produktionsstrukturer</span><span class="sxs-lookup"><span data-stu-id="e0df1-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="e0df1-129">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="e0df1-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e0df1-130">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e0df1-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="e0df1-131">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e0df1-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="e0df1-132">Lager</span><span class="sxs-lookup"><span data-stu-id="e0df1-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e0df1-133">Inköp</span><span class="sxs-lookup"><span data-stu-id="e0df1-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e0df1-134">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e0df1-134">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
