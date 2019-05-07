---
title: Så här skapar du arbetsflöden från arbetsflödesmallar | Microsoft Docs
description: Du kan spara tid när du skapar nya arbetsflöden genom att skapa arbetsflöden från arbetsflödesmallar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 82d288ab59f80c6e5d2e46f8168f10552b5b900d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "912926"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="4dedd-103">Skapa arbetsflöden från arbetsflödesmallar</span><span class="sxs-lookup"><span data-stu-id="4dedd-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="4dedd-104">Du kan spara tid när du skapar nya arbetsflöden genom att skapa arbetsflöden från arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="4dedd-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="4dedd-105">Arbetsflödesmallar representerar icke-redigerbara arbetsflöden som finns i den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4dedd-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4dedd-106">Koderna för arbetsflödesmallar som läggs till av Microsoft har prefixet ”MS-”.</span><span class="sxs-lookup"><span data-stu-id="4dedd-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="4dedd-107">Ett annat sätt att snabbt att skapa ett arbetsflöde är att importera ett befintligt arbetsflöde som du har i en fil utanför [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4dedd-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4dedd-108">Mer information finns i [Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="4dedd-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="4dedd-109">På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="4dedd-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="4dedd-110">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="4dedd-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="4dedd-111">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="4dedd-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="4dedd-112">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="4dedd-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="4dedd-113">Så här skapar du ett arbetsflöde från en arbetsflödesmall</span><span class="sxs-lookup"><span data-stu-id="4dedd-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="4dedd-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4dedd-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4dedd-115">Välj åtgärden **skapa arbetsflödet från mallen**.</span><span class="sxs-lookup"><span data-stu-id="4dedd-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="4dedd-116">Sidan **arbetsflödesmallar**.</span><span class="sxs-lookup"><span data-stu-id="4dedd-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="4dedd-117">Markera en arbetsflödesmall och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dedd-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="4dedd-118">Sidan **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen.</span><span class="sxs-lookup"><span data-stu-id="4dedd-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="4dedd-119">Värdet i fältet **Kod** utökas med till exempel ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen.</span><span class="sxs-lookup"><span data-stu-id="4dedd-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="4dedd-120">Fortsätt med att skapa arbetsflödet genom att redigera arbetsflödesstegen, eller lägg till nya steg.</span><span class="sxs-lookup"><span data-stu-id="4dedd-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="4dedd-121">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="4dedd-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="4dedd-122">Se även</span><span class="sxs-lookup"><span data-stu-id="4dedd-122">See Also</span></span>  
 <span data-ttu-id="4dedd-123">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="4dedd-124">[Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="4dedd-125">[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="4dedd-126">[Ta bort arbetsflöden](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="4dedd-127">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="4dedd-128">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="4dedd-129">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="4dedd-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="4dedd-130">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="4dedd-130">Workflow</span></span>](across-workflow.md)   
