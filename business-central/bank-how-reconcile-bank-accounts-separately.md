---
title: "Stämma av bankkonton separat | Microsoft Docs"
description: "Beskriver hur ditt lagervärde stäms av med redovisningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b14f779a34f44bc8c41bb13b42ec06bea359c9b7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-bank-accounts-separately"></a><span data-ttu-id="5cc93-103">Stämma av bankkonton separat</span><span class="sxs-lookup"><span data-stu-id="5cc93-103">Reconcile Bank Accounts Separately</span></span>
<span data-ttu-id="5cc93-104">För att stämma av bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)] med utdrag från banken måste du först fylla i raderna i fönstret **Bankkontoavstämning**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-104">To reconcile bank accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)] with statements received from the bank, you must fill in the lines in the **Bank Acc. Reconciliation** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5cc93-105">Du kan också stämma av bankkonton i fönstret **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-105">You can also reconcile bank accounts in the **Payment Reconciliation Journal** window.</span></span> <span data-ttu-id="5cc93-106">Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer **Bokför betalningar och stäm av bankkonton**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-106">Any open bank account ledger entries related to the applied customer or vendor ledger entries will be closed when you choose the **Post Payments and Reconcile Bank Account** action.</span></span> <span data-ttu-id="5cc93-107">Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen.</span><span class="sxs-lookup"><span data-stu-id="5cc93-107">This means that the bank account is automatically reconciled for payments that you post with the journal.</span></span> <span data-ttu-id="5cc93-108">Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="5cc93-108">For more information, see [Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>

<span data-ttu-id="5cc93-109">Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera tjänsten Envestnet Yodlee bankfeed och sedan länka dina bankkonton till relaterade onlinebankkonton.</span><span class="sxs-lookup"><span data-stu-id="5cc93-109">To enable import of bank statements as bank feeds, you must first set up and enable the Envestnet Yodlee Bank Feed service, and then link your bank accounts to the related online bank accounts.</span></span> <span data-ttu-id="5cc93-110">Mer information finns i [Konfigurera du bankfeedtjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="5cc93-110">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

<span data-ttu-id="5cc93-111">Raderna i fönstret **Bankkontoavstämning** är uppdelade i två rutor.</span><span class="sxs-lookup"><span data-stu-id="5cc93-111">The lines in the **Bank Acc. Reconciliation** window are divided into two panes.</span></span> <span data-ttu-id="5cc93-112">Rutan **Bankkontoavstämning** visar antingen importerade banktransaktioner eller transaktioner med utestående utbetalningar.</span><span class="sxs-lookup"><span data-stu-id="5cc93-112">The **Bank Statement Lines** pane shows either imported bank transactions or ledger entries with outstanding payments.</span></span> <span data-ttu-id="5cc93-113">Rutan **Bankkontotransaktioner** visar transaktionerna på bankkontot.</span><span class="sxs-lookup"><span data-stu-id="5cc93-113">The **Bank Account Ledger Entries** pane shows the ledger entries in the bank account.</span></span>

<span data-ttu-id="5cc93-114">Aktiviteten att hitta och koppla transaktioner som ska stämmas av benämns som *matchning*.</span><span class="sxs-lookup"><span data-stu-id="5cc93-114">The activity of finding and applying entries to be reconciled is referred to as *matching*.</span></span> <span data-ttu-id="5cc93-115">Du kan välja att utföra matchning automatiskt genom att använda funktionen **Matcha automatiskt**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-115">You can choose to perform matching automatically by using the **Match Automatically** function.</span></span> <span data-ttu-id="5cc93-116">Alternativt kan manuellt välja rader i båda fönster för att koppla varje kontoutdragrad till en eller flera motsvarande bankkontotransaktioner och sedan använda **Matcha manuellt** funktionen.</span><span class="sxs-lookup"><span data-stu-id="5cc93-116">Alternatively, you can manually select lines in both panes to link each bank statement line to one or more related bank account ledger entries, and then use the **Match Manually** function.</span></span> <span data-ttu-id="5cc93-117">Kryssrutan **Kopplad** markeras på rader där transaktioner matchas.</span><span class="sxs-lookup"><span data-stu-id="5cc93-117">The **Applied** checkbox is selected on lines where entries match.</span></span>

<span data-ttu-id="5cc93-118">Du kan fylla i rutan **Kontoutdragrader** i fönstret **Bankkontoavstämning** på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="5cc93-118">You can fill in the **Bank Statement Lines** pane in the **Bank Acc. Reconciliation** window in the following ways:</span></span>

* <span data-ttu-id="5cc93-119">Automatiskt, genom att använda funktionen **Importera bankutdrag** för att fylla i raderna enligt faktiska bankkontotransaktioner som baseras på en fil som tillhandahålls i banken.</span><span class="sxs-lookup"><span data-stu-id="5cc93-119">Automatically, by using the **Import Bank Statement** function to fill in the lines according to actual bank statements based on a file provided by the bank.</span></span>
* <span data-ttu-id="5cc93-120">Manuellt genom att använda funktionen **Föreslå rader** för att fylla i raderna med transaktioner för fakturor som har utestående utbetalningar.</span><span class="sxs-lookup"><span data-stu-id="5cc93-120">Manually, by using the **Suggest Lines** function to fill in the lines with ledger entries for invoices that have outstanding payments.</span></span>

<span data-ttu-id="5cc93-121">När värdet i fältet **Totalt saldo** i rutan **Bankutdragsrader** är lika med värdet i fältet **Saldo att stämma av** i rutan **Bankkontotransaktioner** kan du välja åtgärden **Bokför** för att stämma av de kopplade bankkontotransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="5cc93-121">When the value in the **Total Balance** field in the **Bank Statement Lines** pane equals the value in the **Balance To Reconcile** field in the **Bank Account Ledger Entries** pane, you can choose the **Post** action to reconcile the applied bank account ledger entries.</span></span> <span data-ttu-id="5cc93-122">Alla icke godkända bankkontotransaktioner kommer att stå kvar i fönstret vilket innebär att betalningar som ska bearbetas för bankkonto inte återspeglas i det senaste bankkontoutdraget eller att några betalningar mottogs via checkar.</span><span class="sxs-lookup"><span data-stu-id="5cc93-122">Any non-applied bank account ledger entries will remain in the window, indicating that payments processed for the bank account are not reflected in the latest bank statement, or that some payments were received on checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5cc93-123">Om kontoutdragrader hör till checktransaktioner, kan du inte använda de matchningsfunktionerna.</span><span class="sxs-lookup"><span data-stu-id="5cc93-123">If bank statement lines relate to check ledger entries, then you cannot use the matching functions.</span></span> <span data-ttu-id="5cc93-124">I stället måste du välja åtgärden **Koppla trans.** och sedan välja den relevanta checktransaktionen att matcha kontoutdragraden med.</span><span class="sxs-lookup"><span data-stu-id="5cc93-124">Instead, you must choose the **Apply Entries** action, and then select the relevant check ledger entry to match the bank statement line with.</span></span>

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a><span data-ttu-id="5cc93-125">Så här fyller du i bankavstämningrader genom att importera ett kontoutdrag</span><span class="sxs-lookup"><span data-stu-id="5cc93-125">To fill bank reconciliation lines by importing a bank statement</span></span>
1. <span data-ttu-id="5cc93-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkontoavstämningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5cc93-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Account Reconciliation**, and then choose the related link.</span></span>
2. <span data-ttu-id="5cc93-127">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-127">Choose the **New** action.</span></span>
3. <span data-ttu-id="5cc93-128">Välj ett bankkonto i fältet **Bankkontonr**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-128">In the **Bank Account No.** field, select the relevant bank account.</span></span> <span data-ttu-id="5cc93-129">Bankkontotransaktionerna som finns på bankkonto, visas i rutan **Bankkontotransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-129">The bank account ledger entries that exist on the bank account appear in the **Bank Account Ledger Entries** pane.</span></span>
4. <span data-ttu-id="5cc93-130">Ange datumet på kontoutdraget från banken i fältet **Kontoutdragets datum**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-130">In the **Statement Date** field, enter the date of the statement from the bank.</span></span>
5. <span data-ttu-id="5cc93-131">Ange saldot på kontoutdraget från banken i fältet **Kontoutdragets slutsaldo**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-131">In the **Statement Ending Balance** field, enter the balance of the statement from the bank.</span></span>
6. <span data-ttu-id="5cc93-132">Om du har en bankutdragsfil väljer du åtgärden **Importera bankutdrag**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-132">If you have a bank statement file, choose the **Import Bank Statement** action.</span></span>
7. <span data-ttu-id="5cc93-133">Leta upp filen och välj sedan knappen **Öppna** för att importera banktransaktionerna till raderna i fönstret **Bankkontoavstämning**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-133">Locate the file, and then choose the **Open** button to import the bank transactions into the lines of the **Bank Acc. Reconciliation** window.</span></span>

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a><span data-ttu-id="5cc93-134">Så här fyller du i bankavstämningrader med funktionen Föreslå rader</span><span class="sxs-lookup"><span data-stu-id="5cc93-134">To fill bank reconciliation lines with the Suggest Lines function</span></span>
1. <span data-ttu-id="5cc93-135">I fönstret **Bankkontoavstämning** väljer du åtgärden **Föreslå rader**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-135">In the **Bank Acc. Reconciliation** window, choose the **Suggest Lines** action.</span></span>
2. <span data-ttu-id="5cc93-136">Ange det tidigaste bokföringsdatumet för transaktionsavstämningen i fältet **Startdatum**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-136">In the **Starting Date** field, enter the earliest posting date for the ledger entries to be reconciled.</span></span>
3. <span data-ttu-id="5cc93-137">Ange det senaste bokföringsdatumet för transaktionsavstämningen i fältet **Slutdatum**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-137">In the **Ending Date** field, enter the latest posting date for the ledger entries to be reconciled.</span></span>
4. <span data-ttu-id="5cc93-138">Om du vill att föreslå checktransaktion istället för bankkontotransaktioner markerar du kryssrutan **Ta med checkar**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-138">Select the **Include Checks** check box to any suggest check ledger entries instead of the corresponding bank account ledger entries.</span></span>
5. <span data-ttu-id="5cc93-139">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-139">Choose the **OK** button.</span></span>

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a><span data-ttu-id="5cc93-140">Så här matchar du automatiskt kontoutdragrader med bankkontotransaktioner</span><span class="sxs-lookup"><span data-stu-id="5cc93-140">To match bank statement lines with bank account ledger entries automatically</span></span>
1. <span data-ttu-id="5cc93-141">I fönstret **Bankkontoavstämning** väljer du åtgärden **Matcha automatiskt**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-141">In the **Bank Acc. Reconciliation** window, choose the **Match Automatically**.</span></span> <span data-ttu-id="5cc93-142">Fönstret **Matcha banktransaktioner** öppnas.</span><span class="sxs-lookup"><span data-stu-id="5cc93-142">**The Match Bank Entries** window opens.</span></span>
2. <span data-ttu-id="5cc93-143">Ange antalet dagar före och efter bankkontotransaktionbokföringsdatumet som funktionen ska söka i för att matcha bokföringsdatum i bankkontoutdraget i fältet **Bokföringsdatumtolerans (dagar)**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-143">In the **Transaction Date Tolerance (Days)** field, specify the span of days before and after the bank account ledger entry posting date within which the function will search for matching transaction dates in the bank statement.</span></span>

    <span data-ttu-id="5cc93-144">Om du anger 0 eller lämnar fältet tomt kommer funktionen **Matcha automatiskt** endast söka efter matchande bokföringsdatum på bankkontotransaktionbokföringsdatumet.</span><span class="sxs-lookup"><span data-stu-id="5cc93-144">If you enter 0 or leave the field blank, then the **Match Automatically** function will only search for matching transaction dates on the bank account ledger entry posting date.</span></span>
3. <span data-ttu-id="5cc93-145">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-145">Choose the **OK** button.</span></span>

    <span data-ttu-id="5cc93-146">Alla kontoutdragrader och bankkontotransaktioner som kan matchas ändrar till grönt teckensnitt och **Kopplat** kryssrutan markeras.</span><span class="sxs-lookup"><span data-stu-id="5cc93-146">All bank statement lines and bank account ledger entries that can be matched change to green font, and the **Applied** check box is selected.</span></span>
4. <span data-ttu-id="5cc93-147">Markera kontoutdragraden och välj sedan åtgärden **Ta bort matchning**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-147">To remove a match, select the bank statement line, and then choose the **Remove Match** action.</span></span>

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a><span data-ttu-id="5cc93-148">Så här matchar du manuellt bankutdragsrader med bankkontotransaktioner</span><span class="sxs-lookup"><span data-stu-id="5cc93-148">To match bank statement lines with bank account ledger entries manually</span></span>
1. <span data-ttu-id="5cc93-149">I fönstret **Bankkontoavstämning** markerar du en okopplad rad i rutan **Kontoutdragrader**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-149">In the **Bank Acc. Reconciliation** window, select a non-applied line in the **Bank Statement Lines** pane.</span></span>
2. <span data-ttu-id="5cc93-150">I rutan **Bankkontotransaktioner** markerar du en eller flera bankkontotransaktioner som kan matchas med den valda kontoutdragraden.</span><span class="sxs-lookup"><span data-stu-id="5cc93-150">In the **Bank Account Ledger Entries** pane, select one or more banks account ledger entries that can be matched with the selected bank statement line.</span></span> <span data-ttu-id="5cc93-151">Om du vill välja flera rader, tryck och håll ned CTRL-tangenten.</span><span class="sxs-lookup"><span data-stu-id="5cc93-151">To choose multiple lines, press and hold the Ctrl key.</span></span>
3. <span data-ttu-id="5cc93-152">Välj åtgärden **Matcha manuellt**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-152">Choose the **Match Manually** action.</span></span>

    <span data-ttu-id="5cc93-153">Den valda kontoutdragraden och de valda bankkontotransaktionerna ändrar till grönt teckensnitt och **Kopplat** kryssrutan i det högra fönstret markeras.</span><span class="sxs-lookup"><span data-stu-id="5cc93-153">The selected bank statement line and the selected bank account ledger entries change to green font, and the **Applied** check box in the right pane is selected.</span></span>
4. <span data-ttu-id="5cc93-154">Upprepa moment 1 till och med 3 för alla kontoutdragrader som inte matchas.</span><span class="sxs-lookup"><span data-stu-id="5cc93-154">Repeat steps 1 through 3 for all bank statement lines that are not matched.</span></span>
5. <span data-ttu-id="5cc93-155">Markera kontoutdragraden och välj sedan åtgärden **Ta bort matchning**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-155">To remove a match, select the bank statement line, and then choose the **Remove Match** action.</span></span>

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a><span data-ttu-id="5cc93-156">Så här skapar du saknade transaktioner för att matcha med banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="5cc93-156">To create missing ledger entries to match bank transactions with</span></span>
<span data-ttu-id="5cc93-157">Ibland kan det hända att ett kontoutdrag från banken innehåller belopp som motsvarar en avgift eller räntekostnad.</span><span class="sxs-lookup"><span data-stu-id="5cc93-157">Sometimes a bank statement contain amounts for interest or fees charged.</span></span> <span data-ttu-id="5cc93-158">Sådana banktransaktioner kan inte matchas, eftersom inga relaterade transaktioner finns i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5cc93-158">Such bank transactions cannot be matched because no related ledger entries exist in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5cc93-159">Du måste sedan bokföra en journalrad för varje transaktion för att skapa en artikelrelaterad transaktion som den kan matchas med.</span><span class="sxs-lookup"><span data-stu-id="5cc93-159">You must then post a journal line for each transaction to create a related ledger entry that it can be matched with.</span></span>

1. <span data-ttu-id="5cc93-160">I fönstret **Bankkontoavstämning** väljer du åtgärden **Överföring till redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-160">In the **Bank Acc. Reconciliation** window, choose the **Transfer to General Journal** action.</span></span>  
2. <span data-ttu-id="5cc93-161">I fönstret **Bankavst. trans. åt redov.jnl** anger du vilka redovisningsjournalen om du vill använda och klickar på knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-161">In the **Trans. Bank Rec. to Gen. Jnl.** window, specify which general journal to use, and then choose the **OK** button.</span></span>

    <span data-ttu-id="5cc93-162">Fönstret **Redovisningsjournal** öppnas med nya journalrader för alla bankrapportrader med saknade transaktioner.</span><span class="sxs-lookup"><span data-stu-id="5cc93-162">The **General Journal** window opens containing new journal lines for any banks statement lines with missing ledger entries.</span></span>
3. <span data-ttu-id="5cc93-163">Fyll i journalraden med information, till exempel motkonton.</span><span class="sxs-lookup"><span data-stu-id="5cc93-163">Complete the journal line with relevant information, such as the balancing account.</span></span> <span data-ttu-id="5cc93-164">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="5cc93-164">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>  
4. <span data-ttu-id="5cc93-165">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-165">Choose the **Post** action.</span></span>

    <span data-ttu-id="5cc93-166">När transaktionen har bokförts går du vidare och matchar bankkontotransaktionen med den.</span><span class="sxs-lookup"><span data-stu-id="5cc93-166">When the entry is posted, proceed to match the bank transaction with to it.</span></span>
5. <span data-ttu-id="5cc93-167">Uppdatera eller öppna fönstret **Bankkontoavstämning** igen.</span><span class="sxs-lookup"><span data-stu-id="5cc93-167">Refresh or reopen the **Bank Acc. Reconciliation** window.</span></span> <span data-ttu-id="5cc93-168">Den nya transaktionen ska visas i fönstret **Bankkontotransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="5cc93-168">The new ledger entry will appear in the **Bank Account Ledger Entries** pane.</span></span>
6. <span data-ttu-id="5cc93-169">Matcha kontoutdragraden till bankkontotransaktionen, antingen manuellt eller automatiskt.</span><span class="sxs-lookup"><span data-stu-id="5cc93-169">Match the bank statement line with the bank account ledger entry, either manually or automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cc93-170">Se även</span><span class="sxs-lookup"><span data-stu-id="5cc93-170">See Also</span></span>
[<span data-ttu-id="5cc93-171">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="5cc93-171">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="5cc93-172">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="5cc93-172">Setting Up Banking</span></span>](bank-setup-banking.md)  
<span data-ttu-id="5cc93-173">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5cc93-173">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
