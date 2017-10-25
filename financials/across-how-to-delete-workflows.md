---
title: "Så här raderar du arbetsflöden | Microsoft Docs"
description: "Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det. Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d1b7b29735983e2de0bdaf5d382679d9546a6278
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-workflows"></a><span data-ttu-id="2b46c-104">Så här tar du bort arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="2b46c-104">How to: Delete Workflows</span></span>
<span data-ttu-id="2b46c-105">Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det.</span><span class="sxs-lookup"><span data-stu-id="2b46c-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="2b46c-106">Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**.</span><span class="sxs-lookup"><span data-stu-id="2b46c-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="2b46c-107">När du tar bort ett arbetsflöde, kommer all information i arbetsflödet förloras.</span><span class="sxs-lookup"><span data-stu-id="2b46c-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="2b46c-108">I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="2b46c-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="2b46c-109">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="2b46c-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="2b46c-110">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="2b46c-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="2b46c-111">(Mer information finns i [Så här skapar du arbetsflöde](across-how-to-create-workflows.md).)</span><span class="sxs-lookup"><span data-stu-id="2b46c-111">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="2b46c-112">Så här tar du bort ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="2b46c-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="2b46c-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2b46c-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2b46c-114">Välj arbetsflödet som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="2b46c-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="2b46c-115">Välj åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="2b46c-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="2b46c-116">Eller öppna arbetsflödet som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="2b46c-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="2b46c-117">I fönstret **Kopiera arbetsflöde** väljer du åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="2b46c-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b46c-118">Se även</span><span class="sxs-lookup"><span data-stu-id="2b46c-118">See Also</span></span>  
 <span data-ttu-id="2b46c-119">[Så här skapar du arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2b46c-119">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="2b46c-120">[Så här aktiverar du arbetsflöden](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2b46c-120">[How to: Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="2b46c-121">[Så här visar du arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="2b46c-121">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="2b46c-122">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="2b46c-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="2b46c-123">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2b46c-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="2b46c-124">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2b46c-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="2b46c-125">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="2b46c-125">Workflow</span></span>](across-workflow.md)   

