---
title: "Så här skapar du försäljningsavropsorder | Microsoft Docs"
description: "Du kan använda avropsorder om en kund har avtalat att köpa stora antal som ska levereras i flera mindre leveranser under en bestämd tidsperiod."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 75e170f10927844ca37a001812e78e062e88c451
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-blanket-sales-orders"></a><span data-ttu-id="47039-103">Arbeta med försäljningsavropsorder</span><span class="sxs-lookup"><span data-stu-id="47039-103">Work with Blanket Sales Orders</span></span>
<span data-ttu-id="47039-104">En avropsorder utgör ramen för en långsiktig överenskommelse mellan företaget och en kund.</span><span class="sxs-lookup"><span data-stu-id="47039-104">A blanket sales order represents a framework for a long-term agreement between you and your customer.</span></span>

<span data-ttu-id="47039-105">En avropsorder skapas vanligtvis om en kund har lovat att köpa stora antal som ska levereras i flera mindre leveranser under en bestämd tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="47039-105">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="47039-106">Avropsorder gäller vanligtvis bara en artikel med förbestämda leveransdatum.</span><span class="sxs-lookup"><span data-stu-id="47039-106">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="47039-107">Huvudanledningen till att en avropsorder används i stället för en försäljningsorder är att de antal som anges på en avropsorder inte påverkar artikeldispositionen och därmed kan användas som ett kalkylark för övervakning, prognostisering och planering.</span><span class="sxs-lookup"><span data-stu-id="47039-107">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability and thus can be used as a worksheet for monitoring, forecasting, and planning purposes.</span></span>

<span data-ttu-id="47039-108">På avropsordern kan varje separat leverans anges som en orderrad som sedan kan omvandlas till en försäljningsorder vid leveransen.</span><span class="sxs-lookup"><span data-stu-id="47039-108">On the blanket order, each separate shipment can be set up as an order line, which can then be converted into a sales order at the time of shipping.</span></span>

<span data-ttu-id="47039-109">Ett exempel på en situation där en avropsorder kan användas är om en kund beställer 1 000 enheter av en artikel och vill att 250 artiklar åt gången ska levereras en gång i veckan under den kommande månaden.</span><span class="sxs-lookup"><span data-stu-id="47039-109">An example of when a blanket sales order could be used is if a customer calls and places an order of 1000 units of an item and they want the items to be delivered in 250 units every week over the next month.</span></span>

> [!NOTE]
> <span data-ttu-id="47039-110">Inköpsavropsorder fungerar på samma sätt som en försäljningsavropsorder.</span><span class="sxs-lookup"><span data-stu-id="47039-110">Blanket purchase orders work in a similar way as blanket sales orders.</span></span> <span data-ttu-id="47039-111">Denna dokumentation täcker inte inköpsavropsorder.</span><span class="sxs-lookup"><span data-stu-id="47039-111">This documentation does not cover blanket purchase orders.</span></span>

## <a name="to-create-a-blanket-sales-order"></a><span data-ttu-id="47039-112">Så här skapar du en avropsorder</span><span class="sxs-lookup"><span data-stu-id="47039-112">To create a blanket sales order</span></span>  
1. <span data-ttu-id="47039-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **försäljningsavropsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47039-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="47039-114">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="47039-114">Choose the **New** action.</span></span>  
3. <span data-ttu-id="47039-115">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="47039-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="47039-116">Låt fältet **Orderdatum** vara tomt.</span><span class="sxs-lookup"><span data-stu-id="47039-116">Leave the **Order Date** field blank.</span></span> <span data-ttu-id="47039-117">När separata försäljningsorder skapas från avropsordern anges orderdatum för försäljningsordern som det aktuella arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="47039-117">When the separate sales orders are created from the blanket order, the order date of the sales order is set to equal the actual work date.</span></span>
5. <span data-ttu-id="47039-118">På snabbfliken **Rader** skapar du separata rader för varje utleverans.</span><span class="sxs-lookup"><span data-stu-id="47039-118">On the **Lines** FastTab, create separate lines for each shipment.</span></span> <span data-ttu-id="47039-119">Om kunden t.ex. beställer 1 000 enheter jämnt fördelade över fyra veckor skapar du fyra separata rader med 250 enheter på varje rad.</span><span class="sxs-lookup"><span data-stu-id="47039-119">For instance, if your customer wants 1000 units split out equally between four weeks, you would enter four separate lines of 250 units each.</span></span>   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><span data-ttu-id="47039-120">Så här skapar du en försäljningsorder från en avropsorder</span><span class="sxs-lookup"><span data-stu-id="47039-120">To create a sales order from a blanket sales order</span></span>  

1.  <span data-ttu-id="47039-121">Om du vill skapa en order för någon av raderna i monteringsordern för avrop tar du bort antalet i fältet **Levereras antal** för alla de rader som du INTE vill leverera just nu.</span><span class="sxs-lookup"><span data-stu-id="47039-121">To create an order for any of the lines in the blanket assembly order, remove the quantity in the **Qty. to Ship** field on all the lines that you DO NOT wish to ship at this time.</span></span>  
2.  <span data-ttu-id="47039-122">När du vill börja skapa order väljer du åtgärden **Skapa order** och väljer sedan **Ja**.</span><span class="sxs-lookup"><span data-stu-id="47039-122">When you are ready to create orders, choose the **Make Order**m action, and then choose **Yes**.</span></span> <span data-ttu-id="47039-123">Du får ett meddelande om att avropsordern har tilldelats ett ordernummer.</span><span class="sxs-lookup"><span data-stu-id="47039-123">A message appears informing you that the blanket order has been assigned an order number.</span></span> <span data-ttu-id="47039-124">Observera att avropsordern inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="47039-124">Note that the blanket order has not been deleted.</span></span>  
3.  <span data-ttu-id="47039-125">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="47039-125">Choose the **OK** button.</span></span>  
4.  <span data-ttu-id="47039-126">På snabbfliken **Rad** väljer du åtgärden **Ej bokförda rader** och sedan väljer du åtgärden **Order**.</span><span class="sxs-lookup"><span data-stu-id="47039-126">To see the results of the preceding steps, choose the **Line** action, choose the **Unposted Lines** action, and then choose the **Orders** action.</span></span>  
5.  <span data-ttu-id="47039-127">I fönstret **Försäljningsrader** väljer du önskad försäljningsorde, väljer åtgärden **Rad** och väljer sedan åtgärden **Visa dokument** action.</span><span class="sxs-lookup"><span data-stu-id="47039-127">In the **Sales Lines** window, select the appropriate sales order, choose the **Line** action, and then choose the **Show Document** action.</span></span>  

<span data-ttu-id="47039-128">Följande gäller försäljningsorder, när de har skapats från försäljningsavropsorder:</span><span class="sxs-lookup"><span data-stu-id="47039-128">The following applies to sales orders after they have been created from blanket sales orders:</span></span>  

- <span data-ttu-id="47039-129">När avropsordern har omvandlats till en försäljningsorder innehåller försäljningsordern alla raderna från avropsordern.</span><span class="sxs-lookup"><span data-stu-id="47039-129">After the blanket order is converted into a sales order, the sales order contains all the lines from the blanket order.</span></span> <span data-ttu-id="47039-130">De rader där antalet i fältet **Levereras antal** togs bort visas, men fältet **Antal** är tomt för dessa rader.</span><span class="sxs-lookup"><span data-stu-id="47039-130">The lines where the quantity in the **Qty. to Ship** field was deleted appear, but with blank **Quantity** fields.</span></span> <span data-ttu-id="47039-131">Du kan låta de här raderna vara kvar eller redigera eller ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="47039-131">You may choose to leave, edit, or delete the lines.</span></span>  
- <span data-ttu-id="47039-132">Det är viktigt att komma ihåg att antalet på en försäljningsorderrad inte får vara större än antalet på den associerade avropsorderraden.</span><span class="sxs-lookup"><span data-stu-id="47039-132">It is important to remember that the sales order line quantity must not exceed the quantity of the associated blanket order line.</span></span> <span data-ttu-id="47039-133">Om detta sker går det inte att bokföra försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="47039-133">Otherwise, posting of the sales order will not be possible.</span></span>  
- <span data-ttu-id="47039-134">När försäljningsordern bokförts som levererad och/eller fakturerad uppdateras fälten **Utlevererat antal** och **Fakturerat antal** på den relaterade avropsordern.</span><span class="sxs-lookup"><span data-stu-id="47039-134">When the sales order is posted as shipped and/or invoiced, the **Quantity Shipped** and **Quantity Invoiced** fields are updated on the related blanket order.</span></span>  
- <span data-ttu-id="47039-135">Avropsordernumret och radnumret registreras som försäljningsradernas egenskaper när de skapas från en avropsorder.</span><span class="sxs-lookup"><span data-stu-id="47039-135">The blanket order number and line number are recorded as properties of the sales lines when created from a blanket order.</span></span>  
- <span data-ttu-id="47039-136">Om en försäljningsorder inte skapas direkt från en avropsorder men ändå är relaterad till den kan du skapa en koppling mellan försäljningsordern och avropsordern genom att skriva in numret på den associerade avropsordern i fältet **Avropsordernr**</span><span class="sxs-lookup"><span data-stu-id="47039-136">When sales orders are not created directly from the blanket order but still relate to it, a link between a sales order and a blanket order can be established by entering the associated blanket order number in the **Blanket Order No.**</span></span> <span data-ttu-id="47039-137">på försäljningsorderraden.</span><span class="sxs-lookup"><span data-stu-id="47039-137">field on the sales order line.</span></span>  
- <span data-ttu-id="47039-138">När du har skapat en eller flera försäljningsorder för hela antalet på avropsorderraden, kan inga andra försäljningsorder skapas för samma rad.</span><span class="sxs-lookup"><span data-stu-id="47039-138">After the sales order has been created for the total quantity of a blanket order line, no other sales order can be created for the same line.</span></span> <span data-ttu-id="47039-139">Användare förhindras från att ange ett antal i fältet **antal. att utleverera**.</span><span class="sxs-lookup"><span data-stu-id="47039-139">Users are prevented from entering a quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="47039-140">Om du senare behöver lägga till ytterligare antal på en avropsorder kan du öka värdet i fältet **Antal** och sedan skapa ytterligare order.</span><span class="sxs-lookup"><span data-stu-id="47039-140">If, however, additional quantities need to be added to a blanket order, the value in the **Quantity** field can be increased and additional orders can then be created.</span></span>  
- <span data-ttu-id="47039-141">Den fakturerade försäljningsavropsordern finns kvar i systemet tills den tas bort, antingen genom att enskilda avropsorder tas bort eller att batch-jobbet **Ta bort faktrd förs.avropsord.** körs.</span><span class="sxs-lookup"><span data-stu-id="47039-141">The invoiced blanket sales order remains in the system until it is deleted, either by deleting individual blanket orders or by running the **Delete Invoiced Blanket Sales Orders** batch job.</span></span>  
- <span data-ttu-id="47039-142">Om en kund dessutom har registrerats som en kontakt i modulen Marknadsföring, och om en interaktionsmallkod har angetts för avropsorder i fönstret **Marknadsföringsinställning** registreras en interaktion i tabellen Interaktionslogg när du väljer **Skriv ut** för att skriva ut avropsordern.</span><span class="sxs-lookup"><span data-stu-id="47039-142">If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for blanket sales order in the **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Print** to print the blanket sales order.</span></span>

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a><span data-ttu-id="47039-143">Så här visar du status för avropsorder:</span><span class="sxs-lookup"><span data-stu-id="47039-143">To view the status of a blanket purchase order</span></span>  
<span data-ttu-id="47039-144">Du kan visa statusen för en försäljningsavropsordern i fönstret **Inköpsorderstatistik**.</span><span class="sxs-lookup"><span data-stu-id="47039-144">You can see the status of a blanket sales order in the **Purchase Blanket Order Statistics** window.</span></span> <span data-ttu-id="47039-145">Detta kan vara praktiskt när du börjar fakturera ordern som skapats utifrån avropsordern.</span><span class="sxs-lookup"><span data-stu-id="47039-145">This may be relevant when you start to invoice the order that is created from the blanket purchase order.</span></span>  

1.  <span data-ttu-id="47039-146">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **försäljningsavropsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47039-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="47039-147">Markera en inköpsavropsorder och välj åtgärden **statistik**.</span><span class="sxs-lookup"><span data-stu-id="47039-147">Select a blanket purchase order, and then choose the **Statistics** action.</span></span>  
3.  <span data-ttu-id="47039-148">På snabbfliken **Allmänt** i fönstret **Inköpsorderstatistik** visas översiktsinformation om hela ordern baserat på den totala kvantiteten i de olika **antalsfälten** på avropsorderraderna.</span><span class="sxs-lookup"><span data-stu-id="47039-148">In the **Purchase Blanket Order Statistics** window, on the **General** FastTab, you can see summary information about the entire order based on the total quantity in the various **Quantity fields** on the blanket purchase order lines.</span></span>  

    - <span data-ttu-id="47039-149">På snabbfliken **Fakturering** visas översiktsinformation som baseras på den totala kvantiteten i fälten för **Ant. att fakturera** på avropsorderraderna.</span><span class="sxs-lookup"><span data-stu-id="47039-149">On the **Invoicing** FastTab, you can see summary information based on the total quantity in the **Qty. to Invoice** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="47039-150">På snabbfliken **Leverans** visas översiktsinformation som baseras på den totala kvantiteten i fälten för **Ant. att inlevereras** på avropsorderraderna.</span><span class="sxs-lookup"><span data-stu-id="47039-150">On the **Shipping** FastTab, you can see summary information based on the total quantity in the **Qty. to Receive** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="47039-151">På snabbfliken **Förskottsbetalning** visas översiktsinformation om eventuella förskottsbetalda belopp.</span><span class="sxs-lookup"><span data-stu-id="47039-151">On the **Prepayment** FastTab, you can see summary information about any prepaid amounts.</span></span>  
    - <span data-ttu-id="47039-152">På snabbfliken **Leverantör** visas viss grundläggande information om leverantören.</span><span class="sxs-lookup"><span data-stu-id="47039-152">On the **Vendor** FastTab, you can see certain basic information about the vendor.</span></span>    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><span data-ttu-id="47039-153">Så här väljer du att visa ej bokförda och bokförda försäljningsavropsorderrader</span><span class="sxs-lookup"><span data-stu-id="47039-153">To view unposted and posted blanket sales order lines</span></span>   
<span data-ttu-id="47039-154">Kopplingen mellan avropsordern, försäljning och den ursprungliga försäljningsordern och eventuella övriga försäljningsdokument, bibehålls när du har bokfört som en lista över bokförda och ej bokförda fakturarader för försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="47039-154">The link between the blanket sales order and the originating sales order, and any other sales document, is retained after posting as a list of posted and unposted sales order invoice lines.</span></span>  

1. <span data-ttu-id="47039-155">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **försäljningsavropsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47039-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon enter **Blanket Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="47039-156">Öppna den avropsorder för försäljning som du vill visa.</span><span class="sxs-lookup"><span data-stu-id="47039-156">Open the blanket sales order you want to view.</span></span>
3. <span data-ttu-id="47039-157">Om du vill visa transaktioner som inte har bokförts väljer du åtgärden **Rad** ocgh sedan **Ej bokförda rader**.</span><span class="sxs-lookup"><span data-stu-id="47039-157">To view unposted entries, select the line in question, choose the **Line** action, and then choose the **Unposted Lines** action.</span></span> <span data-ttu-id="47039-158">Välj något av följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="47039-158">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="47039-159">Alternativ</span><span class="sxs-lookup"><span data-stu-id="47039-159">Option</span></span></th>
    <th><span data-ttu-id="47039-160">Description</span><span class="sxs-lookup"><span data-stu-id="47039-160">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-161">**Order**</span><span class="sxs-lookup"><span data-stu-id="47039-161">**Orders**</span></span></td>
    <td><span data-ttu-id="47039-162">Anger öppna order som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-162">Specifies open orders associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-163">**Fakturor**</span><span class="sxs-lookup"><span data-stu-id="47039-163">**Invoices**</span></span></td>
    <td><span data-ttu-id="47039-164">Anger öppna fakturor som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-164">Specifies open invoices that have been associated with the selected line.</span></span> <span data-ttu-id="47039-165">Öppna fakturor kan associeras manuellt till en avropsorder genom att avropsordernumret anges på försäljningsfakturaraden.</span><span class="sxs-lookup"><span data-stu-id="47039-165">Open invoices are manually associated with a blanket order by entering the blanket order number on the sales invoice line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-166">**Returorder**</span><span class="sxs-lookup"><span data-stu-id="47039-166">**Return Orders**</span></span></td>
    <td><span data-ttu-id="47039-167">Anger öppna returorder som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-167">Specifies open return orders that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-168">**Kreditnota**</span><span class="sxs-lookup"><span data-stu-id="47039-168">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="47039-169">Anger öppna kreditnotor som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-169">Specifies open credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="47039-170">
4. Om du vill visa transaktioner som inte har bokförts väljer du åtgärden **Rad** och sedan **Bokförda rader**.</span><span class="sxs-lookup"><span data-stu-id="47039-170">
4. To view posted entries, select the line in question, choose the **Line** action, and then choose the **Posted Lines** action.</span></span> <span data-ttu-id="47039-171">Välj något av följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="47039-171">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="47039-172">Alternativ</span><span class="sxs-lookup"><span data-stu-id="47039-172">Option</span></span></th>
    <th><span data-ttu-id="47039-173">Description</span><span class="sxs-lookup"><span data-stu-id="47039-173">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-174">**Utleveranser**</span><span class="sxs-lookup"><span data-stu-id="47039-174">**Shipments**</span></span></td>
    <td><span data-ttu-id="47039-175">Bokförda leveranser som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-175">Posted shipments associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-176">**Fakturor**</span><span class="sxs-lookup"><span data-stu-id="47039-176">**Invoices**</span></span></td>
    <td><span data-ttu-id="47039-177">Bokförda fakturor som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-177">Posted invoices associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-178">**Returinleveranser**:</span><span class="sxs-lookup"><span data-stu-id="47039-178">**Return Receipts**</span></span></td>
    <td><span data-ttu-id="47039-179">Bokförda returinleveranser som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-179">Posted return receipts that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="47039-180">**Kreditnota**</span><span class="sxs-lookup"><span data-stu-id="47039-180">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="47039-181">Bokförda kreditnotor som är associerade till den markerade raden.</span><span class="sxs-lookup"><span data-stu-id="47039-181">Posted credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="47039-182">
5. I fönstret **Försäljningsrader** väljer du åtgärden **Visa dokument** för att visa transaktionen.</span><span class="sxs-lookup"><span data-stu-id="47039-182">
5. In the **Sales Lines** window, choose the **Show Document** action to view the entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="47039-183">Se även</span><span class="sxs-lookup"><span data-stu-id="47039-183">See Also</span></span>
[<span data-ttu-id="47039-184">Försäljning</span><span class="sxs-lookup"><span data-stu-id="47039-184">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="47039-185">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="47039-185">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="47039-186">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="47039-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
