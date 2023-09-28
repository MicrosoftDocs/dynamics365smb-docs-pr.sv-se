---
title: Använda redovisningsjournaler för att bokföra direkt i redovisningen
description: 'Lär hur du använder journaler för att bokföra ekonomiska transaktioner på redovisningskonton och andra konton, till exempel bank- och leverantörskonton.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 08/29/2023
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# Arbeta med redovisningsjournaler

De flesta finansiella transaktioner bokförs i redovisningen genom dokument, till exempel inköpsfakturor och försäljningsorder. Du kan emellertid även hantera affärsaktiviteter som t.ex.:

* Inköp
* Betalningar
* Använda återkommande journaler för att bokföra periodiseringar
* Återfinansiera kostnader för anställda genom att bokföra journalrader i journaler  

De flesta journalerna baseras på redovisningsjournalen och du kan bearbeta alla transaktioner på sidan **redovisningsjournal**. Läs mer på [Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).  

Du kan till exempel använda bokföra anställdas utgifter för återbetalning. Läs mer på [Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md).

Men [!INCLUDE [prod_short](includes/prod_short.md)] erbjuder också journaler som är optimerade för vissa typer av transaktioner såsom **betalningsjournal** för att registrera betalningar. Mer information finns i [Registrera betalningar och återbetalningar i betalningsjournalen](payables-how-post-payments-refunds.md).  

Du använder redovisningsjournaler för att bokföra ekonomiska transaktioner till redovisningskonton och andra konton. Övriga konton är konton för bank, kund, leverantör och anställd. När du bokför med en redovisningsjournal skapas transaktioner på redovisningskonton även när du till exempel bokför en journalrad på ett kundkonto. Transaktionen bokförs till ett konto för kund reskontra i redovisningen via en bokföringsmall.

Den information som du anger i en journal är tillfällig och kan ändras så länge den finns i journalen. När du bokför journalen, överförs informationen till transaktioner på enskilda konton, där den inte kan ändras. Du kan emellertid ta bort kopplingar från bokförda transaktioner och bokföra återförande eller rättande transaktioner. Läs mer på [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## Lägga till kontext i redovisningsjournaltransaktioner

När du skapar en journal kan du lägga till länkar som ger transaktionerna ett sammanhang. När du bokför journalen kopierar [!INCLUDE [prod_short](includes/prod_short.md)] länkarna till den bokförda journalen och transaktionerna som journalen skapar. Att tillhandahålla länkar kan till exempel göra livet enklare för din revisor. Om du sparar bilder av dina utgiftskvitton på företagets Sharepoint-webbplats kan du lägga till länkar till filerna. När du bokför journalen för att skicka in dina utgifter kan revisorn snabbt komma åt inleveransfilerna.

## Använd journalmallar och journaler

Det finns flera redovisningsjournalmallar. Varje journalmall representeras av en dedikerad sida med särskilda funktioner och fälten som krävs för att stödja dessa funktioner, till exempel sidan **Betalningsavstämningsjournal** för att bearbeta bankbetalningar och sidan **Betalningsjournal** för att betala dina leverantörer eller återbetala dina anställda. Mer information finns i [Gör betalningar](payables-make-payments.md) och [Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner](receivables-how-apply-sales-transactions-manually.md).

För varje journalmall kan du skapa din egen personliga journal som en journal. Du kan till exempel ange din egen journal för betalningsjournalen som har din personliga layout och inställningar. Följande tips är ett exempel på hur du anpassar en journal.

> [!TIP]  
> Om du väljer kryssrutan **Föreslå saldobelopp** på raden för din journal på sidan **Redovisningsjournaler** kommer fältet **Belopp** till exempel, redovisningsjournalrader för samma verifikationsnummer automatiskt att fyllas i med värdet som krävs för att hantera dokumentet. Lär dig mer på [Låta [!INCLUDE[prod_short](includes/prod_short.md)] föreslå värden](ui-let-system-suggest-values.md).

> [!TIP]
> Du kan lägga till eller ta bort fält i journaler genom att anpassa dem. Lär dig hur du [anpassar arbetsytan](ui-personalization-user.md).

### Validera redovisningsjournaler

Du kan aktivera en bakgrundskontroll som förhindrar fördröjningar vid bokföring. Kontrollen meddelar dig när ett misstag i den finansiella journalen som du arbetar med hindrar dig från att bokföra journalen. På sidan **Redovisningsjournal** kan du välja **Felkontroll i bakgrunden** om du vill att [!INCLUDE[prod_short](includes/prod_short.md)] validerar finansiella journaler, till exempel redovisnings- eller utbetalningsjournaler, medan du arbetar med dem.

När du aktiverar valideringen visas faktaboxen **Journalkontroll** på den aktuella raden och i hela partiet. Valideringen sker när du läser in en finansiell journal och väljer en annan journalrad. Panelen **Ärenden totalt** i faktaboxen visar det totala antalet ärenden som [!INCLUDE[prod_short](includes/prod_short.md)] hittade, och du kan välja att den öppnar en översikt över ärendena.

Du kan använda åtgärderna **Visa rader med ärenden** och **Visa alla rader** för att växla mellan journalrader som har eller inte har några ärenden. Den nya faktaboxen **Journalradsinformation** ger snabb överblick över och åtkomst till data från journalrader, till exempel redovisningskonto, kund eller leverantör, samt bokföringsinställningarna för specifika konton.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## Förstå huvudkonton och motkonton

Om du har skapat standardmotkonton för journalerna på sidan **Redovisningsjournaler** fylls motkontot i automatiskt när du fyller i fältet **Kontonr**. Annars fyller du i både fältet **Kontonr** och fältet **Motkonto** manuellt. Ett positivt belopp i fältet **Belopp** debiteras på huvudkontot och krediteras på motkontot. Ett negativt belopp krediteras på huvudkontot och debiteras på motkontot.

> [!NOTE]  
> Moms beräknas separat för huvudkontot och motkontot, så att olika momssatser kan användas för dem.

## Arbeta med återkommande journaler

En återkommande journal är en redovisningsjournal med specifika fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar. Till exempel transaktioner för utgifter som hyra, abonnemang, elektricitet och värme. Med hjälp av återkommande journaler kan du bokföra fasta och variabla belopp och ange automatiska återföringsposter för dagen efter bokföringsdatumet. Med fördelningsnycklar kan du dela upp återkommande transaktioner mellan olika konton. Läs mer på [Fördela återkommande journalbelopp på flera konton](#allocating-recurring-journal-amounts-to-several-accounts).

Med en återkommande journal skapar du transaktioner som ska bokföras regelbundet endast en gång. Till exempel konton, dimensioner och dimensionsvärden, etc. finns kvar i journalen efter bokföring. Om ändringar behövs kan du göra det varje gång du bokför.

### Fält för återkommande metod

Fältet **Återkommande metod** är viktigt. Det bestämmer hur du behandlar beloppet på journalraden efter bokföring. Om du t.ex. vill använda samma belopp varje gång du bokför raden kan du låta beloppet stå kvar. Om du vill använda samma konton och samma text på raden och bara ändra beloppet varje gång du bokför, kan du låta beloppet raderas varje gång du har bokfört.

| Till | Gå till |
| --- | --- |
|F Fast|Journalradens antal kommer att stå kvar när du har bokfört.|
|V Variabel|Journalradens antal kommer att tas bort när du har bokfört.|
|S Saldo|Det bokförda beloppet på kontot på raden kommer att fördelas på de konton som angetts för raden i tabellen Allm. journ. tilldeln. Saldot på kontot blir på det sättet nollställt. Kom ihåg att fylla i fältet **Fördelning %** på sidan **Fördelningar**. Mer information finns i avsnittet [Tilldela återkommande journalbelopp till flera olika konton](#allocating-recurring-journal-amounts-to-several-accounts).|
|ÅF Återföring fast|Journalradens belopp kommer att stå kvar efter det att du har bokfört och en mottransaktion kommer att bokföras nästa dag.|
|ÅV Återföring variabel|Journalradens belopp kommer att tas bort efter det att du har bokfört och en mottransaktion kommer att bokföras på nästa dag.|
|AB Återföring saldo|Det bokförda beloppet på kontot på raden kommer att fördelas på de konton som angetts för raden på sidan **Fördelningar**. Saldot på kontot anges till noll, och en mottransaktion bokförs på nästa dag.|
|BD Saldo efter dimension|Journalraden fördelar kostnader baserat på ett redovisningskontos saldo efter dimension. Du uppmanas att ange de dimensionsfilter som ska användas för att beräkna källredovisningskontots saldo efter dimension som du vill fördela kostnader från. Som ett alternativ kan du välja åtgärden **Dimensionsfilter** senare.|
|Återföring saldo per dimension|Journalraden fördelar kostnader baserat på ett redovisningskontos återföringssaldo efter dimension. Du uppmanas att ange de dimensionsfilter som ska användas för att beräkna källredovisningskontots saldo efter dimension som du vill fördela kostnader från. Du kan också välja åtgärden **Dimensionsfilter** senare.|

> [!NOTE]  
> Momsfälten kan fyllas i antingen på raden i den återkommande journalen eller på raden i fördelningsjournalen, men inte på båda raderna. Det går med andra ord bara att fylla i dem på sidan **Fördelningar** om motsvarande rader i den återkommande journalen inte är ifyllda.

### Fält för återkommande frekvens

Det här datum formel fältet bestämmer hur ofta transaktionen ska bokföras på journalraden och måste fyllas i. Läs mer i [Använd dataformulär](ui-enter-date-ranges.md#use-date-formulas).

#### Exempel

Om journalraden måste bokföras varje månad skriver du "1M". Varje gång du har bokfört kommer datumet i fältet **Bokföringsdatum** att uppdateras till samma datum nästa månad.

Om du vill bokföra en transaktion till den sista dagen i varje månad kan du göra på något av följande sätt:

* Bokför den första transaktionen på den sista dagen i en månad genom att ange 1D+1M-1D (1 dag + 1 månad – 1 dag). Med den här formeln beräknas bokföringsdatumet korrekt oberoende av antalet dagar i månaden.

* Bokför den första transaktionen på en valfri dag i månaden genom att ange 1M+LM. Med en här formeln inträffar bokföringsdatumet efter en hel månad + den löpande månadens återstående dagar.

### Fält för utgångsdatum

Detta fält bestämmer vilket datum raden ska bokföras för sista gången. Raden kommer inte att bokföras efter detta datum.

Fördelen med att använda fältet Utgångsdatum är att raden inte kommer att raderas från journalen direkt. Du kan ange ett senare datum så att du kan använda raden i framtiden.

Om fältet är tomt kommer raden att bokföras varje gång du bokför tills raden tas bort från journalen.

### Fördela återkommande journalbelopp på flera konton

På sidan **Återkommande redovisningsjournal** kan du välja åtgärden **Fördelningar** för att ange hur belopp på den återkommande journalraden fördelas på flera konton och dimensioner. Fördelningen fungerar som en balanskontorad visavi den återkommande journalraden.

Precis som en återkommande journal anger du en fördelning en gång och stannar kvar i fördelningsjournalen när du har bokfört den. Du behöver inte skriva in belopp och fördelningar varje gång du bokför den återkommande journalraden.

Om den återkommande metoden i den återkommande journalen har angetts som **Saldo** or **Återföring saldo** ignoreras alla dimensionsvärdekoder i den återkommande journalen när kontot är nollställt. Det betyder att om du fördelar en återkommande rad på olika dimensionsvärden på sidan **Fördelningar**, så skapas bara en återföringstransaktion.

> [!NOTE]
> Om du fördelar en återkommande journalrad som innehåller en dimensionsvärdekod får du därför inte ange samma kod på sidan **Fördelningar**. Om du gör detta kommer dimensionsvärdena att bli felaktiga.  

Om du vill fördela återkommande journalbelopp baserat på dimensioner anger du fältet **Återkommande metod** som **Saldo efter dimension** eller **Återföra saldo efter dimension**. Om den återkommande metoden i den återkommande journalen har angetts som **Saldo efter dimension** eller **Återföra saldo efter dimension** beaktas alla dimensionsvärdekoder i den återkommande journalen när kontot är nollställt. Om du allokerar en återkommande rad till olika dimensionsvärden på sidan **Allokeringar** skapas återföringstransaktioner som matchar antalet dimensionsvärdekombinationer som saldot består av. Om du allokerar kontosaldo via den återkommande journalen som innehåller en dimensionsvärdekod, kom då ihåg att använda **Saldo efter dimension** eller **Återföra saldo efter dimension** för att se till att dimensionsvärdena är korrekt balanserade eller återförda från källkontot.  

Ditt företag har till exempel ett par affärsenheter och en handfull avdelningar som dina controllers har ställt in som dimensioner. Om du vill påskynda transaktionsprocessen för inköpsfakturor bestämmer du dig för att kräva att leverantörsreskontramedarbetarna endast anger affärsenhetsdimensioner. Eftersom varje affärsenhet har specifika fördelningsnycklar för avdelningsdimensionen – till exempel baserat på antalet medarbetare – kan du använda de återkommande metoderna för **BD-saldo efter dimension** eller **RBD-återföringssaldo efter dimension** för att omfördela utgifter för respektive affärsenhet till rätt avdelningar baserat på fördelningsnycklarna.  

> [!NOTE]
> Dimensioner som du anger på allokeringsrader beräknas inte automatiskt, utan du måste ange vilka dimensionsvärden som måste anges på fördelningskontona. Om du vill bevara kopplingen mellan källkontodimensionen och fördelningskontodimensionen rekommenderar vi att du använder funktionen för [Kostnadsfördelning](finance-about-cost-accounting.md) istället.

#### Exempel: Fördela hyresinbetalningar på olika avdelningar

Du betalar hyra varje månad, så du har skrivit in beloppet på kassakontot på en återkommande journalrad. På sidan **Fördelningar** kan du använda dimensionen Avdelning för att dela utgiften mellan flera avdelningar. Till exempel efter det antal kvadratmeter som varje avdelning upptar. Beräkningen grundas på procentandelen för fördelning på respektive rad. Du kan fördela dem på olika sätt:

* Ange olika konton på olika fördelningsrader för att dela upp hyreskostnader mellan flera konton.
* Ange samma konto men använd olika dimensionsvärdekoder för avdelningsdimensionen på varje rad.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### Beräkning av återföringsdatum

När du använder återkommande redovisningsjournaler för att bokföra periodiseringar vid slutet av en period är det viktigt att du har full kontroll över återföringstransaktioner. På sidan **Återkommande redovisningsjournaler** kan du med hjälp av fältet **Beräkning av återföringsdatum** kontrollera det datum som återföringstransaktionerna ska bokföras när metoder för återkommande återförsel används.

#### Exempel

Periodiseringar bokförs vanligtvis med metoderna **Fast**, **Variabel** eller **Balansering** på journalraden. Bokföringsdatumet för det bokförda beloppet på kontot på journalraden beräknas med den återkommande frekvensen. Bokföringsdatumet för mottransaktionen beräknas med hjälp av fältet **Beräkning av återföringsdatum** enligt följande:

* Om fältet är tomt kommer mottransaktionen att bokföras nästa dag.
* Om fältet innehåller en datumformel (t. ex. **5D** för fem dagar), bokförs mottransaktionen med ett bokföringsdatum beräknat med hjälp av beräkningen av återföringsdatum.

> [!NOTE]
> Som standard är fältet **Beräkning av återföringsdatum** inte tillgängligt på sidan **Återkommande redovisningsjournaler**. Om du vill använda fältet måste du lägga till det genom att anpassa sidan. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

## Arbeta med standardjournaler

När du har skapat journalrader som du vet att du förmodligen kommer att skapa igen, kan du spara dem som en standardjournal innan du bokför journalen. Den här funktionen gäller artikeljournaler och redovisningsjournaler.

> [!NOTE]
> Standardjournaler kanske inte innehåller alla fält som du vill inkludera i de resulterande transaktionerna. Om du till exempel använder en standardredovisningsjournal för att registrera en betalning kommer inte transaktionerna att innehålla fältet betalningssätt.

> [!NOTE]  
> Följande procedur gäller för artikeljournalen, men informationen kan också tillämpas på redovisningsjournalen.

### Så här sparar du som en standardjournal

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikeljournaler** och väljer sedan relaterad länk.
2. Mata på en eller flera journalrader.
3. Markera de journalrader som du vill återanvända.
4. Välj åtgärden **Spara som standardjournal**.
5. På sidan **Spara som standardartikeljournal** måste du definiera en ny eller befintlig standardartikeljournal som raderna ska sparas i:

    Om du redan har skapat en eller flera standardartikeljournaler och du vill ersätta någon av dessa med den nya uppsättningen artikeljournalrader, i fältet **Kod** och välja artikeljournal.
6. Välj **OK** för att bekräfta att du vill byta ut innehållet på den befintliga standardartikeljournalen.
7. För att spara värdena i fältet **A-pris** i standardartikeljournalen väljer du fältet **Spara a-pris**.
8. Om du vill spara värdena i fältet **Antal** väljer du fältet **Spara antal**.
9. Välj **OK** för att spara standardartikeljournalen.

När du sparar standardartikeljournalen visas sidan artikeljournal så att du kan bokföra den.

### Så här återanvänder du standardjournaler

> [!NOTE]
> Standardjournaler har inte alltid samma fält som redovisningsjournaler. När du använder åtgärden Hämta standardjournaler för att kopiera fälten till redovisningsjournalen, kan redovisningsjournalen ha mindre information än om du skapade den manuellt. 

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikeljournaler** och väljer sedan relaterad länk.
2. Välj åtgärden **Få standardjournal**.
3. Om du vill förhandsgranska en standardartikeljournal innan du väljer att återanvända den, klickar du på **Visa journal**.

    Ändringar som du gör i en standardartikeljournal implementeras direkt och visas nästa gång du öppnar eller återanvänder standardartikeljournalen. Se till att ändringen är tillräckligt viktig för att tillämpa allmänt. Annars skapar du den specifika ändringen i artikeljournalen efter att standardartikeljournalraderna har lagts till. Se steg 4.
4. När du kommer tillbaka till sidan **Standardartikeljournaler** väljer du den standardartikeljournal som du vill återanvända och klickar på **OK**.

    Artikeljournalen innehåller raderna som du har sparat. Om artikeljournalen redan har rader visas de nya raderna.

    Om du inte aktiverar fältet **Spara a-pris** när du sparade journalen innehåller fältet **A-pris** på rader som lagts till från standardjournalen värdet från fältet **Styckkostnad** på artikelkortet.

    > [!NOTE]  
    > Om du har aktiverat växlingsknapparna **Spara a-pris** eller **Spara antal** när du sparade journalen ska du nu kontrollera att de nya värdena är korrekta innan du bokför denna artikeljournalen.
    >
    > Om de infogade artikeljournalraderna innehåller sparade a-priser som du inte vill bokföra, kan du justera dem till artikelns aktuella värde:

5. Välj de artikeljournalrader som du vill justera lagret för och välj sedan åtgärden **Omberäkna a-pris**. Denna åtgärd uppdaterar fältet A-pris med artikelns aktuella styckkostnad.
6. Välj åtgärden **Bokföra**.

## Numrera om verifikationsnummer i journaler

För att undvika bokföringsfel som orsakas av dokumentnummer kan du använda åtgärden **Numrera om dokumentnummer** innan du bokför en journal.

I alla journaler som är baserade på redovisningsjournalen är fältet **Dokumentnr** redigerbart så att du kan ange olika nummer för olika journalrader eller samma verifikationsnummer för relaterade journalrader.

Om fältet **Nr-serie** på journalen fylls, kräver bokföringsfunktionen i redovisningsjournaler att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. Välj bara åtgärden **Numrera om dokumentnummer** så uppdateras relevanta **Dokumentnr**-fält. Om relaterade rader grupperades efter verifikationsnummer innan du använde funktionen, förblir de grupperade men kan tilldelas ett annat verifikationsnummer.  

Den här funktionen fungerar även på filtrerade vyer.

Alla omnumreringen av verifikationsnummer skall respektera relaterade tillämpningar, som en ansökan om betalningstillämpning som har gjorts från dokumentet på journalraden till ett leverantörskonto. I enlighet med detta kan fälten **Koppla till ID** och **Koppla till ver.nr.** i de berörda transaktionerna uppdateras.

### Numrera om dokument i journaler

Följande procedur är baserad på sidan **Redovisningsjournal**, men gäller för alla andra journaler som baseras på den redovisningsjournalen, t. ex. sidan **Utbetalningsjournal**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **redovisningsjournaler** och väljer sedan relaterad länk.
2. När du är klar att bokföra journalraderna väljer du **Numrera om dokumentnummer**.

Värden i fältet **Dokumentnr** ändras, om så krävs, så att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. När dokument numreras kan du bokföra journalen.

## Se även

[Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Fördela kostnader och intäkter](year-allocate-costs-income.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Omvärdera lagret i omvärderingsjournalen](inventory-how-revalue-inventory.md)  
[Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md)  
[Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner](receivables-how-apply-sales-transactions-manually.md)  
[Stäm av leverantörsbetalningar med betalningsjournalen eller från bokförda leverantörsreskontratransaktioner](payables-how-apply-purchase-transactions-manually.md)  
[Arbeta med koncerninterna dokument och journaler](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
