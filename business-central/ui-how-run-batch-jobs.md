---
title: Skapa och köra ett batch-jobb | Microsoft Docs
description: Du kör batch-jobben för att bearbeta data och uppdatera information, till exempel, att göra regelbundna redovisningsaktiviteter eller för att utföra beräkningar.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: c54edd1e907c27aca719898319f69f98c0a0a068
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195609"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="8dd80-103">Kör batch-jobb och XML-portar</span><span class="sxs-lookup"><span data-stu-id="8dd80-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="8dd80-104">Ett batch-jobb i är en rutin som bearbetar data i omgångar, till exempel batch-jobbet **Justera valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="8dd80-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="8dd80-105">Det finns batch-jobb som utför regelbundna redovisningsaktiviteter, som till exempel att stänga resultaträkningen i slutet av ett räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="8dd80-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="8dd80-106">Många batch-jobb utför beräkningsarbetet, t.ex beräkning av dröjsmålsränta, valutakursjustering och beräkning av styckkostnaden.</span><span class="sxs-lookup"><span data-stu-id="8dd80-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="8dd80-107">Ett batch-jobb påminner om en rapport, förutom att batch-jobbet använder resultatet från åtgärden för att uppdatera informationen direkt, i stället för att skriva ut resultatet.</span><span class="sxs-lookup"><span data-stu-id="8dd80-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="8dd80-108">Du kan schemalägga när ett batchjobb körs.</span><span class="sxs-lookup"><span data-stu-id="8dd80-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="8dd80-109">Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="8dd80-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="8dd80-110">Så här kör du ett batch-jobb:</span><span class="sxs-lookup"><span data-stu-id="8dd80-110">To run a batch job</span></span>
1. <span data-ttu-id="8dd80-111">För att öppna sidan för begäran tillhörande relevant batch-jobb väljer du ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), anger namnet på batch-jobbet och väljer sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8dd80-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="8dd80-112">Om snabbfliken **Alternativ** finns för batch-jobbet fyller du i fälten för att bestämma vad batch-jobbet ska utföra.</span><span class="sxs-lookup"><span data-stu-id="8dd80-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="8dd80-113">Sidan kanske innehåller en eller flera snabbflikar med filter, som du kan använda för att begränsa vilka data som ingår i batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="8dd80-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="8dd80-114">Du kan ange villkor i de föreslagna filtren eller lägga till fler filter.</span><span class="sxs-lookup"><span data-stu-id="8dd80-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="8dd80-115">Klicka på **OK** för att starta batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="8dd80-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="8dd80-116">Se även</span><span class="sxs-lookup"><span data-stu-id="8dd80-116">See Also</span></span>
[<span data-ttu-id="8dd80-117">Sortera, söka och filtrera listor</span><span class="sxs-lookup"><span data-stu-id="8dd80-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="8dd80-118">Använda jobbköer för att schemalägga uppgifter</span><span class="sxs-lookup"><span data-stu-id="8dd80-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="8dd80-119">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8dd80-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
