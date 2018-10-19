---
title: "Konfigurerar standardrader för återkommande försäljning och inköp | Microsoft Docs"
description: "Du kan definiera försäljningsrader och inköpsrader som du gör ofta och infoga dem på försäljnings- och inköpsdokument för att snabbt fylla i raderna med standardinformationen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="26fef-103">Skapa återkommande försäljnings- och inköpsrader</span><span class="sxs-lookup"><span data-stu-id="26fef-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="26fef-104">Om du ofta behöver skapa försäljnings- och inköpsrader med liknande information, kan du ställa in standardraderna så att du sedan kan infoga på återkommande försäljning och inköpsdokument, till exempel för återkommande påfyllningsorder.</span><span class="sxs-lookup"><span data-stu-id="26fef-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="26fef-105">I följande procedur beskrivs hur du arbetar med in standardförsäljningsrader.</span><span class="sxs-lookup"><span data-stu-id="26fef-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="26fef-106">Det fungerar på liknande sätt för standardstandardinköpsrader.</span><span class="sxs-lookup"><span data-stu-id="26fef-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="26fef-107">Så här skapar du standardförsäljningsrader</span><span class="sxs-lookup"><span data-stu-id="26fef-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="26fef-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Standard förs.rader** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26fef-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="26fef-109">I fönstret **Standard förs.rader** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="26fef-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="26fef-110">I snabbfliken **Allmänt** fyller du i nödvändiga fält.</span><span class="sxs-lookup"><span data-stu-id="26fef-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="26fef-111">I snabbfliken **Rader** ange information i fälten för att förbereda försäljningsrader som återspeglar de standardrader som du förväntar dig att använda som återkommande rader på försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="26fef-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="26fef-112">Infoga standardförsäljningsrader i en försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="26fef-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="26fef-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Fakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26fef-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="26fef-114">Öppna den försäljningsfaktura du vill infoga en eller flera standardförsäljningsrader på.</span><span class="sxs-lookup"><span data-stu-id="26fef-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="26fef-115">Välj åtgärden **få återkommande förs.rader**.</span><span class="sxs-lookup"><span data-stu-id="26fef-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="26fef-116">I fönstret **återkommande försäljningsrader** välj sökknappen i fältet **kod** och välj sedan en uppsättning standardförsäljningsrader.</span><span class="sxs-lookup"><span data-stu-id="26fef-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="26fef-117">För att använda återkommande rader tillsammans med batch-jobbet **Skapa återkommande fakturor** måste du även fylla i fälten **Giltigt från den** och **Giltigt till den** fönstret **återkommande försäljningsrader**.</span><span class="sxs-lookup"><span data-stu-id="26fef-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="26fef-118">För mer information, se Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder.</span><span class="sxs-lookup"><span data-stu-id="26fef-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="26fef-119">Välj **OK** för att infoga standardförsäljningsraderna på fakturan, där du kan använda eller redigera informationen.</span><span class="sxs-lookup"><span data-stu-id="26fef-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="26fef-120">Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder</span><span class="sxs-lookup"><span data-stu-id="26fef-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="26fef-121">Du kan använda batch-jobbet **Skapa återkommande försäljningsfakt.** för att skapa försäljningsfakturor enligt standardförsäljningsrader som tilldelats till kunderna och med bokföringsdatum som infaller inom de giltighetsdatum som du anger på standardförsäljningsraden.</span><span class="sxs-lookup"><span data-stu-id="26fef-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="26fef-122">I fönstret **Återkommande försäljningsrader** kan du också ange en metod för autogirobetalning och medgivande för autogiro.</span><span class="sxs-lookup"><span data-stu-id="26fef-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="26fef-123">De försäljningsfakturor som skapas med batch-jobbet **Skapa återkommande försäljningsfakt.** tar sedan med information som krävs för att kräva betalning för försäljningsfakturorna med SEPA-autogiro.</span><span class="sxs-lookup"><span data-stu-id="26fef-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="26fef-124">Mer information finns i [Kräva in betalningar med SEPA direktdebitering](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="26fef-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="26fef-125">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Skapa återkommande försäljningsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26fef-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="26fef-126">I fönstret **Skapa återkommande försäljningsfakt.** fyller du i de fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="26fef-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="26fef-127">I fältet **kod**filter anger du koden för standardförsäljningsrader som tilldelats kunden som du vill skapa fakturor för.</span><span class="sxs-lookup"><span data-stu-id="26fef-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="26fef-128">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="26fef-128">Choose the **OK** button.</span></span>

<span data-ttu-id="26fef-129">Fakturor skapas för kunder med den angivna standardkundförs.koden och angiven information om direktdebitering, för bokföring på det angivna datumet.</span><span class="sxs-lookup"><span data-stu-id="26fef-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="26fef-130">Se även</span><span class="sxs-lookup"><span data-stu-id="26fef-130">See Also</span></span>  
[<span data-ttu-id="26fef-131">Försäljning</span><span class="sxs-lookup"><span data-stu-id="26fef-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="26fef-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26fef-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

