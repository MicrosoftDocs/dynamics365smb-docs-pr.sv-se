---
title: "Designdetaljer - Stänga efterfrågan och tillgång | Microsoft Docs"
description: "När tillgångsbalanseringen har utförts finns det tre möjliga slutlägen."
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
ms.openlocfilehash: 2be48e11d562f469ab9ef5ac156fdeb46ea51107
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-closing-demand-and-supply"></a><span data-ttu-id="db9b8-103">Designdetaljer: Stänga efterfrågan och tillgång</span><span class="sxs-lookup"><span data-stu-id="db9b8-103">Design Details: Closing Demand and Supply</span></span>
<span data-ttu-id="db9b8-104">När tillgångsbalanseringen har utförts finns det tre möjliga slutlägen:</span><span class="sxs-lookup"><span data-stu-id="db9b8-104">When the supply balancing procedures have been performed, there are three possible end situations:</span></span>  

-   <span data-ttu-id="db9b8-105">Det begärda antalet och datumet för begäranhändelserna har uppfyllts och planeringen för dem kan stängas.</span><span class="sxs-lookup"><span data-stu-id="db9b8-105">The required quantity and date of the demand events have been met and the planning for them can be closed.</span></span> <span data-ttu-id="db9b8-106">Tillgångshändelsen är fortfarande öppen och kan eventuellt täcka nästa efterfrågan, så motkonteringen kan starta igen med aktuell tillgångshändelse och nästa efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="db9b8-106">The supply event is still open and may be able to cover the next demand, so the balancing procedure can start over with the current supply event and the next demand.</span></span>  

-   <span data-ttu-id="db9b8-107">Leveransordern kan inte ändras för att täcka all efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="db9b8-107">The supply order cannot be modified to cover all of the demand.</span></span> <span data-ttu-id="db9b8-108">Efterfråganshändelsen är fortfarande öppen, med visst antal som inte täckts men som kan täckas av nästa tillgångshändelse.</span><span class="sxs-lookup"><span data-stu-id="db9b8-108">The demand event is still open, with some uncovered quantity that may be covered by the next supply event.</span></span> <span data-ttu-id="db9b8-109">På så sätt stängs den aktuella händelsen för efterfrågan, så att motkonteringen kan börja om igen med aktuell efterfrågan och nästa tillgångshändelse.</span><span class="sxs-lookup"><span data-stu-id="db9b8-109">Thus the current supply event is closed, so the balancing act can start over with the current demand and the next supply event.</span></span>  

-   <span data-ttu-id="db9b8-110">All efterfrågan har täckts. Det finns inte någon efterföljande efterfrågan (eller det har inte funnits någon efterfrågan alls).</span><span class="sxs-lookup"><span data-stu-id="db9b8-110">All of the demand has been covered; there is no subsequent demand (or there has been no demand at all).</span></span> <span data-ttu-id="db9b8-111">Om det finns någon överskottstillgång kan den minskas (eller annulleras) och sedan stängas.</span><span class="sxs-lookup"><span data-stu-id="db9b8-111">If there is any surplus supply, it may be decreased (or canceled) and then closed.</span></span> <span data-ttu-id="db9b8-112">Det är möjligt att ytterligare tillförselhändelser finns längre fram i kedjan, och de bör också annulleras.</span><span class="sxs-lookup"><span data-stu-id="db9b8-112">It is possible that additional supply events exist further along in the chain, and they should also be canceled.</span></span>  

 <span data-ttu-id="db9b8-113">Till sist skapar planeringssystemet en orderspårninglänk mellan tillgång och efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="db9b8-113">Last, the planning system will create an order tracking link between the supply and the demand.</span></span>  

## <a name="creating-the-planning-line-suggested-action"></a><span data-ttu-id="db9b8-114">Skapa planeringsraden (föreslagen åtgärd)</span><span class="sxs-lookup"><span data-stu-id="db9b8-114">Creating the Planning Line (Suggested Action)</span></span>  
 <span data-ttu-id="db9b8-115">Om åtgärder – nytt, ändra antal, ändra tidpunkt, ändra tidpunkt och ändra antal eller avbryt – föreslås för att granska leveransordern skapar planeringssystemet en planeringsrad i planeringsförslaget.</span><span class="sxs-lookup"><span data-stu-id="db9b8-115">If any action – New, Change Quantity, Reschedule, Reschedule and Change Quantity, or Cancel – is suggested to revise the supply order, the planning system creates a planning line in the planning worksheet.</span></span> <span data-ttu-id="db9b8-116">På grund av orderspårning skapas planeringsraden inte bara när tillförselhändelsen stängs, utan även om efterfråganshändelsen stängs, även om tillförselhändelsen fortfarande är öppen och kan få ytterligare ändringar när nästa efterfråganshändelse behandlas.</span><span class="sxs-lookup"><span data-stu-id="db9b8-116">Due to order tracking, the planning line is created not only when the supply event is closed, but also if the demand event is closed, even though the supply event is still open and may be subject to additional changes when the next demand event is processed.</span></span> <span data-ttu-id="db9b8-117">Det betyder att när planeringsraden har skapats kan den ändras på nytt.</span><span class="sxs-lookup"><span data-stu-id="db9b8-117">This means that when first created, the planning line may be changed again.</span></span>  

 <span data-ttu-id="db9b8-118">För att minska databasåtkomsten när du hanterar produktionsorder kan planeringsraden underhållas i tre nivåer, med målet att utföra den minst fordrande underhållsnivån:</span><span class="sxs-lookup"><span data-stu-id="db9b8-118">To minimize database access when handling production orders, the planning line can be maintained in three levels, while aiming to perform the least demanding maintenance level:</span></span>  

-   <span data-ttu-id="db9b8-119">Skapa endast planeringsraden med det aktuella förfallodatumet och antalet men utan verksamhetsföljden och komponenterna.</span><span class="sxs-lookup"><span data-stu-id="db9b8-119">Create only the planning line with the current due date and quantity but without the routing and components.</span></span>  

-   <span data-ttu-id="db9b8-120">Inkludera verksamhetsföljd: den planerade verksamhetsföljden läggs ut inklusive beräkning av start- och slutdatum och tidpunkter.</span><span class="sxs-lookup"><span data-stu-id="db9b8-120">Include routing: the planned routing is laid out including calculation of starting and ending dates and times.</span></span> <span data-ttu-id="db9b8-121">Det är fordrande i termer av databasåtkomster.</span><span class="sxs-lookup"><span data-stu-id="db9b8-121">This is demanding in terms of database accesses.</span></span> <span data-ttu-id="db9b8-122">För att fastställa slut- och förfallodatum kan det vara nödvändigt att beräkna detta även om tillförselhändelsen inte har stängts (om det gäller framåtplanering).</span><span class="sxs-lookup"><span data-stu-id="db9b8-122">To determine the ending and due dates, it may be necessary to calculate this even if the supply event has not been closed (in the case of forward scheduling).</span></span>  

-   <span data-ttu-id="db9b8-123">Ta med strukturexpansion: det kan vänta tills precis före tillgångshändelsen är avslutad.</span><span class="sxs-lookup"><span data-stu-id="db9b8-123">Include BOM explosion: this can wait until just before the supply event is closed.</span></span>  

 <span data-ttu-id="db9b8-124">Detta slutför beskrivningarna av hur efterfrågan och tillgång laddas, prioriteras och balanseras av planeringssystemet.</span><span class="sxs-lookup"><span data-stu-id="db9b8-124">This concludes the descriptions of how demand and supply is loaded, prioritized, and balanced by the planning system.</span></span> <span data-ttu-id="db9b8-125">I integration med den här tillgångsplaneringsaktiviteten måste systemet se till att önskad lagernivå för varje planerad artikel upprätthålls enligt dess partiformningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="db9b8-125">In integration with this supply planning activity, the system must ensure that the required inventory level of each planned item is maintained according to its reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db9b8-126">Se även</span><span class="sxs-lookup"><span data-stu-id="db9b8-126">See Also</span></span>  
 <span data-ttu-id="db9b8-127">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="db9b8-127">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="db9b8-128">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="db9b8-128">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="db9b8-129">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="db9b8-129">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
