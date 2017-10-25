---
title: "Så här skapar du förskottsfakturor | Microsoft Docs"
description: "Mer information om hur du hanterar situationer där du eller leverantören kräver förskottsbetalning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a><span data-ttu-id="3acc5-103">Så här skapar du förskottsfakturor</span><span class="sxs-lookup"><span data-stu-id="3acc5-103">How to: Create Prepayment Invoices</span></span>
<span data-ttu-id="3acc5-104">Om du vill att dina kunder ska betala innan du levererar en order till dem eller om en leverantör kräver att du betalar innan de levererar en order till dig, kan du använda funktionen för förskottsbetalning.</span><span class="sxs-lookup"><span data-stu-id="3acc5-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="3acc5-105">När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura.</span><span class="sxs-lookup"><span data-stu-id="3acc5-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="3acc5-106">Du kan använda standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs.</span><span class="sxs-lookup"><span data-stu-id="3acc5-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="3acc5-107">Till exempel, en totalsumma för hela ordern.</span><span class="sxs-lookup"><span data-stu-id="3acc5-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="3acc5-108">I följande procedur beskrivs hur du fakturerar en förskottsbetalning för en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="3acc5-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="3acc5-109">Momenten är liknande för en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="3acc5-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="3acc5-110">Så här skapar du en förskottsfaktura</span><span class="sxs-lookup"><span data-stu-id="3acc5-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="3acc5-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3acc5-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3acc5-112">Skapa en ny försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="3acc5-112">Create a new sales order.</span></span> <span data-ttu-id="3acc5-113">Mer information finns i [Så här säljer du produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="3acc5-113">For more information, see [How to: sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="3acc5-114">På snabbfliken **Förskottsbetalning** fylls fältet **Förskottsbetalning %** fylls i automatiskt om det finns en standardprocentandel för förskottsbetalning på kundkortet.</span><span class="sxs-lookup"><span data-stu-id="3acc5-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="3acc5-115">Du kan ändra innehållet i fältet.</span><span class="sxs-lookup"><span data-stu-id="3acc5-115">You can change the contents of the field.</span></span> <span data-ttu-id="3acc5-116">Procentandelen för förskottsbetalning kopieras bara från huvudet till de rader där standardprocentandelen inte kopieras från artikeln.</span><span class="sxs-lookup"><span data-stu-id="3acc5-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="3acc5-117">Om fältet **Komprimera förskottsbetalning** är markerat kombineras rader på fakturan om:</span><span class="sxs-lookup"><span data-stu-id="3acc5-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="3acc5-118">De har samma redovisningskonto för förskottsbetalningar, enligt de allmänna bokföringsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="3acc5-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="3acc5-119">De har samma dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3acc5-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="3acc5-120">Låt fältet vara tomt om du vill skapa en förskottsfaktura med en rad för varje försäljningsorderrad som det finns en procentandel för förskottsbetalning för.</span><span class="sxs-lookup"><span data-stu-id="3acc5-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="3acc5-121">Fyll i försäljningsraderna.</span><span class="sxs-lookup"><span data-stu-id="3acc5-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="3acc5-122">Om standardprocentandelar för förskottsbetalning har angetts för artiklarna kopieras de automatiskt till fältet **Förskottsbetalning %** på raden.</span><span class="sxs-lookup"><span data-stu-id="3acc5-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="3acc5-123">Annars kopieras den förskottsbetalda procentandelen från huvudet.</span><span class="sxs-lookup"><span data-stu-id="3acc5-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="3acc5-124">Du kan ändra innehållet i fältet **Förskottsbetalning %** på raden.</span><span class="sxs-lookup"><span data-stu-id="3acc5-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="3acc5-125">Om du vill koppla en procentandel för förskottsbetalning till hela ordern ändrar du fältet **Förskottsbetalning %** i huvudet när du har fyllt i raderna.</span><span class="sxs-lookup"><span data-stu-id="3acc5-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="3acc5-126">Visa det totala förskottsbeloppet genom att välja åtgärden **statistik**.</span><span class="sxs-lookup"><span data-stu-id="3acc5-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="3acc5-127">Om du vill justera det totala förskottsbetalningsbeloppet för ordern kan du ändra innehållet i fältet **Förskottsbetalningsbelopp** i fönstret **Förs.orderstatistik**.</span><span class="sxs-lookup"><span data-stu-id="3acc5-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field in the **Sales Order Statistics** window.</span></span>  

    <span data-ttu-id="3acc5-128">Om fältet **Priser inkl. moms** är markerat, kan fältet **Förskottsbetalningsbelopp inkl moms** redigeras</span><span class="sxs-lookup"><span data-stu-id="3acc5-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="3acc5-129">Om du ändrar innehållet i fältet **Förskottsbetalningsbelopp** fördelas beloppet proportionellt på alla rader, förutom på de rader där värdet **0** i fältet **Förskottsbetalning %**.</span><span class="sxs-lookup"><span data-stu-id="3acc5-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="3acc5-130">Du skriver ut en testrapport innan du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan välja åtgärden **Testrapport för förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="3acc5-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="3acc5-131">Du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan åtgärden **Bokför förskottsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="3acc5-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="3acc5-132">Om du vill bokföra och skriva ut förskottsfakturan väljer du åtgärden **Bokför och skriv ut faktura på förskottsbet.**.</span><span class="sxs-lookup"><span data-stu-id="3acc5-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="3acc5-133">Du kan skicka ut ytterligare förskottsfakturor för ordern.</span><span class="sxs-lookup"><span data-stu-id="3acc5-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="3acc5-134">Om du vill göra detta höjer du förskottsbetalningsbeloppet på minst en rad, justerar dokumentdatumet om det behövs och bokför sedan förskottsfakturan.</span><span class="sxs-lookup"><span data-stu-id="3acc5-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="3acc5-135">En ny faktura skapas för skillnaden mellan de förskottsbetalningsbelopp som hittills har fakturerats och det nya förskottsbetalningsbeloppet.</span><span class="sxs-lookup"><span data-stu-id="3acc5-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3acc5-136">Om du befinner dig i Nordamerika kan ändra du inte procentandelen för förskottsbetalning när förskottsfakturan har bokförts.</span><span class="sxs-lookup"><span data-stu-id="3acc5-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="3acc5-137">Detta förhindras i den amerikanska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] eftersom beräkning av moms på annat sätt blir felaktiga.</span><span class="sxs-lookup"><span data-stu-id="3acc5-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="3acc5-138">När du vill bokföra resten av fakturan bokför du den som en vanlig faktura. Förskottsbetalningsbeloppet dras automatiskt av från beloppet som ska betalas.</span><span class="sxs-lookup"><span data-stu-id="3acc5-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3acc5-139">Se även</span><span class="sxs-lookup"><span data-stu-id="3acc5-139">See Also</span></span>  
[<span data-ttu-id="3acc5-140">Fakturera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="3acc5-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="3acc5-141">Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning</span><span class="sxs-lookup"><span data-stu-id="3acc5-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="3acc5-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="3acc5-142">Finance</span></span>](finance.md)  
<span data-ttu-id="3acc5-143">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3acc5-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
