---
title: Bokför årsslutstransaktionen
description: Beskriver hur du öppnar den journal du har angett i batch-jobbet Avslut av resultatkonton och sedan granska och bokföra årsslutstransaktionen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493359"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="6974e-103">Bokför årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="6974e-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="6974e-104">När du har använt batch-jobbet **Avslut av resultatkonton** för att generera transaktioner eller bokslutsposter för årsslut, måste du öppna den journal du har angett i batch-jobbet och sedan granska och bokföra transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="6974e-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="6974e-105">Beroende på organisationens arbetsprocesser kan du välja att avsluta eller inte avsluta bokföringsperioder och räkenskapsår i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6974e-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6974e-106">Följande procedur förutsätter att du har avslutat räkenskapsåret med hjälp av alternativet *Bokföringsperioder*, genererat en årsbokslutstransaktion med hjälp av batchjobbet **Avsluta resultaträkning** och är nu redo att bokföra årsbokslutstransaktionen tillsammans med kontoposter för motbokskapital.</span><span class="sxs-lookup"><span data-stu-id="6974e-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="6974e-107">Organisationen kan välja att arbeta annorlunda, till exempel bokföra årsbokslutstransaktionen som en del av räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6974e-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="6974e-108">Så här bokför du årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="6974e-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="6974e-109">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6974e-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6974e-110">På sidan **Redovisningsjournal** i fältet **Batch-namn** väljer du den batch som innehåller årsavslutstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="6974e-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="6974e-111">Granska transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="6974e-111">Review the entries.</span></span>
4. <span data-ttu-id="6974e-112">Om du vill bokföra journalen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="6974e-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="6974e-113">Om ett fel påträffas visas ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="6974e-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="6974e-114">Om bokföringen utförs tas de bokförda transaktionerna bort från journalen.</span><span class="sxs-lookup"><span data-stu-id="6974e-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="6974e-115">Efter bokföringen bokförs en transaktion på varje resultatkonto så att saldot blir noll och årets resultat överförs till balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="6974e-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="6974e-116">Se även</span><span class="sxs-lookup"><span data-stu-id="6974e-116">See Also</span></span>

[<span data-ttu-id="6974e-117">Avsluta bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="6974e-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="6974e-118">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="6974e-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="6974e-119">Avslut av resultatkonton</span><span class="sxs-lookup"><span data-stu-id="6974e-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="6974e-120">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6974e-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]