---
title: Designdetaljer - Hantera partiformningsmetoder | Microsoft Docs
description: Översikt över aktiviteter för att definiera en ombeställningsmetod inom leveransplanering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fa9563c503fac844abb67d02934e0a0a666deeab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390055"
---
# <a name="design-details-handling-reordering-policies"></a>Designdetaljer: Hantera partiformningsmetoder
För att en artikel ska ingå i leveransplanering måste en ombeställningsmetod definieras. Följande fyra partiformningsmetoder finns:  

* Fast orderkvantitet  
* Maximalt antal  
* Order  
* Parti-för-parti  

Metoderna Fast orderkvantitet och Maximalt antal avser lagerplanering. Även om lagerplaneringen är tekniskt enklare än motkonteringen, måste de här metoderna finnas samtidigt som steg-för-steg-motkontering av tillgångs- och orderspårning. För att kontrollera integrering mellan de två och ge insyn i den komplicerade planeringslogiken finns strikta principer för hur partiformningsmetoder hanteras.  

## <a name="the-role-of-the-reorder-point"></a>Beställningspunktens roll
Förutom allmän balansering av efterfrågan och tillgång måste planeringssystemet också övervaka lagernivåer för de påverkade artiklarna för att respektera de definierade partiformningsmetoderna.  

En beställningspunkt representerar efterfrågan under ledtid. När det planerade lagret hamnar under lagernivån som definieras av beställningspunkten är det dags att beställa ytterligare antal. Under tiden förväntas lagret minska gradvis och eventuellt nå noll (eller säkerhetslagernivån), tills återanskaffning anländer.  

Planeringssystemet föreslår en framåtplanerad leveransorder när planerat lager hamnar under beställningspunkten.  

Beställningspunkten beskriver en viss lagernivå. Lagernivåer kan förändras markant under tidsenheten, och därför måste planeringssystemet ständigt övervaka det planerade tillgängliga lagret.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Övervaka den planerade lagernivån och beställningspunkten
Lager är en typ av tillgång, men för lagerplanering skiljer planeringssystemet mellan två lagernivåer:  

* Planerat lager  
* Planerat tillgängligt lager  

### <a name="projected-inventory"></a>Planerat lager  
Från början är planerat lager antalet i bruttolager, inklusive tidigare tillgång och efterfrågan även om den inte är bokförd, när planeringsprocessen startas I framtiden blir det en rörlig planerad lagernivå som underhålls av bruttoantal från framtida tillgång och efterfrågan, eftersom de introduceras längs tidslinjen (reserverade eller fördelade på andra sätt).  

Det planerade lagret används i planeringssystemet för att övervaka beställningspunkt och för att bestämma beställningsantal när du använder partiformningsmetoden Maximalt antal.  

### <a name="projected-available-inventory"></a>Planerat tillgängligt lager  
Det planerade tillgängliga lagret är en del av det planerade lagret som vid en viss tidpunkt är tillgängligt för att uppfylla behov. Det planerade tillgängliga lagret används av planeringsmotorn när du övervakar säkerhetslagernivån.  

Det planerade tillgängliga lagret används i planeringssystemet för att övervaka säkerhetslagernivån, eftersom säkerhetslagret alltid måste vara tillgänglig för att uppfylla oväntad efterfrågan.  

### <a name="time-buckets"></a>Tidsenheter  
Om du vill ha en noggrann styrning planerat lager är det avgörande att identifiera när beställningspunkten överstigs och att beräkna rätt partistorlek när du använder partiformningsmetoden Maximalt antal.  

Som angavs tidigare beräknas den planerade lagernivån i början av planeringsperioden. Det är en bruttonivå som inte beaktar reservationer och liknande fördelningar. För att övervaka den här lagernivån under planeringsföljden övervakar systemet de samlade ändringarna över en tidsperiod, en tidsenhet. Systemet ser till att tidsenheten är minst en dag, eftersom det är mest den exakta tidsenheten för en efterfrågan- eller tillgångshändelse.  

### <a name="determining-the-projected-inventory-level"></a>Fastställa den planerade lagernivån  
Följande sekvens beskriver hur den planerade lagernivån fastställs:  

* När en tillförselhändelse, t. ex. en inköpsorder har planerats fullständigt kommer det att öka det planerade lagret på förfallodatumet.  
* När en begäranhändelse har blivit fullständigt uppfylld kommer den inte att minska det planerade lagret direkt. I stället bokförs en minska-påminnelse, vilket är en intern post som innehåller datumet och antalet som läggs till i det planerade lagret.  
* När en efterföljande tillförselhändelse planeras och placeras på tidslinjen, utforskas de bokförda minska-påminnelserna en och en fram tills det planerade datumet för leveransen, medan det planerade lagret uppdateras. Under processen kan beställningspunktsnivån för den interna ökningspåminnelsen ha nåtts eller passerats.  
* Om en ny leveransorder introduceras kontrollerar systemet om den har angetts före den aktuella tillgången. Om det är det, blir den nya tillgången aktuell tillgång och balanseringsproceduren börjar om.  

Följande visar en grafisk illustration av den här principen:  

![Fastställa den planerade lagernivån](media/nav_app_supply_planning_2_projected_inventory.png "Fastställa den planerade lagernivån")  

1. Tillgång **Sa** of 4 (fast) stänger Efterfrågan **Da** of -3.  
2. CloseDemand: Skapa en minska-påminnelse på -3 (visas inte).  
3. Tillgång **Sa** har stängts med ett överskott på 1 (inget mer behov finns).  

     Det här ökar den planerade lagernivån till +4, medan det planerade **tillgängliga** lagret blir -1.  

4. Nästa tillgång **Sb** av 2 (en annan order) redan har placerats på tidsplanen.  
5. Systemet kontrollerar om det finns någon minska-påminnelse som föregår **Sb** (det finns det inte, så ingen åtgärd vidtas).  
6. Systemet stänger tillgång **Sb** (ingen mer efterfrågan finns)—antingen A: genom att minska den till 0 (annullera) eller B: genom att låta den vara som den är.  

     Ökar den planerade lagernivån (A: +0 => +4 or B: +2 = +6).  

7. System gör en sista kontroll: Finns det någon minska-påminnelse? Ja, det finns ett på datumet för **Da**.  
8. Programmet lägger till minska-påminnelsen på -3 påminnelse till den planerade lagernivån, antingen A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I händelse av A skapas automatiskt framåtplanerad order som startar på datumet **Da**.  

     I händelse av B når vi beställningspunkten och en ny order skapas.

## <a name="the-role-of-the-time-bucket"></a>Tidsenhetens roll
Avsikten med tidsenheten är samla efterfråganshändelser i tidssidan för att skapa en gemensam leveransorder.  

För partiformningsmetoder som använder en beställningspunkt kan du ange en tidsenhet. Detta säkerställer att efterfrågan inom samma tidsperiod har ackumulerats innan inverkan på planerat lager kontrolleras och om beställningspunkten har passerats. Om beställningspunkten har passerats framåtplaneras en ny leveransorder från slutet av perioden som definieras av tidsenheten. Tidsenheten börjar på planeringsstartdatumet.  

Konceptet med tidsenhet återspeglar den manuella processen för att kontrollera lagernivån ofta istället för vid varje transaktion. Användaren måste definiera frekvens (tidsenheten). Till exempel samlar användaren alla artikelbehov från en leverantör att göra en veckobeställning.  

![Exempel på tidsenhet för planering](media/nav_app_supply_planning_2_reorder_cycle.png "Exempel på tidsenhet för planering")  

Tidsenhet används allmänt för att undvika en kaskadeffekt. Till exempel skapas en balanserad rad med efterfrågan och tillgång där en tidig efterfrågan annulleras, eller ny skapas. Resultatet skulle vara att varje leveransorder (utom den sista) omplaneras.

## <a name="staying-under-the-overflow-level"></a>Hålla sig under överflödesnivån
När du använder policyer för Maximalt antal och Fast orderkvantitet fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten. Det betyder att planeringssystemet kan föreslå överflödig efterfrågan när negativ efterfrågan eller positiva tillförseländringar uppstår utanför den angivna tidsenheten. Om det av denna anledning föreslås en överflödig leverans, beräknar planeringssystemet vilket antal utleveransen ska minskar till (eller tas bort) för att undvika den överflödiga utleveransen. Denna mängd kallas ”Överflödesnivå”. Överflödet kommuniceras som en planeringsrad med åtgärden **Ändra antal (minska)** eller **Avbryta** eller Annullera och följande varningsmeddelande:  

*Observera! Det planerade lagret [xx] är större än överflödesnivån [xx] på förfallodatumet [xx].*  

![Lagrets överflödesnivå](media/supplyplanning_2_overflow1_new.png "Lagrets överflödesnivå")  

###  <a name="calculating-the-overflow-level"></a>Beräknar överflödesnivån  
Överflödesnivån beräknas på olika sätt beroende på planeringsinställningen.  

#### <a name="maximum-qty-reordering-policy"></a>Partiformningsmetoden Maximalt antal  
Överflödesnivå = beställningsgräns  

> [!NOTE]  
>  Om en lägsta partistorlek finns kommer den läggas till enligt följande: Överflödesnivå = maximalt lager + minsta partistorlek.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Partiformningsmetoden Fast orderkvantitet  
Överflödesnivå = Beställningsantal + beställningspunkt  

> [!NOTE]  
>  Om den minsta partistorleken är större än beställningspunkten, kommer den att ersätta enligt följande: Överflödesnivå= Beställningsantal + minsta partistorlek  

#### <a name="order-multiple"></a>Partistorleksmultipel  
Om en ordermultipel finns justerar den överflödesnivån för partiformningsmetoderna Maximalt antal och Orderkvantitet.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Skapa planeringsraden med överflödesvarning  
När en befintlig leverans gör att det planerade lagret blir högre än överflödesnivån vid slutet av en tidsenhet, skapas en planeringsrad. För att varna för den potentiella överflödiga leveransen har planeringsraden ett varningsmeddelande, fältet **Acceptera åtgärdsmeddelande** markeras inte och åtgärdsmeddelandet är antingen Avbryt eller Ändra antal.  

#### <a name="calculating-the-planning-line-quantity"></a>Beräknar antal för planeringsraden  
Planeringsradantal = antal för aktuell efterfrågan – (planerat lager – överflödesnivå)  

> [!NOTE]  
>  Som med alla varningsrader ignoreras all största/minsta partistorlek eller partistorleksmultipel.  

#### <a name="defining-the-action-message-type"></a>Definiera typen av åtgärdsmeddelande  

-   Om planeringsradantalet är större än 0 är åtgärdsmeddelandet Ändra antal  
-   Om planeringsradantalet är lika med eller mindre än 0 är åtgärdsmeddelandet Avbryt  

#### <a name="composing-the-warning-message"></a>Skapar varningsmeddelandet  
I händelse av överflöde visar sidan **Ej spårade planeringselement** ett varningsmeddelande med följande information:  

-   Den planerade lagernivån som utlöste varningen  
-   Den beräknade överflödesnivån  
-   Förfallodatumet för tillgångshändelsen.  

Exempel: "Det planerade lagret 120 är större än överflödesnivå 60 i 28-01-11”  

### <a name="scenario"></a>Scenario  
I det här scenariot ändrar en kund en försäljningsorder från 70 till 40 stycken mellan två planeringskörningar. Överflödesfunktionen går in för att minska inköpet som föreslogs för den initiala försäljningsantalet.  

#### <a name="item-setup"></a>Artikelinställningar  

|Partiformningsmetod|Maximalt antal|  
|-----------------------|------------------|  
|Max. partistorlek|100|  
|Beställningspunkt|50|  
|Lagersaldo|80|  

#### <a name="situation-before-sales-decrease"></a>Läge före försäljningsminskning  

|Utställning|Ändra antal|Planerat lager|  
|-----------|-----------------|-------------------------|  
|Dag ett|Ingen|80|  
|Försäljning|-70|10|  
|Slut på tidsenheten|Ingen|10|  
|Föreslå ny inköpsorder|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Läge efter försäljningsminskning  

|Ändra|Ändra antal|Planerat lager|  
|------------|-----------------|-------------------------|  
|Dag ett|Ingen|80|  
|Försäljning|-40|40|  
|Inköp|+90|130|  
|Slut på tidsenheten|Ingen|130|  
|Föreslås för att minska inköpet<br /><br /> order från 90 till 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Uppdaterar planeringsrader  
 En planeringsrad (varning) skapas för att minska inköpet med 30 från 90 till 60 för att hålla det planerade lagret på 100 enligt överflödesnivån.  

![Planera enligt överflödesnivå](media/nav_app_supply_planning_2_overflow2.png "Planera enligt överflödesnivå")  

> [!NOTE]  
>  Utan funktionen Överflöde skapas ingen varning om den planerade lagernivån är högre än beställningsgränsen. Det kan orsaka en överflödig leverans av 30.

## <a name="handling-projected-negative-inventory"></a>Hantera lagerplanerat negativt
Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln. När beställningspunkten har passerats är det dags att beställa mer. Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot. Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå.  

 Därför anser planeringssystemet att det är ett nödläge om en framtida efterfrågan inte kan uppfyllas från det planerade lagret, eller uttryckt på ett annat sätt, att det planerade lagret blir negativt. Systemet hanterar ett sådant undantag genom att föreslå en ny leveransorder för att uppfylla en del av behovet som inte kan uppfyllas av lager eller annan tillgång. Orderstorleken för den nya leveransordern beaktar inte maximalt lager eller beställningsantal och beaktar inte heller ordermodifierarna Maximal partistorlek, Minsta partistorlek och Partistorleksmultipel. I stället motsvarar det den exakta bristen.  

 Planeringsraden för den här typen av leveransorder ska innehålla en nödvarningsikon och ytterligare information finns i fältet för att informera användaren om situationen.  

 I följande illustration representerar D en nödleveransorder för att justera för ett negativt lagersaldo.  

 ![Förslag på nödplanering för att undvika negativt lagersaldo](media/nav_app_supply_planning_2_negative_inventory.png "Förslag på nödplanering för att undvika negativt lagersaldo")  

1.  Tillgång **A**, initialt planerat lager, är nedanför beställningspunkt.  
2.  En ny framåtplanerad tillgång skapas (**C**).  

     (Antal = Beställningsgräns – Planerad lagernivå)  
3.  Tillgång **A** är stängd efter efterfrågan **B**, som inte täcks helt.  

     (Behov **B** kan försöka schemalägga Tillgång C, men det kommer inte att hända enligt följande tidsenhetsbegreppet.)  
4.  Ny leverans (**D**) skapas för att täcka det återstående antalet i efterfrågan **B**.  
5.  Efterfrågan **B** är stängd (och skapar en betalningspåminnelse till det planerade lagret).  
6.  Den nya tillgången **D** stängs.  
7.  Planerat lager kontrolleras; beställningspunkten har inte passerats.  
8.  Tillgång **C** är stängd (ingen mer efterfrågan finns).  
9. Sista kontroll: Inga utestående lagernivåpåminnelser finns.  

> [!NOTE]  
>  Moment 4 återspeglar hur godkännandesystemet på tidigare versioner än Microsoft Dynamics NAV 2009 SP1.  

Detta slutför beskrivningen av centrala principer för lagerplanering baserat på partiformningsmetoder. Följande avsnitt beskriver egenskaperna för de fyra partiformningsmetoderna som stöds.

## <a name="reordering-policies"></a>Partiformningsmetoder
Partiformningsmetoder anger hur mycket som ska beställas när artikeln behöver fyllas på. Fyra olika partiformningsmetoder finns.  

### <a name="fixed-reorder-qty"></a>Fast orderkvantitet
Metoden Fast orderkvantitet är relaterad till lagerplaneringen av typiska C-objekt (lagerkostnad låg, låg risk för åldrande och/eller många artiklar). Metoden används vanligtvis i samband med en beställningspunkt som återspeglar den förutsedda efterfrågan under artikelns ledtid.  

#### <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet  
Om planeringssystemet identifierar att beställningspunkten har uppnåtts eller passerats i en viss tidsperiod (beställningscykeln) – över eller vid beställningspunkten i början av perioden, och under eller vid beställningspunktem i slutet av perioden – får du ett förslag om att skapa en ny leveransorder för angivet beställningsantal och framåtplanera den från det första datumet efter slutet av tidsenheten.  

Beställningspunktsbegreppet minskar antalet leveransförslag. Det beskriver en manuell process av att ofta gå genom distributionslagret för att kontrollera det faktiska innehållet på de olika lagerplatserna.  

#### <a name="creates-only-necessary-supply"></a>Skapar bara nödvändigt tillgång  
Innan en ny leveransorder föreslås för att uppfylla en beställningspunkt kontrollerar planeringssystemet om leveransen redan har beställts och ska tas emot inom artikelns ledtid. Om en befintlig leveransorder löser problemet genom att ta det planerade lagret till eller över beställningspunkten inom ledtiden, kommer systemet inte att föreslå en ny leveransorder.  

Leveransorder som skapas specifikt för att uppfylla en beställningspunkt utesluts från vanlig tillgångsbalansering, och kommer inte ändras på något sätt efteråt. Om en artikel som använder beställningspunkt ska fasas ut (inte fyllas på) bör du därför granska utestående leveransorder manuellt eller ändra partiformningsmetoden till Parti-för-parti, varigenom systemet minskar eller att annullerar överflödig tillgång.  

#### <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare  
Ordermodifierarna Minsta partistorlek, Maximal partistorlek och Partistorleksmultipel ska inte spela en större roll när den fasta partiformningsmetoden Fast orderkvantitet används. Planeringssystemet beaktar ända dessa ändringsfält och minskar antalet till den angivna partistorleken (och skapar två eller flera leveranser för att uppnå den totala partistorleken), ökar ordern till den angivna lägsta partistorleken eller avrundar partistorleken upp till en angiven ordermultipel.  

#### <a name="combines-with-calendars"></a>Kombineras med kalendrar  
Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.  

#### <a name="should-not-be-used-with-forecast"></a>Ska inte användas med prognos  
Eftersom den förutsedda efterfrågan redan uttrycks på beställningspunktsnivån, är det inte nödvändigt att ta med en prognos i planeringen av en artikel med hjälp av en beställningspunkt. Om det är relevant att basera planen på en prognos använder du metoden Parti-för-parti.  

#### <a name="must-not-be-used-with-reservations"></a>Får inte användas med reservationer  
Om har användaren reserverat ett antal, till exempel kommer ett antal i lager, för ett avlägset behov, störs planeringsgrunden. Även om den planerade lagernivån är godtagbar i förhållande till beställningspunkten, kan det hända att antalet inte är tillgängligt. Systemet kan försöka att kompensera för det genom att skapa undantagsorder, men du rekommenderas att ange fältet Reservera till Aldrig för artiklar som planeras med hjälp av en beställningspunkt.

### <a name="maximum-qty"></a>Maximalt antal
Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.  

Allt som gäller metoden Fast orderkvantitet gäller även för den här metoden. Den enda skillnaden är antalet på i den föreslagna tillgången. När du använder principen för högsta antal definieras beställningsantalet dynamiskt baserat på den planerade lagernivån och kommer därför vanligtvis att skilja sig åt från order till order.  

#### <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet  
Orderkvantitet bestäms vid tidpunkten (slutet av en tidsenhet) när planeringssystemet identifierar att beställningspunkten har passerats. Vid den här tidpunkten mäter systemet luckan mellan den aktuella planerade lagernivån fram till den angivna beställningsgränsen. Det här fältet utgör antalet som ska beställas. Systemet kontrollerar sedan om tillgång redan har beställts någon annanstans för att tas emot under ledtiden och i så fall minskar antalet på den nya leveransorder genom redan beställda antal.  

Systemet kontrollerar att det planerade lagret minst når beställningspunktnivån – i händelse användaren har glömt att ange en beställningsgränsnivå.  

#### <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare  
Beroende på inställningarna kan det vara bra att kombinera principen Max. ant. med ordermodifierare för att säkerställa en minsta partistorlek eller för att avrunda den till ett heltalsnummer av inköpsenheter, eller dela den i flera partier enligt vad som anges av den maximala orderkvantiteten.  

### <a name="combines-with-calendars"></a>Kombineras med kalendrar  
Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.

### <a name="order"></a>Order
I tillverka-mot-order-miljö köps en artikel in eller produceras för att exklusivt täcka en viss efterfrågan. Vanligtvis gäller det A-artiklar och motiveringen för att välja partiformningsmetoden Order kan vara att efterfrågan är ovanlig, ledtiden är oansenlig eller de obligatoriska attributen varierar.  

Programmet skapar order-till-order-länk som fungerar som ett preliminärt samband mellan tillgången, en leveransorder eller lagret och efterfrågan som ska uppfyllas.  

Förutom att använda orderprincipen kan order-till-order-kopplingen användas på följande sätt vid planeringen:  

* När du använder produktionsprincipen Tillverka-Mot-Order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder).  
* När du använder funktionen Försäljningsorderplanering för att skapa en produktionsorder från en försäljningsorder.  

Även om ett produktionsföretag anser sig vara en miljö som tillverkar mot order, kan det vara bra att använda en partiformningsmetod av typen Parti-för-parti om artiklarna är standardartiklar med attribut utan variation. Det medför att systemet använder oplanerat lager och endast ackumulerar försäljningsorder med samma utleveransdatum eller inom en definierad tidsenhet.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Order-till-order-länkar och utgångna förfallodatum  
Till skillnad från de flesta uppsättningar med tillgång-efterfrågan planeras länkade order med förfallodatum före planeringsstartdatumet helt automatiskt. Affärsorsaken till undantaget är att de specifika uppsättningarna med efterfrågan-tillgång måste synkroniseras till körning. För mer information om den frysta zonen som gäller de flesta typerna av efterfrågan-tillgång, se [Hantera order före planeringsstartdatumet](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

### <a name="lot-for-lot"></a>Parti-för-parti
Parti-för-parti-policyn är den mest flexibla eftersom systemet bara reagerar på faktisk efterfrågan, plus att den agerar på förutsedd efterfrågan från prognos och avropsorder, och sedan avräknar orderantalet baserat på efterfrågan. Parti-för-parti-principen gäller A-och B-artiklar där lager kan accepteras men ska undvikas.  

På vissa sätt liknar parti-för-parti-principen som orderprincipen, men den har en generisk inställning till artiklar: den kan ta emot antal i lager, och den samlar ihop efterfrågan och motsvarande tillgång i tidsenheter som definieras av användaren.  

Tidsenheten definieras i fältet **Tidsenhet**. Systemet arbetar med en lägsta tidsenhet av en dag, eftersom det är den minsta tidsenheten för efterfrågan- och tillgångshändelser i systemet (fast i praktiken kan tidsenheten för produktionsorder och komponentbehov vara sekunder).  

Tidsenheten anger också gränser för när en befintlig leveransorder ska omplaneras för att uppfylla en viss efterfrågan. Om tillgången ligger inom tidsenheten kommer den att planeras om framåt eller bakåt för att uppfylla efterfrågan. Annars, om det ligger tidigare, kommer det att orsaka onödig uppbyggnad av lagersaldot och ska avbrytas. Om det ligger senare, kommer en ny leveransorder att skapas i stället.  

Med den här metoden det är också möjligt att definiera ett säkerhetslager för att kompensera för möjliga variationer i tillgången, eller för att uppfylla plötslig efterfrågan.  

Eftersom leveranspartistorleken baseras på faktiskt behov, kan det vara praktiskt att använda ordermodifierare: avrunda partistorleken uppåt för att uppfylla en viss partistorleksmultipel (eller inköpsenhet), öka beställningen till en viss lägsta partistorlek eller minska partistorleken till det angivna högsta antalet (och skapa därmed två eller flera leveranser för att erhålla den totala behovskvantiteten).

## <a name="see-also"></a>Se även  
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]