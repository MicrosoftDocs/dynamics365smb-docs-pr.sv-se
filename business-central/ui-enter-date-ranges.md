---
title: Ange datumintervall i Business Central | Microsoft Docs
description: "Lära dig hur du får en rapport med data från specifika tidsperioder med datumintervall i Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 552578ce097f7f647ed0962fec0448059d3ca3b2
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="d584d-103">Ange datumintervall</span><span class="sxs-lookup"><span data-stu-id="d584d-103">Entering Date Ranges</span></span> 
<span data-ttu-id="d584d-104">Du kan ange filter som innehåller ett startdatum och ett slutdatum om du vill visa enbart de data som finns i datumintervallet eller tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="d584d-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="d584d-105">Speciella regler gäller för hur du kan ange datumintervall.</span><span class="sxs-lookup"><span data-stu-id="d584d-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="d584d-106">Ta **10 högsta kund** som exempel:</span><span class="sxs-lookup"><span data-stu-id="d584d-106">Let's take the **Customer Top 10** as an example:</span></span>

![Ange ett datumintervall på sidan för begäran för listan över 10 högsta kund](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="d584d-108">Här kan du begränsa rapporten till ett datumintervall, till exempel de två senaste veckorna eller totalt 6 veckor eller det intervall du vill använda.</span><span class="sxs-lookup"><span data-stu-id="d584d-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="d584d-109">Om du vill ange datumintervall, ange datum och använda någon **...**</span><span class="sxs-lookup"><span data-stu-id="d584d-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="d584d-110">Eller **|** för att ange projektintervall.</span><span class="sxs-lookup"><span data-stu-id="d584d-110">or **|** to set the range.</span></span> <span data-ttu-id="d584d-111">I vårt exempel, om du vill visa de 10 främsta kunderna för de första två veckorna ställer du in datumfiltret på *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="d584d-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="d584d-112">Här följer några andra exempel:</span><span class="sxs-lookup"><span data-stu-id="d584d-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="d584d-113">Betydelse</span><span class="sxs-lookup"><span data-stu-id="d584d-113">Meaning</span></span> | <span data-ttu-id="d584d-114">Exempel</span><span class="sxs-lookup"><span data-stu-id="d584d-114">Example</span></span> | <span data-ttu-id="d584d-115">Inkluderade transaktioner</span><span class="sxs-lookup"><span data-stu-id="d584d-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="d584d-116">Lika med</span><span class="sxs-lookup"><span data-stu-id="d584d-116">Equal to</span></span>| <span data-ttu-id="d584d-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="d584d-117">12 15 16</span></span> |<span data-ttu-id="d584d-118">Endast de som bokförts 15 december 2016.</span><span class="sxs-lookup"><span data-stu-id="d584d-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="d584d-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="d584d-119">Interval</span></span>| <span data-ttu-id="d584d-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="d584d-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="d584d-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="d584d-121">..12 15 16</span></span>|<span data-ttu-id="d584d-122">De som bokförts på datum mellan och inklusive 15 december 2016 och 15 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="d584d-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="d584d-123">De som bokförts 02-12-15 eller tidigare.</span><span class="sxs-lookup"><span data-stu-id="d584d-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="d584d-124">Antingen eller</span><span class="sxs-lookup"><span data-stu-id="d584d-124">Either/or</span></span>|<span data-ttu-id="d584d-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="d584d-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="d584d-126">Transaktioner registrerade antingen den 15 December eller 16 December 2016.</span><span class="sxs-lookup"><span data-stu-id="d584d-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="d584d-127">Om det finns transaktioner som bokförs båda dagarna kommer alla att visas.</span><span class="sxs-lookup"><span data-stu-id="d584d-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="d584d-128">Du kan också kombinera formattyperna.</span><span class="sxs-lookup"><span data-stu-id="d584d-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="d584d-129">Exempel</span><span class="sxs-lookup"><span data-stu-id="d584d-129">Example</span></span> | <span data-ttu-id="d584d-130">Inkluderade transaktioner</span><span class="sxs-lookup"><span data-stu-id="d584d-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="d584d-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="d584d-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="d584d-132">Transaktioner som bokförts antingen den 15 december 2016, eller på datum mellan och inklusive 01 december 2016 och 31 maj 2017.</span><span class="sxs-lookup"><span data-stu-id="d584d-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="d584d-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="d584d-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="d584d-134">Transaktioner bokförda 14 December eller tidigare, eller transaktioner bokförda 30 December eller senare – d.v.s. alla transaktioner utom de som bokförts på datum mellan och inklusive 15 December och 29.</span><span class="sxs-lookup"><span data-stu-id="d584d-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="d584d-135">Observera att vi har använt Amerikanskt datumformat MMDDÅÅ här.</span><span class="sxs-lookup"><span data-stu-id="d584d-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="d584d-136">När [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tillgängliga för andra marknader, kommer du att kunna använda de format som används.</span><span class="sxs-lookup"><span data-stu-id="d584d-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="d584d-137">Se även</span><span class="sxs-lookup"><span data-stu-id="d584d-137">See Also</span></span>
<span data-ttu-id="d584d-138">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d584d-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d584d-139">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="d584d-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="d584d-140">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="d584d-140">General Business Functionality</span></span>](ui-across-business-areas.md)
