---
title: Exportera du Positive Pay-filer | Microsoft Docs
description: Du kan se till att banken bara godkänner validerade checkar och belopp genom att exportera Positive Pay-fil som innehåller information om leverantör betalning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8856ee09ae728d685d3f57786abc29d9aca93778
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750861"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="dfdcd-103">Exportera en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="dfdcd-103">Export a Positive Pay File</span></span>
<span data-ttu-id="dfdcd-104">För att se till att banken bara godkänner validerade checkar och belopp kan du exportera en Positive Pay-fil med relevant leverantörsinformation, checknummer och betalningsbelopp som du sedan skickar till banken som referens när du behandlar betalningar.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="dfdcd-105">är förkonfigurerat för att stödja Positive Pay-filer för Bank of America och City Bank.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="dfdcd-106">Så här skapar du ett bankkonto för Positive Pay</span><span class="sxs-lookup"><span data-stu-id="dfdcd-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="dfdcd-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfdcd-108">Öppna kortet för den bank du vill använda Positive Pay för.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="dfdcd-109">I fältet **Positive Pay exportkod** anger du POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="dfdcd-110">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="dfdcd-111">För att exportera en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="dfdcd-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="dfdcd-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfdcd-113">Välj det bankkonto som du vill exportera en Positive Pay-fil till.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="dfdcd-114">Välj åtgärden **Positive Pay-export**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="dfdcd-115">Sidan **Positive Pay-export** öppnas och visar betalningar som har gjorts för bankkontot efter det sista överföringsdatumet, enligt fälten **senaste överföringsdatum** och **senaste överföringstid**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="dfdcd-116">I fältet **Brytdatum för uppladdning** anger ett datum före vilket betalningar inte inkluderas i den exporterade filen.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="dfdcd-117">Välj åtgärden **Exportera**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="dfdcd-118">Klicka på **Spara** på sidan **Exportera fil** och spara sedan filen till lämplig plats.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="dfdcd-119">Överför filen till din elektroniska bank.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="dfdcd-120">Skriv ner eller kopiera bekräftelsenumret som du får när filuppladdningen till banken lyckas.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="dfdcd-121">Så här visar du exporterade Positive Pay-poster</span><span class="sxs-lookup"><span data-stu-id="dfdcd-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="dfdcd-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfdcd-123">Välj det bankkonto som du vill visa Positive Pay-exportposter för.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="dfdcd-124">Välj åtgärden **Positive Pay-transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="dfdcd-125">På sidan **Positive Pay-transaktioner** kan du se alla Positive Pay-exportposter för bankkontot.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="dfdcd-126">I fältet **bekräftelsenummer** anger du bekräftelsenummer för varje exportpost som du får vid filöverföring till banken.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="dfdcd-127">Om du vill visa de relaterade betalningsraderna väljer du åtgärden **Positive Pay-transaktionsinformation**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="dfdcd-128">Att återexportera Positive Pay-filer</span><span class="sxs-lookup"><span data-stu-id="dfdcd-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="dfdcd-129">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfdcd-130">Välj det bankkonto som du vill återexportera en Positive Pay-fil till.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="dfdcd-131">Välj åtgärden **Positive Pay-transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="dfdcd-132">Välj den rad för Positive Pay-exportfilen som du vill återexportera.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="dfdcd-133">På sidan **Positive Pay-transaktioner** väljer du åtgärden **Återexportera Positive Pay till fil**.</span><span class="sxs-lookup"><span data-stu-id="dfdcd-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfdcd-134">Se även</span><span class="sxs-lookup"><span data-stu-id="dfdcd-134">See Also</span></span>
[<span data-ttu-id="dfdcd-135">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="dfdcd-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="dfdcd-136">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="dfdcd-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="dfdcd-137">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="dfdcd-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="dfdcd-138">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dfdcd-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
