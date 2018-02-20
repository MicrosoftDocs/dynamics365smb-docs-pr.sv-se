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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3e972ae6532c9531845e2739237b6ccb94d14c12
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="delete-workflows"></a><span data-ttu-id="9b009-104">Ta bort arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="9b009-104">Delete Workflows</span></span>
<span data-ttu-id="9b009-105">Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det.</span><span class="sxs-lookup"><span data-stu-id="9b009-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="9b009-106">Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**.</span><span class="sxs-lookup"><span data-stu-id="9b009-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="9b009-107">När du tar bort ett arbetsflöde, kommer all information i arbetsflödet förloras.</span><span class="sxs-lookup"><span data-stu-id="9b009-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="9b009-108">I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="9b009-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="9b009-109">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="9b009-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="9b009-110">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="9b009-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="9b009-111">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="9b009-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="9b009-112">Så här tar du bort ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="9b009-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="9b009-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9b009-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9b009-114">Välj arbetsflödet som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="9b009-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="9b009-115">Välj åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="9b009-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="9b009-116">Eller öppna arbetsflödet som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="9b009-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="9b009-117">I fönstret **Kopiera arbetsflöde** väljer du åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="9b009-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9b009-118">Se även</span><span class="sxs-lookup"><span data-stu-id="9b009-118">See Also</span></span>  
 <span data-ttu-id="9b009-119">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="9b009-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="9b009-120">[Så här aktiverar du arbetsflöden](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="9b009-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="9b009-121">[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="9b009-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="9b009-122">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="9b009-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="9b009-123">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="9b009-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="9b009-124">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="9b009-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="9b009-125">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="9b009-125">Workflow</span></span>](across-workflow.md)   

