---
title: Datum för beräkning av försäljning | Microsoft Docs
description: Programmet beräknar automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum. Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a2a65f5025a8a79a7d0800d486bcac90fde23538
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789056"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="fd86b-104">Datumberäkning för försäljning</span><span class="sxs-lookup"><span data-stu-id="fd86b-104">Date Calculation for Sales</span></span>
<span data-ttu-id="fd86b-105">I [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknas automatiskt tidigast möjliga leveransdatum för en artikel på en försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="fd86b-105">[!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="fd86b-106">Om kunden har begärt ett särskilt leveransdatum beräknas det datum då artiklarna måste vara tillgängliga för plockning så att varorna faktiskt ska kunna levereras på angiven dag.</span><span class="sxs-lookup"><span data-stu-id="fd86b-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="fd86b-107">Om inget bestämt leveransdatum begärts beräknas det datum då artiklarna kan levereras, med utgångspunkt från det datum då artiklarna är tillgängliga för plockning.</span><span class="sxs-lookup"><span data-stu-id="fd86b-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="fd86b-108">Beräkna ett begärt leveransdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="fd86b-109">Om du anger ett begärt leveransdatum på försäljningsorderraden blir detta datum utgångspunkt för följande beräkningar.</span><span class="sxs-lookup"><span data-stu-id="fd86b-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="fd86b-110">begärt leveransdatum - leveranstid = planerat utleveransdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="fd86b-111">planerat utleveransdatum - avgående lagerhanteringstid = utleveransdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="fd86b-112">Om artiklarna kan plockas på utleveransdatumet kan försäljningsprocessen fortsätta.</span><span class="sxs-lookup"><span data-stu-id="fd86b-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="fd86b-113">Annars visas en varning om slut på lager.</span><span class="sxs-lookup"><span data-stu-id="fd86b-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="fd86b-114">Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda leveransdatumet för att hämta planerat leveransdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D", i fem dagar eller "1V" i en vecka.</span><span class="sxs-lookup"><span data-stu-id="fd86b-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="fd86b-115">Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar.</span><span class="sxs-lookup"><span data-stu-id="fd86b-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="fd86b-116">Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="fd86b-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="fd86b-117">Beräkna tidigaste möjliga leveransdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="fd86b-118">Om du inte har angett ett begärt leveransdatum på försäljningsorderraden, eller om det begärda leveransdatumet inte kan godtas, beräknas det tidigaste datum då artiklarna är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="fd86b-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="fd86b-119">Detta datum anges automatiskt i fältet Leveransdatum på raden. Det datum då du planerar att utleverera artiklarna liksom det datum då varorna kan levereras till kunden beräknas med hjälp av följande formler.</span><span class="sxs-lookup"><span data-stu-id="fd86b-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="fd86b-120">planerat utleveransdatum + avgående lagerhanteringstid = planerat utleveransdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="fd86b-121">planerat utleveransdatum +- leveranstid = planerat leveransdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="fd86b-122">Se även</span><span class="sxs-lookup"><span data-stu-id="fd86b-122">See Also</span></span>  
 <span data-ttu-id="fd86b-123">[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="fd86b-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="fd86b-124">Beräkna orderlöftesdatum</span><span class="sxs-lookup"><span data-stu-id="fd86b-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="fd86b-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fd86b-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
