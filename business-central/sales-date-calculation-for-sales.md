---
title: Datum för beräkning av försäljning | Microsoft Docs
description: Programmet beräknar automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum. Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.
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
ms.openlocfilehash: a620b7ed9d06cdd8adf7b12bea2b55aecea32bcc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251137"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="f265a-104">Datumberäkning för försäljning</span><span class="sxs-lookup"><span data-stu-id="f265a-104">Date Calculation for Sales</span></span>
<span data-ttu-id="f265a-105">I [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknas automatiskt tidigast möjliga leveransdatum för en artikel på en försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="f265a-105">[!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="f265a-106">Om kunden har begärt ett särskilt leveransdatum beräknas det datum då artiklarna måste vara tillgängliga för plockning så att varorna faktiskt ska kunna levereras på angiven dag.</span><span class="sxs-lookup"><span data-stu-id="f265a-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="f265a-107">Om inget bestämt leveransdatum begärts beräknas det datum då artiklarna kan levereras, med utgångspunkt från det datum då artiklarna är tillgängliga för plockning.</span><span class="sxs-lookup"><span data-stu-id="f265a-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="f265a-108">Beräkna ett begärt leveransdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="f265a-109">Om du anger ett begärt leveransdatum på försäljningsorderraden används detta datum som utgångspunkt för följande beräkningar.</span><span class="sxs-lookup"><span data-stu-id="f265a-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="f265a-110">begärt leveransdatum - leveranstid = planerat utleveransdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="f265a-111">planerat utleveransdatum - avgående lagerhanteringstid = utleveransdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="f265a-112">Om artiklarna kan plockas på utleveransdatumet kan försäljningsprocessen fortsätta.</span><span class="sxs-lookup"><span data-stu-id="f265a-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="f265a-113">Om artiklarna inte kan plockas på utleveransdatumet visas en varning om att varan inte finns i lager.</span><span class="sxs-lookup"><span data-stu-id="f265a-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="f265a-114">Beräkna tidigaste möjliga leveransdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="f265a-115">Om du inte har angett ett begärt leveransdatum på försäljningsorderraden, eller om det begärda leveransdatumet inte kan godtas, beräknas det tidigaste datum då artiklarna är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f265a-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="f265a-116">Detta datum anges automatiskt i fältet Leveransdatum på raden. Det datum då du planerar att utleverera artiklarna liksom det datum då varorna kan levereras till kunden beräknas med hjälp av följande formler.</span><span class="sxs-lookup"><span data-stu-id="f265a-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="f265a-117">planerat utleveransdatum + avgående lagerhanteringstid = planerat utleveransdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="f265a-118">planerat utleveransdatum +- leveranstid = planerat leveransdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="f265a-119">Se även</span><span class="sxs-lookup"><span data-stu-id="f265a-119">See Also</span></span>  
 <span data-ttu-id="f265a-120">[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="f265a-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="f265a-121">Beräkna orderlöftesdatum</span><span class="sxs-lookup"><span data-stu-id="f265a-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="f265a-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f265a-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
