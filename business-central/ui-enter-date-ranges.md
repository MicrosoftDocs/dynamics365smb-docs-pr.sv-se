---
title: Ange datum och tider i Business Central
description: Lära dig att ange datum och tider, inklusive olika tips för produktivitet till exempel snabbskrift, uttryck och intervaller.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 8254afc467474906dd80ae76ba134a0bce88c3a0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443649"
---
# <a name="working-with-calendar-dates-and-times"></a>Arbeta med kalenderdatum och tider

[!INCLUDE[prod_short](includes/prod_long.md)] ger flera sätt för att ange datum och tider, inklusive kraftfulla funktioner som förbättrar datainmatning eller hjälper dig att skriva komplexa kalenderuttryck. Det finns olika ställen i programmet där du kan ange datum och tider i ett fält. På t. ex. en försäljningsorder kan du ange leveransdatumet. När du filtrerar listor eller rapportdata, kan du ange datum och tider för att precisera endast den information som du är intresserad av.

## <a name="check-your-region-and-language-settings"></a>Kontrollera inställningarna för region och språk
Sidan **Mina inställningar** anger **Region** och **Språk** du använder i programmet. Dessa inställningar påverkar hur du anger datum och tid.

-   Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras.

-   För datummönster som omfattar ord måste språket för de ord som du använder stämma överens med **språk**-inställningen.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] använder det gregorianska kalendersystemet.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Ange datum

I ett datumfält kan du ange ett datum med standardformat för din region. Olika områden kan använda olika avgränsare mellan dagar, månader och år. Exempelvis använder vissa regioner bindestreck (åååå-mm-dd) och andra snedstreck (åååå/mm/dd). Du kan använda alla avgränsare, även blanksteg och datumet ändras automatiskt till att använda avgränsare som matchar din region.

Observera att formatet som datum visas på utskrivna rapporter eller e-postade dokument påverkas inte av dina personliga inställningar av region.

Om du vill arbeta mer effektivt med datum och tider, använd någon av de metoder eller format som beskrivs nedan.

### <a name="picking-dates-from-the-calendar"></a>Välja datum från kalendern

Ett fält som visar en kalenderikon kan anges med hjälp av kalenderdatumväljaren. Om du vill visa kalenderdatumväljaren, aktivera kalenderikonen eller tryck på kortkommandot Ctrl + Home i fältet.

![Datumfält.](media/ui-date-field.png "Exempel på datumfält")

Se även [Kortkommandon i kalenderdatumväljaren](keyboard-shortcuts.md#calendarshortcuts)

### <a name="day-week-year-pattern"></a>Dag\-vecka\-år-mönster

Du kan ange ett datum som en veckodag följt av ett veckonummer och alternativt ett år. Till exempel Mån25 eller mån25 betyder måndag vecka 25. Om du inte anger ett år används året från arbetsdatumet.

I stället för att ange hela ordet för dagen i veckan, kan du skriva in del av ordet, från början. Om det uppstår konflikter (exempelvis med t som kan vara tisdag eller torsdag) utvärderas dagarna utifrån regionsinställningen. Indata utvärderas först mot arbetsdagen och idag, så tänk på detta när du förkortar. Till exempel t innebär today (idag), så det kan inte innebära: tisdag eller torsdag.

Veckonummersystemet är alltid ISO-8601 där vecka 1 är veckan med 4 januari eller veckan med första torsdagen på året.

### <a name="digit-patterns"></a>Siffermönster

I ett datumfält kan du skriva in två, fyra, sex eller åtta siffror.

-   Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.

-   Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet. Order för den dagen och månaden avgörs av dina regioninställningar. Även om dina regioninställningar har året före dagen och månaden, tolkas fyra siffror som dag och månad.

-   Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.

### <a name="today"></a>I dag

Ange ordet för _idag_, på det språk som anges på sidan **Mina inställningar**, för att ange dagens datum på en post. I stället för att ange hela ordet, kan du skriva in del av ordet, från början. På engelska kan du till exempel ange _t_ eller _tod_ förutsatt att det inte också är början på ett annat ord.

### <a name="period"></a>Period

Om du vill filtrera efter en viss redovisningsperiod i ett datumfält skriver du in p eller ordet period, följt av ett nummer som identifierar bokföringsperioden som p2 eller period4. Bokföringsperioden är i förhållande till räkenskapsåret för det aktuella arbetsdatumet som angetts i ditt rollcenter. Om arbetsdatumet är till exempel **22-03-21**, då är p1, eller bara p filter på den första perioden på räkenskapsåret 2022 (såsom 22-01-01..20-01-31). p15 filter för femtonde bokföringsperioden från början av år 2022 (såsom 23-03-01..21-03-31).

Bokföringsperioder definieras på sidan **Bokföringsperioder**. Om du vill visa eller ändra bokföringsperioderna, öppna sidan [här](https://businesscentral.dynamics.com/?page=100).

### <a name="work-date"></a>Arbetsdatum

Använd ett arbetsdatum för att ange ett datum som inte är dagens datum på poster. Ett arbetsdatum kan t.ex. vara användbart när du vill ange ett visst datum för flera poster. Du anger arbetsdatumet på sidan **Mina inställningar**. 

Ett snabbt sätt att ange arbetsdatumet på en post är att ange en del av eller hela ordet _arbete_, från början av ordet, på det språk som du använder [!INCLUDE[prod_short](includes/prod_long.md)]. På engelska kan du till exempel ange _w_ eller _arbete_. Språket anges också på sidan **Mina inställningar**.

Om du inte har angett något arbetsdatum kommer dagens datum att användas. För mer information, se [Ändra grundläggande inställningar, såsom arbetsdatum](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Avslutsdatum

När du avslutar ett räkenskapsår kan du använda avslutsdatum för att ange att en transaktion är en bokslutspost. Ett avslutsdatum ligger tekniskt sätt mellan två datum, till exempel mellan den 31 december och den 1 januari.

För att ange att ett datum är ett avslutsdatum ange A före datumet såsom A120131. Detta kan användas tillsammans med alla datummönster.

### <a name="examples"></a>Exempel

Följande tabell innehåller exempel på datum med alla format. Det förutsätter regioninställningar som formaterar datum enligt: **år.månad.dag.**, en vecka med start på måndag och på engelska.

|**Format**      |**Tolkning**      |
|---------------|------------------------|
|2022.12.31.|2022.12.31.|
|221231|2022.12.31.|
|22.12.31.|2022.12.31.|
|22.12.31.|2022.12.31.|
|20221231|2022.12.31.|
|22/12,31|2022.12.31.|
|11|arbetsdatum år-arbetsdatum månad-11.|
|1112|arbetsdatum år-11-12.|
|d eller dagens datum|dagens datum|
|p4|datumintervall som innehåller den fjärde bokföringsperioden, till exempel 20-04-01...21-04-30|
|a eller arbetsdagens datum|arbetsdatum|
|m eller måndag|Måndag av arbetsdatumets vecka|
|ti eller tisdag|Tisdag av arbetsdatumets vecka|
|lö eller lördag|Lördag av arbetsdatumets vecka|
|s eller söndag|Söndag av arbetsdatumets vecka|
|t23|Tisdag av vecka 23 arbetsdatumets år|
|t 23|Tisdag av vecka 23 arbetsdatumets år|
|t-1|Tisdag av vecka 1 arbetsdatumets år|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> Inställningsintervall

I listor, summor och rapporter kan du ange filter för datum, tid och datum och tid som innehåller ett startvärde och ett slutvärde om du endast vill visa de data som finns inom intervallet. Standardregler gäller för hur du kan ange datumintervall.

|**Betydelse**|**Exempeluttryck (datum)**|**Data som ingår i filtret**|
|-----------|---------------------|--------------------|
|Intervall|00-12-15..01-01-15<br /><br />..00-12-15<br /><br />p1..p4|Poster med datum från och med 00-12-15 till och med 01-01-15.<br /><br />Poster med datum 00-15-12 eller tidigare.<br /><br />Datumintervall som innehåller den andra, tredje och fjärde bokföringsperioden, till exempel 20-01-01..20-04-30.|
|Antingen eller|00-12-15\|00-12-16|Poster med antingen 00-12-15 eller 00-12-16. Om det finns poster med datum båda dagarna kommer samtliga att visas.|
|Kombination|00-12-15\|00-12-01..00-12-10  <br /><br />..00-12-14\|00-12-30..|Poster med datum 00-12-15 eller mellan och inklusive den 00-12-01 och 00-12-10.  <br /><br />Poster med datum 00-12-14 eller tidigare, eller 00-12-30 eller senare. Detta innebär alla poster utom de med datum från och med 00-12-15 till och med 00-12-29.|

Du kan använda giltiga format i filtret för datumintervall. Till exempel mån14 3..t 4p som tillämpas på ett datum/tidsfält resulterar i ett filter mellan 03:00 måndag vecka 14 det aktuella arbetsdatumets år, inklusive fram till i dag klockan 16:00.

## <a name="using-date-formulas"></a>Använda datumformler
En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas. Du kan ange datumformler i olika fält eller filter för datumberäkning.

> [!NOTE]
>  I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar. Om du till exempel anger 1V, är perioden därefter faktiskt åtta dagar eftersom idag inkluderas. För att ange en period av sju dagar \(en exakt vecka\) inklusive perioden för startdatum måste du ange 6 dagar eller 1 vecka minus 1 dag.

Här följer några exempel på hur datumformler kan användas:

-   Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.

-   Datumformeln i fältet **Betalningsfrist** för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet \(eller från den föregående påminnelsen\) innan en påminnelse ska skapas.

-   Datumformeln i fältet **Förfallodatumformel** bestämmer hur förfallodatumet på påminnelsen beräknas.

Datumformeln kan omfatta högst 20 tecken, både siffror och bokstäver. Du kan använda följande bokstäver som förkortningar för kalenderenheter.

|  Bokstav  |  Betydelse  |
|----------|----------------------|
|A|Aktuell|
|D|Dag\(ar\)|
|V|Vecka\(veckor\)|
|M|Månad\(er\)|
|K|Kvartal\(s\)|
|Å|År\(\)|

Du kan bygga upp en datumformel på tre sätt.

Följande exempel visar hur du använder A för aktuell, plus en tidsenhet.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|AV|Aktuell vecka|
|AM|Aktuell månad|

Följande exempel visar hur du använder ett tal och en tidsenhet. Ett nummer får inte vara högre än 9 999.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|10D|Tio dagar från dagens datum.|
|2V|Två veckor från dagens datum|

Följande exempel visar hur du använder en tidsenhet och ett tal.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|D10|Den tionde dagen varje månad.|
|VD4|Den nästa fjärde dagen i en vecka \(torsdag\)|

Följande exempel visar hur du kombinera dessa tre metoder om så behövs.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|AM+10D|Aktuell månad \+ 10 dagar|

Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|-1Å|1 år sedan från idag|

> [!IMPORTANT]
> Om lagerstället använder en baskalender, tolkas datumformeln som du anger i t. ex. fältet **Leveranstid** enligt kalenderarbetsdagar. Till exempel betyder 1V sju arbetsdagar.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list.](./media/ui-enter-date-ranges/customer-top10-list.png)

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

## <a name="entering-times"></a>Ange tider
När du anger tider kan du infoga alla icke-platsavgränsare som du vill mellan enheterna, men om du använder två siffror för varje enhet upp till millisekunder, är det valfritt.

Du behöver bara skriva de största enheterna som du vill ha, övriga anges till noll. Du kan också utelämna alla AM/PM-indikatorer.

I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas. Det följer regioninställningar som formaterar tid enligt: **Timmar:Minuter:Sekunder.Millisekunder.** och använder du AM- och PM-indikatorer ”AM” och ”PM”.

|**Format**      |**Tolkning**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5|05:30:05|
|053005|05:30:05|
|5:30:5.50|05:30:05.5|
|053005050|05:30:05.05|

Du bör vara medveten om att millisekunder ska tolkas som decimala systemet. Så till exempel 3, 30 och 300 betyder alla 300 millisekunder, medan 03 betyder 30 och 003 innebär 3 millisekunder.

Du kan inte använda 24:00 som midnatt eller välja ett värde som är större än 24:00.

Ordet för ”tid” på det språk som används av [!INCLUDE[prod_short](includes/prod_long.md)] utvärderas till aktuell tid på din dator eller mobil enhet. Du kan skriva in alla ord, från början, såsomt eller TIM.

## <a name="entering-combined-dates-and-times"></a>Ange kombinerade datum och tider

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a>Ange varaktighet
Vissa fält i programmet representerar en varaktighet eller mängden förfluten tid, i stället för ett visst datum eller tid. Du anger varaktigheten som en siffra följd av en enhet.

Här följer några exempel.

|**Varaktighet**|**Enhet**|
|------------|-------------------|
|2t|2 timmar|
|6t 30m|6 timmar 30 minuter|
|6,5t|6 timmar 30 minuter|
|90m|1 timme 30 minuter|
|2d 6t 30m|2 dagar 6 timmar 30 minuter|
|2d 6t 30m 56s 600ms|2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder|

Du kan även ange en siffra som automatiskt konverteras till en varaktighet. Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.

Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.

Till exempel om mätenheten är timmar konverteras siffran 5 till 5 timmar.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)  
[Ange villkor i filter ](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]