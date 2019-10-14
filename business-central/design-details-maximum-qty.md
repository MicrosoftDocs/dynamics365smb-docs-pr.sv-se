---
title: Designdetaljer - Maximalt antal | Microsoft Docs
description: Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: e186beea06fcada9bc0396fc5627c90bbfb06b4e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303154"
---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="08dde-103">Designdetaljer: Maximalt antal</span><span class="sxs-lookup"><span data-stu-id="08dde-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="08dde-104">Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.</span><span class="sxs-lookup"><span data-stu-id="08dde-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  

 <span data-ttu-id="08dde-105">Allt som gäller metoden Fast orderkvantitet gäller även för den här metoden.</span><span class="sxs-lookup"><span data-stu-id="08dde-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="08dde-106">Den enda skillnaden är antalet på i den föreslagna tillgången.</span><span class="sxs-lookup"><span data-stu-id="08dde-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="08dde-107">När du använder principen för högsta antal definieras beställningsantalet dynamiskt baserat på den planerade lagernivån och kommer därför vanligtvis att skilja sig åt från order till order.</span><span class="sxs-lookup"><span data-stu-id="08dde-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  

## <a name="calculated-per-time-bucket"></a><span data-ttu-id="08dde-108">Beräknat per tidsenhet</span><span class="sxs-lookup"><span data-stu-id="08dde-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="08dde-109">Orderkvantitet bestäms vid tidpunkten (slutet av en tidsenhet) när planeringssystemet identifierar att beställningspunkten har passerats.</span><span class="sxs-lookup"><span data-stu-id="08dde-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="08dde-110">Vid den här tidpunkten mäter systemet luckan mellan den aktuella planerade lagernivån fram till den angivna beställningsgränsen.</span><span class="sxs-lookup"><span data-stu-id="08dde-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="08dde-111">Det här fältet utgör antalet som ska beställas.</span><span class="sxs-lookup"><span data-stu-id="08dde-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="08dde-112">Systemet kontrollerar sedan om tillgång redan har beställts någon annanstans för att tas emot under ledtiden och i så fall minskar antalet på den nya leveransorder genom redan beställda antal.</span><span class="sxs-lookup"><span data-stu-id="08dde-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  

 <span data-ttu-id="08dde-113">Systemet kontrollerar att det planerade lagret minst når beställningspunktnivån – i händelse användaren har glömt att ange en beställningsgränsnivå.</span><span class="sxs-lookup"><span data-stu-id="08dde-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  

## <a name="combines-with-order-modifiers"></a><span data-ttu-id="08dde-114">Kombineras med ordermodifierare</span><span class="sxs-lookup"><span data-stu-id="08dde-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="08dde-115">Beroende på inställningarna kan det vara bra att kombinera principen Max. ant. med ordermodifierare för att säkerställa en minsta partistorlek eller för att avrunda den till ett heltalsnummer av inköpsenheter, eller dela den i flera partier enligt vad som anges av den maximala orderkvantiteten.</span><span class="sxs-lookup"><span data-stu-id="08dde-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  

## <a name="combines-with-calendars"></a><span data-ttu-id="08dde-116">Kombineras med kalendrar</span><span class="sxs-lookup"><span data-stu-id="08dde-116">Combines with Calendars</span></span>  
 <span data-ttu-id="08dde-117">Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.</span><span class="sxs-lookup"><span data-stu-id="08dde-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** pages.</span></span>  

 <span data-ttu-id="08dde-118">Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag.</span><span class="sxs-lookup"><span data-stu-id="08dde-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="08dde-119">Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov.</span><span class="sxs-lookup"><span data-stu-id="08dde-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="08dde-120">För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.</span><span class="sxs-lookup"><span data-stu-id="08dde-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  

## <a name="see-also"></a><span data-ttu-id="08dde-121">Se även</span><span class="sxs-lookup"><span data-stu-id="08dde-121">See Also</span></span>  
 <span data-ttu-id="08dde-122">[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="08dde-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="08dde-123">[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="08dde-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="08dde-124">[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="08dde-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="08dde-125">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="08dde-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
