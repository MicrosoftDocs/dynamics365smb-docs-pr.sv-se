---
title: "Granska och bokför du årsslutstransaktionen | Microsoft Docs"
description: "Beskriver hur du öppnar den journal du har angett i batch-jobbet Avslut av resultatkonton och sedan granska och bokföra årsslutstransaktionen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4263f6b3260dd5b8e8fad4f515dcdb61e12eb012
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="50251-103">Bokför årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="50251-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="50251-104">När du har använt batch-jobbet **Avslut av resultatkonton** för att generera transaktioner eller bokslutsposter för årsslut, måste du öppna den journal du har angett i batch-jobbet och sedan granska och bokföra transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="50251-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="50251-105">Så här bokför du årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="50251-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="50251-106">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="50251-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="50251-107">I fönstret **Redovisningsjournal** i fältet **Batch-namn** väljer du den batch som innehåller årsavslutstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="50251-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="50251-108">Granska transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="50251-108">Review the entries.</span></span>
4. <span data-ttu-id="50251-109">Om du vill bokföra journalen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="50251-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="50251-110">Om ett fel påträffas visas ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="50251-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="50251-111">Om bokföringen utförs tas de bokförda transaktionerna bort från journalen.</span><span class="sxs-lookup"><span data-stu-id="50251-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="50251-112">Efter bokföringen bokförs en transaktion på varje resultatkonto så att saldot blir noll och årets resultat överförs till balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="50251-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="50251-113">Se även</span><span class="sxs-lookup"><span data-stu-id="50251-113">See Also</span></span>
[<span data-ttu-id="50251-114">Avsluta bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="50251-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="50251-115">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="50251-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="50251-116">Avslut av resultatkonton</span><span class="sxs-lookup"><span data-stu-id="50251-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="50251-117">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50251-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
