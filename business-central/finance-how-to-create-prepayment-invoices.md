---
title: Så här skapar du förskottsfakturor | Microsoft Docs
description: Mer information om hur du hanterar situationer där du eller leverantören kräver förskottsbetalning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a1f79f089ef8633ca51be35930c5de5c2401b29
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387405"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="9a5ca-103">Skapa förskottsfakturor</span><span class="sxs-lookup"><span data-stu-id="9a5ca-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="9a5ca-104">Om du kräver att dina kunder betalar innan du levererar en order till dem kan du använda funktionen för förskottsbetalning.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="9a5ca-105">Detsamma gäller om leverantören kräver att du betalar innan han/hon levererar en order till dig.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="9a5ca-106">När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="9a5ca-107">Om du har en standardprocentandel för förskottsbetalning för kunden eller leverantören tas den automatiskt med i den resulterande förskottsfakturan.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="9a5ca-108">Du kan också ange en procentandel för förskottsbetalning för hela dokumentet.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="9a5ca-109">När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="9a5ca-110">Du kan använda standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="9a5ca-111">Till exempel, en totalsumma för hela ordern.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="9a5ca-112">I följande procedur beskrivs hur du fakturerar en förskottsbetalning för en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="9a5ca-113">Momenten är liknande för en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="9a5ca-114">Så här skapar du en förskottsfaktura</span><span class="sxs-lookup"><span data-stu-id="9a5ca-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="9a5ca-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a5ca-116">Skapa en ny försäljningsorder för relevant kund.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="9a5ca-117">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="9a5ca-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="9a5ca-118">På snabbfliken **Förskottsbetalning** i fältet **Förskottsbetalning %** anges den procentandel som ska användas för att beräkna förskottsbeloppet.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="9a5ca-119">Om det finns en standardprocentandel på kundkortet fylls fältet i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="9a5ca-120">Du kan ändra procentandelen.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="9a5ca-121">Välj fältet **Komprimera förskottsbetalning** om du vill skapa rader på den förskottsfaktura som kombinerar rader från försäljningsordern om:</span><span class="sxs-lookup"><span data-stu-id="9a5ca-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="9a5ca-122">De har samma redovisningskonto för förskottsbetalningar, enligt de allmänna bokföringsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="9a5ca-123">De har samma dimensioner.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="9a5ca-124">Låt fältet vara tomt om du vill skapa en förskottsfaktura med en rad för varje försäljningsorderrad som det finns en procentandel för förskottsbetalning för, välj då inte fältet **Komprimera förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="9a5ca-125">Förfallodatumet för förskottsbetalningen beräknas automatiskt baserat på värdet i fältet **Betalningsvillkorskod för förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="9a5ca-126">Fyll i försäljningsraderna.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="9a5ca-127">Om du har angett en standard procentandel för förskottsbetalning för kunden eller på snabbfliken **förskottsbetalning** i det här dokumentet kopieras det här värdet till varje rad.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="9a5ca-128">Du kan ändra innehållet i fältet **Förskottsbetalning %** på raden.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="9a5ca-129">Visa det totala förskottsbeloppet genom att välja åtgärden **statistik**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="9a5ca-130">Om du vill justera det totala förskottsbetalningsbeloppet för ordern kan du ändra innehållet i fältet **Förskottsbetalningsbelopp** på sidan **Förs.orderstatistik**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="9a5ca-131">Om fältet **Priser inkl. moms** är markerat, kan fältet **Förskottsbetalningsbelopp inkl moms** redigeras</span><span class="sxs-lookup"><span data-stu-id="9a5ca-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="9a5ca-132">Om du ändrar innehållet i fältet **Förskottsbetalningsbelopp** fördelas beloppet proportionellt på alla rader, förutom på de rader där värdet **0** i fältet **Förskottsbetalning %**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="9a5ca-133">Du skriver ut en testrapport innan du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan välja åtgärden **Testrapport för förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="9a5ca-134">Du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan åtgärden **Bokför förskottsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="9a5ca-135">Om du vill bokföra och skriva ut förskottsfakturan väljer du åtgärden **Bokför och skriv ut faktura på förskottsbet.**.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="9a5ca-136">Du kan skicka ut ytterligare förskottsfakturor för ordern.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="9a5ca-137">Om du vill göra detta höjer du förskottsbetalningsbeloppet på minst en rad, justerar dokumentdatumet om det behövs och bokför sedan förskottsfakturan.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="9a5ca-138">En ny faktura skapas för skillnaden mellan de förskottsbetalningsbelopp som hittills har fakturerats och det nya förskottsbetalningsbeloppet.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="9a5ca-139">Om du befinner dig i Nordamerika kan ändra du inte procentandelen för förskottsbetalning när förskottsfakturan har bokförts.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="9a5ca-140">Detta förhindras i den amerikanska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] eftersom beräkning av moms på annat sätt blir felaktiga.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="9a5ca-141">När du vill bokföra resten av fakturan bokför du den som en vanlig faktura. Förskottsbetalningsbeloppet dras automatiskt av från beloppet som ska betalas.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a5ca-142">Se även</span><span class="sxs-lookup"><span data-stu-id="9a5ca-142">See Also</span></span>

[<span data-ttu-id="9a5ca-143">Fakturera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="9a5ca-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="9a5ca-144">Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning</span><span class="sxs-lookup"><span data-stu-id="9a5ca-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="9a5ca-145">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="9a5ca-145">Finance</span></span>](finance.md)  
<span data-ttu-id="9a5ca-146">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a5ca-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]