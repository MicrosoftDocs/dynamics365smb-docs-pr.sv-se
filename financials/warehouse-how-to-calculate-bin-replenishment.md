---
title: "Så här beräknar du lagerplatsåteranskaffning | Microsoft Docs"
description: "Om lagerstället är inställt på dirigerad artikelinförsel och plockning, beaktas artikelinförsel prioriteter av mallen för lagerstället när införsel av inleveranser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e667ca56aa22fafc7fe6d0a4880c419a4272db26
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="ccb99-103">Beräkna lagerplatsåteranskaffning</span><span class="sxs-lookup"><span data-stu-id="ccb99-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="ccb99-104">Om lagerstället är inställt på dirigerad artikelinförsel och plockning, beaktas artikelinförsel prioriteter av mallen för lagerstället när införsel av inleveranser.</span><span class="sxs-lookup"><span data-stu-id="ccb99-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="ccb99-105">Prioriteter innehåller minimal och maximal kvantitet av lagerplatsinnehåll, som har kopplats till en viss lagerplats, och lagerplatsordningarna.</span><span class="sxs-lookup"><span data-stu-id="ccb99-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="ccb99-106">Om artiklar anländer i fast takt fylls därför de plocklagerplatser på som används mest allt eftersom de töms.</span><span class="sxs-lookup"><span data-stu-id="ccb99-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="ccb99-107">Inleveranser anländer dock inte alltid i en stadig takt.</span><span class="sxs-lookup"><span data-stu-id="ccb99-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="ccb99-108">Ibland köps artiklar in i större kvantiteter så att företaget kan få rabatt, eller så att produktionsenheten kan producera mycket av en artikel för att få en låg styckkostnad.</span><span class="sxs-lookup"><span data-stu-id="ccb99-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="ccb99-109">Då kan det ta ett tag innan artiklarna inlevereras på nytt i distributionslagret, och distributionslagret behöver regelbundet transportera artiklar till plocklagerplatser från volymlagret.</span><span class="sxs-lookup"><span data-stu-id="ccb99-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="ccb99-110">Det kan även vara så att ett nytt parti förväntas inom kort och därför behöver volymlagret tömmas på artiklar innan de nya varorna anländer.</span><span class="sxs-lookup"><span data-stu-id="ccb99-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="ccb99-111">Slutligen gäller att om du har definierat volymlagerplatser med enbart lagerplatstypåtgärden **Artikelinförsel**, d.v.s. åtgärden **Plocka** inte är markerad, måste du alltid fylla på plocklagerplatserna eftersom lagerplatser av artikelinförseltyp inte föreslås för en plockning från lager.</span><span class="sxs-lookup"><span data-stu-id="ccb99-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="ccb99-112">Så här fyller du på plocklagerplatser</span><span class="sxs-lookup"><span data-stu-id="ccb99-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="ccb99-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Transportförslag**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ccb99-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ccb99-114">Välj åtgärden **Beräkna lagerplatsåteranskaffning** för att öppna sidan för rapportbegäran.</span><span class="sxs-lookup"><span data-stu-id="ccb99-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="ccb99-115">Fyll i fönstret för begäran om batch-jobb för att begränsa omfattningen av de påfyllningsförslag som kommer beräknas.</span><span class="sxs-lookup"><span data-stu-id="ccb99-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="ccb99-116">Du kanske är mest intresserad av särskilda artiklar, zoner eller lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="ccb99-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="ccb99-117">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccb99-117">Choose the **OK** button.</span></span> <span data-ttu-id="ccb99-118">Rader skapas för de påfyllningstransporter som måste utföras enligt de regler som har angetts för lagerplatserna och lagerplatsinnehållet, d.v.s. artiklar på lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="ccb99-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="ccb99-119">Om du vill utföra alla påfyllningsförslag klickar du på åtgärden **Skapa transport**.</span><span class="sxs-lookup"><span data-stu-id="ccb99-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="ccb99-120">Lagerpersonalen kan nu hitta instruktionerna under menyobjektet **Transport**, utföra dem och registrera dem.</span><span class="sxs-lookup"><span data-stu-id="ccb99-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="ccb99-121">Om du endast vill utföra vissa förslag tar du bort de rader som är mindre viktiga och skapar sedan en transport.</span><span class="sxs-lookup"><span data-stu-id="ccb99-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="ccb99-122">Nästa gång som du beräknar lagerplatspåfyllning återskapas de förslag som du har tagit bort, om de fortfarande är aktuella.</span><span class="sxs-lookup"><span data-stu-id="ccb99-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ccb99-123">Om följande villkor är uppfyllda för en artikel:</span><span class="sxs-lookup"><span data-stu-id="ccb99-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="ccb99-124">artikeln har ett utgångsdatum,</span><span class="sxs-lookup"><span data-stu-id="ccb99-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="ccb99-125">Fältet **Plocka enligt FEFO** på lagerställekortet är markerat och</span><span class="sxs-lookup"><span data-stu-id="ccb99-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="ccb99-126">Du använder funktionen **Beräkna lagerplatsåteranskaffning**</span><span class="sxs-lookup"><span data-stu-id="ccb99-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="ccb99-127">då innehåller fälten **Från zon** och **Från lagerplats** inga värden. Detta beror på att algoritmen som används för att beräkna varifrån artiklarna ska transporteras endast utlöses när du aktiverar funktionen **Skapa transport**.</span><span class="sxs-lookup"><span data-stu-id="ccb99-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ccb99-128">Se även</span><span class="sxs-lookup"><span data-stu-id="ccb99-128">See Also</span></span>  
[<span data-ttu-id="ccb99-129">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="ccb99-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ccb99-130">Plockning med FEFO</span><span class="sxs-lookup"><span data-stu-id="ccb99-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="ccb99-131">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="ccb99-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ccb99-132">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ccb99-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ccb99-133">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ccb99-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ccb99-134">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="ccb99-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ccb99-135">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ccb99-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

