---
title: "Schemalägga en rapport att köras vid ett visst datum och tider | Microsoft Docs"
description: "Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 16c9c8c896e3517f08a7326eef88ebc646834b1a
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="working-with-reports"></a>Arbeta med rapporter
En rapport samlar in information som baseras på en viss uppsättning kriterier och ordnar och visar informationen i ett format som är lätt att läsa, och kan skrivas ut. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

Du kan visa rapporter i fliken **rapporter** på markerade sidor eller du kan använda sökning för att hitta rapporter efter namn. När du öppnar en rapport visas en sida att vi ska ange information (alternativ och filter) som du bestämmer ska ingå i rapporten. Beroende på vilken rapport anger du till exempel ett datumintervall, en viss post, till exempel en kund eller sorteringsordning. Nedan finns ett exempel:

![Rapportalternativ](media/report_options.png "Rapportalternativ")

## <a name="previewing-a-report"></a>Så här förhandsgranskar du en rapport:
Välj **Förhandsgranskning** för att visa rapporten i Internet-webbläsaren. Peka på ett område i rapporten för att visa menyraden.  

![Verktygsfält för förhandsgranskning av rapport](media/report_viewer.png "Verktygsfält för förhandsgranskning av rapport").

Använda menyraden:

-   Flytta mellan sidor
-   Zooma in och ut
-   Ändra storlek så att den passar i fönstret
-   Välj text

    Du kan kopiera text från en rapport och sedan klistra in den någon annanstans, som en sida i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Med hjälp av musen kan du till exempel trycka och hålla där du vill börja och flyttar sedan musen för att markera ett eller flera ord, meningar eller stycken. Du kan sedan trycka på höger musknapp och välja **Kopiera**. Du kan klistra in den markerade texten där du vill.
-   Panorera dokumentet

    Du kan flytta den synliga delen av rapporten i någon riktning så att du kan se andra områden eller rapporten. Detta är användbart när du har zoomat in för att visa detaljerad information.  Med hjälp av musen kan du till exempel trycka och hålla musknappen var som helst i rapportens förhandsgranskning och sedan flytta musen.

-   Hämta till en PDF-fil på datorn eller i nätverket.
-   Skriv ut


## <a name="saving-a-report"></a>Spara rapporten
Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument genom att välja **skicka till**, och sedan göra ditt val.

## <a name="ScheduleReport"></a> Schemalägga en rapportkörning
Du kan schemalägga en rapport att köras vid ett visst datum och tider. Planerade rapporter anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du kan välja att spara den behandlade rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara behandlar rapporten. Om du väljer att spara rapporten till en fil skickas den bearbetade rapporten till området **Rapportinkorg**, på din startsida där du kan visa den.

Du kan schemalägga en rapport när du öppnar en rapport. Du väljer åtgärden **schema** och sedan anger du information som t.ex. skrivare och tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Om du har sparat den bearbetade rapporten till en fil, kommer den att vara tillgänglig i området **Rapportinkorg**.

## <a name="PrintReport"></a>Skriva ut en rapport
Du kan skriva ut en rapport från knappen **Utskrift** på alternativsidan som visas när du öppnar rapporten eller på menyraden i förhandsgranskningen.

## <a name="using-saved-settings"></a>Använda sparade inställningar
En rapport kan innehålla en eller flera poster i fältet **sparade inställningar**. *Sparade inställningar* är i princip en fördefinierad uppsättning alternativ och filter som du kan använda till rapporten innan du förhandsgranskar eller skickar rapporten till en fil. Att använda sparade inställningar är ett snabbt och pålitligt sätt att konsekvent skapa rapporter som innehåller korrekta data.

Posten vid namn **Senast använda alternativ och filter** med sparade inställningar är alltid tillgänglig. Den här posten anger rapporten till att använda alternativ och filter som användes när du tittade på rapporten.

>[!NOTE]
>Som administratör kan du skapa och hantera de sparade inställningarna för rapporter för alla användare. Mer information finns i [Hantera sparade inställningar i rapporter](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Ändra layout och utseende på en rapport
En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Om du vill växla till en annan layout kan du se [så här: ändra vilken layout som för närvarande används i en rapport](ui-how-change-layout-currently-used-report.md). Om du vill anpassa rapportens layout se [så här: skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se även
[Ange skrivarval för rapporter](ui-specify-printer-selection-reports.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

