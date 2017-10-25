---
title: "Så här kan du planera projektorder | Microsoft Docs"
description: "Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna i fönstret **Förs.orderplanering** används. När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av fönstret **Orderplanering**."
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
ms.openlocfilehash: 49e3ce0ef80dd54f66565f62616b3b8f2a4aaeaa
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-project-orders"></a><span data-ttu-id="a5901-104">Så här kan du planera projektorder</span><span class="sxs-lookup"><span data-stu-id="a5901-104">How to: Plan Project Orders</span></span>
<span data-ttu-id="a5901-105">Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna i fönstret **Förs.orderplanering** används.</span><span class="sxs-lookup"><span data-stu-id="a5901-105">This planning task starts from a sales order and uses the **Sales Order Planning** window.</span></span> <span data-ttu-id="a5901-106">När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="a5901-106">Once you have created a project production order, you can plan it further by using the **Order Planning** window.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="a5901-107">Så här skapar du en projektproduktionsorder</span><span class="sxs-lookup"><span data-stu-id="a5901-107">To create a project production order</span></span>  

1.  <span data-ttu-id="a5901-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a5901-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a5901-109">Markera den försäljningsorder som motsvarar produktionsprojektet och välj sedan åtgärden **planering**.</span><span class="sxs-lookup"><span data-stu-id="a5901-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="a5901-110">I fönstret **Förs.orderplanering** väljer du åtgärden **Skapa prod.order**.</span><span class="sxs-lookup"><span data-stu-id="a5901-110">In the **Sales Order Planning** window, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="a5901-111">I fönstret **Skapa order från försäljning**, i fältet **Ordertyp** markerar du **Prod.order per order**.</span><span class="sxs-lookup"><span data-stu-id="a5901-111">In the **Create Order from Sales** window, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="a5901-112">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a5901-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="a5901-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Produktionsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a5901-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="a5901-114">Öppna den produktionsorder som du skapade nyss.</span><span class="sxs-lookup"><span data-stu-id="a5901-114">Open the production order just created.</span></span>  

    <span data-ttu-id="a5901-115">Observera att fältet **Ursprungstyp** för produktionsordern visas **Försäljningshuvud**, och ordern innehåller flera rader (en för varje försäljningsradartikel som måste skapas).</span><span class="sxs-lookup"><span data-stu-id="a5901-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="a5901-116">Välj åtgärden **Planerad**.</span><span class="sxs-lookup"><span data-stu-id="a5901-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="a5901-117">I fönstret **Orderplanering** väljer du åtgärden **uppdatera** för att beräkna det nya behovet.</span><span class="sxs-lookup"><span data-stu-id="a5901-117">In the **Order Planning** window, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="a5901-118">Orderhuvudraden för projektordern visas, och alla rader med ouppfyllda behov expanderas under den.</span><span class="sxs-lookup"><span data-stu-id="a5901-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="a5901-119">Även om produktionsordern innehåller rader för flera producerade artiklar så visas det totala behovet för alla produktionsorderrader under en orderhuvudrad i fönstret **Orderplanering**, och det ursprungliga kundnamnet visas.</span><span class="sxs-lookup"><span data-stu-id="a5901-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line in the **Order Planning** window, and the original customer name is displayed.</span></span> <span data-ttu-id="a5901-120">Du kan nu fortsätta med att planera för behovet enligt beskrivningen i [Så här: Planera för nya behov per order](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="a5901-120">You can now proceed to plan for the demand as described in [How to: Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a5901-121">Behovsrader i projektproduktionsordern, som har **Prod. Order** i sitt **Återanskaffningssystem** -fält, motsvarar underliggande produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="a5901-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="a5901-122">När du har genererats dessa produktionsorder, måste du återigen beräkna en plan i fönstret **Orderplanering** för att identifiera några ouppfyllda komponentbehov för dem.</span><span class="sxs-lookup"><span data-stu-id="a5901-122">After you have generated these production orders, you must again calculate a plan in the **Order Planning** window to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="a5901-123">I så fall visas de som behovsrader under en typisk rad i ett produktionsorderhuvud, dvs. att projektrelationen inte längre visas i fönstret.</span><span class="sxs-lookup"><span data-stu-id="a5901-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible in the window.</span></span> <span data-ttu-id="a5901-124">Men om du använder orderspårningsfunktionen kan du se bakåt och framåt i alla leveransorder som skapas under den ursprungliga försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="a5901-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5901-125">Se även</span><span class="sxs-lookup"><span data-stu-id="a5901-125">See Also</span></span>
<span data-ttu-id="a5901-126">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a5901-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="a5901-127">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="a5901-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a5901-128">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a5901-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a5901-129">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="a5901-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a5901-130">Inköp</span><span class="sxs-lookup"><span data-stu-id="a5901-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a5901-131">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a5901-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="a5901-132">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="a5901-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="a5901-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5901-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

