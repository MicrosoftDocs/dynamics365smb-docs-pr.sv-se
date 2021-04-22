---
title: 'Gör så här: Exportera och importera arbetsflöden | Microsoft Docs'
description: För att överföra arbetsflöden till andra Business Central-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: de18f704edf03a569d609dbee891b84bb7bfa748
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775753"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="e0f00-103">Exportera och importera arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="e0f00-103">Export and Import Workflows</span></span>
<span data-ttu-id="e0f00-104">För att överföra arbetsflöden till andra [!INCLUDE[prod_short](includes/prod_short.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="e0f00-104">To transfer workflows to other [!INCLUDE[prod_short](includes/prod_short.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="e0f00-105">Ett annat sätt att snabbt skapa arbetsflöden är att skapa arbetsflöden från arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="e0f00-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="e0f00-106">Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="e0f00-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="e0f00-107">På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="e0f00-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="e0f00-108">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="e0f00-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="e0f00-109">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="e0f00-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="e0f00-110">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e0f00-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="e0f00-111">Så här exporterar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="e0f00-111">To export a workflow</span></span>  
1.  <span data-ttu-id="e0f00-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e0f00-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e0f00-113">Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.</span><span class="sxs-lookup"><span data-stu-id="e0f00-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="e0f00-114">På sidan **Exportera fil** väljer du knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="e0f00-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="e0f00-115">Välj en filplats på sidan **Exportera** och välj sedan knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="e0f00-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="e0f00-116">Så här importerar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="e0f00-116">To import a workflow</span></span>  
1.  <span data-ttu-id="e0f00-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e0f00-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e0f00-118">Välj åtgärden **Importera från fil**.</span><span class="sxs-lookup"><span data-stu-id="e0f00-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="e0f00-119">På sidan **Importera** väljer du den XML-fil som innehåller arbetsflödet och sedan knappen **Öppna**.</span><span class="sxs-lookup"><span data-stu-id="e0f00-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="e0f00-120">Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="e0f00-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0f00-121">Se även</span><span class="sxs-lookup"><span data-stu-id="e0f00-121">See Also</span></span>  
 <span data-ttu-id="e0f00-122">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="e0f00-123">[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="e0f00-124">[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="e0f00-125">[Ta bort arbetsflöden](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="e0f00-126">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="e0f00-127">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="e0f00-128">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0f00-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="e0f00-129">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="e0f00-129">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]