---
title: Ange datum och tider i Business Central | Microsoft Docs
description: "Lära dig att ange datum och tider, inklusive olika tips för produktivitet till exempel snabbskrift, uttryck och intervaller. Filtrera listor eller rapporter till specifika datum- och tidsperioder."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8717d60a8449ca300eaf9c1a5c4b137ea1a1a247
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---

# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="93ab0-104">Arbeta med kalenderdatum och tider</span><span class="sxs-lookup"><span data-stu-id="93ab0-104">Working with Calendar Dates and Times</span></span>
[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="93ab0-105">ger flera sätt för att ange datum och tider, inklusive kraftfulla funktioner som förbättrar datainmatning eller hjälper dig att skriva komplexa kalenderuttryck.</span><span class="sxs-lookup"><span data-stu-id="93ab0-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="93ab0-106">Det finns olika ställen i programmet där du kan ange datum och tider i ett fält.</span><span class="sxs-lookup"><span data-stu-id="93ab0-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="93ab0-107">På t.ex. en försäljningsorder kan du ange leveransdatumet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="93ab0-108">När du filtrerar listor eller rapportdata, kan du ange datum och tider för att precisera endast den information som du är intresserad av.</span><span class="sxs-lookup"><span data-stu-id="93ab0-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="93ab0-109">Kontrollera inställningarna för region och språk</span><span class="sxs-lookup"><span data-stu-id="93ab0-109">Check your region and language settings</span></span>
<span data-ttu-id="93ab0-110">[**Mina inställningar**](https://businesscentral.dynamics.com?page=9176 "Gå direkt till sidan för användarinställningar i Business Central") anger **region** och **språk** som används i programmet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="93ab0-111">Dessa inställningar påverkar hur du anger datum och tid.</span><span class="sxs-lookup"><span data-stu-id="93ab0-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="93ab0-112">Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras.</span><span class="sxs-lookup"><span data-stu-id="93ab0-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="93ab0-113">För datummönster som omfattar ord måste språket för de ord som du använder stämma överens med **språk**-inställningen.</span><span class="sxs-lookup"><span data-stu-id="93ab0-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="93ab0-114">använder det gregorianska kalendersystemet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->
## <a name="entering-dates"></a><span data-ttu-id="93ab0-115">Ange datum</span><span class="sxs-lookup"><span data-stu-id="93ab0-115">Entering Dates</span></span>
<span data-ttu-id="93ab0-116">I ett datumfält kan du ange ett datum med standardformat för din region.</span><span class="sxs-lookup"><span data-stu-id="93ab0-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="93ab0-117">Olika områden kan använda olika avgränsare mellan dagar, månader och år.</span><span class="sxs-lookup"><span data-stu-id="93ab0-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="93ab0-118">Exempelvis vissa regioner använder bindestreck (åååå-mm-dd) och andra använda snedstreck (åååå/mm/dd).</span><span class="sxs-lookup"><span data-stu-id="93ab0-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="93ab0-119">Du kan använda alla avgränsare, även blanksteg och datumet ändras automatiskt till att använda avgränsare som matchar din region.</span><span class="sxs-lookup"><span data-stu-id="93ab0-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="93ab0-120">Observera att formatet som datum visas på utskrivna rapporter eller e-postade dokument påverkas inte av dina personliga inställningar av region.</span><span class="sxs-lookup"><span data-stu-id="93ab0-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="93ab0-121">Om du vill arbeta mer effektivt med datum och tider, använd någon av de metoder eller format som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="93ab0-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="93ab0-122">Välja datum från kalendern</span><span class="sxs-lookup"><span data-stu-id="93ab0-122">Picking dates from the calendar</span></span>
<span data-ttu-id="93ab0-123">Ett fält som visar en kalenderikon kan anges med hjälp av kalenderdatumväljaren.</span><span class="sxs-lookup"><span data-stu-id="93ab0-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="93ab0-124">Om du vill visa kalenderdatumväljaren, aktivera kalenderikonen eller tryck på kortkommandot Ctrl + Home i fältet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="93ab0-125">![Datumfält](media/ui-date-field.png "Exempel på ett datumfält")</span><span class="sxs-lookup"><span data-stu-id="93ab0-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="93ab0-126">Se även [Kortkommandon i kalenderdatumväljaren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="93ab0-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="today"></a><span data-ttu-id="93ab0-127">I dag</span><span class="sxs-lookup"><span data-stu-id="93ab0-127">Today</span></span>
<span data-ttu-id="93ab0-128">Ange ordet for `today`, på det språk anges i **språk** inställningen som ska ange datumet till det aktuella datumet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-128">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="93ab0-129">Istället för att ange hela ordet, kan du skriva in delar av ordet från början såsom `t` eller `tod`, förutsatt att det inte är också är början på ett annat ord.</span><span class="sxs-lookup"><span data-stu-id="93ab0-129">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="93ab0-130">Dag\-vecka\-år-mönster</span><span class="sxs-lookup"><span data-stu-id="93ab0-130">Day\-week\-year pattern</span></span>
<span data-ttu-id="93ab0-131">Du kan ange ett datum som en veckodag följt av ett veckonummer och alternativt ett år.</span><span class="sxs-lookup"><span data-stu-id="93ab0-131">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="93ab0-132">Till exempel `Mon25` eller `mon25` betyder måndag vecka 25.</span><span class="sxs-lookup"><span data-stu-id="93ab0-132">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="93ab0-133">Om du inte anger ett år används året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-133">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="93ab0-134">I stället för att ange hela ordet för dagen i veckan, kan du skriva in del av ordet, från början.</span><span class="sxs-lookup"><span data-stu-id="93ab0-134">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="93ab0-135">Om det uppstår konflikter (exempelvis med `s` som kan vara Saturday (lördag) eller Sunday (söndag)), utvärderas dagarna utifrån regionsinställningen.</span><span class="sxs-lookup"><span data-stu-id="93ab0-135">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="93ab0-136">Indata utvärderas först mot `workdate`och `today`, så tänk på detta när du förkortar.</span><span class="sxs-lookup"><span data-stu-id="93ab0-136">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="93ab0-137">Till exempel `t` innebär today (idag), så det kan inte innebära: tisdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="93ab0-137">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="93ab0-138">Veckonummersystemet är alltid ISO-8601 där vecka 1 är veckan med 4 januari eller veckan med första torsdagen på året.</span><span class="sxs-lookup"><span data-stu-id="93ab0-138">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="93ab0-139">Siffermönster</span><span class="sxs-lookup"><span data-stu-id="93ab0-139">Digit patterns</span></span>
<span data-ttu-id="93ab0-140">I ett datumfält kan du skriva in två, fyra, sex eller åtta siffror.</span><span class="sxs-lookup"><span data-stu-id="93ab0-140">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="93ab0-141">Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-141">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="93ab0-142">Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-142">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="93ab0-143">Order för den dagen och månaden avgörs av dina regioninställningar.</span><span class="sxs-lookup"><span data-stu-id="93ab0-143">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="93ab0-144">Även om dina regioninställningar har året före dagen och månaden, tolkas fyra siffror som dag och månad.</span><span class="sxs-lookup"><span data-stu-id="93ab0-144">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="93ab0-145">Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.</span><span class="sxs-lookup"><span data-stu-id="93ab0-145">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="current-work-date"></a><span data-ttu-id="93ab0-146">Aktuellt arbetsdatum</span><span class="sxs-lookup"><span data-stu-id="93ab0-146">Current work date</span></span>
<span data-ttu-id="93ab0-147">Funktionen arbetsdatum låter dig spåra transaktioner med ett datum som skiljer sig från det aktuella datumet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-147">The work date feature allows you to record transations using a date that is different from the current date.</span></span>

<span data-ttu-id="93ab0-148">Ordet för ”arbetsdatum” på det språk som anges av **språk**-inställningen kan ange datumet till det aktuella arbetsdatumet som anges på sidan [**Mina inställningar**](https://businesscentral.dynamics.com?page=9176 "Gå direkt till sidan för användarinställningar i Business Central").</span><span class="sxs-lookup"><span data-stu-id="93ab0-148">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="93ab0-149">I stället för att ange hela ordet, kan du skriva in del av ordet, från början, såsom "a" eller "arbete".</span><span class="sxs-lookup"><span data-stu-id="93ab0-149">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="93ab0-150">Om du inte har definierat ett arbetsdatum, kommer det aktuella datumet användas som arbetsdatum.</span><span class="sxs-lookup"><span data-stu-id="93ab0-150">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="93ab0-151">Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.</span><span class="sxs-lookup"><span data-stu-id="93ab0-151">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="93ab0-152">Se även [Ändra grundläggande inställningar, såsom arbetsdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="93ab0-152">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date)</span></span>

### <a name="closing-date"></a><span data-ttu-id="93ab0-153">Avslutsdatum</span><span class="sxs-lookup"><span data-stu-id="93ab0-153">Closing Date</span></span>
<span data-ttu-id="93ab0-154">När du avslutar ett räkenskapsår kan du använda avslutsdatum för att ange att en transaktion är en bokslutspost.</span><span class="sxs-lookup"><span data-stu-id="93ab0-154">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="93ab0-155">Ett avslutsdatum ligger tekniskt sätt mellan två datum, till exempel mellan den 31 december och den 1 januari.</span><span class="sxs-lookup"><span data-stu-id="93ab0-155">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="93ab0-156">För att ange att ett datum är ett stängningsdatum ange `C` före datumet såsom `C123101`.</span><span class="sxs-lookup"><span data-stu-id="93ab0-156">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="93ab0-157">Detta kan användas tillsammans med alla datummönster.</span><span class="sxs-lookup"><span data-stu-id="93ab0-157">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="93ab0-158">Exempel</span><span class="sxs-lookup"><span data-stu-id="93ab0-158">Examples</span></span>
<span data-ttu-id="93ab0-159">Följande tabell innehåller exempel på datum med alla format.</span><span class="sxs-lookup"><span data-stu-id="93ab0-159">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="93ab0-160">Det förutsätter regioninställningar som formaterar datum enligt: **år.månad.dag.**, en vecka med start på måndag och på engelska.</span><span class="sxs-lookup"><span data-stu-id="93ab0-160">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="93ab0-161">**Format**</span><span class="sxs-lookup"><span data-stu-id="93ab0-161">**Entry**</span></span>      |<span data-ttu-id="93ab0-162">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="93ab0-162">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="93ab0-163">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="93ab0-163">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="93ab0-164">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="93ab0-164">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="93ab0-165">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="93ab0-165">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="93ab0-166">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="93ab0-166">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="93ab0-167">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="93ab0-167">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="93ab0-168">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="93ab0-168">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="93ab0-169">arbetsdatum år.arbetsdatum månad.11.</span><span class="sxs-lookup"><span data-stu-id="93ab0-169">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="93ab0-170">arbetsdatum år.11.12.</span><span class="sxs-lookup"><span data-stu-id="93ab0-170">work date year.11.12.</span></span>|
|<span data-ttu-id="93ab0-171">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="93ab0-171">`t` or `today`</span></span>|<span data-ttu-id="93ab0-172">dagens datum</span><span class="sxs-lookup"><span data-stu-id="93ab0-172">today's date</span></span>|
|<span data-ttu-id="93ab0-173">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="93ab0-173">`w` or `workdate`</span></span>|<span data-ttu-id="93ab0-174">arbetsdatum</span><span class="sxs-lookup"><span data-stu-id="93ab0-174">the working date</span></span>|
|<span data-ttu-id="93ab0-175">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-175">`m` or `Monday`</span></span>|<span data-ttu-id="93ab0-176">Måndag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="93ab0-176">Monday of the work date week</span></span>|
|<span data-ttu-id="93ab0-177">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-177">`tu` or `Tuesday`</span></span>|<span data-ttu-id="93ab0-178">Tisdag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="93ab0-178">Tuesday of the work date week</span></span>|
|<span data-ttu-id="93ab0-179">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-179">`sa` or `Saturday`</span></span>|<span data-ttu-id="93ab0-180">Lördag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="93ab0-180">Saturday of the work date week</span></span>|
|<span data-ttu-id="93ab0-181">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-181">`s` or `Sunday`</span></span>|<span data-ttu-id="93ab0-182">Söndag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="93ab0-182">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="93ab0-183">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="93ab0-183">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="93ab0-184">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="93ab0-184">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="93ab0-185">Tisdag av vecka 1 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="93ab0-185">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="93ab0-186">Inställningsintervall</span><span class="sxs-lookup"><span data-stu-id="93ab0-186">Setting Ranges</span></span>
<span data-ttu-id="93ab0-187">I listor, summor och rapporter kan du ange filter för datum, tid och datum och tid som innehåller ett startvärde och ett slutvärde om du endast vill visa de data som finns inom intervallet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-187">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="93ab0-188">Standardregler gäller för hur du kan ange datumintervall.</span><span class="sxs-lookup"><span data-stu-id="93ab0-188">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="93ab0-189">**Betydelse**</span><span class="sxs-lookup"><span data-stu-id="93ab0-189">**Meaning**</span></span>|<span data-ttu-id="93ab0-190">**Exempeluttryck (datum)**</span><span class="sxs-lookup"><span data-stu-id="93ab0-190">**Sample expression (Date)**</span></span>|<span data-ttu-id="93ab0-191">**Data som ingår i filtret**</span><span class="sxs-lookup"><span data-stu-id="93ab0-191">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="93ab0-192">Intervall</span><span class="sxs-lookup"><span data-stu-id="93ab0-192">Interval</span></span>|<span data-ttu-id="93ab0-193">`12 15 00..01 15 01`  \n`..12 15 00`</span><span class="sxs-lookup"><span data-stu-id="93ab0-193">`12 15 00..01 15 01`  \n`..12 15 00`</span></span>|<span data-ttu-id="93ab0-194">Poster med datum från och med 00-12-15 till och med 01-01-15.</span><span class="sxs-lookup"><span data-stu-id="93ab0-194">Records with dates between and including 12 15 00 and 01 15 01.</span></span>  <span data-ttu-id="93ab0-195">\nPoster med datum 00-15-12 eller tidigare.</span><span class="sxs-lookup"><span data-stu-id="93ab0-195">\nRecords with dates of 12 15 00 or earlier.</span></span>|
|<span data-ttu-id="93ab0-196">Antingen eller</span><span class="sxs-lookup"><span data-stu-id="93ab0-196">Either/or</span></span>|<span data-ttu-id="93ab0-197">\`00-12-15</span><span class="sxs-lookup"><span data-stu-id="93ab0-197">\`12 15 00</span></span>|<span data-ttu-id="93ab0-198">00-12-16\`</span><span class="sxs-lookup"><span data-stu-id="93ab0-198">12 16 00\`</span></span>|<span data-ttu-id="93ab0-199">Poster med antingen 00-12-15 eller 00-12-16.</span><span class="sxs-lookup"><span data-stu-id="93ab0-199">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="93ab0-200">Om det finns poster med datum båda dagarna kommer samtliga att visas.</span><span class="sxs-lookup"><span data-stu-id="93ab0-200">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="93ab0-201">Kombination</span><span class="sxs-lookup"><span data-stu-id="93ab0-201">Combination</span></span>|<span data-ttu-id="93ab0-202">\`00-12-15</span><span class="sxs-lookup"><span data-stu-id="93ab0-202">\`12 15 00</span></span>|<span data-ttu-id="93ab0-203">00-12-01..00-12-10`  \n`..00-12-14</span><span class="sxs-lookup"><span data-stu-id="93ab0-203">12 01 00..12 10 00`  \n`..12 14 00</span></span>|<span data-ttu-id="93ab0-204">00-12-30..\`</span><span class="sxs-lookup"><span data-stu-id="93ab0-204">12 30 00..\`</span></span>|<span data-ttu-id="93ab0-205">Poster med datum 00-12-15 eller mellan och inklusive den 00-12-01 och 00-12-10.</span><span class="sxs-lookup"><span data-stu-id="93ab0-205">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="93ab0-206">\nPoster med datum 00-12-14 eller tidigare, eller 00-12-30 eller senare. Detta innebär alla poster utom de med datum från och med 00-12-15 till och med 00-12-29.</span><span class="sxs-lookup"><span data-stu-id="93ab0-206">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="93ab0-207">Du kan använda giltiga format i filtret för datumintervall.</span><span class="sxs-lookup"><span data-stu-id="93ab0-207">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="93ab0-208">Till exempel `mon14 3..t 4p` som tillämpas på ett datum/tidsfält resulterar i ett filter mellan 03:00 måndag vecka 14 det aktuella arbetsdatumets år, inklusive fram till i dag klockan 16:00.</span><span class="sxs-lookup"><span data-stu-id="93ab0-208">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>


## <a name="using-date-formulas"></a><span data-ttu-id="93ab0-209">Använda datumformler</span><span class="sxs-lookup"><span data-stu-id="93ab0-209">Using Date Formulas</span></span>
<span data-ttu-id="93ab0-210">En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas.</span><span class="sxs-lookup"><span data-stu-id="93ab0-210">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="93ab0-211">Du kan ange datumformler i olika fält eller filter för datumberäkning.</span><span class="sxs-lookup"><span data-stu-id="93ab0-211">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="93ab0-212">I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar.</span><span class="sxs-lookup"><span data-stu-id="93ab0-212">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="93ab0-213">Om du till exempel anger `1W`, är perioden därefter faktiskt åtta dagar eftersom idag inkluderas.</span><span class="sxs-lookup"><span data-stu-id="93ab0-213">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="93ab0-214">För att ange en period av sju dagar \(en exakt vecka\) inklusive perioden för startdatum måste du ange `6D` eller `1W-1D`.</span><span class="sxs-lookup"><span data-stu-id="93ab0-214">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="93ab0-215">Här följer några exempel på hur datumformler kan användas:</span><span class="sxs-lookup"><span data-stu-id="93ab0-215">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="93ab0-216">Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="93ab0-216">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="93ab0-217">Datumformeln i fältet **Betalningsfrist** för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet \(eller från den föregående påminnelsen\) innan en påminnelse ska skapas.</span><span class="sxs-lookup"><span data-stu-id="93ab0-217">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="93ab0-218">Datumformeln i fältet **Förfallodatumformel** bestämmer hur förfallodatumet på påminnelsen beräknas.</span><span class="sxs-lookup"><span data-stu-id="93ab0-218">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="93ab0-219">Datumformeln kan omfatta högst 20 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="93ab0-219">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="93ab0-220">Du kan använda följande bokstäver som förkortningar för kalenderenheter.</span><span class="sxs-lookup"><span data-stu-id="93ab0-220">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="93ab0-221">Bokstav</span><span class="sxs-lookup"><span data-stu-id="93ab0-221">Letter</span></span>  |  <span data-ttu-id="93ab0-222">Betydelse</span><span class="sxs-lookup"><span data-stu-id="93ab0-222">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="93ab0-223">Löpande (innevarande)</span><span class="sxs-lookup"><span data-stu-id="93ab0-223">Current</span></span>|
|`D`|<span data-ttu-id="93ab0-224">Dag\(ar\)</span><span class="sxs-lookup"><span data-stu-id="93ab0-224">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="93ab0-225">Vecka\(veckor\)</span><span class="sxs-lookup"><span data-stu-id="93ab0-225">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="93ab0-226">Månad\(er\)</span><span class="sxs-lookup"><span data-stu-id="93ab0-226">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="93ab0-227">Kvartal\(s\)</span><span class="sxs-lookup"><span data-stu-id="93ab0-227">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="93ab0-228">År\(\)</span><span class="sxs-lookup"><span data-stu-id="93ab0-228">Year\(s\)</span></span>|

<span data-ttu-id="93ab0-229">Du kan bygga upp en datumformel på tre sätt.</span><span class="sxs-lookup"><span data-stu-id="93ab0-229">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="93ab0-230">Följande exempel visar hur du använder `C`, för löpande, plus en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-230">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="93ab0-231">Uttryck</span><span class="sxs-lookup"><span data-stu-id="93ab0-231">Expression</span></span>  |  <span data-ttu-id="93ab0-232">Betydelse</span><span class="sxs-lookup"><span data-stu-id="93ab0-232">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="93ab0-233">Löpande (innevarande) vecka</span><span class="sxs-lookup"><span data-stu-id="93ab0-233">Current week</span></span>|
|`CM`|<span data-ttu-id="93ab0-234">Löpande (innevarande) månad</span><span class="sxs-lookup"><span data-stu-id="93ab0-234">Current month</span></span>|

<span data-ttu-id="93ab0-235">Följande exempel visar hur du använder ett tal och en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-235">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="93ab0-236">Ett nummer får inte vara högre än 9 999.</span><span class="sxs-lookup"><span data-stu-id="93ab0-236">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="93ab0-237">Uttryck</span><span class="sxs-lookup"><span data-stu-id="93ab0-237">Expression</span></span>  |  <span data-ttu-id="93ab0-238">Betydelse</span><span class="sxs-lookup"><span data-stu-id="93ab0-238">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="93ab0-239">Tio dagar från dagens datum.</span><span class="sxs-lookup"><span data-stu-id="93ab0-239">10 days from today</span></span>|
|`2W`|<span data-ttu-id="93ab0-240">Två veckor från dagens datum</span><span class="sxs-lookup"><span data-stu-id="93ab0-240">2 weeks from today</span></span>|

<span data-ttu-id="93ab0-241">Följande exempel visar hur du använder en tidsenhet och ett tal.</span><span class="sxs-lookup"><span data-stu-id="93ab0-241">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="93ab0-242">Uttryck</span><span class="sxs-lookup"><span data-stu-id="93ab0-242">Expression</span></span>  |  <span data-ttu-id="93ab0-243">Betydelse</span><span class="sxs-lookup"><span data-stu-id="93ab0-243">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="93ab0-244">Den tionde dagen varje månad.</span><span class="sxs-lookup"><span data-stu-id="93ab0-244">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="93ab0-245">Den nästa fjärde dagen i en vecka \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="93ab0-245">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="93ab0-246">Följande exempel visar hur du kombinera dessa tre metoder om så behövs.</span><span class="sxs-lookup"><span data-stu-id="93ab0-246">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="93ab0-247">Uttryck</span><span class="sxs-lookup"><span data-stu-id="93ab0-247">Expression</span></span>  |  <span data-ttu-id="93ab0-248">Betydelse</span><span class="sxs-lookup"><span data-stu-id="93ab0-248">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="93ab0-249">Löpande månad \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="93ab0-249">Current month \+ 10 days</span></span>|

<span data-ttu-id="93ab0-250">Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.</span><span class="sxs-lookup"><span data-stu-id="93ab0-250">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="93ab0-251">Uttryck</span><span class="sxs-lookup"><span data-stu-id="93ab0-251">Expression</span></span>  |  <span data-ttu-id="93ab0-252">Betydelse</span><span class="sxs-lookup"><span data-stu-id="93ab0-252">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="93ab0-253">1 år sedan från idag</span><span class="sxs-lookup"><span data-stu-id="93ab0-253">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="93ab0-254">Om lagerstället använder en baskalender, tolkas datumformeln som du anger i t.ex. fältet **Leveranstid** enligt kalenderarbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="93ab0-254">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="93ab0-255">Till exempel betyder `1W` sju arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="93ab0-255">For example, `1W`  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="93ab0-256">Ange tider</span><span class="sxs-lookup"><span data-stu-id="93ab0-256">Entering Times</span></span>
<span data-ttu-id="93ab0-257">När du anger tider kan du infoga alla icke-platsavgränsare som du vill mellan enheterna, men om du använder två siffror för varje enhet upp till millisekunder, är det inte obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="93ab0-257">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="93ab0-258">Du behöver bara skriva de största enheterna som du vill ha, övriga anges till noll.</span><span class="sxs-lookup"><span data-stu-id="93ab0-258">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="93ab0-259">Du kan också utelämna alla AM/PM-indikatorer.</span><span class="sxs-lookup"><span data-stu-id="93ab0-259">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="93ab0-260">I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.</span><span class="sxs-lookup"><span data-stu-id="93ab0-260">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="93ab0-261">Det följer regioninställningar som formaterar tid enligt: **Timmar:Minuter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="93ab0-261">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="93ab0-262">och använder du AM- och PM-indikatorer ”AM” och ”PM”.</span><span class="sxs-lookup"><span data-stu-id="93ab0-262">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="93ab0-263">**Format**</span><span class="sxs-lookup"><span data-stu-id="93ab0-263">**Entry**</span></span>      |<span data-ttu-id="93ab0-264">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="93ab0-264">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="93ab0-265">05:23:17</span><span class="sxs-lookup"><span data-stu-id="93ab0-265">05:23:17</span></span>|
|`5`|<span data-ttu-id="93ab0-266">05:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-266">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="93ab0-267">05:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-267">05:00:00</span></span>|
|`5P`|<span data-ttu-id="93ab0-268">17:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-268">17:00:00</span></span>|
|`12`|<span data-ttu-id="93ab0-269">12:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-269">12:00:00</span></span>|
|`12A`|<span data-ttu-id="93ab0-270">00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-270">00:00:00</span></span>|
|`12P`|<span data-ttu-id="93ab0-271">12:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-271">12:00:00</span></span>|
|`17`|<span data-ttu-id="93ab0-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-272">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="93ab0-273">05:30:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-273">05:30:00</span></span>|
|`0530`|<span data-ttu-id="93ab0-274">05:30:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-274">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="93ab0-275">05:30:05</span><span class="sxs-lookup"><span data-stu-id="93ab0-275">05:30:05</span></span>|
|`053005`|<span data-ttu-id="93ab0-276">05:30:05</span><span class="sxs-lookup"><span data-stu-id="93ab0-276">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="93ab0-277">05:30:050,5</span><span class="sxs-lookup"><span data-stu-id="93ab0-277">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="93ab0-278">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="93ab0-278">05:30:05.05</span></span>|

<span data-ttu-id="93ab0-279">Du bör vara medveten om att millisekunder ska tolkas som decimala systemet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-279">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="93ab0-280">Så till exempel `3`, `30` och `300` betyder alla 300 millisekunder, medan `03` betyder `30` och `003` innebär 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="93ab0-280">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="93ab0-281">Du kan inte använda `24:00` som midnatt eller välja ett värde som är större än 24:00.</span><span class="sxs-lookup"><span data-stu-id="93ab0-281">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="93ab0-282">Ordet för ”tid” på det språk som används av [!INCLUDE[d365fin](includes/d365fin_long_md.md)] utvärderas till aktuell tid på din dator eller mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-282">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="93ab0-283">Du kan skriva in alla ord, från början, såsom `t` eller `TIM`.</span><span class="sxs-lookup"><span data-stu-id="93ab0-283">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="93ab0-284">Ange kombinerade datum och tider</span><span class="sxs-lookup"><span data-stu-id="93ab0-284">Entering combined Dates and Times</span></span>
<span data-ttu-id="93ab0-285">När du anger datum och tid som datum och tid som kombineras till ett enda fält, måste du ange ett blanksteg mellan datumet och tiden.</span><span class="sxs-lookup"><span data-stu-id="93ab0-285">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="93ab0-286">Datumdelen kan bara innehålla blanksteg i form av officiella datumavgränsare för din regionsinställning.</span><span class="sxs-lookup"><span data-stu-id="93ab0-286">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="93ab0-287">Tiden kan innehålla blanksteg runt AM/PM-indikatorn.</span><span class="sxs-lookup"><span data-stu-id="93ab0-287">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="93ab0-288">Det är också möjligt att endast ange ett datum i ett fält för datum och tid, men det går inte att ange endast en gång.</span><span class="sxs-lookup"><span data-stu-id="93ab0-288">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="93ab0-289">I följande tabell visas några exempel på kombinationer av datum/tid.</span><span class="sxs-lookup"><span data-stu-id="93ab0-289">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="93ab0-290">Regioninställningarna i exemplen visar datum i dags\-månads\-årsformat med AM/PM-beteckningar, engelska språket och söndag som veckans början.</span><span class="sxs-lookup"><span data-stu-id="93ab0-290">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="93ab0-291">**Format**</span><span class="sxs-lookup"><span data-stu-id="93ab0-291">**Entry**</span></span>      |<span data-ttu-id="93ab0-292">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="93ab0-292">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="93ab0-293">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="93ab0-293">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="93ab0-294">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="93ab0-294">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="93ab0-295">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-295">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="93ab0-296">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-296">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="93ab0-297">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-297">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="93ab0-298">11\-arbetsdatum månad\-arbetsdatum år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-298">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="93ab0-299">11\-12\-arbetsdatum år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-299">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="93ab0-300">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="93ab0-300">`t` or `today`</span></span>|<span data-ttu-id="93ab0-301">dagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-301">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="93ab0-302">dagens datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-302">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="93ab0-303">dagens datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="93ab0-303">today's date 03:03:03</span></span>|
|<span data-ttu-id="93ab0-304">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="93ab0-304">`w` or `workdate`</span></span>|<span data-ttu-id="93ab0-305">arbetsdagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-305">the working date 00:00:00</span></span>|
|<span data-ttu-id="93ab0-306">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-306">`m` or `Monday`</span></span>|<span data-ttu-id="93ab0-307">Måndag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-307">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="93ab0-308">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-308">`tu` or `Tuesday`</span></span>|<span data-ttu-id="93ab0-309">Tisdag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-309">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="93ab0-310">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-310">`sa` or `Saturday`</span></span>|<span data-ttu-id="93ab0-311">Lördag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-311">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="93ab0-312">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="93ab0-312">`s` or `Sunday`</span></span>|<span data-ttu-id="93ab0-313">Söndag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-313">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="93ab0-314">Tisdag av arbetsdatumets vecka 10:30:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-314">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="93ab0-315">Tisdag av arbetsdatumets vecka 03:03:03</span><span class="sxs-lookup"><span data-stu-id="93ab0-315">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="93ab0-316">Tisdag i en vecka 23 av arbetsdatumets år, aktuell tid på dagen</span><span class="sxs-lookup"><span data-stu-id="93ab0-316">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="93ab0-317">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="93ab0-317">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="93ab0-318">Idag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="93ab0-318">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="93ab0-319">Tisdag av vecka 1 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="93ab0-319">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="93ab0-320">Ange varaktighet</span><span class="sxs-lookup"><span data-stu-id="93ab0-320">Entering Duration</span></span>
<span data-ttu-id="93ab0-321">Vissa fält i programmet representerar en varaktighet eller mängden förfluten tid, i stället för ett visst datum eller tid.</span><span class="sxs-lookup"><span data-stu-id="93ab0-321">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="93ab0-322">Du anger varaktigheten som en siffra följd av en enhet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-322">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="93ab0-323">Här följer några exempel.</span><span class="sxs-lookup"><span data-stu-id="93ab0-323">Here are some examples.</span></span>

|<span data-ttu-id="93ab0-324">**Varaktighet**</span><span class="sxs-lookup"><span data-stu-id="93ab0-324">**Duration**</span></span>|<span data-ttu-id="93ab0-325">**Enhet**</span><span class="sxs-lookup"><span data-stu-id="93ab0-325">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="93ab0-326">2 timmar</span><span class="sxs-lookup"><span data-stu-id="93ab0-326">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="93ab0-327">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="93ab0-327">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="93ab0-328">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="93ab0-328">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="93ab0-329">1 timme 30 minuter</span><span class="sxs-lookup"><span data-stu-id="93ab0-329">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="93ab0-330">2 dagar 6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="93ab0-330">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="93ab0-331">2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder</span><span class="sxs-lookup"><span data-stu-id="93ab0-331">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="93ab0-332">Du kan även ange en siffra som automatiskt konverteras till en varaktighet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-332">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="93ab0-333">Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.</span><span class="sxs-lookup"><span data-stu-id="93ab0-333">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="93ab0-334">Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.</span><span class="sxs-lookup"><span data-stu-id="93ab0-334">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="93ab0-335">Till exempel om mätenheten är timmar konverteras siffran `5` till 5 timmar.</span><span class="sxs-lookup"><span data-stu-id="93ab0-335">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="93ab0-336">Se även</span><span class="sxs-lookup"><span data-stu-id="93ab0-336">See Also</span></span>
<span data-ttu-id="93ab0-337">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="93ab0-337">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="93ab0-338">Datumberäkning för inköp</span><span class="sxs-lookup"><span data-stu-id="93ab0-338">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="93ab0-339">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="93ab0-339">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

