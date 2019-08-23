---
title: Hur du arkiverar försäljnings- och inköpsdokument | Microsoft Docs
description: Du kan arkivera försäljnings- och inköpsorder, offerter, försäljningsreturorder och avropsorder, och du kan använda arkiverade dokumentet för att återskapa dokumentet som det arkiverades från.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2019
ms.author: sgroespe
ms.openlocfilehash: 4d7d9ad0e9c84d5c767095b7b7e786be932625e7
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796694"
---
# <a name="archive-documents"></a><span data-ttu-id="7a8a6-103">Arkivera dokument</span><span class="sxs-lookup"><span data-stu-id="7a8a6-103">Archive Documents</span></span>
<span data-ttu-id="7a8a6-104">Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och avropsorder, till exempel för att spara en kopia av dokumentet för senare användning.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="7a8a6-105">Du kan arkivera ett försäljnings- eller inköpsdokument flera gånger och spara en annan arkiverad version varje gång.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="7a8a6-106">För arkiverade dokument där originalet finns och inte har bokförts, kan du använda funktionen **återställa** för att skriva över originalet med den arkiverade versionen av dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="7a8a6-107">Detta är praktiskt om du behöver återställa innehållet i ett dokument till ett tidigare tillstånd.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="7a8a6-108">För arkiverade dokument där originalet tas bort kan du återanvända innehållet genom att kopiera informationen, till exempel endast med funktionen **Kopiera dokument**.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="7a8a6-109">Så här ställer du in automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="7a8a6-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="7a8a6-110">Du kan ställa in automatisk arkivering av försäljnings- och inköpsorder, offerter, avropsorder och returorder innan du tar bort dokument.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="7a8a6-111">Nedan beskrivs hur du ställer in automatisk arkivering av försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="7a8a6-112">Momenten är liknande för en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="7a8a6-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a8a6-114">På sidan **Försäljningsinställningar** fyller du i följande fält:</span><span class="sxs-lookup"><span data-stu-id="7a8a6-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="7a8a6-115">Fält</span><span class="sxs-lookup"><span data-stu-id="7a8a6-115">Field</span></span>|<span data-ttu-id="7a8a6-116">Description</span><span class="sxs-lookup"><span data-stu-id="7a8a6-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="7a8a6-117">**Arkivering av försäljningsofferter**</span><span class="sxs-lookup"><span data-stu-id="7a8a6-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="7a8a6-118">**Aldrig** om du aldrig vill arkivera försäljningsofferter när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="7a8a6-119">**Fråga** för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="7a8a6-120">**Alltid** om du vill arkivera försäljningsofferter automatiskt när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="7a8a6-121">**Arkivera avropsorder för försäljning**</span><span class="sxs-lookup"><span data-stu-id="7a8a6-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="7a8a6-122">Välj detta alternativ om du vill arkivera avropsorder automatiskt när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="7a8a6-123">**Arkivera inköpsorder och inköpsreturorder**</span><span class="sxs-lookup"><span data-stu-id="7a8a6-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="7a8a6-124">Välj detta alternativ om du vill arkivera försäljningsorder automatiskt när de tas bort.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="7a8a6-125">För att arkivera en försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="7a8a6-125">To archive a sales order</span></span>
<span data-ttu-id="7a8a6-126">Följande förfarande beskriver hur du arkiverar en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="7a8a6-127">Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="7a8a6-128">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7a8a6-129">Öppna en försäljningsorder som du vill arkivera.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="7a8a6-130">Välj åtgärden **Arkivera dokument**.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="7a8a6-131">Försäljningsordern arkiveras.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-131">The sales order is archived.</span></span> <span data-ttu-id="7a8a6-132">Du kan visa den på sidan **Arkiverade försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-132">You can view it on the **Archived Sales Orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="7a8a6-133">Så här återställer du en icke-bokförd försäljningsorder från arkivet</span><span class="sxs-lookup"><span data-stu-id="7a8a6-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="7a8a6-134">Nedan beskrivs hur du ändrar innehållet i en arkiverad försäljningsorder till den ursprungliga försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="7a8a6-135">Detta är endast möjligt när det ursprungliga dokumentet inte ännu bokförts.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="7a8a6-136">Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="7a8a6-137">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arkiverade försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a8a6-138">Markera den arkiverade försäljningsordern eller versionen av den som du vill återskapa och välj sedan åtgärden **Återskapa**.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="7a8a6-139">Innehållet i den ursprungliga försäljningsordern ersätts med värdet för den valda arkiverade versionen.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="7a8a6-140">Ta bort arkiverade förs.orderversioner</span><span class="sxs-lookup"><span data-stu-id="7a8a6-140">To delete archived sales orders</span></span>
<span data-ttu-id="7a8a6-141">Följande förfarande beskriver hur du tar bort arkiverade försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="7a8a6-142">Stegen är liknande för andra arkiverade försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="7a8a6-143">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort arkiverade förs.orderversioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7a8a6-144">På sidan **Ta bort arkiverade försäljningsorderversioner** väljer du lämpliga filter.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="7a8a6-145">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a8a6-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a8a6-146">Se även</span><span class="sxs-lookup"><span data-stu-id="7a8a6-146">See Also</span></span>
[<span data-ttu-id="7a8a6-147">Spåra dokumentrader</span><span class="sxs-lookup"><span data-stu-id="7a8a6-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="7a8a6-148">Försäljning</span><span class="sxs-lookup"><span data-stu-id="7a8a6-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="7a8a6-149">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="7a8a6-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="7a8a6-150">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a8a6-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
