---
title: Skapa bankinsättningar
description: Du kan göra insättningar för att underhålla en transaktionspost som innehåller information som kan kopplas till utestående fakturor och kreditnotor.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'bank, deposit'
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 09/04/2023
ms.custom: bap-template
---
# <a name="create-bank-deposits"></a>Skapa bankinsättningar

> [!NOTE]
> Möjligheten att skapa banktillgodohavanden är ny i Business Central 2022 utgivningscykel 1 för ett flertal land-/regionsversioner. Om du använde Business Central i USA, Kanada eller Mexiko före den versionen kanske du använder tidigare funktioner. Du kan fortsätta, men de nya funktionerna ersätter de gamla i framtida versioner. Om du vill börja använda de nya funktionerna som beskrivs i den här artikeln kan du be din administratör gå till sidan **Funktionshantering** och aktivera **Funktionsuppdatering: Standardiserad bankavstämning och insättningar**.  

Använd sidan **Bankinsättningar** för att registrera tillgodohavanden som ett enda dokument som bokför en eller flera transaktioner på ett bankkonto. Bankinsättningar används vanligtvis för att registrera kontanta insättningar. Sidan Bankinsättningar är tillgänglig i menyn **Kontanthantering** Rollcenter för Business Manager och andra Rollcenter som arbetar med kontanthantering.

Beloppen för bankinsättningar kan komma från flera olika källor:

* Försäljning, med hjälp av ett redovisningskonto för intäkter.
* Kundbetalningar.
* Kontantåterbetalningar från leverantörer, eller kontantbetalningar till dessa. 

Bankinsättningsraderna innehåller information om enskilda insättningar, till exempel checkar från kunder. Summan av beloppen på raderna måste uppgå till det totala beloppet för insättningen.

När du har fyllt i informationen och raderna för insättning måste du bokföra den. Vid bokföring uppdateras de aktuella redovisningarna. Dessa redovisningar inkluderar redovisning samt bank-, kund-och leverantörsreskontran. Bokförda tillgodohavanden lagras för framtida referens på sidan **Bokförda bankinsättningar**.

I rapporten **bankinsättning** visas kund- och leverantörsinsättningar med det ursprungliga insättningsbeloppet, det insättningsbelopp som är fortsatt öppet samt det belopp som används. Rapporten visar även det totala bokförda insättningsbelopp som ska stämmas av.

## <a name="before-you-start"></a>Innan du börjar

Det finns några saker du bör ställa in innan du kan använda bankinsättningar. Du måste ha en nummerserie och en journalmall för redovisning klar. Du bör också ange om du vill bokföra bankinsättningsbelopp som en klumpsumma. Det vill säga totalsumman av alla belopp på insättningsraderna. I annat fall bokförs varje rad som en enskild transaktion. När du bokför en insättning som en enskild banktransaktion kan det vara enklare att utföra bankavstämning.

### <a name="number-series-and-lump-sum-deposits"></a>Insättningar av nummerserie och klumpsumma

Du måste lägga upp en nummerserie för bankinsättningar och sedan ange serien i fältet **Bankinsättningsnr.** på sidan **Inställningar för försäljning och kundfordringar**. Mer information om nummerserier finns i [Skapa nummerserier](ui-create-number-series.md).

På sidan **Inställningar för försäljning och kundreskontra**, om du vill bokföra insättningar som klumpsummor istället för på enskilda rader, aktiverar du reglaget **Bokför bankinsättningar som klumpsummor**. När du bokför en insättning som en klumpsumma skapas en banktransaktion för hela insättningsbeloppet, vilket gör det enklare att utföra bankavstämning.

### <a name="general-journal-templates-for-bank-deposits"></a>Journalmallar för bankinsättningar

Du måste också skapa en redovisningsjournalmall för insättningar. Du använder redovisningsjournaler för att bokföra transaktioner till konton för bank, kund, leverantör, anläggningstillgång samt redovisning. Journalmallarna utformar redovisningsjournalen i syfte att matcha syftet med arbetet. Det innebär att fälten i journalmallen är exakt de som du behöver.

Insättningarna kommer att vara inbetalningar, så du kanske vill återanvända nummerserien för inbetalningsjournaler. Om du behöver skilja mellan bankinsättnings- och inbetalningsjournalposter använder du olika nummerserier.

Du måste också skapa ett batchjobb för mallen. Om du vill skapa ett batchjobb väljer du sidan **Redovisningsmallar** och sedan **Batchar**. Mer information om journaler finns i [Använda journalmallar och journaler](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a>Dimensioner på bankinsättningsrader

Raderna för bankinsättningen kommer automatiskt att använda de standarddimensioner som du har angett i fälten **Avdelningskod** och **Kundgruppskod**. När du väljer **Kund** eller **Leverantör** i fältet **Kontotyp** kommer de dimensioner som angetts för kunden eller leverantören att ersätta standardvärdena. Du ändra radernas dimensioner vid behov.

> [!TIP]
> Dimension på rader anges enligt standarddimensionsprioritet. Raddimensionerna gäller framför sidhuvuddimensionerna. För att undvika konflikter kan du skapa regler som prioriterar när en dimension ska användas beroende på källa. Om du vill ändra hur dimensionerna prioriteras kan du ändra deras rangordning på sidan **Standardprioritering för dimensioner**. Mer information finns i [Konfigurera prioriteringar för standarddimensioner](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit"></a>Skapa ny bankinsättning

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankinsättningar** och väljer sedan relaterad länk.
2. Välj **Nytt** för att öppna sidan **Bankinsättning**.
3. Välj den redovisningsjournalmall som du har skapat för bankinsättningar.  

    > [!NOTE]
    > Om redovisningsjournalmallen har mer än en batch kommer du att uppmanas att välja en.

4. I fältet **Bankkontonr** väljer du det bankkonto du vill göra insättningen på.

    > [!TIP]
    > Du kan kontrollera att du sätter in på rätt konto med hjälp av åtgärderna **Kontokort** och **Kontotransaktioner** för att slå upp transaktionerna för det valda bankkontot. Till exempel för att se om liknande insättningar har gjorts på kontot.

5. I fältet **Totalt insättningsbelopp** anger du insättningens totala belopp. Denna summa måste vara summan av beloppen på alla rader.
6. Fyll i återstående fält om det behövs. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Datumet i fältet **Bokföringsdatum** och dimensionerna i fälten **Avdelningskod** och **Kundgruppskod** tilldelas till de rader som du skapar för bankinsättningen. Du kan ändra dessa vid behov.

7. Beroende på om du vill bokföra bankinsättningen som klumpsumma eller varje rad för sig i bankens redovisning, ska du aktivera/inaktivera reglaget för **Bokför som klumpsumma**. Standardinställningen kommer från samma reglage på sidan **Försäljningsinställningar**.

    > [!NOTE]
    > Fältet **Valutakod** anger den valuta som angetts för det bankkonto som du valt. Du kan inte välja en annan valuta.

8. På snabbfliken **Rader** skapar du en ny rad för respektive kontant betalning som du vill sätta in.
9. I fältet **Kontotyp** anger du var betalningen kommer från. För bankinsättningar är typen vanligen **Kund** eller **Leverantör**.

    > [!NOTE]
    > Du kan också registrera en kontant betalning för en leverantör. Detta gör du genom att välja **Leverantör** och sedan ange betalningsbeloppet som ett negativt tal i fältet **Kreditbelopp** på raden.

10. I fältet **Dokumentnr.** anger du dokumentnumret för den faktura från vilket kreditbeloppet kommer. Du kan använda ett verifikations nummer för varje rad, eller samma nummer för alla rader.

    > [!TIP]
    > Normalt sett behöver du inte fylla i fältet **Dokumenttyp** för de ekonomiska transaktionerna. Om du till exempel vill sätta in kontanter från en dags försäljning lämnar du fältet tomt. Om du vill sätta in kontanter från en kundbetalning väljer du **Betalning**.

11. Om du sätter in en kontant betalning för en viss kundfaktura väljer du åtgärden **Applicera transaktioner** och anger sedan fakturanumret i fältet **Koppla till ID**.
12. Om du är redo att bokföra bankinsättningen väljer du åtgärden **Bokför**.

    > [!TIP]
    > Innan du bokför insättningen kan du använda åtgärden **Testrapport** för att granska dina data. I rapporten visas om det finns några problem, till exempel saknade data, som gör att det inte går att bokföra.  

## <a name="find-posted-bank-deposits"></a>Hitta bokförda bankinsättningar

Sidan **Bokförda bankinsättningar** listar ditt företags tidigare insättningar. I listan kan du granska de kommentarer och dimensioner som har angetts för insättningarna. Du kan öppna bankinsättningen om du vill visa fler detaljer, och därifrån kan du sedan undersöka ytterligare uppgifter. Du kan till exempel välja åtgärden **Sök poster** om du vill visa de bokförda bankkontotransaktionerna. Från bankkontotransaktionen kan du hitta dess tillhörande bokförda redovisningstransaktion.

Om du vill slå upp alla redovisningstransaktioner för de bokförda insättningsraderna går du till sidan **Bokförd redovisningsjournal** och använder åtgärden **Redovisning**. Där hittar du alla redovisningstransaktioner, inklusive transaktioner för kunder och leverantörer.

## <a name="reverse-a-posted-bank-deposit"></a>Återföra en bokförd bankinsättning

Det finns ett par sätt att återföra en bokförd bankinsättning:

* På sidan **Bokförda bankinsättningar** väljer du insättningen och väljer åtgärden **Ångra bokföring**.
* På sidan **Bokförda redovisningsjournaler**, letar upp registret för insättningen och väljer sedan åtgärden **Återföra register**.

> [!NOTE]
> Du kan bara återföra ett register som innehåller en enda typ av transaktion. Det vill säga, journalen får bara innehålla kundtransaktioner eller leverantörstransaktioner, men inte båda två. Om ett register innehåller båda två måste du återföra insättningen manuellt.

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Konfigurera Finance](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]



