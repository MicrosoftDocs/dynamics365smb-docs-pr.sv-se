---
title: Så här bokför du flera dokument på samma gång | Microsoft Docs
description: I stället för att bokföra enskilda dokument var för sig kan du välja flera icke bokförda dokument i en lista för batch-bokföring, antingen för direkt bokföring eller som t.ex. i slutet av dagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 15b0afcf04ad279000de227523f977fdb695fe01
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316793"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="dd5d5-103">Bokföra flera dokument på samma gång</span><span class="sxs-lookup"><span data-stu-id="dd5d5-103">Post Multiple Documents at the Same Time</span></span>
<span data-ttu-id="dd5d5-104">I stället för att bokföra enskilda dokument var för sig kan du välja flera icke bokförda dokument i en lista för direkt bokföring eller för batch-bokföring enligt ett schema, t.ex. i slutet av dagen.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="dd5d5-105">Detta kan vara användbart om endast en ansvarig kan bokföra dokument som skapats av andra användare eller undvika problem med system prestanda vid bokföring under arbetstid.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="dd5d5-106">Så här bokför du flera inköpsorder direkt</span><span class="sxs-lookup"><span data-stu-id="dd5d5-106">To post multiple purchase orders immediately</span></span>
<span data-ttu-id="dd5d5-107">I proceduren nedan beskrivs hur du bokför flera inköpsorder direkt.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="dd5d5-108">Stegen är liknande för alla ingående och utgående dokument.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="dd5d5-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="dd5d5-110">På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:</span><span class="sxs-lookup"><span data-stu-id="dd5d5-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="dd5d5-111">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="dd5d5-111">In the **No.**</span></span> <span data-ttu-id="dd5d5-112">väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="dd5d5-113">Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="dd5d5-114">Välj åtgärden **bokföra** och välj sedan åtgärden **bokför**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="dd5d5-115">Välj knappen **Ja** på bekräftelsemeddelandet.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="dd5d5-116">Så här bokför du flera inköpsorder</span><span class="sxs-lookup"><span data-stu-id="dd5d5-116">To batch post multiple purchase orders</span></span>
<span data-ttu-id="dd5d5-117">I proceduren nedan beskrivs hur du bokför flera inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="dd5d5-118">Stegen är liknande för alla inköps- och försäljningsdokument där åtgärden **batch-bokföring** är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="dd5d5-119">Batch-bokföring av dokument sker i bakgrunden enligt definitionen i en jobbkötransaktion, som måste ställas in först.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-119">Batch posting of documents happens in the background as defined by a job queue entry, which must first be set up.</span></span> <span data-ttu-id="dd5d5-120">Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="dd5d5-120">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="dd5d5-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dd5d5-122">På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:</span><span class="sxs-lookup"><span data-stu-id="dd5d5-122">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="dd5d5-123">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="dd5d5-123">In the **No.**</span></span> <span data-ttu-id="dd5d5-124">väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-124">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="dd5d5-125">Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-125">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="dd5d5-126">Välj åtgärden **bokföra** och välj sedan åtgärden **Bokför batch-jobb**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-126">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="dd5d5-127">På sidan **Batch-bokför inköpsorder** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-127">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > <span data-ttu-id="dd5d5-128">Om du vill skriva ut relaterade rapporter vid bokföring, t.ex. **orderbekräftelse** för försäljningsorder markerar du kryssrutan **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-128">To print related reports when posting, such as the **Order Confirmation** report for sales orders, select the **Print** check box.</span></span><br /><br /> <span data-ttu-id="dd5d5-129">I fältet **Rapportutdatatyp** på sidan **Försäljningsinställningar** eller **Inköpsinställningar** kan du ange om rapporten ska skrivas ut eller matas ut som PDF.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-129">In the **Report Output Type** field on the **Sales and Receivables Setup** page or **Purchases and Payables Setup** page, you define if the report will be printed or output as a PDF.</span></span><br /><br /> <span data-ttu-id="dd5d5-130">Tänk också på att direkt utskrift till en vald skrivare endast är möjlig vid lokala installationer.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-130">Note also that direct printing to a selected printer is only possible in on-premises installations.</span></span>

7. <span data-ttu-id="dd5d5-131">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-131">Choose the **OK** button.</span></span>
8. <span data-ttu-id="dd5d5-132">Om du vill visa potentiella problem som uppstod vid batch-bokföring av dokument öppnar du fönstret **registrera felmeddelande**.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-132">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="dd5d5-133">Inköpsordern läggs nu till i en dedikerad jobbkötransaktion som definierar när dokumenten bokförs.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-133">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="dd5d5-134">Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="dd5d5-134">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="dd5d5-135">Om du väljer **PDF** i fältet **Rapportutdatatyp**, kommer bokförda inköpsorder vara tillgängliga i delen **rapportinkorg** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-135">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd5d5-136">Se även</span><span class="sxs-lookup"><span data-stu-id="dd5d5-136">See Also</span></span>
[<span data-ttu-id="dd5d5-137">Bokför dokument och journaler</span><span class="sxs-lookup"><span data-stu-id="dd5d5-137">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="dd5d5-138">Använda jobbköer för att schemalägga uppgifter</span><span class="sxs-lookup"><span data-stu-id="dd5d5-138">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="dd5d5-139">Redigera bokförda dokument</span><span class="sxs-lookup"><span data-stu-id="dd5d5-139">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="dd5d5-140">Korrigera eller annullera obetalda inköpsfakturor</span><span class="sxs-lookup"><span data-stu-id="dd5d5-140">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="dd5d5-141">Söka efter sidor och information med berätta</span><span class="sxs-lookup"><span data-stu-id="dd5d5-141">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="dd5d5-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dd5d5-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
