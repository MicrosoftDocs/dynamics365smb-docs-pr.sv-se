---
title: Så här använder du fördelningsnycklar i redovisningsjournaler | Microsoft Docs
description: Lär dig hur du kan använda fördelningsnycklar i journaler.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 9c540b04b7dcda7cd3b656a86679228af08261c9
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310930"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="ea77f-103">Så här använder du fördelningsnycklar i redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="ea77f-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="ea77f-104">Du kan fördela en transaktion i en redovisningsjournal på flera olika konton när du bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="ea77f-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="ea77f-105">Fördelningen kan göras efter kvantitet, procentuellt eller med ett belopp.</span><span class="sxs-lookup"><span data-stu-id="ea77f-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="ea77f-106">Så här skapar du fördelningsnycklar</span><span class="sxs-lookup"><span data-stu-id="ea77f-106">To set up allocation keys</span></span>
1. <span data-ttu-id="ea77f-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Återkommande redov.journal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ea77f-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea77f-108">Välj fältet **Journalnamn** för att öppna sidan **redovisningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="ea77f-109">Du kan antingen ändra fördelningar på en befintlig journal i listan eller skapa en ny journal med fördelningar.</span><span class="sxs-lookup"><span data-stu-id="ea77f-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="ea77f-110">För att skapa en y journal väljer du åtgärden **Ny** och går vidare till nästa steg för att skapa en ny journal.</span><span class="sxs-lookup"><span data-stu-id="ea77f-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="ea77f-111">Välj journalen och gå till steg 7 för att ändra fördelningar av en befintlig journal.</span><span class="sxs-lookup"><span data-stu-id="ea77f-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="ea77f-112">I fältet **Namn** anger du ett namn för journalens som t.ex. RENSNING.</span><span class="sxs-lookup"><span data-stu-id="ea77f-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="ea77f-113">I fältet **beskrivning** anger du en beskrivning som t.ex. Rensning av utläggsjournal.</span><span class="sxs-lookup"><span data-stu-id="ea77f-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="ea77f-114">Stäng sidan när du är klar.</span><span class="sxs-lookup"><span data-stu-id="ea77f-114">When you are done, close the page.</span></span> <span data-ttu-id="ea77f-115">En ny, tom återkommande journal öppnas.</span><span class="sxs-lookup"><span data-stu-id="ea77f-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="ea77f-116">Fyll i fälten på raden.</span><span class="sxs-lookup"><span data-stu-id="ea77f-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="ea77f-117">Välj åtgärden **Fördelningar**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="ea77f-118">Lägg till en rad för varje fördelning.</span><span class="sxs-lookup"><span data-stu-id="ea77f-118">Add a line for each allocation.</span></span> <span data-ttu-id="ea77f-119">Du måste fylla i fältet **Fördelning %**, **Fördelningskvantitet** eller **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="ea77f-120">Du måste också fylla i fältet **Nr** och, om du fördelar transaktionen bland globala dimensioner, fälten för globala dimensioner.</span><span class="sxs-lookup"><span data-stu-id="ea77f-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="ea77f-121">Om du anger ett värde i procent på en rad beräknas beloppet i fältet **Belopp** automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ea77f-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="ea77f-122">Dessa belopp har motsatt tecken mot det totala beloppet i fältet **Belopp** i den återkommande journalen.</span><span class="sxs-lookup"><span data-stu-id="ea77f-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="ea77f-123">Välj **OK** för att återgå till sidan **Återkommande redov.journal** fönstret, när du har angett fördelningsraderna.</span><span class="sxs-lookup"><span data-stu-id="ea77f-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="ea77f-124">Fältet **Fördelat belopp (USD)** är ifyllt och matchar fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="ea77f-125">Bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="ea77f-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="ea77f-126">För att ändra en fördelningsnyckel som redan har angetts.</span><span class="sxs-lookup"><span data-stu-id="ea77f-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="ea77f-127">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Återkommande redov.journal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ea77f-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea77f-128">Välj journalen med fördelningen på sidan **Återkommande redov.journal**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="ea77f-129">Välj raden med fördelningen och välj sedan åtgärden **fördelningar**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="ea77f-130">Fyll i de relevanta fälten och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea77f-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea77f-131">Se även</span><span class="sxs-lookup"><span data-stu-id="ea77f-131">See Also</span></span>
[<span data-ttu-id="ea77f-132">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="ea77f-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="ea77f-133">Bokför dokument och journaler</span><span class="sxs-lookup"><span data-stu-id="ea77f-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="ea77f-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea77f-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
