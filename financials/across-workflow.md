---
title: "Arbetsflöden | Microsoft Docs"
description: "Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: 861ff6ac3c2789f83379e4c01c0e1b8f5847d2d6
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="workflow"></a><span data-ttu-id="8f4fc-105">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="8f4fc-105">Workflow</span></span>
<span data-ttu-id="8f4fc-106">Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="8f4fc-107">Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="8f4fc-108">Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="8f4fc-109">I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="8f4fc-110">Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="8f4fc-111">Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="8f4fc-112">Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal förkonfigurerade arbetsflöden som representeras av arbetsflödesmallar som du kan kopiera för att skapa arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="8f4fc-113">Koden för arbetsflödesmallar som läggs till av Microsoft har prefixet ”MS-”.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="8f4fc-114">Mer information finns i listan över arbetsflödesmallar i fönstret Arbetsflödesmallar.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="8f4fc-115">Om ett företagsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds måste en Microsoft-partner implementera dem genom att anpassa applikationskoden.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="8f4fc-116">Mer information finns i [Genomgång: Genomföra nya arbetsflödeshändelser och svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjälpen för utvecklare och IT-proffs.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>  

 <span data-ttu-id="8f4fc-117">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="8f4fc-118">**För att**</span><span class="sxs-lookup"><span data-stu-id="8f4fc-118">**To**</span></span>|<span data-ttu-id="8f4fc-119">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="8f4fc-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8f4fc-120">Konfigurera arbetsflödesanvändare, anger hur användarna får meddeladen och skapa nya arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="8f4fc-121">Implementera nödvändiga arbetsflödeselement genom att anpassa programkoden för nya arbetsflöden i scenarier som inte stöds.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="8f4fc-122">Konfigurera arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="8f4fc-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="8f4fc-123">Aktivera arbetsflöden, agera på arbetsflödemeddelanden inklusive begärandegodkännanden och godkänn begäranden för att utföra ett arbetsflödessteg.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="8f4fc-124">Arkivera och ta bort arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="8f4fc-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="8f4fc-125">Använda arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="8f4fc-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="8f4fc-126">Se även</span><span class="sxs-lookup"><span data-stu-id="8f4fc-126">See Also</span></span>  
[<span data-ttu-id="8f4fc-127">Försäljning</span><span class="sxs-lookup"><span data-stu-id="8f4fc-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="8f4fc-128">Inköp</span><span class="sxs-lookup"><span data-stu-id="8f4fc-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="8f4fc-129">Hantera projekt</span><span class="sxs-lookup"><span data-stu-id="8f4fc-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="8f4fc-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f4fc-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

