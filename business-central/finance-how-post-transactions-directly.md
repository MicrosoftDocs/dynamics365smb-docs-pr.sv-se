---
title: "Registrera kostnader eller intäkter direkt i redovisningen | Microsoft Docs"
description: "Du kan skapa relaterade transaktioner genom att bokföra journalrader på sidan redovisningsjournal för verksamhet som inte representeras av ett dokument, till exempel mindre utgifter eller inbetalningar."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 11/27/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: a1e7137cdc08fb558b6a6d423ce9524fa47eec16
ms.contentlocale: sv-se
ms.lasthandoff: 11/29/2018

---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="4af97-103">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="4af97-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="4af97-104">Du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner direkt på redovisningskonton och andra konton, till exempel bank-, leverantörs- och personalkonton.</span><span class="sxs-lookup"><span data-stu-id="4af97-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="4af97-105">En vanlig användning av redovisningsjournalen är att publicera anställdas utgifter med egna pengar under affärsaktiviteter för senare återbetalning.</span><span class="sxs-lookup"><span data-stu-id="4af97-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="4af97-106">Mer information finns i [Så här registrerar du och återbetalar personalens utgifter](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="4af97-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="4af97-107">Redovisningsjournaler bokför ekonomiska transaktioner direkt till redovisningskonton och andra konton, till exempel bank-, leverantörs- och anställdas konton.</span><span class="sxs-lookup"><span data-stu-id="4af97-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="4af97-108">När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="4af97-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="4af97-109">Så sker till exempel även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="4af97-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="4af97-110">Du kan anpassa din version av en redovisningsjournal genom att ställ ain en journal eller mall.</span><span class="sxs-lookup"><span data-stu-id="4af97-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="4af97-111">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="4af97-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="4af97-112">Till skillnad från transaktioner som har bokförts med dokument som kräver en kreditnotaprocess, kan du korrekt återföra transaktioner som har bokförts med den allmänna journalen.</span><span class="sxs-lookup"><span data-stu-id="4af97-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="4af97-113">Mer information finns i [Återföra bokföringar](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="4af97-113">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="4af97-114">Bokföra transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="4af97-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="4af97-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4af97-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="4af97-116">Öppna relevant buntnamn för redovisningsjournalen.</span><span class="sxs-lookup"><span data-stu-id="4af97-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="4af97-117">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="4af97-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="4af97-118">Fyll i fälten på en ny journalrad efter behov.</span><span class="sxs-lookup"><span data-stu-id="4af97-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="4af97-119">Upprepa steg 3 för alla enskilda transaktioner som du vill tilldela bokföra.</span><span class="sxs-lookup"><span data-stu-id="4af97-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="4af97-120">Om du vill ange flera transaktionsrader ovanför en rad i motkontot, till exempel för ett bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen på sidan **redovisningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="4af97-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="4af97-121">Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="4af97-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="4af97-122">Välj åtgärden **Bokför** för att registrera transaktioner på de angivna redovisningskontona.</span><span class="sxs-lookup"><span data-stu-id="4af97-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="4af97-123">Se även</span><span class="sxs-lookup"><span data-stu-id="4af97-123">See Also</span></span>

[<span data-ttu-id="4af97-124">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="4af97-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="4af97-125">Skapa och återbetala de anställdas utgifter</span><span class="sxs-lookup"><span data-stu-id="4af97-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="4af97-126">Återföra bokningar</span><span class="sxs-lookup"><span data-stu-id="4af97-126">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="4af97-127">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="4af97-127">Finance</span></span>](finance.md)  
<span data-ttu-id="4af97-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4af97-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

