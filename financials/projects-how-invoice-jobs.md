---
title: "Skapa en försäljningsfaktura för att fakturera ett projekt | Microsoft Docs"
description: "Beskriver hur du kan fakturera kunder för projektutgifter allt eftersom projektet fortskrider."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9367dc5875b687b95076efffb3b0df2019332651
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-invoice-jobs"></a><span data-ttu-id="6de0a-103">Så här fakturerar du projekt</span><span class="sxs-lookup"><span data-stu-id="6de0a-103">How to: Invoice Jobs</span></span>
<span data-ttu-id="6de0a-104">Under projektet kan projektkostnade från resursförbrukning, material och projektrelaterade inköp uppstå.</span><span class="sxs-lookup"><span data-stu-id="6de0a-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="6de0a-105">Dessa transaktioner bokförs i projektjournalen.</span><span class="sxs-lookup"><span data-stu-id="6de0a-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="6de0a-106">Det är viktigt att alla kostnader registreras i projektjournalen innan kunden faktureras.</span><span class="sxs-lookup"><span data-stu-id="6de0a-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="6de0a-107">Du kan fakturera hela projektet från fönstret **Projektaktivitetsrader** eller fakturera endast valda fakturerbara rader i fönstret **Planeringsrader**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="6de0a-108">Faktureringen kan göras när projektet har slutförts eller allt eftersom projektet fortlöper enligt ett faktureringsschema.</span><span class="sxs-lookup"><span data-stu-id="6de0a-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6de0a-109">Om du väljer **Fakturerbart** i fältet **Projektradtyp** på inköpsdokumentet för projektrelaterade inköp, skapas projektplaneringsrader som är klara att faktureras till kunden.</span><span class="sxs-lookup"><span data-stu-id="6de0a-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="6de0a-110">Mer information finns i [Så här hanterar du projektleveranser](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="6de0a-110">For more information, see [How to: Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="6de0a-111">Så här skapar och bokför du en försäljningsfaktura för ett projekt</span><span class="sxs-lookup"><span data-stu-id="6de0a-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="6de0a-112">Du kan skapa en faktura för ett projekt för en eller flera projektaktiviteter för en kund, antingen när det arbete som ska faktureras har slutförts eller när datumet för fakturering, som är baserat på ett faktureringsschema, har infallit.</span><span class="sxs-lookup"><span data-stu-id="6de0a-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="6de0a-113">Från fönstret **Projekt** kan du fakturera en kund genom att välja projekt och sedan välja åtgärden **Skapa jobbförsäljningsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="6de0a-114">Efterföljande procedur visar hur du kan använda ett batch-jobb för att fakturera flera projekt.</span><span class="sxs-lookup"><span data-stu-id="6de0a-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="6de0a-115">Välj ikonen ![söka efter sida eller rapport](media/ui-search/search_small.png "ikonen söka efter sida eller rapport"), ange **Projekt - Skapa förs.faktura** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6de0a-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6de0a-116">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="6de0a-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6de0a-117">Ange filter om du vill begränsa de projekt som ska bearbetas av batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="6de0a-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="6de0a-118">Klicka på **OK** för att skapa fakturorna.</span><span class="sxs-lookup"><span data-stu-id="6de0a-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="6de0a-119">Så här skapar du flera projektförsäljningsfakturor från projektplaneringsrader</span><span class="sxs-lookup"><span data-stu-id="6de0a-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="6de0a-120">Du kan skapa en faktura från projektplaneringsrader och då ange antal av artikeln, resursen eller redovisningskontot som du vill fakturera.</span><span class="sxs-lookup"><span data-stu-id="6de0a-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="6de0a-121">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6de0a-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="6de0a-122">Öppna ett relevant projekt.</span><span class="sxs-lookup"><span data-stu-id="6de0a-122">Open a relevant job.</span></span>
3. <span data-ttu-id="6de0a-123">Markera ett projekt där fältet **Typ av projektaktivitet** innehåller **Bokföring** och klicka sedan på åtgärden **Projektplaneringsrader**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="6de0a-124">Gå till fältet **Antal att överföra till faktura** på en projektplaneringsrad och ange antal av artikeln, resursen, typen av redovisningskonto som du vill fakturera.</span><span class="sxs-lookup"><span data-stu-id="6de0a-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="6de0a-125">Välj åtgärden **Skapa försäljningsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="6de0a-126">I fönstret **Projekt - Skapa förs.faktura** anger du bokföringsdatum och om du vill skapa en ny faktura eller koppla denna faktura till en befintlig.</span><span class="sxs-lookup"><span data-stu-id="6de0a-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="6de0a-127">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="6de0a-128">På projektplaneringsradens fält **Antal överfört till faktura** kan du se antalet.</span><span class="sxs-lookup"><span data-stu-id="6de0a-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="6de0a-129">I fönstret **Projektplaneringsrader** väljer du åtgärden **Försäljningsfakturor/kreditnotor**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="6de0a-130">Fönstret **Försäljningsfaktura** öppnas och visar antalet som du har överfört till fakturan.</span><span class="sxs-lookup"><span data-stu-id="6de0a-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="6de0a-131">Gör ytterligare ändringar och välj sedan åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6de0a-132">Ovanstående process är liknande för att skapa, granska och publicera en projektrelaterad försäljningskreditnota.</span><span class="sxs-lookup"><span data-stu-id="6de0a-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="6de0a-133">Så här kan du beräkna och bokföra slutförda projekt</span><span class="sxs-lookup"><span data-stu-id="6de0a-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="6de0a-134">När du har slutfört alla aktiviteter i ett projekt, bland annat bokföringen och faktureringen av förbrukning, måste du uppdatera projektet så att projektet får **Statusen** **Slutförd**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="6de0a-135">Sedan måste du återföra alla PIA som har bokförs i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="6de0a-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="6de0a-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6de0a-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6de0a-137">Välj ett öppet projekt och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="6de0a-138">Markera **Slutförd** i fältet **Status** .</span><span class="sxs-lookup"><span data-stu-id="6de0a-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="6de0a-139">Följ hjälpstegen steg för att beräkna och bokföra PIA.</span><span class="sxs-lookup"><span data-stu-id="6de0a-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="6de0a-140">Följ alternativt steg 5 och 6 för att göra det manuellt.</span><span class="sxs-lookup"><span data-stu-id="6de0a-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="6de0a-141">Välj åtgärden **Beräkna PIA**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="6de0a-142">I fönstret **Projekt - Beräkna PIA** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="6de0a-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="6de0a-143">De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.</span><span class="sxs-lookup"><span data-stu-id="6de0a-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="6de0a-144">Välj åtgärden **Projekt - Bokför PIA i redovisning**.</span><span class="sxs-lookup"><span data-stu-id="6de0a-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="6de0a-145">I fönstret **Projekt - Bokför PIA i redovisning** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="6de0a-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="6de0a-146">De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.</span><span class="sxs-lookup"><span data-stu-id="6de0a-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="6de0a-147">Se även</span><span class="sxs-lookup"><span data-stu-id="6de0a-147">See Also</span></span>
[<span data-ttu-id="6de0a-148">Hantera projekt</span><span class="sxs-lookup"><span data-stu-id="6de0a-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="6de0a-149">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="6de0a-149">Finance</span></span>](finance.md)  
<span data-ttu-id="6de0a-150">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="6de0a-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="6de0a-151">[Försäljning](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="6de0a-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="6de0a-152">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6de0a-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

