---
title: "Avyttra eller ställa av anläggningstillgångar | Microsoft Docs"
description: "Vid kassation, försäljning eller avställning av en anläggningstillgång måste du bokföra ett avyttringsvärde."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f2ccb2c7c020220383591c468b9f0729722ea1b8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="7ff76-103">Avyttra eller ställa av anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="7ff76-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="7ff76-104">När du säljer eller på annat sätt avyttrar en anläggningstillgång, måste avyttringsvärdet bokföras för att beräkna och registrera vinst eller förlust.</span><span class="sxs-lookup"><span data-stu-id="7ff76-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="7ff76-105">En avyttringstransaktion måste vara den sista bokförda transaktionen för en anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="7ff76-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="7ff76-106">För delvis avyttrade anläggningstillgångar kan du bokföra fler än en avyttringstransaktion.</span><span class="sxs-lookup"><span data-stu-id="7ff76-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="7ff76-107">Summan av alla bokförda avyttringsbelopp måste vara ett kreditbelopp.</span><span class="sxs-lookup"><span data-stu-id="7ff76-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="7ff76-108">Om du byter en anläggningstillgång mot en annan måste du registrera både försäljningen av den gamla tillgången (avyttring) och inköpet av den nya (anskaffning).</span><span class="sxs-lookup"><span data-stu-id="7ff76-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="7ff76-109">Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="7ff76-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="7ff76-110">Bokföra en avyttringstransaktion i redovisningsjournalen för anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="7ff76-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="7ff76-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7ff76-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7ff76-112">Skapa en första journalrad och fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="7ff76-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="7ff76-113">Välj **Anskaffningskostnad** i fältet **Avyttring**.</span><span class="sxs-lookup"><span data-stu-id="7ff76-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="7ff76-114">Välj åtgärden **Infoga anl. motkonto**.</span><span class="sxs-lookup"><span data-stu-id="7ff76-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="7ff76-115">En andra journalrad skapas för motkontot som ställs in för bokföring av avyttring.</span><span class="sxs-lookup"><span data-stu-id="7ff76-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="7ff76-116">Steg 4 fungerar bara om du har ställt in följande: I fönstret **Anl. bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Avyttringskonto** redovisningsdebitkontot och fältet **Avuttringskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning.</span><span class="sxs-lookup"><span data-stu-id="7ff76-116">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="7ff76-117">För mer information, se avsnittet "Att ställa in bokföringsmallar för anläggningstillgångar" i avsnittet [Så här ställer du in allmän information för anläggningstillgångar](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="7ff76-117">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="7ff76-118">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="7ff76-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="7ff76-119">Om du säljer eller på annat sätt avyttrar en del av en anläggningstillgång måste du dela upp tillgången innan du kan registrera avyttringstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="7ff76-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="7ff76-120">För mer information, se [Så här överför, delar eller kombinerar du anläggningstillgångar](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="7ff76-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="7ff76-121">Så här visar du avyttringstransaktioner</span><span class="sxs-lookup"><span data-stu-id="7ff76-121">To view disposal ledger entries</span></span>
<span data-ttu-id="7ff76-122">När du säljer eller avyttrar en anläggningstillgång måste avyttringsvärdet bokföras på redovisningskonton där du kan se resultatet.</span><span class="sxs-lookup"><span data-stu-id="7ff76-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="7ff76-123">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7ff76-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7ff76-124">Markera den fasta anläggningstillgång som du vill visa poster för välj sedan åtgärden **Avskrivningsregler**.</span><span class="sxs-lookup"><span data-stu-id="7ff76-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="7ff76-125">Markera den avskrivningsregel som du vill visa poster för välj sedan åtgärden **Transaktionsposter**.</span><span class="sxs-lookup"><span data-stu-id="7ff76-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="7ff76-126">Markera en rad med **Avyttring** i fältet **Anl. bokföringskategori** och klicka sedan på åtgärden **Analysera**, .</span><span class="sxs-lookup"><span data-stu-id="7ff76-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="7ff76-127">I fönstret **Analysera** väljer du redovisningstransaktionen och väljer sedan åtgärden **Visa**.</span><span class="sxs-lookup"><span data-stu-id="7ff76-127">In the **Navigate** window, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="7ff76-128">Fönstret **Redovisningstransaktioner** öppnas där du kan visa de transaktioner som förfogandeinlägget ledde till.</span><span class="sxs-lookup"><span data-stu-id="7ff76-128">The **General Ledger Entries** window opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7ff76-129">Se även</span><span class="sxs-lookup"><span data-stu-id="7ff76-129">See Also</span></span>
[<span data-ttu-id="7ff76-130">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="7ff76-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="7ff76-131">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="7ff76-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="7ff76-132">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="7ff76-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="7ff76-133">Komma igång</span><span class="sxs-lookup"><span data-stu-id="7ff76-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="7ff76-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7ff76-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

