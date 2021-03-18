---
title: Schemalägga en rapport att köras vid ett visst datum och tider | Microsoft Docs
description: Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 7fe5d0870cfc18ab103dc57044fd0ba84b151662
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392454"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeta med rapporter och batch-jobb och XML-portar

En rapport samlar in information som baseras på en viss uppsättning villkor och ordnar och visar informationen i ett format som är lätt att läsa och kan skrivas ut och sparas som en fil. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

Batchjobb och XMLports gör mer eller mindre detsamma som rapporter, men i syfte att utföra en process eller exportera data. Till exempel batch-jobbet **skapa betalningspåminnelser** skapar påminnelsedokument för kunder med förfallna betalningar.  

> [!NOTE]
> Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb och XMLports.

## <a name="getting-started"></a>Kom i gång

Rapporter finns i liken **Rapporter** på valda sidor. Du kan också använda sökfunktionen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") för att hitta rapporter efter namn.

När du öppnar en rapport visas vanligtvis en sidan för förfrågan om batch-jobb, eller XMLport där du kan ange olika alternativ och filter som avgör vad som inkluderas i rapporten. I följande avsnitt förklaras hur du använder sidan för begäran för att bygga, förhandsgranska och skriva ut en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Använda standardvärden – fördefinierade inställningar 

De flesta förfrågningssidor innehåller fältet **Använd standardvärden från**. I det här fältet kan du välja fördefinierade inställningar för rapporten, som automatiskt anger alternativ och filter för rapporten. Välj en post i listrutan så ändras alternativen och filtren på förfrågningssidan därefter.

Posten vid namn **Senast använda alternativ och filter** är alltid tillgänglig. Den här posten anger att rapporten ska använda alternativ och filter som användes förra gången du körde rapporten.

Fältet **Använd standardvärden från** är ett snabbt och tillförlitligt sätt att skapa rapporter som innehåller rätt data. När du har valt en post kan du ändra alternativen och filtren innan du förhandsgranskar eller skriver ut rapporten. Utförda ändringar sparas inte i den post med fördefinierade inställningar som du valde, men de sparas i posten **Senast använda alternativ och filter**.

>[!NOTE]
> De fördefinierade inställningarna ställs in och hanteras vanligtvis av en administratör. Mer information finns i [Hantera sparade inställningar i rapporter och batch-jobb](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Ange data att inkludera i rapporter

Använd fälten under **Alternativ** och **Filter** om du vill ändra begränsningen av den information som du vill ha i rapporten. Du kan ange att filter ska vara mer eller mindre på samma sätt som du anger filter för listor. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Avsnittet **Filtrera lista efter** på sidan för begäran innehåller en allmän filtreringsfunktion för rapporter. Dessa filter är valfria.
>
> Vissa rapporter ignorerar dessa filter, vilket innebär att oavsett vilka filter som anges i avsnittet **Filtrera lista efter** är rapportens resultat detsamma. Det går inte att skapa en lista vars fält ignoreras i vilka rapporter, så du måste experimentera med filtren om du använder dem.
>
> **Exempel**: när du använder batch-jobbet **Skapa betalningspåminnelser**, ett filter för fältet **Kundreskontratransaktioner** i **Senast utskickad bet.påm.nivå** kommer att ignoreras eftersom filter är fasta för det batch-jobbet.

## <a name="previewing-a-report"></a>Förhandsgranska en rapport

När du förhandsgranskar en rapport kan du se hur rapporten kommer att se ut innan du skriver ut den. I förhandsgranskningen visas rapporten i [skrivaren](#Printer) som visas i fältet **Skrivare** på förfrågningssidan. När du har förhandsgranskat kan du gå tillbaka till förfrågningssidan och ändra alternativ och filter efter behov.

Om du vill förhandsgranska en rapport väljer du knappen **Förhandsgranska** eller **Förhandsgranska & stäng** på sidan för rapportförfrågan. Vilken knapp som visas beror på rapporten, så vissa rapporter har knappen **Förhandsgranska**, medan andra har knappen **Förhandsgranska & stäng**. Båda knapparna öppnar en förhandsgranskning av rapporten. Skillnaden är att **Förhandsgranska** håller förfrågningssidan öppen, så att du kan gå tillbaka till den, göra ändringar, förhandsgranska igen eller skriva ut den. Med **Förhandsgranska & stäng** stängs förfrågningssidan, så du måste öppna rapporten igen för att göra ändringar eller skriva ut.

> [!NOTE]
> Om du använder Business Central från utgivningscykel 1 år 2020 eller tidigare visas endast knappen **Förhandsgranska**, som stänger förfrågningssidan vid förhandsgranskning, som beskrivs för **Förhandsgranska & stäng**.

### <a name="working-with-the-preview"></a>Arbeta med förhandsgranskning

I förhandsgranskningen använder du menyraden i förhandsgranskningen av rapporten när du vill:

- Flytta mellan sidor
- Zooma in och ut
- Ändra storlek så att den passar sidan
- Välj text

    Du kan kopiera text från en rapport och sedan klistra in den någon annanstans, som en sida i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word.  Med hjälp av musen kan du till exempel trycka och hålla där du vill börja och flyttar sedan musen för att markera ett eller flera ord, meningar eller stycken. Tryck på höger musknapp och välj **Kopiera**. Klistra sedan in den markerade texten där du vill.
- Panorera dokumentet

    Du kan flytta den synliga delen av rapporten i någon riktning så att du kan se andra områden eller rapporten. Panorering är användbart när du har zoomat in för att visa detaljerad information.  Med hjälp av musen kan du till exempel trycka och hålla musknappen var som helst i rapportens förhandsgranskning och sedan flytta musen.

- Hämta till en PDF-fil på datorn eller i nätverket.
- Skriv ut

## <a name="saving-a-report"></a>Spara rapporten

Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument genom att välja knappen **skicka till**, och sedan göra ditt val.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Schemalägga en rapportkörning

Du kan schemalägga eller köra batch-jobb för rapport att köras vid ett visst datum och tider. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **schema** när du har valt knappen **skicka till** och sedan skriver du in information om t. ex. skrivare, tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

När du schemalägger en rapport som ska köras kan du ange att den måste köras varje torsdag genom att ställa in fältet **Datumformel för nästa körning** till *D4*. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan välja att spara rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara skapa rapporten. Om du väljer att spara rapporten som en fil skickas den bearbetade rapporten till området **Rapportinkorg** i ditt Rollcenter, där du kan visa den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skriva ut en rapport

Du skriver ut en rapport genom att trycka på knappen **Skriv ut** på förfrågningssidan eller på menyraden på sidan **Förhandsgranska**.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Skrivare

Fältet **Skrivare** på förfrågningssidan visar namnet på skrivaren som rapporten skickas till. **(Hanteras av webbläsaren)** anger att rapporten inte har tilldelats någon skrivare. I så fall hanterar webbläsaren utskriften och visar en standardupplevelse där du kan välja en lokal skrivare som är ansluten till enheten.

Du kan inte ändra skrivare med hjälp av fältet **Skrivare**. Om du vill byta skrivare måste du gå till någon av sidorna **Skrivarval** eller **Skrivarhantering**. Inställning av skrivare är vanligtvis administratörens uppgift. Om du vill lära dig mer läser du [Konfigurera skrivare](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Skriva ut rapporter på thailändska

För den thailändska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] kan knappen **Skriv ut** inte skriva ut rapporter på rätt sätt på grund av begränsningar i tjänsten som genererar den utskrivbara PDF-filen. I stället kan du öppna rapporten i Word och spara den som utskrivbar PDF.  

Du kan också be administratören att skapa en layout för en Word-rapport för de mest använda rapporterna. Mer information finns i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ändra rapportlayouter

En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Om du vill växla till en annan layout, se [Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md). Om du vill anpassa rapportens layout, se [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).

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