---
title: Valfria aktiviteter för att avsluta perioder | Microsoft Docs
description: I det här avsnittet beskrivs de valfria processer och aktiviteter för att avsluta bokföringsperioder i Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 1912a3e1731c2a6a86c5fd5eb93c7e2bf2ff8a1b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313790"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="dfaa5-103">Översikt över uppgifter för att avsluta bokföringsperioder</span><span class="sxs-lookup"><span data-stu-id="dfaa5-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="dfaa5-104">tvingar dig inte att avsluta perioder, men det finns många periodslutsaktiviteter (månadsslut) som du kan göra.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-104">does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="dfaa5-105">I det här avsnittet ges en översikt över valfria processer och aktiviteter för att avsluta perioder.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="dfaa5-106">Redovisning</span><span class="sxs-lookup"><span data-stu-id="dfaa5-106">General Ledger</span></span>
* <span data-ttu-id="dfaa5-107">Specificera intervall för bokföringsdatum som gäller hela systemet och är användarspecifik.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="dfaa5-108">Detta anger datumen som bokföring kan göras i.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="dfaa5-109">Beroende på vilka behov som finns i ditt företag kanske du vill tillåta bokföring i början av perioden eller mot slutet.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="dfaa5-110">Mer information finns [Så här anger du bokföringsperioder](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="dfaa5-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="dfaa5-111">Gör alla nödvändiga redovisningsjusteringar.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="dfaa5-112">Uppdatera och bokför återkommande journaler.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="dfaa5-113">Kör kontouppställningar enligt följande:</span><span class="sxs-lookup"><span data-stu-id="dfaa5-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="dfaa5-114">Öppna sidan **Kontouppställning** och klicka på **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="dfaa5-115">Försäljning</span><span class="sxs-lookup"><span data-stu-id="dfaa5-115">Sales and Receivables</span></span>
* <span data-ttu-id="dfaa5-116">Bokför alla försäljningsorder, fakturor, kreditnotor och returorder.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="dfaa5-117">Bokför alla inbetalningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="dfaa5-118">Uppdatera och bokför återkommande journaler som hör till försäljning- och kundreskontra.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="dfaa5-119">Stäm av kundreskontra i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="dfaa5-120">Kör batch-jobbet **Ta bort fakturerade förs.order**</span><span class="sxs-lookup"><span data-stu-id="dfaa5-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="dfaa5-121">Inköp</span><span class="sxs-lookup"><span data-stu-id="dfaa5-121">Purchases and Payables</span></span>
* <span data-ttu-id="dfaa5-122">Bokför alla inköps order, fakturor, kreditnotor och returorder.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="dfaa5-123">Bokför alla betalningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-123">Post all payment journals.</span></span>  
* <span data-ttu-id="dfaa5-124">Uppdatera och bokför återkommande journaler som relaterar till inköps- och leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="dfaa5-125">Kör rapporten **Lev.skulder - ålder** och stäm av leverantörsskulder i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="dfaa5-126">Kör batch-jobbet **Ta bort fakturerade inköpsorder**</span><span class="sxs-lookup"><span data-stu-id="dfaa5-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="dfaa5-127">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="dfaa5-127">Fixed Assets</span></span>
* <span data-ttu-id="dfaa5-128">Alla underhållskostnader har bokförts via anl.journaler eller fakturor</span><span class="sxs-lookup"><span data-stu-id="dfaa5-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="dfaa5-129">Bokföra justeringar.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-129">Post adjustments.</span></span>
* <span data-ttu-id="dfaa5-130">Bokföra uppskrivning</span><span class="sxs-lookup"><span data-stu-id="dfaa5-130">Post appreciation.</span></span>
* <span data-ttu-id="dfaa5-131">Bokföra avskrivning</span><span class="sxs-lookup"><span data-stu-id="dfaa5-131">Post depreciation.</span></span>
* <span data-ttu-id="dfaa5-132">Uppdatera och bokföra återkommande journal för anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="dfaa5-133">Koncernintern</span><span class="sxs-lookup"><span data-stu-id="dfaa5-133">Intercompany</span></span>
* <span data-ttu-id="dfaa5-134">Behandla koncerninterna transaktioner</span><span class="sxs-lookup"><span data-stu-id="dfaa5-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="dfaa5-135">Beräkna och bearbeta Omsättningsskatt</span><span class="sxs-lookup"><span data-stu-id="dfaa5-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="dfaa5-136">Fyll i skattmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="dfaa5-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dfaa5-137">Se även</span><span class="sxs-lookup"><span data-stu-id="dfaa5-137">See Also</span></span>
[<span data-ttu-id="dfaa5-138">Avsluta år och perioder</span><span class="sxs-lookup"><span data-stu-id="dfaa5-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="dfaa5-139">Avsluta böcker</span><span class="sxs-lookup"><span data-stu-id="dfaa5-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="dfaa5-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dfaa5-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
