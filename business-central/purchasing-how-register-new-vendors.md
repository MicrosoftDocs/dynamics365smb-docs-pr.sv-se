---
title: Skapa ett leverantörskort för att registrera en ny leverantör | Microsoft Docs
description: Lär dig skapa ett leverantörskort för att registrera en ny leverantör.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e780967fda8e5c4e8b3a1f2e5e3ed3a05418507d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191049"
---
# <a name="register-new-vendors"></a><span data-ttu-id="ceb90-103">Registrera nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="ceb90-103">Register New Vendors</span></span>
<span data-ttu-id="ceb90-104">Leverantörer erbjuder produkter som du säljer.</span><span class="sxs-lookup"><span data-stu-id="ceb90-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="ceb90-105">Varje leverantör som du har köpt av måste registreras som ett leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="ceb90-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="ceb90-106">Innan du kan registrera nya leverantörer, måste du lägga upp olika inköpskoder som du kan välja mellan, när du fyller i leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="ceb90-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="ceb90-107">När alla obligatoriska huvuddata skapats kan du konfigurera leverantören ytterligare, till exempel genom att prioritera leverantören i betalningssyfte och upprätta en lista över artiklar som leverantören och andra leverantörer kan tillhandahålla.</span><span class="sxs-lookup"><span data-stu-id="ceb90-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="ceb90-108">En annan grupp av inställningsuppgifter för leverantörer är att lägga in dina avtal om inköpspris, rabatter och betalning.</span><span class="sxs-lookup"><span data-stu-id="ceb90-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="ceb90-109">Mer information finns i [Konfigurera inköp](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="ceb90-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="ceb90-110">Leverantörskort innehåller den information som behövs för att köpa produkter från leverantören.</span><span class="sxs-lookup"><span data-stu-id="ceb90-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="ceb90-111">Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="ceb90-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="ceb90-112">Om leverantörsmallar finns för olika leverantörstyper, visas en sida när du skapar ett nytt leverantörskort där du kan välja en lämplig mall.</span><span class="sxs-lookup"><span data-stu-id="ceb90-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="ceb90-113">Om endast en leverantörsmall finns, då använder nya leverantörskort alltid den mallen.</span><span class="sxs-lookup"><span data-stu-id="ceb90-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="ceb90-114">Skapa ett nytt leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="ceb90-114">To create a new vendor card</span></span>
1. <span data-ttu-id="ceb90-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ceb90-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ceb90-116">På sidan **Leverantörer** väljer du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ceb90-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="ceb90-117">Om fler än en leverantörsmall finns, öppnas en sida där du kan välja leverantörsmall.</span><span class="sxs-lookup"><span data-stu-id="ceb90-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="ceb90-118">I detta fall, följ nästa två steg.</span><span class="sxs-lookup"><span data-stu-id="ceb90-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="ceb90-119">Välj den mall som du vill använda för den nya leverantörskortet på sidan **Välj en mall för en ny leverantör**.</span><span class="sxs-lookup"><span data-stu-id="ceb90-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="ceb90-120">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="ceb90-120">Choose the **OK** button.</span></span> <span data-ttu-id="ceb90-121">Ett nytt leverantörskort öppnas med några ifyllda fält med information från mallen.</span><span class="sxs-lookup"><span data-stu-id="ceb90-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="ceb90-122">Fortsätt att fylla i eller ändra fält på leverantörskortet vid behov.</span><span class="sxs-lookup"><span data-stu-id="ceb90-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="ceb90-123">Om du inte känner till den faktureringsadress som kommer att användas för alla fakturor från en leverantör fyller du inte i fältet **Betalningsleverantörsnr**.</span><span class="sxs-lookup"><span data-stu-id="ceb90-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="ceb90-124">Välj i stället betalningsleverantörens nummer när du har skapat en inköpsoffert, order eller ett inköpshuvud.</span><span class="sxs-lookup"><span data-stu-id="ceb90-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="ceb90-125">Leverantören är nu registrerad, och leverantörskortet är klart att användas i inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="ceb90-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="ceb90-126">Om du vill använda detta leverantörskort som en mall när du skapar nya leverantörskort, så fortsätt med att spara den som en leverantörsmall.</span><span class="sxs-lookup"><span data-stu-id="ceb90-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="ceb90-127">Mer information finns i följande avsnitt:</span><span class="sxs-lookup"><span data-stu-id="ceb90-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="ceb90-128">Om du vill spara leverantörskortet som en mall</span><span class="sxs-lookup"><span data-stu-id="ceb90-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="ceb90-129">På sidan **Leverantörskort** väljer du åtgärden **Spara som mall**.</span><span class="sxs-lookup"><span data-stu-id="ceb90-129">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="ceb90-130">Sidan **leverantörsmall** öppnas uppvisar leverantörskortet som mall.</span><span class="sxs-lookup"><span data-stu-id="ceb90-130">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="ceb90-131">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="ceb90-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ceb90-132">Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="ceb90-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="ceb90-133">Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för leverantören.</span><span class="sxs-lookup"><span data-stu-id="ceb90-133">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="ceb90-134">Ändra eller ange dimensionskoder som ska kopplas till nya leverantörskort som skapas med hjälp av mallen.</span><span class="sxs-lookup"><span data-stu-id="ceb90-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="ceb90-135">Välj **OK** när du har slutfört den nya leverantörsmallen.</span><span class="sxs-lookup"><span data-stu-id="ceb90-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="ceb90-136">Leverantörsmallen läggs till listan över leverantörsmallar, så att du kan använda det för att skapa nya leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="ceb90-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="ceb90-137">Se även</span><span class="sxs-lookup"><span data-stu-id="ceb90-137">See Also</span></span>
[<span data-ttu-id="ceb90-138">Slå samman dubblettposter</span><span class="sxs-lookup"><span data-stu-id="ceb90-138">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="ceb90-139">Skapa nummerserier</span><span class="sxs-lookup"><span data-stu-id="ceb90-139">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="ceb90-140">Inköp</span><span class="sxs-lookup"><span data-stu-id="ceb90-140">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ceb90-141">[Registrera inköp](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="ceb90-141">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="ceb90-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ceb90-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
