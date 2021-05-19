---
title: Batch-bokför förbrukning
description: Om bokföringsmetoden är Manuell, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935192"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="93318-103">Batch-bokföra produktionsförbrukning</span><span class="sxs-lookup"><span data-stu-id="93318-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="93318-104">Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="93318-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="93318-105">Om du har markerat fältet **Begär plockning** på lagerställekortet för att ange att lagerstället kräver bearbetning av lagerplockning, behöver du inte använda det här batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="93318-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="93318-106">hanterar förbrukningen när du bokför lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="93318-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="93318-107">Mer information finns i [Plocka för produktion i grundläggande distributionslagerkonfigurationer](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="93318-107">For more information, see [Pick for Production in Basic Warehouse Configurations](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span></span>  

<span data-ttu-id="93318-108">Du kan också ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="93318-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="93318-109">Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="93318-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="93318-110">Om du vill bokföra förbrukning för produktion av en eller flera rader</span><span class="sxs-lookup"><span data-stu-id="93318-110">To post consumption for one or more production order lines</span></span>

1. <span data-ttu-id="93318-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **förbrukningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="93318-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93318-112">Fyll i fälten med data om produktionsorden och om förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="93318-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="93318-113">Använd åtgärden **Beräkna förbrukning** för att generera journalrader från produktionsorder baserat på faktiskt utflöde (den mängd färdiga varor som du har rapporterat) eller på förväntat utflöde (den mängd färdiga varor som förväntas produceras).</span><span class="sxs-lookup"><span data-stu-id="93318-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="93318-114">Om du har konfigurerat platskortet för att kräva bearbetning av lagerplockning kan endast kvantiteter som redan plockas genom en lageraktivitet anges i fältet **Antal** på sidan **Förbrukningsjournal** inte någon beräknad kvantitet..</span><span class="sxs-lookup"><span data-stu-id="93318-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="93318-115">Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="93318-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3. <span data-ttu-id="93318-116">Välj åtgärden **Bokför** om du vill bokföra förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="93318-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="93318-117">De relaterade varulagret minskas.</span><span class="sxs-lookup"><span data-stu-id="93318-117">The related inventories are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="93318-118">Se även</span><span class="sxs-lookup"><span data-stu-id="93318-118">See Also</span></span>

[<span data-ttu-id="93318-119">Produktion</span><span class="sxs-lookup"><span data-stu-id="93318-119">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="93318-120">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="93318-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="93318-121">Planerad</span><span class="sxs-lookup"><span data-stu-id="93318-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="93318-122">Lager</span><span class="sxs-lookup"><span data-stu-id="93318-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="93318-123">Inköp</span><span class="sxs-lookup"><span data-stu-id="93318-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="93318-124">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="93318-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]
