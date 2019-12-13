---
title: Använda arbetsflöden | Microsoft Docs
description: Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 87aa8d8cce10bb07636ee97958af7f9e14afc13a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879313"
---
# <a name="using-workflows"></a><span data-ttu-id="7d971-105">Använda arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="7d971-105">Using Workflows</span></span>
<span data-ttu-id="7d971-106">Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare.</span><span class="sxs-lookup"><span data-stu-id="7d971-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="7d971-107">Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter.</span><span class="sxs-lookup"><span data-stu-id="7d971-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="7d971-108">Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.</span><span class="sxs-lookup"><span data-stu-id="7d971-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="7d971-109">Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare, skapa arbetsflöden, eventuellt tillämpa föregående kodanpassning och ange hur användarna ska meddelas.</span><span class="sxs-lookup"><span data-stu-id="7d971-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="7d971-110">Mer information finns i [Konfigurera arbetsflöden](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="7d971-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7d971-111">Vanliga arbetsflödessteg är när användare begär godkännande av aktiviteter och godkännare accepterar eller avvisar godkännandebegäranden.</span><span class="sxs-lookup"><span data-stu-id="7d971-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="7d971-112">Därför handlar många avsnitt om hur du använder arbetsflöden i godkännande.</span><span class="sxs-lookup"><span data-stu-id="7d971-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="7d971-113">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="7d971-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="7d971-114">**För att**</span><span class="sxs-lookup"><span data-stu-id="7d971-114">**To**</span></span>|<span data-ttu-id="7d971-115">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="7d971-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="7d971-116">Ange ett arbetsflöde för att starta när den första instegshändelsen inträffar.</span><span class="sxs-lookup"><span data-stu-id="7d971-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="7d971-117">Så här aktiverar du arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="7d971-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="7d971-118">Begär godkännande för en aktivitet, som en godkännare, acceptera, avvisa eller delegera godkännanden och skicka eller visa godkännandemeddelanden.</span><span class="sxs-lookup"><span data-stu-id="7d971-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="7d971-119">Använda arbetsflöden för godkännande</span><span class="sxs-lookup"><span data-stu-id="7d971-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="7d971-120">Skapa arbetsflödessteg som begränsar en viss posttyp från att användas innan en viss händelse uppstår, till exempel att posten godkänns.</span><span class="sxs-lookup"><span data-stu-id="7d971-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="7d971-121">Begränsa och tillåt användningen av en post</span><span class="sxs-lookup"><span data-stu-id="7d971-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="7d971-122">Visa avslutade arbetsflödessteginstanser med statusen Avslutat.</span><span class="sxs-lookup"><span data-stu-id="7d971-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="7d971-123">Visa arkiverade instanser för arbetsflödessteg</span><span class="sxs-lookup"><span data-stu-id="7d971-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="7d971-124">Ta bort ett arbetsflöde som du vet inte ska användas längre.</span><span class="sxs-lookup"><span data-stu-id="7d971-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="7d971-125">Ta bort arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="7d971-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="7d971-126">Se även</span><span class="sxs-lookup"><span data-stu-id="7d971-126">See Also</span></span>  
<span data-ttu-id="7d971-127">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="7d971-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="7d971-128">[Arbetsflöde](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="7d971-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="7d971-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d971-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
