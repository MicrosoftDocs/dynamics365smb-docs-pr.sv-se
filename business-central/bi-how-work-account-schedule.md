---
title: Skapa ekonomiska rapporter med ekonomiska data och kontokategorier
description: Beskriver hur du kan använda ekonomiska rapporter för att skapa olika vyer och rapporter för att analysera ekonomisk prestandadata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
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

Redovisningskontokategorier förenklar definitionerna av ekonomiska rapporter och gör dem mer motståndskraftiga mot ändringar i kontoplanens struktur. Läs mer på [Använda kontokategorier för att ändra layout på din redovisning](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

* Namn (kod)
* Description
* Raddefinition
* Kolumndefinition

:::image type="content" source="media/financial-reports.png" alt-text="Visar hur alla ekonomiska rapporter är uppbyggda utifrån en raddefinition och en kolumndefinition." lightbox="media/financial-reports.png":::

> [!NOTE]
> De ekonomiska exempelrapporterna i [!INCLUDE[prod_short](includes/prod_short.md)] är inte färdiga att användas direkt. Beroende på hur du konfigurerar redovisningskonton, dimensioner, redovisningskontokategorier och budgetar måste du justera exempelrad- och kolumndefinitionerna och de ekonomiska rapporter som de används i så att de matchar dina inställningar.

Du kan också använda formler för att jämföra två eller flera ekonomiska rapporter och kolumndefinitioner. Jämförelser kan göra följande saker:

* Skapa anpassade ekonomirapporter.
* Skapa så många ekonomiska rapporter som behövs, var och en med ett unikt namn.
* Skapa olika rapportlayouter och skriva ut rapporterna med de aktuella siffrorna.

## Utbildningsväg: Skapa ekonomiska rapporter i Microsoft Dynamics 365 Business Central

Vill du lära dig hur du skapar budgetar och sedan använder ekonomiska rapporter, dimensioner och rad- och kolumndefinitioner för att generera de ekonomiska rapporter som vanligtvis behövs för de flesta företag?

Börja lära dig på utbildningsvägen [Skapa ekonomiska rapporter i Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## Skapa en ny ekonomisk rapport

Du använder ekonomiska rapporter för att analysera siffror för redovisningskonton eller för att jämföra redovisningstransaktioner med budgettransaktioner. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.

De ekonomiska rapporterna i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)] kanske inte passar ditt företags behov. Du kan snabbt skapa dina egna finansiella rapporter, starta genom att kopiera en befintlig, som beskrivs i steg tre nedan.

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.  
1. På sidan **Ekonomiska rapporter** väljer du åtgärden **Nytt** för att skapa ett nytt namn på ekonomisk rapport. Om du vill återanvända inställningar från en befintlig ekonomisk rapport väljer du åtgärden **Kopiera ekonomisk rapport**.
1. Fyll i rapportens kortnamn (detta kan inte ändras) och beskrivning.
1. Välj en raddefinition och en kolumndefinition.
1. Du kan också välja analysvyer för rad- och kolumndefinitionerna.
1. Välj åtgärden **Redigera ekonomisk rapport** för åtkomst till fler egenskaper i den ekonomiska rapporten.
1. På snabbfliken **Alternativ** kan du redigera rapportbeskrivningen, ändra rad- och kolumndefinitionerna och definiera hur datum ska visas. Datum kan vara en hierarki för dag/vecka/månad/kvartal/år, eller använda bokföringsperioder. För mer information, gå till [Jämföra bokföringsperioder med hjälp av periodformler](#comparing-accounting-periods-using-period-formulas).
1. På snabbfliken **Dimensioner** kan du definiera dimensionsfilter för rapporten.
1. Du kan förhandsgranska rapporten i området under snabbfliken **Dimensioner**.

> [!TIP]
> När du har skapat en ekonomisk rapport kan du använda sidan **Ekonomisk rapport** för att förhandsgranska och validera den. För att öppna sidan väljer du åtgärden **Visa ekonomisk rapport**.  

> [!NOTE]
> När du öppnar en finansiell rapport i läget Visa eller Redigera är filterrutan tillgänglig. Använd inte filterrutan för att ange filter för data i rapporten. Sådana filter kan ge felmeddelanden eller filtrera dem eventuellt inte. Använd i stället fälten på snabbflikarna **Alternativ** och **Dimensioner** för att skapa filter för rapporten.

### Skapa eller redigera en raddefinition

Raddefinitioner i ekonomiska rapporter är en plats för beräkningar som inte kan göras direkt i kontoplanen. Du kan t. ex. skapa delsummor för grupper av konton och sedan ta med denna summa i andra summor. Du kan också beräkna mellanliggande steg som inte visas i slutrapporten.

1. På sidan **Ekonomiska rapporter** väljer du den relevanta ekonomiska rapporten och väljer sedan åtgärden **Redigera raddefinition**.
1. Välj åtgärderna **Infoga redovisningskonton**, **Infoga kassaflödeskonton** och **Infoga kostnadstyper** för att skapa en rad för varje ekonomiskt element som du vill analysera. Du kan till exempel ha en rad för omsättningstillgångar och en annan rad för anläggningstillgångar. För inspiration, utforska ekonomiska rapporter i demonstrationsföretaget CRONUS.

    > [!NOTE]
    > **Radnr.** fältet visar de första 10 tecknen i en identifierare, t.ex. ett kontonummer. Om du lägger till element med identifierare som börjar med samma tio tecken kommer du att ha dubbletter i fältet **Radnr.** . Om det behövs kan du redigera identifierare manuellt när du har infogat elementen. Alla identifierare visas i fältet **Summeringsintervall** .

> [!NOTE]
> Kolumnerna som du anger på varje rad i raddefinitionen representerar kolumnerna tre och uppåt på sidan **Ekonomisk rapport**. De två första kolumnerna **Radnr** och **beskrivning** korrigeras.  

### Skapa eller redigera en kolumndefinition

Använd kolumndefinitioner för att ange vilka kolumner som ska tas med i rapporten. Du kan t.ex. utforma en rapportlayout för att jämföra nettoförändringen för samma period innevarande och föregående år. Du kan ha upp till 15 kolumner i en kolumndefinition. Flera kolumner är till exempel praktiskt om du t.ex. visar budgetar i tolv månader med en kolumn som visar summan.

> [!NOTE]
> En utskriven/granskad/sparad version av en ekonomisk rapport visar maximalt fem kolumner. Om en ekonomisk rapport däremot endast är avsedd för analys på sidan **Ekonomisk rapport** kan du skapa så många kolumner du vill.

1. På sidan **Ekonomiska rapporter** väljer du den relevanta ekonomiska rapporten och väljer sedan åtgärden **Redigera kolumndefinition**.
1. På sidan **Kolumndefinition** skapar du en rad för varje kolumn av ekonomiska data som visas i den finansiella rapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Välj **OK**.
1. Öppna sidan **Ekonomisk rapport** med jämna mellanrum för att kontrollera att den nya kolumndefinitionen fungerar korrekt.

### Skapa en kolumndefinition för att beräkna procentsatser

Du kanske vill lägga till en kolumn i en ekonomisk rapport för att beräkna procentsatser för en summa. Om du t. ex. har rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning i varje rad.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du en ekonomisk rapport.  
1. Välj åtgärden **Redigera ekonomisk rapport** för att skapa en ekonomisk rapportrad för att beräkna den summa som procentsatserna ska baseras på.  
1. lägg till en rad direkt ovanför den första raden för vilken du vill visa en procentsats.  
1. Fyll i fälten på raden på följande sätt: I fältet **summeringstyp** anger du **inställningsbas för procent**. I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på. Ange till exempel **11** om rad 11 innehåller den totala försäljningen.  
1. Välj åtgärden **Redigera kolumndefinition** för att ange en kolumn.  
1. Fyll i fälten på den första raden enligt följande. I fältet **Kolumntyp** väljer du **Formel**. I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av procentsymbolen (%). Om kolumn N innehåller nettoförändringen anger du **N%**.  
1. Upprepa steg 4–7 för varje grupp av rader som du vill dela upp per procentsats.

## Använda kontokategorier för att ändra layout på din redovisning

Du kan använda kontokategorier för att ändra layout på din redovisning. När du har upprättat dina kontokategorier på sidan **Redovisningskontokategorier** kan du välja åtgärden **Skapa ekonomiska rapporter** och uppdatera de underliggande ekonomiska rapporterna för de centrala ekonomiska rapporterna. Nästa gång du kör någon av dessa rapporter, till exempel rapporten **Kontoavstämning** kommer nya summor och underposter att läggas till.

En annan fördel med att använda redovisningskontokategorier framför de råa redovisningskontona i raddefinitionerna är att en ändring i kontoplanens struktur inte påverkar de ekonomiska rapporterna.

> [!NOTE]
> Kontokategorierna på den högsta nivån, till exempel noden **Skulder**, är fasta och du kan inte lägga till egna. Du kan emellertid ta bort och lägga till kontokategorier på lägre nivåer och definiera hur den relaterade ekonomiska rapporten ska visas i rapporter.
>
> Du bör skapa och strukturera egna redovisningskontokategorier från grunden, i en hierarki vid behov, i stället för att försöka omarrangera de befintliga. Du kan t. ex. strukturera om **Skulder** så att de innehåller en nod **Eget kapital** följ **Kortfristiga skulder** och **Långfristiga skulder**. Läs mer i [Mappa redovisningskonton till kontokategorier](finance-general-ledger.md#account-categories).

## Använda dimensioner i ekonomiska rapporter

Inom ekonomisk analys är en dimension data som du lägger till en transaktion som en sorts markör. Dessa data används för att gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare, och enkelt hämta dessa grupper för analys. Du kan använda dimensioner på transaktioner i journaler, dokument och budgetar.

Varje dimension används för att beskriva analysens fokus. Så till exempel en tvådimensionell analys är försäljning per område. Genom att använda fler än två dimensioner när du skapar en transaktion kan du utföra en mer komplex analys. Ett exempel på en komplex analys är att utforska försäljning per försäljningskampanj per kundgrupp per område. Det ger dig större insikt i ditt företag, till exempel hur väl ditt företag fungerar, var det är eller inte blomstrar och var du bör allokera mer resurser. Den insikten hjälper dig att fatta mer välgrundade affärsbeslut. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

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

## Jämföra bokföringsperioder med hjälp av periodformler

Din ekonomiska rapport kan jämföra resultaten av olika bokföringsperioder, till exempel den senaste månaden eller samma månad förra året. Det gör du genom att öppna sidan **Kolumndefinition** och anpassa den genom att lägga till fältet **Formeljämförelseperiod** som en kolumn. Lär dig hur du [anpassar arbetsytan](ui-personalization-user.md). Du kan sedan ange att fältet ska vara en periodformel.  

En bokföringsperiod måste inte stämma överens med kalendern. Men varje räkenskapsår måste ha lika många bokföringsperioder, även om perioderna kan vara olika långa.  

[!INCLUDE[prod_short](includes/prod_short.md)] använder periodformeln för att beräkna varaktigheten för jämförelseperioden i förhållande till perioden som representeras av datumfiltret i en rapport. Jämförelseperioden baseras på perioden för startdatumet i datumfiltret. Följande förkortningar för perioder används:

| Förkortning | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Period.                                                                                |
| SP           | Sista perioden i ett räkenskapsår, halvår eller kvartal.                                   |
| CP           | Aktuell period under räkenskapsåret, halvåret eller kvartalet. Använd CP i formler för att ange den period som formeln ska börja eller sluta med. Till exempel anger RÅ\[1..cp\] tiden från början av det aktuella räkenskapsåret till den aktuella perioden.|
| RÅ           | Räkenskapsåret. Till exempel anger RÅ\[1..3\] det första kvartalet av det aktuella räkenskapsåret. |

Exempel på formler:

| Formel         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Aktuell period.                                                                                  |
| \-1P            | Föregående period.                                                                                 |
| \-1RÅ\[1..LP\]  | Hela föregående räkenskapsåret.                                                                     |
| \-1RÅ           | Aktuell period i föregående räkenskapsår.                                                          |
| \-1RÅ\[1..3\]   | Första kvartalet i föregående räkenskapsår.                                                           |
| \-1RÅ\[1..cp\]  | Från början av föregående räkenskapsår till och med aktuell period i föregående räkenskapsår, inklusive båda perioderna. |
| \-1RÅ\[CP..LP\] | Från aktuell period i föregående räkenskapsår till och med sista perioden i föregående räkenskapsår, inklusive båda perioderna.   |

Om du vill beräkna utifrån regelbundna tidsperioder måste du skriva en formel i fältet **Jämförelse datumformel**. Om fältet till exempel har värdet -1å, jämför [!INCLUDE [prod_short](includes/prod_short.md)] med samma period 1 år tidigare.

> [!NOTE]
> Det är inte alltid transparent vilka perioder som du jämför eftersom du kan ange ett datumfilter för en rapport som omfattar andra datum än de bokföringsperioder som återspeglas i kontoplanen. Så om du skapar en ekonomisk rapport där du vill jämföra denna period med samma period föregående år, så att du kan ställa in fältet **Formeljämförelseperiod** till *-1RÅ*. Sedan kan du köra rapporten 28 februari och ange datumfilter till januari och februari. Som ett resultat jämför den ekonomiska rapporten januari och februari i år med januari föregående år, vilket är den enda avslutade bokföringsperioden av de två för föregående år.  

Läs mer i [Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md).

## Skriva ut och spara ekonomiska rapporter

Du kan skriva ut ekonomiska rapporter med hjälp av enhetens utskriftstjänster. [!INCLUDE[prod_short](includes/prod_short.md)] ger dig även möjlighet att spara rapporter som Excel-arbetsböcker, Word-arbetsböcker, PDF och XML-filer.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du rapporten som ska skrivas ut och väljer sedan åtgärden **Skriv ut**.
1. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. I fältet **Skrivare** väljer du den enhet som rapporten ska skickas till.
    1. Alternativet **(Hanteras av webbläsaren)** anger att rapporten inte har tilldelats någon skrivare. I så fall hanterar webbläsaren utskriften och visar en standardupplevelse där du kan välja en lokal skrivare som är ansluten till enheten. **(Hanteras av webbläsaren)** är inte tillgängligt i [!INCLUDE[prod_short](includes/prod_short.md)] mobilappen eller appen för Teams.
1. Välj åtgärden **Skriv ut**.

### Schemalägga en ekonomisk rapport eller spara som ett PDF-, Word- eller Excel-dokument

En ekonomisk rapport kan sparas som en fil i olika format, till exempel PDF, XML, Word eller Excel. Alternativt kan [!INCLUDE[prod_short](includes/prod_short.md)] genereras återkommande ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du åtgärden **Skriv ut**.
1. Ange rapporten i enlighet därmed och välj åtgärden **Skicka till**.
1. Välj filformat eller åtgärden **Schemalägg** och välj **OK**.
1. Fyll i fälten om du vill skapa en schemalagd eller återkommande ekonomisk rapport. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>För återkommande ekonomiska rapporter ställer du in fälten **Tidigast startdatum/-tid** och **Förfallodatum/-tid** på det första respektive sista datumet för att generera den ekonomiska rapporten. Välj också vilka dagar rapporten ska skapas genom att ställa in fältet **Datumformel för nästa körning** genom att följa formatet som förklaras i avsnittet [Använd datumformler](ui-enter-date-ranges.md#use-date-formulas).

## Importera eller exportera ekonomiska rapportdefinitioner

Du kan importera och exportera ekonomiska rapporter/raddefinitioner som RapidStart-konfigurationspaket, som är användbara när du vill dela informationen med andra företag, t.ex. Paketet skapas i en .rapidstart-fil, vilket komprimerar innehållet.

> [!NOTE]
> När du importerar ekonomiska rapporter/raddefinitioner kommer befintliga poster som har samma namn som de som importeras att bytas ut med de nya definitionerna. Observera att konfigurationspaketet för en rapportdefinition inte skriver över befintliga rad- eller kolumndefinitioner som används i rapportdefinitionen.

Så här importerar eller exporterar du definitioner för ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. Välj den ekonomiska rapporten och välj sedan åtgärden **Importera ekonomisk rapport** eller **Exportera ekonomisk rapport**, beroende på vad du vill göra.

Så här importerar eller exporterar du raddefinitioner för ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Raddefinitioner** och välj relaterad länk.
1. Välj raddefinition och välj sedan åtgärden **Importera raddefinition** eller **Exportera raddefinition**, beroende på vad du vill göra.

## Se även

[Köra och skriva ut rapporter](ui-work-report.md)  
[Ekonomisk business intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
