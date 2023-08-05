---
title: Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner
description: Beskriver hur du använder inbetalningar eller återbetalningar för kunder till en eller flera öppna kundreskontratransaktioner. Det är en del av att stämma av kundbetalningar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 04/01/2021
ms.author: edupont
---
# Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner

När du får en kontant betalning från en kund eller ger en kontant återbetalning kan du använda betalningen eller återbetalningen för att stänga öppna debet eller kredit. Du kan ange det belopp som du vill koppla. Du kan till exempel använda delbetalningar till kundreskontratransaktioner. Att avsluta kundreskontratransaktioner håller kundstatistik, kontoutdrag, ekonomiavgifter och så vidare uppdaterad.

> [!TIP]  
>   På sidan **kundreskontratransaktioner** betyder rött teckensnittet att den relaterade betalningen kommer efter dess förfallodatum. Om en förfallen betalning blir ett problem, hjälper vi dig att minska frekvensen. Du kan aktivera tillägget **prediktioner för sena betalningar** som använder en prediktiv modell som vi har byggt in i Azure Machine Learning för att förutse tidpunkt för betalningar. Dessa prediktioner hjälper dig att minska utestående kundfordringar och finjustera en strategi för samlingar. Om till exempel om en betalning förutsägs att bli försenad kanske du bestämmer dig för att ändra villkoren för kundens betalningsmetod. För mer information, se [prediktioner för sena betalningar](ui-extensions-late-payment-prediction.md).  

Du kan koppla kundreskontratransaktioner på olika sätt:

* Genom att ange information om särskilda sidor:
    * Sidan **utbetalningsavstämningsjournal**. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * Sidan **betalningsregistrering**. Mer information finns i [Så här stämmer du av kundutbetalningar manuellt från en lista med obetalda försäljningsdokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)
    * **Inbetalningsjournalen**. Detta alternativ beskrivs nedan.
* Genom att markera fältet **gäller dok.nr.** på försäljningskreditnotor. Detta alternativ beskrivs nedan.
* Med hjälp av åtgärden **Ange Koppla till ID** för en kundreskontratransaktion. Detta alternativ beskrivs nedan.
* Genom att använda åtgärden **Koppla transaktioner** på sidan **bankinsättning** och sedan ange faktura numret i fältet **Koppla till ID**. Mer information finns i [Skapa bankinsättningar](bank-create-bank-deposits.md)

> [!NOTE]  
>   Om fältet **Avräkningsmetod** på kundkortet innehåller **Koppla till äldsta faktur**, kommer betalningen att kopplas till den äldsta öppna kredittransaktionen om du inte manuellt anger en transaktion. Om avräkningsmetoden för en leverantör är **Manuell** måste du alltid koppla transaktioner manuellt.

## Så här fyller du i och bokför en inbetalningsjournal:
En inbetalningsjournal är en typ av redovisningsjournal. Du kan använda den för att bokföra transaktioner på redovisningskonton, bankkonton, kundkonton, leverantörskonton och konton för anläggningstillgångar. Du kan applicera betalningen på en eller flera debetposter när du bokför betalningen. Du kan även koppla från de bokförda transaktionerna senare.
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inbetalningsjournal** och väljer sedan relaterad länk.
2. Välj åtgärden **Redigera journal**.
3. Välj önskat namn i fältet **Journalnamn**.
4. Fyll i fältet **Bokföringsdatum**.  
5. I fältet **Dokumenttyp** väljer du **Betalning**.

    Fältet **Dokumentnr** fylls i av den nummerserie som har tilldelats journalen.  
6. Använd fältet **Externt verifikationsnr** om du lagrat ett ID t.ex kundens checknummer.
7. I fältet **Kontotyp** väljer du **Kund**.
8. I fältet **bankkontonr.** väljer du relevant redovisningskonto.
9. Gör något av följande om du vill bokföra kopplingen samtidigt som du bokför journalen.
10. I fältet **Motkontotyp** väljer du **Redovisningskonto** för kontantbetalningar eller **Bankkonto** för andra typer av betalningar.
11. Välj kontantkontot för kontantbetalningar eller rätt bankkonto för andra typer av betalningar i fältet **Motkonto**.
12. Bokför journalen.

## Så här kopplar du en betalning till en enskild kundreskontratransaktion
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inbetalningsjournal** och väljer sedan relaterad länk.
2. Välj åtgärden **Redigera journal**.
3. Ange information om den transaktion som ska kopplas på den första journalraden.
4. I fältet **Dokumenttyp** anger du **Betalning**.
5. I fältet **Kontotyp** anger du **Kund**.
6. I fältet **Motkontotyp** anger du **Bankkonto.**
7. I fältet **Kopplas till ver.nr** väljer du fältet för att öppna sidan **Koppla kundtrans.**.
8. På sidan **Koppla kundtrans.** markerar du transaktionen som du vill koppla betalningen till.
9. I fältet **Belopp att koppla** anger du det belopp som du vill koppla till transaktionen. Om du inte anger något belopp kopplas det maximala beloppet.

    Längst ned på sidan **Koppla kundtransaktioner** kan du se beloppet i fältet **Kopplat belopp** och om kopplingen balanserar.  
10. Välj **OK**. På sidan **Inbetalningsjournal** visas nu transaktionen i fälten **Kopplas till dokumenttyp** och **Kopplas till ver.nr.**
11. Bokför inbetalningsjournalen.

## Så här kopplar du en betalning till flera kundreskontratransaktioner
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inbetalningsjournal** och väljer sedan relaterad länk.
2. Välj åtgärden **Redigera journal**.
3. Ange information om den transaktion som ska kopplas på den första journalraden.
4. I fältet **Dokumenttyp** anger du **Betalning**.
5. I fältet **Kontotyp** anger du **Kund**.
6. I fältet **Motkontotyp** anger du **Bankkonto.**
7. I fältet **Belopp** anger du den fullständiga betalningen som ett negativt belopp.
8. Om du vill koppla betalningen till flera kundreskontratransaktioner vid bokföringen väljer du åtgärden **Koppla transaktioner**.  
9. Markera raderna med de poster som du vill koppla transaktionen till och väljer sedan åtgärden **Koppla till ID**.  
10. På varje rad i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten. Om du inte anger något belopp kopplas det maximala beloppet.

    Längst ned på sidan **Koppla kundtransaktioner** kan du se beloppet i fältet **Kopplat belopp** och om kopplingen balanserar.  
11. Välj **OK**.
12. Bokför inbetalningsjournalen.

## Så här kopplar du en kreditnota till en enskild kundreskontratransaktion
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningskreditnotor** och väljer sedan relaterad länk.
2. Öppna relevant försäljningskreditnota.
3. Om du vill koppla kreditnotan till en enskild kundreskontratransaktion vid bokföring klickar du på snabbfliken **Kopplas till ver.nr** och väljer den transaktion som du vill koppla betalningen till.
4. På raden i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten.  

    Om du inte anger något belopp kopplas automatiskt det maximala beloppet. Längst ned på sidan **Koppla kundtransaktioner** kan du se beloppet i fältet **Kopplat belopp** och om kopplingen balanserar.    
5. Välj knappen **OK**. På sidan **Försäljningskreditnota** visas nu transaktionen som du har valt i fälten **Kopplas till dokumenttyp** och **Kopplas till ver.nr.** Och beloppet på den kreditnota som ska bokföras justerat för eventuell kassarabatt.
6. Bokför kreditnotan.

## Så här kopplar du en kreditnota till flera kundreskontratransaktioner
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningskreditnotor** och väljer sedan relaterad länk.
2. Öppna relevant försäljningskreditnota.
3. Om du vill koppla kreditnotan till flera kundreskontratransaktioner vid bokföringen väljer du åtgärden **Koppla transaktioner**.
4. Markera raderna med de poster som du vill koppla transaktionen till och väljer sedan åtgärden **Koppla till ID**.
5. På varje rad i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten. Om du inte anger något belopp kopplas det maximala beloppet.  

    Längst ned på sidan **Koppla kundtransaktioner** kan du se beloppet i fältet **Kopplat belopp** och om kopplingen balanserar.  
6. Välj knappen **OK**. Sidan **Förs.kreditnota** innehåller nu beloppet på den kreditnota som ska bokföras justerat med eventuell kassarabatt.
7. Bokför kreditnotan.

## Så här kopplar du bokförda kundreskontratransaktioner
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna kundkortet för kunden med transaktionerna som du vill koppla.
3. Välj åtgärden **Transaktioner** och välj sedan raden med transaktionen som ska vara kopplingstransaktionen.
4. Välj åtgärden **Koppla transaktioner**. Sidan **Koppla kundtransaktioner** öppnas där du kan se de öppna transaktionerna för kunden.
5. Markera raderna med de poster som du vill koppla transaktionen till och väljer sedan åtgärden **Koppla till ID**. .
6. På varje rad i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten. Om du inte anger något belopp kopplas det maximala beloppet.  

    Längs ned på sidan **Kopplat belopp** kan du se det specifika beloppet i fältet **Koppla kundtransaktioner**.  
7. Välj åtgärden **Bokför kopplade trans.**. Sidan **Bokför kopplade trans.** visas med dokumentnumret för den kopplade transaktionen och bokföringsdatumet för den post som har det senaste bokföringsdatumet.  
8. Klicka på **OK** för att bokföra kopplingen.

    Om den bokförda kopplingen har medfört avslutade kundreskontratransaktioner finns det inte längre någon sådan markering i fältet **Öppen**.    
9. För att se transaktioner, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk. Bläddra till kortet för att den relevanta kunden ska se de redovisningstransaktioner.  

I transaktionslistan på raden som innehåller transaktionen som helt kopplades till kan du se att kryssrutan **Öppen** inte är markerad.  

> [!NOTE]  
>   När du har valt en post på sidan **Koppla kundtransaktioner** eller flera poster genom att anger **Koppla till ID** kommer fältet **Kopplat belopp** på journalraden att innehålla summan av de återstående beloppen för de bokförda poster som du har valt, om inte fältet redan innehåller något värde. Om du väljer **Koppla till äldsta trans.** i fältet **Avräkningsmetod** på kundkortet utförs kopplingen automatiskt.

## Så här kopplar du kundreskontratransaktioner i olika valutor till varandra
Om du säljer i en valuta och får betalt i en annan kan du ändå koppla fakturan till betalningen.  

Här är ett exempel. Du tillämpar post 1 i en valuta på post 2 i en annan valuta. Bokföringsdatumet för transaktion 1 används för att hitta den valutakurs som ska användas för att omvandla belopp i transaktion 2. Rätt valutakurs hittas på sidan **Valutakurser**.  

Koppla kundreskontratransaktioner i olika valutor till varandra måste vara aktiverad. Mer information finns i [Aktivera koppling av kundreskontratransaktioner till olika valutor](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inbetalningsjournal** och väljer sedan relaterad länk.
2. Öppna den journal som du vill ha och fyll i första tomma journalrad med en valutakod.
3. Välj åtgärden **Koppla transaktioner**.
4. Välj raden med den post som du vill koppla till posten i inbetalningsjournalen. Klicka sedan på åtgärden **Koppla till ID** och välj den post som du vill koppla till.
5. Välj knappen **OK** om du vill återvända till inbetalningsjournalen.
6. Bokför försäljningsjournalen.  

> [!IMPORTANT]  
>   När du kopplar poster i olika valutor till varandra omvandlas posterna till USD. Även om valutakurserna är fasta för de två aktuella valutorna, t. ex. mellan USD och EUR, kan det uppstå ett litet restbelopp när beloppen omvandlas till USD. Dessa små restbelopp bokförs som vinster och förluster på kontot som har angetts i fältet **Kursvinster konstaterade** eller i fältet **Kursförluster konstaterade** på sidan **Valutor**. Fältet **Belopp (USD)** justeras också i de aktuella leverantörsreskontratransaktionerna.  

## Så här rättar du en koppling av kundtransaktioner
När du korrigerar en ansökan skapas och bokförs korrigeringsposter för alla transaktioner. Korrigerings transaktionerna är desamma som originalen men har motsatt logg i fältet **belopp**. Korrigerings transaktionerna inkluderar alla redovisnings transaktioner som har härletts från kopplingen. Till exempel kassarabatt och valuta vinster/-förluster. Alla transaktioner som stängdes av kopplingen öppnas på nytt.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna relevant kundkort.
3. Välj åtgärden **Transaktioner**.
4. Välj aktuell transaktion och klicka på åtgärden **Ta bort koppling på trans.**.
5. Välj alternativt åtgärden **Detaljerad transaktion**.
6. Välj aktuell koppling och klicka på åtgärden **Ta bort koppling på trans.**.
7. Fyll i fälten i huvudet och välj sedan åtgärden **Ta bort koppling**.  

> [!IMPORTANT]  
>   Om en transaktion har använts i flera kopplingar måste du ta bort den senaste kopplingen först.  

## Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]