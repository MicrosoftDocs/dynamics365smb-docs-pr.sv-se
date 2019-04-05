---
title: Designdetaljer - Leveransplanering | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de begrepp och metoder som används inom leveransplaneringsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 92496f25d354dd766acd8d301546a5bf4f36c1e3
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807066"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="6fc86-103">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="6fc86-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="6fc86-104">Dokumentationen innehåller detaljerad teknisk insikt i begreppen och principerna som används i leveransplaneringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6fc86-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="6fc86-105">Den förklarar hur planeringssystemet fungerar och hur du justerar algoritmerna för att uppfylla planeringskrav i olika miljöer.</span><span class="sxs-lookup"><span data-stu-id="6fc86-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="6fc86-106">Den introducerar först centrala lösningsbegrepp och beskriver sedan logiken för den centrala mekanismen, tillgångsbalansering, innan den fortsätter att förklara hur lagerplanering utförs med partiformningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="6fc86-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="6fc86-107">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="6fc86-107">In This Section</span></span>  
[<span data-ttu-id="6fc86-108">Designdetaljer: Centrala koncept i planeringssystemet</span><span class="sxs-lookup"><span data-stu-id="6fc86-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="6fc86-109">Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden</span><span class="sxs-lookup"><span data-stu-id="6fc86-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="6fc86-110">Designdetaljer: Balansera efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="6fc86-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="6fc86-111">Designdetaljer: Hantera partiformningsmetoder</span><span class="sxs-lookup"><span data-stu-id="6fc86-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="6fc86-112">Designdetaljer: Planeringsparametrar</span><span class="sxs-lookup"><span data-stu-id="6fc86-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="6fc86-113">Designdetaljer: Planeringsfördelningstabell</span><span class="sxs-lookup"><span data-stu-id="6fc86-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="6fc86-114">Designdetaljer: Efterfrågan vid tomt lagerställe</span><span class="sxs-lookup"><span data-stu-id="6fc86-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="6fc86-115">Designdetaljer: Överföringar i planering</span><span class="sxs-lookup"><span data-stu-id="6fc86-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)
