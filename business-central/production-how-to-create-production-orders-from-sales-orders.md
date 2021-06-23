---
title: Så här skapar du produktionsorder från försäljningsorder
description: Du kan skapa produktionsorder från försäljningsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115242"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="ef44b-103">Så här skapar du produktionsorder från försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="ef44b-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="ef44b-104">Du kan skapa produktionsorder för producerade artiklar direkt från försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="ef44b-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="ef44b-105">Så här skapar du produktionsorder från försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="ef44b-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="ef44b-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ef44b-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ef44b-107">Markera den försäljningsorder som du vill skapa en produktionsorder för.</span><span class="sxs-lookup"><span data-stu-id="ef44b-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="ef44b-108">Välj åtgärden **Planerad**.</span><span class="sxs-lookup"><span data-stu-id="ef44b-108">Choose the **Planning** action.</span></span> <span data-ttu-id="ef44b-109">På sidan **Förs.orderplanering** kan du visa dispositionen för artikeln på i ordern.</span><span class="sxs-lookup"><span data-stu-id="ef44b-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="ef44b-110">Välj åtgärden **Skapa prod.order**.</span><span class="sxs-lookup"><span data-stu-id="ef44b-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="ef44b-111">Välj status och ordertyp.</span><span class="sxs-lookup"><span data-stu-id="ef44b-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="ef44b-112">Tryck på knappen **Ja** för att skapa en eller flera produktionsorder för raderna som har **Prod.order** i fältet **Återanskaffningssystem**.</span><span class="sxs-lookup"><span data-stu-id="ef44b-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="ef44b-113">Behovsrader i den skapade produktionsordern, som har **Prod.order** i sitt **Återanskaffningssystem**-fält, motsvarar underliggande produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ef44b-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="ef44b-114">När du har genererat dessa produktionsorder får du inte glömma att att identifiera ouppfyllda komponentbehov för dem med sidan **Orderplanering** eller funktionen **Omplanering** från skapade order.</span><span class="sxs-lookup"><span data-stu-id="ef44b-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="ef44b-115">Ordertyp</span><span class="sxs-lookup"><span data-stu-id="ef44b-115">Order type</span></span>  
<span data-ttu-id="ef44b-116">Du kan välja mellan två olika sätt att skapa produktionsorder enligt vad som beskrivs i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="ef44b-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="ef44b-117">Alternativ</span><span class="sxs-lookup"><span data-stu-id="ef44b-117">Option</span></span>|<span data-ttu-id="ef44b-118">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ef44b-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="ef44b-119">Artikelorder</span><span class="sxs-lookup"><span data-stu-id="ef44b-119">Item Order</span></span>|<span data-ttu-id="ef44b-120">En produktionsorder skapas för varje nödvändig produktionsorder som representeras av en rad i fönstret **Försäljningsorderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ef44b-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="ef44b-121">Projektorder</span><span class="sxs-lookup"><span data-stu-id="ef44b-121">Project Order</span></span>|<span data-ttu-id="ef44b-122">En produktionsorder skapas för varje nödvändig produktionsorder som representeras av en rad i fönstret **Försäljningsorderplanering**.</span><span class="sxs-lookup"><span data-stu-id="ef44b-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="ef44b-123">När du använder projektorder innehåller fältet **Ursprungstyp** för produktionsordern **Försäljningshuvud**, och ordern innehåller flera rader (en för varje försäljningsradartikel som måste skapas).</span><span class="sxs-lookup"><span data-stu-id="ef44b-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="ef44b-124">Se även</span><span class="sxs-lookup"><span data-stu-id="ef44b-124">See Also</span></span>  
[<span data-ttu-id="ef44b-125">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="ef44b-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ef44b-126">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ef44b-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ef44b-127">Lager</span><span class="sxs-lookup"><span data-stu-id="ef44b-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ef44b-128">Inköp</span><span class="sxs-lookup"><span data-stu-id="ef44b-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ef44b-129">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="ef44b-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="ef44b-130">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="ef44b-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="ef44b-131">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef44b-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
