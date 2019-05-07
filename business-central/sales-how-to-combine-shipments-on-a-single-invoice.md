---
title: Så här kombinerar du leveranser på en enda faktura | Microsoft Docs
description: Om du vill fakturera mer än en leverans åt gången kan du använda funktionen för kombinerade leveranser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3d4aa37a90a700ffb634867c0c96299cec941e35
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926658"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b438d-103">Kombinera leveranser på en enda faktura</span><span class="sxs-lookup"><span data-stu-id="b438d-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="b438d-104">Om du vill fakturera mer än en leverans åt gången kan du använda funktionen för kombinerade leveranser.</span><span class="sxs-lookup"><span data-stu-id="b438d-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="b438d-105">Innan du kan skapa en kombinerad leverans måste mer än en leverans till samma kund och i samma valuta ha bokförts.</span><span class="sxs-lookup"><span data-stu-id="b438d-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="b438d-106">Med andra ord måste du ha fyllt i minst två försäljningsorder och bokfört dem som levererade, men inte fakturerade.</span><span class="sxs-lookup"><span data-stu-id="b438d-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="b438d-107">Om du vill kombinera utleveranser måste du markera kryssrutan **Samlingsfakturering** på snabbfliken **Leverans** på **Kund**-kortet.</span><span class="sxs-lookup"><span data-stu-id="b438d-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b438d-108">Så här kombinerar du utleveranser manuellt på en enda faktura</span><span class="sxs-lookup"><span data-stu-id="b438d-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="b438d-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b438d-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b438d-110">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b438d-110">Choose the **New** action.</span></span> <span data-ttu-id="b438d-111">Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="b438d-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="b438d-112">I fältet **Förs.kundnr.**</span><span class="sxs-lookup"><span data-stu-id="b438d-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="b438d-113">Ange den kund som ska få fakturan för de levererade artiklarna, i fältet.</span><span class="sxs-lookup"><span data-stu-id="b438d-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="b438d-114">På snabbfliken **Rader** klickar du på åtgärden **Hämta utleveransrader**.</span><span class="sxs-lookup"><span data-stu-id="b438d-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="b438d-115">Markera den leveransrad som ska inkluderas på fakturan:</span><span class="sxs-lookup"><span data-stu-id="b438d-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="b438d-116">Markera alla rader och klicka på **OK** om du vill infoga alla rader.</span><span class="sxs-lookup"><span data-stu-id="b438d-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="b438d-117">Markera raderna i fråga och klicka på **OK** om du vill infoga särskilda rader.</span><span class="sxs-lookup"><span data-stu-id="b438d-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="b438d-118">Du kan använda CTRL-tangenten om du vill markera flera rader som inte är i följd.</span><span class="sxs-lookup"><span data-stu-id="b438d-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="b438d-119">Om du har markerat fel leveransrad eller om du vill börja om kan du ta bort raderna på fakturan och köra funktionen **Hämta leveransrader** på nytt.</span><span class="sxs-lookup"><span data-stu-id="b438d-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="b438d-120">Om du vill bokföra fakturan väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="b438d-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b438d-121">Så här kombinerar du utleveranser automatiskt på en enda faktura</span><span class="sxs-lookup"><span data-stu-id="b438d-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="b438d-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Samlingsfakturering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b438d-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="b438d-123">Sidan för begäran om batch-jobb öppnas.</span><span class="sxs-lookup"><span data-stu-id="b438d-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="b438d-124">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b438d-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b438d-125">Markera kryssrutan **Bokför fakturor**.</span><span class="sxs-lookup"><span data-stu-id="b438d-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="b438d-126">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b438d-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b438d-127">Fakturorna måste bokföras manuellt om du inte har markerat kryssrutan **Bokför fakturor** för batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="b438d-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="b438d-128">Så här tar du bort öppna försäljningsorder efter kombinerad utleveransbokföring</span><span class="sxs-lookup"><span data-stu-id="b438d-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="b438d-129">När utleveranser kombineras på en faktura och bokförs, skapas en bokförd försäljningsfaktura för de fakturerade raderna.</span><span class="sxs-lookup"><span data-stu-id="b438d-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="b438d-130">Innehållet i fältet **Fakturerat antal** på den ursprungliga avropsordern eller försäljningsordern uppdateras utifrån det fakturerade antalet.</span><span class="sxs-lookup"><span data-stu-id="b438d-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="b438d-131">När du fakturerar leveranser på det här sättet finns de order som leveranserna bokfördes från kvar, även om de har levererats och fakturerats i sin helhet.</span><span class="sxs-lookup"><span data-stu-id="b438d-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="b438d-132">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort fakturerade försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b438d-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="b438d-133">Fälten **Serienr** .</span><span class="sxs-lookup"><span data-stu-id="b438d-133">Specify in the **No.**</span></span> <span data-ttu-id="b438d-134">vilka försäljningsorder som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b438d-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="b438d-135">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="b438d-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="b438d-136">Du kan också ta bort enskilda försäljningsorder manuellt.</span><span class="sxs-lookup"><span data-stu-id="b438d-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="b438d-137">Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel försäljningsavropsorder.</span><span class="sxs-lookup"><span data-stu-id="b438d-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="b438d-138">Se även</span><span class="sxs-lookup"><span data-stu-id="b438d-138">See Also</span></span>  
[<span data-ttu-id="b438d-139">Försäljning</span><span class="sxs-lookup"><span data-stu-id="b438d-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="b438d-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b438d-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
