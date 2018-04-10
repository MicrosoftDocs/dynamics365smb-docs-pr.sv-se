---
title: Ange fakturaavrundning | Microsoft Docs
description: "Du kan avrunda fakturabelopp när du skapar fakturor. Dessutom kan lokala regler eller lokal praxis kräva att fakturan rundas av på ett visst sätt, till exempel till ett belopp som är delbart med 0,05."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7e140c8c6d31864f6b27f4993e973b42904b0541
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="9e1be-104">Ställa in överavrundning</span><span class="sxs-lookup"><span data-stu-id="9e1be-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="9e1be-105">Om du måste avrunda fakturabelopp när du skapar fakturor, kan du använda funktionen för automatisk avrundning.</span><span class="sxs-lookup"><span data-stu-id="9e1be-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="9e1be-106">När en faktura rundas av infogas en extra rad med avrundningsbeloppet och bokförs tillsammans med övriga fakturarader.</span><span class="sxs-lookup"><span data-stu-id="9e1be-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="9e1be-107">Lokala regler eller lokal praxis kanske kräver att fakturan rundas av på ett visst sätt, till exempel till ett belopp som är delbart med 0,05.</span><span class="sxs-lookup"><span data-stu-id="9e1be-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  
  
<span data-ttu-id="9e1be-108">För att kunna använda den automatiska fakturaavrundningen måste du:</span><span class="sxs-lookup"><span data-stu-id="9e1be-108">To use automatic invoice rounding, you must:</span></span>  
  
* <span data-ttu-id="9e1be-109">ange vilka redovisningskonton som differenserna ska bokföras på.</span><span class="sxs-lookup"><span data-stu-id="9e1be-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="9e1be-110">ange regler för fakturaavrundning i lokal valuta och i utländsk valuta.</span><span class="sxs-lookup"><span data-stu-id="9e1be-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="9e1be-111">aktivera funktionen.</span><span class="sxs-lookup"><span data-stu-id="9e1be-111">Activate the function.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="9e1be-112">Förutom fakturaavrundningsfunktionen kan belopp på fakturor rundas av med funktionerna A-pris avrundning och Belopp avrundning.</span><span class="sxs-lookup"><span data-stu-id="9e1be-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="9e1be-113">Så här skapar du redovisningskonton för avrundningsdifferenser av fakturor</span><span class="sxs-lookup"><span data-stu-id="9e1be-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="9e1be-114">Om du vill använda programmets funktion för automatisk avrundning av fakturabelopp måste du först upprätta redovisningskonton eller konton där avrundningsskillnaderna bokförs.</span><span class="sxs-lookup"><span data-stu-id="9e1be-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="9e1be-115">Innan du kan göra detta måste du definiera produktbokföringsmallar för moms.</span><span class="sxs-lookup"><span data-stu-id="9e1be-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="9e1be-116">Mer information finns i [Ange moms](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="9e1be-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="9e1be-117">Så här skapar du redovisningskonton för avrundningsdifferenser av fakturor</span><span class="sxs-lookup"><span data-stu-id="9e1be-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="9e1be-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9e1be-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e1be-119">På sidan **Kontoplan** ställer du in kontot och kallar det för **Faktura avrundning** eller något liknande.</span><span class="sxs-lookup"><span data-stu-id="9e1be-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9e1be-120"> använder kontonamnet som text för de fakturor som avrundas.</span><span class="sxs-lookup"><span data-stu-id="9e1be-120"> will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="9e1be-121">Beroende på om du använder moms eller omsättningsskatt väljer du i fälten **Omsättn. skatt produktbokföringsmall** eller **Moms produktbokföringsmal** och väljer en bokföringsmall för avrundade belopp.</span><span class="sxs-lookup"><span data-stu-id="9e1be-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="9e1be-122">Du vill kanske skapa en ny gruppkod som kan användas för fakturaavrundning.</span><span class="sxs-lookup"><span data-stu-id="9e1be-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="9e1be-123">Lämna fälten **Typ av bokföring**, och antingen **Omsättn. skatt rörelsebokföringsmall** eller **Moms rörelsebokföringsmall** tomma.</span><span class="sxs-lookup"><span data-stu-id="9e1be-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
<span data-ttu-id="9e1be-124">Nu kan du koppla fakturaavrundningskontot till bokföringsmallar på sidan **Leverantörsbokföringsmallar**.</span><span class="sxs-lookup"><span data-stu-id="9e1be-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="9e1be-125">Så här anger du avrundningsregler för utländska valutor</span><span class="sxs-lookup"><span data-stu-id="9e1be-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="9e1be-126">Innan du kan använda den automatiska fakturaavrundningsfunktionenmåste du ställa in avrundningsregler för utländsk och lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="9e1be-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="9e1be-127">Så här anger du avrundningsregler för utländska valutor:</span><span class="sxs-lookup"><span data-stu-id="9e1be-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="9e1be-128">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Valutor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9e1be-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e1be-129">På sidan **valutor** väljer du valutan för att öppna **valutakort**, och fyller sedan i fälten **Belopp avrundning**, **A-pris avrundning**, **Faktura avrundning** och **Avrundningstyp**.</span><span class="sxs-lookup"><span data-stu-id="9e1be-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>
  
### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="9e1be-130">Så här anger du avrundningsregler för den lokala valutan:</span><span class="sxs-lookup"><span data-stu-id="9e1be-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="9e1be-131">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9e1be-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e1be-132">På sidan **Redovisningsinställningar** på snabbfliken **Allmänt** fyller du i fälten **Faktura avrundning** och **Avrundningstyp**.</span><span class="sxs-lookup"><span data-stu-id="9e1be-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="9e1be-133">Så här aktiverar du funktionen Avrunda fakturabelopp</span><span class="sxs-lookup"><span data-stu-id="9e1be-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="9e1be-134">För att se till att försäljnings- och inköpsfakturor avrundas automatiskt aktiverar du funktionen Avrunda fakturabelopp.</span><span class="sxs-lookup"><span data-stu-id="9e1be-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="9e1be-135">Du kan aktivera fakturaavrundningen separat för försäljnings- och inköpsfakturor.</span><span class="sxs-lookup"><span data-stu-id="9e1be-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="9e1be-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsinställningar** eller **Inköpsinställningar** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9e1be-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e1be-137">På snabbfliken **Allmänt**, välj kryssrutan **Öresutjämning**.</span><span class="sxs-lookup"><span data-stu-id="9e1be-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e1be-138">Se även</span><span class="sxs-lookup"><span data-stu-id="9e1be-138">See Also</span></span>  
[<span data-ttu-id="9e1be-139">Fakturaförsäljning</span><span class="sxs-lookup"><span data-stu-id="9e1be-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="9e1be-140">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="9e1be-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)