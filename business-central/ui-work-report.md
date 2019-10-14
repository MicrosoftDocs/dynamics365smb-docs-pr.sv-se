---
title: Schemalägga en rapport att köras vid ett visst datum och tider | Microsoft Docs
description: Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 709e444d185e6950d6367036db622b30c8062f25
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310618"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeta med rapporter och batch-jobb och XML-portar
En rapport samlar in information som baseras på en viss uppsättning villkor och ordnar och visar informationen i ett format som är lätt att läsa och kan skrivas ut och sparas som en fil. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

Batchjobb och XMLports gör mer eller mindre detsamma som rapporter, men i syfte att utföra en process eller exportera data. Till exempel batch-jobbet **skapa betalningspåminnelser** skapar påminnelsedokument för kunder med förfallna betalningar.  

> [!NOTE]
> Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb och XMLports.

Rapporter finns i fältet **rapporter** på markerade sidor eller du kan använda sökning ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") för att hitta rapporter efter namn.

## <a name="specifying-the-data-to-include-in-reports"></a>Ange data att inkludera i rapporter
När du öppnar en rapport visas vanligtvis en sidan för förfrågan om batch-jobb, eller XMLport där du kan ange olika alternativ och filter som avgör vad som inkluderas i rapporten.

Du kan ange att filter ska vara mer eller mindre på samma sätt som du anger filter för listor. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#-filtering).

> [!Caution]
> Avsnittet **Filtrera lista efter** på sidan för begäran innehåller en allmän filtreringsfunktion för rapporter. Dessa filter är valfria.<br /><br /> Vissa rapporter ignorerar dessa filter, vilket innebär att oavsett vilka filter som anges i avsnittet **Filtrera lista efter** är rapportens resultat detsamma. Det går inte att skapa en lista vars fält ignoreras i vilka rapporter, så du måste experimentera med filtren om du använder dem.<br /><br />
**Exempel**: när du använder batch-jobbet **Skapa betalningspåminnelser**, ett filter för fältet **Kundreskontratransaktioner** i **Senast utskickad bet.påm.nivå** kommer att ignoreras eftersom filter är fasta för det batch-jobbet.

## <a name="SavedSettings"></a>Använda sparade inställningar
Sidan för begäran kan innehålla avsnittet **sparade inställningar** som innehåller en eller flera poster i rutan **Använd standardvärde från**. En sparad inställning är i princip en förinställd grupp inställningar och filter som du kan tillämpa på rapporten innan du förhandsgranskar eller skickar rapporten till en fil. Posten vid namn **Senast använda alternativ och filter** med sparade inställningar är alltid tillgänglig. Den här posten anger rapporten till att använda alternativ och filter som användes när du använde rapporten.

Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data. När du har angett rutan **Använd standardvärde från** till en sparad inställning kan du ändrar valfria alternativ och filter innan du förhandsgranskar eller sparar rapporten. Utförda ändringar sparas inte i de post för sparad ändring som du valde, utan sparas i stället i transaktionen **Senast använda alternativ och filter**.

>[!NOTE]
>Om du innehar administratörsrättigheter kan du skapa och hantera sparade rapportinställningar för samtliga användare. Mer information finns i [Hantera sparade inställningar i rapporter och batch-jobb](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Förhandsgranska en rapport
Välj knappen **förhandsgranska** om du vill visa rapporten. Använd menyraden i förhandsgranskningen av rapporten när du vill:

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
Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument genom att välja knappen **skicka till**, och sedan göra ditt val.

## <a name="ScheduleReport"></a> Schemalägga en rapportkörning
Du kan schemalägga eller köra batch-jobb för rapport att köras vid ett visst datum och tider. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **schema** när du har valt knappen **skicka till** och sedan skriver du in information om t.ex. skrivare, tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

Du kan välja att spara den behandlade rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara behandlar rapporten. Om du väljer att spara rapporten som en fil skickas den bearbetade rapporten till området **Rapportinkorg** i ditt Rollcenter, där du kan visa den.

## <a name="PrintReport"></a>Skriva ut en rapport
Du kan skriva ut en rapport från knappen **Utskrift** på alternativsidan som visas när du öppnar rapporten eller på menyraden i förhandsgranskningen.  

### <a name="printing-reports-in-thai"></a>Skriva ut rapporter på thailändska
För den thailändska versionen av [!INCLUDE[prodshort](includes/prodshort.md)] kan knappen **utskrift** inte skriva ut rapporter på rätt sätt på grund av begränsningar i tjänsten som genererar den utskrivbara PDF-filen. I stället kan du öppna rapporten i Word och spara den som utskrivbar PDF.  

Du kan också be administratören att skapa en layout för en Word-rapport för de mest använda rapporterna. Mer information finns i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ändra rapportlayouter
En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Om du vill växla till en annan layout, se [Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md). Om du vill anpassa rapportens layout, se [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se även
[Ange skrivarval för rapporter](ui-specify-printer-selection-reports.md)  
[Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
