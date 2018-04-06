---
title: "Avsluta bokföringsperioder för räkenskapsåret | Microsoft Docs"
description: "Beskriver hur du avslutar bokföringsperioder som utgör räkenskapsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e136195c7b89635ca85601cdae5047493c237d09
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="close-accounting-periods"></a><span data-ttu-id="797ca-103">Avsluta bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="797ca-103">Close Accounting Periods</span></span>
<span data-ttu-id="797ca-104">När ett räkenskapsår är slut måste du avsluta perioderna som året omfattar.</span><span class="sxs-lookup"><span data-stu-id="797ca-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="797ca-105">Så här avslutar du bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="797ca-105">To close accounting periods</span></span>
1. <span data-ttu-id="797ca-106">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokföringsperioder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="797ca-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="797ca-107">I fönstret **Bokföringsperioder** väljer du åtgärden **Avsluta år**.</span><span class="sxs-lookup"><span data-stu-id="797ca-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="797ca-108">Om flera räkenskapsår är öppna kommer det tidigaste att stängas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="797ca-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="797ca-109">Visar ett meddelande för vilket år som ska stängas och konsekvenserna av att stänga året.</span><span class="sxs-lookup"><span data-stu-id="797ca-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="797ca-110">Välj **ja** för att stänga året.</span><span class="sxs-lookup"><span data-stu-id="797ca-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="797ca-111">Räkenskapsåret stängs och fälten **Avslutat** och **Låst datum** markeras för samtliga perioder i året.</span><span class="sxs-lookup"><span data-stu-id="797ca-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="797ca-112">Räkenskapsåret kan inte öppnas igen och du kan inte heller ta bort markeringen i fälten **Avslutat** eller **Låst datum**.</span><span class="sxs-lookup"><span data-stu-id="797ca-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="797ca-113">Du kan inte avsluta ett räkenskapsår förrän du har upprättat ett nytt.</span><span class="sxs-lookup"><span data-stu-id="797ca-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="797ca-114">Notera att du inte kan ändra startdatumet för det följande räkenskapsåret när räkenskapsåret är avslutat.</span><span class="sxs-lookup"><span data-stu-id="797ca-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="797ca-115">Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året.</span><span class="sxs-lookup"><span data-stu-id="797ca-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="797ca-116">När du gör det markeras transaktionerna som bokförda på ett avslutat räkenskapsår och fältet **Föregående års transaktion** markeras.</span><span class="sxs-lookup"><span data-stu-id="797ca-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="797ca-117">När ett räkenskapsår har avslutats måste resultatkontona avslutas och årets resultat flyttas över till ett konto i balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="797ca-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="797ca-118">Du kan göra samma sak varje gång du bokför på det avslutade räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="797ca-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="797ca-119">Se även</span><span class="sxs-lookup"><span data-stu-id="797ca-119">See Also</span></span>
[<span data-ttu-id="797ca-120">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="797ca-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="797ca-121">Bokför årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="797ca-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="797ca-122">Så här öppnar du ett nytt räkenskapsår:</span><span class="sxs-lookup"><span data-stu-id="797ca-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="797ca-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="797ca-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

