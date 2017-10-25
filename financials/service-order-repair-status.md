---
title: "Så här: ställa in status för serviceorder och reparationer | Microsoft Docs"
description: "Du måste ställa in nio olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="f6c7d-103">Så här: ställa in status för serviceorder och reparationer</span><span class="sxs-lookup"><span data-stu-id="f6c7d-103">How to: Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="f6c7d-104">Du måste ställa in olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="f6c7d-105">Du måste skapa åtminstone nio reparationsstatusalternativ som identifierar situationer eller åtgärder som vidtagits då serviceartiklar servas.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="f6c7d-106">Du kan ange prioriteringsnivåer för alternativen för serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="f6c7d-107">Det finns fyra prioriteter: Hög, medelhög, medellåg och låg.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="f6c7d-108">När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="f6c7d-109">Varje serviceartikels reparationsstatus är kopplad till serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="f6c7d-110">Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="f6c7d-111">Så här skapar du en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="f6c7d-111">To set up a repair status</span></span>  
1. <span data-ttu-id="f6c7d-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Reparationsstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="f6c7d-113">2.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-113">2.</span></span> <span data-ttu-id="f6c7d-114">Skapa en ny reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="f6c7d-115">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="f6c7d-116">I fältet **serviceorderstatus** väljer du orderstatus att länka reparationsstatusen till.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="f6c7d-117">Fältet **Prioritet** visar prioriteten för den serviceorderstatus som du har valt.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="f6c7d-118">Välj en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="f6c7d-118">Choose a repair status.</span></span> <span data-ttu-id="f6c7d-119">Du kan bara välja en.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-119">You can choose only one.</span></span>  
6. <span data-ttu-id="f6c7d-120">Välj fältet **Bokföring tillåten** om du vill kunna bokföra serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="f6c7d-121">Markera kryssrutan **Förestående status tillåten** om du vill kunna ändra serviceorderns status manuellt till alternativet **Förestående** på serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="f6c7d-122">Markera kryssrutorna **Pågående status tillåten**, **Färdig status tillåten** och **Stoppad status tillåten** på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="f6c7d-123">Så här skapar du servicestatusprioriteter</span><span class="sxs-lookup"><span data-stu-id="f6c7d-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="f6c7d-124">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceorderstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f6c7d-125">Välj den serviceorderstatus som du vill ange prioritet för.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="f6c7d-126">I fältet **Prioritet** väljer du önskad prioritet för aktuell serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="f6c7d-127">Upprepa det här steget för varje status.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6c7d-128">Se även</span><span class="sxs-lookup"><span data-stu-id="f6c7d-128">See Also</span></span>  
[<span data-ttu-id="f6c7d-129">Förstå serviceorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="f6c7d-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="f6c7d-130">Ställa in servicehantering</span><span class="sxs-lookup"><span data-stu-id="f6c7d-130">Setting Up Service Management</span></span>](service-setup-service.md)  

