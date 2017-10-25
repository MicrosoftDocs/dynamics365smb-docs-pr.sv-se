---
title: "Så här flyttar du artiklar ad hoc i grundläggande lagerkonfiguration | Microsoft Docs"
description: "Ibland kan du behöva flytta artiklar mellan interna lagerplatser, inte inleverans eller utleveranslagerplatser, utan en viss efterfrågan från ett källdokument. Du kan utföra dessa ad hoc-transporter, till exempel, kan du ordna om distributionslagret, för att få artiklarna till område, eller flytta ytterligare artiklar till och från en produktionsområde utan ett systemsamband med produktionsorderkälldokumentet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 38361c04f4ede35afd20e1fe84128fcdbfe104d0
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-move-items-ad-hoc-in-basic-warehouse-configurations"></a><span data-ttu-id="43a25-104">Så här flyttar du artiklar ad hoc i grundläggande lagerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="43a25-104">How to: Move Items Ad Hoc in Basic Warehouse Configurations</span></span>
<span data-ttu-id="43a25-105">Ibland kan du behöva flytta artiklar mellan interna lagerplatser, inte inleverans eller utleveranslagerplatser, utan en viss efterfrågan från ett källdokument.</span><span class="sxs-lookup"><span data-stu-id="43a25-105">You may occasionally need to move items between internal bins, not receiving or shipping bins, without a specific demand from a source document.</span></span> <span data-ttu-id="43a25-106">Du kan utföra dessa ad hoc-transporter, till exempel, kan du ordna om distributionslagret, för att få artiklarna till område, eller flytta ytterligare artiklar till och från en produktionsområde utan ett systemsamband med produktionsorderkälldokumentet.</span><span class="sxs-lookup"><span data-stu-id="43a25-106">You may perform these ad hoc movements, for example, to reorganize the warehouse, to bring items to an inspection area, or to move additional items to and from a production area without a system relation to the production order source document.</span></span>  

<span data-ttu-id="43a25-107">I grundläggande distributionslagerkonfiguration, dvs lagerställen som använder **Lagerplats ska finnas** inställningsfältet, och möjligen **Begär plockning** och den **Begär artikelinförsel** inställningarna, kan du registrera ad hoc-transporter utan källdokument på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="43a25-107">In basic warehouse configurations, that is locations that use the **Bin Mandatory** setup field and possibly the **Require Pick** and the **Require Put-away** setup fields, you can register ad hoc movements without source documents in the following ways:</span></span>  

    - <span data-ttu-id="43a25-108">Med **Internförflyttning** fönstret.</span><span class="sxs-lookup"><span data-stu-id="43a25-108">With the **Internal Movement** window.</span></span>  
    - <span data-ttu-id="43a25-109">Med fönstret **Artikelgrupperingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="43a25-109">With the **Item Reclassification Journal** window.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="43a25-110">I avancerad lagerkonfiguration, dvs lagerställen som använder **Dirigerad art.inf. och plock.** inställningsfältet använder du **Transportförslag** fönstret eller **Intern Dist.lager plockning** eller **Intern Dist.lager art.införsel** fönstren för flytta artiklar som är ad hoc mellan lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="43a25-110">In advanced warehouse configurations, that is locations that use the **Directed Put-away and Pick** setup field, you use the **Movement Worksheet** window or the **Internal Whse. Pick** or the **Internal Whse. Put-away** windows to move items ad hoc between bins.</span></span>  

## <a name="to-move-items-as-an-internal-movement"></a><span data-ttu-id="43a25-111">Så här flyttar du artiklar som en internförflyttning</span><span class="sxs-lookup"><span data-stu-id="43a25-111">To move items as an internal movement</span></span>  
1.  <span data-ttu-id="43a25-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Interntransport** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="43a25-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Internal Movement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="43a25-113">Fyll i fältet **Nr** på snabbfliken **Allmänt** .</span><span class="sxs-lookup"><span data-stu-id="43a25-113">On the **General** FastTab, fill in the **No.**</span></span> <span data-ttu-id="43a25-114">Fyll Nr fälten, antingen genom att lämna fältet eller genom att välja **AssistEdit** för att välja nummer i nummerserien.</span><span class="sxs-lookup"><span data-stu-id="43a25-114">field, either by leaving the field or by choosing the **AssistEdit** button to select from the number series.</span></span>  
3.  <span data-ttu-id="43a25-115">I **Lagerställekod** fältet, ange det lagerställe där transporten ska utföras.</span><span class="sxs-lookup"><span data-stu-id="43a25-115">In the **Location Code** field, enter the location where the movement takes place.</span></span>  

    <span data-ttu-id="43a25-116">Om lagerstället lagts upp som din standardplats som distributionslageranvändare, infogas lagerställekod i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="43a25-116">If the location is set up as your default location as a warehouse employee, the location code is inserted automatically.</span></span>  
4.  <span data-ttu-id="43a25-117">I **Till lagerplatskod** fältet, ange en kod för den lagerplats som du vill flytta artikeln till.</span><span class="sxs-lookup"><span data-stu-id="43a25-117">In the **To Bin Code** field, enter a code for the bin that you want to move the item to.</span></span> <span data-ttu-id="43a25-118">För produktionen kan detta vara till exempel en öppen produktionslagerplatskod som har angetts på lagerställekortet eller i produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="43a25-118">For production purposes, this could be the open shop floor bin code, for example, as defined on the location card or work center.</span></span>  
5.  <span data-ttu-id="43a25-119">I **Förfallodatum** fältet, ange det datum då transporten måste ha slutförts.</span><span class="sxs-lookup"><span data-stu-id="43a25-119">In the **Due Date** field, enter the date by which the movement must be completed.</span></span>  
6.  <span data-ttu-id="43a25-120">På snabbfliken **Rader** väljer du fältet **Artikelnr** för att öppna fönstret **Lagerplatsinnehåll lista** och välj sedan artikeln som ska flyttas baserat på dess tillgänglighet i lagerplatserna. Det går också att välja **Hämta lagerplatsinnehåll** för att fylla i interförflyttningsrader baserat på dina filter.</span><span class="sxs-lookup"><span data-stu-id="43a25-120">On the **Lines** FastTab, choose the **Item No.** field to open the **Bin Contents List** window, and then select the item to move based on its availability in bins. Alternatively, choose the **Get Bin Contents** action to fill the internal movement lines based on your filters.</span></span> <span data-ttu-id="43a25-121">Mer information finns i beskrivningen för åtgärden **Hämta lagerplatsinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="43a25-121">For more information, see the tooltip for the **Get Bin Content** action.</span></span>   

    <span data-ttu-id="43a25-122">När du har valt artikel innehåller fältet **Från lagerplatskod** automatiskt enligt valt lagerplats, men du kan ändra den till en annan lagerplats där artikeln är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="43a25-122">When you have selected the item, the **From Bin Code** field is automatically filled according to the selected bin content, but you can change it to any other bin where the item is available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="43a25-123">Eftersom **Artikelnr** fältet, och **Från lagerplatskod** fältet är kopplade, deras värden kan ändras oberoende av varandra, när du redigerar endera fältet.</span><span class="sxs-lookup"><span data-stu-id="43a25-123">Because the **Item No.** field and the **From Bin Code** field are connected, their values may change interdependently when you edit either field.</span></span>  

    <span data-ttu-id="43a25-124">Fältet **Till lagerplatskod** fylls i med värdet som du har angett i huvudet, men du kan ändra koden på raden till en annan lagerplatskod som är inte spärrad, eller hängivet till särskilt ändamål.</span><span class="sxs-lookup"><span data-stu-id="43a25-124">The **To Bin Code** field is filled with the value you entered on the header, but you can change it on the line to any other bin code that isn’t blocked or dedicated to special purposes.</span></span> <span data-ttu-id="43a25-125">Se Dedikerad för mer information om batch-jobb avseende att skapa lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="43a25-125">For more information about making bins dedicated, see Dedicated.</span></span>  
7.  <span data-ttu-id="43a25-126">Ange det antal som ska flyttas i **Antal** fältet, när du har definierat lagerplatser som du vill flytta artikeln till och från.</span><span class="sxs-lookup"><span data-stu-id="43a25-126">When you have defined which bins you want to move the item from and to, enter the quantity to move in the **Quantity** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="43a25-127">Antalet måste vara tillgängligt i fältet Från lagerplatskod.</span><span class="sxs-lookup"><span data-stu-id="43a25-127">Quantity must be available in the From Bin code.</span></span>  

8.  <span data-ttu-id="43a25-128">Är du klar att bearbeta internförflyttningen, välj åtgärden **Skapa lagerförflyttning**.</span><span class="sxs-lookup"><span data-stu-id="43a25-128">When you are ready to process the internal movement, choose the **Create Inventory Movement** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="43a25-129">När du har skapat lagerförflyttningen, tas rad för interntransport bort.</span><span class="sxs-lookup"><span data-stu-id="43a25-129">When you have created the inventory movement, the internal movement lines are deleted.</span></span>  

    <span data-ttu-id="43a25-130">Du utför resten av ad hoc-flyttningen i **Lagertransport** fönstret, på samma sätt som du skulle för en transport baserat på källdokument.</span><span class="sxs-lookup"><span data-stu-id="43a25-130">You perform the remainder of the ad hoc movement in the **Inventory Movement** window in the same way as you would for a movement based on source documents.</span></span> <span data-ttu-id="43a25-131">För mer informatio, se [Så här: Flytta komponenter till ett operationsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="43a25-131">For more information, see for example [How to: Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span></span>  

## <a name="to-move-items-with-the-item-reclassification-journal"></a><span data-ttu-id="43a25-132">Så här flyttar du artiklar med artikelgrupperingsjournalen</span><span class="sxs-lookup"><span data-stu-id="43a25-132">To move items with the item reclassification journal</span></span>
<span data-ttu-id="43a25-133">Du kan registrera flyttning av objekt genom att gruppera de lagerplatskoder som finns i stället för att använda dokument för distributionslagertransport.</span><span class="sxs-lookup"><span data-stu-id="43a25-133">In stead of using warehouse movement documents, you can record the moving of items by reclassifying their bin codes.</span></span> <span data-ttu-id="43a25-134">Mer information finns i [så här: Inventera, justera och gruppera lager](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="43a25-134">For more information, see [How to: Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>   
1.  <span data-ttu-id="43a25-135">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="43a25-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="43a25-136">Definiera vilka lagerplatser som du vill flytta artiklar till och från på varje journalrad, genom att fylla i **Lagerplatskod** och **Ny lagerplatskod** fältet.</span><span class="sxs-lookup"><span data-stu-id="43a25-136">On each journal line, define the bins from which and to which you want to move items by filling in the **Bin Code** and the **New Bin Code** fields.</span></span>  

    1.  <span data-ttu-id="43a25-137">Om du vill flytta hela innehållet från en lagerplats till en annan lagerplats väljer du åtgärden **Hämta lagerplatsinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="43a25-137">To move a bin's entire contents to another bin, choose the **Get Bin Contents** action.</span></span>  
    2.  <span data-ttu-id="43a25-138">Fyll i filter för att hitta den lagerplats vars innehåll du vill flytta och klicka på **OK**.</span><span class="sxs-lookup"><span data-stu-id="43a25-138">Fill in the filters to find the bin whose contents you would like to move and then choose the **OK** button.</span></span> <span data-ttu-id="43a25-139">Journalraderna fylls i med innehållet av lagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="43a25-139">The journal lines are filled with the contents of the bin.</span></span>  
3.  <span data-ttu-id="43a25-140">Fyll i de återstående fälten på varje journalrad.</span><span class="sxs-lookup"><span data-stu-id="43a25-140">Fill in the remaining fields on each journal line.</span></span>   
4.  <span data-ttu-id="43a25-141">Bokför Grupperingsjournalen</span><span class="sxs-lookup"><span data-stu-id="43a25-141">Post the reclassification journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="43a25-142">Till skillnad från transportdokument skapar en transportinstruktion som bokförs med grupperingsjournalen, inte ett distributionslagerkrav att utföra den fysiska aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="43a25-142">Unlike with movement documents, a movement posted with the reclassification journal does not create a warehouse request to perform the physical task.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43a25-143">Se även</span><span class="sxs-lookup"><span data-stu-id="43a25-143">See Also</span></span>  
[<span data-ttu-id="43a25-144">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="43a25-144">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="43a25-145">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="43a25-145">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="43a25-146">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="43a25-146">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="43a25-147">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="43a25-147">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="43a25-148">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="43a25-148">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="43a25-149">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43a25-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
