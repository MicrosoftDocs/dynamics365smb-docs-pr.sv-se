---
title: "Registrera och ersätta anställdas affärsrelaterad utgifter | Microsoft Docs"
description: "Bokför anställdas utgifter med redovisningsjournalen för den anställdas konto och bokför senare en betalning till den anställdes bankkonto för att ersätta för affärsrelaterade utgifter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 604b8ee545269707ebcabd3712aee0d4daf253a8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="c38ef-103">Skapa och återbetala de anställdas utgifter</span><span class="sxs-lookup"><span data-stu-id="c38ef-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="c38ef-104"> stöder transaktioner för medarbetare på samma sätt som för leverantörer.</span><span class="sxs-lookup"><span data-stu-id="c38ef-104"> supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="c38ef-105">Därför finns medarbetares bokföringsmallar för att vara säker på att medarbetares transaktioner bokförs i relevanta konton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="c38ef-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="c38ef-106">Medarbetartransaktioner kan bokföras i den lokala valutan.</span><span class="sxs-lookup"><span data-stu-id="c38ef-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="c38ef-107">Återbetalning till anställda stödjer inte kassarabatter och betalningstoleranser.</span><span class="sxs-lookup"><span data-stu-id="c38ef-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="c38ef-108">Om medarbetare lägger ut sina egna pengar under affärsaktiviteter, kan du bokföra kostnader för den anställde.</span><span class="sxs-lookup"><span data-stu-id="c38ef-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="c38ef-109">Du kan sedan ersätta den anställde genom att göra en betalning till den anställdes bankkonto på liknande sätt som när du betalar till leverantörer.</span><span class="sxs-lookup"><span data-stu-id="c38ef-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="c38ef-110">Om du vill registrera en anställd utgifter</span><span class="sxs-lookup"><span data-stu-id="c38ef-110">To record an employee's expense</span></span>
<span data-ttu-id="c38ef-111">Du bokför anställdas utgifter i fönstret **redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="c38ef-111">You post employees' expenses in the **General Journal** window.</span></span>
1. <span data-ttu-id="c38ef-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c38ef-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="c38ef-113">Öppna relevant buntnamn för redovisningsjournalen.</span><span class="sxs-lookup"><span data-stu-id="c38ef-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="c38ef-114">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="c38ef-115">Fyll i fälten på en ny journalrad efter behov.</span><span class="sxs-lookup"><span data-stu-id="c38ef-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="c38ef-116">Upprepa steg 3 för alla utgifter som anställde har.</span><span class="sxs-lookup"><span data-stu-id="c38ef-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="c38ef-117">Om du vill ange flera utgiftsrader ovanför en rad i motkontot, till exempel för den anställdes bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen i fönstret **redovisningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="c38ef-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="c38ef-118">Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera utgifterna.</span><span class="sxs-lookup"><span data-stu-id="c38ef-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="c38ef-119">Välj åtgärden **Bokför** för att registrera kostnader för den anställdes räkning.</span><span class="sxs-lookup"><span data-stu-id="c38ef-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="c38ef-120">Återbetala en medarbetare</span><span class="sxs-lookup"><span data-stu-id="c38ef-120">To reimburse an employee</span></span>
<span data-ttu-id="c38ef-121">Du återbetalar en medarbetare genom att bokföra betalningar till dennes bankkonto i fönstret **betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="c38ef-121">You reimburse employees by posting payments to their bank account in the **Payment Journal** window.</span></span>
1. <span data-ttu-id="c38ef-122">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c38ef-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="c38ef-123">Öppna relevant buntnamn för utbetalningsjournal.</span><span class="sxs-lookup"><span data-stu-id="c38ef-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="c38ef-124">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="c38ef-125">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="c38ef-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="c38ef-126">Mer information finns i [Gör betalningar](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="c38ef-127">Du kan också välja **föreslå betalning för medarbetare** för att automatiskt infoga journalrader för väntande medarbetare återbetalningar.</span><span class="sxs-lookup"><span data-stu-id="c38ef-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="c38ef-128">Om du vill registrera återbetalningen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="c38ef-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="c38ef-129">Så här synkroniserar du återbetalningar med transaktioner för medarbetare</span><span class="sxs-lookup"><span data-stu-id="c38ef-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="c38ef-130">Du kopplar betalningar för medarbetare till deras relaterade öppna transaktioner för medarbetare på samma sätt som du gör för leverantörsbetalningar, till exempel **Betalningsavstämningsjournal** baserat på de relaterade bankkontoutdragstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="c38ef-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example in the **Payment Reconciliation Journal** window, based on the related bank statement entries.</span></span> <span data-ttu-id="c38ef-131">Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="c38ef-132">Du kan också koppla manuellt i fönstret **Personaltransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="c38ef-132">Alternatively, you can apply manually in the **Employee Ledger Entries** window.</span></span> <span data-ttu-id="c38ef-133">Mer information finns i tillhörande [Stämma av leverantörsbetalningar manuellt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-133">For more information, see the related [Reconcile Vendor Payments Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="c38ef-134">Se även</span><span class="sxs-lookup"><span data-stu-id="c38ef-134">See Also</span></span>
[<span data-ttu-id="c38ef-135">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="c38ef-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="c38ef-136">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="c38ef-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="c38ef-137">Återföra bokningar</span><span class="sxs-lookup"><span data-stu-id="c38ef-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="c38ef-138">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="c38ef-138">Finance</span></span>](finance.md)  
<span data-ttu-id="c38ef-139">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c38ef-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
