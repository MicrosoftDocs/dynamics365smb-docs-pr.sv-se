---
title: Så här korrigerar du förskottsbetalningar | Microsoft Docs
description: Du kan korrigera en order efter att du har bokfört en förskottsfaktura för den. Du kan lägga till nya rader på en order efter att du har skickat ut en förskottsbetalning, och sedan kan du bokföra en ny förskottsfaktura. Du kan däremot inte ta bort en rad från en order efter en förskottsbetalning har fakturerats för raden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/03/2020
ms.author: sgroespe
ms.openlocfilehash: d87a36a4a3b812afdc355141d54e454069f2c53f
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534652"
---
# <a name="correct-prepayments"></a><span data-ttu-id="1c1bc-104">Korrigera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="1c1bc-104">Correct Prepayments</span></span>

<span data-ttu-id="1c1bc-105">Du kan korrigera en order efter att du har bokfört en förskottsfaktura för den.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="1c1bc-106">Du kan lägga till nya rader på en order efter att du har skickat ut en förskottsbetalning, och sedan kan du bokföra en ny förskottsfaktura. Du kan däremot inte ta bort en rad från en order efter en förskottsbetalning har fakturerats för raden.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="1c1bc-107">Om du har bokfört en förskottsfaktura för en försäljningsfaktura som du sedan korrigerar eller avbryter, måste du även korrigera eller avbryta förskottsbetalningen.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="1c1bc-108">Så här korrigerar du en förskottsbetalning</span><span class="sxs-lookup"><span data-stu-id="1c1bc-108">To correct a prepayment</span></span>

<span data-ttu-id="1c1bc-109">I följande procedur beskrivs hur du skapar en kreditnota för förskottsbetalning för att annullera alla fakturerade förskottsbetalningar för en order.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="1c1bc-110">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1c1bc-111">Öppna den aktuella försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="1c1bc-112">Välj åtgärden **Förskottsbetalning** och välj sedan åtgärden **Bokför kreditnota för förskottsbetalning** eller åtgärden **Bokför och skriv ut kreditnota för förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="1c1bc-113">På sidan **Försäljningskreditnota** fortsätter du att korrigera de aktuella transaktionerna för varje försäljningskreditnota.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="1c1bc-114">Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="1c1bc-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="1c1bc-115">Om du vill minska antalet i fältet **Radbelopp** måste du först öka procentandelen för förskottsbetalning på raden så att värdet i fältet **Radbelopp, förskottsbetalning** inte blir lägre än värdet i fältet **Fakturabelopp, förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="1c1bc-116">För att göra en förskottsfaktura för eventuella nya rader i försäljningsmeddelandet väljer du åtgärden **Förskottsbetalning** och väljer sedan åtgärden **Bokför förskottsfaktura** eller åtgärden **Bokför och skriv ut faktura på förskottsbet.**.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="1c1bc-117">Om du vill utfärda en ytterligare förskottsfaktura på minst en rad och bokför sedan förskottsfakturan.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="1c1bc-118">En ny faktura skapas för skillnaden mellan förskottsbetalningsbeloppen som fakturerats och de nya förskottsbetalningsbeloppen.</span><span class="sxs-lookup"><span data-stu-id="1c1bc-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1c1bc-119">Se även</span><span class="sxs-lookup"><span data-stu-id="1c1bc-119">See Also</span></span>

[<span data-ttu-id="1c1bc-120">Fakturera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="1c1bc-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="1c1bc-121">Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning</span><span class="sxs-lookup"><span data-stu-id="1c1bc-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="1c1bc-122">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="1c1bc-122">Finance</span></span>](finance.md)  
<span data-ttu-id="1c1bc-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c1bc-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
