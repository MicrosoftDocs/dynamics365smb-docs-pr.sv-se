---
title: Exportera du Positive Pay-filer | Microsoft Docs
description: Du kan se till att banken bara godkänner validerade checkar och belopp genom att exportera Positive Pay-fil som innehåller information om leverantör betalning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bf57ec93a7c238ecdfe177f77fc85d2ff8249994
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390638"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="fc535-103">Exportera en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="fc535-103">Export a Positive Pay File</span></span>
<span data-ttu-id="fc535-104">För att se till att banken bara godkänner validerade checkar och belopp kan du exportera en Positive Pay-fil med relevant leverantörsinformation, checknummer och betalningsbelopp som du sedan skickar till banken som referens när du behandlar betalningar.</span><span class="sxs-lookup"><span data-stu-id="fc535-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fc535-105">är förkonfigurerat för att stödja Positive Pay-filer för Bank of America och City Bank.</span><span class="sxs-lookup"><span data-stu-id="fc535-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="fc535-106">Så här skapar du ett bankkonto för Positive Pay</span><span class="sxs-lookup"><span data-stu-id="fc535-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="fc535-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc535-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc535-108">Öppna kortet för den bank du vill använda Positive Pay för.</span><span class="sxs-lookup"><span data-stu-id="fc535-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="fc535-109">I fältet **Positive Pay exportkod** anger du POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="fc535-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="fc535-110">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="fc535-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="fc535-111">För att exportera en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="fc535-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="fc535-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc535-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc535-113">Välj det bankkonto som du vill exportera en Positive Pay-fil till.</span><span class="sxs-lookup"><span data-stu-id="fc535-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="fc535-114">Välj åtgärden **Positive Pay-export**.</span><span class="sxs-lookup"><span data-stu-id="fc535-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="fc535-115">Sidan **Positive Pay-export** öppnas och visar betalningar som har gjorts för bankkontot efter det sista överföringsdatumet, enligt fälten **senaste överföringsdatum** och **senaste överföringstid**.</span><span class="sxs-lookup"><span data-stu-id="fc535-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="fc535-116">I fältet **Brytdatum för uppladdning** anger ett datum före vilket betalningar inte inkluderas i den exporterade filen.</span><span class="sxs-lookup"><span data-stu-id="fc535-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="fc535-117">Välj åtgärden **Exportera**.</span><span class="sxs-lookup"><span data-stu-id="fc535-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="fc535-118">Klicka på **Spara** på sidan **Exportera fil** och spara sedan filen till lämplig plats.</span><span class="sxs-lookup"><span data-stu-id="fc535-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="fc535-119">Överför filen till din elektroniska bank.</span><span class="sxs-lookup"><span data-stu-id="fc535-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="fc535-120">Skriv ner eller kopiera bekräftelsenumret som du får när filuppladdningen till banken lyckas.</span><span class="sxs-lookup"><span data-stu-id="fc535-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="fc535-121">Så här visar du exporterade Positive Pay-poster</span><span class="sxs-lookup"><span data-stu-id="fc535-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="fc535-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc535-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc535-123">Välj det bankkonto som du vill visa Positive Pay-exportposter för.</span><span class="sxs-lookup"><span data-stu-id="fc535-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="fc535-124">Välj åtgärden **Positive Pay-transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="fc535-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="fc535-125">På sidan **Positive Pay-transaktioner** kan du se alla Positive Pay-exportposter för bankkontot.</span><span class="sxs-lookup"><span data-stu-id="fc535-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="fc535-126">I fältet **bekräftelsenummer** anger du bekräftelsenummer för varje exportpost som du får vid filöverföring till banken.</span><span class="sxs-lookup"><span data-stu-id="fc535-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="fc535-127">Om du vill visa de relaterade betalningsraderna väljer du åtgärden **Positive Pay-transaktionsinformation**.</span><span class="sxs-lookup"><span data-stu-id="fc535-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="fc535-128">Att återexportera Positive Pay-filer</span><span class="sxs-lookup"><span data-stu-id="fc535-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="fc535-129">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc535-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc535-130">Välj det bankkonto som du vill återexportera en Positive Pay-fil till.</span><span class="sxs-lookup"><span data-stu-id="fc535-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="fc535-131">Välj åtgärden **Positive Pay-transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="fc535-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="fc535-132">Välj den rad för Positive Pay-exportfilen som du vill återexportera.</span><span class="sxs-lookup"><span data-stu-id="fc535-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="fc535-133">På sidan **Positive Pay-transaktioner** väljer du åtgärden **Återexportera Positive Pay till fil**.</span><span class="sxs-lookup"><span data-stu-id="fc535-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc535-134">Se även</span><span class="sxs-lookup"><span data-stu-id="fc535-134">See Also</span></span>
[<span data-ttu-id="fc535-135">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="fc535-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="fc535-136">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="fc535-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="fc535-137">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="fc535-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="fc535-138">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fc535-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]