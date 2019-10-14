---
title: 'Designdetaljer: Hantera order före planeringsstartdatumet | Microsoft Docs'
description: Det här avsnittet beskriver de regler som gäller för att planera order i den frysta zonen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: bc594a93987bf8740964b082fed25dc8d7e269fe
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307306"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="dcfa0-103">Designdetaljer: Hantera order före planeringsstartdatumet</span><span class="sxs-lookup"><span data-stu-id="dcfa0-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="dcfa0-104">För att förhindra att en tillförselplan visar omöjliga och därför oanvändbara förslag, betraktar planeringssystemet perioden fram till planeringsstartdatumet som en fryst zon som inget planeras för.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="dcfa0-105">Följande regel gäller för den frysta zonen:</span><span class="sxs-lookup"><span data-stu-id="dcfa0-105">The following rule applies to the frozen zone:</span></span>  

<span data-ttu-id="dcfa0-106">All efterfrågan och tillgång före startdatumet för planeringsperioden anses vara en del av lagret eller levererat.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  

<span data-ttu-id="dcfa0-107">Planeringssystemet föreslår inte, med ett par undantag, några ändringar av leveransorder i den frysta zonen, och inga orderspårninglänkar skapas eller underhålls för den perioden.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  

<span data-ttu-id="dcfa0-108">Undantagen till denna regel är enligt följande:</span><span class="sxs-lookup"><span data-stu-id="dcfa0-108">The exceptions to this rule are as follows:</span></span>  

* <span data-ttu-id="dcfa0-109">Om det planerade tillgängliga lagret, inklusive summan av efterfrågan och tillgång i den frysta zonen, är under noll.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="dcfa0-110">Om serie-/partinummer krävs på de bakåtdaterade beställningarna.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="dcfa0-111">Om uppsättningen tillgång-efterfrågan är kopplad av en order-till-order-princip.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  

<span data-ttu-id="dcfa0-112">Om det ursprungliga tillgängliga lagret är lägre än noll föreslår planeringssystemet en nödleveransorder leveransorder på dagen före planeringsperioden för att täcka det antal som saknas.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="dcfa0-113">Därför kommer det planerade och tillgängliga lagret alltid att vara minst noll när planeringen för den framtida perioden börjar.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="dcfa0-114">Planeringsraden för leveransordern ska innehålla en nödvarningsikon och ytterligare information finns i fältet.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="dcfa0-115">Serie-/partinummer och Order-till-order-länkar är undantagna från den frysta zonen</span><span class="sxs-lookup"><span data-stu-id="dcfa0-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="dcfa0-116">Om serie-/partinummer krävs eller det finns en order-till-order-länk kommer planeringssystemet att ignorera den frysta zonen och ta med sådana antal som har bakåtdaterats från startdatumet, och föreslår eventuellt korrigerande åtgärder om efterfrågan och tillgång är i obalans.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="dcfa0-117">Affärsorsaken till den här principen är att sådana specifika uppsättningar med efterfrågan-tillgång måste matcha för att se till att den aktuella efterfrågan uppfylls.</span><span class="sxs-lookup"><span data-stu-id="dcfa0-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dcfa0-118">Se även</span><span class="sxs-lookup"><span data-stu-id="dcfa0-118">See Also</span></span>  
<span data-ttu-id="dcfa0-119">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="dcfa0-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="dcfa0-120">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="dcfa0-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="dcfa0-121">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="dcfa0-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
