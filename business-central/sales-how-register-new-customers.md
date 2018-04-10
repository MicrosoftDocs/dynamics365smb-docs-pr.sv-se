---
title: "Skapa ett kundkort för att registrera en ny kund | Microsoft Docs"
description: "Beskriver hur du skapar ett kundkort för att registrera information om varje ny kund eller klienten som du säljer till."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: 6ca938a5bcd0fd160c98358d89740e4dfd756e79
ms.contentlocale: sv-se
ms.lasthandoff: 03/28/2018

---
# <a name="register-new-customers"></a><span data-ttu-id="153fc-103">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="153fc-103">Register New Customers</span></span>
<span data-ttu-id="153fc-104">Kunderna är källan till din inkomst.</span><span class="sxs-lookup"><span data-stu-id="153fc-104">Customers are the source of your income.</span></span> <span data-ttu-id="153fc-105">Du måste registrera varje kund som du säljer till som ett kundkort.</span><span class="sxs-lookup"><span data-stu-id="153fc-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="153fc-106">Kundkort innehåller den information som behövs för att sälja produkter till kunden.</span><span class="sxs-lookup"><span data-stu-id="153fc-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="153fc-107">Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="153fc-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="153fc-108">Innan du kan registrera nya kunder, måste du lägga upp olika försäljningskoder som du kan välja mellan, när du fyller i kundkort.</span><span class="sxs-lookup"><span data-stu-id="153fc-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="153fc-109">Mer information finns i [Konfigurera försäljning](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="153fc-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="153fc-110">Om kundmallar finns för olika kundtyper, visas ett fönster när du skapar ett nytt kundkort där du kan välja en lämplig mall.</span><span class="sxs-lookup"><span data-stu-id="153fc-110">If customer templates exist for different customer types, then a window appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="153fc-111">Om endast en kundmall finns, då använder nya kundkort alltid den mallen.</span><span class="sxs-lookup"><span data-stu-id="153fc-111">If only one customer template exists, then new customer cards always use that template.</span></span>

## <a name="to-create-a-new-customer-card"></a><span data-ttu-id="153fc-112">SÅ här skapar du ett nytt kundkort</span><span class="sxs-lookup"><span data-stu-id="153fc-112">To create a new customer card</span></span>
1. <span data-ttu-id="153fc-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="153fc-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="153fc-114">I fönstret **Kunder** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="153fc-114">In the **Customers** window, choose the **New** action.</span></span>

    <span data-ttu-id="153fc-115">Om endast en kundmall finns, då öppnas ett nytt kundkort med fält ifyllda med information från mallen.</span><span class="sxs-lookup"><span data-stu-id="153fc-115">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="153fc-116">Om fler än en kundmall finns, öppnas ett fönster där du kan välja kundmall.</span><span class="sxs-lookup"><span data-stu-id="153fc-116">If more than one customer template exists, then a window opens from which you can select a customer template.</span></span> <span data-ttu-id="153fc-117">I detta fall, följ nästa två steg.</span><span class="sxs-lookup"><span data-stu-id="153fc-117">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="153fc-118">Välj den mall som du vill använda för det nya kundkortet i fönstret **Välj en mall för en ny kund**.</span><span class="sxs-lookup"><span data-stu-id="153fc-118">In the **Select a template for a new customer** window, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="153fc-119">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="153fc-119">Choose the **OK** button.</span></span> <span data-ttu-id="153fc-120">Ett nytt kundkort öppnas med ifyllda fält med information från mallen.</span><span class="sxs-lookup"><span data-stu-id="153fc-120">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="153fc-121">Fortsätt att fylla i eller ändra fält på kundkortet vid behov.</span><span class="sxs-lookup"><span data-stu-id="153fc-121">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="153fc-122">På snabbfliken **Försäljningspriser** ser du specialpriser eller rabatter som du beviljar för kunden om vissa villkor uppfylls, till exempel artikel, lägsta partistorlek eller slutdatum.</span><span class="sxs-lookup"><span data-stu-id="153fc-122">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="153fc-123">Varje rad representerar ett speciellt pris eller radrabatt.</span><span class="sxs-lookup"><span data-stu-id="153fc-123">Each row represents a special price or line discount.</span></span> <span data-ttu-id="153fc-124">Varje kolumn representerar ett kriterium som måste gälla för att garantera specialpriset som du anger i fältet **Enhetspris** eller radrabatten som du anger i fältet **Radrabatt %**.</span><span class="sxs-lookup"><span data-stu-id="153fc-124">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="153fc-125">Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="153fc-125">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="153fc-126">Kunden är nu registrerad, och kundkortet är klart att användas i försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="153fc-126">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="153fc-127">Om du vill använda detta kundkort som en mall när du skapar nya kundkort, så fortsätt med att spara den som en mall.</span><span class="sxs-lookup"><span data-stu-id="153fc-127">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="153fc-128">Mer information finns i följande avsnitt:</span><span class="sxs-lookup"><span data-stu-id="153fc-128">For more information, see the following section.</span></span>

## <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="153fc-129">Om du vill spara kundkortet som en mall</span><span class="sxs-lookup"><span data-stu-id="153fc-129">To save the customer card as a template</span></span>
1. <span data-ttu-id="153fc-130">I fönstret **kundkort** väljer du åtgärden **Spara som mall**.</span><span class="sxs-lookup"><span data-stu-id="153fc-130">In the **Customer Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="153fc-131">Fönstret **Kundmall** öppnas och visar kundkortet som mall.</span><span class="sxs-lookup"><span data-stu-id="153fc-131">The **Customer Template** window opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="153fc-132">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="153fc-132">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="153fc-133">Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="153fc-133">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="153fc-134">Fönstret **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för kunden.</span><span class="sxs-lookup"><span data-stu-id="153fc-134">The **Dimension Templates** window opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="153fc-135">Ändra eller ange dimensionskoder som ska kopplas till nya kundkort som skapas med hjälp av mallen.</span><span class="sxs-lookup"><span data-stu-id="153fc-135">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="153fc-136">Välj **OK** när du har slutfört den nya kundmallen.</span><span class="sxs-lookup"><span data-stu-id="153fc-136">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="153fc-137">Kundmallen läggs till listan över kundmallar, så att du kan använda det för att skapa nya kundkort.</span><span class="sxs-lookup"><span data-stu-id="153fc-137">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="153fc-138">Se även</span><span class="sxs-lookup"><span data-stu-id="153fc-138">See Also</span></span>
[<span data-ttu-id="153fc-139">Skapa nummerserier</span><span class="sxs-lookup"><span data-stu-id="153fc-139">Create Number Series</span></span>](ui-create-number-series.md)  
<span data-ttu-id="153fc-140">[Försäljning](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="153fc-140">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="153fc-141">[Konfigurera försäljning](sales-setup-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="153fc-141">[Setting Up Sales](sales-setup-sales.md)  </span></span>  
<span data-ttu-id="153fc-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="153fc-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

