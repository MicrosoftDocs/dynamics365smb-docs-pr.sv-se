---
title: "Ångra en bokföring genom att bokföra en mottransaktion | Microsoft Docs"
description: "Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 802171d4f421270cb7e9b4f9dfedec9b9fe5ddc6
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-postings"></a><span data-ttu-id="a6ae3-103">Så här: Återföra en bokning</span><span class="sxs-lookup"><span data-stu-id="a6ae3-103">How to: Reverse Postings</span></span>
<span data-ttu-id="a6ae3-104">För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="a6ae3-105">När du har återfört en post måste du skapa en korrekt post.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="a6ae3-106">Du kan endast återföra poster som har bokförts från en redovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="a6ae3-107">En transaktion kan endast återföras en gång.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="a6ae3-108">Läs mer om hur du bokför från en redovisningsjournal, [så här: bokföra transaktioner direkt till redovisningsmodulen ](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="a6ae3-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="a6ae3-109">Om du har bokfört fel negativt antal, till exempel om en inköpsorder med fel antal artiklar och bokfört den som inlevererad men inte fakturerad, kan du ångra bokföringen.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="a6ae3-110">Om du har bokfört fel positivt antal, till exempel om en inköpsreturorder med fel antal artiklar och bokfört den som levererad men inte fakturerad, kan du ångra bokföringen.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="a6ae3-111">Att återföra bokföringen av en redovisningstransaktion journal</span><span class="sxs-lookup"><span data-stu-id="a6ae3-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="a6ae3-112">Du kan återföra poster från alla fönster **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-112">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="a6ae3-113">Följande procedur baseras fönstret **redovisningstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-113">The following procedure is based on the **General Ledger Entries** window.</span></span>
1. <span data-ttu-id="a6ae3-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningstransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="a6ae3-115">Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="a6ae3-116">Observera att det måste komma från en journalbokföring.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="a6ae3-117">I fönstret **Återför transaktionsposter** väljer du önskad post och klickar på åtgärden **Återför**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-117">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="a6ae3-118">Välj knappen **Ja** på bekräftelsemeddelandet.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="a6ae3-119">Så här ångrar du ett bokfört antal i en bokförd inköspleverans</span><span class="sxs-lookup"><span data-stu-id="a6ae3-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="a6ae3-120">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bokförda inköpsinleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6ae3-121">Öppna den bokförda inleveransen som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="a6ae3-122">Markera de rader som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="a6ae3-123">Välj åtgärden **Ångra inleverans**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="a6ae3-124">En rättningsrad infogas under den valda inleveransraden.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="a6ae3-125">Om antalet har inlevererats i en lagerinleverans infogas en rättningsrad i den bokförda lagerinleveransen.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="a6ae3-126">Fälten **Inlevererat antal** och **Inlevrd. antal ej faktrd.** på den relaterade inköpsordern är nollställda.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="a6ae3-127">Så här ångrar du ett bokfört antal i bokförda returleveranser</span><span class="sxs-lookup"><span data-stu-id="a6ae3-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="a6ae3-128">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bokförda returutleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6ae3-129">Öppna den bokförda returutleveranser som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="a6ae3-130">Markera de rader som du vill ångra.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="a6ae3-131">Välj åtgärden **Ångra returutleverans**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="a6ae3-132">En rättningsrad införs nu i det bokförda dokumentet och fälten **Returant. levererat** och **Retur levererat ej faktrd** på returordern ändras till noll.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="a6ae3-133">Gå nu tillbaka till inköpsreturordern som är klar att bokföras.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="a6ae3-134">Observera antalet i fältet **Returordernr** i fönstret **Returordernr**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-134">In the **Posted Return Shipment** window, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="a6ae3-135">.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-135">field.</span></span>  
6.  <span data-ttu-id="a6ae3-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsreturorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="a6ae3-137">Öppna returordern i fråga och välj åtgärden **öppna igen**.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="a6ae3-138">Korrigera värdet i fältet **Antal** och bokför inköpsreturordern igen.</span><span class="sxs-lookup"><span data-stu-id="a6ae3-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a6ae3-139">Se även</span><span class="sxs-lookup"><span data-stu-id="a6ae3-139">See Also</span></span>
[<span data-ttu-id="a6ae3-140">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="a6ae3-140">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="a6ae3-141">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="a6ae3-141">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="a6ae3-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="a6ae3-142">Finance</span></span>](finance.md)  
<span data-ttu-id="a6ae3-143">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a6ae3-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

