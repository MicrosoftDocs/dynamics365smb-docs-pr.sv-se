---
title: "Skapa ett lagerställekort och definiera överföringsflöden | Microsoft Docs"
description: "Du kan skapa ett lagerställekort för varje plats som du vill lagra lagerartiklar, till exempel lager eller distributionscenter, och ange flöden för överföring av artiklar mellan olika lagerställen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 45943ef97eee9d6bf24fd679e5dbbab96f5177f8
ms.contentlocale: sv-se
ms.lasthandoff: 04/18/2018

---
# <a name="set-up-locations"></a><span data-ttu-id="f7b4c-103">Konfigurera platser</span><span class="sxs-lookup"><span data-stu-id="f7b4c-103">Set Up Locations</span></span>
<span data-ttu-id="f7b4c-104">Om du köper, lagrar eller säljer artiklar på mer än en plats eller ett lager, måste du ställa in varje plats med ett lagerställeskort och definiera överföringsflöden.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="f7b4c-105">Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="f7b4c-106">Mer information finns i [Administrera projekt](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="f7b4c-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="f7b4c-107">Skapa ett nytt lagerställeskort</span><span class="sxs-lookup"><span data-stu-id="f7b4c-107">To create a location card</span></span>
1. <span data-ttu-id="f7b4c-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7b4c-109">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="f7b4c-110">I fönstret **Lagerställeskort** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-110">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="f7b4c-111">Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="f7b4c-112">Många fält på lagerställekortet hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="f7b4c-113">Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="f7b4c-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="f7b4c-114">Så här skapar du ett överföringsflöde</span><span class="sxs-lookup"><span data-stu-id="f7b4c-114">To create a transfer route</span></span>
1. <span data-ttu-id="f7b4c-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Överföringsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7b4c-116">Alternativt kan du i fönstret **Lagerställekort** välja åtgärden **Överföringsflöden**.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="f7b4c-117">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="f7b4c-118">I fönstret **Lagerställeskort** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="f7b4c-119">Du kan nu överföra lagerartiklar mellan två lagerställen.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="f7b4c-120">Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="f7b4c-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="f7b4c-121">Se även</span><span class="sxs-lookup"><span data-stu-id="f7b4c-121">See Also</span></span>
[<span data-ttu-id="f7b4c-122">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="f7b4c-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f7b4c-123">[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="f7b4c-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="f7b4c-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7b4c-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f7b4c-125">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="f7b4c-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="f7b4c-126">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f7b4c-126">General Business Functionality</span></span>](ui-across-business-areas.md)

