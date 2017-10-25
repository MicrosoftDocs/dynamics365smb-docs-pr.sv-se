---
title: "Datum för beräkning av inköp | Microsoft Docs"
description: "Programmet beräknar automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum. Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7e569474e3d222a56500665fa73408f47480f338
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="454c8-104">Datumberäkning för inköp</span><span class="sxs-lookup"><span data-stu-id="454c8-104">Date Calculation for Purchases</span></span>
<span data-ttu-id="454c8-105">I [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknas automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum.</span><span class="sxs-lookup"><span data-stu-id="454c8-105">[!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="454c8-106">Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.</span><span class="sxs-lookup"><span data-stu-id="454c8-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="454c8-107">Om du anger ett begärt inleveransdatum i en inköpsorderhuvud, är det beräknade orderdatumet det datum då ordern måste placeras för inleverans av artiklarna på datumet som du valde.</span><span class="sxs-lookup"><span data-stu-id="454c8-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="454c8-108">Då beräknas datumet då artiklarna är tillgängliga för plockning och visas i fältet **Förväntat inleveransdatum**.</span><span class="sxs-lookup"><span data-stu-id="454c8-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="454c8-109">Om inget begärt inleveransdatum anges används orderdatumet på raden som utgångspunkt när programmet beräknar det datum då du kan förvänta dig att ta emot artiklarna och det datum då artiklarna kommer att vara tillgängliga för plockning.</span><span class="sxs-lookup"><span data-stu-id="454c8-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="454c8-110">Beräkna med ett begärt inleveransdatum</span><span class="sxs-lookup"><span data-stu-id="454c8-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="454c8-111">Om ett begärt inleveransdatum angetts på inköpsorderraden används detta datum som utgångspunkt i följande beräkningar:</span><span class="sxs-lookup"><span data-stu-id="454c8-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="454c8-112">begärt inleveransdatum – ledtidsberäkning = orderdatum</span><span class="sxs-lookup"><span data-stu-id="454c8-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="454c8-113">begärt inleveransdatum + ankommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum</span><span class="sxs-lookup"><span data-stu-id="454c8-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="454c8-114">Om du angett ett begärt inleveransdatum i inköpsorderhuvudet kopieras detta datum till motsvarande fält på alla raderna.</span><span class="sxs-lookup"><span data-stu-id="454c8-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="454c8-115">Du kan ändra datumet på raderna eller ta bort datumet på raden.</span><span class="sxs-lookup"><span data-stu-id="454c8-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="454c8-116">Beräkna utan begärt leveransdatum</span><span class="sxs-lookup"><span data-stu-id="454c8-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="454c8-117">Om du skriver in en inköpsorderrad utan ett begärt leveransdatum fylls fältet **Orderdatum** i automatiskt med datumet i fältet **Orderdatum** i inköpshuvudet.</span><span class="sxs-lookup"><span data-stu-id="454c8-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="454c8-118">Detta datum är antingen det datum du angett eller arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="454c8-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="454c8-119">Därefter utförs följande datumberäkningar för inköpsorderraden, med utgångspunkt från orderdatumet:</span><span class="sxs-lookup"><span data-stu-id="454c8-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="454c8-120">orderdatum + ledtidsberäkning = planerat inleveransdatum.</span><span class="sxs-lookup"><span data-stu-id="454c8-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="454c8-121">planerat inleveransdatum + ankommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum</span><span class="sxs-lookup"><span data-stu-id="454c8-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="454c8-122">Om du ändrar orderdatumet på raden, t.ex. om artiklarna inte är tillgängliga hos leverantören förrän vid ett senare datum, beräknas de aktuella datumen automatiskt om på raden.</span><span class="sxs-lookup"><span data-stu-id="454c8-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="454c8-123">Om du ändrar orderdatumet i huvudet kopieras detta datum till fältet **Orderdatum** på samtliga rader, varefter alla relaterade datumfält beräknas om.</span><span class="sxs-lookup"><span data-stu-id="454c8-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="454c8-124">Se även</span><span class="sxs-lookup"><span data-stu-id="454c8-124">See Also</span></span>  
 <span data-ttu-id="454c8-125">[Datumberäkning för försäljning](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="454c8-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="454c8-126">Så här beräknar du ett orderlöftesdatum</span><span class="sxs-lookup"><span data-stu-id="454c8-126">How to: Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="454c8-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="454c8-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
