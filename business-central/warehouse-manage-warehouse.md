---
title: Lageraktiviteter | Microsoft Docs
description: "Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: de9f4a202579f347e8f0ebb3196d9b812a979ca3
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="ffd71-103">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="ffd71-103">Warehouse Management</span></span>
<span data-ttu-id="ffd71-104">Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager.</span><span class="sxs-lookup"><span data-stu-id="ffd71-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="ffd71-105">Vanliga lageraktiviteter omfattar artikelinförsel, att flytta artiklar inom eller mellan lagerställen och att plocka artiklar från montering, produktion eller utleverans.</span><span class="sxs-lookup"><span data-stu-id="ffd71-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="ffd71-106">Montera artiklar för försäljning eller lager måste även ta hänsyn till lageraktiviteter, men dessa klassificeras på annat håll.</span><span class="sxs-lookup"><span data-stu-id="ffd71-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="ffd71-107">Mer information finns i [Monteringshantering](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="ffd71-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="ffd71-108">I stora lager kan dessa olika uppgifter hanteras av olika avdelningar och integrationen hanteras med ett dirigerat arbetsflöde.</span><span class="sxs-lookup"><span data-stu-id="ffd71-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="ffd71-109">I enklare installationer är dessa flöden mindre formaliserade, och lageraktiviteterna utförs med så kallad lagerinförsel och lagerplockning.</span><span class="sxs-lookup"><span data-stu-id="ffd71-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="ffd71-110">Mer information om grundläggande och avancerade konfigurationer finns i [Designdetaljer: översikt över distributionslager](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ffd71-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="ffd71-111">Innan du kan utföra lageraktiviteter måste du ange systemet för relevanta komplexiteten i distributionslagerprocessen.</span><span class="sxs-lookup"><span data-stu-id="ffd71-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="ffd71-112">Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ffd71-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="ffd71-113">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="ffd71-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="ffd71-114">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="ffd71-114">**To**</span></span>|<span data-ttu-id="ffd71-115">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="ffd71-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ffd71-116">Registrera inleveransen av artiklar på lagerställen, antingen med en inköpsorder, under enkla lagerställekonfigurationer, eller med en lagerinleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.</span><span class="sxs-lookup"><span data-stu-id="ffd71-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="ffd71-117">Ta emot artiklar</span><span class="sxs-lookup"><span data-stu-id="ffd71-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="ffd71-118">Hoppa över artikelinförseln och välj processer för att påskynda en artikel direkt från produktion till levereras.</span><span class="sxs-lookup"><span data-stu-id="ffd71-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="ffd71-119">Beräkna direktutleverans av artiklar</span><span class="sxs-lookup"><span data-stu-id="ffd71-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="ffd71-120">Införa artiklar som har inlevererats från inköp, returer, överföringar eller produktionsutflöde enligt den konfigurerade distributionslagerprocessen.</span><span class="sxs-lookup"><span data-stu-id="ffd71-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="ffd71-121">Införa utflöde från artiklar</span><span class="sxs-lookup"><span data-stu-id="ffd71-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="ffd71-122">Flytta artiklar mellan lagerplatser i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="ffd71-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="ffd71-123">Flytta artiklar</span><span class="sxs-lookup"><span data-stu-id="ffd71-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="ffd71-124">Plocka artiklar som ska levereras, överföras eller förbrukas vid montering eller produktion, enligt den konfigurerade distributionslagerprocessen.</span><span class="sxs-lookup"><span data-stu-id="ffd71-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="ffd71-125">Plocka artiklar</span><span class="sxs-lookup"><span data-stu-id="ffd71-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="ffd71-126">Registrera utleverans av artiklar från lagerställen, antingen med en försäljningsorder, under enkla lagerställekonfigurationer, eller med en lagerutleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.</span><span class="sxs-lookup"><span data-stu-id="ffd71-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="ffd71-127">Leverera artiklar</span><span class="sxs-lookup"><span data-stu-id="ffd71-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="ffd71-128">Se även</span><span class="sxs-lookup"><span data-stu-id="ffd71-128">See Also</span></span>  
[<span data-ttu-id="ffd71-129">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="ffd71-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ffd71-130">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ffd71-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ffd71-131">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ffd71-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ffd71-132">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="ffd71-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ffd71-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ffd71-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

