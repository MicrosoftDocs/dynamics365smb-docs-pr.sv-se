---
title: Schemalägga en rapport att köras vid ett visst datum och tider | Microsoft Docs
description: Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 65fcba3f0222b324f132115ea7f1ec53b75d983f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "921415"
---
# <a name="working-with-reports-and-batch-jobs"></a>Arbeta med rapporter och batch-jobb
En rapport samlar in information som baseras på en viss uppsättning villkor och ordnar och visar informationen i ett format som är lätt att läsa, och kan skrivas ut. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

Batchjobb gör mer eller mindre detsamma som rapporter, men i syfte att utföra en process. Till exempel batch-jobbet **skapa betalningspåminnelser** skapar påminnelsedokument för kunder med förfallna betalningar.  

> [!NOTE]
> Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb.

Rapporter finns i fältet **rapporter** på markerade sidor eller du kan använda sökning ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") för att hitta rapporter efter namn.


## <a name="specifying-the-data-to-include-in-the-report"></a>Ange data att inkludera i rapporten
När du öppnar en rapport visas vanligtvis en sida där du kan ange olika alternativ och filter som avgör vad som inkluderas i rapporten. Denna sida kallas sidan för rapportförfrågan. Sidan för rapportförfrågan låter dig exempelvis skapa en rapport för en specifik kund, ett specifikt datumintervall, samt att sortera informationsordningen i rapporten. Här följer ett exempel på en sida för rapportförfrågan:

![Rapportalternativ](media/report_options.png "Rapportalternativ")

> [!Caution]
> Avsnittet **visa resultat** på sidan för begäran innehåller en allmän filtreringsfunktion för rapporter. Dessa filter är valfria.<br /><br /> Vissa rapporter ignorerar dessa filter, vilket innebär att oavsett vilka filter som anges i avsnittet **visa resultat** är rapportens resultat detsamma. Det går inte att skapa en lista vars fält ignoreras i vilka rapporter, så du måste experimentera med filtren om du använder dem.<br /><br />
**Exempel**: när du använder batch-jobbet **Skapa betalningspåminnelser**, ett filter för fältet **Kundreskontratransaktioner** i **Senast utskickad bet.påm.nivå** kommer att ignoreras eftersom filter är fasta för det batch-jobbet.

### <a name="SavedSettings"></a>Använda sparade inställningar
Beroende på hur vissa rapporter utformas kan rapportsidan komma att inkludera avsnittet **Sparade inställningar** som innehåller en eller flera poster i rutan **Använd standardvärde från**. Posterna i denna ruta kallas *sparade inställningar*. En sparad inställning är i princip en förinställd grupp inställningar och filter som du kan tillämpa på rapporten innan du förhandsgranskar eller skickar rapporten till en fil. Posten vid namn **Senast använda alternativ och filter** med sparade inställningar är alltid tillgänglig. Den här posten anger rapporten till att använda alternativ och filter som användes när du tittade på rapporten.

Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data. När du har angett rutan **Använd standardvärde från** till en sparad inställning kan du ändrar valfria alternativ och filter innan du förhandsgranskar eller sparar rapporten. Utförda ändringar sparas inte i de post för sparad ändring som du valde, utan sparas i stället i **Senast använda alternativ och filter**.

>[!NOTE]
>Om du innehar administratörsrättigheter kan du skapa och hantera sparade rapportinställningar för samtliga användare. Mer information finns i [Hantera sparade inställningar i rapporter](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Ange alternativ och filter
Om du ytterligare vill begränsa eller exakt ange den data som ska ingå i rapporten kan du ange ytterligare alternativ och filter.

Filter låter dig visa data baserat på specifika kriterier. Filter grupperas efter den entitet de tillhör, exempelvis **Kund** i ovanstående illustration. Du anger ett filter genom att ange rutan **Där** som det fält du vill tillämpa filtret på och sedan lägga till kriteriet i rutan **är:**.

Du kan lägga till fler filter genom att fylla i rutorna **Och** och **Är** rutor. När du har mer än ett filter kommer endast de resultat som matchar kriterierna för samtliga filter att inkluderas i rapporten.

Beroende på den typ av fält som du filtrerar kan du ange att filterkriterierna ska söka efter en exakt matchning, en delmatchning, ett värdeintervall med mera. För information om hur du ställer in filter, se:
-   [Filtrering](ui-enter-criteria-filters.md#FilterCriteria)
-   [Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Förhandsgranska en rapport
Välj **Förhandsgranskning** för att visa rapporten i Internet-webbläsaren. Peka på ett område i rapporten för att visa menyraden.  

![Verktygsfält för förhandsgranskning av rapport](media/report_viewer.png "Verktygsfält för förhandsgranskning av rapport").

Använda menyraden:

-   Flytta mellan sidor
-   Zooma in och ut
-   Ändra storlek så att den passar sidan
-   Välj text

    Du kan kopiera text från en rapport och sedan klistra in den någon annanstans, som en sida i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Med hjälp av musen kan du till exempel trycka och hålla där du vill börja och flyttar sedan musen för att markera ett eller flera ord, meningar eller stycken. Du kan sedan trycka på höger musknapp och välja **Kopiera**. Du kan klistra in den markerade texten där du vill.
-   Panorera dokumentet

    Du kan flytta den synliga delen av rapporten i någon riktning så att du kan se andra områden eller rapporten. Detta är användbart när du har zoomat in för att visa detaljerad information.  Med hjälp av musen kan du till exempel trycka och hålla musknappen var som helst i rapportens förhandsgranskning och sedan flytta musen.

-   Hämta till en PDF-fil på datorn eller i nätverket.
-   Skriv ut


## <a name="saving-a-report"></a>Spara rapporten
Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument genom att välja **skicka till**, och sedan göra ditt val.

## <a name="ScheduleReport"></a> Schemalägga en rapportkörning
Du kan schemalägga en rapport att köras vid ett visst datum och tider. Planerade rapporter anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du kan välja att spara den behandlade rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara behandlar rapporten. Om du väljer att spara rapporten som en fil skickas den bearbetade rapporten till området **Rapportinkorg** i ditt Rollcenter, där du kan visa den.

Du kan schemalägga en rapport när du öppnar en rapport. Du väljer åtgärden **schema** och sedan anger du information som t.ex. skrivare och tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Om du har sparat den bearbetade rapporten till en fil, kommer den att vara tillgänglig i området **Rapportinkorg**.

## <a name="PrintReport"></a>Skriva ut en rapport
Du kan skriva ut en rapport från knappen **Utskrift** på alternativsidan som visas när du öppnar rapporten eller på menyraden i förhandsgranskningen.

## <a name="changing-the-layout-and-look-of-a-report"></a>Ändra layout och utseende på en rapport
En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Om du vill växla till en annan layout, se [Ändra vilken layout som för närvarande används i en rapport](ui-how-change-layout-currently-used-report.md). Om du vill anpassa rapportens layout, se [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se även
[Ange skrivarval för rapporter](ui-specify-printer-selection-reports.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
