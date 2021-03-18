---
title: Aviseringar för arbetsflöde
description: Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på. Till exempel i en arbetsflödessteg kan händelsen vara att användare 1 begär godkännande av en ny post och åtgärden är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten och åtgärden är att ett meddelande skickas till användare 3, som ska starta en relaterad bearbetning av den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: d11a391a7fd91f6a094dfae9f8908ba4314b357a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378954"
---
# <a name="workflow-notifications"></a><span data-ttu-id="f4448-106">Aviseringar för arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="f4448-106">Workflow Notifications</span></span>

<span data-ttu-id="f4448-107">Konfigurera dina arbetsflöden så att användarna automatiskt meddelas när deras uppmärksamhet krävs för ett steg i det arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="f4448-107">Set up your workflows to automatically notify users when their attention is required for a step in that workflow.</span></span> <span data-ttu-id="f4448-108">Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på.</span><span class="sxs-lookup"><span data-stu-id="f4448-108">Many workflow responses are about notifying a user that an event has occurred that they must act on.</span></span> <span data-ttu-id="f4448-109">Till exempel i en arbetsflödessteg kan händelsen vara att användare 1 begär godkännande av en ny post och åtgärden är att ett meddelande skickas till användare 2, godkännaren.</span><span class="sxs-lookup"><span data-stu-id="f4448-109">For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="f4448-110">I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten och åtgärden är att ett meddelande skickas till användare 3, som ska starta en relaterad bearbetning av den godkända posten.</span><span class="sxs-lookup"><span data-stu-id="f4448-110">On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record.</span></span> <span data-ttu-id="f4448-111">För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost.</span><span class="sxs-lookup"><span data-stu-id="f4448-111">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="f4448-112">Mer information finns i [Arbetsflöden](across-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-112">For more information, see [Workflow](across-workflow.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="f4448-113">Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder meddelanden som e-post och interna noteringar.</span><span class="sxs-lookup"><span data-stu-id="f4448-113">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports notifications as email and as internal notes.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="f4448-114">Alla arbetsflödesmeddelanden skickas via en jobbkö.</span><span class="sxs-lookup"><span data-stu-id="f4448-114">All workflow notifications are sent through a job queue.</span></span> <span data-ttu-id="f4448-115">Se till att jobbkön i din installation är konfigurerad för att hantera arbetsflödesmeddelanden och att kryssrutan **Starta automatiskt från server** är markerad.</span><span class="sxs-lookup"><span data-stu-id="f4448-115">Make sure that the job queue in your installation is set up to handle workflow notifications, and that the **Start Automatically From Server** check box is selected.</span></span> <span data-ttu-id="f4448-116">Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-116">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="set-up-notifications"></a><span data-ttu-id="f4448-117">Ställa in aviseringar</span><span class="sxs-lookup"><span data-stu-id="f4448-117">Set up notifications</span></span>

<span data-ttu-id="f4448-118">Du konfigurerar andra aspekter av arbetsflödesmeddelanden på flera ställen:</span><span class="sxs-lookup"><span data-stu-id="f4448-118">You set up different aspects of workflow notifications in the following places:</span></span>  

* <span data-ttu-id="f4448-119">Godkännaravisering</span><span class="sxs-lookup"><span data-stu-id="f4448-119">Approver notification</span></span>

    <span data-ttu-id="f4448-120">För godkännande arbetsflöden konfigurerar du mottagare av arbetsflödemeddelanden genom att fylla i en rad på sidan **Användarinställningar för godkännande** för varje användare som ingår i arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="f4448-120">For approval workflows, you set up the recipients of workflow notifications by filling a line on the **Approval User Setup** page for each user that takes part in the workflow.</span></span>  

    <span data-ttu-id="f4448-121">Till exempel om användare 2 är specificerat i fältet **Godkännar-ID** på raden för användare 1 så skickas meddelandet om godkännandebegäran till användare 1.</span><span class="sxs-lookup"><span data-stu-id="f4448-121">For example, if User 2 is specified in the **Approver ID** field on the line for User 1, then the approval request notification is sent to User 1.</span></span> <span data-ttu-id="f4448-122">Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  
* <span data-ttu-id="f4448-123">Meddelandescheman</span><span class="sxs-lookup"><span data-stu-id="f4448-123">Notification schedules</span></span>

    <span data-ttu-id="f4448-124">Du definierar när och hur användarna får arbetsflödemeddelanden genom att fylla i sidan **Meddelandeschema** för varje arbetsflödesanvändare.</span><span class="sxs-lookup"><span data-stu-id="f4448-124">You set up when and how users receive workflow notifications by filling the **Notification Schedule** page for each workflow user.</span></span> <span data-ttu-id="f4448-125">Mer information finns i [Så här anger du när och hur användare ska meddelas](across-how-to-specify-when-and-how-to-receive-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-125">For more information, see [Specify When and How to Receive Notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).</span></span>  
* <span data-ttu-id="f4448-126">Anpassa e-postaviseringarna</span><span class="sxs-lookup"><span data-stu-id="f4448-126">Customize the email notifications</span></span>

    <span data-ttu-id="f4448-127">Om du vill kan anpassa du innehållet i e-postmeddelanden genom att ändra rapporten 1320, e-postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="f4448-127">If you want, you can customize the content of the email notification by modifying report 1320, Notification Email.</span></span> <span data-ttu-id="f4448-128">Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-128">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>  
* <span data-ttu-id="f4448-129">Svarsalternativ</span><span class="sxs-lookup"><span data-stu-id="f4448-129">Response options</span></span>

    <span data-ttu-id="f4448-130">Du konfigurerar specifikt innehåll och regler för ett arbetsflödemeddelande när du skapar arbetsflödet i fråga.</span><span class="sxs-lookup"><span data-stu-id="f4448-130">You set up specific content and rules of a workflow notification when you create the workflow in question.</span></span> <span data-ttu-id="f4448-131">Du gör detta genom att välja alternativ på sidan **Alternativ för arbetsflödessvar** för de arbetsflödessvar som representerar meddelandet.</span><span class="sxs-lookup"><span data-stu-id="f4448-131">You do this by selecting options on the **Workflow Response Options** page for the workflow response that represents the notification.</span></span> <span data-ttu-id="f4448-132">Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-132">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

* <span data-ttu-id="f4448-133">Meddela avsändare</span><span class="sxs-lookup"><span data-stu-id="f4448-133">Notify sender</span></span>

    <span data-ttu-id="f4448-134">För arbetsflöden för godkännande lägger du till ett arbetsflödessvarssteg för att meddela avsändaren när begäran har godkänts eller avvisats.</span><span class="sxs-lookup"><span data-stu-id="f4448-134">For approval workflows, add a workflow response step to notify the sender when the request has been approved or rejected.</span></span> <span data-ttu-id="f4448-135">Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f4448-135">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f4448-136">Se även</span><span class="sxs-lookup"><span data-stu-id="f4448-136">See Also</span></span>

[<span data-ttu-id="f4448-137">Konfigurera användare för godkännande</span><span class="sxs-lookup"><span data-stu-id="f4448-137">Set Up Approval Users</span></span>](across-how-to-set-up-approval-users.md)  
[<span data-ttu-id="f4448-138">Konfigurera arbetsflödesanvändare</span><span class="sxs-lookup"><span data-stu-id="f4448-138">Set Up Workflow Users</span></span>](across-how-to-set-up-workflow-users.md)  
[<span data-ttu-id="f4448-139">Ange när och hur meddelanden ska tas emot</span><span class="sxs-lookup"><span data-stu-id="f4448-139">Specify When and How to Receive Notifications</span></span>](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[<span data-ttu-id="f4448-140">Skapa arbetsflöden</span><span class="sxs-lookup"><span data-stu-id="f4448-140">Create Workflows</span></span>](across-how-to-create-workflows.md)  
[<span data-ttu-id="f4448-141">Skapa och ändra anpassade rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="f4448-141">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="f4448-142">Använda jobbköer för att schemalägga uppgifter</span><span class="sxs-lookup"><span data-stu-id="f4448-142">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="f4448-143">Konfigurera e-post</span><span class="sxs-lookup"><span data-stu-id="f4448-143">Set up Email</span></span>](admin-how-setup-email.md)  
[<span data-ttu-id="f4448-144">Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp</span><span class="sxs-lookup"><span data-stu-id="f4448-144">Walkthrough: Setting Up and Using a Purchase Approval Workflow</span></span>](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[<span data-ttu-id="f4448-145">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="f4448-145">Workflow</span></span>](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]