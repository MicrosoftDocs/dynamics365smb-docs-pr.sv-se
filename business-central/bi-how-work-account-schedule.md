---
title: Skapa ekonomiska rapporter med ekonomiska data och kontokategorier
description: Beskriver hur du kan använda ekonomiska rapporter för att skapa olika vyer och rapporter för att analysera ekonomisk prestandadata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: 'Report_25, 103, 104, 108, 195, 196, 197, 198, 488, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Förbereda ekonomiska rapporter med ekonomiska data och kontokategorier

Funktionen **Ekonomiska rapporter** ger dig insikter i ekonomiska data som visas på din kontoplan. Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. Resultaten visas i diagram och rapporter i Rollcentret, till exempel diagram för kassaflöde och resultaträknings- och balansräkningsrapporter. Du öppnar dessa två rapporter, till exempel med åtgärden **Finansiella rapporter** på startsidorna för Business Manager och redovisning.  

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller exempel på ekonomiska rapporter som du kan använda direkt som mallar. Du kan också skapa egna rapporter för att ange vilka siffror som ska jämföras. Du kan till exempel skapa ekonomiska rapporter för att beräkna vinstmarginaler med dimensioner som avdelningar eller kundgrupper. Antalet ekonomiska rapporter du kan skapa är obegränsat och kräver ingen inblandning av en utvecklare.  

## Förutsättningar för ekonomisk rapportering

Ställa in ekonomiska rapporter kräver en förståelse för kontoplanens struktur. Det finns tre nyckelbegrepp som du förmodligen måste vara uppmärksam på innan du utformar dina ekonomiska rapporter:

- Koppla redovisningsbokföringskonton till redovisningskontokategorier.
- Utforma hur dimensioner ska användas.
- Ställ in redovisningsbudgetar

Redovisningskontokategorier förenklar definitionerna av ekonomiska rapporter och gör dem mer motståndskraftiga mot ändringar i kontoplanens struktur. Läs mer på [Använda kontokategorier för att ändra layout på din redovisning](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Genom att ställa in dimensioner kan du dela upp dina ekonomiska data på ett sätt som passar din organisation. Mer information: [Arbeta med dimensioner](finance-dimensions.md). 

Om du vill visa redovisningstransaktioner som procentsatser av budgettransaktionerna måste du skapa redovisningsbudgetar. Läs mer i [Skapa redovisningsbudgetar](finance-how-create-budgets.md).

## Ekonomiska rapporter

Ekonomiska rapporter strukturerar kontona i kontoplanen på ett sätt som gör det enklare att presentera data. Du kan skapa olika layouter för att definiera informationen som du vill hämta från kontoplanen. Ekonomiska rapporter är även en plats för beräkningar som inte kan göras direkt i kontoplanen. Du kan t. ex. skapa delsummor för grupper av konton och sedan ta med denna summa i andra summor. Ett annat exempel är att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper. Dessutom kan du filtrera redovisningstransaktionerna och budgettransaktioner, till exempel efter nettoförändring eller debetbelopp.

> [!NOTE] 
> Matematiskt kan man tänka på en ekonomisk rapport som definierad av två saker:
>
> - En vektor med raddefinitioner som definierar vad som ska beräknas.
> - En vektor med kolumndefinitioner som definierar data för beräkningen.
>
> Den ekonomiska rapporten är sedan den yttre produkten av dessa två vektorer, där varje cellvärde beräknas enligt formeln i raden som tillämpas på datadefinitionen från kolumnen.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Visar hur en ekonomisk rapport är uppbyggd utifrån en raddefinition och en kolumndefinition." lightbox="media/financial-report-definition.svg":::

På sidan **Ekonomiska rapporter** visas hur alla ekonomiska rapporter följer ett mönster som består av följande attribut:

- Namn (kod)
- Description
- Raddefinition
- Kolumndefinition

:::image type="content" source="media/financial-reports.png" alt-text="Visar hur alla ekonomiska rapporter är uppbyggda utifrån en raddefinition och en kolumndefinition." lightbox="media/financial-reports.png":::

> [!NOTE]
> De ekonomiska exempelrapporterna i [!INCLUDE[prod_short](includes/prod_short.md)] är inte färdiga att användas direkt. Beroende på hur du konfigurerar redovisningskonton, dimensioner, redovisningskontokategorier och budgetar måste du justera exempelrad- och kolumndefinitionerna och de ekonomiska rapporter som de används i så att de matchar dina inställningar.

Du kan också använda formler för att jämföra två eller flera ekonomiska rapporter och kolumndefinitioner. Jämförelser kan göra följande saker:

- Skapa anpassade ekonomirapporter.
- Skapa så många ekonomiska rapporter som behövs, var och en med ett unikt namn.
- Skapa olika rapportlayouter och skriva ut rapporterna med de aktuella siffrorna.

## Utbildningsväg: Skapa ekonomiska rapporter i Microsoft Dynamics 365 Business Central

Vill du lära dig hur du skapar budgetar och sedan använder ekonomiska rapporter, dimensioner och rad- och kolumndefinitioner för att generera de ekonomiska rapporter som företag vanligtvis behöver?

Börja med följande utbildningsväg [Skapa ekonomiska rapporter i Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## Skapa en ny ekonomisk rapport

Du använder ekonomiska rapporter för att analysera siffror för redovisningskonton eller för att jämföra redovisningstransaktioner med budgettransaktioner. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.

De ekonomiska rapporterna i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)] kanske inte passar ditt företags behov. Du kan snabbt skapa dina egna finansiella rapporter, starta genom att kopiera en befintlig, som beskrivs i steg 3 nedan.

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.  
1. På sidan **Ekonomiska rapporter** väljer du åtgärden **Nytt** för att skapa ett nytt namn på ekonomisk rapport. Om du vill återanvända inställningar från en befintlig ekonomisk rapport väljer du åtgärden **Kopiera ekonomisk rapport**.
1. Fyll i rapportens kortnamn (du kan inte ändra namnet senare) och beskrivning.
1. Välj en raddefinition och en kolumndefinition.
1. Du kan också välja analysvyer för rad- och kolumndefinitionerna.
1. Välj åtgärden **Redigera ekonomisk rapport** för åtkomst till fler egenskaper i den ekonomiska rapporten.
1. På snabbfliken **Alternativ** kan du redigera rapportbeskrivningen, ändra rad- och kolumndefinitionerna och definiera hur datum ska visas. Datum kan vara en hierarki för dag/vecka/månad/kvartal/år, eller använda bokföringsperioder. För mer information, gå till [Jämföra bokföringsperioder med hjälp av periodformler](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas).
1. På snabbfliken **Dimensioner** kan du definiera dimensionsfilter för rapporten.
1. Du kan förhandsgranska rapporten i området under snabbfliken **Dimensioner**.

> [!TIP]
> När du har skapat en ekonomisk rapport kan du använda sidan **Ekonomisk rapport** för att förhandsgranska och validera den. För att öppna sidan väljer du åtgärden **Visa ekonomisk rapport**.  

> [!NOTE]
> När du öppnar en finansiell rapport i läget Visa eller Redigera är filterrutan tillgänglig. Använd inte filterrutan för att ange filter för data i rapporten. Sådana filter kan ge felmeddelanden eller filtrera dem eventuellt inte. Använd i stället fälten på snabbflikarna **Alternativ** och **Dimensioner** för att skapa filter för rapporten.

### Skapa eller redigera en raddefinition

Raddefinitioner i ekonomiska rapporter är en plats för beräkningar som inte kan göras direkt i kontoplanen. Du kan t. ex. skapa delsummor för grupper av konton och sedan ta med denna summa i andra summor. Du kan också beräkna mellanliggande steg som inte visas i slutrapporten.

Mer information finns i [Raddefinitioner i ekonomisk rapportering](bi-row-definitions.md).

### Skapa eller redigera en kolumndefinition

Använd kolumndefinitioner för att ange vilka kolumner som ska tas med i rapporten. Du kan t.ex. utforma en rapportlayout för att jämföra nettoförändringen för samma period innevarande och föregående år. Du kan ha upp till 15 kolumner i en kolumndefinition. Flera kolumner är till exempel praktiskt om du t.ex. visar budgetar i tolv månader med en kolumn som visar summan.

Mer information finns i [Kolumndefinitioner i ekonomisk rapportering](bi-column-definitions.md).

## Använda dimensioner i ekonomiska rapporter

Inom ekonomisk analys är en dimension data som du lägger till en transaktion som en sorts markör. Dessa data används för att gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare, och enkelt hämta dessa grupper för analys. Du kan använda dimensioner på transaktioner i journaler, dokument och budgetar.

Varje dimension används för att beskriva analysens fokus. Så till exempel en tvådimensionell analys är försäljning per område. Genom att använda fler än två dimensioner när du skapar en transaktion kan du utföra en mer komplex analys. Ett exempel på en komplex analys är att utforska försäljning per försäljningskampanj per kundgrupp per område. Det ger dig större insikt i ditt företag, till exempel hur väl ditt företag fungerar, var det är eller inte blomstrar och var du bör allokera mer resurser. Den insikten hjälper dig att fatta mer välgrundade affärsbeslut. Om du vill lära dig mer går du till [Arbeta med dimensioner](finance-dimensions.md).

## Ställa in ekonomiska rapporter med översikter

Du kan använda en ekonomisk rapport för att skapa en rapport där redovisningssiffror jämförs med budgetsiffror.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du en ekonomisk rapport.  
1. Välj åtgärden **Redigera raddefinition**  
1. På sidan **Raddefinition** väljer du önskat namn på ekonomisk rapport i fältet **Namn**.
1. Välj åtgärden **Infoga redovisningskonton**.  
1. Markera de konton som du vill inkludera i utdraget och välj sedan **OK**.

    Kontona infogas i den ekonomiska rapporten. Om du vill kan du ändra kolumndefinitionen.  
1. Välj åtgärden **Redigera ekonomisk rapport**.  
1. På sidan **Ekonomisk rapport**, på snabbfliken **Dimensioner** ställ in budgetfiltret på önskat filternamn.  
1. Välj **OK**.  

Nu kan du kopiera och klistra in budgetutdraget i ett kalkylblad.  

## Integrera ekonomiska rapporter med Excel

Du kan integrera en ekonomisk rapport med en Excel-arbetsboksmall, justera layouten efter behov och sedan uppdatera Excel-mallen med data från [!INCLUDE[prod_short](includes/prod_short.md)]. Den här integrationen gör det till exempel enklare att skapa månads- och årsbokslut i ett format som passar dig.

### Konfigurera Excel-integrering för en ekonomisk rapport (skapa en Excel-mall)

Om du vill konfigurera Excel-integrering för en ekonomisk rapport följer du dessa steg för att skapa en Excel-mall för en rapport.

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomisak rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du ekonomisk rapport att aktivera med Excel och väljer åtgärden **Exportera till Excel**.
1. Välj åtgärden **Skapa nytt dokument**. Med den här åtgärden hämtas en Excel-mallarbetsbok med ett enda kalkylblad med samma namn som rapporten.
1. Kopiera kalkylbladet och byt namn på det till **Data**.
1. Byt namn på rapportförslaget efter eget tycke.
1. Markera alla celler som visar data från den ekonomiska rapporten (inklusive kolumn- och radrubriker) i rapportförslaget. I menyfliksområdet **Start** hittar du menyn **Nummer** och väljer **Allmänt** som format.
1. Markera cellen längst till vänster i området med data från den ekonomiska rapporten och ange en referens till motsvarande cell i kalkylbladet Data. Dra formeln åt höger för att utöka den till alla celler på den första raden och dra sedan raden nedåt så att den täcker alla rader i den ekonomiska rapporten.
1. Dölj kalkylbladet **Data**.
1. Formatera rapportförslaget så att det passar dina behov.
1. Spara arbetsboken i OneDrive, eller på en liknande plats där filen säkerhetskopieras och versionshanteras.
1. Stäng arbetsboken.

### Köra en ekonomisk rapport med en Excel-mall

Så här kör du en ekonomisk rapport med en Excel-mall:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomisak rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du ekonomisk rapport att aktivera med Excel och väljer åtgärden **Exportera till Excel**.
1. Välj åtgärden **Uppdatera kopia av befintligt dokument**.
1. Ladda upp Excel-mallen (stäng Excel-arbetsboken innan du laddar upp den).
1. På sidan **Namn/värde-sökning** väljer du kalkylbladet Data.
1. [!INCLUDE[prod_short](includes/prod_short.md)] kör den ekonomiska rapporten och sammanfogar resulterande data med din Excel-mall.

## Skriva ut och spara ekonomiska rapporter

Du kan skriva ut ekonomiska rapporter med hjälp av enhetens utskriftstjänster. [!INCLUDE[prod_short](includes/prod_short.md)] ger dig även möjlighet att spara rapporter som Excel-arbetsböcker, Word-arbetsböcker, PDF och XML-filer.

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du rapporten som ska skrivas ut och väljer sedan åtgärden **Skriv ut**.
1. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. I fältet **Skrivare** väljer du den enhet som rapporten ska skickas till.
    1. Alternativet **(Hanteras av webbläsaren)** anger att rapporten inte har tilldelats någon skrivare. I så fall hanterar webbläsaren utskriften och visar en standardupplevelse där du kan välja en lokal skrivare som är ansluten till enheten. **(Hanteras av webbläsaren)** är inte tillgängligt i [!INCLUDE[prod_short](includes/prod_short.md)] mobilappen eller appen för Teams.
1. Välj åtgärden **Skriv ut**.

### Schemalägga en ekonomisk rapport eller spara som ett PDF-, Word- eller Excel-dokument

Du kan spara en ekonomisk rapport som en fil i olika format, till exempel PDF, XML, Word eller Excel. [!INCLUDE[prod_short](includes/prod_short.md)] kan även generera återkommande ekonomiska rapporter.

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du åtgärden **Skriv ut**.
1. Ange rapporten i enlighet därmed och välj åtgärden **Skicka till**.
1. Välj filformat eller åtgärden **Schemalägg** och välj **OK**.
1. Fyll i fälten om du vill skapa en schemalagd eller återkommande ekonomisk rapport. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>För återkommande ekonomiska rapporter ställer du in fälten **Tidigast startdatum/-tid** och **Förfallodatum/-tid** på det första respektive sista datumet för att generera den ekonomiska rapporten. Välj också vilka dagar rapporten ska skapas genom att ställa in fältet **Datumformel för nästa körning** genom att följa formatet som förklaras i avsnittet [Använd datumformler](ui-enter-date-ranges.md#use-date-formulas).


## Metodtips för att arbeta med definitioner av ekonomiska rapporter

Definitioner för ekonomiska rapporter versionshanteras inte. När du ändrar en rapportdefinition ersätts den gamla versionen när ändringen sparas i databasen. Följande lista innehåller några metodtips för hur du arbetar med definitioner av ekonomiska rapporter:

- Om du lägger till rapportdefinitioner väljer du en bra kod och fyller i beskrivningsfältet med en meningsfull text samtidigt som du vet vad du använder rapporten till. Den här informationen hjälper dina medarbetare (och ditt framtida jag) att arbeta med rapporten och kanske ändra rapportdefinitionen.
- Innan du ändrar en rapportdefinition bör du överväga att ta en kopia av den som säkerhetskopia, ifall ändringen inte fungerar som förväntat. Du kan antingen bara kopiera definitionen (ge den ett bra namn) eller exportera den. För mer information går du till [Importera eller exportera definitioner för ekonomiska rapporter](#import-or-export-financial-report-definitions).
- Om du behöver en ny kopia av en definition som [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller är ett enkelt sätt att skapa ett nytt företag som bara innehåller inställningsdata. Exportera sedan definitionen och importera den till det företag där definitionen behöver uppdateras.

## Importera eller exportera ekonomiska rapportdefinitioner

Du kan importera och exportera rapportdefinitioner som RapidStart-konfigurationspaket. Till exempel är konfigurationspaket användbara för att dela information med andra företag. Paketet skapas i en .rapidstart-fil, vilket komprimerar innehållet.

> [!NOTE]
> När du importerar ekonomiska rapportdefinitioner kommer befintliga poster som har samma namn som de som importeras att bytas ut med de nya definitionerna. Konfigurationspaketet för en rapportdefinition skriver inte över befintliga rad- eller kolumndefinitioner som används i rapportdefinitionen.

Så här importerar eller exporterar du definitioner för ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. Välj den ekonomiska rapporten och välj sedan åtgärden **Importera ekonomisk rapport** eller **Exportera ekonomisk rapport**, beroende på vad du vill göra.

Mer information om hur du importerar eller exporterar rad- eller kolumndefinitioner för ekonomiska rapporter finns i följande artiklar: 

- [Importera eller exportera raddefinitioner för ekonomiska rapporter](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions), or
- [Importera eller exportera kolumndefinitioner för ekonomiska rapporter](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Se även

[Raddefinitioner i ekonomiska rapporter](bi-row-definitions.md)  
[Kolumndefinitioner i ekonomiska rapporter](bi-column-definitions.md)  
[Köra och skriva ut rapporter](ui-work-report.md)  
[Ekonomisk business intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
