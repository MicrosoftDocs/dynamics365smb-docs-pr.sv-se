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
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782524"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="9def5-103">Bokföra flera dokument på samma gång</span><span class="sxs-lookup"><span data-stu-id="9def5-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="9def5-104">I stället för att bokföra enskilda dokument var för sig kan du välja flera icke bokförda dokument i en lista för direkt bokföring eller för batch-bokföring enligt ett schema, t.ex. i slutet av dagen.</span><span class="sxs-lookup"><span data-stu-id="9def5-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="9def5-105">Detta kan vara användbart om endast en ansvarig kan bokföra dokument som skapats av andra användare eller undvika problem med system prestanda vid bokföring under arbetstid.</span><span class="sxs-lookup"><span data-stu-id="9def5-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="9def5-106">Så här bokför du flera inköpsorder direkt</span><span class="sxs-lookup"><span data-stu-id="9def5-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="9def5-107">I proceduren nedan beskrivs hur du bokför flera inköpsorder direkt.</span><span class="sxs-lookup"><span data-stu-id="9def5-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="9def5-108">Stegen är liknande för alla ingående och utgående dokument.</span><span class="sxs-lookup"><span data-stu-id="9def5-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="9def5-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9def5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="9def5-110">På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:</span><span class="sxs-lookup"><span data-stu-id="9def5-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="9def5-111">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="9def5-111">In the **No.**</span></span> <span data-ttu-id="9def5-112">väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.</span><span class="sxs-lookup"><span data-stu-id="9def5-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="9def5-113">Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.</span><span class="sxs-lookup"><span data-stu-id="9def5-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="9def5-114">Välj åtgärden **bokföra** och välj sedan åtgärden **bokför**.</span><span class="sxs-lookup"><span data-stu-id="9def5-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="9def5-115">Välj knappen **Ja** på bekräftelsemeddelandet.</span><span class="sxs-lookup"><span data-stu-id="9def5-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="9def5-116">Så här bokför du flera inköpsorder</span><span class="sxs-lookup"><span data-stu-id="9def5-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="9def5-117">I proceduren nedan beskrivs hur du bokför flera inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="9def5-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="9def5-118">Stegen är liknande för alla inköps- och försäljningsdokument där åtgärden **batch-bokföring** är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="9def5-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="9def5-119">Masspublicering av dokument sker i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="9def5-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="9def5-120">[!INCLUDE [prodshort](includes/prodshort.md)] online omfattar standardjobb för bakgrundsinlägg och masspublicering.</span><span class="sxs-lookup"><span data-stu-id="9def5-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="9def5-121">Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="9def5-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="9def5-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="9def5-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9def5-123">På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:</span><span class="sxs-lookup"><span data-stu-id="9def5-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="9def5-124">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="9def5-124">In the **No.**</span></span> <span data-ttu-id="9def5-125">väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.</span><span class="sxs-lookup"><span data-stu-id="9def5-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="9def5-126">Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.</span><span class="sxs-lookup"><span data-stu-id="9def5-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="9def5-127">Välj åtgärden **bokföra** och välj sedan åtgärden **Bokför batch-jobb**.</span><span class="sxs-lookup"><span data-stu-id="9def5-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="9def5-128">På sidan **Batch-bokför inköpsorder** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="9def5-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="9def5-129">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="9def5-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="9def5-130">Om du vill visa potentiella problem som uppstod vid batch-bokföring av dokument öppnar du fönstret **registrera felmeddelande**.</span><span class="sxs-lookup"><span data-stu-id="9def5-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="9def5-131">Inköpsordern läggs nu till i en dedikerad jobbkötransaktion som definierar när dokumenten bokförs.</span><span class="sxs-lookup"><span data-stu-id="9def5-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="9def5-132">Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="9def5-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="9def5-133">Om du väljer **PDF** i fältet **Rapportutdatatyp**, kommer bokförda inköpsorder vara tillgängliga i delen **rapportinkorg** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="9def5-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="9def5-134">Se även</span><span class="sxs-lookup"><span data-stu-id="9def5-134">See Also</span></span>

[<span data-ttu-id="9def5-135">Bokför dokument och journaler</span><span class="sxs-lookup"><span data-stu-id="9def5-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="9def5-136">Använda jobbköer för att schemalägga uppgifter</span><span class="sxs-lookup"><span data-stu-id="9def5-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="9def5-137">Redigera bokförda dokument</span><span class="sxs-lookup"><span data-stu-id="9def5-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="9def5-138">Korrigera eller annullera obetalda inköpsfakturor</span><span class="sxs-lookup"><span data-stu-id="9def5-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="9def5-139">Söka efter sidor och information med berätta</span><span class="sxs-lookup"><span data-stu-id="9def5-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="9def5-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9def5-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
