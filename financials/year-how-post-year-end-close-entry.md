---
title: "Granska och bokför du årsslutstransaktionen | Microsoft Docs"
description: "Beskriver hur du öppnar den journal du har angett i batch-jobbet Avslut av resultatkonton och sedan granska och bokföra årsslutstransaktionen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a><span data-ttu-id="d5e7c-103">Så här bokför du årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="d5e7c-103">How to: Post the Year-End Closing Entry</span></span>
<span data-ttu-id="d5e7c-104">När du har använt batch-jobbet **Avslut av resultatkonton** för att generera transaktioner eller bokslutsposter för årsslut, måste du öppna den journal du har angett i batch-jobbet och sedan granska och bokföra transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="d5e7c-105">Så här bokför du årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="d5e7c-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="d5e7c-106">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5e7c-107">I fönstret **Redovisningsjournal** i fältet **Batch-namn** väljer du den batch som innehåller årsavslutstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="d5e7c-108">Granska transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-108">Review the entries.</span></span>
4. <span data-ttu-id="d5e7c-109">Om du vill bokföra journalen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d5e7c-110">Om ett fel påträffas visas ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="d5e7c-111">Om bokföringen utförs tas de bokförda transaktionerna bort från journalen.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="d5e7c-112">Efter bokföringen bokförs en transaktion på varje resultatkonto så att saldot blir noll och årets resultat överförs till balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5e7c-113">Se även</span><span class="sxs-lookup"><span data-stu-id="d5e7c-113">See Also</span></span>
[<span data-ttu-id="d5e7c-114">Så här avslutar du bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="d5e7c-114">How to: Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="d5e7c-115">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="d5e7c-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d5e7c-116">Avslut av resultatkonton</span><span class="sxs-lookup"><span data-stu-id="d5e7c-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="d5e7c-117">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5e7c-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

