---
title: "Ångra en bokföring genom att bokföra en mottransaktion | Microsoft Docs"
description: "Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: cc624d52ce61cea4a8e92bb7d37e07ad8c769393
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="reverse-postings"></a><span data-ttu-id="fc203-103">Återföra bokningar</span><span class="sxs-lookup"><span data-stu-id="fc203-103">Reverse Postings</span></span>
<span data-ttu-id="fc203-104">För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt.</span><span class="sxs-lookup"><span data-stu-id="fc203-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="fc203-105">När du har återfört en post måste du skapa en korrekt post.</span><span class="sxs-lookup"><span data-stu-id="fc203-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="fc203-106">Du kan endast återföra poster som har bokförts från en redovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="fc203-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="fc203-107">En transaktion kan endast återföras en gång.</span><span class="sxs-lookup"><span data-stu-id="fc203-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="fc203-108">Läs mer om hur du bokför från en redovisningsjournal i [Bokför transaktioner direkt till redovisningsjournalen](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="fc203-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="fc203-109">Om du har bokfört fel negativt antal, till exempel om en inköpsorder med fel antal artiklar och bokfört den som inlevererad men inte fakturerad, kan du ångra bokföringen.</span><span class="sxs-lookup"><span data-stu-id="fc203-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="fc203-110">Om du har bokfört fel positivt antal, till exempel om en inköpsreturorder med fel antal artiklar och bokfört den som levererad men inte fakturerad, kan du ångra bokföringen.</span><span class="sxs-lookup"><span data-stu-id="fc203-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="fc203-111">Att återföra bokföringen av en redovisningstransaktion journal</span><span class="sxs-lookup"><span data-stu-id="fc203-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="fc203-112">Du kan återföra poster från alla sidor **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="fc203-112">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="fc203-113">Följande procedur baseras sidan **redovisningstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="fc203-113">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="fc203-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningstransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc203-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc203-115">Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="fc203-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="fc203-116">Observera att det måste komma från en journalbokföring.</span><span class="sxs-lookup"><span data-stu-id="fc203-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="fc203-117">På sidan **Återför transaktionsposter** väljer du önskad post och klickar på åtgärden **Återför**.</span><span class="sxs-lookup"><span data-stu-id="fc203-117">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="fc203-118">Välj knappen **Ja** på bekräftelsemeddelandet.</span><span class="sxs-lookup"><span data-stu-id="fc203-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="fc203-119">Så här ångrar du ett bokfört antal i en bokförd inköspleverans</span><span class="sxs-lookup"><span data-stu-id="fc203-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="fc203-120">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda inköpsinleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc203-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fc203-121">Öppna den bokförda inleveransen som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="fc203-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="fc203-122">Markera de rader som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="fc203-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="fc203-123">Välj åtgärden **Ångra inleverans**.</span><span class="sxs-lookup"><span data-stu-id="fc203-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="fc203-124">En rättningsrad infogas under den valda inleveransraden.</span><span class="sxs-lookup"><span data-stu-id="fc203-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="fc203-125">Om antalet har inlevererats i en lagerinleverans infogas en rättningsrad i den bokförda lagerinleveransen.</span><span class="sxs-lookup"><span data-stu-id="fc203-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="fc203-126">Fälten **Inlevererat antal** och **Inlevrd. antal ej faktrd.** på den relaterade inköpsordern är nollställda.</span><span class="sxs-lookup"><span data-stu-id="fc203-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="fc203-127">Så här ångrar du ett bokfört antal i bokförda returleveranser</span><span class="sxs-lookup"><span data-stu-id="fc203-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="fc203-128">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda returutleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc203-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fc203-129">Öppna den bokförda returutleveranser som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="fc203-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="fc203-130">Markera de rader som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="fc203-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="fc203-131">Välj åtgärden **Ångra returutleverans**.</span><span class="sxs-lookup"><span data-stu-id="fc203-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="fc203-132">En rättningsrad införs nu i det bokförda dokumentet och fälten **Returant. levererat** och **Retur levererat ej faktrd** på returordern ändras till noll.</span><span class="sxs-lookup"><span data-stu-id="fc203-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="fc203-133">Gå nu tillbaka till inköpsreturordern som är klar att bokföras.</span><span class="sxs-lookup"><span data-stu-id="fc203-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="fc203-134">Observera antalet i fältet **Returordernr** på sidan **Returordernr**.</span><span class="sxs-lookup"><span data-stu-id="fc203-134">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="fc203-135">.</span><span class="sxs-lookup"><span data-stu-id="fc203-135">field.</span></span>  
6.  <span data-ttu-id="fc203-136">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsreturorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc203-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="fc203-137">Öppna returordern i fråga och välj åtgärden **öppna igen**.</span><span class="sxs-lookup"><span data-stu-id="fc203-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="fc203-138">Korrigera värdet i fältet **Antal** och bokför inköpsreturordern igen.</span><span class="sxs-lookup"><span data-stu-id="fc203-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="fc203-139">Bokföra en negativ transaktion</span><span class="sxs-lookup"><span data-stu-id="fc203-139">To post a negative entry</span></span>  
<span data-ttu-id="fc203-140">Använd fältet **Korrigering** för att bokföra en negativ debet istället för en kredit, eller för att bokföra en negativ kredit istället för en debet för ett konto.</span><span class="sxs-lookup"><span data-stu-id="fc203-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="fc203-141">För att uppfylla juridiska krav visas detta fält som standard i alla journaler.</span><span class="sxs-lookup"><span data-stu-id="fc203-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="fc203-142">Fälten **Debetbelopp** och **Kreditbelopp** innehåller både ursprungstransaktionen och den korrigerade transaktionen.</span><span class="sxs-lookup"><span data-stu-id="fc203-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="fc203-143">Dessa fält påverkar inte kontosaldot.</span><span class="sxs-lookup"><span data-stu-id="fc203-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="fc203-144">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fc203-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="fc203-145">Välj önskat batch-namn i fältet **Batch-namn**.</span><span class="sxs-lookup"><span data-stu-id="fc203-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="fc203-146">Ange information i relevanta fält.</span><span class="sxs-lookup"><span data-stu-id="fc203-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="fc203-147">På journalraden som du vill aktivera för negativa poster väljer du kryssrutan **Korrigering**.</span><span class="sxs-lookup"><span data-stu-id="fc203-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="fc203-148">Välj åtgärden **Bokför** och välj sedan knappen **Ja** för att bokföra journalen.</span><span class="sxs-lookup"><span data-stu-id="fc203-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc203-149">Se även</span><span class="sxs-lookup"><span data-stu-id="fc203-149">See Also</span></span>
[<span data-ttu-id="fc203-150">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="fc203-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="fc203-151">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="fc203-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="fc203-152">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="fc203-152">Finance</span></span>](finance.md)  
<span data-ttu-id="fc203-153">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fc203-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

