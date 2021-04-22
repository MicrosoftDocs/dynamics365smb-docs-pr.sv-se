---
title: Ange datum och tider i Business Central | Microsoft Docs
description: Lära dig att ange datum och tider, inklusive olika tips för produktivitet till exempel snabbskrift, uttryck och intervaller. Filtrera listor eller rapporter till specifika datum- och tidsperioder.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 404c39cba663cebc4d9ab30126de97bd20cf7e8e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773536"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="17d99-104">Arbeta med kalenderdatum och tider</span><span class="sxs-lookup"><span data-stu-id="17d99-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="17d99-105">ger flera sätt för att ange datum och tider, inklusive kraftfulla funktioner som förbättrar datainmatning eller hjälper dig att skriva komplexa kalenderuttryck.</span><span class="sxs-lookup"><span data-stu-id="17d99-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="17d99-106">Det finns olika ställen i programmet där du kan ange datum och tider i ett fält.</span><span class="sxs-lookup"><span data-stu-id="17d99-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="17d99-107">På t. ex. en försäljningsorder kan du ange leveransdatumet.</span><span class="sxs-lookup"><span data-stu-id="17d99-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="17d99-108">När du filtrerar listor eller rapportdata, kan du ange datum och tider för att precisera endast den information som du är intresserad av.</span><span class="sxs-lookup"><span data-stu-id="17d99-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="17d99-109">Kontrollera inställningarna för region och språk</span><span class="sxs-lookup"><span data-stu-id="17d99-109">Check your region and language settings</span></span>
<span data-ttu-id="17d99-110">Sidan **Mina inställningar** anger **Region** och **Språk** du använder i programmet.</span><span class="sxs-lookup"><span data-stu-id="17d99-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="17d99-111">Dessa inställningar påverkar hur du anger datum och tid.</span><span class="sxs-lookup"><span data-stu-id="17d99-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="17d99-112">Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras.</span><span class="sxs-lookup"><span data-stu-id="17d99-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="17d99-113">För datummönster som omfattar ord måste språket för de ord som du använder stämma överens med **språk**-inställningen.</span><span class="sxs-lookup"><span data-stu-id="17d99-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="17d99-114">använder det gregorianska kalendersystemet.</span><span class="sxs-lookup"><span data-stu-id="17d99-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="17d99-115">Ange datum</span><span class="sxs-lookup"><span data-stu-id="17d99-115">Entering Dates</span></span>

<span data-ttu-id="17d99-116">I ett datumfält kan du ange ett datum med standardformat för din region.</span><span class="sxs-lookup"><span data-stu-id="17d99-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="17d99-117">Olika områden kan använda olika avgränsare mellan dagar, månader och år.</span><span class="sxs-lookup"><span data-stu-id="17d99-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="17d99-118">Exempelvis använder vissa regioner bindestreck (åååå-mm-dd) och andra snedstreck (åååå/mm/dd).</span><span class="sxs-lookup"><span data-stu-id="17d99-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="17d99-119">Du kan använda alla avgränsare, även blanksteg och datumet ändras automatiskt till att använda avgränsare som matchar din region.</span><span class="sxs-lookup"><span data-stu-id="17d99-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="17d99-120">Observera att formatet som datum visas på utskrivna rapporter eller e-postade dokument påverkas inte av dina personliga inställningar av region.</span><span class="sxs-lookup"><span data-stu-id="17d99-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="17d99-121">Om du vill arbeta mer effektivt med datum och tider, använd någon av de metoder eller format som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="17d99-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="17d99-122">Välja datum från kalendern</span><span class="sxs-lookup"><span data-stu-id="17d99-122">Picking dates from the calendar</span></span>

<span data-ttu-id="17d99-123">Ett fält som visar en kalenderikon kan anges med hjälp av kalenderdatumväljaren.</span><span class="sxs-lookup"><span data-stu-id="17d99-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="17d99-124">Om du vill visa kalenderdatumväljaren, aktivera kalenderikonen eller tryck på kortkommandot Ctrl + Home i fältet.</span><span class="sxs-lookup"><span data-stu-id="17d99-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="17d99-125">![Datumfält](media/ui-date-field.png "Exempel på datumfält")</span><span class="sxs-lookup"><span data-stu-id="17d99-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="17d99-126">Se även [Kortkommandon i kalenderdatumväljaren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="17d99-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="17d99-127">Dag\-vecka\-år-mönster</span><span class="sxs-lookup"><span data-stu-id="17d99-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="17d99-128">Du kan ange ett datum som en veckodag följt av ett veckonummer och alternativt ett år.</span><span class="sxs-lookup"><span data-stu-id="17d99-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="17d99-129">Till exempel Mån25 eller mån25 betyder måndag vecka 25.</span><span class="sxs-lookup"><span data-stu-id="17d99-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="17d99-130">Om du inte anger ett år används året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="17d99-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="17d99-131">I stället för att ange hela ordet för dagen i veckan, kan du skriva in del av ordet, från början.</span><span class="sxs-lookup"><span data-stu-id="17d99-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="17d99-132">Om det uppstår konflikter (exempelvis med t som kan vara tisdag eller torsdag) utvärderas dagarna utifrån regionsinställningen.</span><span class="sxs-lookup"><span data-stu-id="17d99-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="17d99-133">Indata utvärderas först mot arbetsdagen och idag, så tänk på detta när du förkortar.</span><span class="sxs-lookup"><span data-stu-id="17d99-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="17d99-134">Till exempel t innebär today (idag), så det kan inte innebära: tisdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="17d99-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="17d99-135">Veckonummersystemet är alltid ISO-8601 där vecka 1 är veckan med 4 januari eller veckan med första torsdagen på året.</span><span class="sxs-lookup"><span data-stu-id="17d99-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="17d99-136">Siffermönster</span><span class="sxs-lookup"><span data-stu-id="17d99-136">Digit patterns</span></span>

<span data-ttu-id="17d99-137">I ett datumfält kan du skriva in två, fyra, sex eller åtta siffror.</span><span class="sxs-lookup"><span data-stu-id="17d99-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="17d99-138">Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="17d99-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="17d99-139">Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="17d99-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="17d99-140">Order för den dagen och månaden avgörs av dina regioninställningar.</span><span class="sxs-lookup"><span data-stu-id="17d99-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="17d99-141">Även om dina regioninställningar har året före dagen och månaden, tolkas fyra siffror som dag och månad.</span><span class="sxs-lookup"><span data-stu-id="17d99-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="17d99-142">Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.</span><span class="sxs-lookup"><span data-stu-id="17d99-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="17d99-143">I dag</span><span class="sxs-lookup"><span data-stu-id="17d99-143">Today</span></span>

<span data-ttu-id="17d99-144">Ange ordet for idag på det språk som anges i inställningen **språk** som ska ange datumet till det aktuella datumet.</span><span class="sxs-lookup"><span data-stu-id="17d99-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="17d99-145">Istället för att ange hela ordet, kan du skriva in delar av ordet från början såsom i eller ida, förutsatt att det inte är också är början på ett annat ord.</span><span class="sxs-lookup"><span data-stu-id="17d99-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="17d99-146">Period</span><span class="sxs-lookup"><span data-stu-id="17d99-146">Period</span></span>

<span data-ttu-id="17d99-147">Om du vill filtrera efter en viss redovisningsperiod i ett datumfält skriver du in p eller ordet period, följt av ett nummer som identifierar bokföringsperioden som p2 eller period4.</span><span class="sxs-lookup"><span data-stu-id="17d99-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="17d99-148">Bokföringsperioden är i förhållande till räkenskapsåret för det aktuella arbetsdatumet som angetts i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="17d99-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="17d99-149">Om arbetsdatumet är till exempel **22-03-21**, då är p1, eller bara p filter på den första perioden på räkenskapsåret 2022 (såsom 22-01-01..20-01-31).</span><span class="sxs-lookup"><span data-stu-id="17d99-149">For example, if the work date is **03/21/22**, then p1, or just p, filters on the first accounting period of the fiscal year 2022 (such as 01/01/22..01/31/22).</span></span> <span data-ttu-id="17d99-150">p15 filter för femtonde bokföringsperioden från början av år 2022 (såsom 23-03-01..21-03-31).</span><span class="sxs-lookup"><span data-stu-id="17d99-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2022 (such as 03/01/23..03/31/23).</span></span>

<span data-ttu-id="17d99-151">Bokföringsperioder definieras på sidan **Bokföringsperioder**.</span><span class="sxs-lookup"><span data-stu-id="17d99-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="17d99-152">Om du vill visa eller ändra bokföringsperioderna, öppna sidan [här](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="17d99-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="17d99-153">Aktuellt arbetsdatum</span><span class="sxs-lookup"><span data-stu-id="17d99-153">Current work date</span></span>

<span data-ttu-id="17d99-154">Funktionen arbetsdatum låter dig spåra transaktioner med ett datum som skiljer sig från det aktuella datumet.</span><span class="sxs-lookup"><span data-stu-id="17d99-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="17d99-155">Ordet för ”arbetsdatum” på det språk som anges av **språk**-inställningen kan ange datumet till det aktuella arbetsdatumet som anges på sidan **Mina inställningar**.</span><span class="sxs-lookup"><span data-stu-id="17d99-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="17d99-156">I stället för att ange hela ordet, kan du skriva in del av ordet, från början, såsom "a" eller "arbete".</span><span class="sxs-lookup"><span data-stu-id="17d99-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="17d99-157">Om du inte har definierat ett arbetsdatum, kommer det aktuella datumet användas som arbetsdatum.</span><span class="sxs-lookup"><span data-stu-id="17d99-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="17d99-158">Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.</span><span class="sxs-lookup"><span data-stu-id="17d99-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="17d99-159">Se även [Ändra grundläggande inställningar, såsom arbetsdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="17d99-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="17d99-160">Avslutsdatum</span><span class="sxs-lookup"><span data-stu-id="17d99-160">Closing Date</span></span>

<span data-ttu-id="17d99-161">När du avslutar ett räkenskapsår kan du använda avslutsdatum för att ange att en transaktion är en bokslutspost.</span><span class="sxs-lookup"><span data-stu-id="17d99-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="17d99-162">Ett avslutsdatum ligger tekniskt sätt mellan två datum, till exempel mellan den 31 december och den 1 januari.</span><span class="sxs-lookup"><span data-stu-id="17d99-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="17d99-163">För att ange att ett datum är ett avslutsdatum ange A före datumet såsom A120131.</span><span class="sxs-lookup"><span data-stu-id="17d99-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="17d99-164">Detta kan användas tillsammans med alla datummönster.</span><span class="sxs-lookup"><span data-stu-id="17d99-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="17d99-165">Exempel</span><span class="sxs-lookup"><span data-stu-id="17d99-165">Examples</span></span>

<span data-ttu-id="17d99-166">Följande tabell innehåller exempel på datum med alla format.</span><span class="sxs-lookup"><span data-stu-id="17d99-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="17d99-167">Det förutsätter regioninställningar som formaterar datum enligt: **år.månad.dag.**, en vecka med start på måndag och på engelska.</span><span class="sxs-lookup"><span data-stu-id="17d99-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="17d99-168">**Format**</span><span class="sxs-lookup"><span data-stu-id="17d99-168">**Entry**</span></span>      |<span data-ttu-id="17d99-169">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="17d99-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="17d99-170">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-170">2022.12.31.</span></span>|<span data-ttu-id="17d99-171">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-171">2022.12.31.</span></span>|
|<span data-ttu-id="17d99-172">221231</span><span class="sxs-lookup"><span data-stu-id="17d99-172">221231</span></span>|<span data-ttu-id="17d99-173">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-173">2022.12.31.</span></span>|
|<span data-ttu-id="17d99-174">22.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-174">22.12.31.</span></span>|<span data-ttu-id="17d99-175">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-175">2022.12.31.</span></span>|
|<span data-ttu-id="17d99-176">22.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-176">22.12.31.</span></span>|<span data-ttu-id="17d99-177">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-177">2022.12.31.</span></span>|
|<span data-ttu-id="17d99-178">20221231</span><span class="sxs-lookup"><span data-stu-id="17d99-178">20221231</span></span>|<span data-ttu-id="17d99-179">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-179">2022.12.31.</span></span>|
|<span data-ttu-id="17d99-180">22/12,31</span><span class="sxs-lookup"><span data-stu-id="17d99-180">22/12,31</span></span>|<span data-ttu-id="17d99-181">2022.12.31.</span><span class="sxs-lookup"><span data-stu-id="17d99-181">2022.12.31.</span></span>|
|<span data-ttu-id="17d99-182">11</span><span class="sxs-lookup"><span data-stu-id="17d99-182">11</span></span>|<span data-ttu-id="17d99-183">arbetsdatum år-arbetsdatum månad-11.</span><span class="sxs-lookup"><span data-stu-id="17d99-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="17d99-184">1112</span><span class="sxs-lookup"><span data-stu-id="17d99-184">1112</span></span>|<span data-ttu-id="17d99-185">arbetsdatum år-11-12.</span><span class="sxs-lookup"><span data-stu-id="17d99-185">work date year.11.12.</span></span>|
|<span data-ttu-id="17d99-186">d eller dagens datum</span><span class="sxs-lookup"><span data-stu-id="17d99-186">t or today</span></span>|<span data-ttu-id="17d99-187">dagens datum</span><span class="sxs-lookup"><span data-stu-id="17d99-187">today's date</span></span>|
|<span data-ttu-id="17d99-188">p4</span><span class="sxs-lookup"><span data-stu-id="17d99-188">p4</span></span>|<span data-ttu-id="17d99-189">datumintervall som innehåller den fjärde bokföringsperioden, till exempel 20-04-01...21-04-30</span><span class="sxs-lookup"><span data-stu-id="17d99-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="17d99-190">a eller arbetsdagens datum</span><span class="sxs-lookup"><span data-stu-id="17d99-190">w or workdate</span></span>|<span data-ttu-id="17d99-191">arbetsdatum</span><span class="sxs-lookup"><span data-stu-id="17d99-191">the working date</span></span>|
|<span data-ttu-id="17d99-192">m eller måndag</span><span class="sxs-lookup"><span data-stu-id="17d99-192">m or Monday</span></span>|<span data-ttu-id="17d99-193">Måndag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="17d99-193">Monday of the work date week</span></span>|
|<span data-ttu-id="17d99-194">ti eller tisdag</span><span class="sxs-lookup"><span data-stu-id="17d99-194">tu or Tuesday</span></span>|<span data-ttu-id="17d99-195">Tisdag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="17d99-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="17d99-196">lö eller lördag</span><span class="sxs-lookup"><span data-stu-id="17d99-196">sa or Saturday</span></span>|<span data-ttu-id="17d99-197">Lördag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="17d99-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="17d99-198">s eller söndag</span><span class="sxs-lookup"><span data-stu-id="17d99-198">s or Sunday</span></span>|<span data-ttu-id="17d99-199">Söndag av arbetsdatumets vecka</span><span class="sxs-lookup"><span data-stu-id="17d99-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="17d99-200">t23</span><span class="sxs-lookup"><span data-stu-id="17d99-200">t23</span></span>|<span data-ttu-id="17d99-201">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="17d99-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="17d99-202">t 23</span><span class="sxs-lookup"><span data-stu-id="17d99-202">t 23</span></span>|<span data-ttu-id="17d99-203">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="17d99-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="17d99-204">t-1</span><span class="sxs-lookup"><span data-stu-id="17d99-204">t-1</span></span>|<span data-ttu-id="17d99-205">Tisdag av vecka 1 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="17d99-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="17d99-206">Inställningsintervall</span><span class="sxs-lookup"><span data-stu-id="17d99-206">Setting Ranges</span></span>

<span data-ttu-id="17d99-207">I listor, summor och rapporter kan du ange filter för datum, tid och datum och tid som innehåller ett startvärde och ett slutvärde om du endast vill visa de data som finns inom intervallet.</span><span class="sxs-lookup"><span data-stu-id="17d99-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="17d99-208">Standardregler gäller för hur du kan ange datumintervall.</span><span class="sxs-lookup"><span data-stu-id="17d99-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="17d99-209">**Betydelse**</span><span class="sxs-lookup"><span data-stu-id="17d99-209">**Meaning**</span></span>|<span data-ttu-id="17d99-210">**Exempeluttryck (datum)**</span><span class="sxs-lookup"><span data-stu-id="17d99-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="17d99-211">**Data som ingår i filtret**</span><span class="sxs-lookup"><span data-stu-id="17d99-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="17d99-212">Intervall</span><span class="sxs-lookup"><span data-stu-id="17d99-212">Interval</span></span>|<span data-ttu-id="17d99-213">00-12-15..01-01-15</span><span class="sxs-lookup"><span data-stu-id="17d99-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="17d99-214">..00-12-15</span><span class="sxs-lookup"><span data-stu-id="17d99-214">..12 15 00</span></span><br /><br /><span data-ttu-id="17d99-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="17d99-215">p1..p4</span></span>|<span data-ttu-id="17d99-216">Poster med datum från och med 00-12-15 till och med 01-01-15.</span><span class="sxs-lookup"><span data-stu-id="17d99-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="17d99-217">Poster med datum 00-15-12 eller tidigare.</span><span class="sxs-lookup"><span data-stu-id="17d99-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="17d99-218">Datumintervall som innehåller den andra, tredje och fjärde bokföringsperioden, till exempel 20-01-01..20-04-30.</span><span class="sxs-lookup"><span data-stu-id="17d99-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="17d99-219">Antingen eller</span><span class="sxs-lookup"><span data-stu-id="17d99-219">Either/or</span></span>|<span data-ttu-id="17d99-220">00-12-15\|00-12-16</span><span class="sxs-lookup"><span data-stu-id="17d99-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="17d99-221">Poster med antingen 00-12-15 eller 00-12-16.</span><span class="sxs-lookup"><span data-stu-id="17d99-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="17d99-222">Om det finns poster med datum båda dagarna kommer samtliga att visas.</span><span class="sxs-lookup"><span data-stu-id="17d99-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="17d99-223">Kombination</span><span class="sxs-lookup"><span data-stu-id="17d99-223">Combination</span></span>|<span data-ttu-id="17d99-224">00-12-15\|00-12-01..00-12-10</span><span class="sxs-lookup"><span data-stu-id="17d99-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="17d99-225">..00-12-14\|00-12-30..</span><span class="sxs-lookup"><span data-stu-id="17d99-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="17d99-226">Poster med datum 00-12-15 eller mellan och inklusive den 00-12-01 och 00-12-10.</span><span class="sxs-lookup"><span data-stu-id="17d99-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="17d99-227">Poster med datum 00-12-14 eller tidigare, eller 00-12-30 eller senare. Detta innebär alla poster utom de med datum från och med 00-12-15 till och med 00-12-29.</span><span class="sxs-lookup"><span data-stu-id="17d99-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="17d99-228">Du kan använda giltiga format i filtret för datumintervall.</span><span class="sxs-lookup"><span data-stu-id="17d99-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="17d99-229">Till exempel mån14 3..t 4p som tillämpas på ett datum/tidsfält resulterar i ett filter mellan 03:00 måndag vecka 14 det aktuella arbetsdatumets år, inklusive fram till i dag klockan 16:00.</span><span class="sxs-lookup"><span data-stu-id="17d99-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="17d99-230">Använda datumformler</span><span class="sxs-lookup"><span data-stu-id="17d99-230">Using Date Formulas</span></span>
<span data-ttu-id="17d99-231">En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas.</span><span class="sxs-lookup"><span data-stu-id="17d99-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="17d99-232">Du kan ange datumformler i olika fält eller filter för datumberäkning.</span><span class="sxs-lookup"><span data-stu-id="17d99-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="17d99-233">I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar.</span><span class="sxs-lookup"><span data-stu-id="17d99-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="17d99-234">Om du till exempel anger 1V, är perioden därefter faktiskt åtta dagar eftersom idag inkluderas.</span><span class="sxs-lookup"><span data-stu-id="17d99-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="17d99-235">För att ange en period av sju dagar \(en exakt vecka\) inklusive perioden för startdatum måste du ange 6 dagar eller 1 vecka minus 1 dag.</span><span class="sxs-lookup"><span data-stu-id="17d99-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="17d99-236">Här följer några exempel på hur datumformler kan användas:</span><span class="sxs-lookup"><span data-stu-id="17d99-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="17d99-237">Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="17d99-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="17d99-238">Datumformeln i fältet **Betalningsfrist** för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet \(eller från den föregående påminnelsen\) innan en påminnelse ska skapas.</span><span class="sxs-lookup"><span data-stu-id="17d99-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="17d99-239">Datumformeln i fältet **Förfallodatumformel** bestämmer hur förfallodatumet på påminnelsen beräknas.</span><span class="sxs-lookup"><span data-stu-id="17d99-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="17d99-240">Datumformeln kan omfatta högst 20 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="17d99-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="17d99-241">Du kan använda följande bokstäver som förkortningar för kalenderenheter.</span><span class="sxs-lookup"><span data-stu-id="17d99-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="17d99-242">Bokstav</span><span class="sxs-lookup"><span data-stu-id="17d99-242">Letter</span></span>  |  <span data-ttu-id="17d99-243">Betydelse</span><span class="sxs-lookup"><span data-stu-id="17d99-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="17d99-244">A</span><span class="sxs-lookup"><span data-stu-id="17d99-244">C</span></span>|<span data-ttu-id="17d99-245">Aktuell</span><span class="sxs-lookup"><span data-stu-id="17d99-245">Current</span></span>|
|<span data-ttu-id="17d99-246">D</span><span class="sxs-lookup"><span data-stu-id="17d99-246">D</span></span>|<span data-ttu-id="17d99-247">Dag\(ar\)</span><span class="sxs-lookup"><span data-stu-id="17d99-247">Day\(s\)</span></span>|
|<span data-ttu-id="17d99-248">V</span><span class="sxs-lookup"><span data-stu-id="17d99-248">W</span></span>|<span data-ttu-id="17d99-249">Vecka\(veckor\)</span><span class="sxs-lookup"><span data-stu-id="17d99-249">Week\(s\)</span></span>|
|<span data-ttu-id="17d99-250">M</span><span class="sxs-lookup"><span data-stu-id="17d99-250">M</span></span>|<span data-ttu-id="17d99-251">Månad\(er\)</span><span class="sxs-lookup"><span data-stu-id="17d99-251">Month\(s\)</span></span>|
|<span data-ttu-id="17d99-252">K</span><span class="sxs-lookup"><span data-stu-id="17d99-252">Q</span></span>|<span data-ttu-id="17d99-253">Kvartal\(s\)</span><span class="sxs-lookup"><span data-stu-id="17d99-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="17d99-254">Å</span><span class="sxs-lookup"><span data-stu-id="17d99-254">Y</span></span>|<span data-ttu-id="17d99-255">År\(\)</span><span class="sxs-lookup"><span data-stu-id="17d99-255">Year\(s\)</span></span>|

<span data-ttu-id="17d99-256">Du kan bygga upp en datumformel på tre sätt.</span><span class="sxs-lookup"><span data-stu-id="17d99-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="17d99-257">Följande exempel visar hur du använder A för aktuell, plus en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="17d99-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="17d99-258">Uttryck</span><span class="sxs-lookup"><span data-stu-id="17d99-258">Expression</span></span>  |  <span data-ttu-id="17d99-259">Betydelse</span><span class="sxs-lookup"><span data-stu-id="17d99-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="17d99-260">AV</span><span class="sxs-lookup"><span data-stu-id="17d99-260">CW</span></span>|<span data-ttu-id="17d99-261">Aktuell vecka</span><span class="sxs-lookup"><span data-stu-id="17d99-261">Current week</span></span>|
|<span data-ttu-id="17d99-262">AM</span><span class="sxs-lookup"><span data-stu-id="17d99-262">CM</span></span>|<span data-ttu-id="17d99-263">Aktuell månad</span><span class="sxs-lookup"><span data-stu-id="17d99-263">Current month</span></span>|

<span data-ttu-id="17d99-264">Följande exempel visar hur du använder ett tal och en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="17d99-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="17d99-265">Ett nummer får inte vara högre än 9 999.</span><span class="sxs-lookup"><span data-stu-id="17d99-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="17d99-266">Uttryck</span><span class="sxs-lookup"><span data-stu-id="17d99-266">Expression</span></span>  |  <span data-ttu-id="17d99-267">Betydelse</span><span class="sxs-lookup"><span data-stu-id="17d99-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="17d99-268">10D</span><span class="sxs-lookup"><span data-stu-id="17d99-268">10D</span></span>|<span data-ttu-id="17d99-269">Tio dagar från dagens datum.</span><span class="sxs-lookup"><span data-stu-id="17d99-269">10 days from today</span></span>|
|<span data-ttu-id="17d99-270">2V</span><span class="sxs-lookup"><span data-stu-id="17d99-270">2W</span></span>|<span data-ttu-id="17d99-271">Två veckor från dagens datum</span><span class="sxs-lookup"><span data-stu-id="17d99-271">2 weeks from today</span></span>|

<span data-ttu-id="17d99-272">Följande exempel visar hur du använder en tidsenhet och ett tal.</span><span class="sxs-lookup"><span data-stu-id="17d99-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="17d99-273">Uttryck</span><span class="sxs-lookup"><span data-stu-id="17d99-273">Expression</span></span>  |  <span data-ttu-id="17d99-274">Betydelse</span><span class="sxs-lookup"><span data-stu-id="17d99-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="17d99-275">D10</span><span class="sxs-lookup"><span data-stu-id="17d99-275">D10</span></span>|<span data-ttu-id="17d99-276">Den tionde dagen varje månad.</span><span class="sxs-lookup"><span data-stu-id="17d99-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="17d99-277">VD4</span><span class="sxs-lookup"><span data-stu-id="17d99-277">WD4</span></span>|<span data-ttu-id="17d99-278">Den nästa fjärde dagen i en vecka \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="17d99-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="17d99-279">Följande exempel visar hur du kombinera dessa tre metoder om så behövs.</span><span class="sxs-lookup"><span data-stu-id="17d99-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="17d99-280">Uttryck</span><span class="sxs-lookup"><span data-stu-id="17d99-280">Expression</span></span>  |  <span data-ttu-id="17d99-281">Betydelse</span><span class="sxs-lookup"><span data-stu-id="17d99-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="17d99-282">AM+10D</span><span class="sxs-lookup"><span data-stu-id="17d99-282">CM+10D</span></span>|<span data-ttu-id="17d99-283">Aktuell månad \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="17d99-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="17d99-284">Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.</span><span class="sxs-lookup"><span data-stu-id="17d99-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="17d99-285">Uttryck</span><span class="sxs-lookup"><span data-stu-id="17d99-285">Expression</span></span>  |  <span data-ttu-id="17d99-286">Betydelse</span><span class="sxs-lookup"><span data-stu-id="17d99-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="17d99-287">-1Å</span><span class="sxs-lookup"><span data-stu-id="17d99-287">-1Y</span></span>|<span data-ttu-id="17d99-288">1 år sedan från idag</span><span class="sxs-lookup"><span data-stu-id="17d99-288">1 year ago from today</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="17d99-289">Om lagerstället använder en baskalender, tolkas datumformeln som du anger i t. ex. fältet **Leveranstid** enligt kalenderarbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="17d99-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="17d99-290">Till exempel betyder 1V sju arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="17d99-290">For example, 1W  means seven working days.</span></span>
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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

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

## <a name="entering-times"></a><span data-ttu-id="17d99-291">Ange tider</span><span class="sxs-lookup"><span data-stu-id="17d99-291">Entering Times</span></span>
<span data-ttu-id="17d99-292">När du anger tider kan du infoga alla icke-platsavgränsare som du vill mellan enheterna, men om du använder två siffror för varje enhet upp till millisekunder, är det valfritt.</span><span class="sxs-lookup"><span data-stu-id="17d99-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="17d99-293">Du behöver bara skriva de största enheterna som du vill ha, övriga anges till noll.</span><span class="sxs-lookup"><span data-stu-id="17d99-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="17d99-294">Du kan också utelämna alla AM/PM-indikatorer.</span><span class="sxs-lookup"><span data-stu-id="17d99-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="17d99-295">I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.</span><span class="sxs-lookup"><span data-stu-id="17d99-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="17d99-296">Det följer regioninställningar som formaterar tid enligt: **Timmar:Minuter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="17d99-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="17d99-297">och använder du AM- och PM-indikatorer ”AM” och ”PM”.</span><span class="sxs-lookup"><span data-stu-id="17d99-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="17d99-298">**Format**</span><span class="sxs-lookup"><span data-stu-id="17d99-298">**Entry**</span></span>      |<span data-ttu-id="17d99-299">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="17d99-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="17d99-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="17d99-300">05:23:17</span></span>|<span data-ttu-id="17d99-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="17d99-301">05:23:17</span></span>|
|<span data-ttu-id="17d99-302">5</span><span class="sxs-lookup"><span data-stu-id="17d99-302">5</span></span>|<span data-ttu-id="17d99-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-303">05:00:00</span></span>|
|<span data-ttu-id="17d99-304">5AM</span><span class="sxs-lookup"><span data-stu-id="17d99-304">5AM</span></span>|<span data-ttu-id="17d99-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-305">05:00:00</span></span>|
|<span data-ttu-id="17d99-306">5P</span><span class="sxs-lookup"><span data-stu-id="17d99-306">5P</span></span>|<span data-ttu-id="17d99-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-307">17:00:00</span></span>|
|<span data-ttu-id="17d99-308">12</span><span class="sxs-lookup"><span data-stu-id="17d99-308">12</span></span>|<span data-ttu-id="17d99-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-309">12:00:00</span></span>|
|<span data-ttu-id="17d99-310">12A</span><span class="sxs-lookup"><span data-stu-id="17d99-310">12A</span></span>|<span data-ttu-id="17d99-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-311">00:00:00</span></span>|
|<span data-ttu-id="17d99-312">12P</span><span class="sxs-lookup"><span data-stu-id="17d99-312">12P</span></span>|<span data-ttu-id="17d99-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-313">12:00:00</span></span>|
|<span data-ttu-id="17d99-314">17</span><span class="sxs-lookup"><span data-stu-id="17d99-314">17</span></span>|<span data-ttu-id="17d99-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="17d99-315">17:00:00</span></span>|
|<span data-ttu-id="17d99-316">5:30</span><span class="sxs-lookup"><span data-stu-id="17d99-316">5:30</span></span>|<span data-ttu-id="17d99-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="17d99-317">05:30:00</span></span>|
|<span data-ttu-id="17d99-318">0530</span><span class="sxs-lookup"><span data-stu-id="17d99-318">0530</span></span>|<span data-ttu-id="17d99-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="17d99-319">05:30:00</span></span>|
|<span data-ttu-id="17d99-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="17d99-320">5:30:5</span></span>|<span data-ttu-id="17d99-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="17d99-321">05:30:05</span></span>|
|<span data-ttu-id="17d99-322">053005</span><span class="sxs-lookup"><span data-stu-id="17d99-322">053005</span></span>|<span data-ttu-id="17d99-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="17d99-323">05:30:05</span></span>|
|<span data-ttu-id="17d99-324">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="17d99-324">5:30:5,50</span></span>|<span data-ttu-id="17d99-325">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="17d99-325">05:30:05.5</span></span>|
|<span data-ttu-id="17d99-326">053005050</span><span class="sxs-lookup"><span data-stu-id="17d99-326">053005050</span></span>|<span data-ttu-id="17d99-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="17d99-327">05:30:05.05</span></span>|

<span data-ttu-id="17d99-328">Du bör vara medveten om att millisekunder ska tolkas som decimala systemet.</span><span class="sxs-lookup"><span data-stu-id="17d99-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="17d99-329">Så till exempel 3, 30 och 300 betyder alla 300 millisekunder, medan 03 betyder 30 och 003 innebär 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="17d99-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="17d99-330">Du kan inte använda 24:00 som midnatt eller välja ett värde som är större än 24:00.</span><span class="sxs-lookup"><span data-stu-id="17d99-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="17d99-331">Ordet för ”tid” på det språk som används av [!INCLUDE[prod_short](includes/prod_long.md)] utvärderas till aktuell tid på din dator eller mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="17d99-331">The word for 'time' in the language used by [!INCLUDE[prod_short](includes/prod_long.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="17d99-332">Du kan skriva in alla ord, från början, såsomt eller TIM.</span><span class="sxs-lookup"><span data-stu-id="17d99-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="17d99-333">Ange kombinerade datum och tider</span><span class="sxs-lookup"><span data-stu-id="17d99-333">Entering Combined Dates and Times</span></span>

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a><span data-ttu-id="17d99-334">Ange varaktighet</span><span class="sxs-lookup"><span data-stu-id="17d99-334">Entering Duration</span></span>
<span data-ttu-id="17d99-335">Vissa fält i programmet representerar en varaktighet eller mängden förfluten tid, i stället för ett visst datum eller tid.</span><span class="sxs-lookup"><span data-stu-id="17d99-335">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="17d99-336">Du anger varaktigheten som en siffra följd av en enhet.</span><span class="sxs-lookup"><span data-stu-id="17d99-336">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="17d99-337">Här följer några exempel.</span><span class="sxs-lookup"><span data-stu-id="17d99-337">Here are some examples.</span></span>

|<span data-ttu-id="17d99-338">**Varaktighet**</span><span class="sxs-lookup"><span data-stu-id="17d99-338">**Duration**</span></span>|<span data-ttu-id="17d99-339">**Enhet**</span><span class="sxs-lookup"><span data-stu-id="17d99-339">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="17d99-340">2t</span><span class="sxs-lookup"><span data-stu-id="17d99-340">2h</span></span>|<span data-ttu-id="17d99-341">2 timmar</span><span class="sxs-lookup"><span data-stu-id="17d99-341">2 hrs</span></span>|
|<span data-ttu-id="17d99-342">6t 30m</span><span class="sxs-lookup"><span data-stu-id="17d99-342">6h 30 m</span></span>|<span data-ttu-id="17d99-343">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="17d99-343">6 hrs 30 mins</span></span>|
|<span data-ttu-id="17d99-344">6,5t</span><span class="sxs-lookup"><span data-stu-id="17d99-344">6.5h</span></span>|<span data-ttu-id="17d99-345">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="17d99-345">6 hrs 30 mins</span></span>|
|<span data-ttu-id="17d99-346">90m</span><span class="sxs-lookup"><span data-stu-id="17d99-346">90m</span></span>|<span data-ttu-id="17d99-347">1 timme 30 minuter</span><span class="sxs-lookup"><span data-stu-id="17d99-347">1 hr 30 mins</span></span>|
|<span data-ttu-id="17d99-348">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="17d99-348">2d 6h 30m</span></span>|<span data-ttu-id="17d99-349">2 dagar 6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="17d99-349">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="17d99-350">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="17d99-350">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="17d99-351">2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder</span><span class="sxs-lookup"><span data-stu-id="17d99-351">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="17d99-352">Du kan även ange en siffra som automatiskt konverteras till en varaktighet.</span><span class="sxs-lookup"><span data-stu-id="17d99-352">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="17d99-353">Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.</span><span class="sxs-lookup"><span data-stu-id="17d99-353">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="17d99-354">Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.</span><span class="sxs-lookup"><span data-stu-id="17d99-354">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="17d99-355">Till exempel om mätenheten är timmar konverteras siffran 5 till 5 timmar.</span><span class="sxs-lookup"><span data-stu-id="17d99-355">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="17d99-356">Se även</span><span class="sxs-lookup"><span data-stu-id="17d99-356">See Also</span></span>
<span data-ttu-id="17d99-357">[Arbeta med [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="17d99-357">[Working with [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="17d99-358">Datumberäkning för inköp</span><span class="sxs-lookup"><span data-stu-id="17d99-358">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="17d99-359">Ange villkor i filter </span><span class="sxs-lookup"><span data-stu-id="17d99-359">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]