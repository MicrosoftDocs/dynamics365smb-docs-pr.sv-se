---
title: Så här kan du planera projektorder | Microsoft Docs
description: Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna på sidan **Förs.orderplanering** används. När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av sidan **Orderplanering**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 99f60e9811827869dda6f6b79440a36d680fde60
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785977"
---
# <a name="plan-project-orders"></a><span data-ttu-id="7e8a2-104">Planera projektorder</span><span class="sxs-lookup"><span data-stu-id="7e8a2-104">Plan Project Orders</span></span>
<span data-ttu-id="7e8a2-105">Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna på sidan **Förs.orderplanering** används.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-105">This planning task starts from a sales order and uses the **Sales Order Planning** page.</span></span> <span data-ttu-id="7e8a2-106">När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av sidan **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-106">Once you have created a project production order, you can plan it further by using the **Order Planning** page.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="7e8a2-107">Så här skapar du en projektproduktionsorder</span><span class="sxs-lookup"><span data-stu-id="7e8a2-107">To create a project production order</span></span>  

1.  <span data-ttu-id="7e8a2-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7e8a2-109">Markera den försäljningsorder som motsvarar produktionsprojektet och välj sedan åtgärden **planering**.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="7e8a2-110">På sidan **Förs.orderplanering** väljer du åtgärden **Skapa prod.order**.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-110">On the **Sales Order Planning** page, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="7e8a2-111">På sidan **Skapa order från försäljning** markerar du **Ordertyp** i **Prod.order per order**.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-111">On the **Create Order from Sales** page, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="7e8a2-112">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="7e8a2-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **produktionsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="7e8a2-114">Öppna den produktionsorder som du skapade nyss.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-114">Open the production order just created.</span></span>  

    <span data-ttu-id="7e8a2-115">Observera att fältet **Ursprungstyp** för produktionsordern visas **Försäljningshuvud**, och ordern innehåller flera rader (en för varje försäljningsradartikel som måste skapas).</span><span class="sxs-lookup"><span data-stu-id="7e8a2-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="7e8a2-116">Välj åtgärden **Planerad**.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="7e8a2-117">På sidan **Orderplanering** väljer du åtgärden **uppdatera** för att beräkna det nya behovet.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-117">On the **Order Planning** page, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="7e8a2-118">Orderhuvudraden för projektordern visas, och alla rader med ouppfyllda behov expanderas under den.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="7e8a2-119">Även om produktionsordern innehåller rader för flera producerade artiklar så visas det totala behovet för alla produktionsorderrader under en orderhuvudrad på sidan **Orderplanering**, och det ursprungliga kundnamnet visas.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line on the **Order Planning** page, and the original customer name is displayed.</span></span> <span data-ttu-id="7e8a2-120">Du kan nu fortsätta med att planera för behovet enligt beskrivningen i [Planera ny behovsorder efter order](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="7e8a2-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7e8a2-121">Behovsrader i projektproduktionsordern, som har **Prod. Order** i sitt **Återanskaffningssystem** -fält, motsvarar underliggande produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="7e8a2-122">När du har genererats dessa produktionsorder, måste du återigen beräkna en plan på sidan **Orderplanering** för att identifiera några ouppfyllda komponentbehov för dem.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-122">After you have generated these production orders, you must again calculate a plan on the **Order Planning** page to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="7e8a2-123">I så fall visas de som behovsrader under en typisk rad i ett produktionsorderhuvud, dvs. att projektrelationen inte längre visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible on the page.</span></span> <span data-ttu-id="7e8a2-124">Men om du använder orderspårningsfunktionen kan du se bakåt och framåt i alla leveransorder som skapas under den ursprungliga försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="7e8a2-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e8a2-125">Se även</span><span class="sxs-lookup"><span data-stu-id="7e8a2-125">See Also</span></span>
<span data-ttu-id="7e8a2-126">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7e8a2-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="7e8a2-127">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="7e8a2-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7e8a2-128">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7e8a2-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7e8a2-129">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="7e8a2-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7e8a2-130">Inköp</span><span class="sxs-lookup"><span data-stu-id="7e8a2-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7e8a2-131">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7e8a2-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="7e8a2-132">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="7e8a2-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="7e8a2-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e8a2-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
