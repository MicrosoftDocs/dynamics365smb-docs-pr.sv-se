---
title: "Skapa och justera resursanvändning och priser | Microsoft Docs"
description: "Beskriver hur du kan registrera resursförbrukning eller förbrukning för ett projekt för att hålla reda på och hantera kostnader, priser och arbetstyper."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: f110f4cc342f5284e3da2641d56dc13f67c3773a
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-resources-for-jobs"></a><span data-ttu-id="35c38-103">Så här använder du resurser för projekt</span><span class="sxs-lookup"><span data-stu-id="35c38-103">How to: Use Resources for Jobs</span></span>
<span data-ttu-id="35c38-104">Du registrerar förbrukning av resurser i projektjournalen för att hålla reda på kostnader, priser och de specifika projekttyper som är kopplade till projekt.</span><span class="sxs-lookup"><span data-stu-id="35c38-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="35c38-105">Mer information finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="35c38-105">For more information, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="35c38-106">Du kan även bokföra förbrukningen av en resurs i en resursjournal eller projektjournal.</span><span class="sxs-lookup"><span data-stu-id="35c38-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="35c38-107">Transaktioner bokförda i resursjournaler påverkar inte redovisningen.</span><span class="sxs-lookup"><span data-stu-id="35c38-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

> [!NOTE]  
>   <span data-ttu-id="35c38-108">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="35c38-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="35c38-109">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="35c38-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="35c38-110">Så här tilldelar du resurser till projekt</span><span class="sxs-lookup"><span data-stu-id="35c38-110">To assign resources to jobs</span></span>
<span data-ttu-id="35c38-111">Du tilldelar resurser till projekt genom att skapa planeringsrader för projektet.</span><span class="sxs-lookup"><span data-stu-id="35c38-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="35c38-112">Mer information finns i [Så här skapar du Projekt](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="35c38-112">For more information, see [How to: Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="35c38-113">Registrera resursförbrukning för ett projekt</span><span class="sxs-lookup"><span data-stu-id="35c38-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="35c38-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projektjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="35c38-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="35c38-115">Öppna den relevanta projektjournalen och fyll sedan i fälten som behövs.</span><span class="sxs-lookup"><span data-stu-id="35c38-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="35c38-116">När journalen är slutförd väljer du åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="35c38-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="35c38-117">Justera resurspriser</span><span class="sxs-lookup"><span data-stu-id="35c38-117">To adjust resource prices</span></span>
<span data-ttu-id="35c38-118">Om du vill ändra kostnader eller priser för många resurser på en gång kan du använda ett batch-jobb .</span><span class="sxs-lookup"><span data-stu-id="35c38-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="35c38-119">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Justera resurskost./-priser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="35c38-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="35c38-120">Fyll i fälten på en rad efter behov och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="35c38-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="35c38-121">Batch-jobbet varken skapar eller justerar alternativa kostnader eller priser för resurser.</span><span class="sxs-lookup"><span data-stu-id="35c38-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="35c38-122">Detta ändrar bara innehållet i fältet på resurskortet för fältet **Justeringsfält** som du har valt i batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="35c38-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="35c38-123">Justeringarna börjar gälla direkt för resurser så kontrollera justeringsfaktorerna innan du kör batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="35c38-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="35c38-124">Så här får du förslag till resursprisändringar enligt befintliga alternativa priser:</span><span class="sxs-lookup"><span data-stu-id="35c38-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="35c38-125">Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.</span><span class="sxs-lookup"><span data-stu-id="35c38-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="35c38-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursprisändringar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="35c38-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="35c38-127">Välj åtgärden **Föreslå res.prisändring (pris)** och fyll sedan i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="35c38-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="35c38-128">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="35c38-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="35c38-129">När batch-jobbet har avslutats visar fönstret **Resursprisändringar** resultatet av batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="35c38-129">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="35c38-130">Så här får du förslag till resursprisändringar enligt standardpriser</span><span class="sxs-lookup"><span data-stu-id="35c38-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="35c38-131">Om du vill skapa flera alternativa resurspriser baserat på standardpriserna på resurskorten kan du använda ett batch-jobb .</span><span class="sxs-lookup"><span data-stu-id="35c38-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="35c38-132">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursprisändringar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="35c38-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="35c38-133">Välj åtgärden **Föreslå res.prisändring (res)** och fyll sedan i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="35c38-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="35c38-134">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="35c38-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="35c38-135">När batch-jobbet har avslutats öppnar du fönstret **Resursprisändringar** för att visa resultatet av batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="35c38-135">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="35c38-136">Så här får du förslag till resursprisändringar baserat på alternativa priser</span><span class="sxs-lookup"><span data-stu-id="35c38-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="35c38-137">Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.</span><span class="sxs-lookup"><span data-stu-id="35c38-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="35c38-138">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Föreslå res.prisändring (pris)** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="35c38-138">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35c38-139">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="35c38-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="35c38-140">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="35c38-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="35c38-141">När batch-jobbet har avslutats öppnar du fönstret **Resursprisändringar** för att visa resultatet av batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="35c38-141">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="35c38-142">Se även</span><span class="sxs-lookup"><span data-stu-id="35c38-142">See Also</span></span>
[<span data-ttu-id="35c38-143">Projekthantering</span><span class="sxs-lookup"><span data-stu-id="35c38-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="35c38-144">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="35c38-144">Finance</span></span>](finance.md)  
<span data-ttu-id="35c38-145">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="35c38-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="35c38-146">[Försäljning](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="35c38-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="35c38-147">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35c38-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

