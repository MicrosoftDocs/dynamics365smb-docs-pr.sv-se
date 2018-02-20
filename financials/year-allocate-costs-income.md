---
title: "Översikt över arbetsuppgifter för att fördela kostnader och intäkter | Microsoft Docs"
description: "Beskriver uppgiften att fördela en transaktion i en redovisningsjournal på flera olika konton när du bokför journalen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f2a1f762f9380f3cd272e78c4c2f269e9960f38
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="allocate-costs-and-income"></a><span data-ttu-id="cead9-103">Fördela kostnader och intäkter</span><span class="sxs-lookup"><span data-stu-id="cead9-103">Allocate Costs and Income</span></span>
<span data-ttu-id="cead9-104">Du kan fördela en transaktion i en redovisningsjournal på flera olika konton när du bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="cead9-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="cead9-105">Fördelningen kan göras enligt tre olika metoder:</span><span class="sxs-lookup"><span data-stu-id="cead9-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="cead9-106">Antal</span><span class="sxs-lookup"><span data-stu-id="cead9-106">Quantity</span></span>
* <span data-ttu-id="cead9-107">Procent (%)</span><span class="sxs-lookup"><span data-stu-id="cead9-107">Percentage (%)</span></span>
* <span data-ttu-id="cead9-108">Belopp</span><span class="sxs-lookup"><span data-stu-id="cead9-108">Amount</span></span>

<span data-ttu-id="cead9-109">Fördelningsfunktionerna kan användas med återkommande redovisningsjournaler och i anläggningstillgångsjournaler.</span><span class="sxs-lookup"><span data-stu-id="cead9-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="cead9-110">I följande procedurer beskrivs hur du förbereder att fördela kostnader i en återkommande redovisningsjournal genom att definiera fördelningsnycklar.</span><span class="sxs-lookup"><span data-stu-id="cead9-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="cead9-111">När fördelningsnycklar definieras slutför du och bokför journalen som alla andra återkommande redovisningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="cead9-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="cead9-112">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="cead9-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="cead9-113">Så här skapar du fördelningsnycklar</span><span class="sxs-lookup"><span data-stu-id="cead9-113">To set up allocation keys</span></span>
<span data-ttu-id="cead9-114">Du kan fördela en transaktion i en återkommande redovisningsjournal på flera olika konton när du bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="cead9-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="cead9-115">Fördelningen kan göras efter kvantitet, procentuellt eller med ett belopp.</span><span class="sxs-lookup"><span data-stu-id="cead9-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="cead9-116">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Återkommande redov.journal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="cead9-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="cead9-117">Välj fältet **Journalnamn** för att öppna fönstret **redovisningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="cead9-117">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="cead9-118">Du kan antingen ändra fördelningar på en befintlig journal i listan eller skapa en ny journal med fördelningar.</span><span class="sxs-lookup"><span data-stu-id="cead9-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="cead9-119">För att skapa en y journal väljer du åtgärden **Ny** och går vidare till nästa steg för att skapa en ny journal.</span><span class="sxs-lookup"><span data-stu-id="cead9-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="cead9-120">Välj journalen och gå till steg 7 för att ändra fördelningar av en befintlig journal.</span><span class="sxs-lookup"><span data-stu-id="cead9-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="cead9-121">I fältet **Namn** anger du ett namn för journalens som t.ex. RENSNING.</span><span class="sxs-lookup"><span data-stu-id="cead9-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="cead9-122">I fältet **beskrivning** anger du en beskrivning som t.ex. Rensning av utläggsjournal.</span><span class="sxs-lookup"><span data-stu-id="cead9-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="cead9-123">Stäng fönstret när du är klar.</span><span class="sxs-lookup"><span data-stu-id="cead9-123">When you are done, close the window.</span></span> <span data-ttu-id="cead9-124">En ny, tom återkommande journal öppnas.</span><span class="sxs-lookup"><span data-stu-id="cead9-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="cead9-125">Fyll i fälten på raden.</span><span class="sxs-lookup"><span data-stu-id="cead9-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="cead9-126">Välj åtgärden **Fördelningar**.</span><span class="sxs-lookup"><span data-stu-id="cead9-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="cead9-127">Lägg till en rad för varje fördelning.</span><span class="sxs-lookup"><span data-stu-id="cead9-127">Add a line for each allocation.</span></span> <span data-ttu-id="cead9-128">Du måste fylla i fältet **Fördelning %**, **Fördelningskvantitet** eller **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="cead9-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="cead9-129">Du måste också fylla i fältet **Nr** och, om du fördelar transaktionen bland globala dimensioner, fälten för globala dimensioner.</span><span class="sxs-lookup"><span data-stu-id="cead9-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="cead9-130">Om du anger ett värde i procent på en rad beräknas beloppet i fältet **Belopp** automatiskt.</span><span class="sxs-lookup"><span data-stu-id="cead9-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="cead9-131">Dessa belopp har motsatt tecken mot det totala beloppet i fältet **Belopp** i den återkommande journalen.</span><span class="sxs-lookup"><span data-stu-id="cead9-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="cead9-132">Välj **OK** för att återgå till fönstret **Återkommande redov.journal** fönstret, när du har angett fördelningsraderna.</span><span class="sxs-lookup"><span data-stu-id="cead9-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="cead9-133">Fältet **Fördelat belopp (USD)** är ifyllt och matchar fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="cead9-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="cead9-134">Bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="cead9-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="cead9-135">För att ändra en fördelningsnyckel som redan har angetts.</span><span class="sxs-lookup"><span data-stu-id="cead9-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="cead9-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Återkommande redov.journal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="cead9-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="cead9-137">Välj journalen med fördelningen i fältet **Återkommande redov.journal**.</span><span class="sxs-lookup"><span data-stu-id="cead9-137">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="cead9-138">Välj raden med fördelningen och välj sedan åtgärden **fördelningar**.</span><span class="sxs-lookup"><span data-stu-id="cead9-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="cead9-139">Fyll i de relevanta fälten och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="cead9-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="cead9-140">Se även</span><span class="sxs-lookup"><span data-stu-id="cead9-140">See Also</span></span>
[<span data-ttu-id="cead9-141">Avsluta år och perioder</span><span class="sxs-lookup"><span data-stu-id="cead9-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="cead9-142">[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="cead9-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="cead9-143">[Bokför dokument och journaler](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="cead9-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="cead9-144">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cead9-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

