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
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: sv-se
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="00141-103">Ange datumintervall</span><span class="sxs-lookup"><span data-stu-id="00141-103">Entering Date Ranges</span></span>
<span data-ttu-id="00141-104">Du kan ange filter som innehåller ett startdatum och ett slutdatum om du vill visa enbart de data som finns i datumintervallet eller tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="00141-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="00141-105">Speciella regler gäller för hur du kan ange datumintervall.</span><span class="sxs-lookup"><span data-stu-id="00141-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="00141-106">Ta **10 högsta kund** som exempel:</span><span class="sxs-lookup"><span data-stu-id="00141-106">Let's take the **Customer Top 10** as an example:</span></span>

![Ange ett datumintervall på sidan för begäran för listan över 10 högsta kund](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="00141-108">Här kan du begränsa rapporten till ett datumintervall, till exempel de två senaste veckorna eller totalt 6 veckor eller det intervall du vill använda.</span><span class="sxs-lookup"><span data-stu-id="00141-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="00141-109">Om du vill ange datumintervall, ange datum och använda någon **...**</span><span class="sxs-lookup"><span data-stu-id="00141-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="00141-110">Eller **|** för att ange projektintervall.</span><span class="sxs-lookup"><span data-stu-id="00141-110">or **|** to set the range.</span></span> <span data-ttu-id="00141-111">I vårt exempel, om du vill visa de 10 främsta kunderna för de första två veckorna ställer du in datumfiltret på *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="00141-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="00141-112">Här följer några andra exempel:</span><span class="sxs-lookup"><span data-stu-id="00141-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="00141-113">Betydelse</span><span class="sxs-lookup"><span data-stu-id="00141-113">Meaning</span></span> | <span data-ttu-id="00141-114">Exempel</span><span class="sxs-lookup"><span data-stu-id="00141-114">Example</span></span> | <span data-ttu-id="00141-115">Inkluderade transaktioner</span><span class="sxs-lookup"><span data-stu-id="00141-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="00141-116">Lika med</span><span class="sxs-lookup"><span data-stu-id="00141-116">Equal to</span></span>| <span data-ttu-id="00141-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="00141-117">12 15 16</span></span> |<span data-ttu-id="00141-118">Endast de som bokförts 15 december 2016.</span><span class="sxs-lookup"><span data-stu-id="00141-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="00141-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="00141-119">Interval</span></span>| <span data-ttu-id="00141-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="00141-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="00141-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="00141-121">..12 15 16</span></span>|<span data-ttu-id="00141-122">De som bokförts på datum mellan och inklusive 15 december 2016 och 15 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="00141-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="00141-123">De som bokförts 02-12-15 eller tidigare.</span><span class="sxs-lookup"><span data-stu-id="00141-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="00141-124">Antingen eller</span><span class="sxs-lookup"><span data-stu-id="00141-124">Either/or</span></span>|<span data-ttu-id="00141-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="00141-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="00141-126">Transaktioner registrerade antingen den 15 December eller 16 December 2016.</span><span class="sxs-lookup"><span data-stu-id="00141-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="00141-127">Om det finns transaktioner som bokförs båda dagarna kommer alla att visas.</span><span class="sxs-lookup"><span data-stu-id="00141-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="00141-128">Du kan också kombinera formattyperna.</span><span class="sxs-lookup"><span data-stu-id="00141-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="00141-129">Exempel</span><span class="sxs-lookup"><span data-stu-id="00141-129">Example</span></span> | <span data-ttu-id="00141-130">Inkluderade transaktioner</span><span class="sxs-lookup"><span data-stu-id="00141-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="00141-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="00141-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="00141-132">Transaktioner som bokförts antingen den 15 december 2016, eller på datum mellan och inklusive 01 december 2016 och 31 maj 2017.</span><span class="sxs-lookup"><span data-stu-id="00141-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="00141-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="00141-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="00141-134">Transaktioner bokförda 14 December eller tidigare, eller transaktioner bokförda 30 December eller senare – d.v.s. alla transaktioner utom de som bokförts på datum mellan och inklusive 15 December och 29.</span><span class="sxs-lookup"><span data-stu-id="00141-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="00141-135">Observera att vi har använt Amerikanskt datumformat MMDDÅÅ här.</span><span class="sxs-lookup"><span data-stu-id="00141-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="00141-136">När [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tillgängliga för andra marknader, kommer du att kunna använda de format som används.</span><span class="sxs-lookup"><span data-stu-id="00141-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="00141-137">Använda datumformler</span><span class="sxs-lookup"><span data-stu-id="00141-137">Using Date Formulas</span></span>
<span data-ttu-id="00141-138">En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas.</span><span class="sxs-lookup"><span data-stu-id="00141-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="00141-139">Du kan ange datumformler i olika beräkningsfält för datum och i fält för återkomstfrekvens i återkommande journaler.</span><span class="sxs-lookup"><span data-stu-id="00141-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="00141-140">I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar.</span><span class="sxs-lookup"><span data-stu-id="00141-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="00141-141">Om du till exempel anger **1V** är perioden därefter faktiskt åtta dagar eftersom idag inkluderas.</span><span class="sxs-lookup"><span data-stu-id="00141-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="00141-142">För att ange en period om sju dagar (en exakt vecka) inklusive perioden för startdatum måste du ange **6D** eller **1V\-1D**.</span><span class="sxs-lookup"><span data-stu-id="00141-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="00141-143">Här följer några exempel på hur datumformler kan användas:</span><span class="sxs-lookup"><span data-stu-id="00141-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="00141-144">Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="00141-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="00141-145">Datumformeln i fältet **Betalningsfrist** för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet (eller från förfallodatumet för den föregående påminnelsen) innan en påminnelse ska skapas.</span><span class="sxs-lookup"><span data-stu-id="00141-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="00141-146">Datumformeln i fältet **Förfallodatumformel** bestämmer hur förfallodatumet på påminnelsen beräknas.</span><span class="sxs-lookup"><span data-stu-id="00141-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="00141-147">Formeln för datumberäkning kan bara omfatta högst 20 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="00141-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="00141-148">Du kan använda följande bokstäver som förkortningar för tidsangivelser.</span><span class="sxs-lookup"><span data-stu-id="00141-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="00141-149">Bokstav</span><span class="sxs-lookup"><span data-stu-id="00141-149">Letter</span></span>  |  <span data-ttu-id="00141-150">Tidsspecifikation</span><span class="sxs-lookup"><span data-stu-id="00141-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="00141-151">S</span><span class="sxs-lookup"><span data-stu-id="00141-151">C</span></span>|<span data-ttu-id="00141-152">Löpande (innevarande)</span><span class="sxs-lookup"><span data-stu-id="00141-152">Current</span></span>|
|<span data-ttu-id="00141-153">D</span><span class="sxs-lookup"><span data-stu-id="00141-153">D</span></span>|<span data-ttu-id="00141-154">Dag\(ar\)</span><span class="sxs-lookup"><span data-stu-id="00141-154">Day\(s\)</span></span>|
|<span data-ttu-id="00141-155">V</span><span class="sxs-lookup"><span data-stu-id="00141-155">W</span></span>|<span data-ttu-id="00141-156">Vecka\(veckor\)</span><span class="sxs-lookup"><span data-stu-id="00141-156">Week\(s\)</span></span>|
|<span data-ttu-id="00141-157">M</span><span class="sxs-lookup"><span data-stu-id="00141-157">M</span></span>|<span data-ttu-id="00141-158">Månad\(er\)</span><span class="sxs-lookup"><span data-stu-id="00141-158">Month\(s\)</span></span>|
|<span data-ttu-id="00141-159">K</span><span class="sxs-lookup"><span data-stu-id="00141-159">Q</span></span>|<span data-ttu-id="00141-160">Kvartal</span><span class="sxs-lookup"><span data-stu-id="00141-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="00141-161">Å</span><span class="sxs-lookup"><span data-stu-id="00141-161">Y</span></span>|<span data-ttu-id="00141-162">År</span><span class="sxs-lookup"><span data-stu-id="00141-162">Year\(s\)</span></span>|

<span data-ttu-id="00141-163">Du kan bygga upp en datumformel på tre sätt.</span><span class="sxs-lookup"><span data-stu-id="00141-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="00141-164">Följande exempel visar hur du använder **L** för löpande, plus en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="00141-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="00141-165">Uttryck</span><span class="sxs-lookup"><span data-stu-id="00141-165">Expression</span></span>  |  <span data-ttu-id="00141-166">Betydelse</span><span class="sxs-lookup"><span data-stu-id="00141-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="00141-167">LV</span><span class="sxs-lookup"><span data-stu-id="00141-167">CW</span></span>|<span data-ttu-id="00141-168">Löpande (innevarande) vecka</span><span class="sxs-lookup"><span data-stu-id="00141-168">Current week</span></span>|
|<span data-ttu-id="00141-169">LM</span><span class="sxs-lookup"><span data-stu-id="00141-169">CM</span></span>|<span data-ttu-id="00141-170">Löpande (innevarande) månad</span><span class="sxs-lookup"><span data-stu-id="00141-170">Current month</span></span>|

<span data-ttu-id="00141-171">Följande exempel visar hur du använder ett tal och en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="00141-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="00141-172">Ett nummer får inte vara högre än 9 999.</span><span class="sxs-lookup"><span data-stu-id="00141-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="00141-173">Uttryck</span><span class="sxs-lookup"><span data-stu-id="00141-173">Expression</span></span>  |  <span data-ttu-id="00141-174">Betydelse</span><span class="sxs-lookup"><span data-stu-id="00141-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="00141-175">10D</span><span class="sxs-lookup"><span data-stu-id="00141-175">10D</span></span>|<span data-ttu-id="00141-176">Tio dagar från dagens datum.</span><span class="sxs-lookup"><span data-stu-id="00141-176">10 days from today</span></span>|
|<span data-ttu-id="00141-177">2V</span><span class="sxs-lookup"><span data-stu-id="00141-177">2W</span></span>|<span data-ttu-id="00141-178">Två veckor från dagens datum</span><span class="sxs-lookup"><span data-stu-id="00141-178">2 weeks from today</span></span>|

<span data-ttu-id="00141-179">Följande exempel visar hur du använder en tidsenhet och ett tal.</span><span class="sxs-lookup"><span data-stu-id="00141-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="00141-180">Uttryck</span><span class="sxs-lookup"><span data-stu-id="00141-180">Expression</span></span>  |  <span data-ttu-id="00141-181">Betydelse</span><span class="sxs-lookup"><span data-stu-id="00141-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="00141-182">D10</span><span class="sxs-lookup"><span data-stu-id="00141-182">D10</span></span>|<span data-ttu-id="00141-183">Den tionde dagen varje månad.</span><span class="sxs-lookup"><span data-stu-id="00141-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="00141-184">VD4</span><span class="sxs-lookup"><span data-stu-id="00141-184">WD4</span></span>|<span data-ttu-id="00141-185">Den nästa fjärde dagen i en vecka \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="00141-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="00141-186">Följande exempel visar hur du kombinera dessa tre metoder om så behövs.</span><span class="sxs-lookup"><span data-stu-id="00141-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="00141-187">Uttryck</span><span class="sxs-lookup"><span data-stu-id="00141-187">Expression</span></span>  |  <span data-ttu-id="00141-188">Betydelse</span><span class="sxs-lookup"><span data-stu-id="00141-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="00141-189">LM\+10D</span><span class="sxs-lookup"><span data-stu-id="00141-189">CM\+10D</span></span>|<span data-ttu-id="00141-190">Löpande månad \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="00141-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="00141-191">Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.</span><span class="sxs-lookup"><span data-stu-id="00141-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="00141-192">Uttryck</span><span class="sxs-lookup"><span data-stu-id="00141-192">Expression</span></span>  |  <span data-ttu-id="00141-193">Betydelse</span><span class="sxs-lookup"><span data-stu-id="00141-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="00141-194">-1Å</span><span class="sxs-lookup"><span data-stu-id="00141-194">-1Y</span></span>|<span data-ttu-id="00141-195">1 år sedan från idag</span><span class="sxs-lookup"><span data-stu-id="00141-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="00141-196">Om lagerstället använder en baskalender, tolkas datumformeln som du anger i t.ex. fältet **Leveranstid** enligt kalenderarbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="00141-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="00141-197">Till exempel betyder **1V** sju arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="00141-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="00141-198">Se även</span><span class="sxs-lookup"><span data-stu-id="00141-198">See Also</span></span>
<span data-ttu-id="00141-199">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00141-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="00141-200">Datumberäkning för inköp</span><span class="sxs-lookup"><span data-stu-id="00141-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="00141-201">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="00141-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

