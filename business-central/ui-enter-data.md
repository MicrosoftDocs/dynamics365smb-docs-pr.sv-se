---
title: Hur du anger du data i fält | Microsoft Docs
description: Lär dig mer om allmänna funktioner som hjälper dig att ange data i fälten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252464"
---
# <a name="entering-data"></a>Ange data

Det finns många allmänna funktioner som hjälper dig att ange data lättare, snabbare och mer exakt. Dessa allmänna funktioner för dataregistrering beskrivs i den här artikeln.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Kortkommandon

Det finns flera kortkommandon som gör att du kan arbeta ”utan mus” och snabba på din datainmatning, särskilt med storskaliga och återkommande textinmatningsuppgifter.

Mer information om genvägar finns i [Kortkommandon](keyboard-shortcuts.md). I den här artikeln beskrivs några genvägar.

## <a name="QuickEntry"></a>Påskynda datainmatning med snabbinmatning

Snabbinmatning är en funktion som skapats för datainmatning vid användning av tangentbordet. Snabbinmatning fungerar på fält (t.ex. på kortsidorna) och i listor (rader och kolumner). Det är bra när återkommande textinmatningsuppgifter utförs som behöver skapa flera poster i taget, till exempel en uppsättning försäljningsorder eller registrering av nya artiklar.

Du kanske redan känner till att använda Tabb-tangenten för att gå från ett fält på en sida till nästa redigerbara fält. Nackdelen med att använda Tabb-tangenten är att det alltid går sekventiellt till nästa fält. <!-- even if the field is non-editable or seldom filled it in.-->Snabbinmatning låter dig ändra den här sökvägen. Med snabbinmatning använder du Retur-knappen för att navigera i de fält som du är intresserad av, hoppar över skrivskyddade fält och fält som du vanligtvis inte fyller i. Du kanske redan har upptäckt denna funktion på vissa sidor. Detta beror på att programmet redan anger vilka fält som ska inkluderas när du trycker på Retur och vilka som ska hoppas över. Du kan anpassa snabbinmatning genom att anpassa arbetsytan och optimera hur du anger data på varje sida.

### <a name="how-quick-entry-works"></a>Hur snabbinmatning fungerar

Varje fält kan markeras som antingen *inkluderas i snabbinmatning* eller *exkluderas från snabbinmatning*. Som inkluderas i snabbinmatning inkluderas i sökvägen när du trycker på Retur. fält som exkluderas från snabbinmatning kommer inte att göra detta.

När du är klar med att ange data i ett fält trycker du bara på Retur för att bekräfta ändringarna och gå till nästa fält. Om du vill byta riktning och fortsätter till föregående fält trycker du på Shift + Retur. Mer information om genvägar finns i [kortkommandon på tangentbord för snabbinmatning](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tips och råd
Nedan finns användbar information om hur du använder snabbinmatning.

- Den är tillgänglig för alla fält som kan redigeras.
- Den fungerar även i kolumner och rader.
- Den hindrar inte från att komma åt andra element på en sida, till exempel åtgärder. Dessa är tillgängliga genom att använda Tabb och Shift + Tabb.  
- Snabbflikarna behöver inte expanderas för att snabbinmatning ska fungera. Om nästa snabbinmatningsfält finns i en komprimerad snabbflik kommer den snabbfliken automatiskt expandera och fokusera på det tilldelade fältet.
- Snabbinmatning fungerar oavsett om fälten är obligatoriska. Så det är en bra idé att kontrollera att obligatoriska fält är inkluderade i snabbinmatning.
- Som standard inkluderas de flesta fält i snabbinmatning. Så i början kommer uppgiften troligen att utesluta fält från snabbinmatning.

### <a name="how-to-change-quick-entry-fields"></a>Så här ändrar du snabbinmatningsfält

Om du vill ändra vilka fält som ska inkluderas eller exkluderas i snabbinmatning på en sida, kan du använda anpassning.

1. Starta anpassning genom att välja ikonen ![inställningar](media/ui-experience/settings_icon_small.png "ikonen inställningar för rollcenter") och sedan **anpassa**.
2. Välj ett fält som du vill ändra, eller i listor, väljer du motsvarande kolumnrubrik eller väljer antingen **inkludera i snabbinmatning** eller **exkludera snabbinmatning**.

Mer information om anpassning finns i [Anpassa arbetsyta](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Obligatoriska fält

När du anger data på sidor markeras vissa fält med en röd asterisk. Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.  

Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan. Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.  

## <a name="finding-data-as-you-type"></a>Söka efter data allt eftersom du skriver

 När du börjar skriva tecken i ett fält visas en listruta med möjliga fältvärden. Listan ändras allt eftersom du skriver fler tecken, och du kan välja rätt värde när det visas.  

 Många fält har en nedpil-knapp som du kan välja. Du kan välja pilen om du vill visa en lista med data som är tillgängliga för fältet. Knappen har två funktioner beroende på typen av fält:  

-   Sökning – Visar information från en annan tabell som du kan infoga i fältet. Du kan bara välja en i taget.  

-   Lista – Visar den uppsättning alternativ (fasta val) som finns för fältet. Du kan bara markera ett av alternativen.  

## <a name="copying-and-pasting-fields-and-lines"></a>Kopiera och klistra in fält och rader

Du kan kopiera en eller flera rader i en lista eller ett enda fält på en sida och klistra in det du kopierade till samma sida, en annan sida eller ett externt dokument (såsom Microsoft Excel och Outlook e-post). Kortfattat, för att kopiera trycker du på CTRL + C (cmd + C i macOS) på tangentbordet. Klistra in genom att trycka på CTRL + V (cmd + V i macOS).

I en lista kopierar du fältet i samma kolumn i raden ovanför och klistra in den i den aktuella raden, tryck bara på F8.

Mer information finns i [Kopiera och klistra in i Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Fokusera på radartiklar

När du arbetar med dokument som innehåller en radartikeldel, som en försäljningsorder eller en fakturasida kan du växla vyn till att fokusera på poster, i huvudsak expandera radartikeldelen så att den upptar nästan hela arbetsytan, dölja andra delar av den sidan förutom åtgärder överst. Detta ger dig en bättre översikt över radobjekten och ger mer plats att arbeta med dem. Detta är speciellt viktigt när du arbetar med stora radposter och snabb dataregistrering önskas.

En annan fördel är den även ger avancerade filtreringsfunktioner, precis som i andra listor, så bläddra och söka igenom radposter blir ännu enklare.

### <a name="switch-the-focus-on-and-off"></a>Aktivera och inaktivera fokus

För att fokusera på radartiklar väljer du var som helst i radartikeldelen och välj ![ikonen Fokusläge](media/focus-mode.png "ikonen Fokusläge") i övre högra hörnet eller tryck på Ctrl + Shift + F12.

Om du vill växla tillbaka till normal vy, väljer ![ikonen Fokusläge](media/focus-mode.png "ikonen Fokusläge") eller tryck på Ctrl + Shift + F12 igen.

### <a name="filtering-the-line-items"></a>Filtrera radposter

För att starta filtrering, välj ![Filterrutaikon](media/open-filter-pane-icon.png "Filterrutaikon") högst upp i listan eller tryck på **Shift+F3** för att öppna filterrutan. Du kan arbeta med filterrutan som på vilken lista som helst. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#Filtering).

Filtrering är särskilt användbart när du visar och analyserar längre dokument. Anta att du öppnar en bokförd försäljningsfaktura och filtrerar radposter för att visa alla radposter som har en enskild rabatt på mer än 5 % eller ett filter för att visa endast cykeltillbehör med "proffs" i namnet.

## <a name="entering-quantities-by-calculation"></a>Ange antal genom beräkning

När du skriver siffror i antalsfält, till exempel fältet **Antal** för en artikeljournalrad, kan du skriva formeln i stället för summan.  

### <a name="examples"></a>Exempel  

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

För datumfält kan du antingen använda dataväljaren som låter dig välja ett datum från en kalender eller så kan du ange datumen manuellt. Det här avsnittet innehåller en kort översikt över hur du anger datum. Mer information finns i [arbeta med kalenderdatum och tider](ui-enter-date-ranges.md).

För manuell datainmatning kan du skriva in två, fyra, sex eller åtta siffror.  

-   Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.  

-   Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.  

-   Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.  

Du kan också skriva ett datum som en veckodag följt av veckonumret och (valfritt) ett år (exempelvis Mån25, eller mån25 betyder måndagen i vecka 25).  

I stället för att skriva in ett visst datum kan du skriva in någon av dessa koder.  

|Kod|Resultat|  
|--------------|----------------|  
|d|Det här anger dagens datum (detta är datorns systemdatum).|  
|p|Det här anger en bokföringsperiod där `p`innebär att den första bokföringsperiod, `p2` innebär det andra kontot, och så vidare. |
|a|Detta anger arbetsdatumet som har lagts upp i programmet. Om du vill ändra arbetsdatumet, [ändra grundläggande inställningar](ui-change-basic-settings.md). Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.|
|c|Detta anger att datumet efter `c`är ett avslutsdatum, till exempel `C123101`.|  

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Se även  
 [Sortera, söka och filtrera listor](ui-enter-criteria-filters.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
