---
title: "Gruppera anläggningstillgångar | Microsoft Docs"
description: "Du grupperar om en anläggningstillgång till en annan avdelning om du vill dela och kombinera den med andra anläggningstillgångar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 08374662c35dfbdab85097b628a0e0691d75e794
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-split-or-combine-fixed-assets"></a><span data-ttu-id="599c1-103">Överföra, dela eller kombinera anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="599c1-103">Transfer, Split, or Combine Fixed Assets</span></span>
<span data-ttu-id="599c1-104">Du kan använda grupperingsjournalen för anläggningstillgångar när du överför, delar upp och slår ihop anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="599c1-104">You use the fixed asset reclassification journal to transfer, split up, and combine fixed assets.</span></span> <span data-ttu-id="599c1-105">Du visar eller skriver ut resultatet av grupperingen av anläggningstillgångar med rapporten **Anl. - bokföringsvärde 02**.</span><span class="sxs-lookup"><span data-stu-id="599c1-105">You view or print the results of fixed asset reclassification with the **Fixed Asset-Book Value 02** report.</span></span>

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a><span data-ttu-id="599c1-106">Om du vill överföra en anläggningstillgång till en annan avdelning</span><span class="sxs-lookup"><span data-stu-id="599c1-106">To transfer a fixed asset to a different department</span></span>
<span data-ttu-id="599c1-107">Du kan behöva överföra en anläggningstillgång till en annan avdelning, du till exempel placerar en tillgång i produktionsavdelningen när den är under utveckling och sedan flyttar den till administrationsavdelningen när den är färdig.</span><span class="sxs-lookup"><span data-stu-id="599c1-107">You may need to transfer a fixed asset to a different department when, for example, you place an asset in the production department while it is under construction and then move it to the administration department when it is finished.</span></span>  

1. <span data-ttu-id="599c1-108">Skapa en ny anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="599c1-108">Set up a new fixed asset.</span></span> <span data-ttu-id="599c1-109">Ange den nya avdelningen i fältet **Avdelningskod**.</span><span class="sxs-lookup"><span data-stu-id="599c1-109">Enter the new department in the **Department Code** field.</span></span>
2. <span data-ttu-id="599c1-110">Tilldela en avskrivningsregel för anläggningstillgång till den nya anläggningstillgången.</span><span class="sxs-lookup"><span data-stu-id="599c1-110">Assign a fixed asset depreciation book to the new fixed asset.</span></span> <span data-ttu-id="599c1-111">Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="599c1-111">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>
3. <span data-ttu-id="599c1-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anl. grupperingsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Reclass. Journals**, and then choose the related link.</span></span>
4. <span data-ttu-id="599c1-113">Skapa en grupperingsjournal där fältet **Anl.nr.** innehåller den ursprungliga anläggningstillgången och fältet **Nytt anl.nr** innehåller den nya anläggningstillgången som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="599c1-113">Create a reclassification journal where the **FA No.** field contains the original fixed asset, and the **New FA No.** field contains the new fixed asset to be moved.</span></span>  
5. <span data-ttu-id="599c1-114">Välj åtgärden **Gruppera**.</span><span class="sxs-lookup"><span data-stu-id="599c1-114">Choose the **Reclassify** action.</span></span>

    <span data-ttu-id="599c1-115">Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett i fönstret **Anl. journalinställningar** för den angivna avskrivningsregeln.</span><span class="sxs-lookup"><span data-stu-id="599c1-115">Two lines are now created in the fixed asset G/L journal using the template and batch that you have specified in the **FA Journal Setup** window for the specified depreciation book.</span></span> <span data-ttu-id="599c1-116">Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="599c1-116">For more information, see [Set Up Fixed Asset Depreciation](fa-how-setup-depreciation.md).</span></span>
6. <span data-ttu-id="599c1-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>    
7. <span data-ttu-id="599c1-118">I fönstret **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 4 och 5.</span><span class="sxs-lookup"><span data-stu-id="599c1-118">In the **Fixed Asset G/L Journal** window, choose the **Post** action to post the reclassification that you performed in steps 4 and 5.</span></span>

<span data-ttu-id="599c1-119">Om du har bokfört en anskaffningskostnad för en tillgång kan du använda grupperingsjournalen för anläggningstillgångar när du vill dela upp anskaffningskostnaden på flera tillgångar.</span><span class="sxs-lookup"><span data-stu-id="599c1-119">If you have posted an acquisition cost for one asset, you can use the fixed asset reclassification journal to split the acquisition cost among several assets.</span></span>  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a><span data-ttu-id="599c1-120">Om du vill dela en anläggningstillgång i tre anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="599c1-120">To split a fixed asset into three fixed assets</span></span>
<span data-ttu-id="599c1-121">Du kan dela upp en anläggningstillgång till åtskilliga anläggningstillgångar, till exempel när du vill fördela en anläggningstillgång till tre olika avdelningar.</span><span class="sxs-lookup"><span data-stu-id="599c1-121">You can split one fixed asset into multiple fixed assets, for example when you need to distribute a fixed asset onto three different departments.</span></span> <span data-ttu-id="599c1-122">Du kan till exempel flytta 25 % av anskaffningskostnaden och avskrivningskostnaden för den ursprungliga anläggningstillgången till en andra anläggningstillgång och 45 % till en tredje tillgång.</span><span class="sxs-lookup"><span data-stu-id="599c1-122">In that case, you can move, for example, 25 percent of the acquisition cost and depreciation for the original fixed asset to the second fixed asset and 45 percent to the third asset.</span></span> <span data-ttu-id="599c1-123">De återstående 30 % kvarstår på den ursprungliga anläggningstillgången.</span><span class="sxs-lookup"><span data-stu-id="599c1-123">The remaining 30 percent will remain on the original fixed asset.</span></span>

1. <span data-ttu-id="599c1-124">Skapa två nya anläggningstillgången.</span><span class="sxs-lookup"><span data-stu-id="599c1-124">Set up two new fixed assets.</span></span> <span data-ttu-id="599c1-125">Ange den nya avdelningen i fältet **Avdelningskod**.</span><span class="sxs-lookup"><span data-stu-id="599c1-125">Enter the new department in the **Department Code** field.</span></span>
2. <span data-ttu-id="599c1-126">Tilldela en avskrivningsregel för anläggningstillgång till den nya anläggningstillgången.</span><span class="sxs-lookup"><span data-stu-id="599c1-126">Assign fixed asset depreciation books to the new fixed assets.</span></span> <span data-ttu-id="599c1-127">Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="599c1-127">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>
3. <span data-ttu-id="599c1-128">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anl. grupperingsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Reclass. Journals**, and then choose the related link.</span></span>
4. <span data-ttu-id="599c1-129">Skapa två grupperingsjournalrader, en för varje ny anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="599c1-129">Create two reclassification journal lines, one for each new fixed asset.</span></span>
5. <span data-ttu-id="599c1-130">På den första raden anger du den andra anläggningstillgången i fältet **Nytt anl.nr** och 25 i fältet **Gruppera anskaff.kost. %**.</span><span class="sxs-lookup"><span data-stu-id="599c1-130">On the first line, enter the second fixed asset in the **New FA No.** field and 25 in the **Reclassify Acq. Cost %** field.</span></span>
6. <span data-ttu-id="599c1-131">På den andra raden anger du den tredje anläggningstillgången i fältet **Nytt anl.nr** och 40 i fältet **Gruppera anskaff.kost. %**.</span><span class="sxs-lookup"><span data-stu-id="599c1-131">On the second line, enter the third fixed asset in the **New FA No.** field and 40 in the **Reclassify Acq. Cost %** field.</span></span>
7. <span data-ttu-id="599c1-132">På båda rader markerar du kryssrutorna **Gruppera anskaff.kost.** och **Gruppera avskrivning**.</span><span class="sxs-lookup"><span data-stu-id="599c1-132">On both lines, select the **Reclassify Acquisition Cost** and **Reclassify Depreciation** check boxes.</span></span>   
8. <span data-ttu-id="599c1-133">Välj åtgärden **Gruppera**.</span><span class="sxs-lookup"><span data-stu-id="599c1-133">Choose the **Reclassify** action.</span></span>

    <span data-ttu-id="599c1-134">Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett i fönstret **Anl. journalinställningar** för den angivna avskrivningsregeln.</span><span class="sxs-lookup"><span data-stu-id="599c1-134">Two lines are now created in the fixed asset G/L journal using the template and batch that you have specified in the **FA Journal Setup** window for the specified depreciation book.</span></span> <span data-ttu-id="599c1-135">Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="599c1-135">For more information, see [Set Up Fixed Asset Depreciation](fa-how-setup-depreciation.md).</span></span>    
9. <span data-ttu-id="599c1-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>
10. <span data-ttu-id="599c1-137">I fönstret **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 4 till 8.</span><span class="sxs-lookup"><span data-stu-id="599c1-137">In the **Fixed Asset G/L Journal** window, choose the **Post** action to post the reclassification that you performed in steps 4 through 8.</span></span>

## <a name="to-combine-two-fixed-assets-into-one"></a><span data-ttu-id="599c1-138">Om du vill kombinera flera anläggningstillgångar till en</span><span class="sxs-lookup"><span data-stu-id="599c1-138">To combine two fixed assets into one</span></span>
<span data-ttu-id="599c1-139">Du kan kombinera flera anläggningstillgångar till en anläggningstillgång, till exempel när du vill flytta distribuerade anläggningstillgångar till en avdelning.</span><span class="sxs-lookup"><span data-stu-id="599c1-139">You can combine multiple fixed assets into one fixed asset, for example when you move distributed fixed assets into one department.</span></span> <span data-ttu-id="599c1-140">Om du har bokfört anskaffningskostnader och avskrivning anläggningstillgång som ska flyttas, kombineras dessa värden i en enda anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="599c1-140">If you have posted acquisition costs and depreciation for the fixed asset to be moved, those values will be combined in the single fixed asset.</span></span>

1. <span data-ttu-id="599c1-141">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anl. grupperingsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="599c1-142">Skapa en grupperingsjournal där fältet **Anl.nr.** innehåller den anläggningstillgången som ska flyttas/kombineras och fältet **Nytt anl.nr** innehåller den nya anläggningstillgången som ska kombineras med.</span><span class="sxs-lookup"><span data-stu-id="599c1-142">Create a reclassification journal where the **FA No.** field contains the fixed asset to be moved/combined, and the **New FA No.** field contains the fixed asset that it will be combined with.</span></span>
3. <span data-ttu-id="599c1-143">Lämna fältet **Gruppera anskaff.kost. %** tomt om du vill flytta/kombinera den totala anskaffningskostnaden.</span><span class="sxs-lookup"><span data-stu-id="599c1-143">Leave the **Reclassify Acq. Cost %** field empty to move/combine the entire acquisition cost.</span></span>    
4. <span data-ttu-id="599c1-144">Välj kryssrutorna **Gruppera anskaff.kost.** och **Gruppera avskrivning**.</span><span class="sxs-lookup"><span data-stu-id="599c1-144">Select the **Reclassify Acquisition Cost** and **Reclassify Depreciation** check boxes.</span></span>
5. <span data-ttu-id="599c1-145">Välj **Gruppering**på fliken **Åtgärder**.</span><span class="sxs-lookup"><span data-stu-id="599c1-145">On the **Actions** tab, choose **Reclassify**.</span></span>

    <span data-ttu-id="599c1-146">Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett i fönstret **Anl. journalinställningar** för den angivna avskrivningsregeln.</span><span class="sxs-lookup"><span data-stu-id="599c1-146">Two lines are now created in the fixed asset G/L journal using the template and batch that you have specified in the **FA Journal Setup** window for the specified depreciation book.</span></span> <span data-ttu-id="599c1-147">Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="599c1-147">For more information, see [Set Up Fixed Asset Depreciation](fa-how-setup-depreciation.md).</span></span>   
6. <span data-ttu-id="599c1-148">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>
7. <span data-ttu-id="599c1-149">I fönstret **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 2 till 5.</span><span class="sxs-lookup"><span data-stu-id="599c1-149">In the **Fixed Asset G/L Journal** window, choose the **Post** action to post the reclassification that you performed in steps 2 through 5.</span></span>

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a><span data-ttu-id="599c1-150">Så här visar du ändrade avskrivningsregelvärden som beror på gruppering av anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="599c1-150">To view changed depreciation book values due to fixed asset reclassification</span></span>
1. <span data-ttu-id="599c1-151">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anl.bokföringsvärde 02** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="599c1-151">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Book Value 02**, and then choose the related link.</span></span>
2. <span data-ttu-id="599c1-152">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="599c1-152">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="599c1-153">Välj knappen **Skriv ut** eller **Förhandsgranska**.</span><span class="sxs-lookup"><span data-stu-id="599c1-153">Choose the **Print** or **Preview** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="599c1-154">Se även</span><span class="sxs-lookup"><span data-stu-id="599c1-154">See Also</span></span>
[<span data-ttu-id="599c1-155">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="599c1-155">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="599c1-156">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="599c1-156">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="599c1-157">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="599c1-157">Finance</span></span>](finance.md)  
[<span data-ttu-id="599c1-158">Komma igång</span><span class="sxs-lookup"><span data-stu-id="599c1-158">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="599c1-159">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="599c1-159">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
