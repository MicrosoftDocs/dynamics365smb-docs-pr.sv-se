---
title: Köra och skriva ut rapporter
description: Lär dig att lägga en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: ''
ms.date: 09/09/2022
ms.author: jswymer
ms.openlocfilehash: be4817ceac67674b82452b972c38dc316e274e8c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607182"
---
# <a name="run-and-print-reports"></a>Köra och skriva ut rapporter

En rapport samlar in information baserat på en angiven uppsättning kriterier. Den ordnar och presenterar informationen i ett lättläst format som du kan skriva ut eller spara som en fil. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

> [!NOTE]
> Batchjobb och XMLports gör mer eller mindre detsamma som rapporter, men används mer för att bearbeta eller exportera data. Till exempel skapar batch-jobbet **Skapa påminnelser** påminnelsedokument som skickas till kunder med förfallna betalningar. Den här artikeln avser huvudsakligen ”rapporter”, men liknande information gäller för batch-jobb och XMLports.

## <a name="get-started"></a>Kom i gång

Du hittar rapporter i menyn **Rapporter** på valda sidor, listor och kort, eller så kan du använda ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") för att hitta rapporter efter namn. En översikt över inbyggda rapporter som du kan använda i [!INCLUDE[prod_short](includes/prod_short.md)], sorterade efter kategorier, finns i [Tillgängliga rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

När du väljer en rapport visas vanligtvis en sidan för förfrågan&mdash;med rapportens namn&mdash;där du kan ange olika alternativ och filter som avgör vilka data som inkluderas. I följande avsnitt förklaras hur du använder sidan för begäran för att bygga, förhandsgranska och skriva ut en rapport.

## <a name="using-default-valuesmdashpredefined-settings"></a><a name="SavedSettings"></a>Använda standardvärden&mdash;fördefinierade inställningar

De flesta sidor för rapportbegäran innehåller fältet **Använd standardvärden från**. Med det här fältet kan du välja fördefinierade inställningar för rapporten, som automatiskt anger alternativ och filter. Välj en post i listrutan så ändras alternativen och filtren på sidan för rapportbegäran därefter.

Posten vid namn **Senast använda alternativ och filter** är alltid tillgänglig. Den här posten anger att rapporten ska använda alternativ och filter som du använde förra gången du körde rapporten.

Fältet **Använd standardvärden från** är ett snabbt och tillförlitligt sätt att skapa rapporter som innehåller rätt data. När du har valt en post kan du ändra alternativen och filtren innan du förhandsgranskar eller skriver ut rapporten. Utförda ändringar sparas inte i den post med fördefinierade inställningar som du valde, men de sparas i posten **Senast använda alternativ och filter**.

> [!NOTE]
> De fördefinierade inställningarna ställs in och hanteras vanligtvis av en administratör. Läs mer i [Hantera sparade inställningar för rapporter och batch-jobb](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Ange data att inkludera i rapporter

Använd fälten under **Alternativ** och **Filter** om du vill ändra eller begränsa den information som du vill ha i rapporten. Du kan ange att filter ska vara mer eller mindre på samma sätt som du anger filter för listor. Läs mer i avsnittet [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Snabbfliken **Filter** på sidan för rapportbegäran innehåller en allmän filtreringsfunktion för rapporter. Dessa filter är valfria.
>
> Vissa rapporter ignorerar dessa filter, vilket innebär att oavsett vilka filter som anges i snabbfliken **Filter** är rapportens resultat detsamma. Det går inte att skapa en lista vars fält ignoreras i vilka rapporter, så du måste experimentera med filtren om du använder dem.
>
> **Exempel**: När du använder batch-jobbet **Skapa påminnelser** ignoreras ett filter för fältet **Kundreskontratransaktioner** i **Senast utskickad påminnelsenivå** eftersom filter är fasta för det batch-jobbet.

## <a name="previewing-a-report"></a>Förhandsgranska en rapport

När du förhandsgranskar en rapport kan du se hur rapporten kommer att se ut innan du skriver ut den. Förhandsgranskningen baseras inte på den skrivare som har valts i fältet **Skrivare** på begärandesidan. Det kontrolleras av webbläsaren. När du har förhandsgranskat kan du gå tillbaka till förfrågningssidan och ändra alternativ och filter efter behov.

Vilka förhandsgranskningsalternativ du har på sidan **Rapportbegäran** beror på rapporten. För vissa rapporter kan du välja **Förhandsgranska**, men för andra har du alternativet **Förhandsgranska och stäng**. Båda alternativen öppnar en förhandsgranskning av rapporten. Skillnaden är att **Förhandsgranska** håller förfrågningssidan öppen, så att du kan gå tillbaka till den, göra ändringar, förhandsgranska igen eller skriva ut den. Men **Förhandsgranska & stäng** stänger begäranssidan, så du måste öppna rapporten igen för att göra ändringar eller skriva ut.

> [!NOTE]
> Om du använder Business Central från utgivningscykel 1 år 2020 eller tidigare har du endast alternativet **Förhandsgranska**, som stänger begäranssidan vid förhandsgranskning, som beskrivs ovan för **Förhandsgranska & stäng**.

### <a name="work-with-the-preview"></a>Arbeta med förhandsgranskning

I förhandsgranskningen använder du menyraden i förhandsgranskningen av rapporten när du vill:

- Flytta mellan sidor
- Zooma in och ut
- Ändra storlek så att den passar sidan
- Välj text

    Du kan kopiera text från en rapport och sedan klistra in den någon annanstans, som på en sida i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word. Med hjälp av en mus håller du till exempel ned vänster musknapp där du vill börja. Flytta sedan musen för att markera ett eller flera ord, meningar eller stycken. Tryck sedan på höger musknapp och välj **Kopiera**. Du kan nu klistra in den markerade texten där du vill.
- Panorera dokumentet

    Du kan flytta den synliga delen av rapporten i någon riktning för att visa andra områden av rapporten. Panorering är användbart när du har zoomat in för att visa detaljerad information. Med hjälp av musen kan du till exempel trycka och hålla ned vänster musknapp var som helst i rapportens förhandsgranskning och sedan flytta musen för att markera en del av rapporten.

- Hämta till en PDF-fil på datorn eller i nätverket.
- Skriv ut

## <a name="saving-a-report-to-a-file"></a>Spara en rapport i en fil

Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument, en Microsoft Excel-arbetsbok eller ett XML-dokument genom att välja **Skicka till**, och sedan göra ditt val. En fil hämtas till enheten.

Om organisationen har konfigurerat OneDrive för systemfunktioner i stället för att hämtas, öppnas Excel-arbetsböcker och Word-dokument i webbläsaren med antingen Excel eller Word för webben.

> [!TIP]
> Alternativen **Microsoft Excel dokument (endast data)** och **XML-dokument** är oftast avsedda för avancerade ändamål. Du använder vanligtvis dessa alternativ när du gör detaljerade dataanalyser. Läs mer i [Analysera rapportdata med Excel och XML](report-analyze-excel.md).
>
> Du kan också använda **Microsoft Excel-dokumentet (endast data)** om du vill skapa nya Excel-layouter för en viss rapport. Läs mer i [Arbeta med Excel-layouter](ui-excel-report-layouts.md).  

## <a name="scheduling-a-report-to-run-later-or-periodically"></a><a name="ScheduleReport"></a> Schemalägga en rapport att köra senare eller periodvis

Du kan schemalägga en enskild eller återkommande rapport att köras vid ett visst datum och tider. Planerade rapporter anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Välj alternativet **Schema** när du har valt **Skicka till**. Ange sedan information som skrivare samt datum och tid. Rapporten läggs till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

När du schemalägger en rapport som ska köras kan du till exempel ange att den måste köras varje torsdag genom att ställa in fältet **Datumformel för nästa körning** till *D4*. Läs mer i avsnittet [Använda datumformler](ui-enter-date-ranges.md#use-date-formulas).  

Du kan välja att spara rapporten till en fil, (t.ex en Excel-, Word- eller PDF-fil), skriva ut den eller bara skapa rapporten. Om du väljer att spara rapporten som en fil skickas den bearbetade rapporten till sidan **Rapportinkorg** i ditt rollcenter, där du kan visa den. Läs mer i [Dela och exportera rapporter med rapportinkorgen](ui-work-report-inbox.md)

### <a name="manage-scheduled-recurring-reports"></a>Hantera schemalagda återkommande rapporter

Schemalagda rapporter genereras av batchjobb som hanteras på sidan **Jobbkötransaktioner**. Du kan visa status och annan information för varje rapport på sidan, pausa/återuppta rapport-batch-jobbet och generera rapporten på begäran.

Från sidan **Jobbkötransaktioner** kan du även ändra vissa rapportparametrar, som utfiltypen, köringsdatumet samt start- och sluttider. Innan du redigerar en befintlig schemalagd rapport måste du pausa rapportens jobbkö:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Jobbkötransaktioner** och välj sedan relaterad länk.  
2. På sidan **Jobbkötransaktioner** väljer du önskad rapport.
3. Välj åtgärden **Pausa**.
4. Öppna och redigera den schemalagda rapporten genom att välja dess status (*Pausad*).

När du har redigerat rapportalternativen upprepar du de första två stegen och väljer sedan **Ställ in på status Redo** för att fortsätta generera rapporten.

Läs mer om hantering av jobbkö i [Använd jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skriva ut en rapport

Du skriver ut en rapport genom att välja **Skriv ut** på sidan för rapportbegäran eller på menyraden på sidan **Förhandsgranska**.

När en Excel-layout används i en rapport ser du inte fältet **Skrivare** eller knapparna **Skriv ut** eller **Förhandsgranska**. I stället finns alternativet **Hämta**. Om du vill skriva ut väljer du **hämta** och öppnar sedan den hämtade filen i Excel och skriver ut därifrån.

### <a name="printer"></a><a name="Printer"></a>Skrivare

Fältet **Skrivare** på begäranssidan visar namnet på skrivaren som rapporten skickas till. Om du vill ändra en skrivare markerar du bara skrivaren i listan.

> [!NOTE]
> Alternativet **(Hanteras av webbläsaren)** anger att rapporten inte har tilldelats någon skrivare. I så fall hanterar webbläsaren utskriften och visar en standardupplevelse där du kan välja en lokal skrivare som är ansluten till enheten. Alternativet **(Hanteras av webbläsaren)** är inte tillgängligt i [!INCLUDE[prod_short](includes/prod_short.md)] mobilappen eller appen för Microsoft Teams.

> [!TIP]
> Skrivaren som är markerad för dig som standard är inställd på sidan **Skrivarval**. Läs mer om hur du ändrar standardskrivare i avsnittet [Ange standardskrivare](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Skriva ut rapporter på thailändska

För den thailändska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] kan knappen **Skriv ut** inte skriva ut rapporter på rätt sätt på grund av begränsningar i tjänsten som genererar den utskrivbara PDF-filen. I stället kan du öppna rapporten i Word och spara den som utskrivbar PDF.  

Du kan också be administratören att skapa en layout för en Word-rapport för de mest använda rapporterna. Läs mer i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Växla rapportlayouten

En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Du kan ändra layouten på några få sätt:

- När du ska köra en rapport visas den aktuella layouten i fältet **Rapportlayout** på sidan för begäran. Om du tillfälligt vill använda en annan layout markerar du fältet **Rapportlayout** och väljer sedan från en lista med tillgängliga layouter för rapporten.
- Om du vill ändra standardlayouten som används av en rapport går du till någon av sidorna **Rapportlayouter** eller **Val av rapportlayout**.

Läs mer i [Ange layout för en rapport](ui-set-report-layout.md). Om du vill anpassa din egen rapportlayout går du till [Kom igång med att skapa layouter](ui-get-started-layouts.md).

## <a name="advanced-options"></a>Avancerade alternativ

Fälten under snabbfliken **Avancerat** anger begränsningar för den genererade rapporten för att kontrollera skrivarresurserna. Du behöver normalt inte ändra inställningarna om du inte har en stor rapport. Om en rapport överstiger dessa begränsningar när du försöker förhandsgranska eller skriva ut, visas ett meddelande om vilken begränsning som har överskridits. Du kan sedan ändra inställningarna så att de passar din rapport. Varje fält har dock ett maximalt värde som du bör känna till:

|Fält|Maximivärde|
|-----|-------------|
|Maximal återgivningstid|12:00:00|
|Maximalt antal rader|1 000 000|
|Maximalt antal dokument|500|

> [!NOTE]
> De högsta värdena kan vara olika för lokala [!INCLUDE[prod_short](includes/prod_short.md)] och en administratör kan ändra dem. Läs mer i avsnittet [Konfigurera Business Central Server – Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). En översikt över rapporteringsbegränsningar i [!INCLUDE[prod_short](includes/prod_short.md)] online finns i [Operativa gränser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft-utbildning](/training/paths/setup-reporting-dynamics-365-business-central/).

## <a name="see-also"></a>Se även

[Tillgängliga rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Använd rapporter i det dagliga arbetet](reports-use-reports.md)  
[Business Intelligence och rapporteringsöversikt](reports-bi-reporting.md)  
[Ställa in skrivare](ui-specify-printer-selection-reports.md)  
[Kör batch-jobb och XML-portar](ui-how-run-batch-jobs.md)  
[Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Ekonomisk Business Intelligence](bi.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
