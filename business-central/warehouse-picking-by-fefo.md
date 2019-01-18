---
title: "Så här: Aktivera plockning med FEFO | Microsoft Docs"
description: "FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklar, de med de tidigaste utgångsdatumen, plockas först."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 54857d668cdceb9cc1d4e035a496d621b1d9459b
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="3d95a-103">Aktivera plockning av artiklar med FEFO</span><span class="sxs-lookup"><span data-stu-id="3d95a-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="3d95a-104">FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklarna - de med tidigast utgångsdatum - plockas först.</span><span class="sxs-lookup"><span data-stu-id="3d95a-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="3d95a-105">Den här funktionen fungerar bara, när dessa villkor är uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="3d95a-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="3d95a-106">Artikel måste ha en serie-/partinummer.</span><span class="sxs-lookup"><span data-stu-id="3d95a-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="3d95a-107">På artikelns artikelspårningskod har angetts, fältet **SN specifik spårning för dist.lager** , eller **Parti specifik spårning distr.lager** måste väljas.</span><span class="sxs-lookup"><span data-stu-id="3d95a-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="3d95a-108">Artikeln måste bokföras till lagret med ett utgångsdatum.</span><span class="sxs-lookup"><span data-stu-id="3d95a-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="3d95a-109">På lagerställekortet måste kryssrutan **Begär plockning** vara markerad.</span><span class="sxs-lookup"><span data-stu-id="3d95a-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="3d95a-110">Kryssrutan **Plocka enligt FEFO** på lagerställekortet måste vara markerat.</span><span class="sxs-lookup"><span data-stu-id="3d95a-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="3d95a-111">På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.</span><span class="sxs-lookup"><span data-stu-id="3d95a-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="3d95a-112">När alla villkor uppfylls, sorteras serie-/partinumrerade artiklar som ska plockas med de äldsta första alla plockningar och transporter, utom artiklar som använder SN-närmare visst eller partispecifik spårning.</span><span class="sxs-lookup"><span data-stu-id="3d95a-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="3d95a-113">Om någon serie-/partinumrerade artiklar använder specifik spårning, är de respekterade först och under dem, listas de återstående, icke-specifika serie-/partinummer enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="3d95a-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="3d95a-114">Om två serie-/partinumrerade artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie - eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="3d95a-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="3d95a-115">När du plockar serie-/partinumrerade artiklar på lagerplatser som har ställs in för dirigerad artikelinförsel och plockning, plockas bara kvantiteter på lagerplatser av typen *Plock* enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="3d95a-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="3d95a-116">Om du vill aktivera transporter enligt FEFO antingen på sidan **Lagerförflyttning** eller på sidan **Transportförslag**, måste du lämna fältet **Från lagerplats** tomt.</span><span class="sxs-lookup"><span data-stu-id="3d95a-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="3d95a-117">Om fältet **Endast utgångsbokföring** är markerat kommer endast artiklar som inte har förfallit att tas med i plockningen.</span><span class="sxs-lookup"><span data-stu-id="3d95a-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="3d95a-118">Detta gäller även om du inte använder plockning enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="3d95a-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d95a-119">Se även</span><span class="sxs-lookup"><span data-stu-id="3d95a-119">See Also</span></span>  
<span data-ttu-id="3d95a-120">[Plocka artiklar](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="3d95a-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="3d95a-121">[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="3d95a-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="3d95a-122">[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="3d95a-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="3d95a-123">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="3d95a-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="3d95a-124">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="3d95a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3d95a-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d95a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

