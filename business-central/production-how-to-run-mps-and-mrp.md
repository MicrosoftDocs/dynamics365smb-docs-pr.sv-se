---
title: 'Kör komplett planering, nettobehov eller produktionsplan'
description: 'I planeringssystemet beräknas antingen huvudproduktionsplan (MPS) eller nettobehovet (MRP), eller så beräknas båda på samma gång.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Kör komplett planering, nettobehov eller produktionsplan

Begreppen "beräkna planeringsförslag" eller "beräkna nettobehov" syftar på beräkning av produktionsprogram och materialbehov. Beräkningen baseras på faktisk och prognostiserad efterfrågan. I planeringssystemet beräknas antingen huvudproduktionsplan (MPS) eller nettobehovet (MRP), eller så beräknas båda på samma gång.  

- Nettobehov är beräkningen av en produktionsplan baserat på faktiskt behov och efterfrågeprognosen. Beräkningen av produktionsprogrammet används för slutartiklar som har en prognosrad eller en försäljningsorderrad. Dessa artiklar kallas för "nettobehovsartiklar" och identifieras dynamiskt när beräkningen startar.  
- Produktionsplan är beräkningen av materialbehov baserat på faktiskt behov av komponenter och efterfrågeprognosen på komponentnivå. Produktionsplanen beräknas endast för artiklar som inte är nettobehovsartiklar. Det övergripande syftet med produktionsplanen är att tillhandahålla tidsfasade formella planer, utifrån artikel, för att leverera rätt artikel i rätt tid, på rätt plats och i rätt antal.  

Planeringsalgoritmerna för MPS och MRP är desamma. Algoritmerna berör netting, återanvändning av befintliga återanskaffningsorder och åtgärdsmeddelanden. Planeringssystemprocessen används för att söka efter vad som behövs eller kommer att behövas (efterfrågan) och vad som finns i lager eller förväntas finnas i lager (tillgång). När man nettar dessa kvantiteter mot varandra [!INCLUDE[prod_short](includes/prod_short.md)] när dessa kvantiteter kvittas mot varandra. Åtgärdsmeddelanden innehåller förslag om att skapa en ny order, ändra en orderorder (antal eller datum) eller annullera en order. Begreppet "order" inbegriper inköpsorder, monteringsorder, produktionsorder och överföringsorder.

Du kan spåra länkarna som planeringen skapar mellan efterfrågan och utbud på sidan **Orderspårning**. Mer information finns i [Spåra relationer mellan tillgång och efterfrågan](production-how-track-demand-supply.md).

Inställningen av artikelkort, monteringsstrukturer, produktionsstrukturer och verksamhetsföljder påverkar i hög grad att planeringsresultaten blir rätt.  

## Metoder för att skapa en plan  

- **Beräkna fullständig plan**: Bearbeta eller återskapa materialplanen. Den här processen startar när du tar bort alla planerade leveransorder som för närvarande har laddats. Alla poster i databasen planeras på nytt.  
- **Beräkna nettoförändringsplan**: Behandla en nettoförändringsplan. Artiklar tas med i nettoförändringsplaneringen från två typer av förändringar:  
   - **Förändringar i tillgång/efterfrågan:** Dessa ändringar omfattar förändringar i kvantiteter i försäljningsorder, efterfrågeprognosen, monteringsorder, produktionsorder eller inköpsorder. En oplanerad förändring av lagernivån betraktas också som en kvantitetsförändring.  
   - **Förändringar av planeringsparameter:** Dessa ändringar omfattar förändringar i säkerhetslager, beställningspunkt, verksamhetsföljd, strukturlista och förändringar i beräkningen av tidsenhet eller ledtid.  
- **Hämta åtgärdsmeddelanden:** Fungerar som ett verktyg för planering på kort sikt för att varna användaren om ändringar som gjorts sedan du senast beräknade en regenerativ eller nettoförändringsplan.  

Med varje planeringsmetod genererar [!INCLUDE[prod_short](includes/prod_short.md)] kalkylarkstransaktioner med förmodad oändlig kapacitet. Produkktionsgruppers och maskingruppers kapacitet beaktas inte när du utvecklar scheman.  

> [!IMPORTANT]  
> Beräkna fullständig plan är den vanligaste processen. Skapa inköpsförslag och Verkställandet av åtgärdsmeddelanden kan användas för att köra beräkningen av nettoförändringsplanen.  
>
> Du kan köra körningarna Hämta åtgärdsmeddelandeplan mellan fullständig planering och nettoförändringsplanering för att få en omedelbar bild av effekten av schemaändringar. Det är dock inte tänkt att ersätta de fullständiga planeringsprocesserna för regenerativa eller nettoförändringar.  

## Så här beräknar du planeringsförslaget
  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **planeringsförslag** och väljer sedan relaterad länk.  
2. Välj åtgärden **Beräkna fullständig plan** för att öppna sidan **Skapa inköpsförslag**.  
3. Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Alternativ**.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Prod.program**|Beräkna ett huvudproduktionsschema. Artiklar med öppna försäljningsorder eller efterfrågeprognoser tas med i beräkningen. <br/>Om det också finns andra behov, till exempel säkerhetslager, återbeställningspunkt eller öppna produktionskomponentrader, för sådana artiklar inkluderas dessa krav i MPS-beräkningen för att säkerställa att planeringssystemet hanterar hela lagerprofilen.  |  
    |**Nettobehov**|Beräkna materialbehovsplaneringen. Artiklar med beroende behov tas med i den här beräkningen. Prod.program och Nettobehov körs normalt samtidigt. Om du vill köra produktionsplanen och nettobehovet samtidigt, på sidan **Produktionsinställningar** på snabbfliken **Planering**, välj **Kombinerad MPS/MRP-beräkning**.|  
    |**Fr.o.m.-datum**|Utvärdera lagerdispositionen. Om lagersaldot för en artikel är under beställningspunkten framåtplaneras en återanskaffningsorder automatiskt i systemet från det här datumet. Om saldot för en artikel är under värdet för säkerhetslager (per startdatumet) bakåtplaneras en återanskaffningsorder som förfaller på startdatumet för planeringen.|  
    |**T.o.m.-datum**|Slutdatumet för planeringshorisonten. Varken tillgång eller efterfrågan beaktas efter det här datumet. Om beställningscykeln för en artikel sträcker sig efter slutdatumet, är den giltiga planeringshorisonten för artikeln lika med order datum plus beställningscykel.<br/><br/> Planeringshorisonten är den tidsperiod som planen omfattar. Om horisonten är för kort, innebär det att artiklar med en längre ledtid inte beställs i tid. Om den är för lång, innebär det att för mycket tid läggs ned på att granska och bearbeta information som troligtvis förändras innan den behövs. Du kan ange en planeringshorisont för produktion och en längre horisont för inköp, även om detta inte är ett krav. Du bör ställa in en planeringshorisont för inköp och produktion så att den täcker den totala ledtiden för komponenter.|  
    |**Stoppa och visa första felet**|Markera detta alternativ om du vill att planeringskörningen ska avslutas så snart den stöter på ett fel. Ett meddelande visas med information om felet. Om det finns ett fel, kommer endast de planeringsrader som utfördes innan felet påträffades att visas i planeringsförslaget. Om fältet inte har markerats kommer batchjobbet **Skapa inköpsförslag** att fortsätta tills det har slutförts. Fel kommer inte att avbryta batch-jobbet. Om ett eller flera fel inträffar visas ett meddelande när jobbet är klart om hur många artiklar som påverkas. Sidan **Logg över planeringsfel** öppnas därefter för att visa mer information om felet och länkar till de artikelkort som påverkas.|  
    |**Använd prognos**|Välj en prognos som ska inkluderas som efterfrågan när batch-jobbet körs. Standardprognosen ställer du in på snabbfliken **Planering** på sidan **Produktionsinställningar**.|  
    |**Undanta prognos före**|Bestäm hur mycket av en vald prognos som ska inkluderas i planeringskörningen genom att ange ett datum före vilket ingen prognosefterfrågan inkluderas.|  
    |**Ta hänsyn till planeringsparametrar för undantagsvarningar**|Fältet väljs som standard.<br/><br/> Tillgången på planeringsrader med varningar ändras normalt inte enligt planeringsparametrarna. I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet. Du kan dock ange vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar.<br/><br/>|  

4. På snabbfliken **Artikel** kan du ange filter och köra planeringsrutinerna utifrån på artikel, artikelbeskrivning eller lagerställe.  
5. Välj **OK**. Batch-jobbet körs och planeringsrader läggs till i planeringskalkylbladet.  

## Så här kan du verkställa åtgärdsmeddelanden
  
1. På sidan **Planeringsförslag** väljer du åtgärden **Verkställ åtgärdsmeddelande**.  
2. Ange hur du skapar leveranser på snabbfliken **Alternativ**. Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Produktionsorder**|Ange hur man skapar produktionsorder. Du kan göra detta direkt från planeringsradförslagen. Du kan skapa antingen planerade eller fast planerade produktionsorder.|  
    |**Monteringsorder**|Ange hur du vill skapa monteringsorder. Du kan göra detta direkt från planeringsradförslagen.|  
    |**Inköpsorder**|Ange hur du vill skapa inköpsorder. Du kan göra detta direkt från planeringsradförslagen.<br/><br/> Om du väljer att kopiera planeringsradförslagen för inköpsorder till inköpskalkylarket, väljer du mall- och kalkylarksnamn här.|  
    |**Överföringsorder**|Ange hur du vill skapa överföringsorder. Du kan göra detta direkt från planeringsradförslagen.<br/><br/> Om du väljer att kopiera planeringsradförslagen för överföringsorder till inköpskalkylarket, väljer du mall- och kalkylarksnamn här.|  
    |**Kombinera överföringsorder**|Markera om du vill kombinera överföringsorder.|  
    |**Stoppa och visa första felet**|Markera detta alternativ om du vill att batch-jobbet **Verkställ åtgärdsmeddelande åtgärd. – Plan.** ska avslutas så snart ett fel påträffas. Ett meddelande visas med information om felet. Om det finns ett fel, kommer endast de planeringsrader som bearbetades innan felet påträffades att resultera i leveransorder.|  

3. På snabbfliken **Planeringsrad** kan du ange filter för att begränsa antalet åtgärdsmeddelanden som ska verkställas.  
4. Välj **OK**.  

Batch-jobbet tar bort raderna i planeringsförslaget när åtgärdsmeddelandena har verkställts. De övriga raderna finns kvar i planeringsförslaget tills de antingen accepteras vid ett senare tillfälle eller tas bort. Du kan även ta bort raderna manuellt.  

## Åtgärdsmeddelanden
  
Åtgärdsmeddelanden skickas av orderspårningssystemet när det inte går att uppnå balans inom det befintliga ordernätverket. Meddelandena kan ses som ett förslag på hur du kan bearbeta ändringar som återställer jämvikten mellan tillgång och efterfrågan.  

Genereringen av åtgärdsmeddelanden sker en nivå i taget, med hänsyn till varje artikels lägsta-nivå-kod. På så sätt säkerställs att alla artiklar som är kopplade till eller kommer att vara kopplade till förändringar i tillgång och efterfrågan tas i beaktande.  

Användare kan upprätta dämpare för att undvika att få åtgärdsmeddelanden som är små, onödiga eller oviktiga. Dessa dämpare begränsar genereringen av åtgärdsmeddelanden till sådana meddelanden som innehåller information om förändringar som överskrider den definierade kvantiteten eller definierat antal dagar.  

När du har granskat åtgärdsmeddelandena och bestämt om du vill acceptera några eller alla de föreslagna ändringarna väljer du fältet **Acceptera åtgärdsmeddelande**. Uppdatera sedan scheman i enlighet därmed.  

> [!NOTE]  
> Ett åtgärdsmeddelande är ett förslag om att skapa en ny order, annullera en order eller ändra kvantiteten i eller datumet för en order. Med order menas en inköpsorder, överföringsorder eller produktionsorder.  

Följande åtgärdsmeddelanden genereras som svar på obalans i tillgång/efterfrågan.  

|Åtgärdsmeddelande|Beskrivning|  
|--------------------|---------------------------------------|  
|**Ny**|Om en efterfrågan inte kan tillgodoses genom åtgärdsmeddelanden med förslag om att **Ändra antal**, **Omplanera** eller **Omplanera och ändra** i befintliga order, genereras åtgärdsmeddelandet **Ny**, vilket ger kalkylark om en ny order. Meddelandet **Ny** genereras också om det inte finns leveransordrar i artikelns återbeställningscykel. Med det här alternativet fastställs antalet perioder framåt och bakåt i tillgänglighetsprofilen vid sökning efter en order att omplanera.|  
|**Ändra antal**|När kvantiteten ändras för en efterfrågan som spåras till en leveransorder visas åtgärdsmeddelandet **Ändra antal** Meddelandet anger att relaterad tillgång ska ändras så att det motsvarar förändringen i efterfrågan. Om det uppstår ny efterfrågan söker [!INCLUDE[prod_short](includes/prod_short.md)] efter närmast befintliga icke reserverade leveransorder inom beställningscykeln, och skickar ett åtgärdsmeddelande om ändring för ordern.|  
|**Omplanera**|När ett datum ändras för en leverans- eller behovsorder orsakas obalans i ordernätverket, skickas åtgärdsmeddelandet **Omplanera**. Om det finns ett ett-till-ett-samband mellan tillgång och efterfrågan, skapas ett åtgärdsmeddelande för att föreslå att du flyttar leveransordern. Om leveransordern täcker behovet från fler än en försäljningsorder, omplaneras leveransordern till datumet för det första behovet.|  
|**Omplanera och Ändra antal**|Om både datum och kvantiteter för en order ändras måste du ändra planer med avseende på båda. Åtgärdsmeddelanden samlar båda dessa faktorer i ett enda meddelande, **Planera ändra antal** för att säkerställa att balansen i ordernätverket återställs.|  
|**Annullera**|Om behov som har täckts på orderbasis tas bort, skickas ett åtgärdsmeddelande om att annullera kopplade leveransorder. Om behovet inte täcks på orderbasis, skapas ett åtgärdsmeddelande för att ändra i ordern för att på så sätt minska tillgången. Om en leveransorder inte efterfrågas när du genererar åtgärdsmeddelanden, till exempel vid lagerjusteringar, skickar [!INCLUDE[prod_short](includes/prod_short.md)] åtgärdsmeddelandet **Annullera** i kalkylarket.|  

## Se även  

[Planerad](production-planning.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
