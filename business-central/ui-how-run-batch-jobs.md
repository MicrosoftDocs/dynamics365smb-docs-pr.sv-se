---
title: "Skapa och köra ett batch-jobb | Microsoft Docs"
description: "Du kör batch-jobben för att bearbeta data och uppdatera information, till exempel, att göra regelbundna redovisningsaktiviteter eller för att utföra beräkningar."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9a6435120d122db894bcd6c953da5ab8ea78420b
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="run-batch-jobs"></a><span data-ttu-id="b5872-103">Kör batchjobb</span><span class="sxs-lookup"><span data-stu-id="b5872-103">Run Batch Jobs</span></span>
<span data-ttu-id="b5872-104">Ett batch-jobb i är en rutin som bearbetar data i omgångar, till exempel batch-jobbet **Justera valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="b5872-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="b5872-105">Det finns batch-jobb som utför regelbundna redovisningsaktiviteter, som till exempel att stänga resultaträkningen i slutet av ett räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="b5872-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="b5872-106">Många batch-jobb utför beräkningsarbetet, t.ex beräkning av dröjsmålsränta, valutakursjustering och beräkning av styckkostnaden.</span><span class="sxs-lookup"><span data-stu-id="b5872-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="b5872-107">Ett batch-jobb påminner om en rapport, förutom att batch-jobbet använder resultatet från åtgärden för att uppdatera informationen direkt, i stället för att skriva ut resultatet.</span><span class="sxs-lookup"><span data-stu-id="b5872-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="b5872-108">Så här kör du ett batch-jobb:</span><span class="sxs-lookup"><span data-stu-id="b5872-108">To run a batch job</span></span>
1. <span data-ttu-id="b5872-109">Öppna definitionsfönstret för önskat batch-jobb, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange namnet på batch-jobbet och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b5872-109">To open the request window for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="b5872-110">Om snabbfliken **Alternativ** finns för batch-jobbet fyller du i fälten för att bestämma vad batch-jobbet ska utföra.</span><span class="sxs-lookup"><span data-stu-id="b5872-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="b5872-111">Fönstret kanske innehåller en eller flera snabbflikar med filter, som du kan använda för att begränsa vilka data som ingår i batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="b5872-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="b5872-112">Du kan ange villkor i de föreslagna filtren eller lägga till fler filter.</span><span class="sxs-lookup"><span data-stu-id="b5872-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="b5872-113">Klicka på **OK** för att starta batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="b5872-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5872-114">Se även</span><span class="sxs-lookup"><span data-stu-id="b5872-114">See Also</span></span>
[<span data-ttu-id="b5872-115">Söka, filtrera och sortera data</span><span class="sxs-lookup"><span data-stu-id="b5872-115">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="b5872-116">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b5872-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

