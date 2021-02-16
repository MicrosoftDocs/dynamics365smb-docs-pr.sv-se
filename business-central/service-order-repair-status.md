---
title: 'Så här: ställa in status för serviceorder och reparationer | Microsoft Docs'
description: Du måste ställa in nio olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: f9b8fa679254e4886993ee29a1ceba1cf2542cda
ms.sourcegitcommit: 2d2dfb6c3eca1322835f0167dc7dab614346972e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4038466"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="1be25-103">Ställ in status för serviceorder och reparationer</span><span class="sxs-lookup"><span data-stu-id="1be25-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="1be25-104">Du måste ställa in olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.</span><span class="sxs-lookup"><span data-stu-id="1be25-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="1be25-105">Du måste skapa åtminstone nio reparationsstatusalternativ som identifierar situationer eller åtgärder som vidtagits då serviceartiklar servas.</span><span class="sxs-lookup"><span data-stu-id="1be25-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="1be25-106">Du kan ange prioriteringsnivåer för alternativen för serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="1be25-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="1be25-107">De fyra prioriteringarna är **Hög**, **Medelhög**, **Medellåg** och **Låg**.</span><span class="sxs-lookup"><span data-stu-id="1be25-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="1be25-108">När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status.</span><span class="sxs-lookup"><span data-stu-id="1be25-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="1be25-109">Varje serviceartikels reparationsstatus är kopplad till serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="1be25-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="1be25-110">Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="1be25-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="1be25-111">Innan du kan ställa in en reparationsstatus måste du ställa in statusprioriteringar för service.</span><span class="sxs-lookup"><span data-stu-id="1be25-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="1be25-112">Så här skapar du servicestatusprioriteter</span><span class="sxs-lookup"><span data-stu-id="1be25-112">To set up service status priorities</span></span>

1. <span data-ttu-id="1be25-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tjänstorderstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1be25-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1be25-114">Välj den serviceorderstatus som du vill ange prioritet för.</span><span class="sxs-lookup"><span data-stu-id="1be25-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="1be25-115">I fältet **Prioritet** väljer du önskad prioritet för aktuell serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="1be25-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="1be25-116">Upprepa steg 2 och 3 tills du har angett en prioritet för vart och ett av de fyra statusalternativen: **Förestående**, **Pågående**, **Avslutad** och **Pausad**.</span><span class="sxs-lookup"><span data-stu-id="1be25-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="1be25-117">Så här skapar du en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="1be25-117">To set up a repair status</span></span>

1. <span data-ttu-id="1be25-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **reparationsstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1be25-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="1be25-119">Skapa en ny reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="1be25-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="1be25-120">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="1be25-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="1be25-121">I fältet **serviceorderstatus** väljer du orderstatus att länka reparationsstatusen till.</span><span class="sxs-lookup"><span data-stu-id="1be25-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="1be25-122">Fältet **Prioritet** visar prioriteten för den serviceorderstatus som du har valt.</span><span class="sxs-lookup"><span data-stu-id="1be25-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="1be25-123">Välj en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="1be25-123">Choose a repair status.</span></span> <span data-ttu-id="1be25-124">Du kan bara välja en.</span><span class="sxs-lookup"><span data-stu-id="1be25-124">You can choose only one.</span></span> <span data-ttu-id="1be25-125">Reparationsstatus kan inte kopplas till mer än ett reparationsstatusalternativ.</span><span class="sxs-lookup"><span data-stu-id="1be25-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="1be25-126">Välj fältet **Bokföring tillåten** om du vill kunna bokföra serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="1be25-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="1be25-127">Markera kryssrutan **Förestående status tillåten** om du vill kunna ändra serviceorderns status manuellt till alternativet **Förestående** på serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="1be25-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="1be25-128">Markera kryssrutorna **Pågående status tillåten**, **Färdig status tillåten** och **Stoppad status tillåten** på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="1be25-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="1be25-129">Upprepa dessa stegen för respektive reparationsstatusalternativ som du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="1be25-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="1be25-130">Se även</span><span class="sxs-lookup"><span data-stu-id="1be25-130">See Also</span></span>

[<span data-ttu-id="1be25-131">Serviceorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="1be25-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="1be25-132">Ställa in tjänstehantering</span><span class="sxs-lookup"><span data-stu-id="1be25-132">Setting Up Service Management</span></span>](service-setup-service.md)  
