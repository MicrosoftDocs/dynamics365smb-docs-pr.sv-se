---
title: Skapa ett lagerställekort och definiera överföringsflöden
description: Du kan skapa ett lagerställekort för varje plats som du vill lagra lagerartiklar, till exempel lager eller distributionscenter, och ange flöden för överföring av artiklar mellan olika lagerställen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184330"
---
# <a name="set-up-locations"></a><span data-ttu-id="da1db-103">Konfigurera platser</span><span class="sxs-lookup"><span data-stu-id="da1db-103">Set Up Locations</span></span>

<span data-ttu-id="da1db-104">Om du köper, lagrar eller säljer artiklar på mer än en plats eller ett lager, måste du ställa in varje plats med ett lagerställeskort och definiera överföringsflöden.</span><span class="sxs-lookup"><span data-stu-id="da1db-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="da1db-105">[!INCLUDE [prod_short](includes/prod_short.md)] använder platser för att hålla ordning på lagret i både enklare ärenden och i mer komplicerade lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="da1db-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="da1db-106">Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen.</span><span class="sxs-lookup"><span data-stu-id="da1db-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="da1db-107">Mer information finns i [Administrera projekt](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="da1db-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="da1db-108">Lagerställekort</span><span class="sxs-lookup"><span data-stu-id="da1db-108">Location cards</span></span>

<span data-ttu-id="da1db-109">Lagerställekortet anger information om ett lagerställe, till exempel ett distributionslager eller distributionscenter.</span><span class="sxs-lookup"><span data-stu-id="da1db-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="da1db-110">Du tilldelar varje lagerställe ett namn och en kod som representerar lagerstället.</span><span class="sxs-lookup"><span data-stu-id="da1db-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="da1db-111">Du kan sedan ange lagerställekoden i andra delar av programmet när du vill registrera transaktioner för ett visst lagerställe.</span><span class="sxs-lookup"><span data-stu-id="da1db-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="da1db-112">Du kan ange information om lagerplatser och lagerprinciper för varje lagerställe.</span><span class="sxs-lookup"><span data-stu-id="da1db-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="da1db-113">Utifrån de lagerprinciper du väljer kan du välja alternativ på snabbfliken **Lagerplatser** för att definiera vilka lagerplatser som ska användas som standard vid transaktioner.</span><span class="sxs-lookup"><span data-stu-id="da1db-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="da1db-114">Om du använder riktad artikelinförsel och plockning, kan du använda de flesta alternativen på snabbfliken **Lagerplatsprinciper** för att definiera hur du vill använda de olika avancerade lagerfunktionerna.</span><span class="sxs-lookup"><span data-stu-id="da1db-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="da1db-115">Vissa alternativfält tonas ned och inaktiveras av andra inställningar på sidan **Lagerställekort** för att begränsa konfigurationskombinationer som inte stöds.</span><span class="sxs-lookup"><span data-stu-id="da1db-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="da1db-116">Välj åtgärden **Zoner** eller **Lagerplatser** om du vill visa information om zoner och lagerplatser som har definierats för lagerstället.</span><span class="sxs-lookup"><span data-stu-id="da1db-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="da1db-117">Skapa ett nytt lagerställeskort</span><span class="sxs-lookup"><span data-stu-id="da1db-117">To create a location card</span></span>

1. <span data-ttu-id="da1db-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="da1db-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="da1db-119">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="da1db-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="da1db-120">På sidan **Lagerställekort** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="da1db-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="da1db-121">Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.</span><span class="sxs-lookup"><span data-stu-id="da1db-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="da1db-122">Många fält på lagerställekortet hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="da1db-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="da1db-123">Fälten är inte relevanta för företag som inte behöver den mer komplicerade distributionslagerfunktionen.</span><span class="sxs-lookup"><span data-stu-id="da1db-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="da1db-124">Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="da1db-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="da1db-125">Du kan ändra konfigurationen av en plats senare, men du kan inte redigera inställningen av lagerställen som har artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="da1db-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="da1db-126">Sedan kan du definiera överföringsflöden mellan lagerställen, om du har flera lagerställen.</span><span class="sxs-lookup"><span data-stu-id="da1db-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="da1db-127">Så här skapar du ett överföringsflöde</span><span class="sxs-lookup"><span data-stu-id="da1db-127">To create a transfer route</span></span>

1. <span data-ttu-id="da1db-128">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Överföringsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="da1db-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="da1db-129">Alternativt kan du på sidan **Lagerställekort** välja åtgärden **Överföringsflöden**.</span><span class="sxs-lookup"><span data-stu-id="da1db-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="da1db-130">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="da1db-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="da1db-131">På sidan **Lagerställekort** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="da1db-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="da1db-132">Du kan nu överföra lagerartiklar mellan två lagerställen.</span><span class="sxs-lookup"><span data-stu-id="da1db-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="da1db-133">Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="da1db-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="da1db-134">Lagerställen</span><span class="sxs-lookup"><span data-stu-id="da1db-134">Bins</span></span>

<span data-ttu-id="da1db-135">Lagerställen representerar den grundläggande lagerstrukturen och används för att lägga förslag om artiklarnas specifika placering av artiklar.</span><span class="sxs-lookup"><span data-stu-id="da1db-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="da1db-136">När du har skapat lagerplatser kan du definiera det innehåll som du vill placera på respektive lagerplats, eller så kan lagerplatsen fungera som en flytande lagerplats utan att något särskilt innehåll har angetts.</span><span class="sxs-lookup"><span data-stu-id="da1db-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="da1db-137">Om du hanterar lager i en enklare konfiguration behöver du troligtvis inte lagerplatser.Lagerplatser används främst i grundläggande och förebyggande åtgärder för distributionslager.</span><span class="sxs-lookup"><span data-stu-id="da1db-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="da1db-138">Om du hanterar lagret i en mer enkel inställning behöver du troligen inte ha några lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="da1db-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="da1db-139">Om du vill använda lagerplatsfunktionen på ett lagerställe måste du först aktivera funktionen på kortet **Lagerställe** genom att markera fältet **Lagerplatser obligatoriskt** på snabbfliken **Distributionslager**.</span><span class="sxs-lookup"><span data-stu-id="da1db-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="da1db-140">Sedan designar du artikelflödet på lagerstället, genom att ange inställningar för lagerställeskoder i fältet som representerar de olika flödena.</span><span class="sxs-lookup"><span data-stu-id="da1db-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="da1db-141">Innan du kan ange lagerställeskoder på lagerställekortet, måste lagerställeskoderna skapas.</span><span class="sxs-lookup"><span data-stu-id="da1db-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="da1db-142">Mer information finns i [Skapa lagerställen](warehouse-how-to-create-individual-bins.md) och [Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="da1db-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="da1db-143">Zoner</span><span class="sxs-lookup"><span data-stu-id="da1db-143">Zones</span></span>

<span data-ttu-id="da1db-144">Om du vill strukturera lagerplatser under zoner kan du göra det på sidan **Zoner**.</span><span class="sxs-lookup"><span data-stu-id="da1db-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="da1db-145">[!INCLUDE [prod_short](includes/prod_short.md)] kopierar de fält som du har skapat för en viss zon till lagerplatserna i zonen.</span><span class="sxs-lookup"><span data-stu-id="da1db-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="da1db-146">På så sätt kan du fördela en zon till en lagerplats eller en lagerplatsmall (lagerplatsuppläggningsfilter) så fylls flera andra fält i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="da1db-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="da1db-147">Du kan dock välja att bara skapa en zon och strukturera distributionslagret enbart med hjälp av lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="da1db-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="da1db-148">Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="da1db-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="da1db-149">Se även</span><span class="sxs-lookup"><span data-stu-id="da1db-149">See Also</span></span>

[<span data-ttu-id="da1db-150">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="da1db-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="da1db-151">Överföra lager mellan olika lagerställen</span><span class="sxs-lookup"><span data-stu-id="da1db-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="da1db-152">Skapa lagerställen</span><span class="sxs-lookup"><span data-stu-id="da1db-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="da1db-153">Skapa lagerplatstyper</span><span class="sxs-lookup"><span data-stu-id="da1db-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="da1db-154">Ställa in lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="da1db-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="da1db-155">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da1db-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="da1db-156">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="da1db-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="da1db-157">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="da1db-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]