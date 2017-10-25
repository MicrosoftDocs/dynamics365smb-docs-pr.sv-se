---
title: "Ställa in förskottsbetalningar | Microsoft Docs"
description: "Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen. Du kan till exempel kräva en deposition innan du tillverkar artiklar mot order eller också kan du kräva betalning innan du levererar artiklar till en kund. Med hjälp av funktionen för förskottsbetalning kan du fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer. På så sätt kan du se till att alla betalningar bokförs mot en faktura."
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
ms.openlocfilehash: 11aef4cb4b1d40568b63662239a26993782201a3
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-prepayments"></a><span data-ttu-id="5612c-106">Så här: Konfigurera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="5612c-106">How to: Set Up Prepayments</span></span>
<span data-ttu-id="5612c-107">Om du vill att din kund ska betala innan ni levererar till dem eller om er leverentör kräver att ni betalar innan dem levererar till er kan du använda Förskottsbetalningsfunktionen</span><span class="sxs-lookup"><span data-stu-id="5612c-107">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the Prepayment functionality.</span></span> <span data-ttu-id="5612c-108">Funktionen låter dig fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer och för att säkerställa att alla delbetalningar bokförs mot en faktura.</span><span class="sxs-lookup"><span data-stu-id="5612c-108">The functionality enables you to invoice and collect deposits required from customers or to remit deposits to vendors, and to ensure that all partial payments are posted against an invoice.</span></span> <span data-ttu-id="5612c-109">För mer information, se [Så här: skapa försäljningsfakturor](finance-how-to-create-prepayment-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="5612c-109">For more information, see [How to: Create Prepayment Invoices](finance-how-to-create-prepayment-invoices.md).</span></span>

<span data-ttu-id="5612c-110">Innan du kan bokföra förskottsfakturor måste du skapa bokföringskonton i redovisningen och ange nummerserier för förskottsbetalningsdokument.</span><span class="sxs-lookup"><span data-stu-id="5612c-110">Before you can post prepayment invoices, you have to set up the posting accounts in the general ledger, and you have to set up number series for prepayment documents.</span></span>  

<span data-ttu-id="5612c-111">Du kan ange procentandelen av radbeloppet som ska faktureras som förskottsbetalning, för en kund eller leverantör, för alla artiklar eller valda artiklar.</span><span class="sxs-lookup"><span data-stu-id="5612c-111">You can define the percentage of the line amount that will be invoiced for prepayment, for a customer or vendor, for all items or selected items.</span></span> <span data-ttu-id="5612c-112">När du har gjort de nödvändiga inställningarna kan du skapa förskottsfakturor från försäljnings- och inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="5612c-112">After you complete the setup, you can generate prepayment invoices from sales and purchase orders.</span></span> <span data-ttu-id="5612c-113">Du kan använda standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs.</span><span class="sxs-lookup"><span data-stu-id="5612c-113">You can use the default percentages for each sales or purchase line, or you can change the amounts on the invoice as needed.</span></span> <span data-ttu-id="5612c-114">Till exempel, en totalsumma för hela ordern.</span><span class="sxs-lookup"><span data-stu-id="5612c-114">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="5612c-115">Eftersom det förutbetalda beloppet hör till köparen ända tills han/hon har mottagit varan eller tjänsten måste du lägga upp redovisningskonton för förskottsbetalningarna tills slutfakturan är bokförd.</span><span class="sxs-lookup"><span data-stu-id="5612c-115">Because the prepaid amount belongs to the buyer until they have received the goods or services, you need to set up general ledger accounts to hold the prepayment amounts until the final invoice is posted.</span></span> <span data-ttu-id="5612c-116">Förskottsbet. för försäljning måste registreras på ett skuldkonto tills artiklarna är levererade.</span><span class="sxs-lookup"><span data-stu-id="5612c-116">Sales prepayments must be recorded in a liabilities account until the items are shipped.</span></span> <span data-ttu-id="5612c-117">Förskottsbet. för inköp måste registreras på ett tillgångskonto tills artiklarna är levererade.</span><span class="sxs-lookup"><span data-stu-id="5612c-117">Purchase prepayments must be recorded in an assets account until the items are received.</span></span> <span data-ttu-id="5612c-118">Du måste dessutom skapa ett separat redovisningskonto för varje moms-ID.</span><span class="sxs-lookup"><span data-stu-id="5612c-118">In addition, you must set up a separate general ledger account for each VAT identifier.</span></span>

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a><span data-ttu-id="5612c-119">Så här lägger du till konton för förutbetalda poster i bokföringsinställningarna</span><span class="sxs-lookup"><span data-stu-id="5612c-119">To add prepayment accounts to the general posting setup</span></span>  

1. <span data-ttu-id="5612c-120">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bokföringsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5612c-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Posting Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5612c-121">Fyll i följande fält i fönstret **Bokföringsinställningar**:</span><span class="sxs-lookup"><span data-stu-id="5612c-121">In the **General Posting Setup** window, fill in the following fields:</span></span>  

    - <span data-ttu-id="5612c-122">**Förskottsbet.konto, försäljning**</span><span class="sxs-lookup"><span data-stu-id="5612c-122">**Sales Prepayments Account**</span></span>  
    - <span data-ttu-id="5612c-123">**Förskottsbet.konto, inköp**</span><span class="sxs-lookup"><span data-stu-id="5612c-123">**Purch. Prepayments Account**</span></span>  

## <a name="to-set-up-number-series-for-prepayment-documents"></a><span data-ttu-id="5612c-124">Så här skapar du nummerserier för dokument för förskottsbetalning</span><span class="sxs-lookup"><span data-stu-id="5612c-124">To set up number series for prepayment documents</span></span>  

1. <span data-ttu-id="5612c-125">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5612c-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5612c-126">I fönstret **Försäljningsinställningar** fyller du i följande fält:</span><span class="sxs-lookup"><span data-stu-id="5612c-126">In the **Sales & Receivables Setup** window, fill in the following fields:</span></span>  

   - <span data-ttu-id="5612c-127">**Försk.fakt.nr.serie (bokförd)**</span><span class="sxs-lookup"><span data-stu-id="5612c-127">**Posted Prepmt. Inv. Nos.**</span></span>
   - <span data-ttu-id="5612c-128">**Försk.kredit.nr.serie (bokförd)**</span><span class="sxs-lookup"><span data-stu-id="5612c-128">**Posted Prepmt. Cr. Memo Nos.**</span></span>

1. <span data-ttu-id="5612c-129">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5612c-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5612c-130">I fönstret **Inköpsinställningar** fyller du i följande fält:</span><span class="sxs-lookup"><span data-stu-id="5612c-130">In the **Purchases & Payables Setup** window, fill in the following fields:</span></span>

    - <span data-ttu-id="5612c-131">**Försk.fakt.nr.serie (bokförd)**</span><span class="sxs-lookup"><span data-stu-id="5612c-131">**Posted Prepmt. Inv. Nos.**</span></span>
    - <span data-ttu-id="5612c-132">**Försk.kredit.nr.serie (bokförd)**</span><span class="sxs-lookup"><span data-stu-id="5612c-132">**Posted Prepmt. Cr. Memo Nos.**</span></span>

> [!NOTE]  
>  <span data-ttu-id="5612c-133">Du kan använda samma nummerserier för förskottsfakturor och vanliga fakturor eller använda olika nummerserier.</span><span class="sxs-lookup"><span data-stu-id="5612c-133">You can use the same number series for prepayment invoices and regular invoices, or you can use different number series.</span></span> <span data-ttu-id="5612c-134">Om du använder olika serier får dessa inte överlappa, d.v.s. det får inte finnas några nummer som finns med i båda serierna.</span><span class="sxs-lookup"><span data-stu-id="5612c-134">If you use different series, they must not overlap because there must not be any numbers that exist in both series.</span></span>  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a><span data-ttu-id="5612c-135">Ställa in Procentandelar, förskottsbetalning för artiklar, kunder och leverantörer</span><span class="sxs-lookup"><span data-stu-id="5612c-135">To set up prepayment percentages for items, customers, and vendors</span></span>  
<span data-ttu-id="5612c-136">Du kan ställa in en artikels standardprocentandel för alla kunder, en specifik kund eller en kundprisgrupp.</span><span class="sxs-lookup"><span data-stu-id="5612c-136">For an item, you can set up a default prepayment percentage for all customers, a specific customer, or a customer price group.</span></span>  

1. <span data-ttu-id="5612c-137">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5612c-137">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5612c-138">Välj en artikel och välj sedan åtgärden **Procentandel för förskottsbet**.</span><span class="sxs-lookup"><span data-stu-id="5612c-138">Select an item, and then choose the **Prepayment Percentages** action.</span></span>  
3. <span data-ttu-id="5612c-139">I fönstret **Procentandelar, förskottsbetalning för försäljning** fyller du i följande fält:</span><span class="sxs-lookup"><span data-stu-id="5612c-139">In the **Sales Prepayment Percentages** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="5612c-140">Du kan ställa in en kunds eller leverantörs standardprocentandel för förskottsbet. för alla artiklar och alla typer av försäljningsrader.</span><span class="sxs-lookup"><span data-stu-id="5612c-140">For a customer or vendor, you can set up one default prepayment percentage for all items and all types of sales lines.</span></span> <span data-ttu-id="5612c-141">Ange detta på kundkortet eller leverantörskortet.</span><span class="sxs-lookup"><span data-stu-id="5612c-141">You enter this on the customer or vendor card.</span></span>

1. <span data-ttu-id="5612c-142">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5612c-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="5612c-143">Öppna kort för en kund.</span><span class="sxs-lookup"><span data-stu-id="5612c-143">Open the card for a customer.</span></span>
3. <span data-ttu-id="5612c-144">Fyll i fältet **Förskottsbetalning %**.</span><span class="sxs-lookup"><span data-stu-id="5612c-144">Fill in the **Prepayment %** field.</span></span>
4. <span data-ttu-id="5612c-145">Upprepa stegen för andra kunder eller för leverantörer.</span><span class="sxs-lookup"><span data-stu-id="5612c-145">Repeat the steps for other customers or for vendors.</span></span>  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a><span data-ttu-id="5612c-146">Så här fastställer du vilken förskottsbetalda procentandel som har första prioritet</span><span class="sxs-lookup"><span data-stu-id="5612c-146">To determine which prepayment percentage has first priority</span></span>  
<span data-ttu-id="5612c-147">En order kan ha en procentandel för en förskottsbet. i försäljningshuvudet och i olika procentandelar för artiklarna på raderna.</span><span class="sxs-lookup"><span data-stu-id="5612c-147">An order may have a prepayment percentage on the sales header, and a different percentage for the items on the lines.</span></span> <span data-ttu-id="5612c-148">Om du vill fastställa vilken förskottsbetald procentandel som kopplas till varje försäljningsrad letar systemet efter den förskottsbetalda procentandelen i följande ordning, och använder den första standardinställda det hittar:</span><span class="sxs-lookup"><span data-stu-id="5612c-148">To determine which prepayment percentage applies to each sale line, the system looks for the prepayment percentage in the following order and will apply the first default that it finds:</span></span>  
1. <span data-ttu-id="5612c-149">En procentandel för förskottsbet. för artikeln på raden och kunden som ordern är till.</span><span class="sxs-lookup"><span data-stu-id="5612c-149">A prepayment percentage for the item on the line and the customer that the order is for.</span></span>  
2. <span data-ttu-id="5612c-150">En procentandel för förskottsbet. för artikeln på raden och kundprisgruppen som kunden hör till.</span><span class="sxs-lookup"><span data-stu-id="5612c-150">A prepayment percentage for the item on the line and the customer price group that the customer belongs to.</span></span>  
3. <span data-ttu-id="5612c-151">En procentandel för förskottsbet. för artikeln på raden för alla kunder.</span><span class="sxs-lookup"><span data-stu-id="5612c-151">A prepayment percentage for the item on the line for all customers.</span></span>  
4. <span data-ttu-id="5612c-152">Procentandelen för förskottsbet. i försäljnings- eller inköpshuvudet.</span><span class="sxs-lookup"><span data-stu-id="5612c-152">The prepayment percentage on the sales or purchase header.</span></span>  

<span data-ttu-id="5612c-153">Procentandelen för förskottsbet. på kundkortet kommer således endast att användas om det inte finns en inställd procentandel för förskottsbet. för artikeln.</span><span class="sxs-lookup"><span data-stu-id="5612c-153">In other words, the prepayment percentage on the customer card will only apply if there is no prepayment percentage set up for the item.</span></span> <span data-ttu-id="5612c-154">Om du ändrar innehållet i fältet **Förskottsbetalning %** i försäljnings- eller inköpshuvudet efter att du har skapat raderna uppdateras den procentuella förskottsbetalningen.</span><span class="sxs-lookup"><span data-stu-id="5612c-154">However, if you change the contents of the **Prepayment Percentage** field on the sales or purchase header after you create the lines, the prepayment percentage on all of the lines will be updated.</span></span> <span data-ttu-id="5612c-155">Detta gör det enkelt att upprätta en order med en fast procentandel för förskottsbet., utan att ta hänsyn till procentandelen som ställts in för artiklar.</span><span class="sxs-lookup"><span data-stu-id="5612c-155">This makes it easy to create an order with a fixed prepayment percentage, regardless of the percentage set up on items.</span></span>

## <a name="see-also"></a><span data-ttu-id="5612c-156">Se även</span><span class="sxs-lookup"><span data-stu-id="5612c-156">See Also</span></span>  
[<span data-ttu-id="5612c-157">Fakturera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="5612c-157">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="5612c-158">Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning</span><span class="sxs-lookup"><span data-stu-id="5612c-158">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="5612c-159">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="5612c-159">Finance</span></span>](finance.md)  
<span data-ttu-id="5612c-160">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5612c-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
