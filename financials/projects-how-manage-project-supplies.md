---
title: "Köpa artiklar eller tjänster för ett projekt och hantera leveranser | Microsoft Docs"
description: "Beskriver hur du hanterar försörjning och inköp av material och tjänster för projekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 46cae53022ba5d65a370694c9818f52a7bf45525
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-job-supplies"></a><span data-ttu-id="dd6c5-103">Så här hanterar du projektleveranser</span><span class="sxs-lookup"><span data-stu-id="dd6c5-103">How to: Manage Job Supplies</span></span>
<span data-ttu-id="dd6c5-104">Att hantera projektleveranser av artiklar, tjänster och utgifter är en viktig del och aspekt av allt projektgenomförande.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="dd6c5-105">Du kan använda lagerantal eller göra projektspecifika inköp med hjälp av inköpsorder eller inköpsfakturor.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="dd6c5-106">Ett servicejobb för en dator kan till exempel kräva en ny hårddisk.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="dd6c5-107">Du skapar då en inköpsfaktura för att köpa en ny hårddisk och registrerar det i projektet.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="dd6c5-108">Om inköpsprocessen inte kräver att den fysiska transaktionen registreras separat kan ett inköp registreras endast i en inköpsfaktura eller i fönstret **Projektredovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="dd6c5-109">Mer information finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="dd6c5-109">For more information, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="dd6c5-110">Köpa artiklar eller tjänster till ett projekt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-110">To purchase items or services for a job</span></span>
<span data-ttu-id="dd6c5-111">Efterföljande procedur visar hur du använder en inköpsfaktura för att köpa produkter till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="dd6c5-112">Samma steg gäller när du använder en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="dd6c5-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dd6c5-114">Välj åtgärden **Ny** och fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="dd6c5-115">Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="dd6c5-115">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="dd6c5-116">I fälten **Projektnr.** och **Projektaktivitetsnr.** väljer du informationen för det projekt som du vill köpa artiklar eller tjänster för.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="dd6c5-117">Använd funktionen **Välj kolumner** om fältet inte visas.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="dd6c5-118">Mer information finns i [Användaranpassning](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="dd6c5-118">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

    <span data-ttu-id="dd6c5-119">Värdet som du väljer i fältet **Projektradtyp** definierar om en planeringsrad skapas när du bokför artikelförbrukningen.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="dd6c5-120">Om fältet innehåller **Fakturerbart** skapas projektplaneringsrader som är klara att faktureras till kunden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="dd6c5-121">Mer information finns i [Så här skapar du fakturaprojekt](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="dd6c5-121">For more information, see [How to: Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="dd6c5-122">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="dd6c5-123">Visa värdet på inköp till ett projekt</span><span class="sxs-lookup"><span data-stu-id="dd6c5-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="dd6c5-124">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="dd6c5-125">Öppna ett relevant projektkort.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-125">Open a relevant job card.</span></span>

    <span data-ttu-id="dd6c5-126">På snabbfliken **Uppgifter** visar fältet **Utestående order** det totala utestående beloppet, i lokal valuta, för lagerartiklar och tjänster för inköpsdokument för projektaktivitetsraden.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="dd6c5-127">Fältet **Inlevererat bel. ej faktrd** visar värdet för artiklarna som har levererats på inköpsdokument, men ännu inte har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="dd6c5-128">Välj något av fälten för att öppna fönstret **Inköpsrader** där du kan granska information om relaterade inköpsdokumentrader, bland annat vilka artiklar eller tjänster som har inlevererats.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-128">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="dd6c5-129">Så här bokför du en projektrelaterad utgift</span><span class="sxs-lookup"><span data-stu-id="dd6c5-129">To post a job-related expense</span></span>
<span data-ttu-id="dd6c5-130">Om du ådrar dig extraordinära eller engångsutgifter för projekt kan du använda fönstret **Projektredovisningsjournal** för att bokföra dem direkt till det relevanta projektkontot.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="dd6c5-131">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projektredovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dd6c5-132">Skapa en ny rad och registrera information om utgiften, bland annat information i fälten **Projektnr** och **Projektaktivitetsnr**.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="dd6c5-133">När journalen är slutförd väljer du åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="dd6c5-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd6c5-134">Se även</span><span class="sxs-lookup"><span data-stu-id="dd6c5-134">See Also</span></span>
[<span data-ttu-id="dd6c5-135">Projekthantering</span><span class="sxs-lookup"><span data-stu-id="dd6c5-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="dd6c5-136">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="dd6c5-136">Finance</span></span>](finance.md)  
<span data-ttu-id="dd6c5-137">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="dd6c5-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="dd6c5-138">[Försäljning](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="dd6c5-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="dd6c5-139">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dd6c5-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

