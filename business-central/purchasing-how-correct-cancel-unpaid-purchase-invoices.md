---
title: "Korrigera eller annullera obetalda inköpsfakturor | Microsoft Docs"
description: "Förklarar hur du kan korrigera, avbryta eller ångra en bokförd inköpsfaktura eller skapa en inköpskreditnota automatiskt."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7d5b59d15304a497dc4f3c35ac1d19dcd491aaed
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="e14b3-103">Korrigera eller annullera obetalda inköpsfakturor</span><span class="sxs-lookup"><span data-stu-id="e14b3-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="e14b3-104">Du kan korrigera eller annullera en bokförd inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e14b3-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="e14b3-105">Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen.</span><span class="sxs-lookup"><span data-stu-id="e14b3-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="e14b3-106">Om du redan har betalt för produkter på den bokförda inköpsfakturan kan du inte rätta eller annullera den från själva den bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="e14b3-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="e14b3-107">I stället måste du skapa en inköpskreditnota manuellt för att återföra inköpet, alternaivt hanterat med en inköpsreturorder.</span><span class="sxs-lookup"><span data-stu-id="e14b3-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="e14b3-108">Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="e14b3-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="e14b3-109">I fönstret **Bokförd inköpsfaktura** kan du välja knappen **Korrigera** eller knappen **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="e14b3-109">In the **Posted Purchase Invoice** window, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="e14b3-110">När du uppdaterar eller avbryter en bokförd inköpsfaktura gäller den korrigerande inköpskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga inköpsfakturan bokfördes.</span><span class="sxs-lookup"><span data-stu-id="e14b3-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="e14b3-111">Det återför den bokförda inköpsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av inköpskreditnota för din verifieringskedja.</span><span class="sxs-lookup"><span data-stu-id="e14b3-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="e14b3-112">I det följande beskrivs användningen av **Korrigera** och **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="e14b3-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="e14b3-113">Korrigera en bokförd inköpsfaktura</span><span class="sxs-lookup"><span data-stu-id="e14b3-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="e14b3-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e14b3-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e14b3-115">Markera den bokförda inköpsfakturan som du vill korrigera.</span><span class="sxs-lookup"><span data-stu-id="e14b3-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="e14b3-116">Om kryssrutan **Avbruten** kan du inte rätta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.</span><span class="sxs-lookup"><span data-stu-id="e14b3-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="e14b3-117">I fönstret **Bokförd inköpsfaktura** väljer du **korrigera**.</span><span class="sxs-lookup"><span data-stu-id="e14b3-117">In the **Posted Purchase Invoice** window, choose **Correct**.</span></span>

    <span data-ttu-id="e14b3-118">En ny inköpsfaktura med samma information skapas där du kan göra rättningen.</span><span class="sxs-lookup"><span data-stu-id="e14b3-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="e14b3-119">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="e14b3-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="e14b3-120">Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e14b3-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="e14b3-121">En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="e14b3-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="e14b3-122">Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="e14b3-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="e14b3-123">Avbryta en bokförd inköpsfaktura</span><span class="sxs-lookup"><span data-stu-id="e14b3-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="e14b3-124">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e14b3-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e14b3-125">Markera den bokförda inköpsfakturan som du vill annullera.</span><span class="sxs-lookup"><span data-stu-id="e14b3-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="e14b3-126">Om kryssrutan **Avbruten** kan du inte avbryta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.</span><span class="sxs-lookup"><span data-stu-id="e14b3-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="e14b3-127">I fönstret **Bokförd inköpsfaktura** väljer du **avbryt**.</span><span class="sxs-lookup"><span data-stu-id="e14b3-127">In the **Posted Purchase Invoice** window, choose **Cancel**.</span></span>

    <span data-ttu-id="e14b3-128">En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="e14b3-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="e14b3-129">Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e14b3-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="e14b3-130">Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="e14b3-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="e14b3-131">Se även</span><span class="sxs-lookup"><span data-stu-id="e14b3-131">See Also</span></span>
[<span data-ttu-id="e14b3-132">Inköp</span><span class="sxs-lookup"><span data-stu-id="e14b3-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e14b3-133">Registrera inköp</span><span class="sxs-lookup"><span data-stu-id="e14b3-133">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="e14b3-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e14b3-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
