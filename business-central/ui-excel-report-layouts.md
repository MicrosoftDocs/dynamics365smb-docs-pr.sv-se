---
title: Arbeta med Excel-layouter
description: Lär dig skapa och ändra rapportmallar som har skapats med Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 609678742ccf9593407e96ea412a377f37c8abf9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525225"
---
# <a name="working-with-excel-layouts"></a>Arbeta med Excel-layouter

Excel-rapportens layouter baseras på Microsoft Excel arbetsböcker (.xlsx-filer). De ger dig möjlighet att skapa rapporter med hjälp av välbekanta Excel-funktioner för sammanfattning, analys och presentation av data, som formler, PivotTables och PivotCharts.

![Visar ett exempel på en Excel-layout.](media/excel-layout-2.png)

I den här artikeln beskrivs några av de viktigaste sakerna du behöver veta för att komma igång med Excel-layouter.

## <a name="why-use-excel-layouts"></a>Varför använda Excel-layouter?

Här är några fler fördelar med att använda Excel-layouter:

- Skapa interaktiva rapporter med hjälp av visualiseringar som utsnitt
- Visa rå data från rapport datauppsättningen för att få hjälp med att förstå hur rapporten fungerar och var data i visuella objekt kommer från
- Använd de inbyggda Office-funktionerna för att utföra efter behandling i återgivna rapporter, t.ex.:
  - [Skydda kalkylbladen](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Använda känslighetsetiketter](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Lägga till kommentarer och anteckningar](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognoser och analyser](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Använd installerade tillägg och programintegrationer som Power Automate-flöden eller OneDrive.

## <a name="get-started"></a>Kom igång

Det finns huvudsakligen två uppgifter som du behöver för att skapa en Excel-layout i en rapport:

1. Skapa den nya Excel-layoutfilen.
2. Lägg till den nya i rapporten.

## <a name="task-1-create-the-excel-layout-file"></a>Uppgift 1: Skapa den nya Excel-layoutfilen

Det finns tre sätt att skapa en Excel-layoutfil för en rapport på det sätt som beskrivs i det här avsnittet

### <a name="from-any-report"></a>[Från alla rapporter](#tab/any-report)

Du kan göra på följande sätt om du vill skapa en Excel-layout från en rapport, oavsett vilken typ av layout som används. Excel-layouten innehåller det **data** blad och den tabell som krävs ett **rapportmetadata** blad och inget annat.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. I listan **Rapportlayouter** välj valfri layout för rapporten och välj sedan åtgärden **Kör rapport**.
3. På sidan för rapport förfrågan väljer du **Skicka till** > **Microsoft Excel dokument (endast data)** > **OK**.

   I det här steget hämtas en Excel-arbetsbok som innehåller rapport datauppsättningen.
4. Öppna den nedladdade filen i Excel, gör ändringar och spara sedan filen.

### <a name="from-another-excel-layout-on-a-report"></a>[Från en annan Excel-layout i en rapport](#tab/other-layout)

Om det redan finns en Excel-layout för en rapport använder du den befintliga layouten som utgångspunkt. Det finns två tillvägagångssätt för att få en kopia av layouten. Du kan exportera den befintliga layouten från sidan **rapportlayout** eller hämta layouten från sidan för rapportens förfrågan. Du kan hämta en Excel-layouttabell som innehåller alla blad i den befintliga filen på båda sätten. Skillnaden är att från begärandesidan kommer layouten att inkludera faktiska data. Data krävs inte, men det är enklare att designa dem.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Metod 1: exportera layouten från sidan **rapportlayout**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Välj Excel-layouten i listan och välj sedan åtgärden **exportera layout** högst upp på sidan.
3. Öppna filen i Excel, gör ändringar och spara sedan filen.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Metod 2: Hämta layouten från rapportens förfrågan sida

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. I listan **Rapportlayouter** välj valfri layout för rapporten och välj sedan åtgärden **Kör rapport**.
3. Välj på sidan för rapportbegäran **ladda ned**.
4. Öppna filen i Excel, gör ändringar och spara sedan filen.

### <a name="from-al-code"></a>[Från AI-kod](#tab/from-code)

Det här är den mest avancerade. Det kräver kunskap om AL-kod, så den riktar programmerare. Excel-layouterna, i det här fallet, ingår i ett tilläggspaket som du installerar. Mer information finns i [Skapa en Excel-layoutrapport](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) i hjälpen för utvecklare och IT-proffs.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Uppgift 2: Lägg till Excel-layouten i rapporten

När du väl har Excel-layoutfilen är nästa uppgift att lägga till den som en ny layout för rapporten.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Välj **Ny layout**.
3. Ange **rapport-ID** för rapport.
4. Ange ett namn i **Layoutnamn**.
5. Ange **formatalternativ** för **Excel**.
6. Välj **OK** > **Välj** för att öppna Utforskaren på enheten. 
7. Hitta och välj Excel-filen och välj sedan **Öppna**.

   Den valda filen överförs till layouten och du kommer då tillbaka till sidan **rapportlayout**.
8. Om du vill se hur rapporten ser ut med den nya layouten markerar du layouten i listan och väljer **Kör rapport**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Förstå Excel-layouter

Det finns några saker som du bör ta reda på när du börjar skapa eller göra ändringar i Excel-layouter. Alla Excel-layouter måste innehålla två element: ett **datablad** och en **data**-tabell. Dessa element bygger på layouten genom att definiera affärsdata från Business Central som du kan arbeta med. Du kan betrakta **data** bladet som ett slags kontrakt mellan layouten i affärsdata. Du ska använda dessa data som källa för de beräkningar och visuella effekter som du vill presentera i andra blad.

Det finns vissa specifika krav på strukturen i Excel-arbetsboken. Om kraven inte uppfylls får du problem med att använda layouten. Följande diagram och tabell beskriver elementen i en Excel-layout och kraven.

[![Visar de olika elementen i en Excel-layout.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nr|Element|Beskrivning|Obligatoriskt|
|---|-------|----|---|
|1|**Data** blad|<ul><li>Måste ha namnet **data**</li><li>Det går bara att ta med en tabell och tabellen måste ha namnet **data**</li></ul>|![Är nödvändigt](media/check.png) | 
|2|**Data** tabell|<ul><li>Måste ha namnet **data**</li><li>Det måste finnas minst en kolumn.</li><li>Det går bara att ta med kolumner som finns i rapport datauppsättningen.</li><li>Måste börja i första cell **A1** av **Data** blad</li></ul>|![Är nödvändigt](media/check.png)|
|3|Presentationsblad|<ul><li>Används för att presentera data.</li><li>Data hämtas från **data** bladet. </li></ul>||
|4|**Rapportmetadata** blad|<ul><li>Tas automatiskt med om layouten skapades genom export av en annan rapport som Excel</li><li>Innehåller allmän information om rapporten</li><li>Kan tas bort</li></ul>|

Så här sammanfattar du vad du kan och inte kan göra i **data** bladet:

- Ändra inte namnet på **data** bladet, **data** tabellen eller kolumnerna.
- Du kan ta bort eller dölja kolumner.
- Lägg inte till några kolumner om de inte är med i rapport datauppsättningen.
- Du kan placera bladen i valfri ordning. **Data** bladet kan till exempel vara för första eller sista.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
[Förbereda ekonomiska rapporter med kontouppställningar och kontokategorier](bi-how-work-account-schedule.md) 
[Affärsstöd](bi.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analysera rapportdata med Excel](report-analyze-excel.md).


[!INCLUDE[footer-include](includes/footer-banner.md)]