---
title: "Så här ställer du in lagerställen att använda lagerplatser | Microsoft Docs"
description: "Lagerplatser representerar den grundläggande lagerstrukturen och används för att göra förslag om artiklarnas specifika placering av artiklar. När du har skapat lagerplatserna kan du definiera det innehåll som du vill placera på respektive lagerplats, eller så kan lagerplatsen fungera som en flytande lagerplats utan att något särskilt innehåll har angetts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2d84f1222dccca86f5906af1c82fc0e6192173d6
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-locations-to-use-bins"></a><span data-ttu-id="2ae6d-104">Registrera lagerställen för att använda lagerplatser</span><span class="sxs-lookup"><span data-stu-id="2ae6d-104">Set Up Locations to Use Bins</span></span>
<span data-ttu-id="2ae6d-105">Lagerplatser representerar den grundläggande lagerstrukturen och används för att göra förslag om artiklarnas specifika placering av artiklar.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-105">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="2ae6d-106">När du har skapat lagerplatserna kan du definiera det innehåll som du vill placera på respektive lagerplats, eller så kan lagerplatsen fungera som en flytande lagerplats utan att något särskilt innehåll har angetts.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-106">When you have created your bins, you can define very specifically the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span>  

<span data-ttu-id="2ae6d-107">Om du vill använda lagerplatsfunktionerna på ett lagerställe måste du först aktivera dessa på kortet **Lagerställe**.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-107">To use the bin functionality at a location, you first activate the functionality on the **Location** card.</span></span> <span data-ttu-id="2ae6d-108">Sedan designar du artikelflödet på lagerstället, genom att ange inställningar för lagerplatskoder i fältet som representerar de olika flödena.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-108">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2ae6d-109">Innan du kan ange lagerplatskoder på lagerställekortet, måste lagerplatskoderna skapas.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-109">Before you can specify bin codes on the location card, the bin codes must be created.</span></span> <span data-ttu-id="2ae6d-110">Mer information finns i [Skapa lagerplatser](warehouse-how-to-create-individual-bins.md).</span><span class="sxs-lookup"><span data-stu-id="2ae6d-110">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md).</span></span>  

## <a name="to-set-up-a-location-to-use-bins"></a><span data-ttu-id="2ae6d-111">Så här lägger du upp ett lagerställe för att använda lagerplatser</span><span class="sxs-lookup"><span data-stu-id="2ae6d-111">To set up a location to use bins</span></span>  
1.  <span data-ttu-id="2ae6d-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2ae6d-113">Välj lagerstället där du vill använda lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-113">Select the location where you want to use bins.</span></span>  
3.  <span data-ttu-id="2ae6d-114">Välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-114">Choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="2ae6d-115">Markera fältet **Lagerplats ska finnas** på kryssrutan **Dist.lager**.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-115">On the **Warehouse** FastTab, select the **Bin Mandatory** check box.</span></span>  
5.  <span data-ttu-id="2ae6d-116">Om du inte använder dirigerad artikelinförsel och plockning för ett lagerställe fyller du i fältet **Standard lagerplatsval** med den metod som ska användas för att tilldela en standardlagerplats till en artikel.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-116">If you are not using directed put-away and pick for the location, fill in the **Default Bin Selection** field with the method the system should use when assigning a default bin to an item.</span></span>  
6.  <span data-ttu-id="2ae6d-117">Öppna kortet för den plats som du vill ställa in lagerplatser för.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-117">Open the card for the location that you want to set up bins for.</span></span>
7.  <span data-ttu-id="2ae6d-118">På snabbfliken **Lagerplatser** väljer du de lagerplatser som du vill använda som standard för inleveranser, utleveranser samt ankommande, avgående och öppna produktionslagerplatser.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-118">On the **Bins** FastTab, select the bins that you want to use as the default for receipts, shipments, inbound, outbound, and open shop floor bins.</span></span>  
8.  <span data-ttu-id="2ae6d-119">De lagerplatskoder som du fyller i här visas automatiskt i huvudena och på raderna för olika distributionslagerdokument.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-119">The bin codes you fill in here will appear automatically on the headers and on the lines of various warehouse documents.</span></span> <span data-ttu-id="2ae6d-120">Standardlagerplatserna definierar alla start- och slutplaceringar av artiklar i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-120">The default bins define all starting or ending placements of items in the warehouse.</span></span>  
9.  <span data-ttu-id="2ae6d-121">Om du använder dirigerad artikelinförsel och plockning väljer du en lagerplats för distributionslagerjusteringarna.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-121">If you are using directed put-away and pick, select a bin for your warehouse adjustments.</span></span> <span data-ttu-id="2ae6d-122">Lagerplatskoden i **Justering lagerplatskod** fältet anger den virtuella lagerplats där avvikelser i lagret registreras, när du registrerar antingen observerade avvikelser som har registrerats i dist.lagerartikeljournalen, eller avvikelser beräknade när du registrerar en fysiskt dist.lager.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-122">The bin code in the **Adjustment Bin Code** field defines the virtual bin in which to record discrepancies in inventory when you register either observed differences registered in the warehouse item journal, or differences calculated when you register a warehouse physical inventory.</span></span>  
10. <span data-ttu-id="2ae6d-123">Fyll i fälten på snabbfliken **Lagerplatsprinciper** om de är relevanta för distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-123">Fill in the fields on the **Bin Policies** FastTab if they are relevant to your warehouse.</span></span> <span data-ttu-id="2ae6d-124">De viktigaste fälten är **Lagerplats kapacitetsprincip**, **Tillåt brytenhet** och **Artikelinförsel mallkod**.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-124">The most important fields are **Bin Capacity Policy**, **Allow Breakbulk**, and **Put-away Template Code** fields.</span></span>  
11. <span data-ttu-id="2ae6d-125">På snabbfliken **Dist.lager** fyller du i fälten **Avgående lagerhanteringstid**, **Ankommande lagerhanteringstid** och **Baskalenderkod**.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-125">On the **Warehouse** FastTab, fill in the **Outbound Whse. Handling Time**, **Inbound Whse. Handling Time**, and the **Base Calendar Code** fields.</span></span> <span data-ttu-id="2ae6d-126">Mer information finns i [Så här skapar du baskalendrar](across-how-to-assign-base-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="2ae6d-126">For more information, see [Set Up Base Calendars](across-how-to-assign-base-calendars.md).</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="2ae6d-127">Fylla förbrukningslagerplatsen</span><span class="sxs-lookup"><span data-stu-id="2ae6d-127">Filling the Consumption Bin</span></span>
<span data-ttu-id="2ae6d-128">Diagrammet visar hur **Lagerplatskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.</span><span class="sxs-lookup"><span data-stu-id="2ae6d-128">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="2ae6d-129">![Flödesschema för lagerplats](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="2ae6d-129">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ae6d-130">Se även</span><span class="sxs-lookup"><span data-stu-id="2ae6d-130">See Also</span></span>
[<span data-ttu-id="2ae6d-131">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="2ae6d-131">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="2ae6d-132">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="2ae6d-132">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2ae6d-133">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="2ae6d-133">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="2ae6d-134">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="2ae6d-134">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="2ae6d-135">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="2ae6d-135">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="2ae6d-136">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ae6d-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

