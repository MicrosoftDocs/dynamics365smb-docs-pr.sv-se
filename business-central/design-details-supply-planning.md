---
title: Designdetaljer – Leveransplanering | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de begrepp och metoder som används inom leveransplaneringsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 73fcf9a9cb79259f617ef95ec967d01b9adfb621
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785300"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="108c3-103">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="108c3-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="108c3-104">Dokumentationen innehåller detaljerad teknisk insikt i begreppen och principerna som används i leveransplaneringen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="108c3-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="108c3-105">Den förklarar hur planeringssystemet fungerar och hur du justerar algoritmerna för att uppfylla planeringskrav i olika miljöer.</span><span class="sxs-lookup"><span data-stu-id="108c3-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="108c3-106">Den introducerar först centrala lösningsbegrepp och beskriver sedan logiken för den centrala mekanismen, tillgångsbalansering, innan den fortsätter att förklara hur lagerplanering utförs med partiformningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="108c3-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="108c3-107">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="108c3-107">In This Section</span></span>  
[<span data-ttu-id="108c3-108">Designdetaljer: Centrala koncept i planeringssystemet</span><span class="sxs-lookup"><span data-stu-id="108c3-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="108c3-109">Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden</span><span class="sxs-lookup"><span data-stu-id="108c3-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="108c3-110">Designdetaljer: Balansera efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="108c3-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="108c3-111">Designdetaljer: Hantera partiformningsmetoder</span><span class="sxs-lookup"><span data-stu-id="108c3-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="108c3-112">Designdetaljer: Planeringsparametrar</span><span class="sxs-lookup"><span data-stu-id="108c3-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="108c3-113">Designdetaljer: Planeringsfördelningstabell</span><span class="sxs-lookup"><span data-stu-id="108c3-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="108c3-114">Designdetaljer: Efterfrågan vid tomt lagerställe</span><span class="sxs-lookup"><span data-stu-id="108c3-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="108c3-115">Designdetaljer: Överföringar i planering</span><span class="sxs-lookup"><span data-stu-id="108c3-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]