---
title: "Så här skapar du arbetsflödesanvändare | Microsoft Docs"
description: "Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå i arbetsflödena. Det behövs för att ange till exempel vem som ska ta emot en notering för att agera på ett arbetsflödessteg."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0fe05d44acd7fb163996e8a663adb309d229b203
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-workflow-users"></a><span data-ttu-id="67288-104">Konfigurera arbetsflödesanvändare</span><span class="sxs-lookup"><span data-stu-id="67288-104">Set Up Workflow Users</span></span>
<span data-ttu-id="67288-105">Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå i arbetsflödena.</span><span class="sxs-lookup"><span data-stu-id="67288-105">Before you can create workflows, you must set up the users who take part in workflows.</span></span> <span data-ttu-id="67288-106">Det behövs för att ange till exempel vem som ska ta emot en notering för att agera på ett arbetsflödessteg.</span><span class="sxs-lookup"><span data-stu-id="67288-106">This is necessary, for example, to specify who will receive a notification to act on a workflow step.</span></span>  

<span data-ttu-id="67288-107">Konfigurera användare under arbetsflödesanvändargrupper i fönstret **Arbetsflödesanvändargrupp** och ange användarna i ordningsföljd i till exempel en godkännarkedja.</span><span class="sxs-lookup"><span data-stu-id="67288-107">In the **Workflow User Group** window, you set up users under workflow user groups, and you specify the users’ number in a process sequence, such as an approver chain.</span></span>  

<span data-ttu-id="67288-108">Arbetsflödesanvändare som fungerar som godkännandeanvändare, både den som begär och den som godkänner, måste också ställas in i fönstret **Användarinställningar för godkännande**.</span><span class="sxs-lookup"><span data-stu-id="67288-108">Workflow users that function as approval users, both approval requesters and approvers, must also be set up in the **Approval User Setup** window.</span></span> <span data-ttu-id="67288-109">Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="67288-109">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="67288-110">Om du vill definiera att en godkännandebegäran inte godkänns förrän flera godkännare i en godkännandekedja har godkänt den, ställer du in godkännare i en hierarki.</span><span class="sxs-lookup"><span data-stu-id="67288-110">To define that an approval request is not approved until multiple approvers in an approval chain have approved it, set up approvers in a hierarchy.</span></span> <span data-ttu-id="67288-111">För godkännartypen **godkännare** anger du godkännare i fönstret **Användarinställningar för godkännande**.</span><span class="sxs-lookup"><span data-stu-id="67288-111">For approver type **Approver**, set approvers up in the **Approval User Setup** window.</span></span> <span data-ttu-id="67288-112">För godkännartypen **Arbetsflödesanvändargrupp** ställer du in godkännare i fönstret **Arbetsflödesanvändargrupper** och definierar hierarkin genom att tilldela inkrementella nummer till varje godkännare i fältet **Sekvensnr.**</span><span class="sxs-lookup"><span data-stu-id="67288-112">For approver type, **Workflow User Group**, set approvers up in the **Workflow User Groups** window and define the hierarchy by assigning incremental numbers to each approver in the **Sequence No.**</span></span> <span data-ttu-id="67288-113">.</span><span class="sxs-lookup"><span data-stu-id="67288-113">field.</span></span> <span data-ttu-id="67288-114">Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md) och i detta avsnitt.</span><span class="sxs-lookup"><span data-stu-id="67288-114">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md) and this topic.</span></span>  
>   
>  <span data-ttu-id="67288-115">Om du vill definiera att en godkännandebegäran inte godkänns förrän flera likvärdiga godkännare har godkänt den, oberoende av ett hierarki, ställer du in en plan arbetsflödesanvändargrupp.</span><span class="sxs-lookup"><span data-stu-id="67288-115">To define that an approval request is not approved until multiple equal approvers have approved it, regardless of a hierarchy, set up a flat workflow user group.</span></span> <span data-ttu-id="67288-116">För godkännartypen **Arbetsflödesanvändargrupp**, ställer du in godkännare i fönstret **Arbetsflödesanvändargrupper** och definierar samma nummer till varje godkännare i fältet **Sekvensnr.**</span><span class="sxs-lookup"><span data-stu-id="67288-116">For approver type, **Workflow User Group**, set up approvers in the **Workflow User Groups** window and assign the same number to each approver in the **Sequence No.**</span></span> <span data-ttu-id="67288-117">.</span><span class="sxs-lookup"><span data-stu-id="67288-117">field.</span></span> <span data-ttu-id="67288-118">Mer information finns i det här avsnittet.</span><span class="sxs-lookup"><span data-stu-id="67288-118">For more information, see this topic.</span></span>  

### <a name="to-set-up-a-workflow-user"></a><span data-ttu-id="67288-119">Så här konfigurerar du en arbetsflödesanvändare</span><span class="sxs-lookup"><span data-stu-id="67288-119">To set up a workflow user</span></span>  

1. <span data-ttu-id="67288-120">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arbetsflödesanvändargrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="67288-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflow User Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67288-121">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="67288-121">Choose the **New** action.</span></span> <span data-ttu-id="67288-122">Fönstret **Arbetsflödesanvändargrupp** öppnas.</span><span class="sxs-lookup"><span data-stu-id="67288-122">The **Workflow User Group** window opens.</span></span>  
3. <span data-ttu-id="67288-123">Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="67288-123">In the **Code** field, enter a maximum of 20 characters to identify the workflow.</span></span>  
4. <span data-ttu-id="67288-124">Beskriv arbetsflödet i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="67288-124">In the **Description** field, describe the workflow.</span></span>  
5. <span data-ttu-id="67288-125">Fyll i fälten på den första raden enligt beskrivningen i följande tabell på snabbfliken **Medlemmar i arbetsflödesanvändargrupp**.</span><span class="sxs-lookup"><span data-stu-id="67288-125">On the **Workflow User Group Members** FastTab, fill the fields on the first line as described in the following table.</span></span>  

    |<span data-ttu-id="67288-126">Fält</span><span class="sxs-lookup"><span data-stu-id="67288-126">Field</span></span>|<span data-ttu-id="67288-127">Description</span><span class="sxs-lookup"><span data-stu-id="67288-127">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="67288-128">**Användarnamn**</span><span class="sxs-lookup"><span data-stu-id="67288-128">**User Name**</span></span>|<span data-ttu-id="67288-129">Ange användaren som ska ingå i arbetsflöden.</span><span class="sxs-lookup"><span data-stu-id="67288-129">Specify the user who will take part in workflows.</span></span><br /><br /> <span data-ttu-id="67288-130">Användaren måste finnas i fönstret **Användarinställningar**.</span><span class="sxs-lookup"><span data-stu-id="67288-130">The user must exist in the **User Setup** window.</span></span> <span data-ttu-id="67288-131">Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="67288-131">For more information, see [Manage Users and Permissions](ui-how-users-permissions.md).</span></span>|  
    |<span data-ttu-id="67288-132">**Sekvensnr**</span><span class="sxs-lookup"><span data-stu-id="67288-132">**Sequence No.**</span></span>|<span data-ttu-id="67288-133">Ange den ordning som arbetsflödesanvändaren agerar i ett arbetsflöde i förhållanden till andra användare.</span><span class="sxs-lookup"><span data-stu-id="67288-133">Specify the order in which the workflow user engages in a workflow relative to other users.</span></span> <span data-ttu-id="67288-134">Detta fält kan användas, till exempel, för att ange när användaren godkänner i förhållande till andra godkännare när du använder alternativet **Arbetsflödesanvändargrupp** i fältet **Godkännartyp** på det relaterade arbetsflödesvaret.</span><span class="sxs-lookup"><span data-stu-id="67288-134">This field can be used, for example, to specify when the user approves relative to other approvers when you use the **Workflow User Group** option in the **Approver Type** field on the related workflow response.</span></span> <span data-ttu-id="67288-135">**Tips!** Om du vill definiera att en godkännandebegäran inte godkänns förrän flera godkännare har godkänt den, oavsett plats i en hierarki, ställer du in en plan arbetsflödeanvändargrupp genom att tilldela samma sekvensnumret till de relevanta godkännarna.</span><span class="sxs-lookup"><span data-stu-id="67288-135">**TIP:**  To define that an approval request is not approved until multiple equal approvers have approved it, irrespective of a hierarchy, set up a flat workflow user group by assigning the same sequence number to the relevant approvers.</span></span>|  
6. <span data-ttu-id="67288-136">Upprepa steg 5 för att lägga till fler arbetsflödesanvändare i användargruppen.</span><span class="sxs-lookup"><span data-stu-id="67288-136">Repeat step 5 to add more workflow users to the user group.</span></span>  
7. <span data-ttu-id="67288-137">Upprepa steg 2 till 6 för att lägga till fler arbetsflödesanvändargrupper.</span><span class="sxs-lookup"><span data-stu-id="67288-137">Repeat steps 2 through 6 to add more workflow user groups.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67288-138">Se även</span><span class="sxs-lookup"><span data-stu-id="67288-138">See Also</span></span>  
<span data-ttu-id="67288-139">[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md) </span><span class="sxs-lookup"><span data-stu-id="67288-139">[Set Up Approval Users](across-how-to-set-up-approval-users.md) </span></span>  
<span data-ttu-id="67288-140">[Konfigurera arbetsflöden](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="67288-140">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="67288-141">[Använda arbetsflöden](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="67288-141">[Using Workflows](across-use-workflows.md) </span></span>  
<span data-ttu-id="67288-142">[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="67288-142">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
[<span data-ttu-id="67288-143">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="67288-143">Workflow</span></span>](across-workflow.md)   
