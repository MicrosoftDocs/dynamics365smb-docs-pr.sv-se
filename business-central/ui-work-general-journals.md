---
title: Använda en redovisningsjournal för att bokföra direkt i redovisningen | Microsoft Docs
description: Lär hur du använder journaler för att bokföra ekonomiska transaktioner på redovisningskonton och andra konton, till exempel bank- och leverantörskonton.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 5ea488bc03ffa64b0d6c4b5c1466ddf01ca52ab1
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953905"
---
# <a name="working-with-general-journals"></a>Arbeta med redovisningsjournaler

De flesta finansiella transaktioner bokförs i redovisningen genom särskilda dokument, till exempel inköpsfakturor och försäljningsorder. Men du kan också bearbeta affärsaktiviteter, till exempel inköp, utbetalning och återbetalning av anställdas utgifter genom att bokföra journalrader i olika journaler i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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
> Om du väljer kryssrutan **Föreslå saldobelopp** på raden för din journal på sidan **Redovisningsjournaler** kommer fältet **Belopp** till exempel, redovisningsjournalrader för samma verifikationsnummer automatiskt att fyllas i med värdet som krävs för att hantera dokumentet. Mer information finns i [Låta [!INCLUDE[d365fin](includes/d365fin_md.md)] föreslå värden](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Förstå Huvudkonton och motkonton
Om du har skapat standardmotkonton för journalerna på sidan **Redovisningsjournaler** fylls motkontot i automatiskt när du fyller i fältet **Kontonr**. Annars fyller du i både fältet **Kontonr** och fältet **Motkonto** manuellt. Ett positivt belopp i fältet **Belopp** debiteras på huvudkontot och krediteras på motkontot. Ett negativt belopp krediteras på huvudkontot och debiteras på motkontot.

> [!NOTE]  
>   Moms beräknas separat för huvudkontot och motkontot, så att olika momssatser kan användas för dem.

## <a name="working-with-recurring-journals"></a>Arbeta med återkommande journaler
En återkommande journal är en redovisningsjournal med specifika fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar, till exempel hyra, prenumerationer, el och värme. Med fälten för återkommande transaktioner kan du bokföra både fasta och rörliga belopp. Du kan även ange automatiska återföringstransaktioner för dagen efter bokföringsdatum. Du kan även använda fördelningsnycklar för att dela upp återkommande transaktioner mellan olika konton. Mer information finns i avsnittet [Tilldela återkommande journalbelopp till flera olika konton](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Med en återkommande journal kommer transaktioner som ska bokföras regelbundet inte att behöva skrivas in mer än en gång. Det innebär att de konton, dimensioner och dimensionsvärden som du anger kommer att finnas kvar i journalen efter bokföring. Du kan göra eventuella justeringar i samband med varje bokföring.

### <a name="recurring-method-field"></a>Fält för återkommande metod
Detta fält bestämmer hur beloppet på journalraden hanteras efter bokföring. Om du t.ex. vill använda samma belopp varje gång du bokför raden kan du låta beloppet stå kvar. Om du vill använda samma konton och samma text på raden och bara ändra beloppet varje gång du bokför, kan du låta beloppet raderas varje gång du har bokfört.

| Till | Gå till |
| --- | --- |
|Fast|Journalradens antal kommer att stå kvar när du har bokfört.|
|Olika|Journalradens antal kommer att tas bort när du har bokfört.|
|Saldo t.o.m. datum|Det bokförda beloppet på kontot på raden kommer att fördelas på de konton som angetts för raden i tabellen Allm. journ. tilldeln. Saldot på kontot blir på det sättet nollställt. Kom ihåg att fylla i fältet **Fördelning %** på sidan **Fördelningar**. Mer information finns i avsnittet [Tilldela återkommande journalbelopp till flera olika konton](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Återföring fast|Journalradens belopp kommer att stå kvar efter det att du har bokfört och en mottransaktion kommer att bokföras nästa dag.|
|Återföring variabel|Journalradens belopp kommer att tas bort efter det att du har bokfört och en mottransaktion kommer att bokföras på nästa dag.|
|Återföring balansering|Det bokförda beloppet på kontot på raden kommer att fördelas på de konton som angetts för raden på sidan **Fördelningar**. Saldot på kontot anges till noll, och en mottransaktion bokförs på nästa dag.|

> [!NOTE]  
>  Momsfälten kan fyllas i antingen på raden i den återkommande journalen eller på raden i fördelningsjournalen, men inte på båda raderna. Det går med andra ord bara att fylla i dem på sidan **Fördelningar** om motsvarande rader i den återkommande journalen inte är ifyllda.

### <a name="recurring-frequency-field"></a>Fält för återkommande frekvens
Detta fält bestämmer hur ofta transaktionen i journalraden ska bokföras. Det är ett formelfält för datum och måste fyllas i för återkommande journalrader. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Exempel
Om journalraden måste bokföras varje månad skriver du "1M". Varje gång du har bokfört kommer datumet i fältet **Bokföringsdatum** att uppdateras till samma datum nästa månad.

Om du vill bokföra en transaktion till den sista dagen i varje månad kan du göra på något av följande sätt:

- Bokför den första transaktionen på den sista dagen i en månad genom att ange 1D+1M-1D (1 dag + 1 månad - 1 dag). Med den här formeln beräknas bokföringsdatumet korrekt oberoende av antalet dagar i månaden.

- Bokför den första transaktionen på en valfri dag i månaden genom att ange 1M+LM. Med en här formeln inträffar bokföringsdatumet efter en hel månad + den löpande månadens återstående dagar.

### <a name="expiration-date-field"></a>Fält för utgångsdatum
Detta fält bestämmer vilket datum raden ska bokföras för sista gången. Raden kommer inte att bokföras efter detta datum.

Fördelen med att använda fältet är att raden inte kommer att raderas från journalen direkt. Du kan alltid ersätta slutdatumet med ett senare datum så att du kan använda raden längre.

Om fältet är tomt kommer raden att bokföras varje gång du bokför tills raden tas bort från journalen.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Fördela återkommande journalbelopp på flera konton
På sidan **Återkommande redovisningsjournal** kan du välja åtgärden **Fördelningar** för att visa eller hantera hur belopp på den återkommande journalraden fördelas på flera konton och dimensioner. Notera att fördelningen fungerar som en balanskontorad visavi den återkommande journalraden.

Liksom i en återkommande journal behöver du bara skriva in en fördelning en gång. Fördelningen kommer att stå kvar i fördelningsjournalen när du har bokfört, så du behöver inte skriva in belopp och fördelningar varje gång du bokför den återkommande journalraden.

Om den återkommande metoden i den återkommande journalen har angetts som **Saldo** or **Återföring saldo** ignoreras alla dimensionsvärdekoder i den återkommande journalen när kontot är nollställt. Det betyder att om du fördelar en återkommande rad på olika dimensionsvärden på sidan **Fördelningar**, så skapas bara en återföringstransaktion. Om du fördelar en återkommande journalrad som innehåller en dimensionsvärdekod får du därför inte ange samma kod på sidan **Fördelningar**. Om du gör detta kommer dimensionsvärdena att bli felaktiga.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Exempel: Fördela hyresinbetalningar på olika avdelningar
Du betalar hyra varje månad, så du har skrivit in hyresbeloppet på kassakontot på en återkommande journalrad. På sidan **Fördelningar** kan du dela upp utgiften mellan ett flertal avdelningar (dimensionen Avdelning) i enlighet med det antal kvadratmeter som respektive avdelning tar i anspråk. Beräkningen grundas på procentandelen för fördelning på respektive rad. Du kan ange olika konton på olika fördelningsrader (om hyran också ska delas upp på flera konton) eller ange samma konto fast med olika dimensionsvärdekoder för dimensionen Avdelning på respektive rad.

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

    Om du inte markerar fältet **Spara a-pris** under när du använde funktionsjobbet **Spara som standardartikeljournal** innebär detta att fältet **A-pris** på raderna som infogas från standardjournalen  automatiskt kommer att fyllas med artikelns aktuella värde (kopieras från fältet **Styckkostnad** på artikelkortet).

    > [!NOTE]  
    >   Om du har markerat fältet **Spara a-pris** eller **Spara antal** ska du nu kontrollera att de infogade värdena är korrekta för den här speciella lagerjusteringen innan du bokför artikeljournalen.

    Om de infogade artikeljournalraderna innehåller sparade a-priser som du inte vill bokföra, kan du snabbt justera dem till artikelns aktuella värde:

6. Välj de artikeljournalrader som du vill justera lagret för och välj sedan åtgärden **Omberäkna a-pris**. Då uppdateras fältet A-pris med artikelns aktuella styckkostnad.
7. Välj åtgärden **Bokföra**.

## <a name="to-renumber-document-numbers-in-journals"></a>Numrera om verifikationsnummer i journaler
Du kan använda funktionen **Numrera om nummer** innan du bokför en journal, för att kontrollera att du inte får bokföringsfel p.g.a. dokumentets nummerordning.

I alla journaler som är baserade på redovisningsjournalen är fältet **Dokumentnr** redigerbart så att du kan ange olika nummer för olika journalrader eller samma verifikationsnummer för relaterade journalrader.

Om fältet **Nr-serie** på journalen fylls, kräver bokföringsfunktionen i redovisningsjournaler att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. Du kan använda funktionen **Numrera om nummer** innan du bokför journalen, för att kontrollera att du inte får bokföringsfel p.g.a. dokumentets nummerordning. Om relaterade rader grupperades efter verifikationsnummer innan du använde funktionen, förblir de grupperade men kan tilldelas ett annat verifikationsnummer.

Den här funktionen fungerar även på filtrerade vyer.

Alla omnumreringen av verifikationsnummer skall respektera relaterade tillämpningar, som en ansökan om betalningstillämpning som har gjorts från dokumentet på journalraden till ett leverantörskonto. I enlighet med detta kan fälten **Koppla till ID** och **Koppla till ver.nr.** i de berörda transaktionerna uppdateras.

Följande procedur är baserad på sidan **Redovisningsjournal**, men gäller för alla andra journaler som baseras på den redovisningsjournalen, t.ex. sidan **Utbetalningsjournal**.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. När du är klar att bokföra journalraderna väljer du **Numrera om dokumentnummer**.

Värden i fältet **Dokumentnr** ändras, om så krävs, så att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. När dokument numreras kan du fortsätta att bokföra journalen.

## <a name="see-related-training-at-microsoft-learnlearnpathsuse-journals-dynamics-365-business-central"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Se även
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Fördela kostnader och intäkter](year-allocate-costs-income.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
