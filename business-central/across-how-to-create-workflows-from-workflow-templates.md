---
title: "Så här skapar du arbetsflöden från arbetsflödesmallar | Microsoft Docs"
description: "Du kan spara tid när du skapar nya arbetsflöden genom att skapa arbetsflöden från arbetsflödesmallar."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2a8da1e1f06a4556ebdfac28e5fe27adf169a7eb
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="dffc1-103">Skapa arbetsflöden från arbetsflödesmallar</span><span class="sxs-lookup"><span data-stu-id="dffc1-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="dffc1-104">Du kan spara tid när du skapar nya arbetsflöden genom att skapa arbetsflöden från arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="dffc1-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="dffc1-105">Arbetsflödesmallar representerar icke-redigerbara arbetsflöden som finns i den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dffc1-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="dffc1-106">Koderna för arbetsflödesmallar som läggs till av Microsoft har prefixet ”MS-”.</span><span class="sxs-lookup"><span data-stu-id="dffc1-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="dffc1-107">Ett annat sätt att snabbt att skapa ett arbetsflöde är att importera ett befintligt arbetsflöde som du har i en fil utanför [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dffc1-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="dffc1-108">Mer information finns i [Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="dffc1-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="dffc1-109">I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="dffc1-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="dffc1-110">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="dffc1-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="dffc1-111">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="dffc1-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="dffc1-112">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="dffc1-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="dffc1-113">Så här skapar du ett arbetsflöde från en arbetsflödesmall</span><span class="sxs-lookup"><span data-stu-id="dffc1-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="dffc1-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dffc1-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="dffc1-115">Välj åtgärden **skapa arbetsflödet från mallen**.</span><span class="sxs-lookup"><span data-stu-id="dffc1-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="dffc1-116">Fönstret **arbetsflödesmallar**.</span><span class="sxs-lookup"><span data-stu-id="dffc1-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="dffc1-117">Markera en arbetsflödesmall och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="dffc1-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="dffc1-118">Fönstret **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen.</span><span class="sxs-lookup"><span data-stu-id="dffc1-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="dffc1-119">Värdet i fältet **Kod** utökas med till exempel ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen.</span><span class="sxs-lookup"><span data-stu-id="dffc1-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="dffc1-120">Fortsätt med att skapa arbetsflödet genom att redigera arbetsflödesstegen, eller lägg till nya steg.</span><span class="sxs-lookup"><span data-stu-id="dffc1-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="dffc1-121">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="dffc1-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="dffc1-122">Se även</span><span class="sxs-lookup"><span data-stu-id="dffc1-122">See Also</span></span>  
 <span data-ttu-id="dffc1-123">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="dffc1-124">[Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="dffc1-125">[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="dffc1-126">[Ta bort arbetsflöden](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="dffc1-127">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="dffc1-128">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="dffc1-129">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="dffc1-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="dffc1-130">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="dffc1-130">Workflow</span></span>](across-workflow.md)   

