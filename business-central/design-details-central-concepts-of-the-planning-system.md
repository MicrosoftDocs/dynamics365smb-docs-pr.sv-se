---
title: Designdetaljer Centrala koncept i planeringssystemet
description: Planering föreslår åtgärder för att användaren ska utföra åtgärder baserat på efterfråge-/leveranstillfället och artikelns planeringsparametrar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Designdetaljer: Centrala koncept i planeringssystemet

Planeringsfunktionerna finns i ett batchprojekt som väljer först de relevanta artiklarna och period att planera för. Sedan, enligt varje artikels lågnivåkod (strukturplats), anropar batch-jobbet en kodenhet som beräknar en leveransplanering. Kodenheten balanserar uppsättningar med tillgång och efterfrågan och föreslår åtgärder som användaren ska vidta. De föreslagna åtgärderna visas som rader i planeringsförslaget eller inköpskalkylarket.  

![Information på sidan Planeringsförslag.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Information på sidan Planeringsförslag")  

Planeraren i ett företag, till exempel en inköpare eller en produktionsplanerare antas vara användaren i planeringssystemet. Planeringssystemet hjälper användaren genom att utföra de omfattande men ganska rättframma beräkningarna av en plan. Användaren kan sedan koncentrera sig på att lösa svårare problem, till exempel när saker är annorlunda än vanligt.  

Planeringssystemet drivs av förväntad och faktisk kundefterfrågan, till exempel prognoser och försäljningsorder. Planeringsberäkningar ger förslag på åtgärder som du kan vidta för att leverera från leverantörer, monteringar, produktion eller överföringar från andra lagerställen. Ett exempel på föreslagen åtgärd kan vara att skapa nya leveransorder, till exempel inköps- eller produktionsorder. Om det redan finns leveransorder kan de föreslagna åtgärderna vara att du till exempel ska öka eller påskynda order som motsvarar förändringarna i efterfrågan.  

Ett annat mål med planeringssystemet är att se till att lagret inte blir onödigt stort. Om efterfrågan minskas får du i planeringssystemet ett förslag om att användaren ska skjuta upp, minska antalet eller annullera befintliga leveransorder.  

En kodenhet innehåller planeringslogik och följande funktioner:

* MRP och MPS
* Beräkna nettoförändringsplan
* Beräkna fullständig plan

Dock omfattar leveransplanberäkningen olika undersystem.  

Planeringssystemet omfattar inte har någon särskild logik för kapacitetsutjämning eller finplanering. Dessa typer av planeringsarbete utförs separat. Bristen på direkt integrering mellan de två områdena betyder också att betydande kapacitet eller schemaändringar kräver att du kör om planeringen.  

## <a name="planning-parameters"></a>Planeringsparametrar

Planeringsparametrar som du anger för en artikel eller en grupp av artiklar styr vilka åtgärder som planeringssystemet föreslår i olika situationer. Definiera planeringsparametrar för varje artikel för att kontrollera när, hur mycket och hur du fyller på.  

Planeringsparametrar kan också definieras för en valfri kombination av artikel, variant och lagerställe genom att skapa en lagerställeenhet (SKU) för varje nödvändig kombination och sedan ange individuella parametrar. Mer information finns i [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md) och [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Planeringsstartdatum

Planeringssystemet hjälper dig att undvika att ha öppna order tidigare och förslag på åtgärder som inte är möjliga. Planering behandlar alla datum före startdatumet som en frusen zon. Följande regel gäller för den frysta zonen:  

* All efterfrågan och tillgång före startdatumet för planeringsperioden anses vara en del av lagret eller levererat. Med andra ord antas att planen för det tidigare har körts enligt den angivna planen. Läs mer på [Hantera order före planeringsstartdatumet](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynamisk orderspårning (pegging)

Dynamisk orderspårning, med sitt samtidiga skapande av åtgärdsmeddelanden i planeringsförslaget, är inte en del av leveransplaneringssystemet. När en efterfrågan eller tillgång skapas eller ändras länkar dynamisk orderspårning efterfrågan och kvantiteterna för att täcka den i realtid.  

Om du till exempel anger eller ändrar en försäljningsorder, söker dynamisk orderspårning omedelbart efter tillgång för att täcka efterfrågan. Tillgång kan vara från lager eller från en förväntad leveransorder (t.ex en inköpsorder eller produktionsorder). När en leveranskälla kopplar [!INCLUDE [prod_short](includes/prod_short.md)] tillgång och efterfrågan. Du öppnar länken på skrivskyddade sidor från dokumentraderna. När tillgången inte kan hittas skapar det dynamiska orderspårningssystemet åtgärdsmeddelanden i planeringsförslaget med tillförselplankalkylark.  

Med dynamisk orderspårning kan du utvärdera om du accepterar leveransorderförslag. Från leveranssidan visas den efterfrågan som skapade tillgången. Från efterfrågesidan identifierar den tillgången som ska täcka efterfrågan.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Exempel på dynamisk orderspårning.":::

Läs mer på [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md).  

I företaget med ett lågt artikelflöde och mindre avancerade produktstrukturer kan det räcka med att använda dynamisk orderspårning för leveransplanering. Men i mer upptagna miljöer ska planeringssystemet användas för att säkerställa att det finns en korrekt balanserad leveransplanering.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamisk orderspårning kontra planeringssystemet

Det kan vara svårt att skilja mellan planeringssystemet och dynamisk orderspårning. Båda funktionerna visar utdata i planeringsförslaget genom att föreslå åtgärder som planeraren bör vidta. Dock skiljer sig sättet som utflödet produceras.  

Planeringssystemet hanterar hela tillgångs- och efterfrågemönstret för en artikel. Alla nivåer i hierarkistrukturen beaktas längs tids linjen. Dynamisk orderspårning är endast en åtgärd som löser situationen i den ordning som aktiverade den. Vid balansering av tillgång och efterfrågan skapar planeringssystemet länkar i ett aktivt kommandoläge. Vid dynamisk orderspårning skapas länkarna automatiskt när du anger en efterfrågan eller tillgång. När du t.ex. skapar en försäljnings- eller inköpsorder.  

Dynamisk orderspårning länkar efterfrågan och tillgång när data anges, i den ordning som de inkommer. Detta kan leda till en viss oordning i prioriteringar. En försäljningsorder som har registrerats först med ett förfallodatum som nästa månad kan t.ex. vara kopplad till leveransen i lager. Nästa försäljningsorder som förfaller i morgon kan orsaka ett åtgärdsmeddelande för att skapa en ny inköpsorder för att täcka det. I följande bild visas detta scenario.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Exempel på orderspårning vid leveransplanering 1.":::

Planeringssystemet behandlar tillgång och efterfrågan för artiklar på en prioriterad order. Ordern prioriteras enligt förfallodatum och ordertyper. Det vill säga på grundval av first-needed-first-served. Den tar bort alla orderspårninglänkar som skapades dynamiskt och återställer dem enligt förfallodatumsprioritet. När planeringssystemet har körts har det löst alla obalanser mellan tillgång och efterfrågan, som illustreras nedan för samma data.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Exempel på orderspårning vid leveransplanering 2.":::  

När du har kört planeringen innehåller inte tabellen Åtgärdsmeddelandetrans. några åtgärdsmeddelanden. Dessa meddelanden ersätts av de åtgärder som föreslås i planeringsförslaget. Läs mer i [Orderspårninglänkar under planering](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Sekvens och prioritet i planering

Sekvensen för beräkningarna i din plan är viktig för att få projektet gjort inom rimlig tid. Prioriteringen av krav och resurser spelar också en viktig roll för att få de bästa resultatet.  

Planeringssystemet är efterfrågestyrt. Artiklar på hög nivå ska planeras före artiklar på låg nivå, eftersom de kan generera efterfrågan för artiklarna på låg nivå. Till exempel återförsäljningslagerställen ska planeras innan distributionscenter planeras, eftersom återförsäljningslagerstället kan innehålla ytterligare efterfrågan från distributionscentret. På en detaljerad balanseringsnivå, om en släppt leveransorder kan täcka en försäljningsorder, bör systemet inte skapa en ny leveransorder. En tillgång med ett specifikt partinummer ska inte fördelas för att täcka en generisk efterfrågan om en annan efterfrågan kräver det specifika partiet.  

### <a name="item-priority--low-level-code"></a>Artikelprioritet/lågnivåkod

I en produktionsmiljö resulterar efterfrågan på en färdig, säljbar artikel i härledd efterfrågan på komponenter som ingår i den färdiga artikeln. Strukturer kontrollerar komponentstrukturen och kan omfatta flera nivåer av halvfärdiga artiklar. När du planerar en artikel på en nivå skapar det härledd efterfrågan på komponenter på nästa nivå. Denna hierarki leder till slut till en härledd efterfrågan på inköpta artiklar. Planeringssystemet planerar för artiklar efter deras rangordning i den totala strukturhierarkin. Systemet startar med färdiga säljbara artiklar på den översta nivån och fortsätter att dela upp produktstrukturen med artiklarna på lägre nivåer (enligt lågnivåkod).  

I följande bild visas i vilken ordning [!INCLUDE [prod_short](includes/prod_short.md)] leveransorder föreslås på den översta nivån. Förslagen antas och artiklar på låg nivå visas också.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Planera för strukturlistor.":::

Mer information om produktionsavvägningar finns i [Läsa in lagerprofilerna](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Optimera prestanda för beräkningar på låg nivå

Beräkningar av kod på låg nivå kan påverka systemprestanda. Om du vill minska effekten kan du inaktivera **Dynamisk beräkning av lågnivåkod** på sidan **Produktionsinställningar**. När du gör det föreslår [!INCLUDE[prod_short](includes/prod_short.md)] att du skapar en post för återkommande jobbkö som uppdaterar koder på låg nivå dagligen. Du kan se till att jobbet kommer att köras utanför arbetstid genom att ange en starttid i fältet **Tidigaste startdatum/starttid**.

Du kan också påskynda beräkningar av kod på låg nivå genom att välja växlingsknappen **Optimera beräkning av kod på låg nivå** på sidan **Produktionsinställningar**.

> [!IMPORTANT]
> Om du väljer att optimera prestanda använder [!INCLUDE[prod_short](includes/prod_short.md)] nya beräkningsmetoder att fastställer koder på låg nivå. Om du har ett tillägg som är beroende av de händelser som används av de gamla beräkningarna kan tillägget sluta fungera.

### <a name="locations--transfer-level-priority"></a>Lagerställen/Prioritet för överföringsnivå

Företag som har verksamhet på fler än ett lagerställe kan behöva planera för varje lagerställe var för sig. Till exempel kan en artikels säkerhetslagernivå och dess partiformningsmetod skilja sig från ett lagerställe till ett annat. Du måste ange planeringsparametrarna per artikel och lagerställe.  

Du kan använda lagerställeenheter för att ange individuella planeringsparametrar. En lagerställeenhet kan ses som en artikel på ett visst lagerställe. Om du inte har definierat någon lagerställeenhet för lagerstället kommer [!INCLUDE [prod_short](includes/prod_short.md)] använda de parametrar som har angetts på artikelkortet. [!INCLUDE [prod_short](includes/prod_short.md)] beräknar endast en plan för aktiva lagerställen, där det finns befintlig efterfrågan eller tillgång för den angivna artikeln.  

Alla artiklar kan hanteras på valfritt lagerställe, men [!INCLUDE [prod_short](includes/prod_short.md)] har en ganska strikt inställning till lagerställebegreppet. En försäljningsorder för en artikel på ett lagerställe kan inte uppfyllas av lager på ett annat lagerställe. Antalet i lager måste först överföras till det lagerställe som anges på försäljningsordern.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Planera för lagerställeenheter.":::

Läs mer på [Designdetaljer: Överföringar i planering](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Orderprioritet

Inom en given lagerställeenhet representerar det begärda eller tillgängliga datumet den högsta prioriteten. Dagens efterfrågan ska hanteras före kommande dagars efterfrågan. Men förutom någon typ av prioritet, sorteras de olika tillgångs- och efterfråganstyperna enligt affärsbetydelse för att bestämma vilken efterfrågan som ska uppfyllas först. På tillgångssidan avgör orderprioriteten källan till tillgången som ska gälla först. Lär dig mer på [Prioritera order](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Efterfrågeprognoser och avropsorder

Både prognoser och avropsorder representerar förutsedd efterfrågan. Avropsorder, som täcker en kunds påtänkta inköp under en viss tidsperiod, fungerar för att minska osäkerheten i den allmänna prognosen. Avropsorder är en kundspecifik prognos utöver för den ospecificerade prognosen som illustreras i följande bild.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Planera med prognoser.":::

Läs mer på [Prognostiserad efterfrågan minskas av försäljningsorder](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Planeringsfördelning

Alla artiklar ska planeras om när mönstret för tillgång och efterfrågan har ändrats sedan den senaste gången en plan beräknades. Om du till exempel anger en ny försäljningsorder eller ändrar en befintlig beräknar du om planen. Andra anledningar för omplandering är en ändring i prognos eller antal i säkerhetslagret. När du ändrar en struktur genom att lägga till eller ta bort en komponent indikerar det troligtvis en ändring, men endast för komponentartikeln.  

Planeringssystemet övervakar sådana händelser och tilldelar lämpliga artiklar för planeringen.  

För flera lagerställen sker fördelningen på nivån med kombinationen av artikel per lagerställe. Om till exempel en försäljningsorder har skapats vid endast ett lagerställe, kommer [!INCLUDE [prod_short](includes/prod_short.md)] att tilldela artikeln vid det specifika lagerstället för planeringen.  

Anledningen för att välja artikel för planeringen är en fråga om systemprestanda. Om ingen ändring i en artikels efterfrågans-/tillgångsmönster har skett kommer planeringssystemet inte att föreslå några åtgärder som ska vidtas. Utan planeringsfördelningen måste systemet utföra beräkningarna för alla artiklar för att avgöra vad som ska planeras för. För att lära dig mer om orsaker till att tilldela en artikel för planering finns i [Designdetaljer: Tabell för planeringsfördelning](design-details-planning-assignment-table.md).  

Följande är tillgängliga planeringsalternativ:  

* **Beräkna fullständig plan** beräknar alla valda artiklar oavsett om det är nödvändigt eller inte.  
* **Beräkna nettoförändringplan** beräknar endast de valda artiklar som har någon ändring i efterfråge-/tillgångsmönstret, och därför har tilldelats för planering.  

Vissa tror att nettoförändringsplaneringen ska utföras i farten, till exempel när försäljningsorder anges. Att planera i farten kan vara förvirrande eftersom dynamisk orderspårning och åtgärdsmeddelanden också beräknas i farten. [!INCLUDE[prod_short](includes/prod_short.md)] ger disponibel att lova-kontroll i realtid. Den innehåller popup-varningar när du anger försäljningsorder och den aktuella leveransplanen inte kan uppfylla efterfrågan.  

Planeringssystemet planerar endast för de artiklar som du har förberett med lämpliga planeringsparametrar. Annars antas det att du planerar artiklarna manuellt eller halvautomatiskt genom att använda funktionen Orderplanering. Mer information om automatiska planeringsförfaranden finns i [Designdetaljer: Balansera tillgång och efterfrågan](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Artikeldimensioner

Tillgång och efterfrågan kan ha variantkoder och lagerställekoder som måste respekteras när planeringssystemet balanserar efterfrågan och tillgång.  

[!INCLUDE [prod_short](includes/prod_short.md)] hanterar variant- och lagerställekoder som artikeldimensioner på en försäljningsorderrad, lagertransaktion och så vidare. Därefter beräknas en plan för varje kombination av variant och lagerställe som om kombinationen är ett separat artikelnummer.  

I stället för att beräkna en teoretisk kombination av variant och lagerställe, beräknar [!INCLUDE [prod_short](includes/prod_short.md)] endast de kombinationer som faktiskt finns i databasen. För att lära dig mer om hur planeringssystemet hanterar lagerställekoder på begäran, gå till [Designdetaljer: Efterfrågan på tomt lagerställe](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Artikelattribut

Artiklar har ofta allmänna attribut, såsom artikelnummer, variantkod, platskod och typ av beställning. Varje tillgångs- och efterfråganshändelse kan dock ha andra specifikationer, t.ex. serie- eller partinummer. Planeringssystemet planerar dessa attribut på vissa sätt beroende på nivån av specifikation.  

Order-till-order-koppling mellan tillgång och efterfrågan är en annan typ av attribut som påverkar planeringssystemet. Lär dig mer [Order-till-order-länkar](#order-to-order-links).

### <a name="specific-attributes"></a>Specifika attribut

Vissa efterfrågansattribut är specifika och en försörjning måste matcha dem exakt.

* Serie-/partinummer som kräver en viss koppling (dessa attribut krävs om du aktiverar växlingsknappen för **SN-specifik spårning** eller **Partispecifik spårning** på sidan **Artikelspårning kodkort** för artikelspårningskoden som används av artikeln).  
* Länkar till leveransorder som skapas manuellt eller automatiskt för en viss efterfrågan (order-till-order-länkar).  

Planeringssystemet gäller följande regler till dessa attribut:  

* Efterfrågan med specifika attribut kan endast uppfyllas av tillgång med matchande attribut.  
* Tillgång med särskilda attribut kan också uppfylla efterfrågan som inte ber specifikt om dessa attribut.  

Om lager eller prognostiserade leveranser inte kan möta en efterfrågan på specifika attribut, föreslår planeringssystemet en ny leveransorder utan att ta hänsyn till planeringsparametrar.  

### <a name="non-specific-attributes"></a>Icke-specifika attribut

Serie- eller partinummerartiklar utan särskilda artikelspårningsinställningar kan ha icke-specifika serie- eller partinummer. Dessa typer av nummer kan tillämpas på alla serie- eller partinummer. Planeringssystemet har mer frihet att matcha, till exempel en serieefterfrågan med en serietillgång, vanligtvis i lagret.  

Tillgång/efterfrågan med serie-eller parti nummer, specifika eller icke-specifika, är hög prioritet och är undantagna från den frysta zonen. De ingår i planeringen även om de förfaller innan startdatumet för planeringen. Mer information finns i [Serie- och partinummer läses in efter specifikationsnivå](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Mer information om hur planeringssystemet balanserar attribut finns i [Serie- och partinummer och order-till-order-länkar är undantagna från den tidigare perioden](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## <a name="order-to-order-links"></a>Order-till-order-länkar

Order till order innebär att du kan köpa, montera eller producera en artikel för en viss efterfrågan. Det finns flera anledningar till att välja den här principen:

* Efterfrågan är ovanlig.
* Ledtiden är obetydlig.
* De nödvändiga attributen varierar.  

Ett annat fall som använder order-till-order-koppling är när en monteringsorder är kopplad till en försäljningsorder i ett scenario med montering mot kundorder.  

Order-till-order-länkar kopplas mellan efterfrågan och tillgång på fyra sätt:  

* När det planerade artikeln använder partiformningsmetoden **Order**  
* När du använder produktionsprincipen tillverka-mot-order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder)  
* När du skapar produktionsorder för försäljningsorder med funktionen Försäljningsorderplanering  
* När du monterar en artikel på en försäljningsorder (**Monteringsmetod** anges till **Montering mot kundorder**)  

Planeringssystemet föreslår att du bara beställer det antal som krävs. Inköps-, produktions- eller monteringsordern fortsätter matcha efterfrågan. Om t.ex en försäljningsorder ändras i tid eller antal, kommer planeringssystemet föreslår att du ändrar leveransorder på samma sätt.  

När order-till-order-länkar finns tar inte planeringssystemet med kopplad tillgång eller lager i balanseringen. Planeraren kan bestämma om man vill använda den kopplade tillgången eller en ny efterfrågan. I det senare fallet kan de ta bort leveransordern eller reservera den kopplade tillgången manuellt.  

Reservationer och orderspårningslänkar bryts om en situation blir omöjlig. Till exempel när efterfrågan flyttas till ett datum som är tidigare än tillgången. Order-till-order-länkar anpassas till ändringar i efterfrågan eller tillgång och bryts aldrig.  

## <a name="reservations"></a>Reservationer

Planeringssystemet tar inte med några reserverade antal i beräkningen. Om t.ex. ett antal för en försäljningsorder är helt eller delvis reserverat kan du inte använda kvantiteten för att täcka andra efterfrågan.

Planeringssystemet tar inte med några reserverade antal i den planerade lagerprofilen. Det måste ta hänsyn till alla kvantiteter för att bestämma när ombeställningspunkten har passerat och hur många som ska beställas för att uppnå den maximala lagernivån. Onödiga reservationer kan öka risken att lagernivåerna bli låga, eftersom planeringslogiken inte identifierar reserverat antal.  

I följande bild visas hur reservationer kan förhindra planering.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Planera med reservationer.":::

Läs mer på [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Varningar

Den första kolumnen i planeringsförslaget är avsedd för varningsfälten. En varningsikon visas när du skapar en planeringsrad för en ovanlig situation.  

Tillgången på planeringsrader med varningar ändras normalt inte enligt planeringsparametrarna. I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet. Systemet kan dock konfigurerar för att följa vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar. Varningsinformationen visas på sidan **Ej spårade planeringselement** som är också användas för att visa orderspårningslänkar till icke orderrelaterade nätverkstyper. Det finns tre typer av varningar:  

* Nödsituation  
* Undantag  
* Observera!  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Varningar i planeringsförslaget.":::

### <a name="emergency"></a>Nödsituation

Varningen för nödsituation visas i två olika situationer:  

* När lagret är negativt på startdatumet för planeringen  
* När det finns antedaterade tillgångs- eller efterfrågehändelser  

Om lagernivån för en artikel är negativ på startdatumet för planeringen föreslår systemet en nödleverans för det negativa antalet med leverans på startdatumet för planeringen. I varningstexten anges startdatumet och antalet i nödordern. Läs mer på [Hantera planerat negativt lagersaldo](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Dokumentrader med förfallodatum före startdatumet för planeringen konsolideras i en nödleveransorder. Beställningen är planerad att anlända på planeringsstartdatum.  

### <a name="exception"></a>Undantag

Undantagsvarningen visas om det planerade disponibla lagret sjunker under nivån för säkerhetslagret. Planeringssystemet föreslår en leveransorder för att uppfylla behovet på förfallodatumet. I varningstexten framgår vilket antal som gäller för artikelns säkerhetslager och det datum då det understigs.  

Överträdelse av säkerhetslagernivån är ett undantag. Det är inte fallet om ombeställningspunkten är korrekt inställd. Mer information finns i [Ombeställningspunktens roll](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Exceptionella orderförslag hjälper till säkerställa att planerat tillgängligt lager aldrig är lägre än säkerhetslagernivån. Det föreslagna antalet täcker säkerhetslager, utan att överväga planeringsparametrarna. Dock i alla scenarier ska orderändringsfält övervägas.  

> [!NOTE]  
> Planeringssystemet kan ha förbrukats säkerhetslagret med avsikt och fyller sedan omedelbart på det. Lär dig mer på [Förbruka säkerhetslager](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### <a name="attention"></a>Observera!

Den här varningen visas i tre olika situationer:  

* Startdatumet för planeringen ligger tidigare än arbetsdatumet.  
* Planeringsraden föreslår att en släppt inköps- eller produktionsorder ändras.  
* Det planerade lagret överstiger överflödesnivån på förfallodatumet. Lär dig mer på [Hålla sig under överflödesnivån](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Vid planeringsrader med varningar är fältet **Acceptera åtgärdsmeddelande** inte markerat, eftersom planeraren förväntas att undersöka dessa rader innan planen utförs.  

## <a name="error-logs"></a>Felloggar

På sidan för förfrågan **Skapa inköpsförslag** kan du välja fältet **Stoppa och visa första felet** för att planeringskörningen ska stanna när den träffar på det första felet. Ett meddelande visas med information om felet. Om det finns ett fel visar planeringsförslaget endast de planeringsrader som gjordes framgångsrikt innan felet inträffade.  

Om fältet inte har markerats kommer batchjobbet **Skapa inköpsförslag** att fortsätta tills det har slutförts. Fel kommer inte att avbryta batch-jobbet. Om det finns fel visas ett meddelande som anger hur många objekt som påverkades. Sidan **Logg över planeringsfel** ger mer information om felet och ange länkar till de dokument eller konfigurationer som påverkas.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Felmeddelanden i planeringsförslaget.":::

## <a name="planning-flexibility"></a>Planeringsflexibilitet

Det är alltid praktiskt att planera en befintlig leveransorder. Till exempel när produktionen har startats eller om du anställer extra personal på en viss dag för att utföra projekt. Om du vill ange om planeringssystemet kan ändra en order kommer alla leveransorderrader ha fältet **Planeringsflexibilitet** med två alternativ: **Obegränsat** och **Ingen**. Om fältet har värdet **Ingen** kommer planeringssystemet inte försöka ändra leveransorderraden.  

Du kan ställa in fältet manuellt, men i vissa fall ställs det in automatiskt av [!INCLUDE [prod_short](includes/prod_short.md)]. Det faktum att du kan ställa in planeringsflexibilitet är viktigt, eftersom det gör det lätt att anpassa användningen av funktionen till olika arbetsflöden och affärsfall. Mer information om hur detta fält används finns i [Designdetaljer: Planerade överföringar](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Orderplanering

Det grundläggande leveransplaneringsverktyget som representeras av sidan **Orderplanering** har utformats för manuellt beslutsfattande. Den beaktar inte några planeringsparametrar och diskuteras därför inte vidare i den här artikeln. Mer information finns i [Planera för ny behovsorder efter order](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Vi rekommenderar att du inte använder orderplanering om företaget redan använder planering eller inköpskalkylark. Leveransorder som skapas från sidan **Orderplanering** kan ändras eller tas bort under den automatiska planeringskörningen. Dessa ändringar beror på att den automatiska planeringskörningen använder planeringsparametrarna och dessa kanske inte beaktas när du skapade den manuella planen på sidan Orderplanering.  

## <a name="finite-loading"></a>Bestämd beläggning

[!INCLUDE[prod_short](includes/prod_short.md)] ger ett grovt schema för att planera rimlig användning av resurser. Den skapar och underhåller inte automatiskt detaljerade scheman baserat på prioriteringar eller optimeringsregler.  

Den avsedda användningen av resursfunktionen för kapacitetsbegränsningar är följande:

* För att undvika överlagring av resurser
* För att säkerställa att kapaciteten inte lämnas ej fördelad om det skulle kunna minska den omvända tiden för en produktionsorder

När du ska planera med kapacitetsbegränsade resurser ser [!INCLUDE [prod_short](includes/prod_short.md)] till att resurser inte beläggs över sin definierade kapacitet (kritisk beläggning). Det tilldelar varje åtgärd till den närmaste tillgängliga tidsluckan. Om tidsluckan inte är tillräckligt stor för att slutföra hela åtgärden kommer åtgärden att uppdelas i två eller flera delar i de närmaste tidsluckorna.  

> [!NOTE]  
> I händelse av åtgärdsdelning tilldelas inställningstiden bara en gång, eftersom det antas att vissa manuella justeringen sker för att optimera schemat.  

Du kan lägga till dämpartid i resurser för att minimera åtgärdsdelning. Denna tid låter [!INCLUDE [prod_short](includes/prod_short.md)] schemalägga beläggningen den sista tänkbara dagen genom att den kritiska beläggningsprocenten överskrids något.  

## <a name="see-also"></a>Se även

[Designdetaljer: Överföringar i planering](design-details-transfers-in-planning.md)  
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)  
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)  
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
