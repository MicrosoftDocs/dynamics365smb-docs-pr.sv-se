---
title: Designdetaljer - Centrala koncept i planeringssystemet| Microsoft Docs
description: Planeringsfunktionerna ingår i ett batch-jobb som först väljer alla relevanta artiklar och planeringsperiod, och som sedan föreslår möjliga åtgärder som användaren kan vidta baserat på rådande tillgång/efterfrågan och artiklarnas planeringsparametrar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6cfe028d21086269f1492aefde31fe6b659d06b4
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788127"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Designdetaljer: Centrala koncept i planeringssystemet
Planeringsfunktionerna finns i ett batchjobb som väljer först de relevanta artiklarna och period att planera för. Enligt varje artikels lägsta-nivå-kod (strukturposition) anropar batchjobbet sedan en kodenhet som beräknar en tillförselplan genom att balansera uppsättningar med tillgång-efterfrågan och föreslår möjliga åtgärder som användaren kan vidta. De föreslagna åtgärderna visas som rader i planeringsförslaget eller inköpskalkylarket.  

![Information på sidan Planeringsförslag](media/NAV_APP_supply_planning_1_planning_worksheet.png "Information på sidan Planeringsförslag")  

Planeraren i ett företag, till exempel en inköpare eller en produktionsplanerare antas vara användaren i planeringssystemet. Planeringssystemet hjälper användaren genom att utföra de omfattande men ganska rättframma beräkningarna av en plan. Användaren kan sedan koncentrera sig på att lösa svårare problem, till exempel när saker är annorlunda än vanligt.  

Planeringssystemet drivs av förväntad och faktisk kundefterfrågan, till exempel prognoser och försäljningsorder. Om du kör planeringsberäkningen får du i programmet ett förslag på särskilda åtgärder för användaren att vidta för eventuell leverans från leverantörer, monterings- eller produktionsavdelningar, eller överföringar från andra distributionslager. De föreslagna åtgärderna kan vara att skapa nya leveransorder, till exempel inköps - eller produktionsorder. Om det redan finns leveransorder kan de föreslagna åtgärderna vara att du till exempel ska öka eller påskynda order som motsvarar förändringarna i efterfrågan.  

Ett annat mål med planeringssystemet är att se till att lagret inte blir onödigt stort. Om efterfrågan minskas får du i planeringssystemet ett förslag om att användaren ska skjuta upp, minska antalet eller annullera befintliga leveransorder.  

Nettobehov och produktionsprogram, beräkna nettoförändringsplan och beräkna fullständig plan är alla operationer inom en kodenhet som innehåller planeringslogiken. Dock användare leveransplanberäkningen olika undersystem.  

Observera att planeringssystemet inte har någon särskild logik för kapacitetsutjämning eller finplanering. Därför utförs sådant schemaarbete som en separat funktion. Bristen på direkt integrering mellan de två områdena betyder också att betydande kapacitet eller schemaändringar kräver att planeringen körs igen.  

## <a name="planning-parameters"></a>Planeringsparametrar  
Planeringsparametrar som användar anger för en artikel eller en grupp av artiklar styr vilka åtgärder som planeringssystemet föreslår i olika situationer. Planeringsparametrarna definieras på varje artikelkort för att kontrollera när, hur mycket och hur du fyller på.  

Planeringsparametrar kan också definieras för en valfri kombination av artikel, variant och lagerställe genom att skapa en lagerställeenhet (SKU) för varje nödvändig kombination och sedan ange individuella parametrar.  

Mer information finns i [Designdetaljer: Hantera principer för omordning](design-details-handling-reordering-policies.md) och [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Planera startdatum  
För att undvika en leveransplanering som tar med öppna tidigare order och föreslår eventuellt omöjliga på åtgärder, behandlar planeringssystemet alla datum före planeringsstartdatumet som en fryst zon där följande specialregel gäller:  

All efterfrågan och tillgång före startdatumet för planeringsperioden anses vara en del av lagret eller levererat.  

Med andra ord antas att planen för det tidigare har körts enligt den angivna planen.  

Mer information finns i [Hantera order före planeringsstartdatumet](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynamisk orderspårning (pegging)  
Dynamisk orderspårning, med sitt samtidiga skapande av åtgärdsmeddelanden i planeringsförslaget, är inte en del av leveransplaneringssystemet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Den här funktionen länkar, i realtid, behovet och det antal som kan täcka det när en ny efterfrågan eller tillgång registreras eller ändras.  

Till exempel om användaren anger eller ändrar en försäljningsorder söker det dynamiska orderspårningsystemet omedelbart efter en lämplig tillgång för att täcka efterfrågan. Det kan vara från lager eller från en förväntad leveransorder (t.ex en inköpsorder eller produktionsorder). När en tillförselkälla hittas skapar systemet en länk mellan tillgång och efterfrågan och visar den i skrivskyddade sidor som nås från de berörda dokumentraderna. När lämplig efterfrågan inte kan hittas skapar det dynamiska orderspårningsystemet åtgärdsmeddelanden i planeringsförslaget med tillförselplankalkylark som återspeglar dynamiskt saldo. Den dynamiska orderspårningsystemet har ett grundläggande planeringssystem som kan vara till hjälp både för planeraren och andra roller i den interna försörjningskedjan.  

Dynamisk orderspårning kan alltså ses som ett verktyg som hjälper användare att bedöma om de ska acceptera de föreslagna leveransordrarna. Från tillgångssidan kan en användare se vilken efterfrågan som har skapat tillgången, och från efterfråganssidan vilken tillgång som ska täcka efterfrågan.  

![Exempel på dynamisk orderspårning](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Exempel på dynamisk orderspårning")  

För mer information, se [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)  

I företaget med ett lågt artikelflöde och mindre avancerade produktstrukturer kan det vara lämpligt att använda dynamisk orderspårning som huvudsakliga typ av tillförselplanering. Men i mer upptagna miljöer ska planeringssystemet användas för att säkerställa att det alltid finns en korrekt balanserad leveransplanering.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamisk orderspårning kontra planeringssystemet  
Vid en snabb överblick kan det vara svårt att skilja mellan planeringssystemet och dynamisk orderspårning. Båda funktionerna visar utdata i planeringsförslaget genom att föreslå åtgärder som planeraren bör vidta. Dock skiljer sig sättet som utflödet produceras.  

Planeringssystemet hanterar hela mönstret för tillgång-efterfrågan via alla nivåer av strukturhierarkin i tidslinjen, medan dynamisk orderspårning endast hanterar läget för ordern som aktiverade den. När tillgång och efterfrågan balanseras, skapar planeringssystemet länkar i användaraktiverat grupperingsläge, medan dynamisk orderspårning skapar länkarna automatiskt i farten, oavsett när användaren anger ett behov eller en leverans i programmet, t.ex. försäljningsorder eller inköpsorder.  

Dynamisk orderspårning skapar länkar mellan efterfrågan och tillgång när data anges, i den ordning som de inkommer. Det kan leda till en viss oordning i prioriteringar. Exempelvis kan en försäljningsorder som har angetts först, med förfallodatum nästa månad, kopplas till tillgången i lager, medan nästa försäljningsorder som förfaller imorgon kan orsaka ett åtgärdsmeddelande att skapa en ny inköpsorder för att täcka den, som illustreras nedan.  

![Exempel på orderspårning vid leveransplanering 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Exempel på orderspårning vid leveransplanering 1")  

Som motsats hanterar planeringssystemet all efterfrågan och tillgång för en viss artikel, i prioriterad ordning enligt förfallodatum och ordertyper, d.v.s., enligt first-needed/first-served. Den tar bort alla orderspårninglänkar som skapades dynamiskt och återställer dem enligt förfallodatumsprioritet. När planeringssystemet har körts har det löst alla obalanser mellan tillgång och efterfrågan, som illustreras nedan för samma data.  

![Exempel på orderspårning vid leveransplanering 2](media/NAV_APP_supply_planning_1_planning_graph.png "Exempel på orderspårning vid leveransplanering 2")  

Efter planeringskörningen återstår inga åtgärdsmeddelanden i tabellen Åtgärdsmeddelandetrans. eftersom de har ersatts med de föreslagna åtgärderna i planeringsförslaget  

Mer information finns i länkarna för orderspårning under planering i [Balansera tillgång och efterfrågan](design-details-balancing-demand-and-supply.md#balancing-supply-with-demand).  

## <a name="sequence-and-priority-in-planning"></a>Sekvens och prioritet i planering  
När du upprättar en plan är sekvensen med beräkningarna viktig för att få jobbet gjort inom en rimlig tidsram. Dessutom spelar prioriteringen av krav och resurser en viktig roll för att få de bästa resultatet.  

Planeringssystemet i [!INCLUDE[d365fin](includes/d365fin_md.md)] efterfrågestyrt. Artiklar på hög nivå ska planeras före artiklar på låg nivå, eftersom planen för artiklar på hög nivå artiklar kan generera ytterligare efterfrågan för artiklarna på låg nivå. Det innebär till exempel att återförsäljningslagerställen ska planeras innan distributionscenter planeras, eftersom planen för ett återförsäljningslagerställe kan innehålla ytterligare efterfrågan från distributionscentret. På en detaljerad saldonivå betyder det också att en försäljningsorder inte ska aktivera en ny leveransorder om en redan släppt leveransorder kan täcka försäljningsordern. På samma sätt ska en tillgång med ett specifikt partinummer inte fördelas för att täcka en generisk efterfrågan om en annan efterfrågan kräver det specifika partiet.  

### <a name="item-priority--low-level-code"></a>Artikelprioritet / lågnivå kod  
I en produktionsmiljö resulterar efterfrågan på en färdig, säljbar artikel i härledd efterfrågan på komponenter som ingår i den färdiga artikeln. Strukturer kontrollerar komponentstrukturen och kan omfatta flera nivåer av halvfärdiga artiklar. När du planerar en artikel på en nivå skapar det härledd efterfrågan på komponenter på nästa nivå, och så vidare. Det leder till slut till en härledd efterfrågan på inköpta artiklar. Därför planerar planeringssystemet för artiklar i den ordning som de är rankade i den totala strukturhierarkin, och börjar med färdiga säljbara artiklar på högsta nivån och fortsätter nedåt via produktstrukturen till artiklarna för lägre nivå (enligt lägsta-nivå-koden).  

![Planera för strukturlistor](media/NAV_APP_supply_planning_1_BOM_planning.png "Planera för strukturlistor")  

Figurerna visar i vilken följd systemet gör förslag för leveransorder på högsta nivån och om användaren godkänner dessa kalkylark, även för alla artiklar på lägre nivå.  

Mer information om produktionsavvägningar finns i [Läsa in lagerprofilerna](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

### <a name="locations--transfer-level-priority"></a>Lagerställen/Prioritet för överföringsnivå  
Företag som har verksamhet på fler än ett lagerställe kan behöva planera för varje lagerställe var för sig. Till exempel kan en artikels säkerhetslagernivån och dess partiformningsmetod skilja sig från ett lagerställe till ett annat. I det här fallet måste planeringsparametrarna anges per artikel och även per lagerställe.  

Det stöds med användning av lagerställeenheter där enskilda planeringsparametrar kan anges på nivån med lagerställeenheter. En lagerställeenhet kan ses som en artikel på ett visst lagerställe. Om användaren inte har definierat en lagerställeenhet för lagerstället kommer programmet att återgå till parametrarna som har angetts på artikelkortet. Programmet beräknar en plan endast för aktiva lagerställen, d.v.s där det finns befintligt behov eller tillgång för den angivna artikeln.  

I princip kan valfri artikel hanteras på valfritt lagerställe, men programmets inställning till lagerställebegreppet är ganska strikt. En försäljningsorder för ett lagerställe kan exempelvis inte uppfyllas av lagersaldo på ett annat lagerställe. Antalet i lager måste först överföras till det lagerställe som anges på försäljningsordern.  

![Planera för lagerställeenheter](media/NAV_APP_supply_planning_1_SKU_planning.png "Planera för lagerställeenheter")  

Mer information finns i [Designdetaljer: Planerade överföringar](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Orderprioritet  
Inom en given lagerställeenhet representerar det begärda eller tillgängliga datumet den högsta prioriteten. Dagens efterfrågan ska hanteras före kommande dagars efterfrågan. Men förutom någon typ av prioritet, sorteras de olika tillgångs- och efterfråganstyperna enligt affärsbetydelse för att bestämma vilken efterfrågan som ska uppfyllas innan en annan efterfrågan uppfylls. På tillförselsidan avgör orderprioriteten vilken tillgångskälla som ska kopplas innan du kopplar andra tillgångskällor.  

Mer information finns i [Prioritera order](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Efterfrågeprognoser och avropsorder  
Både prognoser och avropsorder representerar förutsedd efterfrågan. Avropsorder, som täcker en kunds påtänkta inköp under en viss tidsperiod, fungerar för att minska osäkerheten i den allmänna prognosen. Avropsorder är en kundspecifik prognos utöver för den ospecificerade prognosen som illustreras under.  

![Planera med prognoser](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planera med prognoser")  

Mer information finns i avsnittet ”Prognosefterfrågan minskas genom försäljningsorder” i [Läsa in lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

## <a name="planning-assignment"></a>Planeringsfördelning  
Alla artiklar ska planeras för, men det finns ingen anledning att beräkna en plan för en artikel om det inte har skett någon ändring i efterfråge- eller tillgångsmönstret sedan senaste gången som en plan beräknades.  

Om användaren har angett en ny försäljningsorder eller har ändrat en befintlig finns det anledning att beräkna om planen. Andra anledningar är en ändring i prognos eller önskat antal i säkerhetslagret. När du ändrar en struktur genom att lägga till eller ta bort en komponent indikerar det troligtvis en ändring, men endast för komponentartikeln.  

Planeringssystemet övervakar sådana händelser och tilldelar lämpliga artiklar för planeringen.  

För flera lagerställen sker fördelningen på nivån med kombinationen av artikel per lagerställe. Om till exempel en försäljningsorder har skapats vid endast ett lagerställe, kommer programmet att tilldela artikeln vid det specifika lagerstället för planeringen.  

Anledningen för att välja artikel för planeringen är en fråga om systemprestanda. Om ingen ändring i en artikels efterfrågans-/tillgångsmönster har skett kommer planeringssystemet inte att föreslå några åtgärder som ska vidtas. Utan planeringsfördelningen måste systemet utföra beräkningarna för alla artiklar för att avgöra vad som ska planeras för, och det skulle dränera systemresurser.  

Den fullständiga listan över anledningar för att tilldela en artikel för planering finns i [Designdetaljer: Tabell för planeringsfördelning](design-details-planning-assignment-table.md).  

Planeringsalternativen i [!INCLUDE[d365fin](includes/d365fin_md.md)] är:  

-   Beräkna fullständig plan – Beräknar alla valda artiklar oavsett om det är nödvändigt eller inte.  
-   Beräkna nettoförändringplan – Beräknar endast de valda artiklar som har någon ändring i efterfråge-/tillgångssmönstret, och därför har tilldelats för planering.  

Vissa användare tror att nettoförändringsplaneringen ska utföras i farten, till exempel när försäljningsorder anges. Det kan vara förvirrande eftersom dynamisk orderspårning och åtgärdsmeddelanden också beräknas i farten. Dessutom erbjuder [!INCLUDE[d365fin](includes/d365fin_md.md)] realtidstillgänglig Disponibel att lova-kontroll, som ger popup-varningar när du anger försäljningsorder om behovet inte kan uppfyllas enligt den aktuella finns leveransplaneringen.  

Utöver dessa fall planerar planeringssystemet endast för de artiklar som användaren har förberett med lämpliga planeringsparametrar. Annars antas det att användaren planerar artiklarna manuellt eller halvautomatiskt genom att använda funktionen Orderplanering.  

Mer information om automatiska planeringsförfaranden finns i [Designdetaljer: Balansera tillgång och efterfrågan](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Artikeldimensioner  
Tillgång och efterfrågan kan ha variantkoder och lagerställekoder som måste respekteras när planeringssystemet balanserar efterfrågan och tillgång.  

Systemet hanterar variant- och lagerställekoder som artikeldimensioner på en försäljningsorderrad, lagertransaktion och så vidare. Därefter beräknas en plan för varje kombination av variant och lagerställe som om kombinationen är ett separat artikelnummer.  

I stället för att beräkna en teoretisk kombination av variant och lagerställe, beräknas endast de kombinationer som faktiskt finns i databasen.  

Se [Designdetaljer: Efterfrågan på tomt lagerställe](design-details-balancing-demand-and-supply.md) för mer information om hur planeringssystemet hanterar platskoder på begäran.  

## <a name="item-attributes"></a>Artikelattribut  
Förutom allmänna artikeldimensioner, t.ex artikelnummer, variantkod, lagerställekod och typ av order, kan varje tillgångs- och efterfråganshändelse ha ytterligare specifikationer i form av serie-/partinummer. Planeringssystemet planerar dessa attribut på vissa sätt beroende på nivån av specifikation.  

Order-till-order-koppling mellan tillgång och efterfrågan är en annan typ av attribut som påverkar planeringssystemet.  

### <a name="specific-attributes"></a>Specifika attribut  
Vissa attribut på efterfrågan är specifika och måste exakt matchas av en motsvarande tillgång. Följande två specifika attribut finns:  

-   Efterfrågade serie-/partinummer som kräver en viss koppling (kryssrutan **SN-specifik spårning** eller **Partispecifik spårning** är markerad på sidan **Kodkort för artikelspårning** för artikelspårningskoden som används av artikeln).  
-   Länkar till leveransorder som skapas manuellt eller automatiskt för en viss efterfrågan (order-till-order-länkar).  

För dessa attribut har planeringssystemet följande regler:  

-   Efterfrågan med specifika attribut kan endast uppfyllas av tillgång med matchande attribut.  
-   Tillgång med särskilda attribut kan också uppfylla behov som inte ber specifikt om dessa attribut.  

Om ett behov för specifika attribut inte kan uppfyllas av lager eller planerade leveranser, kommer planeringssystemet att föreslå en ny leveransorder som täcker den aktuella efterfrågan utan hänsyn till planeringsparametrar.  

### <a name="non-specific-attributes"></a>Icke-specifika attribut  
Serie-/partinumrerade artiklar utan specifik artikelspårningsinställning kan ha serie-/partinummer som inte måste kopplas till exakt samma serie-/partinummer, men kan kopplas till varje serie- eller partinummer. Det ger planeringssystemet mer frihet att matcha, till exempel en serieefterfrågan med en serietillgång, vanligtvis i lagret.  

Efterfrågan med serie-/partinummer, specifika eller icke-specifika, anses högprioriterade och är därför undantagna från den frysta zonen, vilket betyder att de ska ingå i planering även om de förfaller före planeringsstartdatumet.  

Mer information finns i avsnittet "Serie-/partinummer läses in efter specifikationsnivå" i [Läsa in lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

Mer information om hur planeringssystemet balanserar attribut finns i [Serie-/partinummer och Order-till-order-länkar är undantagna från den frysta zonen](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Order-till-Order-länkar  
Order-till-order-anskaffning betyder att en artikel köps in, monteras eller produceras för att exklusivt täcka en viss efterfrågan. Vanligtvis gäller det A-artiklar och motiveringen för att välja den här metoden kan vara att efterfrågan är ovanlig, ledtiden är oansenlig eller de obligatoriska attributen varierar.  

Ett annat specialfall som använder order-till-order-koppling är när en monteringsorder är kopplad till en försäljningsorder i ett scenario med montering mot kundorder.  

Order-till-order-länkar kopplas mellan efterfrågan och tillgång på fyra sätt:  

-   När det planerade artikeln använder partiformningsmetoden Order.  
-   När du använder produktionsprincipen Tillverka-Mot-Order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder).  
-   När du skapar produktionsorder för försäljningsorder med funktionen Försäljningsorderplanering.  
-   När du sammanställer en artikel till en försäljningsorder. (Monteringsmetoden anges till Montering mot kundorder.  

I dessa fall föreslår planeringssystemet bara att beställa det antal som krävs. När den har skapats fortsätter inköps-, produktions- eller monteringsordern att matcha den motsvarande efterfrågan. Om t.ex en försäljningsorder ändras i tid eller antal, kommer planeringssystemet att föreslå att motsvarande leveransorder ändras på samma sätt.  

När order-till-order-länkar finns tar inte planeringssystemet med kopplad tillgång eller lager i balanseringen. Det är upp till användaren att utvärdera om den länkade tillgången ska används för att täcka annan eller ny efterfrågan, och i så fall ta bort leveransordern eller reservera den länkade tillgången manuellt.  

Reservationer och orderspårninglänkar bryts om en situation blir omöjlig, till exempel att efterfrågan till ett datum tidigare än leveransen. Order-till-order-länken anpassas till eventuella ändringar i efterfrågan eller tillgång och därmed bryts länken aldrig.  

## <a name="reservations"></a>Reservationer  
Planeringssystemet tar inte med några reserverade antal i beräkningen. Till exempel om en försäljningsorder har avslutats helt eller delvis mot reserverat antal i lager, kan det reserverade antalet i lagret inte användas för att täcka annan efterfrågan. Planeringssystemet tar inte med denna uppsättning med efterfrågan-tillgång i beräkningen.  

Planeringssystemet inkluderar fortfarande reserverat antal i den planerade lagerprofilen, eftersom alla kvantiteter måste beaktas både när du fastställer när beställningspunkten har passerats, och hur många som ska beställas för att uppnå och inte överskrida den maximala lagernivån. Därför leder onödiga reservationer till ökade risk för att lagernivåerna bli låga, eftersom planeringslogiken inte identifierar reserverat antal.  

Följande illustration visar hur reservationer kan förhindra den mest genomförbara planen.  

![Planera med reservationer](media/NAV_APP_supply_planning_1_reservations.png "Planera med reservationer")  

För mer information, se [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)  

## <a name="warnings"></a>Varningar  
Den första kolumnen i planeringsförslaget är avsedd för varningsfälten. I det här fältet kommer alla planeringsrader som skapats för en ovanlig situation att ha en varningsikon, som användaren kan klicka på för att få mer information.  

Tillgången på planeringsrader med varningar ändras normalt inte enligt planeringsparametrarna. I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet. Systemet kan dock konfigurerar för att följa vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar. Mer information finns i beskrivningen av alternativen för batch-jobbet **Skapa inköpsförslag - Planeringsförslag** respektive batchjobbet **Inköpskalkylarket Skapa inköpsförslag - inköpskalkylark** .  

Varningsinformationen visas på sidan **Ej spårade planeringselement** som är också användas för att visa orderspårningslänkar till icke orderrelaterade nätverkstyper. Följande typer av varningar förekommer:  

-   Nödsituation  
-   Undantag  
-   Observera!  

![Varningar i planeringsförslaget](media/NAV_APP_supply_planning_1_warnings.png "Varningar i planeringsförslaget")  

### <a name="emergency"></a>Nödsituation  
Varningen för nödsituation visas i två olika situationer:  

-   När lagret är negativt på startdatumet för planeringen.  
-   När det finns antedaterade försörjnings- eller behovshändelser.  

Om lagernivån för en artikel är negativ på startdatumet för planeringen föreslår systemet en nödleverans för det negativa antalet med leverans på startdatumet för planeringen. I varningstexten anges startdatumet och antalet i nödordern. Mer information finns i [Hantera planerat negativt lager](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Eventuella dokumentrader med förfallodatum före startdatumet för planeringen konsolideras i en nödleveransorder för artikeln med leverans på startdatumet för planeringen.  

### <a name="exception"></a>Undantag  
Undantagsvarningen visas om det planerade disponibla lagret sjunker under nivån för säkerhetslagret. Planeringssystemet föreslår en leveransorder för att uppfylla behovet på förfallodatumet. I varningstexten framgår vilket antal som gäller för artikelns säkerhetslager och det datum då det understigs.  

Att bryta säkerhetslagrets nivå betraktas som ett undantag eftersom det inte bör inträffa om beställningspunkten har ställts in korrekt. Mer information finns i [Ombeställningspunktens roll](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

I allmänhet garanterar exceptionella orderförslag att planerat tillgängligt lager aldrig är lägre än säkerhetslagernivån. Detta innebär dock att det föreslagna antalet bara täcker säkerhetslager, utan att överväga planeringsparametrarna. Dock i alla scenarier ska orderändringsfält övervägas.  

> [!NOTE]  
>  Planeringssystemet kan ha förbrukats säkerhetslagret med avsikt och fyller sedan omedelbart på det. Mer information finns i [Säkerhetslager kan förbrukas](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Observera!  
Den här varningen visas i tre olika situationer:  

-   Startdatumet för planeringen ligger tidigare än arbetsdatumet.  
-   Planeringsraden föreslår att en släppt inköps- eller produktionsorder ändras.  
-   Det planerade lagret överstiger överflödesnivån på förfallodatumet. Mer information finns i [Hålla sig under överflödesnivån](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  Vid planering av rader med varningar är fältet **Acceptera åtgärdsmeddelande** inte markerat, eftersom planeraren förväntas att undersöka dessa rader innan planen utförs.  

## <a name="error-logs"></a>Felloggar  
På sidan Skapa inköpsförslag kan användaren välja fältet **Stoppa och visa första felet** för att planeringskörningen ska stanna när den träffar på det första felet. På samma gång visas ett meddelande med information om felet. Om det finns ett fel, kommer endast de planeringsrader som skapades innan felet påträffades att visas i planeringsförslaget.  

Om fältet inte har markerats kommer batchjobbet Skapa inköpsförslag att fortsätta tills det har slutförts. Fel kommer inte att avbryta batch-jobbet. Om det finns fler än ett fel, visas ett meddelande efter slutförandet som meddelar hur många artiklar som påverkas av fel. Sidan **Logg över planeringsfel** öppnas därefter för att visa mer information om felet och ange länkar till de dokument eller artikelkort som påverkas.  

![Felmeddelanden i planeringsförslaget](media/NAV_APP_supply_planning_1_error_log.png "Felmeddelanden i planeringsförslaget")  

## <a name="planning-flexibility"></a>Planeringsflexibilitet  
Det är inte alltid praktiskt att planera en befintlig leveransorder, till exempel när produktionen har inletts eller extra personer anställs på en viss dag för att utföra jobbet. Om du vill ange om en befintlig beställning kan ändras av planeringssystemet har alla leveransorderrader fältet Planeringsflexibilitet med två alternativ: Obegränsat och Ingen. Om fältet har värdet Ingen kommer planeringssystemet inte försöka ändra leveransorderraden.  

Fältet kan ställas in manuellt av användaren, men i vissa fall ställs det in automatiskt. Det faktum att planeringsflexibilitet kan ställas in manuellt av användaren är viktigt, eftersom det gör det lätt att anpassa förbrukningen av funktionen till olika arbetsflöden och affärsfall.  

Mer information om hur detta fält används finns i [Designdetaljer: Planerade överföringar](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Orderplanering  
Det grundläggande leveransplaneringsverktyget som representeras av sidan **Orderplanering** har utformats för manuellt beslutsfattande. Den beaktar inte några planeringsparametrar och diskuteras därför inte vidare i det här dokumentet. Se hjälpen i [!INCLUDE[d365fin](includes/d365fin_md.md)] för mer information om funktionen Orderplanering.  

> [!NOTE]  
>  Orderplanering bör inte användas om företaget redan använder planering eller inköpskalkylark. Leveransorder som skapas från sidan **Orderplanering** kan ändras eller tas bort under den automatiska planeringskörningen. Detta beror på att den automatiska planeringskörningen använder planeringsparametrarna och dessa kanske inte beaktas av användaren som skapade den manuella planen på sidan Orderplanering.  

##  <a name="finite-loading"></a>Bestämd beläggning  
[!INCLUDE[d365fin](includes/d365fin_md.md)] är ett ERP-system av standardtyp, inget avsändningssystem eller kontrollsystem för butiksgolv. Den planerar för ett möjligt utnyttjande av resurser genom att ange grovt schema, men det skapar och underhåller inte automatiskt detaljerade scheman som baseras på prioriteter eller optimeringsregler.  

Det påtänkta användningen av funktionen Kap.begränsning för resurs är 1): om du vill undvika överbelastning av specifika resurser och 2): om du vill säkerställa att ingen kapacitet blir ej fördelad om den kan öka produktionstiden för en produktionsorder. Funktionen har inga anläggningar eller alternativ om du vill prioritera eller optimera operationer, vilket man kan förvänta sig i ett avsändningssystem. Det kan ge en grov uppskattning av kapaciteten som är praktisk för att identifiera flaskhalsar och undvika att överlasta resurser.  

När du ska planera med kapacitetsbegränsade resurser ser systemet till att ingen resurs beläggs över sin definierade kapacitet (kritisk beläggning). Det ske genom att tilldela varje operation till den närmaste tillgängliga tidsluckan. Om tidsluckan inte är tillräckligt stor för att slutföra hela åtgärden kommer åtgärden att uppdelas i två eller flera delar som placeras i de närmaste tidsluckorna.  

> [!NOTE]  
>  I händelse av åtgärdsdelning tilldelas inställningstiden bara en gång, eftersom det antas att vissa manuella justeringen sker för att optimera schemat.  

Dämpartid kan läggas till i resurser för att minimera åtgärdsdelning. Det gör att systemet kan schemalägga laddning till den sista möjliga dagen genom att överskrida den kritiska beläggningsprocenten något om det kan minska antalet operationer som delas.  

Detta slutför översikten över centrala koncept för leveransplanering i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Följande avsnitt utforskar dessa begrepp närmare och placerar dem i kontexten av kärnplaneringsprocedurerna, balansering av efterfrågan och tillgång samt hanteringen av partiformningsmetoder.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Överföringar i planering](design-details-transfers-in-planning.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)
