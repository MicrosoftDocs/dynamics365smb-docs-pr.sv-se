---
title: Skapa ett leverantörskort för att registrera en ny leverantör | Microsoft Docs
description: Lär dig skapa ett leverantörskort för att registrera en ny leverantör.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772660"
---
# <a name="register-new-vendors"></a><span data-ttu-id="677c3-103">Registrera nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="677c3-103">Register New Vendors</span></span>

<span data-ttu-id="677c3-104">Leverantörer erbjuder produkter som du säljer.</span><span class="sxs-lookup"><span data-stu-id="677c3-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="677c3-105">Varje leverantör som du har köpt av måste registreras som ett leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="677c3-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="677c3-106">Innan du kan registrera nya leverantörer, måste du lägga upp olika inköpskoder som du kan välja mellan, när du fyller i leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="677c3-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="677c3-107">När alla obligatoriska huvuddata skapats kan du konfigurera leverantören ytterligare, till exempel genom att prioritera leverantören i betalningssyfte och upprätta en lista över artiklar som leverantören och andra leverantörer kan tillhandahålla.</span><span class="sxs-lookup"><span data-stu-id="677c3-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="677c3-108">En annan grupp av inställningsuppgifter för leverantörer är att lägga in dina avtal om inköpspris, rabatter och betalning.</span><span class="sxs-lookup"><span data-stu-id="677c3-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="677c3-109">Mer information finns i [Konfigurera inköp](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="677c3-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="677c3-110">Leverantörskort innehåller den information som behövs för att köpa produkter från leverantören.</span><span class="sxs-lookup"><span data-stu-id="677c3-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="677c3-111">Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="677c3-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="677c3-112">Om leverantörsmallar finns för olika leverantörstyper, visas en sida när du skapar ett nytt leverantörskort där du kan välja en lämplig mall.</span><span class="sxs-lookup"><span data-stu-id="677c3-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="677c3-113">Om endast en leverantörsmall finns, då använder nya leverantörskort alltid den mallen.</span><span class="sxs-lookup"><span data-stu-id="677c3-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a><span data-ttu-id="677c3-114">Lägga till nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="677c3-114">Adding new vendors</span></span>

<span data-ttu-id="677c3-115">För att registrera en ny leverantör måste du fylla i ett leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="677c3-115">To register a new vendor, you must fill in a vendor card.</span></span> <span data-ttu-id="677c3-116">Du kan upprätta mallar för olika leverantörsprofiler eller lägga till leverantör utan mallar.</span><span class="sxs-lookup"><span data-stu-id="677c3-116">You can establish templates for different vendor profiles, or you can add vendors without templates.</span></span> <span data-ttu-id="677c3-117">Du kan också skapa en leverantör från en kontakt.</span><span class="sxs-lookup"><span data-stu-id="677c3-117">You can also create a vendor from a contact.</span></span> <span data-ttu-id="677c3-118">Mer information finns i [Att skapa en kund, leverantör, anställd eller bankkonto från en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).</span><span class="sxs-lookup"><span data-stu-id="677c3-118">For more information, see [To create a customer, vendor, employee, or bank account from a contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).</span></span>  

> [!NOTE]  
> <span data-ttu-id="677c3-119">Om leverantörsmallar finns för olika leverantörstyper, visas en sida när du skapar ett nytt leverantörskort där du kan välja en lämplig mall.</span><span class="sxs-lookup"><span data-stu-id="677c3-119">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="677c3-120">Om endast en leverantörsmall finns, då använder nya leverantörskort alltid den mallen.</span><span class="sxs-lookup"><span data-stu-id="677c3-120">If only one vendor template exists, then new vendor cards always use that template.</span></span>  

### <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="677c3-121">Skapa ett nytt leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="677c3-121">To create a new vendor card</span></span>

1. <span data-ttu-id="677c3-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="677c3-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="677c3-123">På sidan **Leverantörer** väljer du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="677c3-123">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="677c3-124">Om fler än en leverantörsmall finns, öppnas en sida där du kan välja leverantörsmall.</span><span class="sxs-lookup"><span data-stu-id="677c3-124">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="677c3-125">I detta fall, följ nästa två steg.</span><span class="sxs-lookup"><span data-stu-id="677c3-125">In that case, follow the next two steps.</span></span>
    1. <span data-ttu-id="677c3-126">Välj den mall som du vill använda för den nya leverantörskortet på sidan **Välj en mall för en ny leverantör**.</span><span class="sxs-lookup"><span data-stu-id="677c3-126">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
    2. <span data-ttu-id="677c3-127">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="677c3-127">Choose the **OK** button.</span></span> <span data-ttu-id="677c3-128">Ett nytt leverantörskort öppnas med några ifyllda fält med information från mallen.</span><span class="sxs-lookup"><span data-stu-id="677c3-128">A new vendor card opens with some fields filled with information from the template.</span></span>
3. <span data-ttu-id="677c3-129">Fortsätt att fylla i eller ändra fält på leverantörskortet vid behov.</span><span class="sxs-lookup"><span data-stu-id="677c3-129">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > <span data-ttu-id="677c3-130">Om du inte vet vilken faktureringsadress som ska användas för respektive faktura från en leverantör fyller du inte i fältet **Leverantörsnr.**.</span><span class="sxs-lookup"><span data-stu-id="677c3-130">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Vendor No.** field.</span></span> <span data-ttu-id="677c3-131">Välj i stället betalningsleverantörens nummer när du har skapat en inköpsoffert, order eller ett inköpshuvud.</span><span class="sxs-lookup"><span data-stu-id="677c3-131">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="677c3-132">Leverantören är nu registrerad, och leverantörskortet är klart att användas i inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="677c3-132">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="677c3-133">Om du vill använda detta leverantörskort som en mall när du skapar nya leverantörskort, så fortsätt med att spara den som en leverantörsmall.</span><span class="sxs-lookup"><span data-stu-id="677c3-133">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="677c3-134">Mer information finns i avsnittet [Så här sparar du leverantörskortet som en mall](#to-save-the-vendor-card-as-a-template).</span><span class="sxs-lookup"><span data-stu-id="677c3-134">For more information, see the [To save the vendor card as a template](#to-save-the-vendor-card-as-a-template) section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="677c3-135">Ta bort leverantörskort</span><span class="sxs-lookup"><span data-stu-id="677c3-135">Deleting vendor cards</span></span>

<span data-ttu-id="677c3-136">Om du har bokfört en transaktion för en leverantör kan du inte ta bort kortet eftersom transaktionerna kan behövas för revision.</span><span class="sxs-lookup"><span data-stu-id="677c3-136">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="677c3-137">Om du vill ta bort leverantörskort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.</span><span class="sxs-lookup"><span data-stu-id="677c3-137">To delete vendor cards with ledger entries, contact your Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="677c3-138">Om du vill spara leverantörskortet som en mall</span><span class="sxs-lookup"><span data-stu-id="677c3-138">To save the vendor card as a template</span></span>

1. <span data-ttu-id="677c3-139">På sidan **Leverantörskort** väljer du åtgärden **Spara som mall**.</span><span class="sxs-lookup"><span data-stu-id="677c3-139">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="677c3-140">Sidan **leverantörsmall** öppnas uppvisar leverantörskortet som mall.</span><span class="sxs-lookup"><span data-stu-id="677c3-140">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="677c3-141">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="677c3-141">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="677c3-142">Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="677c3-142">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="677c3-143">Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för leverantören.</span><span class="sxs-lookup"><span data-stu-id="677c3-143">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="677c3-144">Ändra eller ange dimensionskoder som ska kopplas till nya leverantörskort som skapas med hjälp av mallen.</span><span class="sxs-lookup"><span data-stu-id="677c3-144">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="677c3-145">Välj **OK** när du har slutfört den nya leverantörsmallen.</span><span class="sxs-lookup"><span data-stu-id="677c3-145">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="677c3-146">Leverantörsmallen läggs till listan över leverantörsmallar, så att du kan använda det för att skapa nya leverantörskort.</span><span class="sxs-lookup"><span data-stu-id="677c3-146">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="677c3-147">Se även</span><span class="sxs-lookup"><span data-stu-id="677c3-147">See Also</span></span>

[<span data-ttu-id="677c3-148">Slå samman dubblettposter</span><span class="sxs-lookup"><span data-stu-id="677c3-148">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="677c3-149">Skapa nummerserier</span><span class="sxs-lookup"><span data-stu-id="677c3-149">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="677c3-150">Inköp</span><span class="sxs-lookup"><span data-stu-id="677c3-150">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="677c3-151">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="677c3-151">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="677c3-152">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="677c3-152">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]