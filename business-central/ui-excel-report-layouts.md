---
title: Arbeta med Excel-layouter
description: Lär dig skapa och ändra rapportmallar som har skapats med Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 05/30/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="working-with-microsoft-excel-layouts"></a>Arbeta med Microsoft Excel-layouter

Microsoft Excel-rapportlayouter baseras på Excel-arbetsböcker (.xlsx-filer). Med dem kan du skapa rapporter som innehåller välbekanta Excel-funktioner för sammanfattning, analys och presentation av data som formler, PivotTables och PivotCharts.

![Visar ett exempel på en Excel-layout.](media/excel-layout-2.png)

I den här artikeln beskrivs några av de viktigaste sakerna du behöver veta för att komma igång med Excel-layouter.

## <a name="why-use-excel-layouts"></a>Varför använda Excel-layouter?

Fördelar med att använda Excel-layouter:

- Skapa interaktiva rapporter med hjälp av visualiseringar som utsnitt.
- Visa rådata från rapportdatauppsättningen, vilket hjälper dig att förstå hur rapporten fungerar och var data i visuella objekt kommer från.
- Använd de inbyggda Microsoft Office-funktionerna för att utföra efterbehandling i återgivna rapporter, t.ex.:
  - [Skydda kalkylbladen](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Använda känslighetsetiketter](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Lägga till kommentarer och anteckningar](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognoser och analyser](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Använd installerade tillägg och programintegrationer som Power Automate-flöden eller OneDrive.

> [!TIP]
> När OneDrive-integrationsinställningar, när du kör en rapport med en Excel-layout, kopieras Excel-arbetsboksfilen till OneDrive och sedan öppnas i Excel Online. Mer information finns i [Spara Excel-arbetsböcker och rapportfiler i OneDrive](./across-onedrive-overview.md#save-excel-workbooks-and-report-files-in-onedrive)

## <a name="get-started"></a>Kom i gång

Det finns huvudsakligen två uppgifter som du behöver för att skapa en Excel-layout i en rapport:

1. Skapa den nya Excel-layoutfilen.
2. Lägg till den nya i rapporten.

## <a name="task-1-create-the-excel-layout-file"></a>Uppgift 1: Skapa den nya Excel-layoutfilen

Det finns tre sätt att skapa en Excel-layoutfil för en rapport.

### [Från alla rapporter](#tab/any-report)

Följ dessa steg om du vill skapa en Excel-layout från en rapport, oavsett vilken typ av layout som används. Excel-layouten innehåller det **data** blad och den tabell som krävs ett **rapportmetadata** blad och inget annat.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. På sidan **Rapportlayouter** väljer du en layout för rapporten och väljer sedan åtgärden **Kör rapport**.
3. På sidan för rapportförfrågan väljer du **Skicka till** > **Microsoft Excel-dokument (endast data)** > **OK**.

   I det här steget hämtas en Excel-arbetsbok som innehåller rapport datauppsättningen.
4. Öppna den nedladdade filen i Excel, gör ändringar och spara sedan filen.

### [Från en annan Excel-rapportlayout](#tab/other-layout)

Om det redan finns en Excel-layout för en rapport kan du använda den befintliga layouten som utgångspunkt. Det finns två tillvägagångssätt för att få en kopia av layouten. Du kan antingen exportera den befintliga layouten från sidan **Rapportlayout** eller hämta layouten från sidan för rapportens förfrågan. Du kan hämta en Excel-layouttabell som innehåller alla blad i den befintliga filen på båda sätten. Skillnaden är att när du laddar ner den från begärandesidan inkluderar layouten faktiska data. (Data krävs inte, men det är enklare att designa dem.)

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Metod 1: exportera layouten från sidan **rapportlayout**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Välj Excel-layouten i listan och välj sedan åtgärden **exportera layout** högst upp på sidan.
3. Öppna filen i Excel, gör ändringar och spara sedan filen.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Metod 2: Hämta layouten från rapportens förfrågan sida

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. På sidan **Rapportlayouter** väljer du en layout för rapporten och väljer sedan åtgärden **Kör rapport**.
3. Välj på sidan för rapportbegäran **Ladda ned**.
4. Öppna filen i Excel, gör ändringar och spara sedan filen.

### [Från AI-kod](#tab/from-code)

Det här är den mest avancerade metoden för att skapa en layout för en Excel-rapport. Eftersom det kräver kunskap om AL-kod riktas den mot programmerare. Med den här metoden är Excel-layouterna del av ett tilläggspaket som du installerar. Läs mer på [Skapa en Excel-layoutrapport](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) i hjälpen för utvecklare och IT-proffs.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Uppgift 2: Lägg till Excel-layouten i rapporten

När du väl har Excel-layoutfilen är nästa uppgift att lägga till den som en ny layout för rapporten.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Välj **Ny layout**.
3. Ställ in **Rapport-ID** till *Rapport*.
4. Ange ett namn i **Layoutnamn**.
5. Ange **formatalternativ** för **Excel**.
6. Välj **OK**, gör sedan ett av följande steg för att ladda upp layoutfilen för rapporten:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Den valda filen överförs till layouten så öppnas sidan **Rapportlayout**.
8. För att se hur rapporten ser ut i den nya layouten väljer du layouten från listan och väljer sedan **Kör rapport**.

<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet must include a table named **Data**.

**Data** table
  - The **Data** sheet must include a table named **Data**.
  - The table must have at least one column and can only include columns that are also in the report dataset.
  - The table must start in the first cell **A1** of the **Data** sheet.

3. Report metadata 
-->

## <a name="understanding-excel-layouts"></a>Förstå Excel-layouter

Det finns några saker som du behöver veta eller överväga när du skapar eller gör ändringar i Excel-layouter. Alla Excel-layouter måste innehålla två element: ett **datablad** och en **data**-tabell. Dessa element bygger på layouten genom att definiera affärsdata från Business Central som du kan arbeta med. Du kan betrakta **data**-bladet som ett slags kontrakt mellan layouten i affärsdata. Du ska använda dessa data som källa för de beräkningar och visuella effekter som du vill presentera i andra blad.

Det finns vissa specifika krav på strukturen i Excel-arbetsboken. Om kraven inte uppfylls får du problem med att använda layouten. Följande diagram och tabell beskriver elementen i en Excel-layout och kraven.

[![Visar de olika elementen i en Excel-layout.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nr.|Element|Description|Obligatoriskt|
|---|-------|----|---|
|1|**Data** blad|<ul><li>Måste ha namnet **Data**.</li><li>Kan endast inkludera en tabell, som måste ha namnet **Data**.</li></ul>|![Är nödvändigt](media/check.png) | 
|2|**Data** tabell|<ul><li>Måste ha namnet **Data**.</li><li>Det måste finnas minst en kolumn.</li><li>Det går bara att ta med kolumner som finns i rapport datauppsättningen.</li><li>Måste börja i första cell **A1** av **Data**-bladet.</li></ul>|![Är nödvändigt](media/check.png)|
|3|Presentationsblad|<ul><li>Används för att presentera data.</li><li>Data hämtas från **data** bladet. </li></ul>||
|4|**Rapportmetadata** blad|<ul><li>Tas automatiskt med om layouten skapades genom export av en annan Excel-rapport.</li><li>Innehåller allmän information om rapporten.</li><li>Kan tas bort.</li></ul>|

Sammanfattningsvis är detta vad du bör och inte bör göra **data**-bladet:

- Ändra inte namnet på **data** bladet, **data** tabellen eller kolumnerna.
- Du kan ta bort eller dölja kolumner.
- Lägg inte till några kolumner om de inte är med i rapport datauppsättningen.
- Du kan placera bladen i valfri ordning med **data**-bladet först eller sist.

## <a name="see-also"></a>Se även
[Skapa en Excel-layoutrapport (utvecklardokumentation)](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout?toc=/dynamics365/business-central/toc.json)  
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout (äldre)](ui-how-import-and-export-report-layout.md)  
[Analysera rapportdata med Excel](report-analyze-excel.md)  
[Arbeta med rapporter](ui-work-report.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
