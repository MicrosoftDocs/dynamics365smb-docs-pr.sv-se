---
title: Designdetaljer - Disposition i distributionslagret | Microsoft Docs
description: Systemet måste ha en konstant kontroll på artikeltillgänglighet i distributionslagret, så att avgående beställningar kan flöda effektivt och ge bästa möjliga leveranser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 38218c497f7d3892b19d0b594ff3863004f69ac4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246870"
---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="dde19-103">Designdetaljer: Disposition i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="dde19-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="dde19-104">Systemet måste ha en konstant kontroll på artikeltillgänglighet i distributionslagret, så att avgående beställningar kan flöda effektivt och ge bästa möjliga leveranser.</span><span class="sxs-lookup"><span data-stu-id="dde19-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

 <span data-ttu-id="dde19-105">Dispositionen varierar beroende på fördelningar på lagerplatsnivån när distributionslageraktiviteter, till exempel plockning och transport, inträffar och när lagerreservationssystemet har begränsningar som ska uppfyllas.</span><span class="sxs-lookup"><span data-stu-id="dde19-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="dde19-106">En ganska komplex algoritm kontrollerar att alla villkor är uppfyllda innan antal tilldelas till plockningar för utgående flöden.</span><span class="sxs-lookup"><span data-stu-id="dde19-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>  

## <a name="bin-content-and-reservations"></a><span data-ttu-id="dde19-107">Lagerplats och reservationer</span><span class="sxs-lookup"><span data-stu-id="dde19-107">Bin Content and Reservations</span></span>  
 <span data-ttu-id="dde19-108">I en installation av lagerstyrning finns artikelantalet både som distributionslagertransaktioner, i modulen Distributionslager och som artikeltransaktioner, i modulen Lager.</span><span class="sxs-lookup"><span data-stu-id="dde19-108">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="dde19-109">Dessa två transaktionstyper innehåller information om var artiklarna finns och om de är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="dde19-109">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="dde19-110">Distributionslagertransaktioner definierar en artikels tillgänglighet per lagerplats och lagerplatstyp, vilket kallas lagerplatsinnehåll.</span><span class="sxs-lookup"><span data-stu-id="dde19-110">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="dde19-111">Artikeltransaktioner definierar en artikels disposition genom dess reservation till avgående dokument.</span><span class="sxs-lookup"><span data-stu-id="dde19-111">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="dde19-112">Särskild funktion i plockningsalgoritmen finns för att beräkna den kvantitet som är tillgänglig för plockning när lagerplatsinnehåll kopplas ihop med reservationer.</span><span class="sxs-lookup"><span data-stu-id="dde19-112">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="dde19-113">Disponibelt antal att plocka</span><span class="sxs-lookup"><span data-stu-id="dde19-113">Quantity Available to Pick</span></span>  
 <span data-ttu-id="dde19-114">Om till exempel plockningsalgoritmen inte beaktar artikelantal som har reserverats för en väntande försäljningsframgångs, kan dessa artiklar plockas för en annan försäljningsorder som ska utlevereras tidigare, vilket hindrar att den första försäljningen uppfylls.</span><span class="sxs-lookup"><span data-stu-id="dde19-114">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="dde19-115">För att undvika den här situationen drar plockningsalgoritmen bort antal som har reserverats för andra avgående dokument, antal på befintliga plockdokument och antal som har plockas men som ännu inte har levererats eller förbrukats.</span><span class="sxs-lookup"><span data-stu-id="dde19-115">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="dde19-116">Resultatet visas i fältet **Disponibelt att plocka** på sidan **Plockningskalkylark** där fältet beräknas dynamiskt.</span><span class="sxs-lookup"><span data-stu-id="dde19-116">The result is displayed in the **Available Qty. to Pick** field on the **Pick Worksheet** page, where the field is calculated dynamically.</span></span> <span data-ttu-id="dde19-117">Värdet beräknas också när användaren skapar distributionslagerplockningarna direkt för avgående dokument.</span><span class="sxs-lookup"><span data-stu-id="dde19-117">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="dde19-118">Sådana utgående dokument kan vara försäljningsorder, produktionsförbrukning eller utgående överföringar, där resultatet visas i de relaterade antalsfälten, till exempel **Ant. att hantera**.</span><span class="sxs-lookup"><span data-stu-id="dde19-118">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dde19-119">Angående prioriteten för reservationer subtraheras antalet som ska reserveras från antalet som är disponibelt att plockas.</span><span class="sxs-lookup"><span data-stu-id="dde19-119">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="dde19-120">Till exempel om antalet som är tillgängligt på plocklagerplatser är 5 enheter, men 100 enheter finns på införsel-lagerplatser, och du försöker att reservera mer än 5 enheter för ytterligare en order, kommer ett felmeddelande visas eftersom den här extra kvantiteten måste vara tillgänglig på plocklagerplatser.</span><span class="sxs-lookup"><span data-stu-id="dde19-120">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="dde19-121">Beräknar disponibelt antal att plocka</span><span class="sxs-lookup"><span data-stu-id="dde19-121">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="dde19-122">Antalet som är tillgängligt att plocka beräknas så här:</span><span class="sxs-lookup"><span data-stu-id="dde19-122">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="dde19-123">disponibelt antal att plocka = antal på plocklagerplatser - antal i plockning och transport – (reserverat antal på plocklagerplatser + reserverat antal i plockning och transport)</span><span class="sxs-lookup"><span data-stu-id="dde19-123">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="dde19-124">Följande diagram visar de olika elementen i beräkningen.</span><span class="sxs-lookup"><span data-stu-id="dde19-124">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="dde19-125">![Plockas med reservation överlappad](media/design_details_warehouse_management_availability_2.png "Plockas med reservation överlappad")</span><span class="sxs-lookup"><span data-stu-id="dde19-125">![Available to pick with reservation overlap](media/design_details_warehouse_management_availability_2.png "Available to pick with reservation overlap")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="dde19-126">Disponibelt antal att reservera</span><span class="sxs-lookup"><span data-stu-id="dde19-126">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="dde19-127">Eftersom begreppen för lagerplatsinnehåll och reservation finns till samtidigt, måste antalet artiklar som är disponibla att reservera justeras mot fördelningar till utgående distributionslagerdokument.</span><span class="sxs-lookup"><span data-stu-id="dde19-127">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="dde19-128">Det bör vara möjligt att reservera alla artiklar i lager, utom de som har inlett avgående behandling.</span><span class="sxs-lookup"><span data-stu-id="dde19-128">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="dde19-129">Antalet som är tillgängligt att reservera definieras som antalet på alla dokument och alla lagerplatstyper, utom följande avgående antal:</span><span class="sxs-lookup"><span data-stu-id="dde19-129">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="dde19-130">Antal i oregistrerade plockdokument</span><span class="sxs-lookup"><span data-stu-id="dde19-130">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="dde19-131">Antal i utleveranslagerplatser</span><span class="sxs-lookup"><span data-stu-id="dde19-131">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="dde19-132">Antal i till-produktion-lagerplatser</span><span class="sxs-lookup"><span data-stu-id="dde19-132">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="dde19-133">Antal i öppna produktionslagerplatser</span><span class="sxs-lookup"><span data-stu-id="dde19-133">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="dde19-134">Antal i till-montering-lagerplatser</span><span class="sxs-lookup"><span data-stu-id="dde19-134">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="dde19-135">Antal på justeringlagerplatser</span><span class="sxs-lookup"><span data-stu-id="dde19-135">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="dde19-136">Resultatet visas i fältet **Totalt disponibelt antal** på sidan **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="dde19-136">The result is displayed in the **Total Available Quantity** field on the **Reservation** page.</span></span>  

 <span data-ttu-id="dde19-137">På en reservationsrad visas antalet som inte kan reserveras, eftersom det har fördelats i distributionslagret, i fältet **Fördelat antal i dist.lager** på sidan **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="dde19-137">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field on the **Reservation** page.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="dde19-138">Beräknar disponibelt antal att reservera</span><span class="sxs-lookup"><span data-stu-id="dde19-138">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="dde19-139">Antalet som är tillgängligt att reservera beräknas så här:</span><span class="sxs-lookup"><span data-stu-id="dde19-139">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="dde19-140">disponibelt antal att reservera = totalt antal i lager - antal i plockning och transport för källdokument - reserverat antal - antal i avgående lagerplatser</span><span class="sxs-lookup"><span data-stu-id="dde19-140">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="dde19-141">Följande diagram visar de olika elementen i beräkningen.</span><span class="sxs-lookup"><span data-stu-id="dde19-141">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="dde19-142">![Tillgänglig att reservera per lagerställe fördelningar](media/design_details_warehouse_management_availability_3.png "Tillgänglig att reservera per lagerställe fördelningar")</span><span class="sxs-lookup"><span data-stu-id="dde19-142">![Avaliable to reserve per warehouse allocation](media/design_details_warehouse_management_availability_3.png "Avaliable to reserve per warehouse allocation")</span></span>  

## <a name="see-also"></a><span data-ttu-id="dde19-143">Se även</span><span class="sxs-lookup"><span data-stu-id="dde19-143">See Also</span></span>  
 [<span data-ttu-id="dde19-144">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="dde19-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)
