---
title: Korrigera eller annullera obetalda inköpsfakturor | Microsoft Docs
description: Förklarar hur du kan korrigera, avbryta eller ångra en bokförd inköpsfaktura eller skapa en inköpskreditnota automatiskt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3d0d1234a6459b153a436ed2dfe9a3a2f667ab89
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192753"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="470b8-103">Korrigera eller annullera obetalda inköpsfakturor</span><span class="sxs-lookup"><span data-stu-id="470b8-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="470b8-104">Du kan korrigera eller annullera en bokförd inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="470b8-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="470b8-105">Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen.</span><span class="sxs-lookup"><span data-stu-id="470b8-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="470b8-106">Om du redan har betalt för produkter på den bokförda inköpsfakturan kan du inte rätta eller annullera den från själva den bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="470b8-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="470b8-107">I stället måste du skapa en inköpskreditnota manuellt för att återföra inköpet, alternaivt hanterat med en inköpsreturorder.</span><span class="sxs-lookup"><span data-stu-id="470b8-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="470b8-108">Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="470b8-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="470b8-109">På sidan **Bokförd inköpsfaktura** kan du välja knappen **Korrigera** eller knappen **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="470b8-109">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="470b8-110">När du uppdaterar eller avbryter en bokförd inköpsfaktura gäller den korrigerande inköpskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga inköpsfakturan bokfördes.</span><span class="sxs-lookup"><span data-stu-id="470b8-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="470b8-111">Det återför den bokförda inköpsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av inköpskreditnota för din verifieringskedja.</span><span class="sxs-lookup"><span data-stu-id="470b8-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="470b8-112">I det följande beskrivs användningen av **Korrigera** och **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="470b8-112">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="470b8-113">Korrigera en bokförd inköpsfaktura</span><span class="sxs-lookup"><span data-stu-id="470b8-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="470b8-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="470b8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="470b8-115">Markera den bokförda inköpsfakturan som du vill korrigera.</span><span class="sxs-lookup"><span data-stu-id="470b8-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="470b8-116">Om kryssrutan **Avbruten** kan du inte rätta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.</span><span class="sxs-lookup"><span data-stu-id="470b8-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="470b8-117">På sidan **Bokförd inköpsfaktura** väljer du **korrigera**.</span><span class="sxs-lookup"><span data-stu-id="470b8-117">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="470b8-118">En ny inköpsfaktura med samma information skapas där du kan göra rättningen.</span><span class="sxs-lookup"><span data-stu-id="470b8-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="470b8-119">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="470b8-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="470b8-120">Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="470b8-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="470b8-121">En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="470b8-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="470b8-122">Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="470b8-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="470b8-123">Avbryta en bokförd inköpsfaktura</span><span class="sxs-lookup"><span data-stu-id="470b8-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="470b8-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="470b8-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="470b8-125">Markera den bokförda inköpsfakturan som du vill annullera.</span><span class="sxs-lookup"><span data-stu-id="470b8-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="470b8-126">Om kryssrutan **Avbruten** kan du inte avbryta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.</span><span class="sxs-lookup"><span data-stu-id="470b8-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="470b8-127">På sidan **Bokförd inköpsfaktura** väljer du **Annullera**.</span><span class="sxs-lookup"><span data-stu-id="470b8-127">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="470b8-128">En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="470b8-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="470b8-129">Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="470b8-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="470b8-130">Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="470b8-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="470b8-131">Delfakturabokföring stöds också</span><span class="sxs-lookup"><span data-stu-id="470b8-131">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="470b8-132">Om annulleringen är knuten till en delfakturabokföring uppdateras den ursprungliga inköpsorderraden så att den återspeglar det annullerade fakturerade antalet.</span><span class="sxs-lookup"><span data-stu-id="470b8-132">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="470b8-133">Fälten **Ant. att fakturera** och **Antal fakturerat** på den relaterade inköpsorderraden återställs till värdena före delbokföringen.</span><span class="sxs-lookup"><span data-stu-id="470b8-133">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="470b8-134">Se även</span><span class="sxs-lookup"><span data-stu-id="470b8-134">See Also</span></span>
[<span data-ttu-id="470b8-135">Inköp</span><span class="sxs-lookup"><span data-stu-id="470b8-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="470b8-136">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="470b8-136">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="470b8-137">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="470b8-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
