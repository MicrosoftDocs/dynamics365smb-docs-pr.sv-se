---
title: "Valfria aktiviteter för att avsluta perioder | Microsoft Docs"
description: "I det här avsnittet beskrivs valfria processer och aktiviteter för att avsluta bokföringsperioder i Finance and Operations, Business edition."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 344e294083813d41b415ad07e6e8acdd3fe5047b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="e32e8-103">Översikt över uppgifter för att avsluta bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="e32e8-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e32e8-104"> tvingar dig inte att avsluta perioder, men det finns många periodslutsaktiviteter (månadsslut) som du kan göra.</span><span class="sxs-lookup"><span data-stu-id="e32e8-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="e32e8-105">I det här avsnittet ges en översikt över valfria processer och aktiviteter för att avsluta perioder.</span><span class="sxs-lookup"><span data-stu-id="e32e8-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="e32e8-106">Redovisning</span><span class="sxs-lookup"><span data-stu-id="e32e8-106">General Ledger</span></span>
* <span data-ttu-id="e32e8-107">Specificera intervall för bokföringsdatum som gäller hela systemet och är användarspecifik.</span><span class="sxs-lookup"><span data-stu-id="e32e8-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="e32e8-108">Detta anger datumen som bokföring kan göras i.</span><span class="sxs-lookup"><span data-stu-id="e32e8-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="e32e8-109">Beroende på vilka behov som finns i ditt företag kanske du vill tillåta bokföring i början av perioden eller mot slutet.</span><span class="sxs-lookup"><span data-stu-id="e32e8-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="e32e8-110">Mer information finns [Så här anger du bokföringsperioder](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="e32e8-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="e32e8-111">Gör alla nödvändiga redovisningsjusteringar.</span><span class="sxs-lookup"><span data-stu-id="e32e8-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="e32e8-112">Uppdatera och bokför återkommande journaler.</span><span class="sxs-lookup"><span data-stu-id="e32e8-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="e32e8-113">Kör kontouppställningar enligt följande:</span><span class="sxs-lookup"><span data-stu-id="e32e8-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="e32e8-114">Öppna fönstret **Kontouppställning** och klicka på **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="e32e8-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="e32e8-115">Försäljning</span><span class="sxs-lookup"><span data-stu-id="e32e8-115">Sales and Receivables</span></span>
* <span data-ttu-id="e32e8-116">Bokför alla försäljningsorder, fakturor, kreditnotor och returorder.</span><span class="sxs-lookup"><span data-stu-id="e32e8-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="e32e8-117">Bokför alla inbetalningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="e32e8-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="e32e8-118">Uppdatera och bokför återkommande journaler som hör till försäljning- och kundreskontra.</span><span class="sxs-lookup"><span data-stu-id="e32e8-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="e32e8-119">Stäm av kundreskontra i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e32e8-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="e32e8-120">Kör batch-jobbet **Ta bort fakturerade förs.order**</span><span class="sxs-lookup"><span data-stu-id="e32e8-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="e32e8-121">Inköp</span><span class="sxs-lookup"><span data-stu-id="e32e8-121">Purchases and Payables</span></span>
* <span data-ttu-id="e32e8-122">Bokför alla inköps order, fakturor, kreditnotor och returorder.</span><span class="sxs-lookup"><span data-stu-id="e32e8-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="e32e8-123">Bokför alla betalningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="e32e8-123">Post all payment journals.</span></span>  
* <span data-ttu-id="e32e8-124">Uppdatera och bokför återkommande journaler som relaterar till inköps- och leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="e32e8-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="e32e8-125">Kör rapporten **Lev.skulder - ålder** och stäm av leverantörsskulder i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e32e8-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="e32e8-126">Kör batch-jobbet **Ta bort fakturerade inköpsorder**</span><span class="sxs-lookup"><span data-stu-id="e32e8-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="e32e8-127">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="e32e8-127">Fixed Assets</span></span>
* <span data-ttu-id="e32e8-128">Alla underhållskostnader har bokförts via anl.journaler eller fakturor</span><span class="sxs-lookup"><span data-stu-id="e32e8-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="e32e8-129">Bokföra justeringar.</span><span class="sxs-lookup"><span data-stu-id="e32e8-129">Post adjustments.</span></span>
* <span data-ttu-id="e32e8-130">Bokföra uppskrivning</span><span class="sxs-lookup"><span data-stu-id="e32e8-130">Post appreciation.</span></span>
* <span data-ttu-id="e32e8-131">Bokföra avskrivning</span><span class="sxs-lookup"><span data-stu-id="e32e8-131">Post depreciation.</span></span>
* <span data-ttu-id="e32e8-132">Uppdatera och bokföra återkommande journal för anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="e32e8-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="e32e8-133">Koncernintern</span><span class="sxs-lookup"><span data-stu-id="e32e8-133">Intercompany</span></span>
* <span data-ttu-id="e32e8-134">Behandla koncerninterna transaktioner</span><span class="sxs-lookup"><span data-stu-id="e32e8-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="e32e8-135">Beräkna och bearbeta Omsättningsskatt</span><span class="sxs-lookup"><span data-stu-id="e32e8-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="e32e8-136">Fyll i skattmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="e32e8-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e32e8-137">Se även</span><span class="sxs-lookup"><span data-stu-id="e32e8-137">See Also</span></span>
[<span data-ttu-id="e32e8-138">Avsluta år och perioder</span><span class="sxs-lookup"><span data-stu-id="e32e8-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="e32e8-139">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="e32e8-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="e32e8-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e32e8-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

