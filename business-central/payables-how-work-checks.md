---
title: "Utfärda, Skriv ut, Avbryt och Makulera checkar | Microsoft Docs"
description: "Beskriver hur du utfärdar checkar med utbetalningsjournalen, skriver ut checkar och annullerar checkar eller granskar checktransaktioner i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0c1b37616b4aafc9535f2d3fbf60b915c490dd0b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-checks"></a><span data-ttu-id="5a5c2-103">Arbeta med checkar</span><span class="sxs-lookup"><span data-stu-id="5a5c2-103">Work With Checks</span></span>
<span data-ttu-id="5a5c2-104">Du kan skicka elektroniska och manuella checkar i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5a5c2-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5a5c2-105">För båda metoder används utbetalningsjournalen för att utfärda checkar till leverantörer.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="5a5c2-106">Du kan även makulera checkar och granska checktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="5a5c2-107">I processen för att utfärda checkar får du förslag på betalningar, transaktioner skapas och datorcheckar skrivs ut.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5a5c2-108">Om du vill vara säker på att banken bara godkänner validerade checkar och belopp kan du skicka en fil som innehåller information om leverantör, check ch betalning.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="5a5c2-109">Mer information finns i [Exportera en Positive Pay-fil](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="5a5c2-109">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="5a5c2-110">Skrivaren måste vara korrekt inställd med checkformulären, och du måste definiera vilken checklayout som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="5a5c2-111">Mer information finns i [Definiera checklayouter](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="5a5c2-111">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="5a5c2-112">Så här kan du utfärda checkar</span><span class="sxs-lookup"><span data-stu-id="5a5c2-112">To issue checks</span></span>
1. <span data-ttu-id="5a5c2-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="5a5c2-114">Fyll i journalen med relevanta utbetalningar, till exempel genom att använda funktionen Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="5a5c2-115">Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="5a5c2-115">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="5a5c2-116">I fältet **bankbetalningstyp** på journalrader för betalning, som du vill att göra med checkar väljer du ett av följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="5a5c2-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="5a5c2-117">**Datorcheck** Välj alternativet om du vill att programmet ska upprätta, och senare skriva ut, en check på beloppet på utbetalningsjournalens rad.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="5a5c2-118">Du måste skriva ut checkarna, innan du kan bokföra journalraderna.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="5a5c2-119">Du kan bara välja **Datorcheck** eller **Handskriven check** om **Motkontotyp** eller **Kontotyp** är Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="5a5c2-120">**Manuell check** Välj alternativet om du vill skriva en check för hand och vill att programmet ska upprätta en motsvarande checktransaktion för beloppet.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="5a5c2-121">Med det här alternativen kan du inte skriva ut checkar från [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5a5c2-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5a5c2-122">Du kan bara välja **Manuell check** eller **Handskriven check** om **Motkontotyp** eller **Kontotyp** är Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
     >   <span data-ttu-id="5a5c2-123">Du måste skriva ut datorcheckarna, innan du kan bokföra de relaterade journalraderna.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="5a5c2-124">Vid datorcheckar väljer du **Skriv ut check**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="5a5c2-125">I fönstret **Check** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="5a5c2-126">Välj knappen **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5a5c2-127">Om du vill skriva ut checkar i flera olika valutor från olika bankkonton måste du köra batch-jobbet **Skriv ut check** separat för varje valuta och ange bankkontot.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="5a5c2-128">Att skriva ut checkar som inte har bokförts</span><span class="sxs-lookup"><span data-stu-id="5a5c2-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="5a5c2-129">Du kan makulera checkar som inte har bokförts när de har skrivits ut, genom att använda åtgärden **Makulera check** i fönstret **Betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="5a5c2-130">I fönstret **Betalningsjournal** väljer du **Makulera check** och sedan väljer du checken som ska annulleras.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="5a5c2-131">Så här makulerar du checkar:</span><span class="sxs-lookup"><span data-stu-id="5a5c2-131">To void checks</span></span>
<span data-ttu-id="5a5c2-132">När checkbetalning har bokförts, kan du bara ångra (makulera) checkar från de resulterande banktransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="5a5c2-133">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="5a5c2-134">Välj det relevanta bankkontot och välj åtgärden **Redigerat** och välj sedan åtgärden **checktransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="5a5c2-135">I fönstret **checktransaktioner** väljer du åtgärden **Makuler check**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="5a5c2-136">Markera kryssrutan **Makulera endast check**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="5a5c2-137">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a5c2-138">Se även</span><span class="sxs-lookup"><span data-stu-id="5a5c2-138">See Also</span></span>
[<span data-ttu-id="5a5c2-139">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="5a5c2-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="5a5c2-140">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="5a5c2-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="5a5c2-141">Exportera en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="5a5c2-141">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="5a5c2-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a5c2-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

