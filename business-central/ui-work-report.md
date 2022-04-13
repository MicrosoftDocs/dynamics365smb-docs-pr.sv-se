---
title: Köra och skriva ut rapporter
description: Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 03/24/2022
ms.author: jswymer
ms.openlocfilehash: fade19b2ecb4d2c17b5d5775074f2f715496a908
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512686"
---
# <a name="run-and-print-reports"></a>Köra och skriva ut rapporter

En rapport samlar in information baserat på en angiven uppsättning kriterier. Den ordnar och presenterar informationen i ett lättläst format som du kan skriva ut eller spara som en fil. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

Batchjobb och XMLports gör mer eller mindre detsamma som rapporter, men används mer för att bearbeta eller exportera data. Till exempel batch-jobbet **skapa betalningspåminnelser** skapar påminnelsedokument för kunder med förfallna betalningar.  

> [!NOTE]
> Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb och XMLports.

## <a name="get-started"></a>Kom igång

Rapporter finns i liken **Rapporter** på valda sidor. Du kan också använda sökfunktionen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") för att hitta rapporter efter namn.

När du öppnar en rapport visas vanligtvis en sidan för förfrågan om batch-jobb, eller XMLport där du kan ange olika alternativ och filter som avgör vad som inkluderas i rapporten. I följande avsnitt förklaras hur du använder sidan för begäran för att bygga, förhandsgranska och skriva ut en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Använda standardvärden – fördefinierade inställningar

De flesta förfrågningssidor innehåller fältet **Använd standardvärden från**. I det här fältet kan du välja fördefinierade inställningar för rapporten, som automatiskt anger alternativ och filter för rapporten. Välj en post i listrutan så ändras alternativen och filtren på förfrågningssidan därefter.

Posten vid namn **Senast använda alternativ och filter** är alltid tillgänglig. Den här posten anger att rapporten ska använda alternativ och filter som användes förra gången du körde rapporten.

Fältet **Använd standardvärden från** är ett snabbt och tillförlitligt sätt att skapa rapporter som innehåller rätt data. När du har valt en post kan du ändra alternativen och filtren innan du förhandsgranskar eller skriver ut rapporten. Utförda ändringar sparas inte i den post med fördefinierade inställningar som du valde, men de sparas i posten **Senast använda alternativ och filter**.

>[!NOTE]
> De fördefinierade inställningarna ställs in och hanteras vanligtvis av en administratör. Mer information finns i [Hantera sparade inställningar i rapporter och batch-jobb](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Ange data att inkludera i rapporter

Använd fälten under **Alternativ** och **Filter** om du vill ändra begränsningen av den information som du vill ha i rapporten. Du kan ange att filter ska vara mer eller mindre på samma sätt som du anger filter för listor. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Avsnittet **Filtrera lista efter** på sidan för begäran innehåller en allmän filtreringsfunktion för rapporter. Dessa filter är valfria.
>
> Vissa rapporter ignorerar dessa filter, vilket innebär att oavsett vilka filter som anges i avsnittet **Filtrera lista efter** är rapportens resultat detsamma. Det går inte att skapa en lista vars fält ignoreras i vilka rapporter, så du måste experimentera med filtren om du använder dem.
>
> **Exempel**: när du använder batch-jobbet **Skapa betalningspåminnelser**, ett filter för fältet **Kundreskontratransaktioner** i **Senast utskickad bet.påm.nivå** kommer att ignoreras eftersom filter är fasta för det batch-jobbet.

## <a name="previewing-a-report"></a>Förhandsgranska en rapport

När du förhandsgranskar en rapport kan du se hur rapporten kommer att se ut innan du skriver ut den. Förhandsgranskningen baseras inte på den skrivare som har valts i fältet **Skrivare** på begärandesidan. Det kontrolleras av webbläsaren. När du har förhandsgranskat kan du gå tillbaka till förfrågningssidan och ändra alternativ och filter efter behov.

Om du vill förhandsgranska en rapport väljer du knappen **Förhandsgranska** eller **Förhandsgranska & stäng** på sidan för rapportförfrågan. Vilken knapp som visas beror på rapporten, så vissa rapporter har knappen **Förhandsgranska**, medan andra har knappen **Förhandsgranska & stäng**. Båda knapparna öppnar en förhandsgranskning av rapporten. Skillnaden är att **Förhandsgranska** håller förfrågningssidan öppen, så att du kan gå tillbaka till den, göra ändringar, förhandsgranska igen eller skriva ut den. Med **Förhandsgranska & stäng** stängs förfrågningssidan, så du måste öppna rapporten igen för att göra ändringar eller skriva ut.

> [!NOTE]
> Om du använder Business Central från utgivningscykel 1 år 2020 eller tidigare visas endast knappen **Förhandsgranska**, som stänger förfrågningssidan vid förhandsgranskning, som beskrivs för **Förhandsgranska & stäng**.

### <a name="work-with-the-preview"></a>Arbeta med förhandsgranskning

I förhandsgranskningen använder du menyraden i förhandsgranskningen av rapporten när du vill:

- Flytta mellan sidor
- Zooma in och ut
- Ändra storlek så att den passar sidan
- Välj text

    Du kan kopiera text från en rapport och sedan klistra in den någon annanstans, som en sida i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word.  Med hjälp av en mus håller du till exempel ned där du vill börja. Flytta sedan musen för att markera ett eller flera ord, meningar eller stycken. Tryck på höger musknapp och välj **Kopiera**. Klistra sedan in den markerade texten där du vill.
- Panorera dokumentet

    Du kan flytta den synliga delen av rapporten i någon riktning så att du kan se andra områden eller rapporten. Panorering är användbart när du har zoomat in för att visa detaljerad information.  Med hjälp av musen kan du till exempel trycka och hålla musknappen var som helst i rapportens förhandsgranskning och sedan flytta musen.

- Hämta till en PDF-fil på datorn eller i nätverket.
- Skriv ut

## <a name="saving-a-report-to-a-file"></a>Spara en rapport i en fil

Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-arbetsblad eller XML-dokument genom att välja knappen **skicka till**, och sedan göra ditt val.

> [!TIP]
> Alternativen **Microsoft Excel dokument (endast data)** och **XML-dokument** är oftast avsedda för avancerade ändamål. Du använder vanligt vis dessa alternativ när du gör detaljerade dataanalyser. Mer information finns i [Analysera rapportdata med Excel och XML](report-analyze-excel.md).
>
> Du kan också använda **Microsoft Excel dokumentet (endast data)** om du vill skapa nya Excel-layouter för en viss rapport. Mer information finns i [Arbeta med Excel-layout](ui-excel-report-layouts.md).  
  
<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="scheduling-a-report-to-run-later"></a><a name="ScheduleReport"></a> Schemalägga en rapport att köra senare

Du kan schemalägga eller köra batch-jobb för rapport att köras vid ett visst datum och tider. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **schema** när du har valt knappen **skicka till** och sedan skriver du in information om t. ex. skrivare, tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

När du schemalägger en rapport som ska köras kan du ange att den måste köras varje torsdag genom att ställa in fältet **Datumformel för nästa körning** till *D4*. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#use-date-formulas).  

Du kan välja att spara rapporten till en fil, (t.ex en Excel-, Word- eller PDF-fil), skriva ut den eller bara skapa rapporten. Om du väljer att spara rapporten som en fil skickas den bearbetade rapporten till området **Rapportinkorg** i ditt Rollcenter, där du kan visa den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skriva ut en rapport

Du skriver ut en rapport genom att trycka på knappen **Skriv ut** på förfrågningssidan eller på menyraden på sidan **Förhandsgranska**.

När en Excel-layout används i en rapport ser du inte fältet **skrivare**, knappen **Skriv ut** eller **Förhandsgranska**. I stället finns en knapp för att **hämta**. Om du vill skriva ut väljer du **hämta** och öppnar sedan den hämtade filen i Excel och skriver ut därifrån.

### <a name="printer"></a><a name="Printer"></a>Skrivare

Fältet **Skrivare** på förfrågningssidan visar namnet på skrivaren som rapporten skickas till. Om du vill ändra en skrivare markerar du bara skrivaren i listan.

> [!NOTE]
> **(Hanteras av webbläsaren)** anger att rapporten inte har tilldelats någon skrivare. I så fall hanterar webbläsaren utskriften och visar en standardupplevelse där du kan välja en lokal skrivare som är ansluten till enheten. **(Hanteras av webbläsaren)** är inte tillgängligt i [!INCLUDE[prod_short](includes/prod_short.md)] mobilappen eller appen för Microsoft Teams.

> [!TIP]
> Skrivaren som är markerad för dig som standard är inställd på sidan **Skrivarval**. Information om hur du ändrar standardskrivaren finns i [Så här väljer du vilka skrivare som skriver ut vilka rapporter](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Skriva ut rapporter på thailändska

För den thailändska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] kan knappen **Skriv ut** inte skriva ut rapporter på rätt sätt på grund av begränsningar i tjänsten som genererar den utskrivbara PDF-filen. I stället kan du öppna rapporten i Word och spara den som utskrivbar PDF.  

Du kan också be administratören att skapa en layout för en Word-rapport för de mest använda rapporterna. Mer information finns i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Växla rapportlayouten

En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Om du vill växla till en annan layout, se [Ange layout för en rapport](ui-set-report-layout.md). Om du vill anpassa rapportens layout, se [Kom igång med att skapa layouter](ui-get-started-layouts.md).

## <a name="advanced-options"></a>Avancerade alternativ

Fälten under **Avancerat** anger begränsningar för den genererade rapporten för att kontrollera skrivarresurserna. Du behöver normalt inte ändra inställningarna om du inte har en stor rapport. Om en rapport överstiger dessa begränsningar när du försöker förhandsgranska eller skriva ut, visas ett meddelande om vilken begränsning som har överskridits. Du kan sedan ändra inställningarna så att de passar din rapport. Varje fält har dock ett maximalt värde som du bör känna till:

|Fält|Maximivärde|
|-----|-------------|
|Maximal återgivningstid|12:00:00|
|Maximalt antal rader|1 000 000|
|Maximalt antal dokument|500|

> [!NOTE]
> De högsta värdena kan vara olika för lokala [!INCLUDE[prod_short](includes/prod_short.md)] och en administratör kan ändra dem. Mer information finns i [Konfigurera Business Central Server – Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). En översikt över rapporteringsbegränsningar [!INCLUDE[prod_short](includes/prod_short.md)] online finns i [Operativa gränser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Se även

[Ställa in skrivare](ui-specify-printer-selection-reports.md)  
[Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]