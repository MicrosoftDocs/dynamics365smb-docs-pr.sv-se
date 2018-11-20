---
title: Designdetaljer - Order | Microsoft Docs
description: "Det här avsnittet innehåller information om order-till-order-länkar i en tillverka-mot-order-miljö."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 4152dfb744215034383239ea98847fbf7b5751e9
ms.contentlocale: sv-se
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-order"></a><span data-ttu-id="b43cf-103">Designdetaljer: Order</span><span class="sxs-lookup"><span data-stu-id="b43cf-103">Design Details: Order</span></span>
<span data-ttu-id="b43cf-104">I tillverka-mot-order-miljö köps en artikel in eller produceras för att exklusivt täcka en viss efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="b43cf-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="b43cf-105">Vanligtvis gäller det A-artiklar och motiveringen för att välja partiformningsmetoden Order kan vara att efterfrågan är ovanlig, ledtiden är oansenlig eller de obligatoriska attributen varierar.</span><span class="sxs-lookup"><span data-stu-id="b43cf-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  

<span data-ttu-id="b43cf-106">Programmet skapar order-till-order-länk som fungerar som ett preliminärt samband mellan tillgången, en leveransorder eller lagret och efterfrågan som ska uppfyllas.</span><span class="sxs-lookup"><span data-stu-id="b43cf-106">The program creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  

<span data-ttu-id="b43cf-107">Förutom att använda orderprincipen kan order-till-order-kopplingen användas på följande sätt vid planeringen:</span><span class="sxs-lookup"><span data-stu-id="b43cf-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  

* <span data-ttu-id="b43cf-108">När du använder produktionsprincipen Tillverka-Mot-Order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder).</span><span class="sxs-lookup"><span data-stu-id="b43cf-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="b43cf-109">När du använder funktionen Försäljningsorderplanering för att skapa en produktionsorder från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="b43cf-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  

<span data-ttu-id="b43cf-110">Även om ett produktionsföretag anser sig vara en miljö som tillverkar mot order, kan det vara bra att använda en partiformningsmetod av typen Parti-för-parti om artiklarna är standardartiklar med attribut utan variation.</span><span class="sxs-lookup"><span data-stu-id="b43cf-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="b43cf-111">Det medför att systemet använder oplanerat lager och endast ackumulerar försäljningsorder med samma utleveransdatum eller inom en definierad tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="b43cf-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  

## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="b43cf-112">Order-till-order-länkar och utgångna förfallodatum</span><span class="sxs-lookup"><span data-stu-id="b43cf-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="b43cf-113">Till skillnad från de flesta uppsättningar med tillgång-efterfrågan planeras länkade order med förfallodatum före planeringsstartdatumet helt automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b43cf-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="b43cf-114">Affärsorsaken till undantaget är att de specifika uppsättningarna med efterfrågan-tillgång måste synkroniseras till körning.</span><span class="sxs-lookup"><span data-stu-id="b43cf-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="b43cf-115">För mer information om den frysta zonen som gäller de flesta typerna av efterfrågan-tillgång, se [Designdetaljer: Hantera order före planeringsstartdatumet](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="b43cf-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b43cf-116">Se även</span><span class="sxs-lookup"><span data-stu-id="b43cf-116">See Also</span></span>  
<span data-ttu-id="b43cf-117">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="b43cf-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="b43cf-118">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="b43cf-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="b43cf-119">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="b43cf-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="b43cf-120">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="b43cf-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

