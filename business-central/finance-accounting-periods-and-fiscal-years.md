---
title: Arbeta med bokföringsperioder och räkenskapsår | Microsoft Docs
description: Lär dig hur du arbetar med bokföringsperioder för att definiera när företaget rapporterar resultat.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 50df903e664f98f038a82c646dd3bd9c2f5ef479
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "936630"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a><span data-ttu-id="2f6bf-103">Arbeta med bokföringsperioder och räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f6bf-103">Working with Accounting Periods and Fiscal Years</span></span>
<span data-ttu-id="2f6bf-104">Bokföringsperioder som även kallas rapporteringsperioder, är perioder som ett företag eller en organisation rapporterar resultat, exempelvis genom att generera deras resultat- eller balansräkning.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-104">Accounting periods, which are also known as reporting periods, are periods of time for which a company or organization reports financial performance, for example, by generating their income statement or balance sheet.</span></span> <span data-ttu-id="2f6bf-105">Bokföringsperioder avser vanligtvis företagets räkenskapsår, som kan innehålla flera bokföringsperioder, till exempel månader eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-105">Typically, accounting periods refer to the company's fiscal year, which can contain several accounting periods, such as months or quarters.</span></span>

<span data-ttu-id="2f6bf-106">För många företag sammanfaller räkenskapsåret inte med kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-106">For many companies the fiscal year does not align with the calendar year.</span></span> <span data-ttu-id="2f6bf-107">Till exempel slutar räkenskapsåret den 30 juni i stället för den 31 december.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-107">For example, the fiscal year might end on June 30th rather than December 31st.</span></span> <span data-ttu-id="2f6bf-108">För nyskapade företag kan räkenskapsåret vara längre än tolv månader.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-108">For newly created companies, the fiscal might actually be longer than 12 months.</span></span> 

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2f6bf-109">kräver endast bokföringsperioder om du vill avsluta en resultaträkning eller köra aktiviteter för datakomprimering.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-109">only requires accounting periods only if you want to close an income statement, or run data compression tasks.</span></span> 

<span data-ttu-id="2f6bf-110">Du kan använda bokföringsperioder vid rapportering.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-110">You can use accounting periods in reporting.</span></span> <span data-ttu-id="2f6bf-111">Till exempel när du granskar bokförda transaktioner på sidan **Saldo/budget** där rapporteringsintervallet kan anges.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-111">For example, when you are reviewing posted entries on the **Balance/Budget** page where the reporting interval can be specified.</span></span> <span data-ttu-id="2f6bf-112">Ett av alternativen du kan ange för att rapportera efter bokföringsperiod.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-112">One of the options you may specify to report by accounting period.</span></span> <span data-ttu-id="2f6bf-113">Du kan också skapa en kontouppställning som jämför resultaten för olika perioder.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-113">You can also build an account schedule that compares results for different accounting periods.</span></span>

## <a name="creating-a-new-fiscal-year"></a><span data-ttu-id="2f6bf-114">Skapa ett nytt räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f6bf-114">Creating a new fiscal year</span></span>
<span data-ttu-id="2f6bf-115">Du kan skapa bokföringsperioder samtidigt, med hjälp av batch-jobbet **skapa räkenskapsår** eller manuellt.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-115">You can create accounting periods in bulk, by using eh **Create Fiscal Year** batch job, or manually.</span></span>

### <a name="how-to-create-accounting-periods-in-bulk"></a><span data-ttu-id="2f6bf-116">Så här skapar du flera redovisningsperioder samtidigt</span><span class="sxs-lookup"><span data-stu-id="2f6bf-116">How to create accounting periods in-bulk</span></span>
<span data-ttu-id="2f6bf-117">Använd batch-jobbet **skapa räkenskapsår** om du vill dela upp ett räkenskapsår i lika långa perioder.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-117">Use the **Create Fiscal Year** batch job to divide a fiscal year into periods of equal length.</span></span>  

1. <span data-ttu-id="2f6bf-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokföringsperioder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f6bf-119">Välj åtgärden **Skapa år**.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-119">Choose the **Create Year** action.</span></span>  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. <span data-ttu-id="2f6bf-120">I fältet **Startdatum** anger du det datum när räkenskapsåret börjar.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-120">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span>  
4. <span data-ttu-id="2f6bf-121">I fältet **Antal perioder** ange antalet bokföringsperioder som räkenskapsåret ska innehålla.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-121">In the **No. of Periods** field, enter the number of accounting periods to divide the fiscal year into.</span></span> <span data-ttu-id="2f6bf-122">Det kan finnas upp till 365 perioder per år.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-122">There can be up to 365 periods in a year.</span></span>  
5. <span data-ttu-id="2f6bf-123">I fältet **periodlängd** anger du en varaktighet för varje period.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-123">In the **Period Length** field, enter a duration for each period.</span></span> <span data-ttu-id="2f6bf-124">Exempelvis 1M för en månad, 1Q för ett kvartal och 1Y för ett år.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-124">For example, 1M for one month, 1Q for one quarter, and 1Y for one year.</span></span>  
6. <span data-ttu-id="2f6bf-125">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-125">Choose **OK**.</span></span>  

### <a name="how-to-create-accounting-periods-manually"></a><span data-ttu-id="2f6bf-126">Så här skapar du flera redovisningsperioder manuellt</span><span class="sxs-lookup"><span data-stu-id="2f6bf-126">How to create accounting periods manually</span></span>
<span data-ttu-id="2f6bf-127">Om redovisningsperioder för räkenskapsåret har olika varaktighet såsom 4-4-5-kalendern som används i detaljhandeln kan du manuellt ställa in den.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-127">If the accounting periods in your fiscal year have different durations, like the 4-4-5 calendar used in retail, you can manually set it up.</span></span>  
  
1. <span data-ttu-id="2f6bf-128">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokföringsperioder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f6bf-129">I fältet **Startdatum** anger du det datum när räkenskapsåret börjar.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-129">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span> <span data-ttu-id="2f6bf-130">Fältet **Namn** visar namnet på månaden.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-130">The **Name** field will show the name of the month.</span></span>  
3. <span data-ttu-id="2f6bf-131">Markera kryssrutan **Nytt räkenskapsår** för att indikera att detta är den första perioden under året.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-131">Choose the **New Fiscal Year** check box to indicate that this is the first period in the year.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2f6bf-132">kommer att använda denna period för att bestämma vilka perioder som avslutas vid årets slut.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-132">will use this period to determine which periods to close at year-end.</span></span>
4. <span data-ttu-id="2f6bf-133">Upprepa steg 2 och 3 för varje återstående period.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-133">Repeat steps 2 and 3 for each remaining period.</span></span>  

## <a name="closing-a-fiscal-year"></a><span data-ttu-id="2f6bf-134">Avsluta ett räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f6bf-134">Closing a Fiscal Year</span></span>
<span data-ttu-id="2f6bf-135">Avsluta räkenskapsåret är en av åtgärderna för att avsluta böckerna.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-135">Closing the fiscal year is one of the tasks for closing the books.</span></span> <span data-ttu-id="2f6bf-136">Efter att du avslutar ett räkenskapsår markeras kryssrutorna **Avslutat** och **Låst datum** för samtliga perioder i året.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-136">After you close a fiscal year, the **Closed** and **Date Locked** check boxes are selected for all periods in the year.</span></span> <span data-ttu-id="2f6bf-137">Du kan inte öppna ett år igen eller avmarkera kryssrutorna.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-137">You cannot reopen a year or clear the check boxes.</span></span>

> [!NOTE]  
>  <span data-ttu-id="2f6bf-138">Du måste alltid ha minst ett oavslutat räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-138">You must always have at least one open fiscal year.</span></span> <span data-ttu-id="2f6bf-139">När du avslutar ett år, försäkra dig om att ett nytt år har skapats.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-139">When closing a year, ensure that a new year has been created.</span></span> <span data-ttu-id="2f6bf-140">Notera även att efter att du avslutat ett år kan du inte ändra startdatumet för det följande året.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-140">Also, note that after you close one year, you cannot change the starting date of the following year.</span></span>

1. <span data-ttu-id="2f6bf-141">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokföringsperioder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f6bf-142">Välj åtgärden **Avsluta år**.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-142">Choose the **Close Year** action.</span></span>  

## <a name="posting-entries-to-a-closed-fiscal-year"></a><span data-ttu-id="2f6bf-143">Bokför transaktioner till ett avslutat räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-143">Posting Entries to a Closed Fiscal Year</span></span>
<span data-ttu-id="2f6bf-144">Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-144">Although a fiscal year is closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="2f6bf-145">När du gör det markeras transaktionerna som bokförda på ett avslutat räkenskapsår och kryssrutan **Föregående års transaktion** markeras.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-145">When you do, the entries are marked as posted to a closed fiscal year and the **Prior Year Entry** check box is selected.</span></span> <span data-ttu-id="2f6bf-146">Som standard visas inte kryssrutan på sidan, men du kan lägga till den.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-146">By default, the check box is not displayed on the page, but you can add it.</span></span> <span data-ttu-id="2f6bf-147">Nästa steg är att avsluta resultaträkningskontona och överföra årets resultat till ett konto i balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-147">The next steps are to close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="2f6bf-148">Upprepa dessa steg varje gång du bokför transaktioner i ett avslutat räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-148">Repeat these steps each time you post entries to a closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f6bf-149">Se även</span><span class="sxs-lookup"><span data-stu-id="2f6bf-149">See Also</span></span>
[<span data-ttu-id="2f6bf-150">Avsluta böckerna</span><span class="sxs-lookup"><span data-stu-id="2f6bf-150">Closing the Books</span></span>](year-close-books.md)  
[<span data-ttu-id="2f6bf-151">Avsluta år och perioder</span><span class="sxs-lookup"><span data-stu-id="2f6bf-151">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="2f6bf-152">Så här: Arbeta med kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="2f6bf-152">How to Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
  





