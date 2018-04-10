---
title: "Bokföra komponenter utifrån operationens utflöde | Microsoft Docs"
description: "För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**. Mer information finns i  Bokföringsmetod."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4d2109a462d5d1a755cf7ffaf45129bec2234376
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="47f71-104">Bokföra komponenter utifrån verksamhetens utflöde</span><span class="sxs-lookup"><span data-stu-id="47f71-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="47f71-105">För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**.</span><span class="sxs-lookup"><span data-stu-id="47f71-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="47f71-106">Om du definierar verksamhetsföljdslänkkoder också utförs beräkning och bokföring när varje operation har slutförts, och antal, som faktiskt förbrukades i operationen, bokförs.</span><span class="sxs-lookup"><span data-stu-id="47f71-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="47f71-107">Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="47f71-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="47f71-108">Om t.ex. en produktionsorder för att kunna producera 800 meter kräver 8 kg av en komponent så, när du bokför 200 meter som utflöde, bokförs 2 kg automatiskt som förbrukning.</span><span class="sxs-lookup"><span data-stu-id="47f71-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="47f71-109">Den här funktionen är användbar för följande:</span><span class="sxs-lookup"><span data-stu-id="47f71-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="47f71-110">**Lagervärdering** - värdetransaktioner för förbrukning och utflöde har skapats parallellt, i takt med att produktionsordern fortskrider.</span><span class="sxs-lookup"><span data-stu-id="47f71-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="47f71-111">Utan verksamhetsföljdslänkkoder minskar lagervärdet när utflödet bokförs och ökar sedan vid en senare tidpunkt, när värdet för komponentförbrukning bokförs tillsammans med färdig produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="47f71-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="47f71-112">**Lagerdispositionen** - med tidsfasad förbrukningsbokföring, är tillgängligheten till komponentartiklarna mer uppdaterad, vilket är viktigt för att underhålla det interna saldot mellan tillgång och efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="47f71-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="47f71-113">Utan verksamhetsföljdslänkkoder kan andra behov av komponenten tro att den är tillgänglig så länge det finns en väntande försenad förbrukningsbokföring.</span><span class="sxs-lookup"><span data-stu-id="47f71-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="47f71-114">**JIT** – med möjligheten att anpassa produkter till pågående kundförfrågningar kan du reducera kassation genom att se till att arbets- och systemändringar endast görs när det behövs.</span><span class="sxs-lookup"><span data-stu-id="47f71-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="47f71-115">Följande procedur visar hur kopplingskoder för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen.</span><span class="sxs-lookup"><span data-stu-id="47f71-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="47f71-116">Bokföra komponenter utifrån operationens utflöde</span><span class="sxs-lookup"><span data-stu-id="47f71-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="47f71-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47f71-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="47f71-118">Välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="47f71-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="47f71-119">På snabbfliken **Återanskaffning**, i fältet **Bokföringsmetod**, markera **framåt**.</span><span class="sxs-lookup"><span data-stu-id="47f71-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="47f71-120">Välj **Plocka + framåt** om komponenten ska användas på ett lagerställe som har skapats för dirigerad artikelinförsel och plockning.</span><span class="sxs-lookup"><span data-stu-id="47f71-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="47f71-121">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Operationsföljder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47f71-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="47f71-122">Definiera verksamhetsföljdslänkkoder för varje operation som förbrukar komponenten.</span><span class="sxs-lookup"><span data-stu-id="47f71-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="47f71-123">Mer information finns i [Skapa verksamhetsföljder ](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="47f71-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="47f71-124">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Prod.struktur**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47f71-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="47f71-125">Definiera verksamhetsföljdslänkkoder från varje instans av komponenten till operationen där den förbrukas.</span><span class="sxs-lookup"><span data-stu-id="47f71-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="47f71-126">Komponenten måste ha en verksamhetsföljdlänk till den sista operationen i verksamhetsföljden.</span><span class="sxs-lookup"><span data-stu-id="47f71-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="47f71-127">Se även</span><span class="sxs-lookup"><span data-stu-id="47f71-127">See Also</span></span>  
[<span data-ttu-id="47f71-128">Skapa produktionsstrukturer</span><span class="sxs-lookup"><span data-stu-id="47f71-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="47f71-129">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="47f71-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="47f71-130">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="47f71-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="47f71-131">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="47f71-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="47f71-132">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47f71-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="47f71-133">Inköp</span><span class="sxs-lookup"><span data-stu-id="47f71-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="47f71-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="47f71-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
