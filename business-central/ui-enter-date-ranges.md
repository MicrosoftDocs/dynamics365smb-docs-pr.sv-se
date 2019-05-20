---
title: Ange datum och tider i Business Central | Microsoft Docs
description: Lära dig att ange datum och tider, inklusive olika tips för produktivitet till exempel snabbskrift, uttryck och intervaller. Filtrera listor eller rapporter till specifika datum- och tidsperioder.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: c7e80edfd796056176d37ad12a56c76e64bb44e6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250946"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="4419c-104">Arbeta med kalenderdatum och tider</span><span class="sxs-lookup"><span data-stu-id="4419c-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="4419c-105">ger flera sätt för att ange datum och tider, inklusive kraftfulla funktioner som förbättrar datainmatning eller hjälper dig att skriva komplexa kalenderuttryck.</span><span class="sxs-lookup"><span data-stu-id="4419c-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="4419c-106">Det finns olika ställen i programmet där du kan ange datum och tider i ett fält.</span><span class="sxs-lookup"><span data-stu-id="4419c-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="4419c-107">På t.ex. en försäljningsorder kan du ange leveransdatumet.</span><span class="sxs-lookup"><span data-stu-id="4419c-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="4419c-108">När du filtrerar listor eller rapportdata, kan du ange datum och tider för att precisera endast den information som du är intresserad av.</span><span class="sxs-lookup"><span data-stu-id="4419c-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="4419c-109">Kontrollera inställningarna för region och språk</span><span class="sxs-lookup"><span data-stu-id="4419c-109">Check your region and language settings</span></span>

<span data-ttu-id="4419c-110">[**Mina inställningar**](https://businesscentral.dynamics.com?page=9176 "Gå direkt till sidan för användarinställningar i Business Central") anger **region** och **språk** som används i programmet.</span><span class="sxs-lookup"><span data-stu-id="4419c-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="4419c-111">Dessa inställningar påverkar hur du anger datum och tid.</span><span class="sxs-lookup"><span data-stu-id="4419c-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="4419c-112">Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras.</span><span class="sxs-lookup"><span data-stu-id="4419c-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="4419c-113">För datummönster som omfattar ord måste språket för de ord som du använder stämma överens med **språk**-inställningen.</span><span class="sxs-lookup"><span data-stu-id="4419c-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="4419c-114">använder det gregorianska kalendersystemet.</span><span class="sxs-lookup"><span data-stu-id="4419c-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="4419c-115">Ange datum</span><span class="sxs-lookup"><span data-stu-id="4419c-115">Entering Dates</span></span>

<span data-ttu-id="4419c-116">I ett datumfält kan du ange ett datum med standardformat för din region.</span><span class="sxs-lookup"><span data-stu-id="4419c-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="4419c-117">Olika områden kan använda olika avgränsare mellan dagar, månader och år.</span><span class="sxs-lookup"><span data-stu-id="4419c-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="4419c-118">Exempelvis vissa regioner använder bindestreck (åååå-mm-dd) och andra använda snedstreck (åååå/mm/dd).</span><span class="sxs-lookup"><span data-stu-id="4419c-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="4419c-119">Du kan använda alla avgränsare, även blanksteg och datumet ändras automatiskt till att använda avgränsare som matchar din region.</span><span class="sxs-lookup"><span data-stu-id="4419c-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="4419c-120">Observera att formatet som datum visas på utskrivna rapporter eller e-postade dokument påverkas inte av dina personliga inställningar av region.</span><span class="sxs-lookup"><span data-stu-id="4419c-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="4419c-121">Om du vill arbeta mer effektivt med datum och tider, använd någon av de metoder eller format som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4419c-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="4419c-122">Välja datum från kalendern</span><span class="sxs-lookup"><span data-stu-id="4419c-122">Picking dates from the calendar</span></span>

<span data-ttu-id="4419c-123">Ett fält som visar en kalenderikon kan anges med hjälp av kalenderdatumväljaren.</span><span class="sxs-lookup"><span data-stu-id="4419c-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="4419c-124">Om du vill visa kalenderdatumväljaren, aktivera kalenderikonen eller tryck på kortkommandot Ctrl + Home i fältet.</span><span class="sxs-lookup"><span data-stu-id="4419c-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="4419c-125">![Datumfält](media/ui-date-field.png "Exempel på ett datumfält")</span><span class="sxs-lookup"><span data-stu-id="4419c-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="4419c-126">Se även [Kortkommandon i kalenderdatumväljaren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="4419c-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="4419c-127">Dag\-vecka\-år-mönster</span><span class="sxs-lookup"><span data-stu-id="4419c-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="4419c-128">Du kan ange ett datum som en veckodag följt av ett veckonummer och alternativt ett år.</span><span class="sxs-lookup"><span data-stu-id="4419c-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="4419c-129">Till exempel `Mon25` eller `mon25` betyder måndag vecka 25.</span><span class="sxs-lookup"><span data-stu-id="4419c-129">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="4419c-130">Om du inte anger ett år används året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="4419c-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="4419c-131">I stället för att ange hela ordet för dagen i veckan, kan du skriva in del av ordet, från början.</span><span class="sxs-lookup"><span data-stu-id="4419c-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="4419c-132">Om det uppstår konflikter (exempelvis med `s` som kan vara Saturday (lördag) eller Sunday (söndag)), utvärderas dagarna utifrån regionsinställningen.</span><span class="sxs-lookup"><span data-stu-id="4419c-132">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="4419c-133">Indata utvärderas först mot `workdate`och `today`, så tänk på detta när du förkortar.</span><span class="sxs-lookup"><span data-stu-id="4419c-133">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="4419c-134">Till exempel `t` innebär today (idag), så det kan inte innebära: tisdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="4419c-134">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="4419c-135">Veckonummersystemet är alltid ISO-8601 där vecka 1 är veckan med 4 januari eller veckan med första torsdagen på året.</span><span class="sxs-lookup"><span data-stu-id="4419c-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="4419c-136">Siffermönster</span><span class="sxs-lookup"><span data-stu-id="4419c-136">Digit patterns</span></span>

<span data-ttu-id="4419c-137">I ett datumfält kan du skriva in två, fyra, sex eller åtta siffror.</span><span class="sxs-lookup"><span data-stu-id="4419c-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="4419c-138">Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="4419c-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="4419c-139">Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="4419c-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="4419c-140">Order för den dagen och månaden avgörs av dina regioninställningar.</span><span class="sxs-lookup"><span data-stu-id="4419c-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="4419c-141">Även om dina regioninställningar har året före dagen och månaden, tolkas fyra siffror som dag och månad.</span><span class="sxs-lookup"><span data-stu-id="4419c-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="4419c-142">Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.</span><span class="sxs-lookup"><span data-stu-id="4419c-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="4419c-143">I dag</span><span class="sxs-lookup"><span data-stu-id="4419c-143">Today</span></span>

<span data-ttu-id="4419c-144">Ange ordet for `today`, på det språk anges i **språk** inställningen som ska ange datumet till det aktuella datumet.</span><span class="sxs-lookup"><span data-stu-id="4419c-144">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="4419c-145">Istället för att ange hela ordet, kan du skriva in delar av ordet från början såsom `t` eller `tod`, förutsatt att det inte är också är början på ett annat ord.</span><span class="sxs-lookup"><span data-stu-id="4419c-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="4419c-146">Period</span><span class="sxs-lookup"><span data-stu-id="4419c-146">Period</span></span>

<span data-ttu-id="4419c-147">Om du vill filtrera efter en viss redovisningsperiod i ett datumfält skriver du in `p`, eller ordet `period`, följt av ett nummer som identifierar bokföringsperioden som `p2` eller `period4`.</span><span class="sxs-lookup"><span data-stu-id="4419c-147">To filter on a specific accounting period, in a date field enter the letter `p`, or the word `period`, followed by a number that identifies the accounting period, like `p2` or `period4`.</span></span> <span data-ttu-id="4419c-148">Bokföringsperioden är i förhållande till räkenskapsåret för det aktuella arbetsdatumet som angetts i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="4419c-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="4419c-149">Om arbetsdatumet är till exempel **03/21/20**, då är `p1`, eller bara `p` filter på den första perioden på räkenskapsåret 2020 (såsom `01/01/20..01/31/20`).</span><span class="sxs-lookup"><span data-stu-id="4419c-149">For example, if the work date is **03/21/20**, then `p1`, or just `p`, filters on the first accounting period of the fiscal year 2020 (such as `01/01/20..01/31/20`).</span></span> <span data-ttu-id="4419c-150">`p15` filter för femtonde bokföringsperioden från början av år 2020 (såsom `03/01/21..03/31/21`).</span><span class="sxs-lookup"><span data-stu-id="4419c-150">`p15` filters on the fifteenth accounting period from the start of fiscal year 2020 (such as `03/01/21..03/31/21`).</span></span> 

<span data-ttu-id="4419c-151">Bokföringsperioder definieras på sidan **Bokföringsperioder**.</span><span class="sxs-lookup"><span data-stu-id="4419c-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="4419c-152">Om du vill visa eller ändra bokföringsperioderna, öppna sidan [här ](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="4419c-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="4419c-153">Aktuellt arbetsdatum</span><span class="sxs-lookup"><span data-stu-id="4419c-153">Current work date</span></span>

<span data-ttu-id="4419c-154">Funktionen arbetsdatum låter dig spåra transaktioner med ett datum som skiljer sig från det aktuella datumet.</span><span class="sxs-lookup"><span data-stu-id="4419c-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="4419c-155">Ordet för ”arbetsdatum” på det språk som anges av **språk**-inställningen kan ange datumet till det aktuella arbetsdatumet som anges på sidan [**Mina inställningar**](https://businesscentral.dynamics.com?page=9176 "Gå direkt till sidan för användarinställningar i Business Central").</span><span class="sxs-lookup"><span data-stu-id="4419c-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="4419c-156">I stället för att ange hela ordet, kan du skriva in del av ordet, från början, såsom "a" eller "arbete".</span><span class="sxs-lookup"><span data-stu-id="4419c-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="4419c-157">Om du inte har definierat ett arbetsdatum, kommer det aktuella datumet användas som arbetsdatum.</span><span class="sxs-lookup"><span data-stu-id="4419c-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="4419c-158">Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.</span><span class="sxs-lookup"><span data-stu-id="4419c-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="4419c-159">Se även [Ändra grundläggande inställningar, såsom arbetsdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="4419c-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="4419c-160">Avslutsdatum</span><span class="sxs-lookup"><span data-stu-id="4419c-160">Closing Date</span></span>

<span data-ttu-id="4419c-161">När du avslutar ett räkenskapsår kan du använda avslutsdatum för att ange att en transaktion är en bokslutspost.</span><span class="sxs-lookup"><span data-stu-id="4419c-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="4419c-162">Ett avslutsdatum ligger tekniskt sätt mellan två datum, till exempel mellan den 31 december och den 1 januari.</span><span class="sxs-lookup"><span data-stu-id="4419c-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="4419c-163">För att ange att ett datum är ett stängningsdatum ange `C` före datumet såsom `C123101`.</span><span class="sxs-lookup"><span data-stu-id="4419c-163">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="4419c-164">Detta kan användas tillsammans med alla datummönster.</span><span class="sxs-lookup"><span data-stu-id="4419c-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="4419c-165">Exempel</span><span class="sxs-lookup"><span data-stu-id="4419c-165">Examples</span></span>

<span data-ttu-id="4419c-166">Följande tabell innehåller exempel på datum med alla format.</span><span class="sxs-lookup"><span data-stu-id="4419c-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="4419c-167">Det förutsätter regioninställningar som formaterar datum enligt: **år.månad.dag.**, en vecka med start på måndag och på engelska.</span><span class="sxs-lookup"><span data-stu-id="4419c-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="4419c-168">**Format**</span><span class="sxs-lookup"><span data-stu-id="4419c-168">**Entry**</span></span>      |<span data-ttu-id="4419c-169">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="4419c-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="4419c-170">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="4419c-170">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="4419c-171">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="4419c-171">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="4419c-172">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="4419c-172">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="4419c-173">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="4419c-173">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="4419c-174">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="4419c-174">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="4419c-175">2018-12-31.</span><span class="sxs-lookup"><span data-stu-id="4419c-175">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="4419c-176">arbetsdatum år.arbetsdatum månad.11.</span><span class="sxs-lookup"><span data-stu-id="4419c-176">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="4419c-177">arbetsdatum år.11.12.</span><span class="sxs-lookup"><span data-stu-id="4419c-177">work date year.11.12.</span></span>|
|<span data-ttu-id="4419c-178">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="4419c-178">`t` or `today`</span></span>|<span data-ttu-id="4419c-179">dagens datum</span><span class="sxs-lookup"><span data-stu-id="4419c-179">today's date</span></span>|
|`p4`|<span data-ttu-id="4419c-180">datumintervall som innehåller den fjärde bokföringsperioden, till exempel `04/01/20..04/30/20`</span><span class="sxs-lookup"><span data-stu-id="4419c-180">date range that includes the fourth accounting period, such as `04/01/20..04/30/20`</span></span>|
|<span data-ttu-id="4419c-181">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="4419c-181">`w` or `workdate`</span></span>|<span data-ttu-id="4419c-182">arbetsdatum</span><span class="sxs-lookup"><span data-stu-id="4419c-182">the working date</span></span>|
|<span data-ttu-id="4419c-183">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="4419c-183">`m` or `Monday`</span></span>|<span data-ttu-id="4419c-184">Måndag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="4419c-184">Monday of the work date week</span></span>|
|<span data-ttu-id="4419c-185">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="4419c-185">`tu` or `Tuesday`</span></span>|<span data-ttu-id="4419c-186">Tisdag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="4419c-186">Tuesday of the work date week</span></span>|
|<span data-ttu-id="4419c-187">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="4419c-187">`sa` or `Saturday`</span></span>|<span data-ttu-id="4419c-188">Lördag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="4419c-188">Saturday of the work date week</span></span>|
|<span data-ttu-id="4419c-189">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="4419c-189">`s` or `Sunday`</span></span>|<span data-ttu-id="4419c-190">Söndag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="4419c-190">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="4419c-191">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="4419c-191">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="4419c-192">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="4419c-192">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="4419c-193">Tisdag av vecka 1 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="4419c-193">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="4419c-194">Inställningsintervall</span><span class="sxs-lookup"><span data-stu-id="4419c-194">Setting Ranges</span></span>

<span data-ttu-id="4419c-195">I listor, summor och rapporter kan du ange filter för datum, tid och datum och tid som innehåller ett startvärde och ett slutvärde om du endast vill visa de data som finns inom intervallet.</span><span class="sxs-lookup"><span data-stu-id="4419c-195">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="4419c-196">Standardregler gäller för hur du kan ange datumintervall.</span><span class="sxs-lookup"><span data-stu-id="4419c-196">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="4419c-197">**Betydelse**</span><span class="sxs-lookup"><span data-stu-id="4419c-197">**Meaning**</span></span>|<span data-ttu-id="4419c-198">**Exempeluttryck (datum)**</span><span class="sxs-lookup"><span data-stu-id="4419c-198">**Sample expression (Date)**</span></span>|<span data-ttu-id="4419c-199">**Data som ingår i filtret**</span><span class="sxs-lookup"><span data-stu-id="4419c-199">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="4419c-200">Intervall</span><span class="sxs-lookup"><span data-stu-id="4419c-200">Interval</span></span>|`12 15 00..01 15 01`<br /><br />`..12 15 00`<br /><br />`p1..p4`|<span data-ttu-id="4419c-201">Poster med datum från och med 00-12-15 till och med 01-01-15.</span><span class="sxs-lookup"><span data-stu-id="4419c-201">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="4419c-202">Poster med datum 00-15-12 eller tidigare.</span><span class="sxs-lookup"><span data-stu-id="4419c-202">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="4419c-203">Datumintervall som innehåller den andra, tredje och fjärde bokföringsperioden, till exempel `01/01/20..04/30/20`.</span><span class="sxs-lookup"><span data-stu-id="4419c-203">Date range that includes the second, third, and fourth accounting periods, such as `01/01/20..04/30/20`.</span></span>|
|<span data-ttu-id="4419c-204">Antingen eller</span><span class="sxs-lookup"><span data-stu-id="4419c-204">Either/or</span></span>|`12 15 00|12 16 00`|<span data-ttu-id="4419c-205">Poster med antingen 00-12-15 eller 00-12-16.</span><span class="sxs-lookup"><span data-stu-id="4419c-205">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="4419c-206">Om det finns poster med datum båda dagarna kommer samtliga att visas.</span><span class="sxs-lookup"><span data-stu-id="4419c-206">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="4419c-207">Kombination</span><span class="sxs-lookup"><span data-stu-id="4419c-207">Combination</span></span>|<span data-ttu-id="4419c-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span><span class="sxs-lookup"><span data-stu-id="4419c-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span></span>|<span data-ttu-id="4419c-209">Poster med datum 00-12-15 eller mellan och inklusive den 00-12-01 och 00-12-10.</span><span class="sxs-lookup"><span data-stu-id="4419c-209">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="4419c-210">\nPoster med datum 00-12-14 eller tidigare, eller 00-12-30 eller senare. Detta innebär alla poster utom de med datum från och med 00-12-15 till och med 00-12-29.</span><span class="sxs-lookup"><span data-stu-id="4419c-210">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="4419c-211">Du kan använda giltiga format i filtret för datumintervall.</span><span class="sxs-lookup"><span data-stu-id="4419c-211">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="4419c-212">Till exempel `mon14 3..t 4p` som tillämpas på ett datum/tidsfält resulterar i ett filter mellan 03:00 måndag vecka 14 det aktuella arbetsdatumets år, inklusive fram till i dag klockan 16:00.</span><span class="sxs-lookup"><span data-stu-id="4419c-212">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="4419c-213">Använda datumformler</span><span class="sxs-lookup"><span data-stu-id="4419c-213">Using Date Formulas</span></span>
<span data-ttu-id="4419c-214">En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas.</span><span class="sxs-lookup"><span data-stu-id="4419c-214">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="4419c-215">Du kan ange datumformler i olika fält eller filter för datumberäkning.</span><span class="sxs-lookup"><span data-stu-id="4419c-215">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="4419c-216">I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar.</span><span class="sxs-lookup"><span data-stu-id="4419c-216">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="4419c-217">Om du till exempel anger `1W`, är perioden därefter faktiskt åtta dagar eftersom idag inkluderas.</span><span class="sxs-lookup"><span data-stu-id="4419c-217">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="4419c-218">För att ange en period av sju dagar \(en exakt vecka\) inklusive perioden för startdatum måste du ange `6D` eller `1W-1D`.</span><span class="sxs-lookup"><span data-stu-id="4419c-218">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="4419c-219">Här följer några exempel på hur datumformler kan användas:</span><span class="sxs-lookup"><span data-stu-id="4419c-219">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="4419c-220">Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="4419c-220">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="4419c-221">Datumformeln i fältet **Betalningsfrist** för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet \(eller från den föregående påminnelsen\) innan en påminnelse ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4419c-221">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="4419c-222">Datumformeln i fältet **Förfallodatumformel** bestämmer hur förfallodatumet på påminnelsen beräknas.</span><span class="sxs-lookup"><span data-stu-id="4419c-222">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="4419c-223">Datumformeln kan omfatta högst 20 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="4419c-223">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="4419c-224">Du kan använda följande bokstäver som förkortningar för kalenderenheter.</span><span class="sxs-lookup"><span data-stu-id="4419c-224">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="4419c-225">Bokstav</span><span class="sxs-lookup"><span data-stu-id="4419c-225">Letter</span></span>  |  <span data-ttu-id="4419c-226">Betydelse</span><span class="sxs-lookup"><span data-stu-id="4419c-226">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="4419c-227">Löpande (innevarande)</span><span class="sxs-lookup"><span data-stu-id="4419c-227">Current</span></span>|
|`D`|<span data-ttu-id="4419c-228">Dag\(ar\)</span><span class="sxs-lookup"><span data-stu-id="4419c-228">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="4419c-229">Vecka\(veckor\)</span><span class="sxs-lookup"><span data-stu-id="4419c-229">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="4419c-230">Månad\(er\)</span><span class="sxs-lookup"><span data-stu-id="4419c-230">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="4419c-231">Kvartal\(s\)</span><span class="sxs-lookup"><span data-stu-id="4419c-231">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="4419c-232">År\(\)</span><span class="sxs-lookup"><span data-stu-id="4419c-232">Year\(s\)</span></span>|

<span data-ttu-id="4419c-233">Du kan bygga upp en datumformel på tre sätt.</span><span class="sxs-lookup"><span data-stu-id="4419c-233">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="4419c-234">Följande exempel visar hur du använder `C`, för löpande, plus en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="4419c-234">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="4419c-235">Uttryck</span><span class="sxs-lookup"><span data-stu-id="4419c-235">Expression</span></span>  |  <span data-ttu-id="4419c-236">Betydelse</span><span class="sxs-lookup"><span data-stu-id="4419c-236">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="4419c-237">Löpande (innevarande) vecka</span><span class="sxs-lookup"><span data-stu-id="4419c-237">Current week</span></span>|
|`CM`|<span data-ttu-id="4419c-238">Löpande (innevarande) månad</span><span class="sxs-lookup"><span data-stu-id="4419c-238">Current month</span></span>|

<span data-ttu-id="4419c-239">Följande exempel visar hur du använder ett tal och en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="4419c-239">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="4419c-240">Ett nummer får inte vara högre än 9 999.</span><span class="sxs-lookup"><span data-stu-id="4419c-240">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="4419c-241">Uttryck</span><span class="sxs-lookup"><span data-stu-id="4419c-241">Expression</span></span>  |  <span data-ttu-id="4419c-242">Betydelse</span><span class="sxs-lookup"><span data-stu-id="4419c-242">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="4419c-243">Tio dagar från dagens datum.</span><span class="sxs-lookup"><span data-stu-id="4419c-243">10 days from today</span></span>|
|`2W`|<span data-ttu-id="4419c-244">Två veckor från dagens datum</span><span class="sxs-lookup"><span data-stu-id="4419c-244">2 weeks from today</span></span>|

<span data-ttu-id="4419c-245">Följande exempel visar hur du använder en tidsenhet och ett tal.</span><span class="sxs-lookup"><span data-stu-id="4419c-245">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="4419c-246">Uttryck</span><span class="sxs-lookup"><span data-stu-id="4419c-246">Expression</span></span>  |  <span data-ttu-id="4419c-247">Betydelse</span><span class="sxs-lookup"><span data-stu-id="4419c-247">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="4419c-248">Den tionde dagen varje månad.</span><span class="sxs-lookup"><span data-stu-id="4419c-248">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="4419c-249">Den nästa fjärde dagen i en vecka \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="4419c-249">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="4419c-250">Följande exempel visar hur du kombinera dessa tre metoder om så behövs.</span><span class="sxs-lookup"><span data-stu-id="4419c-250">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="4419c-251">Uttryck</span><span class="sxs-lookup"><span data-stu-id="4419c-251">Expression</span></span>  |  <span data-ttu-id="4419c-252">Betydelse</span><span class="sxs-lookup"><span data-stu-id="4419c-252">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="4419c-253">Löpande månad \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="4419c-253">Current month \+ 10 days</span></span>|

<span data-ttu-id="4419c-254">Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.</span><span class="sxs-lookup"><span data-stu-id="4419c-254">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="4419c-255">Uttryck</span><span class="sxs-lookup"><span data-stu-id="4419c-255">Expression</span></span>  |  <span data-ttu-id="4419c-256">Betydelse</span><span class="sxs-lookup"><span data-stu-id="4419c-256">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="4419c-257">1 år sedan från idag</span><span class="sxs-lookup"><span data-stu-id="4419c-257">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="4419c-258">Om lagerstället använder en baskalender, tolkas datumformeln som du anger i t.ex. fältet **Leveranstid** enligt kalenderarbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="4419c-258">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="4419c-259">Till exempel betyder `1W` sju arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="4419c-259">For example, `1W`  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="4419c-260">Ange tider</span><span class="sxs-lookup"><span data-stu-id="4419c-260">Entering Times</span></span>
<span data-ttu-id="4419c-261">När du anger tider kan du infoga alla icke-platsavgränsare som du vill mellan enheterna, men om du använder två siffror för varje enhet upp till millisekunder, är det inte obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="4419c-261">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="4419c-262">Du behöver bara skriva de största enheterna som du vill ha, övriga anges till noll.</span><span class="sxs-lookup"><span data-stu-id="4419c-262">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="4419c-263">Du kan också utelämna alla AM/PM-indikatorer.</span><span class="sxs-lookup"><span data-stu-id="4419c-263">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="4419c-264">I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.</span><span class="sxs-lookup"><span data-stu-id="4419c-264">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="4419c-265">Det följer regioninställningar som formaterar tid enligt: **Timmar:Minuter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="4419c-265">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="4419c-266">och använder du AM- och PM-indikatorer ”AM” och ”PM”.</span><span class="sxs-lookup"><span data-stu-id="4419c-266">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="4419c-267">**Format**</span><span class="sxs-lookup"><span data-stu-id="4419c-267">**Entry**</span></span>      |<span data-ttu-id="4419c-268">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="4419c-268">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="4419c-269">05:23:17</span><span class="sxs-lookup"><span data-stu-id="4419c-269">05:23:17</span></span>|
|`5`|<span data-ttu-id="4419c-270">05:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-270">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="4419c-271">05:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-271">05:00:00</span></span>|
|`5P`|<span data-ttu-id="4419c-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-272">17:00:00</span></span>|
|`12`|<span data-ttu-id="4419c-273">12:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-273">12:00:00</span></span>|
|`12A`|<span data-ttu-id="4419c-274">00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-274">00:00:00</span></span>|
|`12P`|<span data-ttu-id="4419c-275">12:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-275">12:00:00</span></span>|
|`17`|<span data-ttu-id="4419c-276">17:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-276">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="4419c-277">05:30:00</span><span class="sxs-lookup"><span data-stu-id="4419c-277">05:30:00</span></span>|
|`0530`|<span data-ttu-id="4419c-278">05:30:00</span><span class="sxs-lookup"><span data-stu-id="4419c-278">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="4419c-279">05:30:05</span><span class="sxs-lookup"><span data-stu-id="4419c-279">05:30:05</span></span>|
|`053005`|<span data-ttu-id="4419c-280">05:30:05</span><span class="sxs-lookup"><span data-stu-id="4419c-280">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="4419c-281">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="4419c-281">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="4419c-282">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="4419c-282">05:30:05.05</span></span>|

<span data-ttu-id="4419c-283">Du bör vara medveten om att millisekunder ska tolkas som decimala systemet.</span><span class="sxs-lookup"><span data-stu-id="4419c-283">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="4419c-284">Så till exempel `3`, `30` och `300` betyder alla 300 millisekunder, medan `03` betyder `30` och `003` innebär 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="4419c-284">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="4419c-285">Du kan inte använda `24:00` som midnatt eller välja ett värde som är större än 24:00.</span><span class="sxs-lookup"><span data-stu-id="4419c-285">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="4419c-286">Ordet för ”tid” på det språk som används av [!INCLUDE[d365fin](includes/d365fin_long_md.md)] utvärderas till aktuell tid på din dator eller mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="4419c-286">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="4419c-287">Du kan skriva in alla ord, från början, såsom `t` eller `TIM`.</span><span class="sxs-lookup"><span data-stu-id="4419c-287">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="4419c-288">Ange kombinerade datum och tider</span><span class="sxs-lookup"><span data-stu-id="4419c-288">Entering combined Dates and Times</span></span>
<span data-ttu-id="4419c-289">När du anger datum och tid som datum och tid som kombineras till ett enda fält, måste du ange ett blanksteg mellan datumet och tiden.</span><span class="sxs-lookup"><span data-stu-id="4419c-289">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="4419c-290">Datumdelen kan bara innehålla blanksteg i form av officiella datumavgränsare för din regionsinställning.</span><span class="sxs-lookup"><span data-stu-id="4419c-290">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="4419c-291">Tiden kan innehålla blanksteg runt AM/PM-indikatorn.</span><span class="sxs-lookup"><span data-stu-id="4419c-291">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="4419c-292">Det är också möjligt att endast ange ett datum i ett fält för datum och tid, men det går inte att ange endast en gång.</span><span class="sxs-lookup"><span data-stu-id="4419c-292">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="4419c-293">I följande tabell visas några exempel på kombinationer av datum/tid.</span><span class="sxs-lookup"><span data-stu-id="4419c-293">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="4419c-294">Regioninställningarna i exemplen visar datum i dags\-månads\-årsformat med AM/PM-beteckningar, engelska språket och söndag som veckans början.</span><span class="sxs-lookup"><span data-stu-id="4419c-294">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="4419c-295">**Format**</span><span class="sxs-lookup"><span data-stu-id="4419c-295">**Entry**</span></span>      |<span data-ttu-id="4419c-296">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="4419c-296">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="4419c-297">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="4419c-297">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="4419c-298">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="4419c-298">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="4419c-299">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-299">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="4419c-300">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-300">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="4419c-301">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-301">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="4419c-302">11\-arbetsdatum månad\-arbetsdatum år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-302">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="4419c-303">11\-12\-arbetsdatum år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-303">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="4419c-304">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="4419c-304">`t` or `today`</span></span>|<span data-ttu-id="4419c-305">dagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-305">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="4419c-306">dagens datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="4419c-306">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="4419c-307">dagens datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="4419c-307">today's date 03:03:03</span></span>|
|<span data-ttu-id="4419c-308">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="4419c-308">`w` or `workdate`</span></span>|<span data-ttu-id="4419c-309">arbetsdagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-309">the working date 00:00:00</span></span>|
|<span data-ttu-id="4419c-310">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="4419c-310">`m` or `Monday`</span></span>|<span data-ttu-id="4419c-311">Måndag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-311">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="4419c-312">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="4419c-312">`tu` or `Tuesday`</span></span>|<span data-ttu-id="4419c-313">Tisdag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-313">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="4419c-314">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="4419c-314">`sa` or `Saturday`</span></span>|<span data-ttu-id="4419c-315">Lördag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-315">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="4419c-316">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="4419c-316">`s` or `Sunday`</span></span>|<span data-ttu-id="4419c-317">Söndag av arbetsdatumets vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-317">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="4419c-318">Tisdag av arbetsdatumets vecka 10:30:00</span><span class="sxs-lookup"><span data-stu-id="4419c-318">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="4419c-319">Tisdag av arbetsdatumets vecka 03:03:03</span><span class="sxs-lookup"><span data-stu-id="4419c-319">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="4419c-320">Tisdag i en vecka 23 av arbetsdatumets år, aktuell tid på dagen</span><span class="sxs-lookup"><span data-stu-id="4419c-320">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="4419c-321">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="4419c-321">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="4419c-322">Idag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="4419c-322">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="4419c-323">Tisdag av vecka 1 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="4419c-323">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="4419c-324">Ange varaktighet</span><span class="sxs-lookup"><span data-stu-id="4419c-324">Entering Duration</span></span>
<span data-ttu-id="4419c-325">Vissa fält i programmet representerar en varaktighet eller mängden förfluten tid, i stället för ett visst datum eller tid.</span><span class="sxs-lookup"><span data-stu-id="4419c-325">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="4419c-326">Du anger varaktigheten som en siffra följd av en enhet.</span><span class="sxs-lookup"><span data-stu-id="4419c-326">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="4419c-327">Här följer några exempel.</span><span class="sxs-lookup"><span data-stu-id="4419c-327">Here are some examples.</span></span>

|<span data-ttu-id="4419c-328">**Varaktighet**</span><span class="sxs-lookup"><span data-stu-id="4419c-328">**Duration**</span></span>|<span data-ttu-id="4419c-329">**Enhet**</span><span class="sxs-lookup"><span data-stu-id="4419c-329">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="4419c-330">2 timmar</span><span class="sxs-lookup"><span data-stu-id="4419c-330">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="4419c-331">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="4419c-331">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="4419c-332">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="4419c-332">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="4419c-333">1 timme 30 minuter</span><span class="sxs-lookup"><span data-stu-id="4419c-333">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="4419c-334">2 dagar 6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="4419c-334">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="4419c-335">2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder</span><span class="sxs-lookup"><span data-stu-id="4419c-335">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="4419c-336">Du kan även ange en siffra som automatiskt konverteras till en varaktighet.</span><span class="sxs-lookup"><span data-stu-id="4419c-336">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="4419c-337">Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.</span><span class="sxs-lookup"><span data-stu-id="4419c-337">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="4419c-338">Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.</span><span class="sxs-lookup"><span data-stu-id="4419c-338">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="4419c-339">Till exempel om mätenheten är timmar konverteras siffran `5` till 5 timmar.</span><span class="sxs-lookup"><span data-stu-id="4419c-339">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="4419c-340">Se även</span><span class="sxs-lookup"><span data-stu-id="4419c-340">See Also</span></span>
<span data-ttu-id="4419c-341">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4419c-341">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4419c-342">Datumberäkning för inköp</span><span class="sxs-lookup"><span data-stu-id="4419c-342">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="4419c-343">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="4419c-343">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
