---
title: Stäm av kvitton för leverantörsbetalningar eller återbetalningar i utbetalningsjournalen
description: 'Om du vill bearbeta, matcha eller stämma av leverantörsbetalningar eller återbetalningar manuellt, kopplar du beloppet till en eller flera öppna leverantörsreskontratransaktioner.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment application, payment processing, match payments'
ms.search.form: '62, 233, 522, 623'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Stäm av leverantörsbetalningar med betalningsjournalen eller från bokförda leverantörsreskontratransaktioner
När du skickar ett betalningskvitto till, eller tar emot en återbetalning från, en leverantör måste du bestämma om du ska koppla betalningen eller återbetalningen till en eller flera öppna debet- eller kreditposter. Du kan ange det exakta beloppet som ska kopplas till betalningsinleveransen eller återbetalningen och därmed endast delvis koppla leverantörsreskontratransaktioner. Du måste koppla alla leverantörsreskontratransaktioner för att leverantörsstatistik och rapporter över kontoutdrag och ränteintäkter ska bli korrekta.

> [!NOTE]  
>   Leverantörer föredrar ibland återbetalning framför en kreditnota som ska användas mot framtida fakturor, särskilt om du returnerar artiklar som du redan har betalt eller om du har betalat för mycket för en faktura.

Du kan koppla leverantörsreskontratransaktioner på tre olika sätt:

* Genom att ange information på den dedikerade sidan som till exempel fönstret **Utbetalningsjournal** och sidan **Betalningsavstämningsjournal**.
* Från inköpskreditnotor.
* Från leverantörsreskontratransaktioner efter att inköpsdokument har bokförts men inte har kopplats.

> [!NOTE]  
>   Om fältet **Avräkningsmetod** på leverantörskortet innehåller **Koppla till äldsta faktura**, kommer betalningen att kopplas automatiskt till den äldsta öppna kredittransaktionen om du inte manuellt anger vilken transaktion som ska kopplas till. Om avräkningsmetoden för en kund är **Manuell** måste du koppla transaktioner manuellt.

Du kan koppla leverantörsbetalningar manuellt till dess relaterade inköpsdokument, när du bokför utbetalningarna på sidan **Utbetalningsjournal**. Mer information om att fylla i utbetalningsjournalen finns i [Göra delbetalningar](payables-make-payments.md).

Du kan också koppla leverantörsbetalningar och kundutbetalningar när utbetalningarna visas som negativa banktransaktioner på banken. På sidan **Betalningsavstämningsjournal** kan du använda funktioner för import av kontoutdrag, automatisk koppling och bankkontoavstämning. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Så här kopplar du en betalning till en enskild eller flera leverantörsreskontratransaktioner
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningsjournal** och väljer sedan relaterad länk.
2. Ange information om betalningstransaktionen på den första journalraden på sidan **Utbetalningsjournal**.
3. Så här kopplar du en enskild leverantörsreskontratransaktion:
   1. I fältet **Kopplas till ver.nr** väljer du fältet för att öppna sidan **Koppla leverantörstrans.**.
   2. På sidan **Koppla leverantörstrans.** markerar du transaktionen som du vill koppla betalningen till.
   3. På raden i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten.
4. Eller så här kopplar du flera leverantörsreskontratransaktioner:

   1. Välj åtgärden **Koppla transaktioner**.
   2. På sidan **Koppla leverantörstrans.** markerar du raden med transaktioner som du vill koppla betalningen till.
   3. Välj åtgärden **Koppla till ID**.  
   4. På varje rad i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten.

      Om du inte anger något belopp kopplas automatiskt det maximala beloppet. Längst ned på sidan **Koppla leverantörstransaktioner** kan du se beloppet i fältet Kopplat belopp och om kopplingen balanserar.
5. Välj **OK**.
6. Om du vill bokföra utbetalningsjournalen väljer du åtgärden **Bokför**.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Så här kopplar du en kreditnota till en enskild eller flera leverantörsreskontratransaktioner:
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpskreditnota** och väljer sedan relaterad länk.
2. Öppna den kreditnota som du vill koppla.
3. Fyll i relevant information i huvudet.
4. För att koppla en enstaka leverantörsreskontratransaktion väljer du på snabbfliken **Koppling** i fältet **Kopplas till ver.nr** den transaktion som krediten kopplas till och sedan i fältet **Belopp att koppla** anger du beloppet som ska kopplas till transaktionen.
5. Eller så här kopplar du flera leverantörsreskontratransaktioner:

   1. Välj åtgärden **Koppla transaktioner**.
   2. Markera raderna med transaktioner som du vill koppla kreditnotan till.
   3. Välj åtgärden **Koppla till ID**.  
   4. På varje rad i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten.

       Om du inte anger något belopp kopplas automatiskt det maximala beloppet. Längst ned på sidan **Koppla leverantörstransaktioner** kan du se beloppet i fältet **Kopplat belopp** och se om kopplingen balanserar.
6. Välj knappen **OK**.  
   På sidan **Inköpskreditnota** visas nu transaktionen som du har valt i fältet **Kopplas till dokumenttyp** och fältet **Kopplas till ver.nr.** Sidan innehåller nu också beloppet på den kreditnota som ska bokföras justerat med eventuell kassarabatt.
7. Klicka på knappen **Bokför** för att bokföra inköpskreditnotan.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Så här kopplar du bokförda leverantörsreskontratransaktioner:
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna relevant leverantör med poster som redan bokförts.
3. Välj åtgärden **Transaktioner** och välj sedan åtgärden **Koppla transaktioner**.
4. På sidan **Koppla leverantörstrans.** visas leverantörens öppna transaktioner.
5. Markera raden med den transaktion som ska kopplas.
6. Välj åtgärden **Koppla till ID**.

    I fältet **Koppla till ID** visas tre asterisker om du arbetar i ett enanvändarsystem, eller ditt användar-id om du arbetar i ett fleranvändarsystem.  
7. På varje rad i fältet **Belopp att koppla** anger du det belopp som du vill koppla till posten.

    Om du inte anger något belopp kopplas automatiskt det maximala beloppet. Längs ned på sidan **Koppla leverantörstrans.** kan du se beloppet i fältet **Kopplat belopp**.
8. Välj åtgärden **Bokför kopplade trans.**.  

    Sidan **Bokför kopplade trans.** öppnas med dokumentnumret för den kopplade transaktionen och bokföringsdatumet för den post som har det senaste bokföringsdatumet.
9. Klicka på **OK** för att bokföra kopplingen.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Så här kopplar du leverantörsreskontratransaktioner i olika valutor till varandra:
Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du ändå koppla fakturan till betalningen.

Om du kopplar en post (post 1) i en valuta till en post (post 2) i en annan valuta används bokföringsdatumet för post 1 för att söka efter rätt valutakurs att omvandla belopp efter i post 2. Rätt valutakurs hittas på sidan **Valutakurser**. I detta fall måste du aktivera koppling av leverantörsreskontratransaktioner i olika valutor. Mer information finns i [Aktivera koppling av kundreskontratransaktioner till olika valutor](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Betalningsjournal** och väljer sedan relaterad länk.
2. Öppna den journal som du vill ha och fyll i första tomma journalrad med en valutakod.
3. Välj åtgärden **Koppla transaktioner**.
4. Välj raden med den post som du vill koppla till posten i utbetalningsjournalen. Klicka sedan på åtgärden **Koppla till ID** och välj den post som du vill koppla till.
5. Välj knappen **OK** om du vill återvända till utbetalningsjournalen.
6. Bokför utbetalningsjournalen.

> [!IMPORTANT]  
>   När du kopplar poster i olika valutor till varandra omvandlas posterna till USD. Även om valutakurserna är fasta för de två aktuella valutorna, t. ex. mellan USD och EUR, kan det uppstå ett litet restbelopp när beloppen i utländsk valuta omvandlas till USD. Dessa små restbelopp bokförs som vinster och förluster på kontot som har angetts i fältet **Kursvinster konstaterade** eller i fältet **Kursförluster konstaterade** på sidan **Valutor**. Fältet **Belopp (USD)** justeras också i de aktuella leverantörsreskontratransaktionerna.

## <a name="to-unapply-an-application-of-vendor-entries"></a>Så här tar du bort en koppling av leverantörstransaktioner
När du tar bort en felaktig koppling skapas och bokförs korrigeringstransaktioner som är identiska med den ursprungliga transaktionen, men med motsatt tecken i beloppsfältet för alla transaktioner, inklusive all redovisningsbokföring som gjorts i redovisningen till följd av kopplingen, t. ex. kassarabatter och valutakursvinster/-förluster. Alla transaktioner som stängdes av kopplingen öppnas på nytt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna relevant leverantörskort.
3. Välj åtgärden **Transaktioner**.
4. Välj aktuell transaktion och klicka på åtgärden **Ta bort koppling på trans.**.
5. Välj alternativt åtgärden **Detaljerad transaktion**.
6. Välj aktuell koppling och klicka på åtgärden **Ta bort koppling på trans.**.
7. Fyll i fälten i huvudet och välj sedan åtgärden **Ta bort koppling**.

> [!IMPORTANT]  
>   Om en transaktion har använts i flera kopplingar måste du ta bort den senaste kopplingen först.

## <a name="see-also"></a>Se även
[Leverantörsreskontra](payables-manage-payables.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
