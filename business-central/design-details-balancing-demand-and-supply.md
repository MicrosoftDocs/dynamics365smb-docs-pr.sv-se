---
title: Designdetaljer – Balansera efterfrågan och tillgång
description: I den här artikeln beskrivs hur du prioriterar mål genom att balansera efterfrågan och tillgång.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand" />Designdetaljer: Balansera efterfrågan och tillgång

För att förstå hur planeringssystemet fungerar är det viktigt att du förstår att det är prioriterade mål:  

* Alla behov uppfylls av tillräcklig tillgång.  
* All tillgång har ett syfte.  

Allmänt kan dessa mål uppnås genom att balansera tillgång med efterfrågan.  

## <a name="supply-and-demand" />Tillgång och efterfrågan

Begreppet *leverans* avser alla typer av positiv eller ankommande kvantitet, till exempel:

* Lager
* Inköp
* Montering
* Produktion
* Ankommande överföringar
* Försäljningsreturer  

Termen *efterfrågan* avser alla typer av bruttoefterfrågan, t.ex.:

* En artikel för en försäljningsorder
* En komponent för en produktionsorder

[!INCLUDE [prod_short](includes/prod_short.md)]låter dig använda mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer.

För att sortera källorna till tillgång och efterfrågan ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler. En profil är för efterfråganshändelser och den är för motsvarande tillgångshändelser. Varje tillgångshändelse representerar en enhet på en order, till exempel:

* En försäljningsorderrad
* En artikeltransaktion
* En produktionsorderrad

När lagerprofiler laddas balanseras uppsättningarna med efterfrågan-tillgång för att skapa ut en tillförselplan som uppfyller de angivna målen.

Lagernivåer och planeringsparametrar är andra typer av tillgång och efterfrågan. Dessa typer genomgår integrerad motkontering för att fylla på lagerartiklar. Läs mer på [Designdetaljer: Hanterapartiformningsmetoder](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief" />Begreppet motkonto i korthet

Efterfrågan kommer från kunderna. Tillgång är det som du kan skapa och ta bort för att fastställa saldo. Planeringssystemet börjar med efterfrågan och spårar sedan tillbaka till tillgången.  

Lagerprofilerna innehåller information om efterfrågan och tillgång, antal och tidsplan. Dessa profiler utgör de två sidorna av den balanserande skalan.  

Syftet med planering är att balansera tillgång och efterfrågan för en artikel för att se till att tillgång matchar efterfrågan som definieras av planläggningsparametrar och regler.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Översikt över balansering av tillgång och efterfrågan.":::

## <a name="process-orders-before-the-planning-start-date" />Hantera order före planeringsstartdatumet

För att undvika att en leveransplan visar orimliga förslag, kommer planeringssystemet inte att planera något under perioden före planeringsstartdatumet. Följande regel gäller för den perioden:

* All efterfrågan och tillgång före startdatumet för planeringsperioden anses vara en del av lagret eller levererat.  

Med ett par undantag kommer planeringssystemet inte att föreslå några ändringar av leveransorder i den perioden och inte skapa några orderspårninglänkar för den perioden. Undantagen till denna regel är enligt följande:  

* Lagret som planeras vara tillgängligt, inklusive summan av efterfrågan och tillgång i den perioden, är under noll.  
* Bakåtdaterade beställningar kräver serie- eller partinummer.  
* Uppsättningen tillgång-efterfrågan är kopplad av en order-till-order-princip. 

Om det ursprungliga tillgängliga lagret är lägre än noll föreslår planeringssystemet en nödleveransorder leveransorder på dagen före planeringsperioden för att täcka det antal som saknas. Därför kommer det planerade och tillgängliga lagret alltid att vara minst noll när planeringen för den framtida perioden börjar. Planeringsraden för leveransordern ska innehålla en nödvarningsikon och ge ytterligare information.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period" />Serie- och partinummer och order-till-order-länkar är undantagna från föregående period

Om serie- eller partinummer krävs eller om det finns en order-till-order-länk ignoreras regeln om föregående period. Det omfattar bakåtdaterade kvantiteter från startdatumet och kan föreslå korrigerande åtgärder om tillgång och efterfrågan inte synkroniseras. Dessa uppsättningar med efterfrågan-tillgång måste stämma överens för att säkerställa att en viss efterfrågan uppfylls.

## <a name="load-inventory-profiles" />Läsa in lagerprofiler

För att sortera källorna till tillgång och efterfrågan ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.  

Tillgång och efterfrågan med förfallodatum på eller efter planeringsstartdatumet laddas i varje lagerprofil. När typerna med tillgång och efterfrågan är inlästa sorteras de enligt övergripande prioriteter, t.ex.:

* Förfallodatum
* Lägsta-nivå-koder
* Lagerställe
* Variant

Orderprioriteter tillämpas de olika typerna för att uppfylla den viktigaste efterfrågan först. Lär dig mer på [Prioritera order](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Efterfrågan kan också vara negativ. Behandla negativ efterfrågan som tillgång. Till skillnad från vanlig tillgång anses negativ efterfrågan vara fast tillgång. Planeringssystemet tar hänsyn till det, men föreslår inga ändringar.  

I allmänhet betraktar planeringssystemet alla leveransorder efter planeringsstartdatumet som möjliga att ändra för att uppfylla behov. Men så snart en kvantitet bokförs från en leveransorder kan den inte längre ändras av planeringssystemet. Det går inte att planera följande order på nytt:  

* Släppta produktionsorder där förbrukning eller utflöde har bokförts.  
* Monteringsorder där förbrukning eller utflöde har bokförts.  
* Överföring order där utleveransen har bokförts.  
* Inköpsorder där inleverans har bokförts.  

Förutom att ladda typerna med tillgång och efterfrågan, laddas vissa typer med hänsyn till speciella regler och beroenden. I följande avsnitt beskrivs dessa regler och beroenden.  

### <a name="item-dimensions-are-separated" />Artikeldimensioner är separerade

Leveransplanen måste beräknas per kombination av artikeldimensioner, till exempel variant och lagerställe. Endast de kombinationer med ett efterfrågan och/eller tillgång måste beräknas.  

I planeringssystemet sker en sökning efter kombinationer i lagerprofilen. När den hittar en ny kombination, skapas en internkontrollpost som innehåller den faktiska informationen om kombinationen. Planeringssystemet infogar lagerställeenheten som kontrollposten eller yttre loop. Det medför att planeringsparametrar anges enligt en kombination av variant och lagerställe och systemet kan fortsätta till den interna loopen. 

> [!NOTE]  
> Du måste inte ange en lagerställeenhetspost när du anger efterfrågan och/eller tillgång för en viss kombination av variant och lagerställe. Om en lagerställeenhet inte finns för en viss kombination skapar [!INCLUDE [prod_short](includes/prod_short.md)] sin egna tillfälliga lagerställeenhetspost som baseras på data från artikeln. Om växlingsknappen **Lagerställe ska finnas** aktiveras för **sidan Lagerinställningar** måste du antingen skapa en lagerställeenhet eller aktivera växlingsknappen **Komponenter vid lagerställe**. Läs mer på [Planera med och utan lagerställen](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level" />Serie- och partinummer läses in efter specifikationsnivå

Serie- och partinummer läses in i lagerprofilerna tillsammans med tillgång och efterfrågan som de har tilldelats.  

Tillgångs- och efterfrågansattribut ordnas i prioritetsordning samt efter specifikationsnivå. Eftersom matchningar av serie- och partinummer återspeglar specifikationsnivån, kommer en mer specifik efterfrågan att matchas före en mindre specifik efterfrågan. En viss efterfrågan kan till exempel vara ett partinummer som har angetts för en försäljningsrad. En mindre specifik efterfrågan kan vara en försäljning från ett partinummer.

> [!NOTE]  
> Den enda dedikerade prioriteringreglen för serie- och partinumrerad tillgång och efterfrågan är nivån av specifikation som definieras av deras kombinationer och hur artikelspårningsinställningen ställs in för artiklarna.  

Under balanseringen avser planeringssystemet tillgångar som har serie- och partinummer som oböjliga. Systemet ökar eller omplanerar inte sådana leveransorder. Ett undantag är om de används i en order till order-relation. Läs mer på [Order-till-order-länkar bryts aldrig](#order-to-order-links-are-never-broken). Detta undantag skyddar tillgången från att ta emot flera, eventuellt motsägande, åtgärdsmeddelanden när den har varierande attribut. Olika attribut kan t.ex. vara när efterfrågan har en samling olika serienummer.  

En annan orsak till varför serie- och partipartinumrerad efterfrågan är oböjlig beror på att serie- och partinummer ofta tilldelas sent i processen. Det kan vara förvirrande om ändringarna föreslås vid den punkten.  

Balansering av serie- och partinummer respekterar inte regeln om att inte planera någonting före planeringens startdatum. Om tillgång och efterfrågan inte är synkroniserade föreslår planeringssystemet ändringar eller förslår nya order oberoende av startdatumet för planeringen.  

### <a name="order-to-order-links-are-never-broken" />Order-till-order-länkar bryts aldrig

När du planerar en order-till-order-artikel får den länkade tillgången endast användas för vad den ursprungligen ämnades för. Den länkade efterfrågan ska inte täckas av någon annan tillgång, även om tillgången är tillgänglig vad gäller tid och antal. Exempelvis kan du inte använda en monteringsorder som är kopplad till en försäljningsorder i ett scenario för montering mot kundorder för att täcka annan efterfrågan.  

Order-till-order-tillgång och efterfrågan måste balanseras korrekt. Planeringssystemet säkerställer tillgången utan att överväga storleksparametrar för ordern, modifierare och antal i lager (annat än antal som är knutna till länkade order). Av samma anledning föreslår systemet en minskning överskjutande tillgångar om den länkade efterfrågan minskas.  

Denna motkontering påverkar också tidsplanen. Den begränsade horisonten som anges som tidsenheten beaktas inte; tillgången omplaneras om tidsplaneringen för efterfrågan har ändrats. Emellertid respekteras dämpartiden och förhindrar tillgång på orderbasis från att schemaläggas, förutom den interna tillgången i en flernivå-produktionsorder (projektorder).  

> [!NOTE]  
> Serie- och partinummer kan också anges på order-till-order-efterfrågan. I så fall betraktas inte tillgången som oböjlig, vilket vanligtvis är fallet för serienummer och partinummer. I det här fallet ökar eller minskar systemet enligt ändringarna i efterfrågan. Om en efterfrågan har varierande serie- och partinummer, till exempel mer än ett partinummer, föreslås en leveransorder per parti.  

> [!NOTE]  
> Prognoser ska inte leda till att skapa leveransorder som är bundna av en order-till-order-länk. Om prognosen används den bör endast användas som för att skapa av härledd efterfrågan i en produktionsmiljö.

### <a name="component-need-is-loaded-according-to-production-order-changes" />Komponentbehov läses in enligt produktionsorderändringar

När du arbetar med produktionsorder måste planeringssystemet övervaka de nödvändiga komponenterna innan du laddar dem i begäranprofilen. Komponentrader som skapas från en ändrad produktionsorder ersätter rader från den ursprungliga beställningen. Ändringen säkerställer att planeringssystemet inte duplicerar planeringsrader för ett komponentbehov.  

### <a name="consume-safety-stock" />Förbruka säkerhetslager

Antalet i säkerhetslager är en efterfrågan och laddas i lagerprofilen på planeringsstartdatumet.  

Säkerhetslager är en lagerkvantitet som läggs undan för att uppfylla osäkerheter i efterfrågan under påfyllning. Men den kan förbrukas för att uppfylla en efterfrågan. I så fall säkerställer planeringssystemet att säkerhetslagret ersätts snabbt. Systemet föreslår en leveransorder för att fylla på säkerhetslagret på det datum som det förbrukas. Planeringsraden visar en ikon för en undantagsvarning som indikerar att säkerhetslagret delvis eller helt förbrukats och måste fyllas på genom en undantagsorder för det saknade antalet.  

### <a name="forecast-demand-is-reduced-by-sales-orders" />Prognostiserad efterfrågan minskas av försäljningsorder

Efterfrågeprognosen uttrycker förutsedd framtida efterfrågan. Medan den faktiska efterfrågan anges, vanligtvis som försäljningsorder för producerade artiklar, förbrukar den prognosen.

Själva prognosen minskas inte av försäljningsorder Dock minskas prognosantalet som används i planeringsberäkningen (efter försäljningsorderantalet) innan det återstående antalet, om det finns något, anges i profilen för efterfrågan. För försäljning under en period inkluderar planeringen både öppna försäljningsorder och artikeltransaktioner från den levererade försäljningen. Undantaget från regeln är när de kommer från en avropsorder.  

Du måste definiera en giltig prognosperiod. Datumet på det prognostiserade antalet anger startdatum för perioden, och datumet på nästa prognos definierar sedan slutet av perioden.  

Prognosen för perioder före planeringsperioden används inte, oavsett om den förbrukades. Den första prognossiffran av intresse är antingen planeringsstartdatumet eller det närmaste datumet till det.  

Prognosen kan vara för olika typer av efterfrågan:

* Oberoende efterfrågan, till exempel försäljningsorder
* Härledd efterfrågan, till exempel produktionsorderkomponenter.

En artikel kan ha båda typerna av prognos. Under planeringen sker förbrukningen separat, först för härledd efterfrågan och sedan för icke härledd efterfrågan.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders" />Avropsorderbegäran minskas med försäljningsorder

Prognostisering kompletteras av avropsorder för försäljning som ett sätt att ange framtida efterfrågan från en specifik kund. Som med den (ospecificerade) prognosen bör de faktiska försäljningarna förbruka den förutsedda efterfrågan, och det återstående antalet ska ingå i lagerprofilen för efterfrågan. Förbrukningen minskar inte avropsorderantalet.

Planeringsberäkningen inkluderar öppna försäljningsorder länkade till den specifika avropsorderraden, men inte någon giltig tidsperiod. Den inkluderar inte heller den bokförda ordern eftersom bokföringsproceduren redan har reducerat det utestående avropsorderantalet.

## <a name="prioritize-orders" />Prioritera order

Inom ett visst SKU motsvarar det begärda eller tillgängliga datumet den högsta prioriteten. Dagens efterfrågan bör behandlas före nästa veckas efterfrågan. Förutom den övergripande prioriteten, kommer planeringssystemet att göra följande förslag enligt orderprioriteter:

* Vilken typ av efterfrågan du bör uppfylla först.
* Vilken tillgångskälla ska kopplas innan du kopplar andra tillgångskällor.  

Den laddade tillgången och efterfrågan bidrar till en profil för planerade lagret enligt prioriteter.  

### <a name="priorities-on-the-demand-side" />Prioriteter på efterfråganssidan

1. Redan levererat: Artikeltransaktion  
2. Inköpsreturorder  
3. Försäljningsorder  
4. Tjänsteorder  
5. Produktionskomponentbehov  
6. Rad för monteringsorder  
7. utgående överföringsorder  
8. Avropsorder (som inte redan har förbrukats av motsvarande försäljningsorder)  
9. Prognos (som inte redan har förbrukats av andra försäljningsorder)  

> [!NOTE]  
> Köpreturer ingår vanligtvis inte i tillförselplanläggning; de ska alltid reserverats från partiet som ska returneras. Om de inte har reserverats spelar inköpsreturer en roll i dispositionen och är högt prioriterade för att undvika att planeringssystemet föreslår en leveransorder bara för att hantera en inköpsretur.  

### <a name="priorities-on-the-supply-side" />Prioriteter på tillgångssidan

1. Finns redan i lager: Artikeltransaktion (Planeringsflexibilitet = Ingen)  
2. Försäljningsreturorder (planeringsflexibilitet = ingen)  
3. inkommande överföringsorder  
4. Produktionsorder  
5. Monteringsorder  
6. Inköpsorder  

### <a name="priority-related-to-the-state-of-supply-and-demand" />Prioritet kopplad till status för tillgång och efterfrågan

Utöver prioriteterna från typen av tillgång och efterfrågan finns det andra saker som påverkar planeringens flexibilitet. Till exempel lageraktiviteter och status för följande order:

* FÖRS
* Inköp
* Överföring:
* Montering
* Produktion

Status för dessa order har följande effekter: 

1. Hanteras delvis (planeringsflexibilitet = ingen)  
2. Redan pågående i distributionslagret (Planeringsflexibilitet = Ingen)  
3. Släppt – alla ordertyper (Planeringsflexibilitet = Obegränsad)  
4. Fast planerad produktionsorder (Planeringsflexibilitet = Obegränsad)  
5. Planerad/öppen – alla ordertyper (Planeringsflexibilitet = Obegränsad)

## <a name="balancing-supply-with-demand" />Balansera tillgång med efterfrågan

Planeringssystemet balanserar tillgång och efterfrågan genom att föreslå åtgärder för att ändra leveransorder som inte är balanserade. Balanseringen inträffar för varje kombination av variant och lagerställe.  

Anta att de olika lagerprofilerna innehåller två strängar:

* En sträng för efterfrågan, sorterad efter datum och prioritet
* En motsvarande sträng med tillgångshändelser

Varje händelse refererar till sin ursprungstyp och sitt id. Reglerna för balansering av artikeln är rättframma. Matchande tillgång och efterfrågan kan uppstå när som helst under processen:  

1. Ingen efterfrågan eller försörjning finns för artikel =>planläggningen har slutförts (eller ska inte starta).  
2. Efterfrågan finns, men det finns inte någon tillgång =>tillgång bör föreslås.  
3. Tillgång finns, men det finns inte efterfrågan på den => tillgång bör annulleras.  
4. Både efterfrågan och tillgång finns => frågor ska ställas och besvaras innan [!INCLUDE [prod_short](includes/prod_short.md)] kan se till att tillgången kan uppfylla efterfrågan.

    Om tidpunkten för av leveransen inte passar, kanske leveransen kan omplaneras enligt följande:  

    1. Om tillgången placeras tidigare än efterfrågan kan kanske tillgången planeras så att lagret är så lågt som möjligt.  
    2. Leverans placeras före efterfrågan, kan kanske leverans framåtplaneras. Annars kommer systemet att föreslå ny tillgång.  
    3. Om tillgången uppfyller efterfrågan på datumet kan planeringssystemet undersöka om tillgångens antal kan täcka efterfrågan.  

    När tidsplanen är på plats kan det antalet som ska levereras beräknas enligt följande:  

    1. Om tillgångsantalet är mindre än efterfrågan kan tillgångsantalet ökas (eller inte om du har en princip om maximalt antal).  
    2. Om tillgångsantalet är större än efterfrågan kan tillgångsantalet minskas (eller inte om du har en princip om minsta antal).  

    I det här skedet finns ett av följande situationer:  

    1. Den aktuella efterfrågan kan täckas, i vilket fall den kan stängas och planeringen för nästa efterfrågan kan starta.  
    2. Tillgången har nått sitt maximum, och en del av efterfråganskvantiteten täcks inte. I det här fallet kan planeringssystemet stänga den aktuella tillgången och gå vidare till nästa.  

 Du startar om med nästa efterfrågan och den aktuella tillgången eller vice versa. Den aktuella tillgången kan kanske täcka även nästa efterfrågan, eller den aktuella efterfrågan inte ännu inte har täckts helt.  

### <a name="rules-for-actions-for-supply-events" />Regler om åtgärder för tillgångshändelser

För beräkningar uppifrån och ned där tillgång måste uppfylla efterfrågan, tas efterfrågan för given. Det ligger utanför planeringssystemets kontroll. Däremot kan planeringssystemet hantera försörjningssidan och göra följande förslag:

* Skapa nya leveransorder
* Tidsplanera om befintliga order eller ändra deras antal
* Annullera leveransorder som inte längre behövs  

För att exkludera en befintlig leveransorder från planeringsförslagen, kan han ange att den inte har någon planeringsflexibilitet (Planeringsflexibilitet = Ingen). Överskjutande tillgång för ordern används för att täcka efterfrågan, men ingen åtgärd föreslås. 

I allmänhet har totala tillgång en planeringsflexibilitet som begränsas av villkoren för var och en av de föreslagna åtgärderna.  

* **Omplanera ut**: Datumet på en befintlig leveransorder kan omplaneras ut för att uppfylla efterfrågans förfallodatum om inte:

  * Det representerar lager (alltid på dag noll).  
  * Den har en order-till-order som är kopplad till en annan efterfrågan.  
  * Det finns utanför fönstret för omplanering i tidsenheten.
  * Det finns en närmare tillgång som kan användas.  
  * Å andra sidan kan användaren bestämma att inte ändra tidpunkten eftersom:
  * Leveransordern har kopplats till en annan efterfrågan på ett tidigare datum.  
  * Den nödvändiga omplaneringen är så minimal att den är försumbar.  

* **Omplanera in**: Datumet på en befintlig leveransorder kan omplaneras in, utom i följande villkor:

  * Det är direkt kopplat till viss övrig efterfrågan.  
  * Det finns utanför fönstret för omplanering som definieras av tidsenheten.

> [!NOTE]  
> När du planerar en artikel med hjälp av en beställningspunkt, kan leveransorder alltid planeras om Det är vanligt i framåtplanerade leveransorder som aktiveras av en beställningspunkt.

* **Öka antalet**: Antalet på en befintlig leveransorder kan ökas för att uppfylla efterfrågan, såvida inte leveransordern är kopplad direkt till en efterfrågan av order-till-order-koppling.  

> [!NOTE]  
> Även om du kan öka leveransorder, kan ökningen begränsas på grund av en definierad maximal partistorlek.  

* **Minska antalet**: En befintlig leveransorder med ett överskott som jämförs med en befintlig efterfrågan kan minskas för att uppfylla efterfrågan.  

> [!NOTE]  
> Även om antalet kan minskas kan det fortfarande finns ett överskott jämfört med efterfrågan på grund av en definierad lägsta partistorlek eller flera order. 

* **Annullera**: Som ett specialfall av åtgärden minska antal kan leveransordern annulleras om den har minskats till noll. 
* **Ny**: Om ingen leveransorder finns, eller en befintlig inte kan ändras så att den uppfyller kvantiteten som krävs på förfallodatumet, föreslås en ny leveransorder.  

### <a name="determine-the-supply-quantity" />Fastställa tillgångsantalet

Du definierar planeringsparametrar som styr det föreslagna antalet för varje leveransorder.  

När planeringssystemet beräknar antalet på en ny leveransorder eller antalsändringen på en befintlig order kan det föreslagna antalet skilja sig från den faktiska efterfrågan.  

Om ett maximalt lager eller fasta partistorlekar väljs kan det föreslagna antalet ökas för att uppfylla det fasta antalet eller det maximal lagret. Om en partiformningsmetod använder en beställningspunkt kan antalet ökas minst för att uppfylla beställningspunkten. 

Det föreslagna antalet kan ändras i den här sekvensen:  

1. Ned till den maximala partistorleken.  
2. Upp till minsta partistorlek  
3. Upp till den närmaste ordermultipeln.

### <a name="order-tracking-links-during-planning" />Orderspårninglänkar under planering

För orderspårning under planering ordnar planeringssystemet om orderspårninglänkarna för kombinationerna av artiklar, varianter och lagerställen. Systemet ordnar om spårningslänkarna av följande anledningar:

* För att kontrollera om det finns förslag som täcker all efterfrågan och se till att alla leveransorder behövs.  
* Orderspårningslänkarna måste balanseras om regelbundet.  

Över tid blir orderspårningslänkar obalanserade. Länkarna blir obalanserade eftersom orderspårningsnätverket inte struktureras om förrän en efterfrågans- eller tillgångshändelse faktiskt stängs.

Innan tillgången balanseras efter efterfrågan tar planeringssystemet bort alla orderspårningslänkar. Under balanseringsprocessen, när en efterfrågans- eller en tillgångshändelse stängs skapas nya orderspårninglänkar mellan tillgång och efterfrågan.  

> [!NOTE]  
> Även om artikeln inte ställts in för dynamisk orderspårning skapar planeringssystemet balanserade orderspårningslänkar.

## <a name="close-balanced-supply-and-demand" />Stäng balanserad tillgång och efterfrågan

Balanserad tillgång har tre möjliga resultat:

* Det begärda antalet och datumet för efterfråganshändelserna uppfylls och planeringen för dem kan stängas. Tillgångshändelsen förblir öppen och kan täcka nästa efterfrågan. Genom att hålla tillgångshändelsen öppen kan balanseringsprocessen börja om med tillgångshändelse och nästa efterfrågan.  
* Leveransordern kan inte ändras för att täcka all efterfrågan. Efterfråganshändelsen är fortfarande öppen, med visst antal som inte täckts men som kan täckas av nästa tillgångshändelse. På så sätt stängs den aktuella händelsen för efterfrågan, så att motkonteringen kan börja om igen med aktuell efterfrågan och nästa tillgångshändelse.  
* All efterfrågan har täckts och det finns inte någon efterföljande efterfrågan (eller det fanns ingen efterfrågan alls). Överskottstillgång kan minskas (eller annulleras) och sedan stängas. Andra tillgångshändelser bör också avbrytas.  

Till sist skapar planeringssystemet en orderspårninglänk mellan tillgång och efterfrågan.  

### <a name="create-the-planning-line-suggested-action" />Skapa planeringsraden (föreslagen åtgärd)

Om åtgärden **Nytt**, **Ändra antal**, **Omplanera**, **Omplanera och ändra antal** eller **Avbryt** föreslås för att granska leveransordern, planeringssystemet skapar en planeringsrad i planeringsförslaget. För orderspårning skapas planeringsraden inte bara när leveranshändelsen är stängd, utan även om efterfrågehändelsen är stängd. Detta gäller även om leveranshändelsen fortfarande är öppen och kan ändras när nästa efterfrågehändelse bearbetas. Planeringsraden kan ändras igen när den skapas.

Om du vill minska belastningen på databasen när du hanterar produktionsorder kan du underhålla planeringsraden på tre nivåer:

* Skapa endast planeringsraden med det aktuella förfallodatumet och antalet men utan verksamhetsföljden och komponenterna.  
* Inkludera verksamhetsföljd: den planerade verksamhetsföljden inkluderar beräkning av start- och slutdatum och tidpunkter. Inkludera verksamhetsföljd är fordrande i termer av databasåtkomster. För att fastställa slut- och förfallodatum kan det vara nödvändigt att beräkna verksamhetsföljden även om tillförselhändelsen inte har stängts. Om du till exempel utför planeringen framåt.  
* Ta med strukturexpansion: kan ske precis före tillgångshändelsen är avslutad.

## <a name="see-also" />Se även

[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
