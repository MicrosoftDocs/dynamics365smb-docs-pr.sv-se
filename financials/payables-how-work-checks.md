---
title: "Utfärda, Skriv ut, Avbryt och Makulera checkar | Microsoft Docs"
description: "Beskriver hur du utfärdar checkar med utbetalningsjournalen, skriver ut checkar och annullerar checkar eller granskar checktransaktioner i Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0875164a3afee7a835346a8d4b9323dda9ebf080
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-checks"></a><span data-ttu-id="e05a8-103">Så här arbetar du med checkar</span><span class="sxs-lookup"><span data-stu-id="e05a8-103">How to: Work With Checks</span></span>
<span data-ttu-id="e05a8-104">Du kan skicka elektroniska och manuella checkar i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e05a8-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e05a8-105">För båda metoder används utbetalningsjournalen för att utfärda checkar till leverantörer.</span><span class="sxs-lookup"><span data-stu-id="e05a8-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="e05a8-106">Du kan även makulera checkar och granska checktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e05a8-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="e05a8-107">I processen för att utfärda checkar får du förslag på betalningar, transaktioner skapas och datorcheckar skrivs ut.</span><span class="sxs-lookup"><span data-stu-id="e05a8-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e05a8-108">Om du vill vara säker på att banken bara godkänner validerade checkar och belopp kan du skicka en fil som innehåller information om leverantör, check ch betalning.</span><span class="sxs-lookup"><span data-stu-id="e05a8-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="e05a8-109">Mer information finns i [Så här exporterar du Positive Pay-fil](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="e05a8-109">For more information, see [How to: Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="e05a8-110">Skrivaren måste vara korrekt inställd med checkformulären, och du måste definiera vilken checklayout som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e05a8-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="e05a8-111">Mer information finns i [Så här definierar du checklayouter](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="e05a8-111">For more information, see [How to: Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="e05a8-112">Så här kan du utfärda checkar</span><span class="sxs-lookup"><span data-stu-id="e05a8-112">To issue checks</span></span>
1. <span data-ttu-id="e05a8-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e05a8-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e05a8-114">Fyll i journalen med relevanta utbetalningar, till exempel genom att använda funktionen Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="e05a8-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="e05a8-115">Mer information finns i [Så här föreslår du leverantörsbetalningar](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="e05a8-115">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="e05a8-116">I fältet **bankbetalningstyp** på journalrader för betalning, som du vill att göra med checkar väljer du ett av följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="e05a8-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="e05a8-117">**Datorcheck** Välj alternativet om du vill att programmet ska upprätta, och senare skriva ut, en check på beloppet på utbetalningsjournalens rad.</span><span class="sxs-lookup"><span data-stu-id="e05a8-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="e05a8-118">Du måste skriva ut checkarna, innan du kan bokföra journalraderna.</span><span class="sxs-lookup"><span data-stu-id="e05a8-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="e05a8-119">Du kan bara välja **Datorcheck** eller **Handskriven check** om **Motkontotyp** eller **Kontotyp** är Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="e05a8-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="e05a8-120">**Manuell check** Välj alternativet om du vill skriva en check för hand och vill att programmet ska upprätta en motsvarande checktransaktion för beloppet.</span><span class="sxs-lookup"><span data-stu-id="e05a8-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="e05a8-121">Med det här alternativen kan du inte skriva ut checkar från [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e05a8-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e05a8-122">Du kan bara välja **Manuell check** eller **Handskriven check** om **Motkontotyp** eller **Kontotyp** är Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="e05a8-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="e05a8-123">Du måste skriva ut datorcheckarna, innan du kan bokföra de relaterade journalraderna.</span><span class="sxs-lookup"><span data-stu-id="e05a8-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="e05a8-124">Vid datorcheckar väljer du **Skriv ut check**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="e05a8-125">I fönstret **Check** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e05a8-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="e05a8-126">Välj knappen **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e05a8-127">Om du vill skriva ut checkar i flera olika valutor från olika bankkonton måste du köra batch-jobbet **Skriv ut check** separat för varje valuta och ange bankkontot.</span><span class="sxs-lookup"><span data-stu-id="e05a8-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="e05a8-128">Att skriva ut checkar som inte har bokförts</span><span class="sxs-lookup"><span data-stu-id="e05a8-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="e05a8-129">Du kan makulera checkar som inte har bokförts när de har skrivits ut, genom att använda åtgärden **Makulera check** i fönstret **Betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="e05a8-130">I fönstret **Betalningsjournal** väljer du **Makulera check** och sedan väljer du checken som ska annulleras.</span><span class="sxs-lookup"><span data-stu-id="e05a8-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="e05a8-131">Så här makulerar du checkar:</span><span class="sxs-lookup"><span data-stu-id="e05a8-131">To void checks</span></span>
<span data-ttu-id="e05a8-132">När checkbetalning har bokförts, kan du bara ångra (makulera) checkar från de resulterande banktransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="e05a8-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="e05a8-133">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e05a8-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="e05a8-134">Välj det relevanta bankkontot och välj åtgärden **Redigerat** och välj sedan åtgärden **checktransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="e05a8-135">I fönstret **checktransaktioner** väljer du åtgärden **Makuler check**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="e05a8-136">Markera kryssrutan **Makulera endast check**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="e05a8-137">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="e05a8-138">Se även</span><span class="sxs-lookup"><span data-stu-id="e05a8-138">See Also</span></span>
[<span data-ttu-id="e05a8-139">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="e05a8-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="e05a8-140">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="e05a8-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="e05a8-141">Så här exporterar du en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="e05a8-141">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="e05a8-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e05a8-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

