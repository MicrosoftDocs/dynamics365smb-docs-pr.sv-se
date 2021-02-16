---
title: Avyttra eller ställa av anläggningstillgångar | Microsoft Docs
description: Vid kassation, försäljning eller avställning av en anläggningstillgång måste du bokföra ett avyttringsvärde.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 16d052c67a2d9b5513e9dac901dfeddce0527512
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749424"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="a136a-103">Avyttra eller ställa av anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="a136a-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="a136a-104">När du säljer eller på annat sätt avyttrar en anläggningstillgång, måste avyttringsvärdet bokföras för att beräkna och registrera vinst eller förlust.</span><span class="sxs-lookup"><span data-stu-id="a136a-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="a136a-105">En avyttringstransaktion måste vara den sista bokförda transaktionen för en anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="a136a-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="a136a-106">För delvis avyttrade anläggningstillgångar kan du bokföra fler än en avyttringstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a136a-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="a136a-107">Summan av alla bokförda avyttringsbelopp måste vara ett kreditbelopp.</span><span class="sxs-lookup"><span data-stu-id="a136a-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="a136a-108">Om du byter en anläggningstillgång mot en annan måste du registrera både försäljningen av den gamla tillgången (avyttring) och inköpet av den nya (anskaffning).</span><span class="sxs-lookup"><span data-stu-id="a136a-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="a136a-109">Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="a136a-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="a136a-110">Följande åtgärder förutsätter att du redan har skapat relevanta bokföringsmallar på sidan **Anl. bokföringsmallar**.</span><span class="sxs-lookup"><span data-stu-id="a136a-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="a136a-111">Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="a136a-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="a136a-112">Bokföra en avyttringstransaktion i redovisningsjournalen för anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="a136a-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="a136a-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Redovisningsjournaler för anläggningstillgång** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a136a-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a136a-114">Skapa en första journalrad och fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="a136a-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="a136a-115">Välj **Anskaffningskostnad** i fältet **Avyttring**.</span><span class="sxs-lookup"><span data-stu-id="a136a-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="a136a-116">Välj åtgärden **Infoga anl. motkonto**.</span><span class="sxs-lookup"><span data-stu-id="a136a-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="a136a-117">En andra journalrad skapas för motkontot som ställs in för bokföring av avyttring.</span><span class="sxs-lookup"><span data-stu-id="a136a-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a136a-118">Steg 4 fungerar bara om du har ställt in följande: På sidan **Anl. bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Avyttringskonto** redovisningsdebitkontot och fältet **Avuttringskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning.</span><span class="sxs-lookup"><span data-stu-id="a136a-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="a136a-119">Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="a136a-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="a136a-120">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="a136a-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="a136a-121">Om du säljer eller på annat sätt avyttrar en del av en anläggningstillgång måste du dela upp tillgången innan du kan registrera avyttringstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="a136a-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="a136a-122">För mer information, se [Så här överför, delar eller kombinerar du anläggningstillgångar](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="a136a-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="a136a-123">Så här visar du avyttringstransaktioner</span><span class="sxs-lookup"><span data-stu-id="a136a-123">To view disposal ledger entries</span></span>
<span data-ttu-id="a136a-124">När du säljer eller avyttrar en anläggningstillgång måste avyttringsvärdet bokföras på redovisningskonton där du kan se resultatet.</span><span class="sxs-lookup"><span data-stu-id="a136a-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="a136a-125">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a136a-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a136a-126">Markera den fasta anläggningstillgång som du vill visa poster för välj sedan åtgärden **Avskrivningsregler**.</span><span class="sxs-lookup"><span data-stu-id="a136a-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="a136a-127">Markera den avskrivningsregel som du vill visa poster för välj sedan åtgärden **Transaktionsposter**.</span><span class="sxs-lookup"><span data-stu-id="a136a-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="a136a-128">Markera en rad med **Avyttring** i fältet **Anl. bokföringskategori** och klicka sedan på åtgärden **Hitta transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a136a-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Find Entries** action.</span></span>  
5. <span data-ttu-id="a136a-129">På sidan **Hitta transaktioner** väljer du redovisningstransaktionen och väljer sedan åtgärden **Visa relaterade transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a136a-129">On the **Find Entries** page, select the general ledger entry line, and then choose the **Show Related Entries** action.</span></span>  

<span data-ttu-id="a136a-130">Sidan **Redovisningstransaktioner** öppnas där du kan visa de transaktioner som förfogandeinlägget ledde till.</span><span class="sxs-lookup"><span data-stu-id="a136a-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a136a-131">Se även</span><span class="sxs-lookup"><span data-stu-id="a136a-131">See Also</span></span>

[<span data-ttu-id="a136a-132">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="a136a-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="a136a-133">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="a136a-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="a136a-134">[Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="a136a-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="a136a-135">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="a136a-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="a136a-136">Komma igång</span><span class="sxs-lookup"><span data-stu-id="a136a-136">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="a136a-137">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a136a-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a136a-138">Hitta transaktioner</span><span class="sxs-lookup"><span data-stu-id="a136a-138">Find Entries</span></span>](ui-find-entries.md)  
