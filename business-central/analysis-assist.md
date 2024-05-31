---
title: Analysera data i listor med hjälp av Copilot (förhandsversion)
description: Lär dig hur du använder Copilot i Business Central för att analysera data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Analysera data i listor med hjälp av Copilot (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

I den här artikeln beskriver vi hur du använder *analyshjälp* när du analyserar data på listsidor.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Om analyshjälp

Analysassistenten är en Copilot för [analysläget](analysis-mode.md) på listsidor i Business Central. Analysläget ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. Om du vill analysera data i analysläget skapar du fliken *analysflik* där du transformerar data för att visa önskade aggregeringar och sammanfattningar. Du kan till exempel ordna fält i rader och kolumner, ange filter, sortera kolumner och pivotera efter fält. Med analyshjälp, istället för att göra denna uppgift manuellt, uppnår du mycket av samma&mdash;eller åtminstone som en början&mdash;genom att använda ord. Genom att uttrycka den struktur du vill ha på naturligt språk, som "sortera på kvantitet från minsta till största" eller "visa genomsnittlig kostnad per kategori", använder analyshjälp AI för att generera ett förslag till layout på en analysflik.


<!-- 

 However, the data analysis mode requires some understanding of how to structure fields to meet the desired aggregations and summarizations. It requires you to move fields around to the appropriate areas within analysis mode pane which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals. Analysis assist minimizes these requirments by enabling you to express the desired layout in words. , like "group which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals
--> 
## Förutsättningar

- Funktionen analyshjälp är aktiverad och du får behörighet att använda den. Den uppgiften är vanligtvis av en administratör. [Läs mer om att konfigurera Copilot och AI-funktioner](enable-ai.md).
- Visningsspråket i Business Central är inställt på något av följande engelska språk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Läs mer om hur du ändrar språk](ui-change-basic-settings.md#language).
- Din Business Central-miljö finns i alla länder/regioner utom Kanada (den här funktionen är ännu inte tillgänglig i Kanada).

<!--
> [!NOTE]
> You may notice some list pages that don't include the **Analyze** switch for changing to the analysis mode. The reason is that developers can disable analysis mode on specific pages by using the [AnalysisModeEnabled property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL.-->

## Kom i gång

1. Öppna listsidan du vill analysera.

   Om du t.ex. vill arbeta med sidan **Artiklar** markerar du ![Förstoringsglas som öppnar funktionen Berätta.](media/ui-search/search_small.png) ikon (<kbd>Alt</kbd>+<kbd>Q</kbd>), ange *artiklar* och väljer sedan relaterad länk.

1. Du kan börja analysera data med Copilot direkt från listsidan eller genom att först gå in i analysläget. Gör något av följande för att komma igång:

    - I åtgärdsfältet högst upp på sidan väljer du ![Visar copilot-ikonen](media/copilot-icon.png) **Copilot** > **Analysera lista**.
    - I åtgärdsfältet högst upp på sidan väljer du ![Visar ikonen för ange analysläge](media/analysis-mode-icon.png) **Gå in i analysläge**, sedan ![Visar copilot-ikonen](media/copilot-icon.png) **Copilot** > **Skapa ny analys**.

1. I fönstret **Analysera** med Copilot anger du en beskrivning av den layout du vill använda. Den här beskrivningen kallas för en *prompt*.

    ![Visar analyshjälp Copilot](media/analysis-assist.png)

    > [!TIP]
    > Om du vill ha hjälp med att skriva en prompt väljer du ![Visar ikonen för visa prompt](media/prompt-guide-icon.png) **Promptguide** och väljer ett av alternativen för att komma igång. Texten inom hakparentes `[ ]` visas bara som ett exempel och ingår inte i Copilot-fönstret.

1. Välj **Generera** och vänta sedan medan Copilot genererar layouten på den nya analysfliken.
1. Granska resultaten på den nya analysfliken.

   > [!NOTE]
   > Om du navigerar bort från den nya analysfliken (som att gå till en annan analysflik eller sida) eller gör layoutändringar på fliken (som att sortera kolumner eller ändra inställningar i fliken **Kolumner** och **Analysfilter**) sparas den nya analysfliken automatiskt och Copilot stängs.

1. Om du vill ändra den genererade analysen kan du göra något av följande:

   - Om du vill bygga vidare på föregående instruktioner anger du informationen i rutan **Lägg till mer information om analysen** och väljer sedan ![Visa justeringspilen](media/analysis-assist-adjust-button.png) **Justera**. Copilot kommer ihåg dina tidigare instruktioner och använder dem för att göra justeringar.

   - För att börja från början genom att lägga till nya instruktioner, välj ![Visar pennikonen för redigeringsprompten](media/edit-pencil.png) **Redigera prompt:**, lägg till informationen i prompten och välj sedan **Generera**.

1. Om du vill spara analysflik väljer du **Behåll den**. Om du inte vill spara den väljer du **Ignorera**.

## Prompttips och exempel

Att skapa effektiva prompter för Copilot är viktigt för att få korrekta och relevanta analysförslag. Det finns också sätt att minimera text som du lägger till i prompter för att det ska gå snabbare att skriva. Här är några tips och riktlinjer följt av några exempel:

- Var kortfattad och undvik långa meningar eller flera meningar.
- Kontrollera att fältnamnen som används i prompter ligger något nära de faktiska fältnamnen på sidan.
- Använd naturligt språk, uttryck den datastruktur du vill ha på ett vänligt och konversationsmässigt sätt.
- Använd vanliga nyckelord, fraser och termer som används i dataanalys, till exempel `group by` och `sum` `sort by` så vidare.
- Om det första svaret inte är vad du vill ha lägger du till uppföljningsinstruktioner eller omformulerar den senaste instruktionen.
- Vanliga förkortningar är acceptabla.
- Brevfall är inte viktigt.

### Exempel

Dessa följande snabba exempel använder analyshjälp på listan **Artiklar**. Artikelsidan innehåller tre summerbara fält för analys: **Lagersaldo**, **Styckkostnad**, **A-pris**.

Prompt: `Show items by brand and unit of measure`

Den här prompten försöker visa summor för alla summeringsfält, grupperade efter varumärke och **Basenhet**. Men i det här fallet matchar "varumärke" inte något fältnamn, så Copilot kan förmodligen inte hitta ett matchande fält så det ber dig att omformulera prompt och försöka igen.

Prompt: `Show items by type and uom`

Denna prompt visar totaler för alla summerbara fält, grupperade efter fältet **Typ** och **Basenhet**. Men istället för att skriva ut "måttenhet" används förkortningen `uom`.

Prompt: `Show total quantity per type per UoM`

Den här prompt skapar en pivottabell i fältet **Lagersaldo** per **Basenhet** per **Typ**.

## Se även

[Ansvarig AI vanliga frågor för analyshjälp](faqs-analysis-assist.md)  
[Ad hoc-dataanalys](reports-adhoc-analysis.md)  
