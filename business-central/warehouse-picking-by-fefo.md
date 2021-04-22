---
title: 'Så här: Aktivera plockning med FEFO | Microsoft Docs'
description: FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklar, de med de tidigaste utgångsdatumen, plockas först.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784073"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="c8b18-103">Aktivera plockning av artiklar med FEFO</span><span class="sxs-lookup"><span data-stu-id="c8b18-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="c8b18-104">FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklarna – de med tidigast utgångsdatum – plockas först.</span><span class="sxs-lookup"><span data-stu-id="c8b18-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="c8b18-105">Den här funktionen fungerar bara, när dessa villkor är uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="c8b18-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="c8b18-106">Artikel måste ha en serie-/partinummer.</span><span class="sxs-lookup"><span data-stu-id="c8b18-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="c8b18-107">På artikelns artikelspårningskod har angetts, fältet **SN dist.lager spårning** , eller **Parti dist.lager spårning** måste väljas.</span><span class="sxs-lookup"><span data-stu-id="c8b18-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="c8b18-108">Artikeln måste bokföras till lagret med ett utgångsdatum.</span><span class="sxs-lookup"><span data-stu-id="c8b18-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="c8b18-109">På platsen måste växlingsknappar **Begär plockning**, **Plocka enligt FEFO** och **Lagerplats ska finnas** aktiveras.</span><span class="sxs-lookup"><span data-stu-id="c8b18-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="c8b18-110">När alla villkor uppfylls, sorteras serie-/partinumrerade artiklar som ska plockas med de äldsta första alla plockningar och transporter, utom artiklar som använder SN-närmare visst eller partispecifik spårning.</span><span class="sxs-lookup"><span data-stu-id="c8b18-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c8b18-111">Om någon serie-/partinumrerade artiklar använder specifik spårning, är de respekterade först och under dem, listas de återstående, icke-specifika serie-/partinummer enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="c8b18-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="c8b18-112">Om två serie-/partinumrerade artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie – eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="c8b18-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="c8b18-113">När du plockar serie-/partinumrerade artiklar på lagerställen som har ställs in för dirigerad artikelinförsel och plockning, plockas bara kvantiteter på lagerställen av typen *Plock* enligt FEFO.</span><span class="sxs-lookup"><span data-stu-id="c8b18-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="c8b18-114">Om du vill aktivera transporter enligt FEFO, lämna fältet **Från lagerplats** tomt på sidan **Lagerförflyttning** på sidan **Transportkalkylark**.</span><span class="sxs-lookup"><span data-stu-id="c8b18-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="c8b18-115">Om fältet **Endast utgångsbokföring** markeras på **Artikelspårning kodkort**, endast föremål som inte har löpt ut ingår i valet och raderna sorteras enligt FEFO-principen.</span><span class="sxs-lookup"><span data-stu-id="c8b18-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8b18-116">Se även</span><span class="sxs-lookup"><span data-stu-id="c8b18-116">See Also</span></span>  
<span data-ttu-id="c8b18-117">[Plocka artiklar](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="c8b18-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="c8b18-118">[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="c8b18-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="c8b18-119">[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="c8b18-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="c8b18-120">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="c8b18-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="c8b18-121">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="c8b18-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c8b18-122">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c8b18-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]