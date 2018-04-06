---
title: Designdetaljer - Tidsenhetens roll | Microsoft Docs
description: "Avsikten med tidsenheten är samla efterfråganshändelser i tidsfönstret för att skapa en gemensam leveransorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 099465f0ef7bdafa3df80c377cd83b177bb68072
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="867e4-103">Designdetaljer: Tidsenhetens roll</span><span class="sxs-lookup"><span data-stu-id="867e4-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="867e4-104">Avsikten med tidsenheten är samla efterfråganshändelser i tidsfönstret för att skapa en gemensam leveransorder.</span><span class="sxs-lookup"><span data-stu-id="867e4-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="867e4-105">För partiformningsmetoder som använder en beställningspunkt kan du ange en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="867e4-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="867e4-106">Detta säkerställer att efterfrågan inom samma tidsperiod har ackumulerats innan inverkan på planerat lager kontrolleras och om beställningspunkten har passerats.</span><span class="sxs-lookup"><span data-stu-id="867e4-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="867e4-107">Om beställningspunkten har passerats framåtplaneras en ny leveransorder från slutet av perioden som definieras av tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="867e4-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="867e4-108">Tidsenheten börjar på planeringsstartdatumet.</span><span class="sxs-lookup"><span data-stu-id="867e4-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="867e4-109">Konceptet med tidsenhet återspeglar den manuella processen för att kontrollera lagernivån ofta istället för vid varje transaktion.</span><span class="sxs-lookup"><span data-stu-id="867e4-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="867e4-110">Användaren måste definiera frekvens (tidsenheten).</span><span class="sxs-lookup"><span data-stu-id="867e4-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="867e4-111">Till exempel samlar användaren alla artikelbehov från en leverantör att göra en veckobeställning.</span><span class="sxs-lookup"><span data-stu-id="867e4-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 <span data-ttu-id="867e4-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span><span class="sxs-lookup"><span data-stu-id="867e4-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span></span>  
  
 <span data-ttu-id="867e4-113">Tidsenhet används allmänt för att undvika en kaskadeffekt.</span><span class="sxs-lookup"><span data-stu-id="867e4-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="867e4-114">Till exempel skapas en balanserad rad med efterfrågan och tillgång där en tidig efterfrågan annulleras, eller ny skapas.</span><span class="sxs-lookup"><span data-stu-id="867e4-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="867e4-115">Resultatet skulle vara att varje leveransorder (utom den sista) omplaneras.</span><span class="sxs-lookup"><span data-stu-id="867e4-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="867e4-116">Se även</span><span class="sxs-lookup"><span data-stu-id="867e4-116">See Also</span></span>  
 <span data-ttu-id="867e4-117">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="867e4-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="867e4-118">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="867e4-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="867e4-119">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="867e4-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="867e4-120">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="867e4-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
