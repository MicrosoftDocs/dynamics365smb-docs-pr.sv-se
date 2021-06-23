---
title: Använda redovisningsjournaler för att bokföra direkt i redovisningen
description: Lär hur du använder journaler för att bokföra ekonomiska transaktioner på redovisningskonton och andra konton, till exempel bank- och leverantörskonton. Använd återkommande journaler för att bokföra periodiseringar och fördela saldon efter dimensionsvärden.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual, renumber, bulk-post
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d452720f5fff046a994ff5df0b2ea7bb5a209236
ms.sourcegitcommit: 652e4b0e1a09bff265014d9f8eb3b038ab0db79e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087725"
---
# <a name="working-with-general-journals"></a>Arbeta med redovisningsjournaler

De flesta finansiella transaktioner bokförs i redovisningen genom särskilda dokument, till exempel inköpsfakturor och försäljningsorder. Men du kan också bearbeta affärsaktiviteter, till exempel inköp, utbetalning, användning av återkommande journaler för att bokföra periodiseringar eller återbetalning av anställdas utgifter genom att bokföra journalrader i olika journaler i [!INCLUDE[prod_short](includes/prod_short.md)].  

De flesta journalerna baseras på *redovisningsjournalen* och du kan bearbeta alla transaktioner på sidan **redovisningsjournal**. Mer information finns i [Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).  

Du kan till exempel använda anställdas utgifter med egna pengar för affärsrelaterade utgifter för senare återbetalning. Mer information finns i [Så här registrerar du och återbetalar personalens utgifter](finance-how-record-reimburse-employee-expenses.md).

Men i de flesta fall vill du använda journaler som är optimerade för vissa typer av transaktioner såsom **betalningsjournal** för att registrera betalningar. Mer information finns i [Registrera betalningar och återbetalningar i betalningsjournalen](payables-how-post-payments-refunds.md).  

Du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner direkt på redovisningskonton och andra konton, till exempel bank-, leverantörs- och personalkonton. När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton. Så sker till exempel även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall.

Den information som du anger i en journal är tillfällig och kan ändras så länge den finns i journalen. När du bokför journalen, överförs informationen till transaktioner på enskilda konton, där den inte kan ändras. Du kan emellertid ta bort kopplingar från bokförda transaktioner och bokföra återförande eller rättande transaktioner. Mer information finns i [återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Använda Journalmallar och journaler

Det finns flera redovisningsjournalmallar. Varje journalmall representeras av en dedikerad sida med särskilda funktioner och fälten som krävs för att stödja dessa funktioner, till exempel sidan **Betalningsavstämningsjournal** för att bearbeta bankbetalningar och sidan **Betalningsjournal** för att betala dina leverantörer eller återbetala dina anställda. Mer information finns i [Gör betalningar](payables-make-payments.md) och [Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner](receivables-how-apply-sales-transactions-manually.md).

För varje journalmall kan du skapa din egen personliga journal som en journal. Du kan till exempel ange din egen journal för betalningsjournalen som har din personliga layout och inställningar. Följande tips är ett exempel på hur du anpassar en journal.

> [!TIP]  
> Om du väljer kryssrutan **Föreslå saldobelopp** på raden för din journal på sidan **Redovisningsjournaler** kommer fältet **Belopp** till exempel, redovisningsjournalrader för samma verifikationsnummer automatiskt att fyllas i med värdet som krävs för att hantera dokumentet. Mer information finns i [Låta [!INCLUDE[prod_short](includes/prod_short.md)] föreslå värden](ui-let-system-suggest-values.md).

> [!TIP]
> Om du vill lägga till eller ta bort fält i journaler använder du den **personliga** banderollen. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Validera redovisningsjournaler
För att förhindra fördröjningar vid bokföring kan du aktivera en bakgrundskontroll som meddelar dig när det finns ett misstag i den redovisningsjournal som du arbetar med så att du inte kan bokföra journalen. På sidan **Redovisningsjournal** kan du välja **Felkontroll i bakgrunden** om du vill att [!INCLUDE[prod_short](includes/prod_short.md)] validerar finansiella journaler, till exempel redovisnings- eller utbetalningsjournaler, medan du arbetar med dem. 

När du aktiverar valideringen visas faktaboxen **Journalkontroll** intill journalraderna, där ärenden visas på den aktuella raden och i hela partiet. Valideringen sker när du läser in en finansiell journal och väljer en annan journalrad. Panelen **Ärenden totalt** i faktaboxen visar det totala antalet ärenden som [!INCLUDE[prod_short](includes/prod_short.md)] hittade, och du kan välja att den öppnar en översikt över ärendena. 

Du kan använda åtgärderna **Visa rader med ärenden** och **Visa alla rader** för att växla mellan journalrader som har eller inte har några ärenden. Den nya faktaboxen **Journalradsinformation** ger snabb överblick över och åtkomst till data från journalrader, till exempel redovisningskonto, kund eller leverantör, samt bokföringsinställningarna för specifika konton.     

### <a name="reversing-journals-to-correct-mistakes"></a>Återföra journaler för att korrigera misstag
När du arbetar med journaler som har många rader och något går fel, är det viktigt att du har ett enkelt sätt att korrigera misstag. På sidan **Bokförd redovisningsjournal** finns några åtgärder som kan hjälpa dig.

* **Kopiera valda rader till journal** – Kopiera endast de rader som du väljer.
* **Kopiera redovisningsjournal till journal** – Kopiera alla rader som tillhör samma bokförda redovisningsjournal.

Med hjälp av dessa åtgärder kan du skapa en kopia av en rad i redovisningsjournal eller en batch och sedan ange följande:

* Den journal som du kopierar raderna till
* Om motsatta tecken (en journal som återförs)
* Ett annat bokföringsdatum eller verifikationsnummer

Om du vill tillåta att journaler kopieras till bokförda redovisningsjournaler går du till sidan **Redovisningsjournalmallar** och markerar kryssrutan **Kopiera till bokförda journalrader**. När du tillåter att användare kopierar bokförda redovisningsjournaler kan du, om så behövs, inaktivera kopiering av specifika journaler.

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Förstå Huvudkonton och motkonton
Om du har skapat standardmotkonton för journalerna på sidan **Redovisningsjournaler** fylls motkontot i automatiskt när du fyller i fältet **Kontonr**. Annars fyller du i både fältet **Kontonr** och fältet **Motkonto** manuellt. Ett positivt belopp i fältet **Belopp** debiteras på huvudkontot och krediteras på motkontot. Ett negativt belopp krediteras på huvudkontot och debiteras på motkontot.

> [!NOTE]  
> Moms beräknas separat för huvudkontot och motkontot, så att olika momssatser kan användas för dem.

## <a name="working-with-recurring-journals"></a>Arbeta med återkommande journaler
En återkommande journal är en redovisningsjournal med specifika fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar, till exempel hyra, prenumerationer, el och värme. Med fälten för återkommande transaktioner kan du bokföra både fasta och rörliga belopp. Du kan även ange automatiska återföringstransaktioner för dagen efter bokföringsdatum. Du kan även använda fördelningsnycklar för att dela upp återkommande transaktioner mellan olika konton. Mer information finns i avsnittet [Tilldela återkommande journalbelopp till flera olika konton](#allocating-recurring-journal-amounts-to-several-accounts).

Med en återkommande journal kommer transaktioner som ska bokföras regelbundet inte att behöva skrivas in mer än en gång. Det innebär att de konton, dimensioner och dimensionsvärden som du anger kommer att finnas kvar i journalen efter bokföring. Du kan göra eventuella justeringar i samband med varje bokföring.

### <a name="recurring-method-field"></a>Fält för återkommande metod

Detta fält bestämmer hur beloppet på journalraden hanteras efter bokföring. Om du t. ex. vill använda samma belopp varje gång du bokför raden kan du låta beloppet stå kvar. Om du vill använda samma konton och samma text på raden och bara ändra beloppet varje gång du bokför, kan du låta beloppet raderas varje gång du har bokfört.

| Till | Gå till |
| --- | --- |
|F Fast|Journalradens antal kommer att stå kvar när du har bokfört.|
|V Variabel|Journalradens antal kommer att tas bort när du har bokfört.|
|S Saldo|Det bokförda beloppet på kontot på raden kommer att fördelas på de konton som angetts för raden i tabellen Allm. journ. tilldeln. Saldot på kontot blir på det sättet nollställt. Kom ihåg att fylla i fältet **Fördelning %** på sidan **Fördelningar**. Mer information finns i avsnittet [Tilldela återkommande journalbelopp till flera olika konton](#allocating-recurring-journal-amounts-to-several-accounts).|
|ÅF Återföring fast|Journalradens belopp kommer att stå kvar efter det att du har bokfört och en mottransaktion kommer att bokföras nästa dag.|
|ÅV Återföring variabel|Journalradens belopp kommer att tas bort efter det att du har bokfört och en mottransaktion kommer att bokföras på nästa dag.|
|AB Återföring saldo|Det bokförda beloppet på kontot på raden kommer att fördelas på de konton som angetts för raden på sidan **Fördelningar**. Saldot på kontot anges till noll, och en mottransaktion bokförs på nästa dag.|
|BD Saldo efter dimension|Journalraden fördelar kostnader baserat på ett redovisningskontos saldo efter dimension. Du uppmanas att ange de dimensionsfilter som ska användas för att beräkna källredovisningskontots saldo efter dimension som du vill fördela kostnader från. Du kan också välja åtgärden **Dimensionsfilter** senare.|
|RBD Återföring saldo efter dimension|Journalraden fördelar kostnader baserat på ett redovisningskontos återföringssaldo efter dimension. Du uppmanas att ange de dimensionsfilter som ska användas för att beräkna källredovisningskontots saldo efter dimension som du vill fördela kostnader från. Du kan också välja åtgärden **Dimensionsfilter** senare.|

> [!NOTE]  
> Momsfälten kan fyllas i antingen på raden i den återkommande journalen eller på raden i fördelningsjournalen, men inte på båda raderna. Det går med andra ord bara att fylla i dem på sidan **Fördelningar** om motsvarande rader i den återkommande journalen inte är ifyllda.

### <a name="recurring-frequency-field"></a>Fält för återkommande frekvens
Detta fält bestämmer hur ofta transaktionen i journalraden ska bokföras. Det är ett formelfält för datum och måste fyllas i för återkommande journalrader. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Exempel
Om journalraden måste bokföras varje månad skriver du "1M". Varje gång du har bokfört kommer datumet i fältet **Bokföringsdatum** att uppdateras till samma datum nästa månad.

Om du vill bokföra en transaktion till den sista dagen i varje månad kan du göra på något av följande sätt:

- Bokför den första transaktionen på den sista dagen i en månad genom att ange 1D+1M-1D (1 dag + 1 månad – 1 dag). Med den här formeln beräknas bokföringsdatumet korrekt oberoende av antalet dagar i månaden.

- Bokför den första transaktionen på en valfri dag i månaden genom att ange 1M+LM. Med en här formeln inträffar bokföringsdatumet efter en hel månad + den löpande månadens återstående dagar.

### <a name="expiration-date-field"></a>Fält för utgångsdatum
Detta fält bestämmer vilket datum raden ska bokföras för sista gången. Raden kommer inte att bokföras efter detta datum.

Fördelen med att använda fältet är att raden inte kommer att raderas från journalen direkt. Du kan alltid ersätta slutdatumet med ett senare datum så att du kan använda raden längre.

Om fältet är tomt kommer raden att bokföras varje gång du bokför tills raden tas bort från journalen.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Fördela återkommande journalbelopp på flera konton

På sidan **Återkommande redovisningsjournal** kan du välja åtgärden **Fördelningar** för att visa eller hantera hur belopp på den återkommande journalraden fördelas på flera konton och dimensioner. Notera att fördelningen fungerar som en balanskontorad visavi den återkommande journalraden.

Liksom i en återkommande journal behöver du bara skriva in en fördelning en gång. Fördelningen kommer att stå kvar i fördelningsjournalen när du har bokfört, så du behöver inte skriva in belopp och fördelningar varje gång du bokför den återkommande journalraden.

Om den *återkommande metoden* i den återkommande journalen har angetts som **Saldo** eller **Återföring saldo** ignoreras alla dimensionsvärdekoder i den återkommande journalen när kontot är nollställt. Det betyder att om du fördelar en återkommande rad på olika dimensionsvärden på sidan **Fördelningar**, så skapas bara en återföringstransaktion. Om du fördelar en återkommande journalrad som innehåller en dimensionsvärdekod får du därför inte ange samma kod på sidan **Fördelningar**. Om du gör detta kommer dimensionsvärdena att bli felaktiga.  

Om du vill fördela återkommande journalbelopp baserat på dimensioner anger du fältet **Återkommande metod** som **Saldo efter dimension** eller **Återföra saldo efter dimension** istället. Om den återkommande metoden i den återkommande journalen har angetts som **Saldo efter dimension** eller **Återföra saldo efter dimension** beaktas alla dimensionsvärdekoder i den återkommande journalen när kontot är nollställt. Om du allokerar en återkommande rad till olika dimensionsvärden på sidan **Allokeringar** skapas därför ett antal återföringstransaktioner som matchar antalet dimensionsvärdekombinationer som saldot består av. Om du allokerar kontosaldo via den återkommande journalen som innehåller en dimensionsvärdekod, kom då ihåg att använda **Saldo efter dimension** eller **Återföra saldo efter dimension** för att se till att dimensionsvärdena är korrekt balanserade eller återförda från källkontot.  

Ditt företag har till exempel ett par affärsenheter och en handfull avdelningar som dina controllers har ställt in som dimensioner. Om du vill påskynda transaktionsprocessen för inköpsfakturor bestämmer du dig för att kräva att leverantörsreskontramedarbetarna endast anger affärsenhetsdimensioner. Eftersom varje affärsenhet har specifika fördelningsnycklar för avdelningsdimensionen - till exempel baserat på antalet medarbetare - kan du använda de återkommande metoderna för **BD-saldo efter dimension** eller **RBD-återföringssaldo efter dimension** för att omfördela utgifter för respektive affärsenhet till rätt avdelningar baserat på fördelningsnycklarna.  

> [!NOTE]
> Dimensioner som du anger på allokeringsrader beräknas inte automatiskt, utan du måste ange vilka dimensionsvärden som måste anges på fördelningskontona. Om du vill bevara kopplingen mellan källkontodimensionen och fördelningskontodimensionen rekommenderar vi att du använder funktionen för [Kostnadsfördelning](finance-about-cost-accounting.md) istället.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Exempel: Fördela hyresinbetalningar på olika avdelningar
Du betalar hyra varje månad, så du har skrivit in hyresbeloppet på kassakontot på en återkommande journalrad. På sidan **Fördelningar** kan du dela upp utgiften mellan ett flertal avdelningar (dimensionen Avdelning) i enlighet med det antal kvadratmeter som respektive avdelning tar i anspråk. Beräkningen grundas på procentandelen för fördelning på respektive rad. Du kan ange olika konton på olika fördelningsrader (om hyran också ska delas upp på flera konton) eller ange samma konto fast med olika dimensionsvärdekoder för dimensionen Avdelning på respektive rad.

### <a name="reversal-date-calculation"></a>Beräkning av återföringsdatum
När du använder återkommande redovisningsjournaler för att bokföra periodiseringar vid slutet av en period är det viktigt att du har full kontroll över återföringstransaktioner. På sidan **Återkommande redovisningsjournaler** kan du med hjälp av fältet **Beräkning av återföringsdatum** kontrollera det datum som återföringstransaktionerna ska bokföras när metoder för återkommande återförsel används.

#### <a name="example"></a>Exempel
Periodiseringar bokförs vanligtvis med metoderna Fast, Variabel eller Balansering på journalraden. Bokföringsdatumet för det bokförda beloppet på kontot på journalraden beräknas med den återkommande frekvensen. Bokföringsdatumet för mottransaktionen beräknas med hjälp av fältet **Beräkning av återföringsdatum** enligt följande:

* Om fältet är tomt kommer mottransaktionen att bokföras nästa dag.
* Om fältet innehåller en datumformel (t. ex. **5D** för fem dagar), bokförs mottransaktionen med ett bokföringsdatum beräknat med hjälp av beräkningen av återföringsdatum.

> [!NOTE]
> Som standard är fältet **Beräkning av återföringsdatum** inte tillgängligt på sidan **Återkommande redovisningsjournaler**. Om du vill använda fältet måste du lägga till det genom att anpassa sidan. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

## <a name="working-with-standard-journals"></a>Arbeta med Standardjournaler
När du har skapat journalrader som du vet att du förmodligen kommer att skapa igen, kan du spara dem som en standardjournal innan du bokför journalen. Den här funktionen gäller artikeljournaler och redovisningsjournaler.

> [!NOTE]  
>   Följande procedur gäller för artikeljournalen, men informationen kan också tillämpas på redovisningsjournalen.

### <a name="to-save-a-standard-journal"></a>Så här sparar du som en standardjournal
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager artikeljournaler** och välj sedan relaterad länk.
2. Mata på en eller flera journalrader.
3. Markera de journalrader som du vill återanvända.
4. Välj åtgärden **Spara som standardjournal**.
5. På sidan **Spara som standardartikeljournal** måste du definiera en ny eller befintlig standardartikeljournal som raderna ska sparas i:

    Om du redan har skapat en eller flera standardartikeljournaler och du vill ersätta någon av dessa med den nya uppsättningen artikeljournalrader, i fältet Kod och välja koden.
6. Välj knappen **OK** för att bekräfta att du vill skriva över den befintliga standardartikeljournalen och byta ut allt innehåll.
7. Välj fältet **Spara a-pris**, om du vill spara värdena i fältet **A-pris** i standardartikeljournalen.
8. Välj fältet **Spara antal**, om du vill att appen ska spara värdena i fältet **Antal**.
9. Välj knappen **OK** för att spara standardartikeljournalen.

När du har sparat standardartikeljournalen visas sidan Artikeljournal så att du kan fortsätta att bokföra den, samtidigt som du vet att den lätt kan återskapas nästa gång du bokför samma eller likartade rader.

### <a name="to-reuse-a-standard-journal"></a>Så här återanvänder du standardjournaler

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager artikeljournaler** och välj sedan relaterad länk.
2. Välj åtgärden **Få standardjournal**.

    Sidan Standardartikeljournaler visas med koder och beskrivningar för alla befintliga standardartikeljournaler.
3. Om du vill förhandsgranska en standardartikeljournal innan du väljer att återanvända den, klickar du på **Visa journal**.

    Alla ändringar som du gör i en standardartikeljournal införs omedelbart. De finns där nästa gång du öppnar eller återanvänder standardartikeljournalen i fråga. Du bör därför vara säker på att ändringen är tillräckligt viktig för att tillämpa allmänt. Annars skapar du den specifika ändringen i artikeljournalen efter att standardartikeljournalraderna har infogats. Se punkt 4 nedan.
4. När du kommer tillbaka till sidan **Standardartikeljournaler** väljer du den standardartikeljournal som du vill återanvända och klickar på **OK**.

    Nu är artikeljournalen ifylld med raderna som du har sparat som standardartikeljournal. Om det redan finns journalrader i artikeljournalen, placeras de infogade raderna under de befintliga journalraderna.

    Om du inte markerade fältet **Spara enhetsbelopp** när du använde funktionsjobbet **Spara som standardartikeljournal**, innebär detta att fältet **Enhetsbelopp** på rader som infogas från standardjournalen automatiskt kommer att fyllas med artikelns aktuella värde (kopieras från fältet **Styckkostnad** på artikelkortet).

    > [!NOTE]  
    > Om du har markerat fältet **Spara a-pris** eller **Spara antal** ska du nu kontrollera att de infogade värdena är korrekta för den här speciella lagerjusteringen innan du bokför artikeljournalen.

    Om de infogade artikeljournalraderna innehåller sparade a-priser som du inte vill bokföra, kan du snabbt justera dem till artikelns aktuella värde:

5. Välj de artikeljournalrader som du vill justera lagret för och välj sedan åtgärden **Omberäkna a-pris**. Då uppdateras fältet A-pris med artikelns aktuella styckkostnad.
6. Välj åtgärden **Bokföra**.

## <a name="to-renumber-document-numbers-in-journals"></a>Numrera om verifikationsnummer i journaler

Du kan använda funktionen **Numrera om nummer** innan du bokför en journal, för att kontrollera att du inte får bokföringsfel p.g.a. dokumentets nummerordning.

I alla journaler som är baserade på redovisningsjournalen är fältet **Dokumentnr** redigerbart så att du kan ange olika nummer för olika journalrader eller samma verifikationsnummer för relaterade journalrader.

Om fältet **Nr-serie** på journalen fylls, kräver bokföringsfunktionen i redovisningsjournaler att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. Välj bara åtgärden **Numrera om dokumentnummer** så uppdateras relevanta **Dokumentnr**-fält. Om relaterade rader grupperades efter verifikationsnummer innan du använde funktionen, förblir de grupperade men kan tilldelas ett annat verifikationsnummer.  

Den här funktionen fungerar även på filtrerade vyer.

Alla omnumreringen av verifikationsnummer skall respektera relaterade tillämpningar, som en ansökan om betalningstillämpning som har gjorts från dokumentet på journalraden till ett leverantörskonto. I enlighet med detta kan fälten **Koppla till ID** och **Koppla till ver.nr.** i de berörda transaktionerna uppdateras.

### <a name="to-renumber-documents-in-journals"></a>Numrera om dokument i journaler

Följande procedur är baserad på sidan **Redovisningsjournal**, men gäller för alla andra journaler som baseras på den redovisningsjournalen, t. ex. sidan **Utbetalningsjournal**.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. När du är klar att bokföra journalraderna väljer du **Numrera om dokumentnummer**.

Värden i fältet **Dokumentnr** ändras, om så krävs, så att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. När dokument numreras kan du fortsätta att bokföra journalen.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
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