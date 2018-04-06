---
title: "Överföra banktillgångar | Microsoft Docs"
description: "Du kan överföra belopp från ett bankkonto, till exempel olika valutor genom att bokföra transaktionen i redovisningsjournalen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 54e8a7bf7ca8761d6317b57d45e64f9ee628f4b8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="44bd7-103">Överföra banktillgångar</span><span class="sxs-lookup"><span data-stu-id="44bd7-103">Transfer Bank Funds</span></span>
<span data-ttu-id="44bd7-104">Ibland kan du behöva överföra ett belopp från ett bankkonto till ett annat.</span><span class="sxs-lookup"><span data-stu-id="44bd7-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="44bd7-105">För att göra detta måste du bokföra en transaktion i redovisningsjournalen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="44bd7-106">Uppgiften varierar beroende på om bankkontona använder samma valuta eller olika valutor.</span><span class="sxs-lookup"><span data-stu-id="44bd7-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="44bd7-107">Så här bokför du en överföring mellan bankkonton med samma valutakod</span><span class="sxs-lookup"><span data-stu-id="44bd7-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="44bd7-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="44bd7-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="44bd7-109">Fyll i fälten **Bokföringsdatum** och **Verifikationsnr** på en .</span><span class="sxs-lookup"><span data-stu-id="44bd7-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="44bd7-110">Ange **Bankkonto** i fältet **Kontotyp**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="44bd7-111">I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.</span><span class="sxs-lookup"><span data-stu-id="44bd7-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="44bd7-112">Ange det belopp som ska överföras i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="44bd7-113">I fältet **Motkontotyp** väljer du **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="44bd7-114">I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna till.</span><span class="sxs-lookup"><span data-stu-id="44bd7-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="44bd7-115">Bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="44bd7-116">Så här bokför du överföringar mellan bankkonton med olika valutakoder</span><span class="sxs-lookup"><span data-stu-id="44bd7-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="44bd7-117">För att överföra pengar mellan bankkonton som använder olika valutor måste du bokföra två redovisningsjournalrader.</span><span class="sxs-lookup"><span data-stu-id="44bd7-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="44bd7-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="44bd7-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="44bd7-119">Skapa två journalrader och fyll i fälten **Bokföringsdatum** och **Verifikationsnr**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="44bd7-120">På den första journalraden anger du **Bankkonto** i fältet **Typ**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="44bd7-121">I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.</span><span class="sxs-lookup"><span data-stu-id="44bd7-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="44bd7-122">I fältet **Belopp** anger du beloppet i samma valuta som bankontot.</span><span class="sxs-lookup"><span data-stu-id="44bd7-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="44bd7-123">Ange kreditbelopp med ett minustecken.</span><span class="sxs-lookup"><span data-stu-id="44bd7-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="44bd7-124">Ange debetbelopp utan ett minustecken.</span><span class="sxs-lookup"><span data-stu-id="44bd7-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="44bd7-125">I fältet **Motkontotyp** väljer du **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="44bd7-126">I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna till.</span><span class="sxs-lookup"><span data-stu-id="44bd7-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="44bd7-127">På den andra journalraden anger du **Bankkonto** i fältet **Typ**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="44bd7-128">I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna till.</span><span class="sxs-lookup"><span data-stu-id="44bd7-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="44bd7-129">I fältet **Belopp** anger du beloppet i samma valuta som bankontot.</span><span class="sxs-lookup"><span data-stu-id="44bd7-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="44bd7-130">Ange kreditbelopp med ett minustecken.</span><span class="sxs-lookup"><span data-stu-id="44bd7-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="44bd7-131">Ange debetbelopp utan ett minustecken.</span><span class="sxs-lookup"><span data-stu-id="44bd7-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="44bd7-132">I fältet **Motkontotyp** väljer du **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="44bd7-133">I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna från.</span><span class="sxs-lookup"><span data-stu-id="44bd7-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="44bd7-134">Om de valutakurser som används i journalen inte är samma som valutakurserna i fönstret **Valutakurser** skapar du en tredje rad för valutavinsten eller valutaförlusten.</span><span class="sxs-lookup"><span data-stu-id="44bd7-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="44bd7-135">Ange **Redovisningskonto** i fältet **Kontotyp**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="44bd7-136">Ange numret för redovisningskontot för valutavinster och valutaförluster i fältet **Kontonr**.</span><span class="sxs-lookup"><span data-stu-id="44bd7-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="44bd7-137">Ange valutavinsten eller valutaförlusten i fältet **Belopp** med eller utan ett minustecken för respektive kredit och debet.</span><span class="sxs-lookup"><span data-stu-id="44bd7-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="44bd7-138">Bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="44bd7-139">Se även</span><span class="sxs-lookup"><span data-stu-id="44bd7-139">See Also</span></span>
[<span data-ttu-id="44bd7-140">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="44bd7-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="44bd7-141">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="44bd7-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="44bd7-142">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="44bd7-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="44bd7-143">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44bd7-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

