---
title: Hur du anger du data i fält | Microsoft Docs
description: Det finns många allmänna funktioner som gör det snabbt och enkelt att registrera data. Dessa funktioner för dataregistrering beskrivs i det här avsnittet.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: f1bd2fb92f787d52c5bbab8c2210b9d424c1ffd5
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/19/2019
ms.locfileid: "852499"
---
# <a name="entering-data"></a>Ange data
Det finns många allmänna funktioner som gör det snabbt och enkelt att registrera data. Dessa funktioner för dataregistrering beskrivs i den här artikeln.  

I exemplen nedan används demonstrationsdata.

## <a name="mandatory-fields"></a>Obligatoriska fält
När du anger data på sidor markeras vissa fält med en röd asterisk. Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.  

Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan. Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.  


## <a name="finding-data-as-you-type"></a>Söka efter data allt eftersom du skriver  
 När du börjar skriva tecken i ett fält visas en listruta med möjliga fältvärden. Listan ändras allt eftersom du skriver fler tecken, och du kan välja rätt värde när det visas.  

 Många fält har en nedpil-knapp som du kan välja. Du kan välja pilen om du vill visa en lista med data som är tillgängliga för fältet. Knappen har två funktioner beroende på typen av fält:  

-   Sökning – Visar information från en annan tabell som du kan infoga i fältet. Du kan bara välja en i taget.  

-   Lista – Visar den uppsättning alternativ (fasta val) som finns för fältet. Du kan bara markera ett av alternativen.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Ange antal genom beräkning  
 När du skriver siffror i antalsfält, till exempel fältet **Antal** för en artikeljournalrad, kan du skriva formeln i stället för summan.  

## <a name="examples"></a>Exempel  

-   Om du skriver 19+19 beräknas fältet till 38.  

-   Om skriver 41-9 beräknas fältet till 32.  

-   Om du skriver 12*4 beräknas fältet till 48.  

-   Om du skriver 12/4 beräknas fältet till 3.  

## <a name="entering-negative-numbers"></a>Ange negativa antal
Du kan ange negativa antal på två sätt. Numret -20,5 som kan anges:  

-   -20.5  

    eller
-   20.5-  

 I båda fallen registreras beloppet som -20,5.  

 Om det sista tecknet i uttrycket är **+** eller **-**, kommer hela uttrycket registreras med det tecknet. Ett exempel, **10-20+**, ska leda till 10 och inte -10.  

## <a name="entering-dates-and-times"></a>Ange datum och tider
Du kan ange datum och tider i alla datumfält. Du kan skriva datum med eller utan avgränsare.

> [!NOTE]  
> Hur du anger datum och klockslag beror på dina **region**-inställningar. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Ange datum  
 I ett datumfält kan du skriva in två, fyra, sex eller åtta siffror.  

-   Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.  

-   Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.  

-   Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.  

 Du kan också skriva ett datum som en veckodag följt av veckonumret och (valfritt) ett år (exempelvis Mån25, eller mån25 betyder måndagen i vecka 25).  

 I stället för att skriva in ett visst datum kan du skriva in någon av de två koderna nedan.  

|Kod|Resultat|  
|--------------|----------------|  
|d|Det här är dagens datum (detta är datorns systemdatum).|  
|a|Detta är arbetsdatumet som har lagts upp i programmet. Om du vill ändra arbetsdatumet, [ändra grundläggande inställningar](ui-change-basic-settings.md). Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a>Ange tider  
 När du anger tider kan du infoga vilken avgränsare du vill mellan enheterna. Detta är dock inte obligatoriskt. Du behöver inte skriva minuter, sekunder eller AM/PM.  

 I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.  

|Transaktion|Tolkning|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5.50|05:30:05.5|  
|053005050|05:30:05.05|  

 Du måste ange två siffror för varje tidsenhet om du inte använder någon avgränsare.  

## <a name="entering-datetimes"></a>Ange datum och tid  
 När du anger datum och tid måste du ange ett blanksteg mellan datumet och tiden.  

 Listan nedan innehåller de olika sätt som du kan ange datum och tid på och en förklaring av hur de ska tolkas.  

|Transaktion|Tolkning|  
|---------------|------------------------|  
|021213 132455|02-12-13 13:24:55|  
|02-12-1 10|02-12-01 10:00:00|  
|02.12.1 5|02-12-01 05:00:00|  
|02.12.1|02-12-01 00:00:00|  
|11 12|11-innevarande månad-innevarande år 12:00:00|  
|11 12 12|11-12-innevarande år 12:00:00|  
|d eller dagens datum|dagens datum 00:00:00|  
|d tid|dagens datum aktuell tid|  
|d 10:30|dagens datum 10:30:00|  
|d 03:03:03|dagens datum 03:03:03|  
|a eller arbetsdagens datum|arbetsdagens datum 00:00:00|  
|m eller måndag|måndag i innevarande vecka 00:00:00|  
|ti eller tisdag|tisdag i innevarande vecka 00:00:00|  
|on eller onsdag|onsdag i innevarande vecka 00:00:00|  
|to eller torsdag|torsdag i innevarande vecka 00:00:00|  
|fr eller fredag|fredag i innevarande vecka 00:00:00|  
|lö eller lördag|lördag i innevarande vecka 00:00:00|  
|sö eller söndag|söndag i innevarande vecka 00:00:00|  
|ti 10:30|tisdag i innevarande vecka 10:30:00|  
|ti 03:03:03|tisdag i innevarande vecka 03:03:03|  

## <a name="entering-duration"></a>Ange varaktighet  
 Du anger varaktigheten som en siffra följd av en enhet.  

 Här följer några exempel.  

|Varaktighet|Måttenhet**|  
|------------------|-------------------------|  
|2t|2 timmar|  
|6t 30m|6 timmar 30 minuter|  
|6,5t|6 timmar 30 minuter|  
|90m|1 timme 30 minuter|  
|2d 6t 30m|2 dagar 6 timmar 30 minuter|  
|2d 6t 30m 56s 600ms|2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder|  

 Du kan även ange en siffra som automatiskt konverteras till en varaktighet. Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.  

 Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.  

 Numret 5 konverteras till 5 timmar om enheten är timmar.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Använda datumformler  
 En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas. Du kan ange datumformler i olika beräkningsfält för datum och i fält för återkomstfrekvens i återkommande journaler.  

> [!NOTE]  
>  I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar. Därefter om du anger, till exempel 1 vecka, är perioden faktiskt åtta dagar eftersom idag inkluderas. För att ange en period av sju dagar (en exakt vecka) inklusive perioden för startdatum måste du ange 6 dagar eller 1 vecka minus 1 dag.  

 Här följer några exempel på hur datumformler kan användas:  

-   Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.  

-   Datumformeln i fältet Betalningsfrist för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet (eller från den föregående påminnelsen) innan en påminnelse ska skapas.  

-   Datumformeln i fältet Förfallodatumformel bestämmer hur förfallodatumet på påminnelsen beräknas.  

 Formeln för datumberäkning kan bara omfatta högst 20 tecken, både siffror och bokstäver. Du kan använda följande bokstäver som förkortningar för tidsangivelser.  

|||  
|-|-|  
|L|Löpande (innevarande)|  
|D|Dag/dagar|  
|V|Vecka/veckor|  
|M|Månad/månader|  
|K|Kvartal|  
|Å|År|  

 Du kan bygga upp en datumformel på tre sätt.  

 Följande exempel visar hur aktuell plus en tidsenhet.  

|||  
|-|-|  
|LV|Löpande (innevarande) vecka|  
|LM|Löpande (innevarande) månad|  

 Följande exempel visar hur ett antal och en tidsenhet. Ett nummer får inte vara högre än 9 999.  

|||  
|-|-|  
|10D|Tio dagar från dagens datum.|  
|2V|Två veckor från dagens datum|  

 Följande exempel visar hur en tidsenhet och ett antal.  

|||  
|-|-|  
|D10|Den tionde dagen varje månad.|  
|VD4|Den nästa fjärde dagen i en vecka (torsdag)|  

 Följande exempel visar hur du kombinera dessa tre metoder om så behövs.  

|||  
|-|-|  
|LM+10D|Löpande månad + 10 dagar|  

 Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.  

|||  
|-|-|  
|-1Å|1 år sedan från idag|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Se även  
 [Sortera, söka och filtrera listor](ui-enter-criteria-filters.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
