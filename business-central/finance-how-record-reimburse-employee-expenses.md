---
title: Registrera och ersätta anställdas affärsrelaterad utgifter | Microsoft Docs
description: Bokför anställdas utgifter med redovisningsjournalen för den anställdas konto och bokför senare en betalning till den anställdes bankkonto för att ersätta för affärsrelaterade utgifter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: edef774738233890af240b20622cc40585d79116
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783828"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="6935e-103">Skapa och återbetala de anställdas utgifter</span><span class="sxs-lookup"><span data-stu-id="6935e-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="6935e-104">stöder transaktioner för medarbetare på samma sätt som för leverantörer.</span><span class="sxs-lookup"><span data-stu-id="6935e-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="6935e-105">Därför finns medarbetares bokföringsmallar för att vara säker på att medarbetares transaktioner bokförs i relevanta konton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="6935e-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="6935e-106">Medarbetartransaktioner kan bokföras i den lokala valutan.</span><span class="sxs-lookup"><span data-stu-id="6935e-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="6935e-107">Återbetalning till anställda stödjer inte kassarabatter och betalningstoleranser.</span><span class="sxs-lookup"><span data-stu-id="6935e-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="6935e-108">Om medarbetare lägger ut sina egna pengar under affärsaktiviteter, kan du bokföra kostnader för den anställde.</span><span class="sxs-lookup"><span data-stu-id="6935e-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="6935e-109">Du kan sedan ersätta den anställde genom att göra en betalning till den anställdes bankkonto på liknande sätt som när du betalar till leverantörer.</span><span class="sxs-lookup"><span data-stu-id="6935e-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="6935e-110">I den här artikeln beskrivs hur du registrerar kostnader i böckerna och hur du återbetalar den anställde.</span><span class="sxs-lookup"><span data-stu-id="6935e-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="6935e-111">Din organisation kan ha en portal eller app där anställda kan skicka sina utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="6935e-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="6935e-112">Om du vill registrera en anställd utgifter</span><span class="sxs-lookup"><span data-stu-id="6935e-112">To record an employee's expense</span></span>
<span data-ttu-id="6935e-113">Du bokför anställdas utgifter på sidan **redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="6935e-113">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="6935e-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="6935e-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="6935e-115">Öppna relevant buntnamn för redovisningsjournalen.</span><span class="sxs-lookup"><span data-stu-id="6935e-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="6935e-116">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6935e-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="6935e-117">Fyll i fälten på en ny journalrad efter behov.</span><span class="sxs-lookup"><span data-stu-id="6935e-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="6935e-118">Upprepa steg 3 för alla utgifter som anställde har.</span><span class="sxs-lookup"><span data-stu-id="6935e-118">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="6935e-119">Om du vill ange flera utgiftsrader ovanför en rad i motkontot, till exempel för den anställdes bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen på sidan **redovisningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="6935e-119">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="6935e-120">Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera utgifterna.</span><span class="sxs-lookup"><span data-stu-id="6935e-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="6935e-121">Välj åtgärden **Bokför** för att registrera kostnader för den anställdes räkning.</span><span class="sxs-lookup"><span data-stu-id="6935e-121">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="6935e-122">Återbetala en medarbetare</span><span class="sxs-lookup"><span data-stu-id="6935e-122">To reimburse an employee</span></span>
<span data-ttu-id="6935e-123">Du återbetalar en medarbetare genom att bokföra betalningar till dennes bankkonto på sidan **betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="6935e-123">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="6935e-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Utbetalningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6935e-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="6935e-125">Öppna relevant buntnamn för utbetalningsjournal.</span><span class="sxs-lookup"><span data-stu-id="6935e-125">Open the relevant payment journal batch.</span></span> <span data-ttu-id="6935e-126">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6935e-126">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="6935e-127">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="6935e-127">Fill in the fields as necessary.</span></span> <span data-ttu-id="6935e-128">Mer information finns i [Gör betalningar](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="6935e-128">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="6935e-129">Du kan också välja **föreslå betalning för medarbetare** för att automatiskt infoga journalrader för väntande medarbetare återbetalningar.</span><span class="sxs-lookup"><span data-stu-id="6935e-129">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="6935e-130">Om du vill registrera återbetalningen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="6935e-130">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="6935e-131">Så här synkroniserar du återbetalningar med transaktioner för medarbetare</span><span class="sxs-lookup"><span data-stu-id="6935e-131">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="6935e-132">Du kopplar betalningar för medarbetare till deras relaterade öppna transaktioner för medarbetare på samma sätt som du gör för leverantörsbetalningar, till exempel på sidan **Betalningsavstämningsjournal** baserat på de relaterade bankkontoutdragstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6935e-132">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="6935e-133">Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="6935e-133">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="6935e-134">Du kan också koppla manuellt på sidan **Personaltransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="6935e-134">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="6935e-135">Mer information finns i tillhörande [Stäm av leverantörsbetalningar med betalningsjournalen eller från bokförda leverantörsreskontratransaktioner](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="6935e-135">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="6935e-136">Se även</span><span class="sxs-lookup"><span data-stu-id="6935e-136">See Also</span></span>
[<span data-ttu-id="6935e-137">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="6935e-137">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="6935e-138">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="6935e-138">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="6935e-139">Återföra journalbokningar och ångra inleveranser/utleveranser</span><span class="sxs-lookup"><span data-stu-id="6935e-139">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="6935e-140">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="6935e-140">Finance</span></span>](finance.md)  
<span data-ttu-id="6935e-141">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6935e-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]