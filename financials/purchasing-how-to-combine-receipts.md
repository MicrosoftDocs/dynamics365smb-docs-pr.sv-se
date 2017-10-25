---
title: "Så här kombinerar du inleveranser | Microsoft Docs"
description: "Om du vill fakturera mer än en inleverans i taget kan du använda funktionen Kombinera inleveranser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9b3599a3f1a2cfc53d682a153eda8395e892305b
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-receipts-on-a-single-invoice"></a><span data-ttu-id="a96ec-103">Så här kombinerar du inleveranser på en enda faktura</span><span class="sxs-lookup"><span data-stu-id="a96ec-103">How to: Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="a96ec-104">Om du vill fakturera mer än en inleverans i taget kan du använda funktionen **Kombinera inleveranser**.</span><span class="sxs-lookup"><span data-stu-id="a96ec-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="a96ec-105">Innan du kan skapa en kombinerad inleverans måste du bokföra mer än en inköpsinleverans från samma leverantör i samma valuta.</span><span class="sxs-lookup"><span data-stu-id="a96ec-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="a96ec-106">Med andra ord måste du ha fyllt i två eller flera inköpsorder och bokfört dem som inlevererade (men inte fakturerade).</span><span class="sxs-lookup"><span data-stu-id="a96ec-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="a96ec-107">När inleveranser kombineras på en faktura och bokförs, skapas en bokförd inköpsfaktura för de fakturerade raderna.</span><span class="sxs-lookup"><span data-stu-id="a96ec-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="a96ec-108">Fältet **Fakturerat antal** på den ursprungliga inköpsordern eller inköpsavropsordern uppdateras utifrån det fakturerade antalet.</span><span class="sxs-lookup"><span data-stu-id="a96ec-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="a96ec-109">Emellertid tas det ursprungliga inköpsdokumentet inte bort, även om det är helt inlevererat och fakturerat, och därför måste du ta bort inköpsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="a96ec-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="a96ec-110">Så här kombinerar du inleveranser:</span><span class="sxs-lookup"><span data-stu-id="a96ec-110">To combine receipts</span></span>  
1. <span data-ttu-id="a96ec-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a96ec-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a96ec-112">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a96ec-112">Choose the **New** action.</span></span> <span data-ttu-id="a96ec-113">Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a96ec-113">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="a96ec-114">På snabbfliken **Rader** klickar du på åtgärden **Hämta inleveransrader**.</span><span class="sxs-lookup"><span data-stu-id="a96ec-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="a96ec-115">Välj flera inleveransrader som du vill inkludera på fakturan.</span><span class="sxs-lookup"><span data-stu-id="a96ec-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="a96ec-116">Om du har valt en ogiltig rad, eller du måste börja om från början, behöver du bara ta bort raderna från fakturan och köra funktionen **Hämta inleveransrader** på nytt.</span><span class="sxs-lookup"><span data-stu-id="a96ec-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="a96ec-117">Om du vill bokföra fakturan väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="a96ec-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="a96ec-118">Så här tar du bort öppna inköpsorder efter kombinerad inleveransbokföring</span><span class="sxs-lookup"><span data-stu-id="a96ec-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="a96ec-119">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Ta bort fakturerade inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a96ec-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="a96ec-120">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="a96ec-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="a96ec-121">.</span><span class="sxs-lookup"><span data-stu-id="a96ec-121">.</span></span>
3. <span data-ttu-id="a96ec-122">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96ec-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="a96ec-123">Du kan också ta bort enskilda order manuellt.</span><span class="sxs-lookup"><span data-stu-id="a96ec-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="a96ec-124">Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel inköpsavropsorder.</span><span class="sxs-lookup"><span data-stu-id="a96ec-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="a96ec-125">Se även</span><span class="sxs-lookup"><span data-stu-id="a96ec-125">See Also</span></span>  
[<span data-ttu-id="a96ec-126">Inköp</span><span class="sxs-lookup"><span data-stu-id="a96ec-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a96ec-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a96ec-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
