---
title: "Gör så här: Exportera och importera arbetsflöden | Microsoft Docs"
description: "När du överför arbetsflöden till andra Dynamics 365-databaser kan du exportera och importera arbetsflöden, t.ex för att spara tid när du skapar nya arbetsflöden."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a><span data-ttu-id="1590a-103">Gör så här: Exportera och importera arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="1590a-103">How to: Export and Import Workflows</span></span>
<span data-ttu-id="1590a-104">För att överföra arbetsflöden till andra [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="1590a-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="1590a-105">Ett annat sätt att snabbt skapa arbetsflöden är att skapa arbetsflöden från arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="1590a-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="1590a-106">Mer information finns i [Så här skapar du arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="1590a-106">For more information, see [How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="1590a-107">I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="1590a-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="1590a-108">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="1590a-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="1590a-109">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="1590a-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="1590a-110">(Mer information finns i [Så här skapar du arbetsflöde](across-how-to-create-workflows.md).)</span><span class="sxs-lookup"><span data-stu-id="1590a-110">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="1590a-111">Så här exporterar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="1590a-111">To export a workflow</span></span>  
1.  <span data-ttu-id="1590a-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1590a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1590a-113">Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.</span><span class="sxs-lookup"><span data-stu-id="1590a-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="1590a-114">I fönstret **Exportera fil** väljer du knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="1590a-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="1590a-115">Välj en filplats i fönstret **Exportera** och välj sedan knappen **Spara**.</span><span class="sxs-lookup"><span data-stu-id="1590a-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="1590a-116">Så här importerar du ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="1590a-116">To import a workflow</span></span>  
1.  <span data-ttu-id="1590a-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1590a-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1590a-118">Välj åtgärden **Importera från fil**.</span><span class="sxs-lookup"><span data-stu-id="1590a-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="1590a-119">I fönstret **Importera** väljer du den XML-fil som innehåller arbetsflödet och sedan knappen **Öppna**.</span><span class="sxs-lookup"><span data-stu-id="1590a-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="1590a-120">Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="1590a-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1590a-121">Se även</span><span class="sxs-lookup"><span data-stu-id="1590a-121">See Also</span></span>  
 <span data-ttu-id="1590a-122">[Så här skapar du arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-122">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="1590a-123">[Så här skapar du arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-123">[How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="1590a-124">[Så här visar du arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-124">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="1590a-125">[Så här tar du bort arbetsflöden](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-125">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="1590a-126">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="1590a-127">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="1590a-128">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1590a-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="1590a-129">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="1590a-129">Workflow</span></span>](across-workflow.md)   

