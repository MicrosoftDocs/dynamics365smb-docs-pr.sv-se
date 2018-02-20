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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8ffd5d6893b2b6c8ce7b7377c586f4f5414279b5
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="3b299-103">Ställ in status för serviceorder och reparationer</span><span class="sxs-lookup"><span data-stu-id="3b299-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="3b299-104">Du måste ställa in olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.</span><span class="sxs-lookup"><span data-stu-id="3b299-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="3b299-105">Du måste skapa åtminstone nio reparationsstatusalternativ som identifierar situationer eller åtgärder som vidtagits då serviceartiklar servas.</span><span class="sxs-lookup"><span data-stu-id="3b299-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="3b299-106">Du kan ange prioriteringsnivåer för alternativen för serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="3b299-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="3b299-107">Det finns fyra prioriteter: Hög, medelhög, medellåg och låg.</span><span class="sxs-lookup"><span data-stu-id="3b299-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="3b299-108">När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status.</span><span class="sxs-lookup"><span data-stu-id="3b299-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="3b299-109">Varje serviceartikels reparationsstatus är kopplad till serviceorderstatusen.</span><span class="sxs-lookup"><span data-stu-id="3b299-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="3b299-110">Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="3b299-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="3b299-111">Så här skapar du en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="3b299-111">To set up a repair status</span></span>  
1. <span data-ttu-id="3b299-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Reparationsstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3b299-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="3b299-113">2.</span><span class="sxs-lookup"><span data-stu-id="3b299-113">2.</span></span> <span data-ttu-id="3b299-114">Skapa en ny reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="3b299-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="3b299-115">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="3b299-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="3b299-116">I fältet **serviceorderstatus** väljer du orderstatus att länka reparationsstatusen till.</span><span class="sxs-lookup"><span data-stu-id="3b299-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="3b299-117">Fältet **Prioritet** visar prioriteten för den serviceorderstatus som du har valt.</span><span class="sxs-lookup"><span data-stu-id="3b299-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="3b299-118">Välj en reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="3b299-118">Choose a repair status.</span></span> <span data-ttu-id="3b299-119">Du kan bara välja en.</span><span class="sxs-lookup"><span data-stu-id="3b299-119">You can choose only one.</span></span>  
6. <span data-ttu-id="3b299-120">Välj fältet **Bokföring tillåten** om du vill kunna bokföra serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="3b299-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="3b299-121">Markera kryssrutan **Förestående status tillåten** om du vill kunna ändra serviceorderns status manuellt till alternativet **Förestående** på serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.</span><span class="sxs-lookup"><span data-stu-id="3b299-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="3b299-122">Markera kryssrutorna **Pågående status tillåten**, **Färdig status tillåten** och **Stoppad status tillåten** på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="3b299-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="3b299-123">Så här skapar du servicestatusprioriteter</span><span class="sxs-lookup"><span data-stu-id="3b299-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="3b299-124">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Tjänsteorderstatus** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3b299-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3b299-125">Välj den serviceorderstatus som du vill ange prioritet för.</span><span class="sxs-lookup"><span data-stu-id="3b299-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="3b299-126">I fältet **Prioritet** väljer du önskad prioritet för aktuell serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="3b299-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="3b299-127">Upprepa det här steget för varje status.</span><span class="sxs-lookup"><span data-stu-id="3b299-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b299-128">Se även</span><span class="sxs-lookup"><span data-stu-id="3b299-128">See Also</span></span>  
[<span data-ttu-id="3b299-129">Förstå serviceorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="3b299-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="3b299-130">Ställa in tjänstehantering</span><span class="sxs-lookup"><span data-stu-id="3b299-130">Setting Up Service Management</span></span>](service-setup-service.md)  

