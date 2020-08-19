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
ms.date: 06/10/2020
ms.author: sgroespe
ms.openlocfilehash: 11c3fa284a457db1de272a3d92ebc7fc873ad933
ms.sourcegitcommit: 99cecd005f8ede70e9a3d163a457fcb9aadb6843
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/10/2020
ms.locfileid: "3549898"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeta med rapporter och batch-jobb och XML-portar

En rapport samlar in information som baseras på en viss uppsättning villkor och ordnar och visar informationen i ett format som är lätt att läsa och kan skrivas ut och sparas som en fil. Det finns flera rapporter som du kan använda i hela programmet. Rapporterna innehåller vanligtvis information i förhållande till kontexten på den aktuella sidan. Till exempel sidan **kund** innehåller rapporter för de 10 främsta kunderna och fönstret försäljningsstatistik.

Batchjobb och XMLports gör mer eller mindre detsamma som rapporter, men i syfte att utföra en process eller exportera data. Till exempel batch-jobbet **skapa betalningspåminnelser** skapar påminnelsedokument för kunder med förfallna betalningar.  

> [!NOTE]
> Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb och XMLports.

Rapporter finns i liken **Rapporter** på valda sidor. Du kan också använda sökfunktionen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") för att hitta rapporter efter namn.

## <a name="specifying-the-data-to-include-in-reports"></a>Ange data att inkludera i rapporter
När du öppnar en rapport visas vanligtvis en sidan för förfrågan om batch-jobb, eller XMLport där du kan ange olika alternativ och filter som avgör vad som inkluderas i rapporten.

Du kan ange att filter ska vara mer eller mindre på samma sätt som du anger filter för listor. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Avsnittet **Filtrera lista efter** på sidan för begäran innehåller en allmän filtreringsfunktion för rapporter. Dessa filter är valfria.
>
> Vissa rapporter ignorerar dessa filter, vilket innebär att oavsett vilka filter som anges i avsnittet **Filtrera lista efter** är rapportens resultat detsamma. Det går inte att skapa en lista vars fält ignoreras i vilka rapporter, så du måste experimentera med filtren om du använder dem.
>
> **Exempel**: när du använder batch-jobbet **Skapa betalningspåminnelser**, ett filter för fältet **Kundreskontratransaktioner** i **Senast utskickad bet.påm.nivå** kommer att ignoreras eftersom filter är fasta för det batch-jobbet.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Använda sparade inställningar
Sidan för begäran kan innehålla avsnittet **sparade inställningar** som innehåller en eller flera poster i rutan **Använd standardvärde från**. En sparad inställning är i princip en förinställd grupp inställningar och filter som du kan tillämpa på rapporten innan du förhandsgranskar eller skickar rapporten till en fil. Posten vid namn **Senast använda alternativ och filter** med sparade inställningar är alltid tillgänglig. Den här posten anger rapporten till att använda alternativ och filter som användes när du använde rapporten.

Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data. När du har angett rutan **Använd standardvärde från** till en sparad inställning kan du ändrar valfria alternativ och filter innan du förhandsgranskar eller sparar rapporten. Utförda ändringar sparas inte i de post för sparad ändring som du valde, utan sparas i stället i transaktionen **Senast använda alternativ och filter**.

>[!NOTE]
>Om du innehar administratörsrättigheter kan du skapa och hantera sparade rapportinställningar för samtliga användare. Mer information finns i [Hantera sparade inställningar i rapporter och batch-jobb](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Förhandsgranska en rapport

Tryck på knappen **Förhandsgranska** för att visa rapporten på sidan för rapportförfrågan. Använd menyraden i förhandsgranskningen av rapporten när du vill:

- Flytta mellan sidor
- Zooma in och ut
- Ändra storlek så att den passar sidan
- Välj text

    Du kan kopiera text från en rapport och sedan klistra in den någon annanstans, som en sida i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Med hjälp av musen kan du till exempel trycka och hålla där du vill börja och flyttar sedan musen för att markera ett eller flera ord, meningar eller stycken. Du kan sedan trycka på höger musknapp och välja **Kopiera**. Du kan klistra in den markerade texten där du vill.
- Panorera dokumentet

    Du kan flytta den synliga delen av rapporten i någon riktning så att du kan se andra områden eller rapporten. Detta är användbart när du har zoomat in för att visa detaljerad information.  Med hjälp av musen kan du till exempel trycka och hålla musknappen var som helst i rapportens förhandsgranskning och sedan flytta musen.

- Hämta till en PDF-fil på datorn eller i nätverket.
- Skriv ut

## <a name="saving-a-report"></a>Spara rapporten
Du kan spara en rapport i ett PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument genom att välja knappen **skicka till**, och sedan göra ditt val.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Schemalägga en rapportkörning

Du kan schemalägga eller köra batch-jobb för rapport att köras vid ett visst datum och tider. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **schema** när du har valt knappen **skicka till** och sedan skriver du in information om t.ex. skrivare, tid och datum. Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten. När rapporten behandlas tas artikeln bort från jobbkön. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

När du schemalägger en rapport som ska köras kan du ange att den måste köras varje torsdag genom att ställa in fältet **Datumformel för nästa körning** till *D4*. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan välja att spara den behandlade rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara behandlar rapporten. Om du väljer att spara rapporten som en fil skickas den bearbetade rapporten till området **Rapportinkorg** i ditt Rollcenter, där du kan visa den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skriva ut en rapport

Du skriver ut en rapport genom att trycka på knappen **Skriv ut** på sidan för rapportförfrågan eller på menyraden på sidan **Förhandsgranska**.

### <a name="printer-selection"></a>Skrivarval

Rapporten skrivs ut från den skrivare som visas i fältet **Vald skrivare** på sidan för rapportförfrågan. Du kan inte ändra skrivare från den här sidan.

Den valda skrivaren anges antingen på sidan **Skrivarval** eller så är det standardskrivaren som anges på sidan **Skrivarhantering**. Om du vill använda en annan skrivare läser du [Konfigurera skrivare](ui-specify-printer-selection-reports.md).

Om ingen skrivare anges på sidan **Skrivarval** eller om du anger standardskrivare på sidan **Skrivarhantering** används funktionen webbläsarutskrift. I det här fallet visas **Webbläsare** i fältet **Vald skrivare** på sidan för rapportförfrågan. 

### <a name="browser-printing"></a>Webbläsarutskrift

Eftersom [!INCLUDE[prodshort](includes/prodshort.md)] är en molntjänst kan den inte nå lokala skrivare som är anslutna till din dator. Den kan emellertid ansluta till molnbaserade skrivare. I den generiska versionen av [!INCLUDE[prodshort](includes/prodshort.md)] har en molnskrivare med namnet **E-postskrivare** installerats som ett tillägg och är klar att användas efter den ursprungliga installationen.

Om en molnskrivare inte har installerats eller konfigurerats, eller om en installerad skrivare havererar, kommer utskriften att ske via webbläsarens standardalternativ för utskrift.

> [!NOTE]
> Alternativen för webbläsarutskrift fungerar oberoende av [!INCLUDE[prodshort](includes/prodshort.md)]. Så skrivarinställningar som kan ha skapats från skrivare i [!INCLUDE[prodshort](includes/prodshort.md)] överförs inte till alternativen för webbläsarutskrift.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Skriva ut rapporter på thailändska
För den thailändska versionen av [!INCLUDE[prodshort](includes/prodshort.md)] kan knappen **Skriv ut** inte skriva ut rapporter på rätt sätt på grund av begränsningar i tjänsten som genererar den utskrivbara PDF-filen. I stället kan du öppna rapporten i Word och spara den som utskrivbar PDF.  

Du kan också be administratören att skapa en layout för en Word-rapport för de mest använda rapporterna. Mer information finns i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ändra rapportlayouter
En rapportlayout styr vad som ska visas i en rapport, hur den ordnas och hur den är formaterad. Om du vill växla till en annan layout, se [Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md). Om du vill anpassa rapportens layout, se [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se även

[Ställa in skrivare](ui-specify-printer-selection-reports.md)  
[Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
