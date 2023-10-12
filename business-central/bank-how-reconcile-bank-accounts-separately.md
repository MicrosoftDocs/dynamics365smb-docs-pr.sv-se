---
title: Stämma av bankkonton
description: Lära dig hur du stämmer av transaktioner i Business Central med transaktioner i kontoutdragen från din bank.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Stämma av bankkonton

Bankavstämningen säkerställer att det som finns i dina böcker matchar de utdrag som du får från banken. Bankkontoavstämningen jämför och matchar transaktionerna i de bankkonton som du har skapat i [!INCLUDE[prod_short](includes/prod_short.md)] med banktransaktioner hos banken. Vid avstämningen kan du bokföra saldona till dina bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)] så att de blir tillgängliga för ekonomichefer. Bankavstämning är också ett praktiskt sätt att upptäcka och lösa problem med saknade betalningar och bokföringsfel.

I den här artikel beskrivs hur du stämmer av bankkonton från sidan **Bankkontoavstämning**.

Du kan också stämma av bankkonton på sidan **Betalningsavstämningsjournal** när du bearbetar betalningar. Öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer åtgärden **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för de betalningar som du bokför med journalen. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I Nordamerika kan du också utföra detta arbete på sidan **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler. Du använder den här sidan i stället för sidan **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** på sidan **Redovisningsinställningar**. Mer information finns i avsnittet [stämma av bankkonton](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Förenta staterna: lokal funktion.

Raderna på sidan **Bankkontoavstämning** är uppdelade i två rutor. Rutan **Bankkontoavstämning** visar antingen importerade banktransaktioner eller transaktioner med utestående utbetalningar. Rutan **Bankkontotransaktioner** visar transaktionerna på det interna bankkontot.

Avstämning av transaktioner i utdrag från banken med banktransaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] kallas *matchning*. Det finns två sätt att matcha transaktioner med banktransaktioner:

* Du kan matcha automatiskt med åtgärden **Matcha automatiskt**.
* Du kan manuellt välja rader i båda fönster för att koppla varje kontoutdragsrad till en eller flera motsvarande bankkontotransaktioner och sedan använda åtgärden **Matcha manuellt**.

Kryssrutan **Kopplad** markeras på rader där transaktioner matchas. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md). Om du anger ett slutdatum för utdraget i bankkontoavstämningen efter att du har matchat raderna med transaktioner, kommer [!INCLUDE [prod_short](includes/prod_short.md)] att återställa matchningarna för rader och transaktioner som inträffar efter detta datum.

> [!NOTE]
> När du har angett ett datum i fältet Slutdatum för kontoutdraget, filtrerar sidan bankkontotransaktionerna banktransaktionerna så att endast transaktioner fram till det datumet visas. Du kan bara bokföra bankkontoavstämningar med banktransaktioner på eller före slutdatum för kontoutdraget. Filtret ser till att bankens redovisning balanseras med bankkontoutdraget på slutdatum för utdraget, med skillnaden som utestående betalningar och checkar.

När värdet i fältet **Total saldo** i **Kontoutdragrader** är lika med det totala värdet av **Bankkontotransaktioner** plus fältet **Saldo för senaste kontoavstämning** i **Bankkontotransaktioner** kan du välja **Bok**. Omatchat bankkontotransaktioner kommer att finnas kvar på sidan, vilket indikerar en viss avvikelse som du bör lösa för att stämma av bankkontot.

Alla rader som inte kan matchas, vilket anges med ett värde i fältet **Skillnad**, finns kvar på sidan **Bankkontoavstämning** efter bokföring. De representerar någon form av avvikelse som du måste lösa innan du kan slutföra bankkontoavstämningen. I tabellen nedan beskrivs några typiska affärssituationer som kan orsaka skillnader.

| Differens | Orsak | Åtgärd |
|------------|--------|------------|
| En transaktion i bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] finns inte med på kontoutdraget. | Banktransaktionen skapades inte trots att en bokföring gjordes i [!INCLUDE[prod_short](includes/prod_short.md)]. | Skapa den saknade transaktionen (eller be en gäldenär att utföra den). Importera sedan bankutdragsfilen eller ange transaktionen manuellt. |
| En transaktion på kontoutdraget finns inte som ett dokument eller en journalrad i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaktion gjordes utan motsvarande bokföring i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en journalradsbokföring för en utgift. | Skapa och bokför den saknade transaktionen. Information om ett snabbt sätt att göra detta på finns i [Så här skapar du saknade transaktioner för att matcha banktransaktioner med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| En transaktion i det interna bankkontot motsvarar en banktransaktion, men viss information är för annorlunda för att ge en matchning. | Information, till exempel belopp eller kundnamn, angavs på olika sätt i banktransaktionen eller den interna bokföringen. | Granska informationen och matcha sedan de två manuellt. Du kan också korrigera matchningsfelet. |

Du måste lösa skillnaderna, till exempel genom att skapa saknade poster och korrigera icke-matchande information, eller genom att utföra saknade penningtransaktioner, tills du kan slutföra och bokföra bankkontoavstämningen.

Du kan fylla i rutan **Kontoutdragrader** på sidan **Bankkontoavstämning** på följande sätt:

* Automatiskt: Genom att använda funktionen **Import kontoutdrag** för att fylla i rutan **Kontoutdragsrad** med bankkontotransaktioner som baseras på en importerad fil eller ström som tillhandahålls av banken.
* Manuellt: Genom att använda funktionen **Föreslå rader** för att fylla i rutan **Kontoutdragsrader** i enlighet med fakturor i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalningar.

## Lägg till bankutdragsrader genom att importera ett kontoutdrag

Fönstret **Kontoutdragsrader** fylls med banktransaktioner enligt en importerad fil eller ström som tillhandahålls av banken.

Om du vill importera bankutdrag som bankflöden måste du ställa in tjänsten Envestnet Yodlee Bank Feed. Konfigurationen inbegriper länkning av dina bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)] till de relaterade onlinebankkontona. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan också importera bankutdragsfiler i komma- eller semikolonavgränsat format (.CSV). Använd **Konfigurera importformat för en kontoutdragsfil** assisterad installation för att definiera importformat för kontoutdrag och bifoga formatet till ett bankkonto. Du kan sedan använda dessa format när du importerar bankutdrag på sidan **Bankkontoavstämning**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **bankkontoavstämning** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Välj ett bankkonto i fältet **Bankkontonr**. Bankkontotransaktionerna som finns på bankkonto, visas i rutan **Bankkontotransaktioner**.
4. Ange datumet på kontoutdraget från banken i fältet **Kontoutdragets datum**.
5. Ange saldot på kontoutdraget från banken i fältet **Kontoutdragets slutsaldo**.
6. Om du har en bankutdragsfil väljer du åtgärden **Importera bankutdrag**.
7. Leta upp filen och välj sedan knappen **Öppna** för att importera banktransaktionerna till rutan **Kontoutdragsrader** på sidan **Bankkontoavstämning**.

## Så här fyller du i bankavstämningrader med åtgärden Föreslå rader

Rutan **Kontoutdragsrader** fylls i enligt fakturorna i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalningar.  

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Föreslå rader**.
2. Ange det tidigaste bokföringsdatumet för transaktionsavstämningen i fältet **Startdatum**.
3. Ange det senaste bokföringsdatumet för transaktionsavstämningen i fältet **Slutdatum**.

    > [!NOTE]
    > Normalt motsvarar slutdatum det datum som har angetts i fältet **Kontoutdragets datum**. Om du däremot vill stämma av transaktionerna för endast en del av en period kan du ange ett annat slutdatum.

4. Om du inte vill att bankkontotransaktionerna ska ta med omatchade öppna återförda transaktioner väljer du alternativet **Ignorera återförda transaktioner**. Som standard inkluderar listan med bankkontotransaktioner återförda transaktioner fram till kontoutdragets datum.
5. Välj **OK**.

## Så här matchar du automatiskt kontoutdragrader med bankkontotransaktioner

Sidan **Bankkontoavstämning** erbjuder automatiskt matchande funktioner baserade på en textmatchning på en kontoutdragsrad (vänster ruta) med text på en eller flera redovisningstransaktioner för bankkontot (höger ruta). Du kan skriva över de föreslagna automatiska matchningarna, och du kan också välja att inte använda automatisk matchning alls. För mer information, se [Så här matchar du kontoutdragrader med bankkontotransaktioner manuellt](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Du kan undersöka basen för matchningar med hjälp av åtgärden **matcha detaljer**. Informationen innehåller t.ex. namnen på de fält som innehöll matchande värden.  

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Matcha automatiskt**. Sidan **Matcha banktransaktioner** öppnas.
2. Ange antalet dagar före och efter bankkontotransaktionbokföringsdatumet som åtgärden ska söka i för att matcha bokföringsdatum i bankkontoutdraget i fältet **Bokföringsdatumtolerans (dagar)**.

    Om du anger 0 eller lämnar fältet tomt kommer åtgärden **Matcha automatiskt** endast söka efter matchande bokföringsdatum på bankkontotransaktionbokföringsdatumet.
3. Välj **OK**.

    Raderna är färgkodade så att du lättare förstår vad du ska göra med dem. Kontoutdragsrader och bankkontotransaktioner som kan matchas på den aktuella bankavstämningen ändras till grönt teckensnitt med fetstil. Bankkontotransaktioner som är matchade med andra bankavstämningar visas med blått teckensnitt i kursiv stil.
4. Markera kontoutdragraden och välj sedan åtgärden **Ta bort matchning**.

> [!TIP]
> Du kan använda en blandning av manuell och automatisk matchning. Om du har manuellt matchade transaktioner skrivs inte dina val över med automatisk matchning.

## Så här matchar du manuellt bankutdragsrader med bankkontotransaktioner

> [!TIP]
> När du matchar rader och transaktioner manuellt kan åtgärderna **Visa alla**, **Visa återförda transaktioner**, **Dölj återförda transaktioner** och **Visa icke-matchande** göra det enklare att få en överblick. Som standard innehåller bankkontotransaktionerna inte omatchade återförda transaktioner. Om du vill ta med dessa poster i listan och matcha dem manuellt väljer du åtgärden **Visa återförda transaktioner**. Om du väljer att dölja återförda transaktioner när du har gjort en eller flera matchningar visas de matchade transaktionerna fortfarande.

> [!NOTE]
> Du kan inte bokföra en bankavstämning om du har flera-till-ett-matchande och de kombinerade beloppen innehåller differenser. Det här gäller även om de kombinerade skillnaderna blir noll.
>
> Här följer ett exempel på en många-till-ett-matchning med skillnader. Värdet 200 för bankutdragspost 1 matchas till två banktransaktioner som har ett totalt värde på 180. Differensen är 20. Värdet 350 för bankutdragspost 2 matchas till två andra banktransaktioner som har ett totalt värde på 370. Differensen är-20, vilket innebär att värdet 20 beräknas för bankutdrag 1.  
>
> Om du vill bokföra en bankavstämning med differenser på raderna bokför du differenserna och matchar dem för de bokförda transaktionerna.

1. På sidan **Bankkontoavstämning** markerar du en okopplad rad i rutan **Kontoutdragrader**.
2. I rutan **Bankkontotransaktioner** markerar du en eller flera bankkontotransaktioner som kan matchas med den valda kontoutdragraden. Om du vill välja flera rader, tryck och håll ned <kbd>CTRL</kbd>-tangenten och välj raderna.

   > [!TIP]
   > Du kan också matcha flera bankutdragsrader manuellt med en bankkontotransaktion. Det kan till exempel vara användbart om bankinsättningen innehöll flera betalningsmetoder, t.ex. kreditkort från olika utfärdare och din bank visar dem som separata rader.
3. Välj åtgärden **Matcha manuellt**.

    Den valda kontoutdragraden och de valda bankkontotransaktionerna ändrar till grönt teckensnitt och **Kopplat** kryssrutan i det högra fönstret markeras.
4. Upprepa moment 1 till och med 3 för alla kontoutdragrader som inte matchas.

> [!TIP]
> Markera kontoutdragraden och välj sedan åtgärden **Ta bort matchning**. Om du har matchat flera bankutdragsrader till en transaktion och behöver ta bort en eller flera av de matchade raderna, tas alla manuella matchningar bort för transaktionen när du väljer **ta bort matchning**.

## Så här validerar du bankavstämningen

Om du vill dubbelkolla bankkontoavstämningen innan du bokför den, kan du använda åtgärden **Testrapport** för att förhandsgranska avstämningen. Rapporten är tillgänglig i följande sammanhang:

* När du förbereder en bankkontoavstämning på sidan **Bankkontoavstämning**.
* När du stämmer av betalningar på sidan **Betalningsavstämningsjournal**.

Rader som inte kan matchas visas på sidan **Bankavstämning** när de har bokförts. Raderna innehåller ett värde i fältet **Differens**. Differensen representerar en avvikelse som du måste lösa innan du kan slutföra bankkontoavstämningen. I tabellen nedan beskrivs några typiska affärssituationer som kan orsaka skillnader.

| Differens | Orsak | Åtgärd |
|------------|--------|------------|
| En transaktion i bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] finns inte med på kontoutdraget. | Banktransaktionen skapades inte trots att en bokföring gjordes i [!INCLUDE[prod_short](includes/prod_short.md)]. | Skapa den saknade transaktionen (eller be en gäldenär att utföra den). Importera sedan bankutdragsfilen eller ange transaktionen manuellt. |
| En transaktion på kontoutdraget finns inte som ett dokument eller en journalrad i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaktion gjordes utan motsvarande bokföring i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en journalradsbokföring för en utgift. | Skapa och bokför den saknade transaktionen. Information om ett snabbt sätt att göra detta på finns i [Så här skapar du saknade transaktioner för att matcha banktransaktioner med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| En transaktion i det interna bankkontot motsvarar en banktransaktion, men viss information är för annorlunda för att ge en matchning. | Information, till exempel belopp eller kundnamn, angavs på olika sätt i banktransaktionen eller den interna bokföringen. | Granska informationen och matcha sedan de två manuellt. Du kan också korrigera matchningsfelet. |

Du måste lösa skillnaderna, till exempel genom att skapa saknade poster och korrigera icke-matchande information, eller genom att utföra saknade penningtransaktioner, tills du kan slutföra och bokföra bankkontoavstämningen.

> [!NOTE]
> Sidan bankavstämning och testrapport förutsätter att du bara synkroniserar under perioden fram till slutdatum för kontoutdraget. Om du matchar en kontoutdragsrad till en banktransaktion innan du skriver in ett slutdatum för kontoutdraget och sedan anger ett slutdatum för kontoutdraget som infaller efter slutdatumet för banktransaktionen, kommer data i testrapporten att bli fel.

I följande tabell beskrivs fälten på testrapporten, som kan hjälpa dig att slutföra bankavstämningen.

|Fält  |Description  |
|---------|---------|
|Kontoutdragets datum| Det datum som anges i fältet **Kontoutdragets** datum på sidan **Bankkontoavstämning**.|
|Saldo senaste kontoavstämning|Saldot anges i fältet **Saldo för senaste utdrag** datum på sidan **Bankkontoavstämning**. Det fylls i automatiskt med den senaste avstämningen för samma bankkonto. Värdet är noll om det är den första bankkontoavstämningen.|
|Kontoutdragets slutsaldo|Saldot anges i fältet **Kontoutdragets slutsaldo** på sidan **Bankkontoavstämning**. |
|Redovisningskontonr. <*nummer*> Saldo den <*datum*> | Saldot på redovisningskontot på slutdatum för kontoutdraget. Detta är det ofiltrerade saldot från och med det datumet. Om din bank använder din lokala valuta, bör saldot vara samma som ditt bankkontosaldo (som visas till höger i rapporthuvudet) när du har matchat alla utdragsrader. En tom **()** i namnet på det här fältet innebär att din bank använder lokal valuta.<br><br>En avvikelse i det här fältet och i föregående fält kan tyda på att du har bokfört direkt på redovisningskontot, eller att du använder samma redovisningskonto för flera banker, vilket inte rekommenderas. Bankerna kopplas till redovisningen via bankkontots bokföringsmall som angetts för kontot.<br><br>I testrapporten visas ett varningsmeddelande om du har direkt bokföring, även om saldot för bokföringen är noll. Direkt bokföring som inte är balanserad leder ofta till ackumulerade skillnader för framtida bankavstämningar. Kontrollera redovisningen och redovisningstransaktionerna innan du bokför bankkontoavstämningen. Om du vill ha mer information om direkt bokföring går du till [undvika direkt bokföring](#avoid-direct-posting).|
|Redovisningskontonr. <*nummer*> Saldo (<*LCY*>) den <*datum*>| Saldot på redovisningskontot på slutdatum för kontoutdraget i lokal valuta. Saldot omvandlas till bankkontots valuta med hjälp av valutakursen som är giltig på kontoutdragets slutdatum. Detta är det ofiltrerade saldot från och med det datumet. Du jämför med detta med fältet **Redovisningskontonr. <* nummer *> Saldo per <* datum*>* om din bank använder en utländsk valuta. Värdet i fältet Redovisningskontonr. <* nummer *> Saldo per <* datum*> för lokal valuta kan skilja sig något eftersom valuta konverteringen kan ge små skillnader. Bankens saldo bör vara mycket nära detta saldo.  |
|Bankkontos saldo per <*datum*>| Saldot på bankkontot på slutdatum för kontoutdraget.|
|Summa differenser    | Summan av skillnaderna för kontoutdragsraderna. Om du vill komma åt informationen aktiverar du **Skriv ut utestående transaktioner** när du anger kriterier för rapporten. En differens är en bankkontoutdragsrad som inte matchas helt till en eller flera bankkontotransaktioner. Du kan inte bokföra en bankkontoavstämning som har differenser. Du kan bokföra en bankkontoavstämning som innehåller banktransaktioner som inte stämmer överens med kontoutdragsrader. Det här värdet visas i **Utestående banktransaktioner** och i ett separat avsnitt om du aktiverar växla Skriv ut utestående transaktioner.      |
|Saldo vid kontoavstämning     | Värdet anges i fältet **Kontoutdragets slutsaldo** på sidan **Bankkontoavstämning**.  |
|Utestående banktransaktioner     | Summan av icke-matchade, bankposter utan check som har ett bokföringsdatum på eller före utdragets slutdatum. Detta inträffar när du registrerar transaktioner innan de registreras i din bank. Till exempel i slutet av en period. När du skapar nästa bankkontoavstämning kan du stämma av dessa transaktioner.        |
|Utestående checkar     | Summan av icke-matchade bankposter för checkar som har ett bokföringsdatum på eller före utdragets slutdatum. Detta inträffar när du registrerar transaktioner innan de registreras i din bank. Detta kan t. ex. inträffa för checkar om en leverantör inte löser in en check samma period som du har registrerat den. När du skapar nästa bankkontoavstämning kan du stämma av dessa transaktioner.        |
|Bankkontos saldo     | Summan av värdena på slutsaldot i bankkontoutdraget, utestående banktransaktioner och utestående checkar. När du har hanterat alla skillnader i de matchade posterna matchar saldot ditt banksaldo. Du har till exempel konto för alla matchade transaktioner samt de transaktioner som inte matchar detta bankkontoutdrag. Du kan lägga upp avstämningen.        |

> [!TIP]
> Om du kör **Testrapport** från sidan **betalningsavstämningsjournal**, [!INCLUDE [prod_short](includes/prod_short.md)] beräknar värdet i **Kontoutdragets slutsaldo** så här:
>
> * saldo senaste kontoavstämning + summan av alla rader i betalningsavstämningsjournalen
>
> Du kan använda värdet för att jämföra med kontoutdraget.

## Så här skapar du saknade transaktioner att matcha med banktransaktioner

Ibland kan det hända att ett kontoutdrag från banken innehåller belopp som motsvarar en avgift eller räntekostnad. Sådana banktransaktionsrader kan inte matchas eftersom inga relaterade transaktioner finns i [!INCLUDE[prod_short](includes/prod_short.md)]. Du måste sedan bokföra en journalrad för varje transaktion för att skapa en artikelrelaterad transaktion som den kan matchas med.

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Överföring till redovisningsjournal**.  
2. På sidan **Bankavst. trans. åt redov.jnl** anger du vilka redovisningsjournalen om du vill använda och klickar på knappen **OK**.

    Sidan **Redovisningsjournal** öppnas med nya journalrader för alla bankrapportrader med saknade transaktioner.
3. Fyll i journalraden med information, till exempel motkonton. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).  
4. Om du vill granska resultatet av en bokföring innan du bokför, väljer du åtgärden **testrapport** och väljer sedan ett alternativ för åtkomst till rapporten. Rapporten **bankkontoutdrag** visar samma fält som rubrik på sidan **Bankkontoavstämning**.
5. Välj åtgärden **Bokföra**.

    När transaktionen har bokförts matchar du bankkontoutdraget till den.
6. Uppdatera eller öppna sidan **Bankkontoavstämning** igen. Den nya transaktionen ska visas i fönstret **Bankkontotransaktioner**.
7. Matcha kontoutdragraden till bankkontotransaktionen, antingen manuellt eller automatiskt.

## Hitta utestående transaktioner i föregående perioder

Du kan använda kontoutdragsrapporten för att söka efter utestående transaktioner i föregående perioder. Utestående transaktioner har öppnats före kontoutdragets datum och har inte stängts eller stängts efter att bankavstämningen bokfördes.

När du kör kontoutdragsrapporten från sidan Kontoutdragslista kan du aktivera **Utestående transaktioner** så innehåller rapporten ett avsnitt med utestående transaktioner.

**Exempel** Vi har bankkontotransaktionerna A, B och C i vårt bankkonto för augusti månad. När vi stämmer av vårt bankkonto för augusti hittar vi en bankutdragsrad som matchar post A, men ingen för B och C. Så vi bokför avstämningen med transaktion A avstämd och B och C som utestående transaktioner.

I september erhåller vi en betalning för transaktion B och bestämmer oss för att stämma av vårt bankkonto. Om vi kör kontoutdragsrapporten innan vi bokför avstämningen har vi en avstämd transaktion och en utestående.

Om vi skriver ut rapporten för augusti har vi utestående transaktioner för våra B- och C-transaktioner även om vi avslutade transaktioner B i september.

## Ångra en bankkontoavstämning

Om du upptäcker ett misstag i en bokförd bankavstämning kan du använda åtgärden **Ångra** på sidan **Bankkontoutdragslista** för att korrigera det. När du ångrar en bokförd bankavstämning flyttas transaktionerna till sidan **Bankavstämning** och markeras som **Öppna**, vilket innebär att de inte stämts av. Du kan sedan rätta bankavstämningen och bokföra den igen.

> [!NOTE]
> I den Nordamerikanska versionen måste du aktivera brytaren **Bankavstämn. med auto-matchning** på sidan **Redovisningsinställning** om du vill använda funktionen Ångra för bokförda bankavstämningar och kontoutdrag. Funktionen Ångra är inte tillgänglig för kontoutdrag som har bokförts från kalkylblad för bankavstämning.

### Återanvända kontoutdragsnumret

Det kontoutdragsnummer som används för den nya bankavstämningen tas från bankkontot, precis som saldot för senaste kontoavstämning. Du kan ändra dessa värden innan du börjar en ny bankavstämning. När du skapar en ny bankavstämning kontrollerar emellertid [!INCLUDE[d365fin](includes/d365fin_md.md)] om utdragsnumret redan har tilldelats ett bokfört kontoutdrag. Om numret redan används men du vill att det nya kontoutdraget ska använda det istället, kan du använda åtgärden **Ändra dokumentnr.** åtgärden på sidan **Bankkontoavstämn.**.

### Exempel

Nedan följer några exempel på hur du kan korrigera ett misstag i en bokförd bankavstämning med eller utan att använda samma utdragsnummer.

#### Exempel 1

Du utförde bankavstämningar för januari, februari och mars. Kontoutdragsnumret var 100 för mars. Senare upptäcker du att mars bara inkluderade transaktioner fram till och med den 30, vilket innebär att transaktionerna för den 31 saknas. Därför måste du göra om bankavstämningen för mars. I det här fallet öppnar vi fönstret **Kontoutdrag**, väljer utdraget för mars och väljer sedan **Ångra**. 

Den nya bankavstämningen erhåller utdragsnummer 101. Om du vill tilldela om numret 100 väljer du **Ändra utdragsnr.** och ange **100**. 

> [!TIP]
> Glöm inte att ange lämpligt slutdatum för utdrag (i detta exempel: den 31 mars) och redigera fältet **Saldo för senaste kontoavstämning**. 

#### Exempel 2

Du utförde bankavstämningar för januari, februari, juni och juli. Du upptäcker att februari var felaktigt. Vi antar att det hade utdragsnummer 100. På samma sätt som i Exempel 1 använder du fältet Ångra och Ändra utdragsnr. åtgärder för att ändra utdragsnumret på samma sätt som i Exempel #1 ovan, och du kan nu göra om bankavstämningen för februari.  

Efter att du har bokfört den korrigerade bankavstämningen för februari kommer, på motsvarande bankkontokort, fältet **Senaste utdragsnr.** att ange **100**, och fältet **Saldo för senaste kontoavstämning** att ange slutsaldot för februariutlåtandet. 

Om nästa bankavstämning du gör är för mars kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] att tilldela 101 som utdragsnummer och ge den rätt **Saldo för senaste kontoavstämning**.

Om nästa bankavstämning du gör är för augusti bör du överväga att ändra värdena i fälten **Senaste utdragsnr.** och **Saldo för senaste utdrag** på kortet **Bankkonto** innan du upprättar nästa bankavstämning, eller använd åtgärden **Ändra utdragsnr** och ändra även värdet i fältet **Saldo för senaste utdrag** på sidan för bankavstämning.

> [!NOTE]
> Utdrags numret är viktigt när du gör bankavstämningar med importerade CAMT-filer som innehåller utdragsnummer eller när du stämmer av baserat på utskrivna kontoutdrag. Om du bara hämtar en serie banktransaktioner från internetbanken är utdragsnumret vanligen oviktigt.  
>
> Saldot för senaste kontoavstämning lagras på bankkontot för att minimera misstag vid bankavstämningar, men det kan också redigeras, så att du kan utföra dina bankavstämningar i valfri ordning. Detta innebär också att om du ångrar ett kontoutdrag kanske det nya slutsaldot inte är saldot för den senaste kontoavstämningen på nästa kontoutdrag. Det finns ingen funktion som gör att du kan flytta ett saldo framåt till alla efterföljande kontoutdrag, så tänk på detta när du använder Ångra.  

## Undvik direktbokföring

Använd inte ett redovisningskonto som tillåter direkt bokföring i bankkontots bokföringsmall. Direkt bokföring innebär att kopplingen mellan bankkontotransaktionen och redovisningskontotransaktionen bryts. När du stämmer av ditt bankkonto kommer transaktioner som bokförts direkt till redovisningskontot inte att tas med och det är svårt att slutföra avstämningen.

Detta misstag inträffar ofta när du anger ett ingående saldo för ett bankkonto. Det är viktigt att du inte bokför det ingående saldot direkt i redovisningen. Transaktioner på redovisningskontot som bokförs direkt till redovisningskontot orsakar problem. Dessa transaktioner kan t.ex. hindra dig från att stämma av ditt bankkonto. För bankkonton med utländsk valuta kan transaktionerna medföra att avvikelser ackumuleras när du har bokfört fler bankavstämningar på grund av valutakursjusteringar. Ofta bokförs det ingående banksaldot direkt på bank-kontot och beloppet fylls sedan i på redovisningskontot. Du kan också ångra det senare mot det redovisningskonto som du använder för att balansera det öppna redovisningssaldot. I båda fallen måste du balansera eventuell direkt bokföring till redovisningskontot innan du börjar med den första bankkontoavstämningen, framför allt om bankkontot är i en utländsk valuta.

## Se även

[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Definiera regler för automatisk koppling av betalningar](receivables-how-set-up-payment-application-rules.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
