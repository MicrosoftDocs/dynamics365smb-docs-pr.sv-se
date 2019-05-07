---
title: 'Så här: Planera lagertransporter i kalkylark | Microsoft Docs'
description: Planera transporter i kalkylarket med hjälp av Återanskaffningsfunktionen eller manuellt planera de rader som du vill skapa som transportinstruktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5cc450ef7591cf36eff1307da70cc032442486d3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931051"
---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="e5a3c-103">Planera lagertransporter i kalkylark</span><span class="sxs-lookup"><span data-stu-id="e5a3c-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="e5a3c-104">Planera transporter i kalkylarket med hjälp av Återanskaffningsfunktionen eller manuellt planera de rader som du vill skapa som transportinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="e5a3c-105">Så här beräknar du återanskaffningstransporter:</span><span class="sxs-lookup"><span data-stu-id="e5a3c-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="e5a3c-106">Allt eftersom artiklarna i distributionslagret levereras till kunderna innehåller lagerplatser med högst lagerplatsordning allt färre artiklar.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="e5a3c-107">Om du vill fylla på plocklagerplatserna med högst lagerplatsordning med artiklar från andra lagerplatser kan du köra funktionen **Beräkna lagerplatsåteranskaffning** på sidan **Transportkalkylark**</span><span class="sxs-lookup"><span data-stu-id="e5a3c-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function on the **Movement Worksheet** page</span></span>

1.  <span data-ttu-id="e5a3c-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Transportförslag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e5a3c-109">Välj åtgärden **Beräkna lagerplatsåteranskaffning**.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e5a3c-110">skapar rader som anger exakt hur du ska flytta artiklar från lagerplatser med låg lagerplatsordning till lagerplatser med högre lagerplatsordning.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e5a3c-111">Föreslår en transport enligt FEFO när du aktiverar **Skapa transport** operationen, om följande villkor är uppfyllda för en artikel:</span><span class="sxs-lookup"><span data-stu-id="e5a3c-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="e5a3c-112">artikeln har ett utgångsdatum,</span><span class="sxs-lookup"><span data-stu-id="e5a3c-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="e5a3c-113">Fältet **Plocka enligt FEFO** på lagerställekortet är markerat och</span><span class="sxs-lookup"><span data-stu-id="e5a3c-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="e5a3c-114">På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="e5a3c-115">fälten **Från zon** och **Från lagerplats** innehåller inga värden.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="e5a3c-116">Mer information finns i [Plocka enligt FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="e5a3c-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="e5a3c-117">Titta igenom raderna och ändra dem vid behov, eller ta bort vissa av raderna om du inte har tillräckligt med tid att utföra alla.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="e5a3c-118">Välj åtgärden **Skapa transport** för att skapa en distributionslagerinstruktion till lagerpersonalen.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="e5a3c-119">Du kan flytta hela innehållet i en eller flera lagerplatser med funktionen Hämta lagerplatsinnehåll:</span><span class="sxs-lookup"><span data-stu-id="e5a3c-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="e5a3c-120">Du kan även använda Transportkalkylark för att planera andra lagertransporter inom distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="e5a3c-121">När du till exempel vill placera artiklar på en lagerplats för kvalitetskontroll kan du använda transportförslaget för att planera den åtgärden och sedan skapa en transportinstruktion för en anställd.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="e5a3c-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Transportförslag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e5a3c-123">Välj åtgärden **Hämta lagerplatsinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="e5a3c-124">Använd sidan för begäran för att filtrera vilka lagerplatser och artiklar som ska visas på transportförslagets rader.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-124">Use the request page to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="e5a3c-125">Fyll i de relevanta fälten på sidan för begäran av batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-125">Fill in the relevant fields in the batch job request page.</span></span> <span data-ttu-id="e5a3c-126">Om du till exempel vill visa lagerplatsinnehållet för alla lagerplatser i en viss zon på lagerstället fyller du i fältet **Zonkod**.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="e5a3c-127">Om du vill hämta rader för alla lagerplatser som innehåller en viss artikel fyller du i fältet **Artikelnr**.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e5a3c-128">Du kan inte manuellt flytta artiklar in och ut ur en lagerplats av typen RECEIVE. Detta beror på att artiklar som finns i en lagerplats av RECEIVE-typ måste registreras som införda innan de blir en del av det tillgängliga lagret.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="e5a3c-129">Om du hämtar många rader väljer du **Sortera** för att välja en sorteringsmetod som du kan använda för att bestämma den ordning som raderna ska visas med i kalkylarket och klickar sedan på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e5a3c-130">Förflyttningsrader hämtas enligt FEFO när du aktiverar **Hämta lagerplatsinnehåll** operationen, om följande villkor är uppfyllda för en artikel:</span><span class="sxs-lookup"><span data-stu-id="e5a3c-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="e5a3c-131">artikeln har ett utgångsdatum,</span><span class="sxs-lookup"><span data-stu-id="e5a3c-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="e5a3c-132">Fältet **Plocka enligt FEFO** på lagerställekortet är markerat och</span><span class="sxs-lookup"><span data-stu-id="e5a3c-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="e5a3c-133">På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="e5a3c-134">fälten **Från zon** och **Från lagerplats** innehåller inga värden.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="e5a3c-135">Fyll i en del av de hämtade raderna för att spegla de ändringar som du vill utföra.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="e5a3c-136">För varje artikel som du vill flytta måste du fylla i fälten **Artikelnr**, **Från lagerplatskod**, **Till lagerplatskod** och **Antal**.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="e5a3c-137">Ta bort ofullständiga rader som du bara använde i informationssyfte.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="e5a3c-138">När raderna i transportkalkylarket korrekt speglar hur transporten ska utföras av lagerpersonalen klickar du på åtgärden **Skapa transport** för att skapa instruktionerna för personalen.</span><span class="sxs-lookup"><span data-stu-id="e5a3c-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e5a3c-139">Se även</span><span class="sxs-lookup"><span data-stu-id="e5a3c-139">See Also</span></span>  
[<span data-ttu-id="e5a3c-140">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="e5a3c-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="e5a3c-141">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="e5a3c-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e5a3c-142">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="e5a3c-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="e5a3c-143">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="e5a3c-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="e5a3c-144">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="e5a3c-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="e5a3c-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e5a3c-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
