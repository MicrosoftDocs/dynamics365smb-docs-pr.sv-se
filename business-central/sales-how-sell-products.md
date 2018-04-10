---
title: "Skapa en försäljningsorder och sälja produkter | Microsoft Docs"
description: "Beskriver hur du skapar en försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/03/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b4dfdeb3cf49867699907c444147060727d3f146
ms.openlocfilehash: e3dd910eed2151121f75e754a3afc39c3d529691
ms.contentlocale: sv-se
ms.lasthandoff: 04/09/2018

---
# <a name="sell-products"></a><span data-ttu-id="24092-103">Sälja produkter</span><span class="sxs-lookup"><span data-stu-id="24092-103">Sell Products</span></span>
<span data-ttu-id="24092-104">Du kan skapa en försäljningsorder eller försäljningsfaktura för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.</span><span class="sxs-lookup"><span data-stu-id="24092-104">You create a sales order or sales invoice to record your agreement with a customer to sell certain products on certain delivery and payment terms.</span></span>

> [!NOTE]  
>   <span data-ttu-id="24092-105">Du måste använda försäljningsorder om din försäljningsprocess kräver att du t.ex. kan leverera delar av en orderkvantitet eftersom hela kvantiteten inte är tillgängliga på en gång.</span><span class="sxs-lookup"><span data-stu-id="24092-105">You use sales orders if your sales process requires that you can ship parts of an order quantity, for example, because the full quantity is not available at once.</span></span> <span data-ttu-id="24092-106">Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="24092-106">If you sell items by delivering directly from your vendor to your customer, as a drop shipment, then you must also use sales orders.</span></span> <span data-ttu-id="24092-107">För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="24092-107">For more information, see [Make Drop Shipments](sales-how-drop-shipment.md).</span></span> <span data-ttu-id="24092-108">I alla andra aspekter fungerar försäljningsorder på samma sätt som försäljningsfakturor.</span><span class="sxs-lookup"><span data-stu-id="24092-108">In all other aspects, sales orders work the same way as sales invoices.</span></span> <span data-ttu-id="24092-109">Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="24092-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

<span data-ttu-id="24092-110">Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsorder när du instämmer om försäljningen.</span><span class="sxs-lookup"><span data-stu-id="24092-110">You can negotiate with the customer by first creating a sales quote, which you can convert to a sales order when you agree on the sale.</span></span> <span data-ttu-id="24092-111">Mer information finns i [Skapa erbjudanden](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="24092-111">For more information, see [Make Offers](sales-how-make-offers.md).</span></span>

<span data-ttu-id="24092-112">När kunden har bekräftat avtalet, till exempel efter en offertprocess, skickar du en orderbekräftelse för att registrera dina åtagande att leverera produkterna enligt överenskomment.</span><span class="sxs-lookup"><span data-stu-id="24092-112">After the customer has confirmed the agreement, for example after a quote process, you can send an order confirmation to record your obligation to deliver the products as agreed.</span></span>

<span data-ttu-id="24092-113">När du har levererat produkterna, antingen helt eller delvis, bokför du försäljningsordern som levererade eller som levererade och fakturerade för att skapa kundreskontratransaktioner i systemet.</span><span class="sxs-lookup"><span data-stu-id="24092-113">When you deliver the products, either fully or partially, you post the sales order as shipped or as shipped and invoiced to create the related item and customer ledger entries in your system.</span></span> <span data-ttu-id="24092-114">När du bokför försäljningsorder, kan du också e-posta dokument som en PDF-bilaga.</span><span class="sxs-lookup"><span data-stu-id="24092-114">When you post the sales order, you can also email the document as a PDF attachment.</span></span> <span data-ttu-id="24092-115">Du kan använda ifylld e-postbrödtext med en sammanfattning av ordern och betalningsinformationen, till exempel en länk till PayPal.</span><span class="sxs-lookup"><span data-stu-id="24092-115">You can have the email body prefilled with a summary of the order and payment information, such as a link to PayPal.</span></span> <span data-ttu-id="24092-116">Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="24092-116">For more information, see [Send Documents by Email](ui-how-send-documents-email.md).</span></span>

<span data-ttu-id="24092-117">I affärsmiljöer där kunden måste betala för produkter i förväg måste du vänta på kvittot på betalning innan du levererar produkterna.</span><span class="sxs-lookup"><span data-stu-id="24092-117">In business environments where the customer must pay before products are delivered, such as in retail, you must wait for the receipt of payment before you deliver the products.</span></span> <span data-ttu-id="24092-118">I de flesta fall behandlar du inkommande betalningar några veckor efter leverans, genom att koppla betalningarna till dess relaterade obetalda bokförda försäljningsfakturor.</span><span class="sxs-lookup"><span data-stu-id="24092-118">In most cases, you process incoming payments some weeks after delivery by applying the payments to their related posted, unpaid sales invoices.</span></span> <span data-ttu-id="24092-119">Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="24092-119">For more information, see [Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>

<span data-ttu-id="24092-120">Det är enkelt att rätta eller avbryta en bokförd försäljningsfaktura som härrör från en försäljningsorder, innan den har betalas.</span><span class="sxs-lookup"><span data-stu-id="24092-120">You can easily correct or cancel a posted sales invoice resulting from a sales order before it is paid.</span></span> <span data-ttu-id="24092-121">Det är användbart om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen.</span><span class="sxs-lookup"><span data-stu-id="24092-121">This is useful if you want to correct a typing mistake or if the customer requests a change early in the order process.</span></span> <span data-ttu-id="24092-122">Mer information finns i [Så här kan du korrigera eller annullera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md).</span><span class="sxs-lookup"><span data-stu-id="24092-122">For more information, see [Correct or Cancel Unpaid Sales Invoices](sales-how-correct-cancel-sales-invoice.md).</span></span> <span data-ttu-id="24092-123">Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota för att återföra försäljningen.</span><span class="sxs-lookup"><span data-stu-id="24092-123">If the posted sales invoice is paid, then you must create a sales credit memo to reverse the sale.</span></span> <span data-ttu-id="24092-124">Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="24092-124">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>

<span data-ttu-id="24092-125">Artiklar kan vara både lagerartiklar och tjänster, betecknade med typerna **objekt - lager** och **objekt - tjänst** på försäljningsraderna.</span><span class="sxs-lookup"><span data-stu-id="24092-125">Items can be both inventory items and services, denoted by the **Item - Inventory** and **Item - Service** types on sales lines.</span></span> <span data-ttu-id="24092-126">Försäljningsorderprocessen är samma för båda artikeltyper.</span><span class="sxs-lookup"><span data-stu-id="24092-126">The sales order process is the same for both item types.</span></span> <span data-ttu-id="24092-127">Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="24092-127">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

<span data-ttu-id="24092-128">Du kan fylla i kundfälten på försäljningsorder på två sätt, beroende på om kunden redan har registrerats.</span><span class="sxs-lookup"><span data-stu-id="24092-128">You can fill customer fields on the sales order in two ways depending on whether the customer is already registered.</span></span> <span data-ttu-id="24092-129">Se steg 2 och 3 i följande procedur.</span><span class="sxs-lookup"><span data-stu-id="24092-129">See steps 2 and 3 in the following procedure.</span></span>

## <a name="to-create-a-sales-order"></a><span data-ttu-id="24092-130">Så här skapar du försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="24092-130">To create a sales order</span></span>
1. <span data-ttu-id="24092-131">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="24092-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="24092-132">Ange namnet på en befintlig kund i fältet **Kund**.</span><span class="sxs-lookup"><span data-stu-id="24092-132">In the **Customer** field, enter the name of an existing customer.</span></span>

    <span data-ttu-id="24092-133">Andra fält i fönstret **Försäljningsorder** fylls nu i med standardinformation om den valda kunden.</span><span class="sxs-lookup"><span data-stu-id="24092-133">Other fields in the **Sales Order** window are now filled with the standard information of the selected customer.</span></span> <span data-ttu-id="24092-134">Om kunden inte är registrerad, gör så här:</span><span class="sxs-lookup"><span data-stu-id="24092-134">If the customer is not registered, then follow these steps:</span></span>
3. <span data-ttu-id="24092-135">Ange namnet på en ny kund i fältet **Kund**.</span><span class="sxs-lookup"><span data-stu-id="24092-135">In the **Customer** field, enter the name of the new customer.</span></span>
4. <span data-ttu-id="24092-136">Välj knappen **ja** i dialogrutan om registrering av den nya kunden.</span><span class="sxs-lookup"><span data-stu-id="24092-136">In the dialog box about registering the new customer, choose the **Yes** button.</span></span>
5. <span data-ttu-id="24092-137">Välj en mall det nya kundkortet ska baseras på i fönstret **Välj en mall för en ny kund** och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="24092-137">In the **Select a template for a new customer** window, choose a template to base the new customer card on, and then choose the **OK** button.</span></span>

    <span data-ttu-id="24092-138">Ett nytt kundkort öppnas med förifylld information från den markerade kundmallen.</span><span class="sxs-lookup"><span data-stu-id="24092-138">A new customer card opens, prefilled with the information on the selected customer template.</span></span> <span data-ttu-id="24092-139">Fältet **Namn** förifylls med nya kundens namn som du har angett på Försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="24092-139">The **Name** field is prefilled with the new customer’s name that you entered on the sales order.</span></span>
6. <span data-ttu-id="24092-140">Fortsätt att fylla de återstående fälten på kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-140">Proceed to fill in the remaining fields on the customer card.</span></span> <span data-ttu-id="24092-141">Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="24092-141">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>  
7. <span data-ttu-id="24092-142">Välj **OK** för att gå tillbaka till fönstret **Försäljningsorder**, när du har slutfört kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-142">When you have completed the customer card, choose the **OK** button to return to the **Sales Order** window.</span></span>

    <span data-ttu-id="24092-143">Flera fält i Försäljningsorder är nu ifyllda med information som du har angett på det nya kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-143">Several fields on the sales order are now filled with information that you specified on the new customer card.</span></span>
8. <span data-ttu-id="24092-144">I fönstret **Försäljningsorder** fyller du i de återstående fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="24092-144">Fill in the remaining fields in the **Sales Order** window as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    <span data-ttu-id="24092-145">Du är nu redo att fylla i Försäljningsorderraderna med lagerförda artiklar eller tjänster som du vill sälja till kunden.</span><span class="sxs-lookup"><span data-stu-id="24092-145">You are now ready to fill in the sales order lines with inventory items or services that you want to sell to the customer.</span></span>

    <span data-ttu-id="24092-146">Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.</span><span class="sxs-lookup"><span data-stu-id="24092-146">If you have set up recurring sales lines for the customer, such as a monthly replenishment order, then you can insert these lines on the order by choosing the **Get Recurring Sales Lines** action.</span></span>
9. <span data-ttu-id="24092-147">Ange numret på en lagerförd artikel eller service på snabbfliken **Rader** Snabbfliken, i **Artikel** fältet.</span><span class="sxs-lookup"><span data-stu-id="24092-147">On the **Lines** FastTab, in the **Item** field, enter the number of an inventory item or service.</span></span>  
10. <span data-ttu-id="24092-148">Skriv det antal artiklar som ska säljas i fältet **Kvantitet**.</span><span class="sxs-lookup"><span data-stu-id="24092-148">In the **Quantity** field, enter the number of items to be sold.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="24092-149">För artiklar av typen Tjänst är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden.</span><span class="sxs-lookup"><span data-stu-id="24092-149">For items of type Service, the quantity is a time unit, such as hours, as indicated in the **Unit of Measure Code** field on the line.</span></span>

    <span data-ttu-id="24092-150">Fältet **Radbelopp** uppdateras och visar värdet i fältet **Enhetspris** multiplicerat med värdet i fältet **Kvantitet**.</span><span class="sxs-lookup"><span data-stu-id="24092-150">The **Line Amount** field is updated to show the value in the **Unit Price** field multiplied by the value in the **Quantity** field.</span></span>

    <span data-ttu-id="24092-151">Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-151">The price and line amounts are shown with or without sales tax depending on what you selected in the **Prices Including Tax** field on the customer card.</span></span>
11. <span data-ttu-id="24092-152">Ange ett värde i procent, om du vill bevilja kunden en rabatt på produkten i fältet **Radrabatt %**.</span><span class="sxs-lookup"><span data-stu-id="24092-152">In the **Line Discount %** field, enter a percentage if you want to grant the customer a discount on the product.</span></span> <span data-ttu-id="24092-153">Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.</span><span class="sxs-lookup"><span data-stu-id="24092-153">The value in the **Line Amount** field is updated accordingly.</span></span>

    <span data-ttu-id="24092-154">Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på offertraden automatiskt om de överenskomna prisvillkorna uppfylls.</span><span class="sxs-lookup"><span data-stu-id="24092-154">If you have set up special item prices on the **Sales Prices and Sales Line Discounts** FastTab on the customer or item card, then the price and amount on the quote line are automatically updated if the agreed price criteria are met.</span></span> <span data-ttu-id="24092-155">Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="24092-155">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>
12. <span data-ttu-id="24092-156">Ange en text i fältet **Beskrivning** på en tom rad för att lägga till en kommentar om offertraden som kunden kan se på den utskrivna offerten.</span><span class="sxs-lookup"><span data-stu-id="24092-156">To add a comment about the quote line that the customer can see on the printed sales quote, write a text in the **Description** field on an empty line.</span></span>  
13. <span data-ttu-id="24092-157">Upprepa moment 9 till 12 för varje artikel som du vill att erbjuda kunden.</span><span class="sxs-lookup"><span data-stu-id="24092-157">Repeat steps 9 through 12 for every item that you want to offer to the customer.</span></span>

    <span data-ttu-id="24092-158">Summorna under raderna beräknas automatiskt när du skapar eller ändrar rader.</span><span class="sxs-lookup"><span data-stu-id="24092-158">The totals under the lines are automatically calculated as you create or modify lines.</span></span>
14. <span data-ttu-id="24092-159">Ett nytt kundkort visar information från den markerade kundmallen.</span><span class="sxs-lookup"><span data-stu-id="24092-159">A new customer card displays the information on the selected customer template.</span></span> <span data-ttu-id="24092-160">Fyll i resterande fält.</span><span class="sxs-lookup"><span data-stu-id="24092-160">Fill in the remaining fields.</span></span> <span data-ttu-id="24092-161">Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="24092-161">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>  
15. <span data-ttu-id="24092-162">Välj knappen **OK** för att gå tillbaka till fönstret **Försäljningsorder** när du har slutfört kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-162">When you have completed the customer card, choose the **OK** button to return to the **Sales Order** window.</span></span>

    <span data-ttu-id="24092-163">Flera fält i Försäljningsorder är nu ifyllda med information som du har angett på det nya kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-163">Several fields on the sales order are now filled with information that you specified on the new customer card.</span></span>
16. <span data-ttu-id="24092-164">I fönstret **Försäljningsorder** fyller du i de återstående fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="24092-164">Fill in the remaining fields in the **Sales Order** window as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="24092-165">Du är nu klar att fylla i försäljningsorderraderna för produkter som du säljer till kunden eller för en transaktion med den kund som du vill registrera en post i ett redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="24092-165">You are now ready to fill in the sales order lines for products that you are selling to the customer or for any transaction with the customer that you want to record in a G/L account.</span></span>   

    <span data-ttu-id="24092-166">Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.</span><span class="sxs-lookup"><span data-stu-id="24092-166">If you have set up recurring sales lines for the customer, such as a monthly replenishment order, then you can insert these lines on the order by choosing the **Get Recurring Sales Lines** action.</span></span>  
17. <span data-ttu-id="24092-167">På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.</span><span class="sxs-lookup"><span data-stu-id="24092-167">On the **Lines** FastTab, in the **Type** field, select what type of product, charge, or transaction that you will post for the customer with the sales line.</span></span>

18. <span data-ttu-id="24092-168">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="24092-168">In the **No.**</span></span> <span data-ttu-id="24092-169">väljer du en post som ska bokföras enligt värdet i fältet **Typ**.</span><span class="sxs-lookup"><span data-stu-id="24092-169">field, select a record to post according to the value in the **Type** field.</span></span>

    <span data-ttu-id="24092-170">Du lämnar fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="24092-170">You leave the **No.**</span></span> <span data-ttu-id="24092-171">tomt i följande fall:</span><span class="sxs-lookup"><span data-stu-id="24092-171">field empty in the following cases:</span></span>

    * <span data-ttu-id="24092-172">Om raden är avsedd för en kommentar.</span><span class="sxs-lookup"><span data-stu-id="24092-172">If the line is for a comment.</span></span> <span data-ttu-id="24092-173">Skriv kommentaren i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="24092-173">Write the comment in the **Description** field.</span></span>
    * <span data-ttu-id="24092-174">Om raden är avsedd för en ej lagerförd artikel.</span><span class="sxs-lookup"><span data-stu-id="24092-174">If the line is for a nonstock item.</span></span> <span data-ttu-id="24092-175">Välj åtgärden **Markera ej lagerförda artiklar**.</span><span class="sxs-lookup"><span data-stu-id="24092-175">Choose the **Select Nonstock Items** action.</span></span> <span data-ttu-id="24092-176">Mer information finns i [Arbeta med ej lagerförda artiklar](inventory-how-work-nonstock-items.md).</span><span class="sxs-lookup"><span data-stu-id="24092-176">For more information, see [Work With Nonstock Items](inventory-how-work-nonstock-items.md).</span></span>

19. <span data-ttu-id="24092-177">I fältet **Antal** anger du hur många enheter av produkt, kostnad eller transaktion som registreras på raden för kunden.</span><span class="sxs-lookup"><span data-stu-id="24092-177">In the **Quantity** field, enter how many units of the product, charge, or transaction that the line will record for the customer.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="24092-178">Om artikeln är av typen **Artikel - tjänst** eller **Resurs** är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden.</span><span class="sxs-lookup"><span data-stu-id="24092-178">If the item is of type **Item - Service** or **Resource**, the quantity is a time unit, such as hours, as indicated in the **Unit of Measure Code** field on the line.</span></span> <span data-ttu-id="24092-179">Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md).</span><span class="sxs-lookup"><span data-stu-id="24092-179">For more information, see [Set Up Item Units of Measure](inventory-how-setup-units-of-measure.md).</span></span>

    <span data-ttu-id="24092-180">Värdet i fältet **Radbelopp** beräknas som *enhetspris* x *antal*.</span><span class="sxs-lookup"><span data-stu-id="24092-180">The value in the **Line Amount** field is calculated as *Unit Price* x *Quantity*.</span></span>  

    <span data-ttu-id="24092-181">Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.</span><span class="sxs-lookup"><span data-stu-id="24092-181">The price and line amounts are with or without sales tax, depending on what you selected in the **Prices Including Tax** field on the customer card.</span></span>  
20. <span data-ttu-id="24092-182">Om du vill ge en rabatt kan du ange ett procenttal i fältet **radrabatt %**.</span><span class="sxs-lookup"><span data-stu-id="24092-182">If you want to give a discount, enter a percentage in the **Line Discount %** field.</span></span> <span data-ttu-id="24092-183">Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.</span><span class="sxs-lookup"><span data-stu-id="24092-183">The value in the **Line Amount** field updates accordingly.</span></span>  

    <span data-ttu-id="24092-184">Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på försäljningsraden automatiskt om de överenskomna prisvillkorna uppfylls.</span><span class="sxs-lookup"><span data-stu-id="24092-184">If special item prices are set up on the **Sales Prices and Sales Line Discounts** FastTab on the customer or item card, the price and amount on the sales line automatically update if the price criteria is met.</span></span> <span data-ttu-id="24092-185">Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="24092-185">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>  
21. <span data-ttu-id="24092-186">Upprepa moment 9 till 12 för varje produkt som du vill att sälja till kunden.</span><span class="sxs-lookup"><span data-stu-id="24092-186">Repeat steps 9 through 12 for every product or charge you want to sell to the customer.</span></span>  

    <span data-ttu-id="24092-187">Summorna under raderna beräknas automatiskt när du skapar eller ändrar rader.</span><span class="sxs-lookup"><span data-stu-id="24092-187">The totals under the lines are automatically calculated as you create or modify lines.</span></span>  
22. <span data-ttu-id="24092-188">I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.</span><span class="sxs-lookup"><span data-stu-id="24092-188">In the **Invoice Discount Amount** field, enter an amount that should be deducted from the value shown in the **Total Incl. Tax** field.</span></span>

    <span data-ttu-id="24092-189">Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**.</span><span class="sxs-lookup"><span data-stu-id="24092-189">If you have set up invoice discounts for the customer, then the specified percentage value is automatically inserted in the **Invoice Discount %** field if the criteria are met, and the related amount is inserted in the **Inv. Discount Amount Excl. Tax** field.</span></span> <span data-ttu-id="24092-190">Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="24092-190">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>
23. <span data-ttu-id="24092-191">Att enbart leverera en del av orderkvantiteten , anger denna kvantitet i **Ant. att utleverera**.</span><span class="sxs-lookup"><span data-stu-id="24092-191">To only ship a part of the order quantity, enter that quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="24092-192">Värdet kopieras till **Ant. att fakturera**.</span><span class="sxs-lookup"><span data-stu-id="24092-192">The value is copied to the **Qty. to Invoice** field.</span></span>
24. <span data-ttu-id="24092-193">För att enbart fakturera en del av den levererade kvantiteten , anger du denna kvantitet i **Ant. att fakturera**.</span><span class="sxs-lookup"><span data-stu-id="24092-193">To only invoice a part of the shipped quantity, enter that quantity in the **Qty. to Invoice** field.</span></span> <span data-ttu-id="24092-194">Antalet kan inte vara högre än värdet i fältet **Ant. att utleverera**.</span><span class="sxs-lookup"><span data-stu-id="24092-194">The quantity must be lower than the value in the **Qty. to Ship** field.</span></span>   
25. <span data-ttu-id="24092-195">När försäljningsorderraderna slutförda väljer du åtgärden **Bokföra och skicka**.</span><span class="sxs-lookup"><span data-stu-id="24092-195">When the sales order lines are completed, choose the **Post and Send** action.</span></span>

<span data-ttu-id="24092-196">Dialogrutan **Bokför och skicka bekräftelse** visar kundens standardmetod för mottagning av dokument.</span><span class="sxs-lookup"><span data-stu-id="24092-196">The **Post and Send Confirmation** dialog box displays the customer's preferred method of receiving documents.</span></span> <span data-ttu-id="24092-197">Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**.</span><span class="sxs-lookup"><span data-stu-id="24092-197">You can change the sending method by choosing the lookup button for the **Send Document to** field.</span></span> <span data-ttu-id="24092-198">Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="24092-198">For more information, see [Set Up Document Sending Profiles](sales-how-setup-document-send-profiles.md).</span></span>

<span data-ttu-id="24092-199">Relaterade artiklar och kundtransaktionerna skapas nu i systemet, och försäljningsorder matas ut som ett PDF-dokument.</span><span class="sxs-lookup"><span data-stu-id="24092-199">The related item and customer ledger entries are now created in your system, and the sales order is output as a PDF document.</span></span> <span data-ttu-id="24092-200">När försäljningsordern bokförs helt tas den bort från listan över försäljningsorder och ersätts med nya dokument i listan över bokförda försäljningsfakturor och listan över bokförda försäljningsleveranser.</span><span class="sxs-lookup"><span data-stu-id="24092-200">When the sales order is fully posted, it is removed from the list of sales orders and replaced with new documents in the list of posted sales invoices and the list of posted sales shipments.</span></span>

## <a name="see-also"></a><span data-ttu-id="24092-201">Se även</span><span class="sxs-lookup"><span data-stu-id="24092-201">See Also</span></span>
[<span data-ttu-id="24092-202">Försäljning</span><span class="sxs-lookup"><span data-stu-id="24092-202">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="24092-203">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="24092-203">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="24092-204">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="24092-204">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="24092-205">Skicka dokument som e-post</span><span class="sxs-lookup"><span data-stu-id="24092-205">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="24092-206">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="24092-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
