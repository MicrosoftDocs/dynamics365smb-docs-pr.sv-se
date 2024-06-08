---
title: Designdetaljer – Hantera partiformningsmetoder
description: Den här artikeln innehåller en översikt över de partiformningsmetoder som du kan använda vid leveransplanering.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="design-details-handling-reordering-policies"></a>Designdetaljer: Hantera partiformningsmetoder

Om du vill inkludera en artikel i leveransplaneringen måste du ange en partiformningsmetod för artikeln på sidan **artikelkort** . Följande partiformningsmetoder finns:  

* Fast orderkvantitet  
* Maximalt antal  
* Order  
* Parti-för-parti  

Metoderna **Fast partistorlek** och **Maximalt antal** avser lagerplanering. Dessa metoder samverkar med stegvis balansering av tillgångs- och orderspårning.  

## <a name="the-role-of-the-reorder-point"></a>Beställningspunktens roll

En beställningspunkt representerar efterfrågan under ledtid. När lagret planeras att hamna under nivån som definieras av beställningspunkten är det dags att beställa mer. Lagret minskas gradvis tills återanskaffning anländer. Det kan nå noll eller säkerhetslagernivån. Planeringssystemet föreslår en framåtplanerad leveransorder när planerat lager hamnar under beställningspunkten.  

Lagernivåer kan flyttas betydligt under en tidsperiod. Därför övervakar planeringssystemet alltid tillgängligt lager.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Övervaka den planerade lagernivån och beställningspunkten

Lager är en typ av tillgång, men för lagerplanering skiljer planeringssystemet mellan två lagernivåer:  

* Planerat lager  
* Planerat tillgängligt lager  

### <a name="projected-inventory"></a>Planerat lager

I början av planeringsförfarandet är det planerade lagret bruttokvantiteten för lagret. Bruttokvantiteten inkluderar bokförd och inte bokförd tillgång och efterfrågan tidigare. Denna kvantitet blir en planerad lagernivå som innehåller bruttokvantiteter från framtida tillgång och efterfrågan. Framtida tillgång och efterfrågan introduceras längs tidslinjen, oavsett om det är reserverat eller fördelas på annat sätt.  

Planeringssystemet använder planerat lager för att övervaka beställningspunkt och för att bestämma partistorleken när du använder partiformningsmetoden **Maximalt antal**.  

### <a name="projected-available-inventory"></a>Planerat tillgängligt lager

Det planerade tillgängliga lagret är det lager som är tillgängligt för att uppfylla efterfrågan vid en given tidpunkt. Planeringssystemet använder det planerade tillgängliga lagret när säkerhetslagernivån övervakas. Säkerhetslager måste alltid vara tillgängligt för oväntad efterfrågan.  

### <a name="time-buckets"></a>Tidsenheter

Planerat lager är avgörande att identifiera när beställningspunkten överstigs och att beräkna rätt partistorlek när du använder partiformningsmetoden **Maximalt antal**.  

Den planerade lagernivån beräknas i början av planeringsperioden. Det är en bruttonivå som inte beaktar reservationer och andra fördelningar. För att övervaka den här lagernivån under planeringsföljden övervakar planeringssystemet de samlade ändringarna över en tidsperiod. Denna period kallas för en *tidsenhet*. Om du vill veta mer om tidsenheter kan du gå till [tidsenheters roll](#the-role-of-the-time-bucket). Planeringssystemet säkerställer att tidsenheten är minst en dag. En dag är den minsta tidsenheten för efterfråge- och tillgångshändelser.  

### <a name="determining-the-projected-inventory-level"></a>Fastställa den planerade lagernivån

Följande sekvens beskriver hur planeringssystemet fastställer den planerade lagernivån:  

* När en tillgångshändelse, t.ex. en inköpsorder har planerats fullständigt kommer den att öka det planerade lagret på händelsens förfallodatum.  
* När en efterfrågehändelse har blivit fullständigt uppfylld kommer den inte att minska det planerade lagret direkt. I stället bokförs en minska-påminnelse, vilket är en intern post som innehåller datumet och antalet som läggs till i det planerade lagret.  
* När en senare tillgångshändelse planeras och läggs till på tidslinjen, undersöker systemet bokförda minskade påminnelser en i taget efter tillgångens planerade datum. Under processen kan beställningspunktsnivån för den interna ökningspåminnelsen ha nåtts eller passerats.  
* Om en ny leveransorder introduceras kontrollerar den om den har angetts före den aktuella tillgången. Om det är det, blir den nya tillgången aktuell tillgång och balanseringsproceduren börjar om.  

I följande bild visas denna metod.  

![Fastställa den planerade lagernivån.](media/nav_app_supply_planning_2_projected_inventory.png "Fastställa den planerade lagernivån")  

1. Tillgång **Sa** of 4 (fast) stänger Efterfrågan **Da** of -3.  
2. CloseDemand: Skapa en minska-påminnelse på -3 (visas inte).  
3. Tillgång **Sa** har stängts med ett överskott på 1 (ingen mer efterfrågan finns).  

     Det här ökar den planerade lagernivån till +4, medan det planerade **tillgängliga** lagret blir -1.  

4. Nästa tillgång **Sb** av 2 (en annan order) redan har placerats på tidsplanen.  
5. Planeringssystemet kontrollerar om det finns någon minska-påminnelse som föregår **Sb** (i detta exempel finns det inte, så ingen åtgärd vidtas).  
6. Planeringssystemet stänger tillgång **Sb** (ingen mer efterfrågan finns) – antingen A genom att minska den till 0 (annullera) eller B genom att låta den vara som den är.  

     Den planerade lagernivån ökar (A: +0 => +4 eller B: +2 = +6).  

7. Planeringssystemet utför en sista kontroll. Finns det någon minska-påminnelse? Ja, det finns ett på datumet för **Da**.  
8. Planeringssystemet lägger till minska-påminnelsen på -3 påminnelse till den planerade lagernivån, antingen A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. För A skapar planeringssystemet en framåtplanerad order som startar på datumet **Da**. För B nås beställningspunkten och en ny order skapas.

## <a name="the-role-of-the-time-bucket"></a>Tidsenhetens roll

Avsikten med tidsenheten är samla efterfråganshändelser i en tidperiod för att skapa en gemensam leveransorder.  

För partiformningsmetoder som använder en beställningspunkt kan du ange en tidsenhet. Tidsenheter hjälper till att säkerställa att efterfrågan inom samma tidsperiod ackumuleras. Systemet kontrollerar sedan effekten på det planerade lagret och om beställningspunkten har passerats.

Om beställningspunkten har passerats kommer systemet att framåtplanera en ny leveransorder från slutet av tidsenheten. Tidsenheten börjar på planeringsstartdatumet.  

Konceptet med tidsenhet återspeglar den manuella processen för att kontrollera lagernivån ofta istället för vid varje transaktion. Du definierar frekvens (tidsenheten). Till exempel samlar du alla artikelbehov från en leverantör att göra en veckobeställning.  

![Exempel på tidsenhet för planering.](media/nav_app_supply_planning_2_reorder_cycle.png "Exempel på tidsenhet för planering")  

Tidsenheter används ofta för att undvika en kaskadeffekt. Till exempel skapas en balanserad rad med efterfrågan och tillgång där en tidig efterfrågan annulleras, eller ny skapas. Resultatet skulle vara att varje leveransorder (utom den sista) omplaneras.

## <a name="stay-below-the-overflow-level"></a>Stanna under överflödesnivån

När du använder partiformningsmetoderna **Maximalt antal** och **Fast partistorlek** fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten. Det kan föreslå extra tillgång när ändringar i negativ efterfrågan eller positiv tillgång sker utanför tidsenheten. För extra tillgång beräknar planeringssystemet det antal som du vill minska tillgångar med. Denna mängd kallas ”Överflödesnivå”. Överflödet kommuniceras som en planeringsrad med åtgärden **Ändra antal (minska)** eller **Avbryta** och följande varningsmeddelande:  

* Obs! Det planerade lagret [xx] är större än överflödesnivån [xx] på förfallodatumet [xx].*  

![Lagrets överflödesnivå.](media/supplyplanning_2_overflow1_new.png "Lagrets överflödesnivå")  

### <a name="calculating-the-overflow-level"></a>Beräknar överflödesnivån

Överflödesnivån beräknas på olika sätt beroende på partiformningsmetoden.  

#### <a name="maximum-qty"></a>Maximalt antal

Överflödesnivå = beställningsgräns  

> [!NOTE]  
> Om du använder en minsta partistorlek läggs den till enligt följande:
>
> överflödesnivå = beställningsgränsen + minsta partistorlek.  

#### <a name="fixed-reorder-qty"></a>Fast orderkvantitet

överflödesnivå = beställningsantal + beställningspunkt  

> [!NOTE]  
> Om den minsta partistorleken är högre än beställningspunkten ersätts den på följande sätt:
>
> överflödesnivå = beställningsantal + minsta partistorlek  

#### <a name="order-multiple"></a>Partistorleksmultipel

Om en ordermultipel finns justerar den överflödesnivån för partiformningsmetoderna Maximalt antal och fast partistorlek.  

### <a name="creating-the-planning-line-with-an-overflow-warning"></a>Skapa planeringsraden med överflödesvarning

En planeringsrad skapas när en tillgång gör att det planerade lagret blir högre än överflödesnivån vid slutet av en tidsenhet. För att varna för extra tillgång har planeringsraden ett varningsmeddelande, fältet **Acceptera åtgärdsmeddelande** markeras inte och åtgärdsmeddelandet är antingen **Avbryt** eller **Ändra antal.**  

#### <a name="calculating-the-planning-line-quantity"></a>Beräknar antal för planeringsraden

Antalet som finns på planeringsraden beräknas så här:

planeringsradantal = antal för aktuell efterfrågan – (planerat lager – överflödesnivå)  

> [!NOTE]  
> Som med alla varningsrader ignoreras all största/minsta partistorlek eller partistorleksmultipel.  

#### <a name="defining-the-action-message-type"></a>Definiera typen av åtgärdsmeddelande

* Om planeringsradantalet är större än 0 är åtgärdsmeddelandet **Ändra antal.**  
* Om planeringsradantalet är lika med eller mindre än 0 är åtgärdsmeddelandet **Avbryt**  

#### <a name="composing-the-warning-message"></a>Skapar varningsmeddelandet

I händelse av överflöde visar sidan **Ej spårade planeringselement** ett varningsmeddelande med följande information:  

* Den planerade lagernivån som utlöste varningen  
* Den beräknade överflödesnivån  
* Förfallodatumet för tillgångshändelsen  

Exempel: "Det planerade lagret 120 är större än överflödesnivå 60 i 01-28-23”  

### <a name="example-scenario"></a>Exempelscenario

I det här scenariot ändrar en kund en försäljningsorder från 70 till 40 stycken mellan två planeringskörningar. Överflödesfunktionen minskar inköpet som föreslogs för den initiala försäljningsantalet.  

#### <a name="item-setup"></a>Inställningar för artiklar

|Partiformningsmetod|Maximalt antal|  
|-----------------------|------------------|  
|Max. partistorlek|100|  
|Beställningspunkt|50|  
|Lager|80|  

#### <a name="situation-before-sales-decrease"></a>Läge före försäljningsminskning

|Händelse|Ändra antal|Planerat lager|  
|-----------|-----------------|-------------------------|  
|Dag ett|Ingen|80|  
|Försäljning|-70|10|  
|Slut på tidsenheten|Ingen|10|  
|Föreslå ny inköpsorder|+90|100|  

#### <a name="situation-after-sales-decrease"></a>Läge efter försäljningsminskning

|Ändra|Ändra antal|Planerat lager|  
|------------|-----------------|-------------------------|  
|Dag ett|Ingen|80|  
|Försäljning|-40|40|  
|Inköp|+90|130|  
|Slut på tidsenheten|Ingen|130|  
|Föreslås för att minska inköpet<br><br> order från 90 till 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Uppdaterar planeringsrader

Systemet skapar en planeringsrad med en varning för att minska inköpet med 30 från 90 till 60 för att hålla det planerade lagret på 100 enligt överflödesnivån.  

![Planera enligt överflödesnivå.](media/nav_app_supply_planning_2_overflow2.png "Planera enligt överflödesnivå")  

> [!NOTE]  
> Utan funktionen Överflöde skapas ingen varning om den planerade lagernivån är högre än maximala vilket kan orsaka extra tillgång på 30.

## <a name="handling-projected-negative-inventory"></a>Hantera planerat negativt lager

Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln. Det planerade lagret måste vara stort nog för att täcka efterfrågan tills den nya beställningen tas emot. Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå.  

I planeringssystemet anses det vara en nödsituation om en framtida efterfrågan inte kan betjänas från det planerade lagret. Eller, uttryckt på ett annat sätt, att det planerade lagret blir negativt. I systemet föreslås att du skapar en ny leveransorder för att täcka den ouppfyllda delen av efterfrågan. Storleken på den nya leveransordern anser inte att beställningsgränsen eller orderkvantiteten når följande orderändringar:

* Max. partistorlek
* Min. partistorlek
* Partistorleksmultipel 

I stället motsvarar det den exakta bristen.  

Planeringsraden för denna typ av leveransordern kommer att visa en **nödvarningsikon** och ytterligare information om situationen.  

I följande bild representerar D en nödleveransorder för att justera för ett negativt lagersaldo.  

![Förslag på nödplanering för att undvika negativt lagersaldo.](media/nav_app_supply_planning_2_negative_inventory.png "Förslag på nödplanering för att undvika negativt lagersaldo")  

1. Tillgång **A**, initialt planerat lager, är nedanför beställningspunkt.  
2. En ny framåtplanerad tillgång skapas (**C**).  

     (antal = beställningsgräns – planerad lagernivå)  
3. Tillgång **A** är stängd efter efterfrågan **B**, som inte täcks helt.  

     (Efterfrågan **B** kan försöka schemalägga Tillgång C, men tidsenheten förhindrar det.)  
4. Ny leverans (**D**) skapas för att täcka det återstående antalet i efterfrågan **B**.  
5. Efterfrågan **B** är stängd (och skapar en betalningspåminnelse till det planerade lagret).  
6. Den nya tillgången **D** stängs.  
7. Planerat lager kontrolleras. Beställningspunkten har inte passerats.  
8. Tillgång **C** är stängd (ingen mer efterfrågan finns).  
9. Sista kontrollen. Inga utestående lagernivåpåminnelser finns.  

Följande avsnitt beskriver egenskaperna för de fyra partiformningsmetoderna som stöds.

## <a name="reordering-policies"></a>Partiformningsmetoder

Partiformningsmetoder anger hur mycket som ska beställas när artikeln behöver fyllas på. Fyra olika partiformningsmetoder finns.  

### <a name="fixed-reorder-quantity"></a>Fast orderkvantitet

Metoden Fast partistorlek används vanligtvis för lagerplanering för artiklar med följande egenskaper:

* Låg lagerkostnad
* Låg risk för åldrande
* Lågt antal artiklar

Metoden används vanligtvis i samband med en beställningspunkt som återspeglar den förutsedda efterfrågan under artikelns ledtid.  

#### <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet

Om du når eller går över beställningspunkten i en tidsenhet (beställningscykel), föreslår systemet två åtgärder:

* Skapa en ny leveransorder för partistorleken
* Framåtplanera ordern från det första datumet efter slutet på tidsenheten  

Beställningspunktens tidsenhet minskar antalet leveransförslag. Det återspeglar en procedur för att manuellt kontrollera det faktiska innehållet på lagerplatser i distributionslagret.  

#### <a name="creates-only-necessary-supply"></a>Skapar bara nödvändigt tillgång

Innan det föreslår en ny leveransorder för att uppfylla en beställningspunkt söker planeringssystemet efter följande tillgång:

* Om tillgången redan har beställts
* Om du förväntar dig att erhålla tillgången i artikelns ledtid

Systemet kommer inte att föreslå en ny leveransorder om en tillgång tar med planerade lagret till eller över beställningspunkten inom ledtiden.  

Leveransorder som skapas specifikt för att uppfylla en beställningspunkt utesluts från tillgångsbalansering och kommer inte att ändras. Om du vill utfasa en artikel med en beställningspunkt granskar du de utestående leveransorderna manuellt eller byter partiformningsmetod till **parti-för-parti**. Systemet kommer att minska eller avbryta extra tillgång.  

#### <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare

Ordermodifierarna Minsta partistorlek, Maximal partistorlek och Partistorleksmultipel ska inte spela en betydande roll när du använder metoden Fast orderkvantitet. I planeringssystemet tas dessa emellertid med i beräkningen:

* Minska antalet till den angivna maximala partistorleken (och skapa två eller fler tillgångar för att nå den totala partistorleken)
* Öka ordern till den angivna minsta partistorleken
* Avrunda partistorleken för att uppfylla en angiven ordermultipel  

#### <a name="combines-with-calendars"></a>Kombineras med kalendrar

Innan en ny leveransorder föreslås för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om ordern är schemalagd för en ledig dag. De kalendrar som du anger i fältet **Baskalenderkod** på sidorna **Företagsinformation** och **Lagerställekort**.  

Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Om du flyttar datumet kan det leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.  

#### <a name="shouldnt-be-used-with-forecasts"></a>Ska inte användas med prognos

Eftersom den förutsedda efterfrågan redan uttrycks på beställningspunktsnivån, är det inte nödvändigt att ta med en prognos i planeringen. Om det är relevant att basera planen på en prognos använder du metoden **Parti-för-parti**.  

#### <a name="must-not-be-used-with-reservations"></a>Får inte användas med reservationer

Om du har reserverat ett antal, till exempel kommer ett antal i lager, för ett avlägset behov, störs planeringsgrunden. Även om den planerade lagernivån är godtagbar i förhållande till beställningspunkten, kan det hända att antalet inte är tillgängligt. Systemet kan försöka kompensera genom att skapa undantagsorder. Vi rekommenderar dock att fältet **Reservera** inte har ställts in på **Aldrig** för artiklar som planeras med en beställningspunkt.

### <a name="maximum-quantity"></a>Maximalt antal

Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.  

Allt som gäller metoden Fast orderkvantitet gäller även för den här metoden. Den enda skillnaden är antalet på i den föreslagna tillgången. När du använder principen för högsta antal definieras beställningsantalet dynamiskt baserat på den planerade lagernivån. Därför skiljer den sig vanligen från order till order.  

#### <a name="calculate-per-time-bucket"></a>Beräknat per tidsenhet

När du når eller går över beställningspunkten bestäms partiformningsmetoden vid slutet av en tidsenhet. Det mäter luckan mellan den aktuella planerade lagernivån och den angivna beställningsgränsen för att bestämma antal i order. Systemet kontrollerar sedan:

* Om tillgången redan har beställts
* Om du förväntar dig att erhålla tillgången i artikelns ledtid

I så fall minskar systemet kvantiteten på den nya leveransordern med de kvantiteter som redan har beställts.  

Om du inte anger en maximal lagerkvantitet ser planeringssystemet till att det planerade lagret når orderkvantiteten.

#### <a name="combine-with-order-modifiers"></a>Kombineras med ordermodifierare

Beroende på din inställning kanske det är bäst att kombinera principen för maximalt antal med ordermodifierare: 

* För att säkerställa minsta partistorlek
* Avrunda antalet till ett heltalsnummer för inköpsenheter
* Dela kvantiteten i partier som definieras av den maximal partistorleken  

### <a name="combine-with-calendars"></a>Kombineras med kalendrar

Innan en ny leveransorder föreslås för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om ordern är schemalagd för en ledig dag. De kalendrar som du anger i fältet **Baskalenderkod** på sidorna **Företagsinformation** och **Lagerställekort**.  

Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Om du flyttar datumet kan det leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.

### <a name="order"></a>Order

I tillverka-mot-order-miljö köps en artikel in eller produceras för att täcka en viss efterfrågan. Partiformningsmetoden används vanligtvis för artiklar med följande egenskaper

* Efterfrågan är ovanlig
* Ledtiden är obetydlig
* De nödvändiga attributen varierar  

[!INCLUDE [prod_short](includes/prod_short.md)] skapar order-till-order-länk som fungerar som ett preliminärt samband mellan tillgången (en leveransorder eller lagret) och efterfrågan. Du kan koppla en order till order-länk under planeringen på följande sätt:  

* När du använder produktionsprincipen Tillverka-Mot-Order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder)  
* När du använder funktionen Försäljningsorderplanering för att skapa en produktionsorder från en försäljningsorder  

> [!TIP]
> Om artikelattribut inte varierar kanske det är bäst att använda partiformningsmetoden parti-för-parti. Det medför att systemet använder oplanerat lager och endast ackumulerar försäljningsorder med samma utleveransdatum eller inom en definierad tidsenhet.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Order-till-order-länkar och utgångna förfallodatum

Till skillnad från de flesta uppsättningar med tillgång-efterfrågan planeras länkade order med förfallodatum före planeringsstartdatumet helt automatiskt. Orsaken till undantaget är att de specifika uppsättningarna med efterfrågan-tillgång måste synkroniseras. För mer information om den frysta zonen som gäller de flesta typerna av efterfrågan-tillgång, se [Hantera order före planeringsstartdatumet](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### <a name="lot-for-lot"></a>Parti-för-parti

Parti-för-parti-metoden är den mest flexibla eftersom systemet endast reagerar på faktisk efterfrågan. Det fungerar på förutsedd efterfrågan från prognos och avropsorder och avräknar sedan orderkvantiteten baserat på efterfrågan. Metoden gäller för artiklar där lager kan accepteras men ska undvikas.  

På vissa sätt påminner parti-för-parti-metoden om orderprincipen. Den kan godta antal i lagret och sedan bunta in efterfrågan och tillgång i de tidsenheter du definierar.

Du anger tidsenheter i fältet **Tidsenhet** på sidan **Artikelkort**. Den minsta storleken på tidsenheten är en dag, eftersom det är den minsta måttenheten för tillgångs- och efterfrågehändelserna i [!INCLUDE [prod_short](includes/prod_short.md)].  

Tidsenheten anger också gränser för när du ska omplanera en leveransorder för att uppfylla en viss efterfrågan. Tillgången ligger inom tidsenheten kommer den att planeras om framåt eller bakåt för att uppfylla efterfrågan. Tidigare tillgång kommer att orsaka extra lager och du bör avbryta den. För tillgång som är senare, skapa en ny leveransorder.  

Med den här metoden kan du ange ett säkerhetslager för att kompensera ändringar i tillgång eller för att uppfylla en oväntad efterfrågan. Metoden parti-för-parti kan också innehålla en utjämningsperiod och utjämningsantal som reducerar orderplaneringen.  

Tillsammans med fältet **Omplaneringsperiod** bidrar **Partiackumuleringsperiod** till att definiera företagets beställningscykeln. Från datumet för det första behovet samlas alla behov i nästa partiackumuleringsperiod till en leveransorder på datumet för det första behovet. Behov som ligger utanför partiackumuleringsperioden omfattas inte av leveransorder.

Eftersom leveranspartistorleken baseras på den faktiska efterfrågan, kan det vara praktiskt att använda ordermodifierare:

* Avrunda orderkvantiteten för att uppfylla en ordermultipel (eller inköpsenhet)
* Öka ordern till den angivna minsta partistorleken
* Minska antalet till det angivna maximala antalet (och skapa två eller fler tillgångar för att nå det totala antalet som behövs)

## <a name="see-also"></a>Se även

[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)  
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)  
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
