---
title: Avsluta bokföringsperioder för räkenskapsåret | Microsoft Docs
description: Beskriver hur du avslutar bokföringsperioder som utgör räkenskapsåret.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e49f067eb0410e3d2f6f84241ae83be041bce918
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925378"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="ea3f2-103">Avsluta bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="ea3f2-103">Close Accounting Periods</span></span>
<span data-ttu-id="ea3f2-104">När ett räkenskapsår är slut måste du avsluta perioderna som året omfattar.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="ea3f2-105">Så här avslutar du bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="ea3f2-105">To close accounting periods</span></span>
1. <span data-ttu-id="ea3f2-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokföringsperiod** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea3f2-107">På sidan **Bokföringsperioder** väljer du åtgärden **Avsluta år**.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="ea3f2-108">Om flera räkenskapsår är öppna kommer det tidigaste att stängas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="ea3f2-109">Visar ett meddelande för vilket år som ska stängas och konsekvenserna av att stänga året.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="ea3f2-110">Välj **ja** för att stänga året.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="ea3f2-111">Räkenskapsåret stängs och fälten **Avslutat** och **Låst datum** markeras för samtliga perioder i året.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="ea3f2-112">Räkenskapsåret kan inte öppnas igen och du kan inte heller ta bort markeringen i fälten **Avslutat** eller **Låst datum**.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ea3f2-113">Du kan inte avsluta ett räkenskapsår förrän du har upprättat ett nytt.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="ea3f2-114">Notera att du inte kan ändra startdatumet för det följande räkenskapsåret när räkenskapsåret är avslutat.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="ea3f2-115">Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="ea3f2-116">När du gör det markeras transaktionerna som bokförda på ett avslutat räkenskapsår och fältet **Föregående års transaktion** markeras.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="ea3f2-117">När ett räkenskapsår har avslutats måste resultatkontona avslutas och årets resultat flyttas över till ett konto i balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="ea3f2-118">Du kan göra samma sak varje gång du bokför på det avslutade räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="ea3f2-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea3f2-119">Se även</span><span class="sxs-lookup"><span data-stu-id="ea3f2-119">See Also</span></span>

[<span data-ttu-id="ea3f2-120">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="ea3f2-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="ea3f2-121">Bokför årsslutstransaktionen</span><span class="sxs-lookup"><span data-stu-id="ea3f2-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="ea3f2-122">Arbeta med bokföringsperioder och räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="ea3f2-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="ea3f2-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea3f2-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
