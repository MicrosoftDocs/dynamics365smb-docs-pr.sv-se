---
title: Ångra en bokföring genom att bokföra en mottransaktion | Microsoft Docs
description: Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 808459f9c77d797c58a5956a5641c97bc398734e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306232"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a><span data-ttu-id="d5549-103">Återföra journalbokningar och ångra inleveranser/utleveranser</span><span class="sxs-lookup"><span data-stu-id="d5549-103">Reverse Journal Postings and Undo Receipts/Shipments</span></span>
<span data-ttu-id="d5549-104">För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt.</span><span class="sxs-lookup"><span data-stu-id="d5549-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="d5549-105">När du har återfört en post måste du skapa en korrekt post.</span><span class="sxs-lookup"><span data-stu-id="d5549-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="d5549-106">Du kan endast återföra poster som har bokförts från en redovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="d5549-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="d5549-107">En transaktion kan endast återföras en gång.</span><span class="sxs-lookup"><span data-stu-id="d5549-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="d5549-108">Om du vill ångra en bokföring av inleverans eller utleverans innan de bokförs som fakturerade kan du använda funktionen **ångra** i det bokförda dokumentet.</span><span class="sxs-lookup"><span data-stu-id="d5549-108">To undo a receipt or shipment posting, before they are posted as invoiced, you can use the **Undo** function on the posted document.</span></span> <span data-ttu-id="d5549-109">Du kan ångra kvantiteter av typen **artikel**.</span><span class="sxs-lookup"><span data-stu-id="d5549-109">You can undo quantities of type **Item**.</span></span>

<span data-ttu-id="d5549-110">Om du har bokfört fel negativt antal, till exempel om en inköpsorder med fel antal artiklar och bokfört den som inlevererad men inte fakturerad, kan du ångra bokföringen.</span><span class="sxs-lookup"><span data-stu-id="d5549-110">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items, and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="d5549-111">Om du har bokfört fel positivt antal, till exempel en utleverans eller en inköpsreturorder med fel antal artiklar och bokfört den som levererad men inte fakturerad, kan du ångra bokföringen.</span><span class="sxs-lookup"><span data-stu-id="d5549-111">If you have made an incorrect positive quantity posting, such as a sales shipment or a purchase return shipment with the wrong number of items, and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="d5549-112">Att återföra bokföringen av en redovisningstransaktion journal</span><span class="sxs-lookup"><span data-stu-id="d5549-112">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="d5549-113">Du kan återföra poster från alla sidor **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d5549-113">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="d5549-114">Följande procedur baseras sidan **redovisningstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d5549-114">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="d5549-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningstransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5549-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5549-116">Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="d5549-116">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="d5549-117">Observera att det måste komma från en journalbokföring.</span><span class="sxs-lookup"><span data-stu-id="d5549-117">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="d5549-118">På sidan **Återför transaktionsposter** väljer du önskad post och klickar på åtgärden **Återför**.</span><span class="sxs-lookup"><span data-stu-id="d5549-118">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="d5549-119">Välj knappen **Ja** på bekräftelsemeddelandet.</span><span class="sxs-lookup"><span data-stu-id="d5549-119">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="d5549-120">Bokföra en negativ transaktion</span><span class="sxs-lookup"><span data-stu-id="d5549-120">To post a negative entry</span></span>  
<span data-ttu-id="d5549-121">Använd fältet **Korrigering** för att bokföra en negativ debet istället för en kredit, eller för att bokföra en negativ kredit istället för en debet för ett konto.</span><span class="sxs-lookup"><span data-stu-id="d5549-121">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="d5549-122">För att uppfylla juridiska krav visas detta fält som standard i alla journaler.</span><span class="sxs-lookup"><span data-stu-id="d5549-122">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="d5549-123">Fälten **Debetbelopp** och **Kreditbelopp** innehåller både ursprungstransaktionen och den korrigerade transaktionen.</span><span class="sxs-lookup"><span data-stu-id="d5549-123">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="d5549-124">Dessa fält påverkar inte kontosaldot.</span><span class="sxs-lookup"><span data-stu-id="d5549-124">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="d5549-125">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5549-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="d5549-126">Välj önskat batch-namn i fältet **Batch-namn**.</span><span class="sxs-lookup"><span data-stu-id="d5549-126">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="d5549-127">Ange information i relevanta fält.</span><span class="sxs-lookup"><span data-stu-id="d5549-127">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="d5549-128">På journalraden som du vill aktivera för negativa poster väljer du kryssrutan **Korrigering**.</span><span class="sxs-lookup"><span data-stu-id="d5549-128">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="d5549-129">Välj åtgärden **Bokför** och välj sedan knappen **Ja** för att bokföra journalen.</span><span class="sxs-lookup"><span data-stu-id="d5549-129">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="d5549-130">Så här ångrar du ett bokfört antal i en bokförd inköspleverans</span><span class="sxs-lookup"><span data-stu-id="d5549-130">To undo a quantity posting on a posted purchase receipt</span></span>  
<span data-ttu-id="d5549-131">Nedan beskrivs hur du återställer en bokförd inleverans.</span><span class="sxs-lookup"><span data-stu-id="d5549-131">The following described how to undo a posted receipt.</span></span> <span data-ttu-id="d5549-132">Momenten är liknande för bokförda utleveranser.</span><span class="sxs-lookup"><span data-stu-id="d5549-132">The steps are similar for posted shipments.</span></span>

1.  <span data-ttu-id="d5549-133">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda inköpsinleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5549-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d5549-134">Öppna den bokförda inleveransen som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="d5549-134">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="d5549-135">Markera de rader som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="d5549-135">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="d5549-136">Välj åtgärden **Ångra inleverans**.</span><span class="sxs-lookup"><span data-stu-id="d5549-136">Choose **Undo Receipt** action.</span></span>

<span data-ttu-id="d5549-137">En rättningsrad infogas under den valda inleveransraden.</span><span class="sxs-lookup"><span data-stu-id="d5549-137">A corrective line is inserted under the selected receipt line.</span></span> <span data-ttu-id="d5549-138">Om antalet har inlevererats i en lagerinleverans infogas en rättningsrad i den bokförda lagerinleveransen.</span><span class="sxs-lookup"><span data-stu-id="d5549-138">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

<span data-ttu-id="d5549-139">Fälten **Inlevererat antal** och **Inlevrd. antal ej faktrd.** på den relaterade inköpsordern är nollställda.</span><span class="sxs-lookup"><span data-stu-id="d5549-139">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="d5549-140">Så här ångrar du ett bokfört antal i bokförda returleveranser</span><span class="sxs-lookup"><span data-stu-id="d5549-140">To undo and then redo a quantity posting on a posted return shipment</span></span>
<span data-ttu-id="d5549-141">Nedan beskrivs hur du återställer en bokförd returutleverans och sedan bokför inköpsreturen med en ny kvantitet.</span><span class="sxs-lookup"><span data-stu-id="d5549-141">The following described how to undo a posted return shipment and then repost the purchase return with a new quantity.</span></span>

1.  <span data-ttu-id="d5549-142">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda returutleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5549-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d5549-143">Öppna den bokförda returutleveranser som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="d5549-143">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="d5549-144">Markera de rader som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="d5549-144">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="d5549-145">Välj åtgärden **Ångra returutleverans**.</span><span class="sxs-lookup"><span data-stu-id="d5549-145">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="d5549-146">En rättningsrad införs nu i det bokförda dokumentet och fälten **Returant. levererat** och **Retur levererat ej faktrd** på returordern ändras till noll.</span><span class="sxs-lookup"><span data-stu-id="d5549-146">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="d5549-147">Gå nu tillbaka till inköpsreturordern som är klar att bokföras.</span><span class="sxs-lookup"><span data-stu-id="d5549-147">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="d5549-148">Observera antalet i fältet **Returordernr** på sidan **Returordernr**.</span><span class="sxs-lookup"><span data-stu-id="d5549-148">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="d5549-149">.</span><span class="sxs-lookup"><span data-stu-id="d5549-149">field.</span></span>  
6.  <span data-ttu-id="d5549-150">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsreturorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5549-150">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="d5549-151">Öppna returordern i fråga och välj åtgärden **öppna igen**.</span><span class="sxs-lookup"><span data-stu-id="d5549-151">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="d5549-152">Korrigera värdet i fältet **Antal** och bokför inköpsreturordern igen.</span><span class="sxs-lookup"><span data-stu-id="d5549-152">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d5549-153">Se även</span><span class="sxs-lookup"><span data-stu-id="d5549-153">See Also</span></span>
[<span data-ttu-id="d5549-154">Ångra monteringsboking</span><span class="sxs-lookup"><span data-stu-id="d5549-154">Undo Assembly Posting</span></span>](assembly-how-to-undo-assembly-posting.md)  
[<span data-ttu-id="d5549-155">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="d5549-155">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="d5549-156">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="d5549-156">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="d5549-157">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="d5549-157">Finance</span></span>](finance.md)  
<span data-ttu-id="d5549-158">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5549-158">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
