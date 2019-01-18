---
title: "Tjänsteorderstatus och reparationsstatus | Microsoft Docs"
description: "Fältet Status på sidan Serviceorder och serviceartikelns reparationsstatus som visas i fältet Reparationsstatuskod på sidan Serviceorder har ett visst samband i modulen Servicehantering Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a7ef1f214bda9c78113b320ddbd331b5a3e7de33
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="55755-104">Tjänsteorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="55755-104">Service Order Status and Repair Status</span></span>
<span data-ttu-id="55755-105">Fältet **Status** på sidan **Serviceorder** och serviceartikelns reparationsstatus som visas i fältet **Reparationsstatuskod** på sidan **Serviceorder** har ett visst samband i Servicehantering</span><span class="sxs-lookup"><span data-stu-id="55755-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="55755-106">Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.</span><span class="sxs-lookup"><span data-stu-id="55755-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="55755-107">De två statusfälten är inte kopplade till fältet **Släppningsstatus** i huvudet på serviceordern, som styr lagerhanteringen av serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="55755-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

 <span data-ttu-id="55755-108">När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status.</span><span class="sxs-lookup"><span data-stu-id="55755-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="55755-109">För att se den status som anger den generella reparationsstatusen för enskilda serviceartiklar måste du ange följande:</span><span class="sxs-lookup"><span data-stu-id="55755-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="55755-110">Den serviceorderstatus som respektive reparationsstatus är länkad till.</span><span class="sxs-lookup"><span data-stu-id="55755-110">The service order status that each repair status is linked to.</span></span> <span data-ttu-id="55755-111">Mer information finns i Tjänsteorderstatus.</span><span class="sxs-lookup"><span data-stu-id="55755-111">For more information, see Service Order Status.</span></span>  
* <span data-ttu-id="55755-112">Prioritetsnivå för varje serverorderstatusalternativ.</span><span class="sxs-lookup"><span data-stu-id="55755-112">The level of priority of each service order status option.</span></span> <span data-ttu-id="55755-113">Mer information finns i Prioritet.</span><span class="sxs-lookup"><span data-stu-id="55755-113">For more information, see Priority.</span></span>  

 <span data-ttu-id="55755-114">När du omvandlar en serviceoffert till en serviceorder ändras reparationsstatus för alla serviceartiklar i ordern till **Initial** och serviceorderstatusen till **Förestående**.</span><span class="sxs-lookup"><span data-stu-id="55755-114">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="55755-115">Ange serviceorderstatus för reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="55755-115">Specifying Service Order Status for Repair Status</span></span>  
<span data-ttu-id="55755-116">Varje reparationsstatus är länkad till en viss serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="55755-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="55755-117">Alternativen för serviceorderstatus är **Förestående**, **På gång**, **Stoppad** och **Avslutad**.</span><span class="sxs-lookup"><span data-stu-id="55755-117">The options for the service order status are as follows: **Pending**, **In Process**, **On Hold**, and **Finished**.</span></span> <span data-ttu-id="55755-118">Det finns nio olika alternativ för reparationsstatus: **Initial**, **På gång**, **Hänvisad**, **Delvis servad**, **Offert avslutad**, **Väntar på kund**, **Beställt reservdelar**, **Reservdelar inlevererade** och **Avslutad**.</span><span class="sxs-lookup"><span data-stu-id="55755-118">The repair status options are as follows: **Initial**, **In Process**, **Referred**, **Partly Serviced**, **Quote Finished**, **Waiting for Customer**, **Spare Part Ordered**, **Spare Part Received**, and **Finished**.</span></span>  

### <a name="pending"></a><span data-ttu-id="55755-119">Förestående</span><span class="sxs-lookup"><span data-stu-id="55755-119">Pending</span></span>  
<span data-ttu-id="55755-120">Tjänsteorderstatusen **Förestående** anger att servicen kan inledas eller fortsätta när som helst.</span><span class="sxs-lookup"><span data-stu-id="55755-120">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="55755-121">Därför kan fyra av alternativen för reparationsstatus, nämligen **Initial**, **Hänvisad**, **Delvis servad** och **Reservdelar inlevererade**, alla länkas till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="55755-121">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="55755-122">Pågående</span><span class="sxs-lookup"><span data-stu-id="55755-122">In Process</span></span>  
<span data-ttu-id="55755-123">Tjänsteorderstatusen **På gång** anger att servicen pågår.</span><span class="sxs-lookup"><span data-stu-id="55755-123">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="55755-124">Därför kan två av alternativen för reparationsstatus, nämligen **På gång** och **Beställt reservdelar**, länkas till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="55755-124">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="55755-125">Om du länkar statusen **Beställt reservdelar** till servicestatusen **På gång** måste du även länka statusen **Beställt reservdelar** till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="55755-125">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="55755-126">Stoppad</span><span class="sxs-lookup"><span data-stu-id="55755-126">On Hold</span></span>  
<span data-ttu-id="55755-127">Tjänsteorderstatusen **Stoppad** anger att servicen tillfälligt har stoppats i väntan på svar från kunden eller reservdelar innan servicen kan inledas.</span><span class="sxs-lookup"><span data-stu-id="55755-127">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="55755-128">Därför kan tre av alternativen för reparationsstatus, nämligen **Offert avslutad**, **Beställt reservdelar** och **Väntar på kund**, alla länkas till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="55755-128">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="55755-129">Avslutad</span><span class="sxs-lookup"><span data-stu-id="55755-129">Finished</span></span>  
<span data-ttu-id="55755-130">Tjänsteorderstatusen **Avslutad** anger att servicen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="55755-130">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="55755-131">Därför är reparationsstatusen **Avslutad** länkad till den här statusen.</span><span class="sxs-lookup"><span data-stu-id="55755-131">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="55755-132">Tilldela en serviceorderstatus prioritet</span><span class="sxs-lookup"><span data-stu-id="55755-132">Assigning Priority to Service Order Status</span></span>  
<span data-ttu-id="55755-133">När du ändrar reparationsstatus för en serviceartikel identifieras de serviceorderstatusalternativ som är länkade till olika reparationsstatusalternativ för alla serviceartiklar i ordern.</span><span class="sxs-lookup"><span data-stu-id="55755-133">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="55755-134">Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="55755-134">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="55755-135">Du måste välja vilken serviceorderstatus som innehåller viktigast information om serviceorderstatusen och tilldela den högst prioritet o.s.v.</span><span class="sxs-lookup"><span data-stu-id="55755-135">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

### <a name="example"></a><span data-ttu-id="55755-136">Exempel</span><span class="sxs-lookup"><span data-stu-id="55755-136">Example</span></span>  
<span data-ttu-id="55755-137">En typisk fördelning av prioritetsnivå kan se ut så här:</span><span class="sxs-lookup"><span data-stu-id="55755-137">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="55755-138">Pågående – hög</span><span class="sxs-lookup"><span data-stu-id="55755-138">In Process - High</span></span>  
* <span data-ttu-id="55755-139">Förestående – medelhög</span><span class="sxs-lookup"><span data-stu-id="55755-139">Pending - Medium high</span></span>  
* <span data-ttu-id="55755-140">Stoppad – medellåg</span><span class="sxs-lookup"><span data-stu-id="55755-140">On Hold - Medium low</span></span>  
* <span data-ttu-id="55755-141">Färdig – låg</span><span class="sxs-lookup"><span data-stu-id="55755-141">Finished - Low</span></span>  

<span data-ttu-id="55755-142">Om t.ex. en serviceartikel har reparationsstatus **Initial**, länkad till serviceorderstatus **Förestående**, en annan har **På gång**, länkad till servicestatus **På gång**, och en tredje har **Beställt reservdelar**, länkad till servicestatus **Stoppad**, blir den resulterande serviceorderstatus **På gång** eftersom den har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="55755-142">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="55755-143">Se även</span><span class="sxs-lookup"><span data-stu-id="55755-143">See Also</span></span>  
[<span data-ttu-id="55755-144">Ställ in status för tjänsteorder och reparationer</span><span class="sxs-lookup"><span data-stu-id="55755-144">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="55755-145">Ställa in tjänstehantering</span><span class="sxs-lookup"><span data-stu-id="55755-145">Setting Up Service Management</span></span>](service-setup-service.md)  

