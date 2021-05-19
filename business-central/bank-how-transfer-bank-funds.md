---
title: Överföra banktillgångar
description: Du kan överföra belopp från ett bankkonto, till exempel olika valutor genom att bokföra transaktionen i redovisningsjournalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985393"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="ccd60-103">Överföra banktillgångar</span><span class="sxs-lookup"><span data-stu-id="ccd60-103">Transfer Bank Funds</span></span>

<span data-ttu-id="ccd60-104">Du kan ibland komma att behöva överföra ett belopp från ett bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] till ett annat.</span><span class="sxs-lookup"><span data-stu-id="ccd60-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="ccd60-105">För att göra detta måste du bokföra en transaktion på sidan **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="ccd60-106">Uppgiften varierar beroende på om bankkontona använder samma valuta eller olika valutor.</span><span class="sxs-lookup"><span data-stu-id="ccd60-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="ccd60-107">Så här bokför du en överföring mellan bankkonton med samma valutakod</span><span class="sxs-lookup"><span data-stu-id="ccd60-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="ccd60-108">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ccd60-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ccd60-109">Fyll i fälten **Bokföringsdatum** och **Verifikationsnr** på en .</span><span class="sxs-lookup"><span data-stu-id="ccd60-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="ccd60-110">Ange **Bankkonto** i fältet **Kontotyp**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="ccd60-111">I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.</span><span class="sxs-lookup"><span data-stu-id="ccd60-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="ccd60-112">Ange det belopp som ska överföras i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="ccd60-113">Sedan måste du ange balanskontot.</span><span class="sxs-lookup"><span data-stu-id="ccd60-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="ccd60-114">Om du inte kan se de relevanta fälten kan du välja åtgärden **Visa fler kolumner** för att visa alla tillgängliga fält.</span><span class="sxs-lookup"><span data-stu-id="ccd60-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="ccd60-115">I fältet **Motkontotyp** väljer du **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="ccd60-116">I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna till.</span><span class="sxs-lookup"><span data-stu-id="ccd60-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="ccd60-117">Bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="ccd60-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="ccd60-118">Så här bokför du överföringar mellan bankkonton med olika valutakoder</span><span class="sxs-lookup"><span data-stu-id="ccd60-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="ccd60-119">För att överföra pengar mellan bankkonton som använder olika valutor måste du bokföra två redovisningsjournalrader.</span><span class="sxs-lookup"><span data-stu-id="ccd60-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="ccd60-120">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ccd60-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ccd60-121">Skapa två journalrader och fyll i fälten **Bokföringsdatum** och **Verifikationsnr**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="ccd60-122">På den första journalraden anger du **Bankkonto** i fältet **Typ**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="ccd60-123">I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.</span><span class="sxs-lookup"><span data-stu-id="ccd60-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="ccd60-124">I fältet **Belopp** anger du beloppet i samma valuta som bankontot, med eller utan minustecken.</span><span class="sxs-lookup"><span data-stu-id="ccd60-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="ccd60-125">Ett belopp utan ett tecken är ett debetbelopp och ett belopp med ett minustecken är ett kreditbelopp.</span><span class="sxs-lookup"><span data-stu-id="ccd60-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd60-126">Vissa företag föredrar att överföra mellan konton på separata journalrader.</span><span class="sxs-lookup"><span data-stu-id="ccd60-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="ccd60-127">Andra företag föredrar att bokföra allt på en journalrad med hjälp av ett balanskonto.</span><span class="sxs-lookup"><span data-stu-id="ccd60-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="ccd60-128">Hör med din lokala expert om du är osäker på vad du ska göra.</span><span class="sxs-lookup"><span data-stu-id="ccd60-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="ccd60-129">Om företaget föredrar att använda ett balanskonto, ställer du in fältet **Balanskontotyp** till **Bankkonto** och ställer in fältet **Balanskontonummer** på det bankkonto som du vill överföra pengarna till.</span><span class="sxs-lookup"><span data-stu-id="ccd60-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="ccd60-130">Gå sedan vidare till steg 9 eller 10.</span><span class="sxs-lookup"><span data-stu-id="ccd60-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="ccd60-131">Om företaget föredrar att använda en separat journalrad går du vidare till nästa steg.</span><span class="sxs-lookup"><span data-stu-id="ccd60-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="ccd60-132">På den andra journalraden anger du **Bankkonto** i fältet **Typ**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="ccd60-133">I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna till.</span><span class="sxs-lookup"><span data-stu-id="ccd60-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="ccd60-134">I fältet **Belopp** anger du beloppet i samma valuta som bankontot, med eller utan minustecken.</span><span class="sxs-lookup"><span data-stu-id="ccd60-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="ccd60-135">Ett belopp utan ett tecken är ett debetbelopp och ett belopp med ett minustecken är ett kreditbelopp.</span><span class="sxs-lookup"><span data-stu-id="ccd60-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="ccd60-136">Om de valutakurser som används i journalen inte är samma som valutakurserna på sidan **Valutakurser** skapar du en ny journalrad för valutakursvinsten eller valutakursförlusten.</span><span class="sxs-lookup"><span data-stu-id="ccd60-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="ccd60-137">Ange **Redovisningskonto** i fältet **Kontotyp**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="ccd60-138">Ange numret för redovisningskontot för valutavinster och valutaförluster i fältet **Kontonr**.</span><span class="sxs-lookup"><span data-stu-id="ccd60-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="ccd60-139">Ange valutakursvinst eller -förlust i fältet **Belopp** med eller utan ett minustecken.</span><span class="sxs-lookup"><span data-stu-id="ccd60-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="ccd60-140">Ett belopp utan ett tecken är ett debetbelopp och ett belopp med ett minustecken är ett kreditbelopp.</span><span class="sxs-lookup"><span data-stu-id="ccd60-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="ccd60-141">Bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="ccd60-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccd60-142">Se även</span><span class="sxs-lookup"><span data-stu-id="ccd60-142">See Also</span></span>

[<span data-ttu-id="ccd60-143">Jämka bankkonton</span><span class="sxs-lookup"><span data-stu-id="ccd60-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="ccd60-144">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="ccd60-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ccd60-145">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="ccd60-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="ccd60-146">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ccd60-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]