---
title: Skapa ekonomiska rapporter med ekonomiska data och kontokategorier
description: Beskriver hur du kan använda ekonomiska rapporter för att skapa olika vyer och rapporter för att analysera ekonomisk prestandadata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories" />Förbereda Financial Reporting med ekonomiska data och kontokategorier

Ekonomiska rapporter ger dig insikt i ekonomiska data som lagras i din kontoplan. Ekonomiska rapporter analyserar siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. Resultaten visas i diagram och rapporter i Rollcentret, till exempel diagram för kassaflöde och resultaträknings- och balansräkningsrapporter.

Du öppnar dessa två rapporter, till exempel med åtgärden **Finansiella rapporter** i Business Manager och rollcenter för redovisning.  

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller exempel på ekonomiska rapporter som du kan använda direkt. Du kan också skapa egna rader och kolumner för att ange vilka siffror som ska jämföras. Du kan till exempel skapa ekonomiska rapporter för att beräkna vinstmarginaler med dimensioner som avdelningar eller kundgrupper. Antalet anpassade bokslut du kan skapa är obegränsat.  

Ställa in ekonomiska rapporter kräver en förståelse för den ekonomiska informationen i kontoplanen. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna, men det kräver att du har skapat budgetar. Läs mer i [Skapa redovisningsbudgetar](finance-how-create-budgets.md).

## <a name="financial-reports" />Ekonomiska rapporter

Ekonomiska rapporter strukturerar kontona i kontoplanen på ett sätt som gör det enklare att presentera data. Du kan skapa olika layouter för att definiera informationen som du vill hämta från kontoplanen. Ekonomiska rapporter är en plats för beräkningar som inte kan göras direkt i kontoplanen. Du kan t. ex. skapa delsummor för grupper av konton och sedan ta med denna summa i andra summor. Ett annat exempel är att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper. Dessutom kan du filtrera redovisningstransaktionerna och budgettransaktioner, till exempel efter nettoförändring eller debetbelopp.

Du kan även jämföra två eller flera ekonomiska rapporter och kolumndefinitioner med hjälp av formler, så att du kan göra följande:

* Skapa anpassade ekonomirapporter.
* Skapa så många ekonomiska rapporter som behövs, var och en med ett unikt namn.
* Skapa olika rapportlayouter och skriva ut rapporterna med de aktuella siffrorna.

## <a name="gl-account-categories" />Redovisningskontokategorier

Du kan använda kontokategorier för att ändra layout på din redovisning. När du har upprättat dina kontokategorier på sidan **Redovisningskontokategorier** kan du välja åtgärden **Skapa ekonomiska rapporter** och uppdatera de underliggande ekonomiska rapporterna för de centrala ekonomiska rapporterna. Nästa gång du kör någon av dessa rapporter, till exempel rapporten **Kontoavstämning** kommer nya summor och underposter att läggas till.

> [!NOTE]
> Kontokategorierna på den högsta nivån, till exempel noden **Skulder**, är fasta och du kan inte lägga till egna. Du kan emellertid ta bort och lägga till kontokategorier på lägre nivåer och definiera hur den relaterade ekonomiska rapporten ska visas i rapporter.
>
> Du bör skapa och strukturera egna redovisningskontokategorier från grunden, i en hierarki vid behov, i stället för att försöka omarrangera de befintliga. Du kan t. ex. strukturera om **Skulder** så att de innehåller en nod **Eget kapital** följ **Kortfristiga skulder** och **Långfristiga skulder**.

## <a name="create-a-new-financial-report" />Skapa en ny ekonomisk rapport

Du använder ekonomiska rapporter för att analysera siffror för redovisningskonton eller för att jämföra redovisningstransaktioner med budgettransaktioner. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.

De ekonomiska rapporterna i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)] kanske inte passar ditt företags behov. Du kan snabbt skapa dina egna finansiella rapporter, starta genom att kopiera en befintlig, som beskrivs i steg tre nedan.

> [!TIP]
> När du har skapat en ekonomisk rapport kan du använda sidan **Ekonomisk rapport** för att förhandsgranska och validera en nyligen definierad ekonomisk rapport. För att öppna sidan väljer du åtgärden **Redigera ekonomisk rapport**.  

> [!NOTE]
> När du öppnar en finansiell rapport i läget Visa eller Redigera är filterrutan tillgänglig. Använd dock inte fönstret för att ange filter för data i rapporten. Filtren kan ge felmeddelanden eller filtrera dem eventuellt inte. Använd i stället filterfälten på snabbflikarna **alternativ** och **dimensioner**.

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.  
2. På sidan **Ekonomiska rapporter** väljer du åtgärden **Nytt** för att skapa ett nytt namn på ekonomisk rapport.
3. Om du vill återanvända inställningar från en befintlig ekonomisk rapport väljer du åtgärden **Kopiera ekonomisk rapport**.
4. Fyll i fälten om det behövs. I fältet **kolumndefinition** väljer du en befintlig definition, som du senare kan redigera om du vill.

    Kolumndefinitioner anger parametrar som ekonomiska data på raderna visas enligt. Till exempel kan en kolumndefinition innehålla fyra kolumner som du kan använda för att jämföra nettoförändringen för samma period innevarande och föregående år. Mer information finns i avsnittet [Redigera en kolumndefinition](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Välj åtgärden **Redigera raddefinition**.
6. Välj åtgärderna **Infoga redovisningskonton**, **Infoga kassaflödeskonton** och **Infoga kostnadstyper** för att skapa en rad för varje ekonomiskt element som du vill analysera. Du kan till exempel ha en rad för omsättningstillgångar och en annan rad för anläggningstillgångar. För inspiration, se ekonomiska rapporter i demonstrationsföretaget CRONUS.

    > [!NOTE]
    > **Radnr.** fältet visar de första 10 tecknen i en identifierare, t.ex. ett kontonummer. Om du lägger till element med identifierare som börjar med samma tio tecken kommer du att ha dubbletter i fältet **Radnr.** . Om det behövs kan du redigera identifierare manuellt när du har infogat elementen. Alla identifierare visas i fältet **Summeringsintervall** .

7. På sidan **Ekonomiska rapporter** väljer du åtgärden **Redigera ekonomisk rapport** för att se den slutliga ekonomiska rapporten.
8. På sidan **Ekonomisk rapport** i fältet **Kolumndefinition** väljer du en annan kolumndefinition för att utforska ekonomiska data med andra parametrar.
9. Välj **OK**.

Du har nu definierat basen för den ekonomiska rapporten, raderna för ekonomiska data som ska visas och en befintlig layout för kolumner för att visa data på rader med anpassade parametrar. Om standardkolumndefinitionen som du valde i steg 4 inte passar dina önskemål, följ stegen i [Redigera en kolumndefinition](#edit-a-column-definition).

### <a name="edit-a-column-definition" />Redigera en kolumndefinition

Använd kolumndefinitioner för att ange vilka kolumner som ska tas med i rapporten. Du kan t.ex. utforma en layout för att jämföra nettoförändringen för samma period innevarande och föregående år. Du kan ha upp till 15 kolumner, vilket kan vara praktiskt om du t.ex. visar budgetar i tolv månader med en kolumn som visar summan.

> [!NOTE]
> En utskriven/granskad/sparad version av en ekonomisk rapport visar maximalt fem kolumner. Om en ekonomisk rapport däremot endast är avsedd för analys på sidan **Ekonomisk rapport** kan du skapa så många kolumner du vill.

1. På sidan **Ekonomiska rapporter** väljer du den relevanta ekonomiska rapporten och väljer sedan åtgärden **Redigera kolumndefinition**.
2. På sidan **Kolumndefinition** skapar du en rad för varje kolumn av ekonomiska data som visas i den finansiella rapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj **OK**.
4. Öppna sidan **Ekonomisk rapport** med jämna mellanrum för att kontrollera att den nya kolumndefinitionen fungerar korrekt.

> [!NOTE]
> Kolumnerna som du anger på varje rad representerar kolumnerna tre och uppåt på sidan **Ekonomisk rapport**. De två första kolumnerna **Radnr** och **beskrivning** korrigeras.  

### <a name="create-a-column-that-calculates-percentages" />Skapa en kolumn för att beräkna procentsatser

Du kan lägga till en kolumn i en ekonomisk rapport för att beräkna procentsatser för en summa. Om du t. ex. har rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning i varje rad.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
2. På sidan **Ekonomiska rapporter** väljer du en ekonomisk rapport.  
3. Välj åtgärden **Redigera ekonomisk rapport** för att skapa en ekonomisk rapportrad för att beräkna den summa som procentsatserna ska baseras på.  
4. Infoga en rad direkt ovanför den första raden för vilken du vill visa en procentsats.  
5. Fyll i fälten på raden på följande sätt: I fältet **summeringstyp** anger du **inställningsbas för procent**. I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på. Ange till exempel **11** om rad 11 innehåller den totala försäljningen.  
6. Välj åtgärden **Redigera kolumndefinition** för att ange en kolumn.  
7. Fyll i fälten på raden på följande sätt: I fältet **kolumntyp** väljer **formeln**. I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av procentsymbolen (%). Om kolumn N innehåller nettoförändringen anger du **N%**.  
8. Upprepa steg 4–7 för varje grupp av rader som du vill dela upp per procentsats.

## <a name="set-up-financial-reports-with-overviews" />Ställa in ekonomiska rapporter med översikter

Du kan använda en ekonomisk rapport för att skapa en rapport där redovisningssiffror jämförs med budgetsiffror.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
2. På sidan **Ekonomiska rapporter** väljer du en ekonomisk rapport.  
3. Välj åtgärden **Redigera raddefinition**  
4. På sidan **Raddefinition** väljer du önskat namn på ekonomisk rapport i fältet **Namn**.
5. Välj åtgärden **Infoga redovisningskonton**.  
6. Markera de konton som du vill inkludera i utdraget och välj sedan **OK**.

    Kontona infogas i den ekonomiska rapporten. Om du vill kan du ändra kolumndefinitionen.  
7. Välj åtgärden **Redigera ekonomisk rapport**.  
8. På sidan **Ekonomisk rapport**, på snabbfliken **Dimensioner** ställ in budgetfiltret på önskat filternamn.  
9. Välj **OK**.  

Nu kan du kopiera och klistra in budgetutdraget i ett kalkylblad.  

## <a name="comparing-accounting-periods-using-period-formulas" />Jämföra bokföringsperioder med hjälp av periodformler

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

## <a name="print-and-save-financial-reports" />Skriva ut och spara ekonomiska rapporter

Du kan skriva ut ekonomiska rapporter med hjälp av enhetens utskriftstjänster. [!INCLUDE[prod_short](includes/prod_short.md)] ger dig även möjlighet att spara rapporter som Microsoft Excel-arbetsböcker, Microsoft Word-dokument, PDF-filer och XML-filer.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
2. På sidan **Ekonomiska rapporter** väljer du rapporten som ska skrivas ut och väljer sedan åtgärden **Skriv ut**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I fältet **Skrivare** väljer du den enhet som rapporten ska skickas till.
    1. Alternativet **(Hanteras av webbläsaren)** anger att rapporten inte har tilldelats någon skrivare. I så fall hanterar webbläsaren utskriften och visar en standardupplevelse där du kan välja en lokal skrivare som är ansluten till enheten. **(Hanteras av webbläsaren)** är inte tillgängligt i [!INCLUDE[prod_short](includes/prod_short.md)] mobilappen eller appen för Microsoft Teams.
5. Välj åtgärden **Skriv ut**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document" />Schemalägga en ekonomisk rapport eller spara som ett PDF-, Word- eller Excel-dokument

En ekonomisk rapport kan sparas som en fil i olika format, till exempel PDF, XML, Word eller Excel. Alternativt kan [!INCLUDE[prod_short](includes/prod_short.md)] ställas in på att generera återkommande ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
2. På sidan **Ekonomiska rapporter** väljer du åtgärden **Skriv ut**.
3. Ange rapporten i enlighet därmed och välj åtgärden **Skicka till**.
4. Välj filformat eller åtgärden **Schemalägg** och välj **OK**.
5. Fyll i fälten om du vill skapa en schemalagd eller återkommande ekonomisk rapport. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * För återkommande ekonomiska rapporter ställer du in fälten **Tidigast startdatum/-tid** och **Förfallodatum/-tid** på det första respektive sista datumet för att generera den ekonomiska rapporten. Välj också vilka dagar rapporten ska skapas genom att ställa in fältet **Datumformel för nästa körning** genom att följa formatet som förklaras i avsnittet [Använd datumformler](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports" />Importera eller exportera ekonomiska rapporter

Du kan importera och exportera ekonomiska rapporter som RapidStart-konfigurationspaket, som är användbara när du vill dela informationen med andra företag, t.ex. Paketet skapas i en .rapidstart-fil, vilket komprimerar innehållet.

### <a name="import-and-export-financial-reports" />Importera och exportera ekonomiska rapporter

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
2. Välj den ekonomiska rapporten och välj sedan åtgärden **Importera ekonomisk rapport** eller **Exportera ekonomisk rapport**, beroende på vad du vill göra.

> [!NOTE]
> När du importerar ekonomiska rapporter kommer befintliga poster som har samma namn som de som importeras att tas bort.

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-financial-reports-dynamics-365-business-centralindex" />Se relaterad [Microsoft-utbildning](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also" />Se även

[Köra och skriva ut rapporter](ui-work-report.md)  
[Financial Business Intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
