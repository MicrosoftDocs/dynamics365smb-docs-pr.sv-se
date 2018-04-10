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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e4ee3dc56de6c4ca6b6229c0b436c9407d73534a
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="aa290-103">Aktivera plockning av artiklar med FEFO</span><span class="sxs-lookup"><span data-stu-id="aa290-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="aa290-104">FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklarna - de med tidigast utgångsdatum - plockas först.</span><span class="sxs-lookup"><span data-stu-id="aa290-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="aa290-105">Den här funktionen fungerar bara, när dessa villkor är uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="aa290-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="aa290-106">Artikel måste ha en serie-/partinummer.</span><span class="sxs-lookup"><span data-stu-id="aa290-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="aa290-107">På artikelns artikelspårningskod har angetts, fältet **SN specifik spårning för dist.lager** , eller **Parti specifik spårning distr.lager** måste väljas.</span><span class="sxs-lookup"><span data-stu-id="aa290-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="aa290-108">Artikeln måste bokföras till lagret med ett utgångsdatum.</span><span class="sxs-lookup"><span data-stu-id="aa290-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="aa290-109">På lagerställekortet måste kryssrutan **Begär plockning** vara markerad.</span><span class="sxs-lookup"><span data-stu-id="aa290-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="aa290-110">Kryssrutan **Plocka enligt FEFO** på lagerställekortet måste vara markerat.</span><span class="sxs-lookup"><span data-stu-id="aa290-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="aa290-111">På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.</span><span class="sxs-lookup"><span data-stu-id="aa290-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="aa290-112">När alla villkor uppfylls, sorteras serie-/partinumrerade artiklar som ska plockas med de äldsta första alla plockningar och transporter, utom artiklar som använder SN-närmare visst eller partispecifik spårning.</span><span class="sxs-lookup"><span data-stu-id="aa290-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="aa290-113">Om någon serie-/partinumrerade artiklar använder specifik spårning, är de respekterade först och under dem, listas de återstående, icke-specifika serie-/partinummer enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="aa290-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>  

 <span data-ttu-id="aa290-114">Om två serie-/partinumrerade artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie - eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="aa290-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span> <span data-ttu-id="aa290-115">Om serie - eller partinummer är samma, väljs artikeln som registrerades först.</span><span class="sxs-lookup"><span data-stu-id="aa290-115">If the serial or lot numbers are the same, then the program selects the item that was registered first.</span></span>  

> [!NOTE]  
>  -   <span data-ttu-id="aa290-116">När du plockar serie-/partinumrerade artiklar på lagerplatser som har ställs in för dirigerad artikelinförsel och plockning, plockas bara kvantiteter på lagerplatser av typen *Plock* enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="aa290-116">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
> -   <span data-ttu-id="aa290-117">Om du vill aktivera transporter enligt FEFO antingen i **lagerförflyttning** fönster eller **Transportkalkylark** fönstret, måste du lämna **Från binge** fältet tomt.</span><span class="sxs-lookup"><span data-stu-id="aa290-117">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
> -   <span data-ttu-id="aa290-118">Om fältet **Endast utgångsbokföring** är markerat kommer endast artiklar som inte har förfallit att tas med i plockningen.</span><span class="sxs-lookup"><span data-stu-id="aa290-118">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="aa290-119">Detta gäller även om du inte använder plockning enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="aa290-119">This applies even if you are not using Pick according to FEFO.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa290-120">Se även</span><span class="sxs-lookup"><span data-stu-id="aa290-120">See Also</span></span>  
<span data-ttu-id="aa290-121">[Plocka artiklar](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="aa290-121">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="aa290-122">[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="aa290-122">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="aa290-123">[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="aa290-123">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="aa290-124">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="aa290-124">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="aa290-125">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="aa290-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="aa290-126">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa290-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
