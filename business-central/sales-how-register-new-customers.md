---
title: Skapa ett kundkort för att registrera en ny kund | Microsoft Docs
description: Beskriver hur du skapar ett kundkort för att registrera information om varje ny kund eller klienten som du säljer till.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: cc48c7c55edac8af9333dd04661a828c528621b8
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503979"
---
# <a name="register-new-customers"></a><span data-ttu-id="7e19e-103">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="7e19e-103">Register New Customers</span></span>

<span data-ttu-id="7e19e-104">Kunderna är källan till din inkomst.</span><span class="sxs-lookup"><span data-stu-id="7e19e-104">Customers are the source of your income.</span></span> <span data-ttu-id="7e19e-105">Du måste registrera varje kund som du säljer till som ett kundkort.</span><span class="sxs-lookup"><span data-stu-id="7e19e-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="7e19e-106">Kundkort innehåller den information som behövs för att sälja produkter till kunden.</span><span class="sxs-lookup"><span data-stu-id="7e19e-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="7e19e-107">Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="7e19e-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="7e19e-108">Innan du kan registrera nya kunder, måste du lägga upp olika försäljningskoder som du kan välja mellan, när du fyller i kundkort.</span><span class="sxs-lookup"><span data-stu-id="7e19e-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="7e19e-109">Mer information finns i [Konfigurera försäljning](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="7e19e-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="7e19e-110">Lägga till nya kunder</span><span class="sxs-lookup"><span data-stu-id="7e19e-110">Adding new customers</span></span>

<span data-ttu-id="7e19e-111">För att registrera en ny kund måste du fylla i ett kundkort.</span><span class="sxs-lookup"><span data-stu-id="7e19e-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="7e19e-112">Du kan upprätta mallar för olika kundprofiler eller lägga till kunder utan mallar.</span><span class="sxs-lookup"><span data-stu-id="7e19e-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="7e19e-113">Om kundmallar finns för olika kundtyper, visas en sida när du skapar ett nytt kundkort där du kan välja en lämplig mall.</span><span class="sxs-lookup"><span data-stu-id="7e19e-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="7e19e-114">Om endast en kundmall finns, då använder nya kundkort alltid den mallen.</span><span class="sxs-lookup"><span data-stu-id="7e19e-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="7e19e-115">SÅ här skapar du ett nytt kundkort</span><span class="sxs-lookup"><span data-stu-id="7e19e-115">To create a new customer card</span></span>

1. <span data-ttu-id="7e19e-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7e19e-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7e19e-117">På sidan **Kunder** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7e19e-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="7e19e-118">Om endast en kundmall finns, då öppnas ett nytt kundkort med fält ifyllda med information från mallen.</span><span class="sxs-lookup"><span data-stu-id="7e19e-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="7e19e-119">Om fler än en kundmall finns, öppnas en sida där du kan välja kundmall.</span><span class="sxs-lookup"><span data-stu-id="7e19e-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="7e19e-120">I detta fall, följ nästa två steg.</span><span class="sxs-lookup"><span data-stu-id="7e19e-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="7e19e-121">Välj den mall som du vill använda för det nya kundkortet på sidan **Välj en mall för en ny kund**.</span><span class="sxs-lookup"><span data-stu-id="7e19e-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="7e19e-122">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="7e19e-122">Choose the **OK** button.</span></span> <span data-ttu-id="7e19e-123">Ett nytt kundkort öppnas med ifyllda fält med information från mallen.</span><span class="sxs-lookup"><span data-stu-id="7e19e-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="7e19e-124">Fortsätt att fylla i eller ändra fält på kundkortet vid behov.</span><span class="sxs-lookup"><span data-stu-id="7e19e-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="7e19e-125">På snabbfliken **Försäljningspriser** ser du specialpriser eller rabatter som du beviljar för kunden om vissa villkor uppfylls, till exempel artikel, lägsta partistorlek eller slutdatum.</span><span class="sxs-lookup"><span data-stu-id="7e19e-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="7e19e-126">Varje rad representerar ett speciellt pris eller radrabatt.</span><span class="sxs-lookup"><span data-stu-id="7e19e-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="7e19e-127">Varje kolumn representerar ett kriterium som måste gälla för att garantera specialpriset som du anger i fältet **Enhetspris** eller radrabatten som du anger i fältet **Radrabatt %**.</span><span class="sxs-lookup"><span data-stu-id="7e19e-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="7e19e-128">Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="7e19e-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="7e19e-129">Kunden är nu registrerad, och kundkortet är klart att användas i försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="7e19e-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="7e19e-130">Om du vill använda detta kundkort som en mall när du skapar nya kundkort, så fortsätt med att spara den som en mall.</span><span class="sxs-lookup"><span data-stu-id="7e19e-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="7e19e-131">Mer information finns i följande avsnitt:</span><span class="sxs-lookup"><span data-stu-id="7e19e-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="7e19e-132">Om du vill spara kundkortet som en mall</span><span class="sxs-lookup"><span data-stu-id="7e19e-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="7e19e-133">På sidan **Kundkort** väljer du åtgärden **Spara som mall**.</span><span class="sxs-lookup"><span data-stu-id="7e19e-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="7e19e-134">Sidan **Kundmall** öppnas och visar kundkortet som mall.</span><span class="sxs-lookup"><span data-stu-id="7e19e-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="7e19e-135">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="7e19e-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7e19e-136">Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="7e19e-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="7e19e-137">Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för kunden.</span><span class="sxs-lookup"><span data-stu-id="7e19e-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="7e19e-138">Ändra eller ange dimensionskoder som ska kopplas till nya kundkort som skapas med hjälp av mallen.</span><span class="sxs-lookup"><span data-stu-id="7e19e-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="7e19e-139">Välj **OK** när du har slutfört den nya kundmallen.</span><span class="sxs-lookup"><span data-stu-id="7e19e-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="7e19e-140">Kundmallen läggs till listan över kundmallar, så att du kan använda det för att skapa nya kundkort.</span><span class="sxs-lookup"><span data-stu-id="7e19e-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="7e19e-141">Ta bort kundkort</span><span class="sxs-lookup"><span data-stu-id="7e19e-141">Deleting customer cards</span></span>

<span data-ttu-id="7e19e-142">Om du har bokfört en transaktion för en kund kan du inte ta bort kortet eftersom transaktionerna kan behövas för revision.</span><span class="sxs-lookup"><span data-stu-id="7e19e-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="7e19e-143">Om du vill ta bort kundkort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.</span><span class="sxs-lookup"><span data-stu-id="7e19e-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e19e-144">Se även</span><span class="sxs-lookup"><span data-stu-id="7e19e-144">See Also</span></span>

[<span data-ttu-id="7e19e-145">Definiera betalningssätt</span><span class="sxs-lookup"><span data-stu-id="7e19e-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="7e19e-146">Slå samman dubblettposter</span><span class="sxs-lookup"><span data-stu-id="7e19e-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="7e19e-147">Skapa nummerserier</span><span class="sxs-lookup"><span data-stu-id="7e19e-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="7e19e-148">Försäljning</span><span class="sxs-lookup"><span data-stu-id="7e19e-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="7e19e-149">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="7e19e-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="7e19e-150">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e19e-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
