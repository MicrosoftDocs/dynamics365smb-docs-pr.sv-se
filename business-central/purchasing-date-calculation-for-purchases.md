---
title: Datum för beräkning av inköp | Microsoft Docs
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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 41b1b1b0459706a8c061a0044824b5b7c4c9aa62
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312586"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="8d0b0-104">Datumberäkning för inköp</span><span class="sxs-lookup"><span data-stu-id="8d0b0-104">Date Calculation for Purchases</span></span>
<span data-ttu-id="8d0b0-105">I [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknas automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-105">[!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="8d0b0-106">Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="8d0b0-107">Om du anger ett begärt inleveransdatum i en inköpsorderhuvud, är det beräknade orderdatumet det datum då ordern måste placeras för inleverans av artiklarna på datumet som du valde.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="8d0b0-108">Då beräknas datumet då artiklarna är tillgängliga för plockning och visas i fältet **Förväntat inleveransdatum**.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="8d0b0-109">Om inget begärt inleveransdatum anges används orderdatumet på raden som utgångspunkt när programmet beräknar det datum då du kan förvänta dig att ta emot artiklarna och det datum då artiklarna kommer att vara tillgängliga för plockning.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="8d0b0-110">Beräkna med ett begärt inleveransdatum</span><span class="sxs-lookup"><span data-stu-id="8d0b0-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="8d0b0-111">Om ett begärt inleveransdatum angetts på inköpsorderraden används detta datum som utgångspunkt i följande beräkningar:</span><span class="sxs-lookup"><span data-stu-id="8d0b0-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="8d0b0-112">begärt inleveransdatum – ledtidsberäkning = orderdatum</span><span class="sxs-lookup"><span data-stu-id="8d0b0-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="8d0b0-113">begärt inleveransdatum + ankommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum</span><span class="sxs-lookup"><span data-stu-id="8d0b0-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="8d0b0-114">Om du angett ett begärt inleveransdatum i inköpsorderhuvudet kopieras detta datum till motsvarande fält på alla raderna.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="8d0b0-115">Du kan ändra datumet på raderna eller ta bort datumet på raden.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!Note]
> <span data-ttu-id="8d0b0-116">Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda inleveransdatumet för att hämta planerat orderdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D", i fem dagar eller "1V" i en vecka.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="8d0b0-117">Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="8d0b0-118">Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="8d0b0-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="8d0b0-119">Beräkna utan begärt leveransdatum</span><span class="sxs-lookup"><span data-stu-id="8d0b0-119">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="8d0b0-120">Om du skriver in en inköpsorderrad utan ett begärt leveransdatum fylls fältet **Orderdatum** i automatiskt med datumet i fältet **Orderdatum** i inköpshuvudet.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="8d0b0-121">Detta datum är antingen det datum du angett eller arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="8d0b0-122">Därefter utförs följande datumberäkningar för inköpsorderraden, med utgångspunkt från orderdatumet:</span><span class="sxs-lookup"><span data-stu-id="8d0b0-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="8d0b0-123">orderdatum + ledtidsberäkning = planerat inleveransdatum.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="8d0b0-124">planerat inleveransdatum + ankommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum</span><span class="sxs-lookup"><span data-stu-id="8d0b0-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="8d0b0-125">Om du ändrar orderdatumet på raden, t.ex. om artiklarna inte är tillgängliga hos leverantören förrän vid ett senare datum, beräknas de aktuella datumen automatiskt om på raden.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="8d0b0-126">Om du ändrar orderdatumet i huvudet kopieras detta datum till fältet **Orderdatum** på samtliga rader, varefter alla relaterade datumfält beräknas om.</span><span class="sxs-lookup"><span data-stu-id="8d0b0-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d0b0-127">Se även</span><span class="sxs-lookup"><span data-stu-id="8d0b0-127">See Also</span></span>  
 <span data-ttu-id="8d0b0-128">[Datumberäkning för försäljning](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="8d0b0-128">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="8d0b0-129">Beräkna orderlöftesdatum</span><span class="sxs-lookup"><span data-stu-id="8d0b0-129">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="8d0b0-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d0b0-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
