---
title: "Designdetaljer - Parti-för-parti | Microsoft Docs"
description: "Lär dig att använda de parti-för-parti som ska kvitta orderkvantiteten baserat på behov."
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
ms.openlocfilehash: 1a9a2a019a623f4e60efa48876bdf78a7ce47404
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="6ee4c-103">Designdetaljer: Parti-för-parti</span><span class="sxs-lookup"><span data-stu-id="6ee4c-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="6ee4c-104">Parti-för-parti-policyn är den mest flexibla eftersom systemet bara reagerar på faktisk efterfrågan, plus att den agerar på förutsedd efterfrågan från prognos och avropsorder, och sedan avräknar orderantalet baserat på efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="6ee4c-105">Parti-för-parti-principen gäller A-och B-artiklar där lager kan accepteras men ska undvikas.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  
  
<span data-ttu-id="6ee4c-106">På vissa sätt liknar parti-för-parti-principen som orderprincipen, men den har en generisk inställning till artiklar: den kan ta emot antal i lager, och den samlar ihop efterfrågan och motsvarande tillgång i tidsenheter som definieras av användaren.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  
  
<span data-ttu-id="6ee4c-107">Tidsenheten definieras i fältet **Tidsenhet**.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="6ee4c-108">Systemet arbetar med en lägsta tidsenhet av en dag, eftersom det är den minsta tidsenheten för efterfrågan- och tillgångshändelser i systemet (fast i praktiken kan tidsenheten för produktionsorder och komponentbehov vara sekunder).</span><span class="sxs-lookup"><span data-stu-id="6ee4c-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  
  
<span data-ttu-id="6ee4c-109">Tidsenheten anger också gränser för när en befintlig leveransorder ska omplaneras för att uppfylla en viss efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="6ee4c-110">Om tillgången ligger inom tidsenheten kommer den att planeras om framåt eller bakåt för att uppfylla efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="6ee4c-111">Annars, om det ligger tidigare, kommer det att orsaka onödig uppbyggnad av lagersaldot och ska avbrytas.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="6ee4c-112">Om det ligger senare, kommer en ny leveransorder att skapas i stället.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-112">If it lies later, a new supply order will be created instead.</span></span>  
  
<span data-ttu-id="6ee4c-113">Med den här metoden det är också möjligt att definiera ett säkerhetslager för att kompensera för möjliga variationer i tillgången, eller för att uppfylla plötslig efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="6ee4c-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  
  
<span data-ttu-id="6ee4c-114">Eftersom leveranspartistorleken baseras på faktiskt behov, kan det vara praktiskt att använda ordermodifierare: avrunda partistorleken uppåt för att uppfylla en viss partistorleksmultipel (eller inköpsenhet), öka beställningen till en viss lägsta partistorlek eller minska partistorleken till det angivna högsta antalet (och skapa därmed två eller flera leveranser för att erhålla den totala behovskvantiteten).</span><span class="sxs-lookup"><span data-stu-id="6ee4c-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ee4c-115">Se även</span><span class="sxs-lookup"><span data-stu-id="6ee4c-115">See Also</span></span>  
<span data-ttu-id="6ee4c-116">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="6ee4c-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="6ee4c-117">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="6ee4c-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="6ee4c-118">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="6ee4c-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="6ee4c-119">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="6ee4c-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
