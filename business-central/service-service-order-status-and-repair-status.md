---
title: Tjänsteorderstatus och reparationsstatus
description: Fältet Status på sidan Serviceorder och serviceartikelns reparationsstatus som visas i fältet Reparationsstatuskod på sidan Serviceorder har ett visst samband i modulen Servicehantering Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 9bbe3a4263250a7d06bfffa2019114eba72a31ca
ms.sourcegitcommit: 2d2dfb6c3eca1322835f0167dc7dab614346972e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4038624"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="a109c-104">Tjänsteorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="a109c-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="a109c-105">Fältet **Status** på sidan **Serviceorder** och serviceartikelns reparationsstatus som visas i fältet **Reparationsstatuskod** på sidan **Serviceorder** har ett visst samband i Servicehantering</span><span class="sxs-lookup"><span data-stu-id="a109c-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="a109c-106">Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.</span><span class="sxs-lookup"><span data-stu-id="a109c-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="a109c-107">De två statusfälten är inte kopplade till fältet **Släppningsstatus** i huvudet på serviceordern, som styr lagerhanteringen av serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="a109c-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="a109c-108">När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status.</span><span class="sxs-lookup"><span data-stu-id="a109c-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="a109c-109">För att se den status som anger den generella reparationsstatusen för enskilda serviceartiklar måste du ange följande:</span><span class="sxs-lookup"><span data-stu-id="a109c-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="a109c-110">Den serviceorderstatus som respektive reparationsstatus är länkad till.</span><span class="sxs-lookup"><span data-stu-id="a109c-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="a109c-111">Prioritetsnivå för varje serverorderstatusalternativ.</span><span class="sxs-lookup"><span data-stu-id="a109c-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="a109c-112">När du omvandlar en serviceoffert till en serviceorder ändras reparationsstatus för alla serviceartiklar i ordern till **Initial** och serviceorderstatusen till **Förestående**.</span><span class="sxs-lookup"><span data-stu-id="a109c-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="a109c-113">Innan du kan skapa serviceorder måste du ställa in statusen för reparationer och statusprioriteringar för service.</span><span class="sxs-lookup"><span data-stu-id="a109c-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="a109c-114">Mer information finns i [Ställa in status för om serviceorder och reparationer](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="a109c-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="a109c-115">Ange serviceorderstatus för reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="a109c-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="a109c-116">Varje reparationsstatus är länkad till en viss serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="a109c-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="a109c-117">Alternativen för serviceorderstatusen är följande:</span><span class="sxs-lookup"><span data-stu-id="a109c-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="a109c-118">**Förestående**</span><span class="sxs-lookup"><span data-stu-id="a109c-118">**Pending**</span></span>
* <span data-ttu-id="a109c-119">**Pågående**</span><span class="sxs-lookup"><span data-stu-id="a109c-119">**In Process**</span></span>
* <span data-ttu-id="a109c-120">**Stoppad**</span><span class="sxs-lookup"><span data-stu-id="a109c-120">**On Hold**</span></span>
* <span data-ttu-id="a109c-121">**Avslutad**</span><span class="sxs-lookup"><span data-stu-id="a109c-121">**Finished**</span></span>

<span data-ttu-id="a109c-122">Alternativen för reparationsstatus är följande:</span><span class="sxs-lookup"><span data-stu-id="a109c-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="a109c-123">**Initial**</span><span class="sxs-lookup"><span data-stu-id="a109c-123">**Initial**</span></span>
* <span data-ttu-id="a109c-124">**Pågående**</span><span class="sxs-lookup"><span data-stu-id="a109c-124">**In Process**</span></span>
* <span data-ttu-id="a109c-125">**Refrerad**</span><span class="sxs-lookup"><span data-stu-id="a109c-125">**Referred**</span></span>
* <span data-ttu-id="a109c-126">**Delvist servad**</span><span class="sxs-lookup"><span data-stu-id="a109c-126">**Partly Serviced**</span></span>
* <span data-ttu-id="a109c-127">**Offert avslutad**</span><span class="sxs-lookup"><span data-stu-id="a109c-127">**Quote Finished**</span></span>
* <span data-ttu-id="a109c-128">**Väntar på kund**</span><span class="sxs-lookup"><span data-stu-id="a109c-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="a109c-129">**Reservdel beställd**</span><span class="sxs-lookup"><span data-stu-id="a109c-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="a109c-130">**Reservdel inlevererad**</span><span class="sxs-lookup"><span data-stu-id="a109c-130">**Spare Part Received**</span></span>
* <span data-ttu-id="a109c-131">**Avslutad**</span><span class="sxs-lookup"><span data-stu-id="a109c-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="a109c-132">Förestående</span><span class="sxs-lookup"><span data-stu-id="a109c-132">Pending</span></span>

<span data-ttu-id="a109c-133">Tjänsteorderstatusen **Förestående** anger att servicen kan inledas eller fortsätta när som helst.</span><span class="sxs-lookup"><span data-stu-id="a109c-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="a109c-134">Därför kan fyra av alternativen för reparationsstatus, nämligen **Initial**, **Hänvisad**, **Delvis servad** och **Reservdelar inlevererade**, alla länkas till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="a109c-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="a109c-135">Pågående</span><span class="sxs-lookup"><span data-stu-id="a109c-135">In Process</span></span>

<span data-ttu-id="a109c-136">Tjänsteorderstatusen **På gång** anger att servicen pågår.</span><span class="sxs-lookup"><span data-stu-id="a109c-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="a109c-137">Därför kan två av alternativen för reparationsstatus, nämligen **På gång** och **Beställt reservdelar**, länkas till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="a109c-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="a109c-138">Om du länkar statusen **Beställt reservdelar** till servicestatusen **På gång** måste du även länka statusen **Beställt reservdelar** till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="a109c-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="a109c-139">Stoppad</span><span class="sxs-lookup"><span data-stu-id="a109c-139">On Hold</span></span>

<span data-ttu-id="a109c-140">Tjänsteorderstatusen **Stoppad** anger att servicen tillfälligt har stoppats i väntan på svar från kunden eller reservdelar innan servicen kan inledas.</span><span class="sxs-lookup"><span data-stu-id="a109c-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="a109c-141">Därför kan tre av alternativen för reparationsstatus, nämligen **Offert avslutad**, **Beställt reservdelar** och **Väntar på kund**, alla länkas till den här serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="a109c-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="a109c-142">Avslutad</span><span class="sxs-lookup"><span data-stu-id="a109c-142">Finished</span></span>

<span data-ttu-id="a109c-143">Tjänsteorderstatusen **Avslutad** anger att servicen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="a109c-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="a109c-144">Därför är reparationsstatusen **Avslutad** länkad till den här statusen.</span><span class="sxs-lookup"><span data-stu-id="a109c-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="a109c-145">Tilldela en serviceorderstatus prioritet</span><span class="sxs-lookup"><span data-stu-id="a109c-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="a109c-146">När du ändrar reparationsstatus för en serviceartikel identifieras de serviceorderstatusalternativ som är länkade till olika reparationsstatusalternativ för alla serviceartiklar i ordern.</span><span class="sxs-lookup"><span data-stu-id="a109c-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="a109c-147">Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="a109c-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="a109c-148">Du måste välja vilken serviceorderstatus som innehåller viktigast information om serviceorderstatusen och tilldela den högst prioritet o.s.v.</span><span class="sxs-lookup"><span data-stu-id="a109c-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="a109c-149">När du sedan skapar en ny serviceorder och lägger till serviceartiklar i den uppdateras fältet **Prioritet** serviceorderhuvudet baserat på prioriteringarna för serviceartiklarna.</span><span class="sxs-lookup"><span data-stu-id="a109c-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="a109c-150">Exempel</span><span class="sxs-lookup"><span data-stu-id="a109c-150">Example</span></span>

<span data-ttu-id="a109c-151">En typisk fördelning av prioritetsnivå kan se ut så här:</span><span class="sxs-lookup"><span data-stu-id="a109c-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="a109c-152">Pågående – hög</span><span class="sxs-lookup"><span data-stu-id="a109c-152">In Process - High</span></span>  
* <span data-ttu-id="a109c-153">Förestående – medelhög</span><span class="sxs-lookup"><span data-stu-id="a109c-153">Pending - Medium high</span></span>  
* <span data-ttu-id="a109c-154">Stoppad – medellåg</span><span class="sxs-lookup"><span data-stu-id="a109c-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="a109c-155">Färdig – låg</span><span class="sxs-lookup"><span data-stu-id="a109c-155">Finished - Low</span></span>  

<span data-ttu-id="a109c-156">Om t.ex. en serviceartikel har reparationsstatus **Initial**, länkad till serviceorderstatus **Förestående**, en annan har **På gång**, länkad till servicestatus **På gång**, och en tredje har **Beställt reservdelar**, länkad till servicestatus **Stoppad**, blir den resulterande serviceorderstatus **På gång** eftersom den har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="a109c-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a109c-157">Se även</span><span class="sxs-lookup"><span data-stu-id="a109c-157">See Also</span></span>

[<span data-ttu-id="a109c-158">Ställ in status för tjänsteorder och reparationer</span><span class="sxs-lookup"><span data-stu-id="a109c-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="a109c-159">Ställa in tjänstehantering</span><span class="sxs-lookup"><span data-stu-id="a109c-159">Setting Up Service Management</span></span>](service-setup-service.md)  
