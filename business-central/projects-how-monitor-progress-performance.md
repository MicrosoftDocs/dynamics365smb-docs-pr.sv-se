---
title: Definiera en PIA-metod och övervaka projektets framsteg | Microsoft Docs
description: Beskriver hur du skapar en PIA-metod och beräknar PIA för att uppskatta det ekonomiska värdet i lika jobb medan de pågår.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fac1c041108cacfcabf18b04d128949d05e1d283
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938127"
---
# <a name="monitor-job-progress-and-performance"></a><span data-ttu-id="e1a91-103">Övervaka projektframsteg och -resultat</span><span class="sxs-lookup"><span data-stu-id="e1a91-103">Monitor Job Progress and Performance</span></span>
<span data-ttu-id="e1a91-104">Allt eftersom ett projekt fortlöper används material och resurser och de, och andra kostnader, måste bokföras i projektet.</span><span class="sxs-lookup"><span data-stu-id="e1a91-104">As a job progresses, materials, resources, and other expenses are consumed and must be posted to the job.</span></span> <span data-ttu-id="e1a91-105">Produkter i arbete (PIA) är en funktion som gör att du kan uppskatta värdet i projektet i redovisningen medan projekten pågår.</span><span class="sxs-lookup"><span data-stu-id="e1a91-105">Work in Process (WIP) is a feature that enables you to estimate the financial value of jobs in the general ledger while the jobs are ongoing.</span></span> <span data-ttu-id="e1a91-106">I många fall kan du bokföra kostnader för ett projekt innan du fakturerar projektet.</span><span class="sxs-lookup"><span data-stu-id="e1a91-106">In many cases, you might post expenses for a job before invoicing a job.</span></span> <span data-ttu-id="e1a91-107">Om endast kostnader bokförts blir er finansiella rapport oriktig.</span><span class="sxs-lookup"><span data-stu-id="e1a91-107">When only expenses have been posted, your financial statement will be inaccurate.</span></span> <span data-ttu-id="e1a91-108">Mer information finns i [Förstå PIA-metoder](projects-understanding-wip.md).</span><span class="sxs-lookup"><span data-stu-id="e1a91-108">For more information, see [Understanding WIP Methods](projects-understanding-wip.md).</span></span>

<span data-ttu-id="e1a91-109">Om du vill hålla reda på värdet i redovisningen kan du beräkna PIA (Produkter i arbete) och bokföra värdet i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-109">To track the value in the general ledger, you can calculate WIP and post the value to the general ledger.</span></span>

<span data-ttu-id="e1a91-110">Du kan beräkna PIA baserat på:</span><span class="sxs-lookup"><span data-stu-id="e1a91-110">You can calculate WIP based on the following:</span></span>

* <span data-ttu-id="e1a91-111">Kostnadsvärde</span><span class="sxs-lookup"><span data-stu-id="e1a91-111">Cost Value</span></span>
* <span data-ttu-id="e1a91-112">Försäljningsvärde</span><span class="sxs-lookup"><span data-stu-id="e1a91-112">Sales Value</span></span>
* <span data-ttu-id="e1a91-113">Identifierbar kostnad</span><span class="sxs-lookup"><span data-stu-id="e1a91-113">Recognizable Cost</span></span>
* <span data-ttu-id="e1a91-114">Färdigställningsgrad</span><span class="sxs-lookup"><span data-stu-id="e1a91-114">Percentage of Completion</span></span>
* <span data-ttu-id="e1a91-115">Slutfört kontrakt</span><span class="sxs-lookup"><span data-stu-id="e1a91-115">Completed Contract</span></span>

<span data-ttu-id="e1a91-116">Om du vill visa resultatet med någon annan metod ändrar du metoden och beräknar om PIA.</span><span class="sxs-lookup"><span data-stu-id="e1a91-116">If you want to view the result using a different method, you can change the method and calculate WIP again.</span></span> <span data-ttu-id="e1a91-117">Det finns ingen gräns för hur många gånger du kan beräkna PIA.</span><span class="sxs-lookup"><span data-stu-id="e1a91-117">There is no limit to the number of times that you calculate WIP.</span></span> <span data-ttu-id="e1a91-118">PIA beräknas bara, det bokförs inte i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-118">WIP is only calculated, it does not get posted to the general ledger.</span></span> <span data-ttu-id="e1a91-119">När du har beräknat PIA kan du bokföra det i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-119">After you have calculated WIP, you can post to the general ledger.</span></span>

## <a name="to-create-a-job-wip-method"></a><span data-ttu-id="e1a91-120">Skapa en PIA-metod för projektet</span><span class="sxs-lookup"><span data-stu-id="e1a91-120">To create a job WIP method</span></span>
<span data-ttu-id="e1a91-121">Du kan skapa en PIA-metoden för projektet som visar behoven i organisationen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-121">You can create a job WIP method that reflects the needs of your organization.</span></span> <span data-ttu-id="e1a91-122">När du har skapat detta kan du ange vilken PIA-beräkningsmetod som ska användas som standard i organisationen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-122">After you have created it, you can set it as the default job WIP calculation method that will be used in your organization.</span></span>  

> [!NOTE]
> <span data-ttu-id="e1a91-123">När du har använt den nya metoden för att skapa PIA-transaktioner kan du inte ta bort metoden eller ändra den.</span><span class="sxs-lookup"><span data-stu-id="e1a91-123">After you have used your new method to create WIP entries, you cannot delete the method or modify it.</span></span>  

1. <span data-ttu-id="e1a91-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **PIA-metoder för projekt** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job WIP Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1a91-125">Välj åtgärden **Ny** och fyll sedan i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e1a91-125">Choose the **New** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="e1a91-126">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="e1a91-126">Close the page.</span></span>   
4. <span data-ttu-id="e1a91-127">För att göra den nya metoden till standard väljer du ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), anger **Projektinställningar** och väljer sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-127">To make this new method the default, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs Setup**, and then choose the related link.</span></span>  
5. <span data-ttu-id="e1a91-128">I fältet **Standard-PIA-metod** väljer du metoden i listan.</span><span class="sxs-lookup"><span data-stu-id="e1a91-128">In the **Default WIP Method** field, choose the method from the list.</span></span>

## <a name="to-define-a-wip-method-for-a-job"></a><span data-ttu-id="e1a91-129">Så här definierar du en PIA-metod för ett projekt</span><span class="sxs-lookup"><span data-stu-id="e1a91-129">To define a WIP method for a job</span></span>
<span data-ttu-id="e1a91-130">När du skapar ett nytt projekt måste du ange vilken PIA-metod för projektet som gäller.</span><span class="sxs-lookup"><span data-stu-id="e1a91-130">When you create a new job, you must specify which job WIP method that applies.</span></span> <span data-ttu-id="e1a91-131">I vissa fall har metoden för PIA-redovisningstransaktioner för projekt, som du kan använda, ställts in för dig som standard.</span><span class="sxs-lookup"><span data-stu-id="e1a91-131">In some cases, which Job WIP method that you can use has been set up for you as a default.</span></span>

1. <span data-ttu-id="e1a91-132">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="e1a91-133">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-133">Choose the **New** action.</span></span> <span data-ttu-id="e1a91-134">Mer information finns i [Skapa projekt](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="e1a91-134">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>  
3. <span data-ttu-id="e1a91-135">PÅ sidan **Projektkort**, i fältet **PIA-metod**, väljer du en PIA-metod i listan.</span><span class="sxs-lookup"><span data-stu-id="e1a91-135">On the **Job Card** page, in the **WIP Method** field, select a WIP method from the list.</span></span> <span data-ttu-id="e1a91-136">Om en standardmetod har definierats, kan du välja ett annat alternativ vid behov.</span><span class="sxs-lookup"><span data-stu-id="e1a91-136">If a default method has been defined, you can select another option if needed.</span></span>  

## <a name="to-calculate-wip"></a><span data-ttu-id="e1a91-137">Så här beräknar du PIA</span><span class="sxs-lookup"><span data-stu-id="e1a91-137">To calculate WIP</span></span>
<span data-ttu-id="e1a91-138">Du kan fastställa PIA-beloppet som ska bokföras på balansräkningskonton för periodslutsrapporteringen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-138">You can determine the WIP amount that is to be posted to balance sheet accounts for the period end reporting.</span></span> <span data-ttu-id="e1a91-139">Du kan använda batch-jobbet **Projekt – Beräkna PIA** om du vill göra detta.</span><span class="sxs-lookup"><span data-stu-id="e1a91-139">You use the **Job Calculate WIP** batch job to do this.</span></span>  

1. <span data-ttu-id="e1a91-140">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt – Beräkna PIA** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Calculate WIP**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1a91-141">Välj åtgärden **Beräkna PIA**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-141">Choose the **Calculate WIP** action.</span></span>
3. <span data-ttu-id="e1a91-142">På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e1a91-142">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>
4. <span data-ttu-id="e1a91-143">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-143">Choose the **OK** button.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e1a91-144">Batch-jobbet beräknar bara PIA.</span><span class="sxs-lookup"><span data-stu-id="e1a91-144">The batch job only calculates the WIP.</span></span> <span data-ttu-id="e1a91-145">Detta bokförs inte i Redovisning.</span><span class="sxs-lookup"><span data-stu-id="e1a91-145">It is not posted to the general ledger.</span></span> <span data-ttu-id="e1a91-146">Om du vill bokföra måste du köra batch-jobbet **Bokför PIA i redovisning** när du har beräknat PIA.</span><span class="sxs-lookup"><span data-stu-id="e1a91-146">To do so, you must run the **Post WIP to G/L** batch job when you have calculated the WIP.</span></span> <span data-ttu-id="e1a91-147">Mer information finns i följande procedur:</span><span class="sxs-lookup"><span data-stu-id="e1a91-147">For more information, see the following procedure.</span></span>

## <a name="to-post-wip"></a><span data-ttu-id="e1a91-148">Bokföra PIA</span><span class="sxs-lookup"><span data-stu-id="e1a91-148">To post WIP</span></span>
<span data-ttu-id="e1a91-149">När du har beräknat PIA kan du bokföra det på balansräkningskonton för rapportering vid periodens slut.</span><span class="sxs-lookup"><span data-stu-id="e1a91-149">When you have calculated WIP, you can post it to balance sheet accounts for the period end reporting.</span></span> <span data-ttu-id="e1a91-150">Använd batch-jobbet **Projekt – Bokför PIA i redovisning** om du vill göra detta.</span><span class="sxs-lookup"><span data-stu-id="e1a91-150">You use the **Job Post WIP to G/L** batch job to do this.</span></span>

1. <span data-ttu-id="e1a91-151">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt – Bokför PIA i redovisning** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-151">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Post WIP to G/L**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1a91-152">På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e1a91-152">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="e1a91-153">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-153">Choose the **OK** button.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="e1a91-154">Beräkna och bokföra slutförda projekt</span><span class="sxs-lookup"><span data-stu-id="e1a91-154">To calculate and post job completion entries</span></span>
<span data-ttu-id="e1a91-155">När du har slutfört alla aktiviteter i ett projekt, bland annat bokföringen och faktureringen av förbrukning, måste du uppdatera projektet så att projektet får **Statusen** **Slutförd**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-155">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="e1a91-156">Sedan måste du återföra alla PIA som har bokförs i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e1a91-156">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="e1a91-157">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-157">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1a91-158">Välj ett öppet projekt och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-158">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="e1a91-159">Markera **Slutförd** i fältet **Status** .</span><span class="sxs-lookup"><span data-stu-id="e1a91-159">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="e1a91-160">Följ hjälpstegen steg för att beräkna och bokföra PIA.</span><span class="sxs-lookup"><span data-stu-id="e1a91-160">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="e1a91-161">Följ alternativt steg 5 och 6 för att göra det manuellt.</span><span class="sxs-lookup"><span data-stu-id="e1a91-161">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="e1a91-162">Välj åtgärden **Beräkna PIA**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-162">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="e1a91-163">På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e1a91-163">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="e1a91-164">De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.</span><span class="sxs-lookup"><span data-stu-id="e1a91-164">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="e1a91-165">Välj åtgärden **Projekt – Bokför PIA i redovisning**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-165">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="e1a91-166">På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="e1a91-166">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="e1a91-167">De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.</span><span class="sxs-lookup"><span data-stu-id="e1a91-167">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="to-view-job-ledger-entries"></a><span data-ttu-id="e1a91-168">Så här visar du projekttransaktioner</span><span class="sxs-lookup"><span data-stu-id="e1a91-168">To view job ledger entries</span></span>
<span data-ttu-id="e1a91-169">Alla projektrelaterade transaktioner registreras i bokförda projektjournaler och numreras i ordningsföljd med start från nummer ett.</span><span class="sxs-lookup"><span data-stu-id="e1a91-169">All job-related entries are recorded in job registers and are numbered sequentially, starting with 1.</span></span> <span data-ttu-id="e1a91-170">I den bokförda projektjournalen kan du få en överblick över alla projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e1a91-170">From the job register, you can get an overview of all job ledger entries.</span></span>    

1. <span data-ttu-id="e1a91-171">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda projektjournaler** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="e1a91-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Registers**, and then choose the related link.</span></span>
2. <span data-ttu-id="e1a91-172">Välj en relevant journal och välj sedan åtgärden **Projekttransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="e1a91-172">Select a relevant register, and then choose **Job Ledger** action.</span></span>

<span data-ttu-id="e1a91-173">På sidan **Projekttransaktioner** kan du granska de transaktioner som är kopplade till alla projekt.</span><span class="sxs-lookup"><span data-stu-id="e1a91-173">On the **Job Ledger Entries** page you can review the entries that are associated with any job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1a91-174">Se även</span><span class="sxs-lookup"><span data-stu-id="e1a91-174">See Also</span></span>
<span data-ttu-id="e1a91-175">[Hantera projekt](projects-manage-projects.md)
[hantera lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="e1a91-175">[Managing Projects](projects-manage-projects.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
[<span data-ttu-id="e1a91-176">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="e1a91-176">Finance</span></span>](finance.md)  
<span data-ttu-id="e1a91-177">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="e1a91-177">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="e1a91-178">[Försäljning](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="e1a91-178">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="e1a91-179">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e1a91-179">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
