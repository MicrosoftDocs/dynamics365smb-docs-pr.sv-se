---
title: Använda arbetsflöden
description: Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Lär dig mer om de olika åtgärder du måste vidta för att börja använda arbetsflöden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787013"
---
# <a name="using-workflows"></a><span data-ttu-id="f0361-104">Använda arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="f0361-104">Using Workflows</span></span>
<span data-ttu-id="f0361-105">Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare.</span><span class="sxs-lookup"><span data-stu-id="f0361-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="f0361-106">Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter.</span><span class="sxs-lookup"><span data-stu-id="f0361-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="f0361-107">Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.</span><span class="sxs-lookup"><span data-stu-id="f0361-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="f0361-108">Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare, skapa arbetsflöden, eventuellt tillämpa föregående kodanpassning och ange hur användarna ska meddelas.</span><span class="sxs-lookup"><span data-stu-id="f0361-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="f0361-109">Mer information finns i [Konfigurera arbetsflöden](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f0361-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f0361-110">Vanliga arbetsflödessteg är när användare begär godkännande av aktiviteter och godkännare accepterar eller avvisar godkännandebegäranden.</span><span class="sxs-lookup"><span data-stu-id="f0361-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="f0361-111">Därför handlar många avsnitt om hur du använder arbetsflöden i godkännande.</span><span class="sxs-lookup"><span data-stu-id="f0361-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="f0361-112">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="f0361-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="f0361-113">**För att**</span><span class="sxs-lookup"><span data-stu-id="f0361-113">**To**</span></span>|<span data-ttu-id="f0361-114">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="f0361-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="f0361-115">Ange ett arbetsflöde för att starta när den första instegshändelsen inträffar.</span><span class="sxs-lookup"><span data-stu-id="f0361-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="f0361-116">Så här aktiverar du arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="f0361-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="f0361-117">Begär godkännande för en aktivitet, som en godkännare, acceptera, avvisa eller delegera godkännanden och skicka eller visa godkännandemeddelanden.</span><span class="sxs-lookup"><span data-stu-id="f0361-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="f0361-118">Använda arbetsflöden för godkännande</span><span class="sxs-lookup"><span data-stu-id="f0361-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="f0361-119">Skapa arbetsflödessteg som begränsar en viss posttyp från att användas innan en viss händelse uppstår, till exempel att posten godkänns.</span><span class="sxs-lookup"><span data-stu-id="f0361-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="f0361-120">Begränsa och tillåt användningen av en post</span><span class="sxs-lookup"><span data-stu-id="f0361-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="f0361-121">Visa avslutade arbetsflödessteginstanser med statusen Avslutat.</span><span class="sxs-lookup"><span data-stu-id="f0361-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="f0361-122">Visa arkiverade instanser för arbetsflödessteg</span><span class="sxs-lookup"><span data-stu-id="f0361-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="f0361-123">Ta bort ett arbetsflöde som du vet inte ska användas längre.</span><span class="sxs-lookup"><span data-stu-id="f0361-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="f0361-124">Ta bort arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="f0361-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="f0361-125">Se även</span><span class="sxs-lookup"><span data-stu-id="f0361-125">See Also</span></span>  
<span data-ttu-id="f0361-126">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f0361-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="f0361-127">[Arbetsflöde](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="f0361-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="f0361-128">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0361-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]