---
title: Så här raderar du arbetsflöden | Microsoft Docs
description: Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det. Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0cdec04115ebfe089ee89cdc5db8cf28e3963eb8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305434"
---
# <a name="delete-workflows"></a><span data-ttu-id="0cf65-104">Ta bort arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="0cf65-104">Delete Workflows</span></span>
<span data-ttu-id="0cf65-105">Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det.</span><span class="sxs-lookup"><span data-stu-id="0cf65-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="0cf65-106">Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**.</span><span class="sxs-lookup"><span data-stu-id="0cf65-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="0cf65-107">När du tar bort ett arbetsflöde, kommer all information i arbetsflödet förloras.</span><span class="sxs-lookup"><span data-stu-id="0cf65-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="0cf65-108">På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="0cf65-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="0cf65-109">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="0cf65-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="0cf65-110">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="0cf65-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="0cf65-111">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0cf65-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="0cf65-112">Så här tar du bort ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="0cf65-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="0cf65-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0cf65-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0cf65-114">Välj arbetsflödet som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="0cf65-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="0cf65-115">Välj åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="0cf65-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="0cf65-116">Eller öppna arbetsflödet som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="0cf65-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="0cf65-117">På sidan **Kopiera arbetsflöde** väljer du åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="0cf65-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0cf65-118">Se även</span><span class="sxs-lookup"><span data-stu-id="0cf65-118">See Also</span></span>  
 <span data-ttu-id="0cf65-119">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0cf65-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="0cf65-120">[Så här aktiverar du arbetsflöden](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0cf65-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="0cf65-121">[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="0cf65-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="0cf65-122">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="0cf65-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="0cf65-123">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0cf65-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="0cf65-124">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0cf65-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="0cf65-125">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="0cf65-125">Workflow</span></span>](across-workflow.md)   
