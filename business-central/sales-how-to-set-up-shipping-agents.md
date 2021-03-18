---
title: Så här skapar du speditörer | Microsoft Docs
description: Du kan lägga upp en kod för och ange information om var och en av dina speditörer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 68c271cc452d60cef8b457f5dc1273279d9cb351
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382956"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="5aa7e-103">Så här konfigurerar du speditörer</span><span class="sxs-lookup"><span data-stu-id="5aa7e-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="5aa7e-104">Du kan lägga upp en kod för och ange information om var och en av dina speditörer.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="5aa7e-105">Om du anger en Internet-adress för speditören och denne tillhandahåller godsupplysningstjänster på Internet kan du använda den automatiska funktionen för godsupplysning.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="5aa7e-106">Mer information finns i [Så här spårar du paket](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="5aa7e-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="5aa7e-107">När du anger speditörer på dina försäljningsorder kan du också ange vilken typ av service varje speditör erbjuder.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="5aa7e-108">Du kan ange obegränsat antal tjänster för varje speditör, samt ange leveranstid för varje service.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="5aa7e-109">När en speditörsservice har kopplats till en försäljningsorderrad inkluderas leveranstiden för tjänsten i orderlöftesberäkningen för den raden.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="5aa7e-110">Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="5aa7e-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="5aa7e-111">Så här lägger du upp en speditör</span><span class="sxs-lookup"><span data-stu-id="5aa7e-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="5aa7e-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **speditör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5aa7e-113">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="5aa7e-114">.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-114">.</span></span>  
3.  <span data-ttu-id="5aa7e-115">Välj åtgärden **Speditörsservice**.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="5aa7e-116">I **Speditörsservice** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="5aa7e-117">Om du tar bort en speditör på orderraden tas även speditörsservicekoden bort.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="5aa7e-118">Därefter omberäknas innehållet i fält som delvis baserats på speditörsservicen.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5aa7e-119">Se även</span><span class="sxs-lookup"><span data-stu-id="5aa7e-119">See Also</span></span>
[<span data-ttu-id="5aa7e-120">Så här definierar du leveransmetoder</span><span class="sxs-lookup"><span data-stu-id="5aa7e-120">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)  
<span data-ttu-id="5aa7e-121">[Spåra paket](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="5aa7e-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="5aa7e-122">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="5aa7e-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5aa7e-123">Lager</span><span class="sxs-lookup"><span data-stu-id="5aa7e-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5aa7e-124">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="5aa7e-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="5aa7e-125">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="5aa7e-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="5aa7e-126">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="5aa7e-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5aa7e-127">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5aa7e-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]