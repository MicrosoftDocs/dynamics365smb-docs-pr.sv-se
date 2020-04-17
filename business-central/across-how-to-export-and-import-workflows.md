---
title: 'Gör så här: Exportera och importera arbetsflöden | Microsoft Docs'
description: För att överföra arbetsflöden till andra Business Central-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2d309940d177491ce24f49884f388a5c233147fa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188282"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="27bd0-103">Exportera och importera arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="27bd0-103">Export and Import Workflows</span></span>
<span data-ttu-id="27bd0-104">För att överföra arbetsflöden till andra [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="27bd0-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="27bd0-105">Ett annat sätt att snabbt skapa arbetsflöden är att skapa arbetsflöden från arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="27bd0-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="27bd0-106">Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="27bd0-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="27bd0-107">På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="27bd0-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="27bd0-108">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="27bd0-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="27bd0-109">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="27bd0-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="27bd0-110">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="27bd0-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="27bd0-111">Så här exporterar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="27bd0-111">To export a workflow</span></span>  
1.  <span data-ttu-id="27bd0-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="27bd0-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27bd0-113">Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.</span><span class="sxs-lookup"><span data-stu-id="27bd0-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="27bd0-114">På sidan **Exportera fil** väljer du knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="27bd0-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="27bd0-115">Välj en filplats på sidan **Exportera** och välj sedan knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="27bd0-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="27bd0-116">Så här importerar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="27bd0-116">To import a workflow</span></span>  
1.  <span data-ttu-id="27bd0-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="27bd0-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27bd0-118">Välj åtgärden **Importera från fil**.</span><span class="sxs-lookup"><span data-stu-id="27bd0-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="27bd0-119">På sidan **Importera** väljer du den XML-fil som innehåller arbetsflödet och sedan knappen **Öppna**.</span><span class="sxs-lookup"><span data-stu-id="27bd0-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="27bd0-120">Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="27bd0-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27bd0-121">Se även</span><span class="sxs-lookup"><span data-stu-id="27bd0-121">See Also</span></span>  
 <span data-ttu-id="27bd0-122">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="27bd0-123">[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="27bd0-124">[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="27bd0-125">[Ta bort arbetsflöden](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="27bd0-126">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="27bd0-127">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="27bd0-128">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="27bd0-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="27bd0-129">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="27bd0-129">Workflow</span></span>](across-workflow.md)   
