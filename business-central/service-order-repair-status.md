---
title: 'Så här: ställa in status för serviceorder och reparationer | Microsoft Docs'
description: Du måste ställa in nio olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cb6ba334d4584d6e3ead25606a612686258eae9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776822"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="bc27b-103">Ställ in status för serviceorder och reparationer</span><span class="sxs-lookup"><span data-stu-id="bc27b-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="bc27b-104">Du måste ställa in olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.</span><span class="sxs-lookup"><span data-stu-id="bc27b-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="bc27b-105">Du måste skapa åtminstone nio reparationsstatusalternativ som identifierar situationer eller åtgärder som vidtagits då serviceartiklar servas.</span><span class="sxs-lookup"><span data-stu-id="bc27b-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="bc27b-106">Du kan ange prioriteringsnivåer för alternativen för serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="bc27b-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="bc27b-107">De fyra prioriteringarna är **Hög**, **Medelhög**, **Medellåg** och **Låg**.</span><span class="sxs-lookup"><span data-stu-id="bc27b-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="bc27b-108">När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status.</span><span class="sxs-lookup"><span data-stu-id="bc27b-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="bc27b-109">Varje serviceartikels reparationsstatus är kopplad till serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="bc27b-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="bc27b-110">Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="bc27b-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="bc27b-111">Innan du kan ställa in en reparationsstatus måste du ställa in statusprioriteringar för service.</span><span class="sxs-lookup"><span data-stu-id="bc27b-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="bc27b-112">Så här skapar du servicestatusprioriteter</span><span class="sxs-lookup"><span data-stu-id="bc27b-112">To set up service status priorities</span></span>

1. <span data-ttu-id="bc27b-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tjänstorderstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bc27b-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc27b-114">Välj den serviceorderstatus som du vill ange prioritet för.</span><span class="sxs-lookup"><span data-stu-id="bc27b-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="bc27b-115">I fältet **Prioritet** väljer du önskad prioritet för aktuell serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="bc27b-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="bc27b-116">Upprepa steg 2 och 3 tills du har angett en prioritet för vart och ett av de fyra statusalternativen: **Förestående**, **Pågående**, **Avslutad** och **Pausad**.</span><span class="sxs-lookup"><span data-stu-id="bc27b-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="bc27b-117">Så här skapar du en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="bc27b-117">To set up a repair status</span></span>

1. <span data-ttu-id="bc27b-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **reparationsstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bc27b-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc27b-119">Skapa en ny reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="bc27b-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="bc27b-120">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="bc27b-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="bc27b-121">I fältet **serviceorderstatus** väljer du orderstatus att länka reparationsstatusen till.</span><span class="sxs-lookup"><span data-stu-id="bc27b-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="bc27b-122">Fältet **Prioritet** visar prioriteten för den serviceorderstatus som du har valt.</span><span class="sxs-lookup"><span data-stu-id="bc27b-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="bc27b-123">Välj en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="bc27b-123">Choose a repair status.</span></span> <span data-ttu-id="bc27b-124">Du kan bara välja en.</span><span class="sxs-lookup"><span data-stu-id="bc27b-124">You can choose only one.</span></span> <span data-ttu-id="bc27b-125">Reparationsstatus kan inte kopplas till mer än ett reparationsstatusalternativ.</span><span class="sxs-lookup"><span data-stu-id="bc27b-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="bc27b-126">Välj fältet **Bokföring tillåten** om du vill kunna bokföra serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="bc27b-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="bc27b-127">Markera kryssrutan **Förestående status tillåten** om du vill kunna ändra serviceorderns status manuellt till alternativet **Förestående** på serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="bc27b-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="bc27b-128">Markera kryssrutorna **Pågående status tillåten**, **Färdig status tillåten** och **Stoppad status tillåten** på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="bc27b-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="bc27b-129">Upprepa dessa stegen för respektive reparationsstatusalternativ som du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="bc27b-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc27b-130">Se även</span><span class="sxs-lookup"><span data-stu-id="bc27b-130">See Also</span></span>

[<span data-ttu-id="bc27b-131">Serviceorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="bc27b-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="bc27b-132">Ställa in tjänstehantering</span><span class="sxs-lookup"><span data-stu-id="bc27b-132">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]