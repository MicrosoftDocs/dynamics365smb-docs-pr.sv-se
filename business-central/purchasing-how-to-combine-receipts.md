---
title: Så här kombinerar du inleveranser | Microsoft Docs
description: Om du vill fakturera mer än en inleverans i taget kan du använda funktionen Kombinera inleveranser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/02/2020
ms.author: sgroespe
ms.openlocfilehash: f5b3c47ab430b89c2f747f73bc427e045a902992
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534677"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="4e450-103">Kombinera inleveranser på en enda faktura</span><span class="sxs-lookup"><span data-stu-id="4e450-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="4e450-104">Om du vill fakturera mer än en inleverans i taget kan du använda funktionen **Kombinera inleveranser**.</span><span class="sxs-lookup"><span data-stu-id="4e450-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="4e450-105">Innan du kan skapa en kombinerad inleverans måste du bokföra mer än en inköpsinleverans från samma leverantör i samma valuta.</span><span class="sxs-lookup"><span data-stu-id="4e450-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="4e450-106">Med andra ord måste du ha fyllt i två eller flera inköpsorder och bokfört dem som inlevererade (men inte fakturerade).</span><span class="sxs-lookup"><span data-stu-id="4e450-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="4e450-107">När inleveranser kombineras på en faktura och bokförs, skapas en bokförd inköpsfaktura för de fakturerade raderna.</span><span class="sxs-lookup"><span data-stu-id="4e450-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="4e450-108">Fältet **Fakturerat antal** på den ursprungliga inköpsordern eller inköpsavropsordern uppdateras utifrån det fakturerade antalet.</span><span class="sxs-lookup"><span data-stu-id="4e450-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="4e450-109">Emellertid tas det ursprungliga inköpsdokumentet inte bort, även om det är helt inlevererat och fakturerat, och därför måste du ta bort inköpsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="4e450-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="4e450-110">Det går inte att korrigera eller annullera den resulterande inköpsfakturan senare.</span><span class="sxs-lookup"><span data-stu-id="4e450-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="4e450-111">Om du vill ändra en inköpsfaktura som skapas på det här sättet måste du använda inköpskreditnotor.</span><span class="sxs-lookup"><span data-stu-id="4e450-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="4e450-112">Mer information finns i [Korrigera eller annullera obetalda inköpssfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="4e450-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="4e450-113">Så här kombinerar du inleveranser:</span><span class="sxs-lookup"><span data-stu-id="4e450-113">To combine receipts</span></span>

1. <span data-ttu-id="4e450-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="4e450-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4e450-115">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4e450-115">Choose the **New** action.</span></span> <span data-ttu-id="4e450-116">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="4e450-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="4e450-117">På snabbfliken **Rader** klickar du på åtgärden **Hämta inleveransrader**.</span><span class="sxs-lookup"><span data-stu-id="4e450-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="4e450-118">Välj flera inleveransrader som du vill inkludera på fakturan.</span><span class="sxs-lookup"><span data-stu-id="4e450-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="4e450-119">Om du har valt en ogiltig rad, eller du måste börja om från början, behöver du bara ta bort raderna från fakturan och köra funktionen **Hämta inleveransrader** på nytt.</span><span class="sxs-lookup"><span data-stu-id="4e450-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="4e450-120">Om du vill bokföra fakturan väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="4e450-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="4e450-121">Så här tar du bort öppna inköpsorder efter kombinerad inleveransbokföring</span><span class="sxs-lookup"><span data-stu-id="4e450-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="4e450-122">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ta bort fakturerade inköpsordrar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4e450-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="4e450-123">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="4e450-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="4e450-124">.</span><span class="sxs-lookup"><span data-stu-id="4e450-124">.</span></span>
3. <span data-ttu-id="4e450-125">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e450-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="4e450-126">Du kan också ta bort enskilda order manuellt.</span><span class="sxs-lookup"><span data-stu-id="4e450-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="4e450-127">Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel inköpsavropsorder.</span><span class="sxs-lookup"><span data-stu-id="4e450-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e450-128">Se även</span><span class="sxs-lookup"><span data-stu-id="4e450-128">See Also</span></span>

[<span data-ttu-id="4e450-129">Inköp</span><span class="sxs-lookup"><span data-stu-id="4e450-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4e450-130">Korrigera eller annullera obetalda inköpsfakturor</span><span class="sxs-lookup"><span data-stu-id="4e450-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="4e450-131">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e450-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
