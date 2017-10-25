---
title: "Gör så här: Exportera och importera arbetsflöden | Microsoft Docs"
description: "För att överföra arbetsflöden till andra [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden."
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
ms.openlocfilehash: 8126d3850103819e885d9d131ca3074f1b7cfda1
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-and-import-workflows"></a><span data-ttu-id="fd0df-103">Gör så här: Exportera och importera arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="fd0df-103">How to: Export and Import Workflows</span></span>
<span data-ttu-id="fd0df-104">För att överföra arbetsflöden till andra [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="fd0df-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="fd0df-105">Ett annat sätt att snabbt skapa arbetsflöden är att skapa arbetsflöden från arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="fd0df-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="fd0df-106">Mer information finns i [Så här skapar du arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fd0df-106">For more information, see [How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="fd0df-107">I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="fd0df-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="fd0df-108">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="fd0df-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="fd0df-109">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="fd0df-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="fd0df-110">(Mer information finns i [Så här skapar du arbetsflöde](across-how-to-create-workflows.md).)</span><span class="sxs-lookup"><span data-stu-id="fd0df-110">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="fd0df-111">Så här exporterar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="fd0df-111">To export a workflow</span></span>  
1.  <span data-ttu-id="fd0df-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fd0df-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fd0df-113">Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.</span><span class="sxs-lookup"><span data-stu-id="fd0df-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="fd0df-114">I fönstret **Exportera fil** väljer du knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="fd0df-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="fd0df-115">Välj en filplats i fönstret **Exportera** och välj sedan knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="fd0df-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="fd0df-116">Så här importerar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="fd0df-116">To import a workflow</span></span>  
1.  <span data-ttu-id="fd0df-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fd0df-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fd0df-118">Välj åtgärden **Importera från fil**.</span><span class="sxs-lookup"><span data-stu-id="fd0df-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="fd0df-119">I fönstret **Importera** väljer du den XML-fil som innehåller arbetsflödet och sedan knappen **Öppna**.</span><span class="sxs-lookup"><span data-stu-id="fd0df-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="fd0df-120">Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="fd0df-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fd0df-121">Se även</span><span class="sxs-lookup"><span data-stu-id="fd0df-121">See Also</span></span>  
 <span data-ttu-id="fd0df-122">[Så här skapar du arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-122">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="fd0df-123">[Så här skapar du arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-123">[How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="fd0df-124">[Så här visar du arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-124">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="fd0df-125">[Så här tar du bort arbetsflöden](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-125">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="fd0df-126">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="fd0df-127">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="fd0df-128">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fd0df-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="fd0df-129">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="fd0df-129">Workflow</span></span>](across-workflow.md)   

