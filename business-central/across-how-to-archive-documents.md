---
title: "Hur du arkiverar försäljnings- och inköpsdokument | Microsoft Docs"
description: "Du kan arkivera försäljnings- och inköpsorder, offerter, försäljningsreturorder och avropsorder, och du kan använda arkiverade dokumentet för att återskapa dokumentet som det arkiverades från."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4827e25d97127faf691b96df9868320bb47dee39
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="archive-documents"></a><span data-ttu-id="3418e-103">Arkivera dokument</span><span class="sxs-lookup"><span data-stu-id="3418e-103">Archive Documents</span></span>
<span data-ttu-id="3418e-104">Du kan arkivera försäljnings- och inköpsorder, offerter, försäljningsreturorder och avropsorder, och du kan använda arkiverade dokumentet för att återskapa dokumentet som det arkiverades från.</span><span class="sxs-lookup"><span data-stu-id="3418e-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="3418e-105">Så här ställer du in automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="3418e-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="3418e-106">Du kan ställa in automatisk arkivering av försäljnings- och inköpsorder, offerter, avropsorder och returorder innan du tar bort dokument.</span><span class="sxs-lookup"><span data-stu-id="3418e-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="3418e-107">Nedan beskrivs hur du ställer in automatisk arkivering av försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="3418e-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="3418e-108">Momenten är liknande för en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="3418e-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="3418e-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3418e-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="3418e-110">På sidan **Försäljningsinställningar** fyller du i följande fält:</span><span class="sxs-lookup"><span data-stu-id="3418e-110">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="3418e-111">Fält</span><span class="sxs-lookup"><span data-stu-id="3418e-111">Field</span></span>|<span data-ttu-id="3418e-112">Description</span><span class="sxs-lookup"><span data-stu-id="3418e-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="3418e-113">**Arkivering av försäljningsofferter**</span><span class="sxs-lookup"><span data-stu-id="3418e-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="3418e-114">**Aldrig** om du aldrig vill arkivera försäljningsofferter när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="3418e-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="3418e-115">**Fråga** för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="3418e-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="3418e-116">**Alltid** om du vill arkivera försäljningsofferter automatiskt när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="3418e-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="3418e-117">**Arkivera avropsorder för försäljning**</span><span class="sxs-lookup"><span data-stu-id="3418e-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="3418e-118">Välj detta alternativ om du vill arkivera avropsorder automatiskt när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="3418e-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="3418e-119">**Arkivera inköpsorder och inköpsreturorder**</span><span class="sxs-lookup"><span data-stu-id="3418e-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="3418e-120">Välj detta alternativ om du vill arkivera försäljningsorder automatiskt när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="3418e-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="3418e-121">För att arkivera en försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="3418e-121">To archive a sales order</span></span>
<span data-ttu-id="3418e-122">Följande förfarande beskriver hur du arkiverar en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="3418e-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="3418e-123">Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.</span><span class="sxs-lookup"><span data-stu-id="3418e-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="3418e-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3418e-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3418e-125">Öppna en försäljningsorder som du vill arkivera.</span><span class="sxs-lookup"><span data-stu-id="3418e-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="3418e-126">Välj åtgärden **Arkivera dokument**.</span><span class="sxs-lookup"><span data-stu-id="3418e-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="3418e-127">Försäljningsordern arkiveras.</span><span class="sxs-lookup"><span data-stu-id="3418e-127">The sales order is archived.</span></span> <span data-ttu-id="3418e-128">Du kan visa den på sidan **Arkiverade försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="3418e-128">You can view it on the **Archived Sales orders** page.</span></span> <span data-ttu-id="3418e-129">Härifrån kan du också använda den för att återskapa den försäljningsorder som den arkiverades från.</span><span class="sxs-lookup"><span data-stu-id="3418e-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="3418e-130">Återskapa en försäljningsorder från arkivet</span><span class="sxs-lookup"><span data-stu-id="3418e-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="3418e-131">Följande förfarande beskriver hur du återskapar en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="3418e-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="3418e-132">Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.</span><span class="sxs-lookup"><span data-stu-id="3418e-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="3418e-133">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arkiverade försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3418e-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="3418e-134">Markera den arkiverade försäljningsorder som du vill återskapa och välj sedan åtgärden **Återskapa**.</span><span class="sxs-lookup"><span data-stu-id="3418e-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="3418e-135">Försäljningsordern skapas och läggs till på sidan **Försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="3418e-135">The sales order is created and added to the **Sales Orders** page.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="3418e-136">Ta bort arkiverade förs.orderversioner</span><span class="sxs-lookup"><span data-stu-id="3418e-136">To delete archived sales orders</span></span>
<span data-ttu-id="3418e-137">Följande förfarande beskriver hur du tar bort arkiverade försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="3418e-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="3418e-138">Stegen är liknande för andra arkiverade försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="3418e-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="3418e-139">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort arkiverade förs.orderversioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3418e-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3418e-140">På sidan **Ta bort arkiverade försäljningsorderversioner** väljer du lämpliga filter.</span><span class="sxs-lookup"><span data-stu-id="3418e-140">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="3418e-141">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="3418e-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="3418e-142">Se även</span><span class="sxs-lookup"><span data-stu-id="3418e-142">See Also</span></span>
[<span data-ttu-id="3418e-143">Spåra dokumentrader</span><span class="sxs-lookup"><span data-stu-id="3418e-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="3418e-144">Försäljning</span><span class="sxs-lookup"><span data-stu-id="3418e-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="3418e-145">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="3418e-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="3418e-146">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3418e-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

