---
title: Designdetaljer - Balansera tillgång med efterfrågan | Microsoft Docs
description: För att förstå hur planeringssystemet fungerar är det nödvändigt att förstå de prioriterade målen för planeringssystemet. Viktigast av allt är att se till att alla behov ska uppfyllas av tillräcklig försörjning och leverans har en funktion för att förstå hur planeringssystemet fungerar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a1e55d983abae5f85807039da6dd4d846c3e40b3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185714"
---
# <a name="design-details-balancing-demand-and-supply"></a>Designdetaljer: Balansera efterfrågan och tillgång
För att förstå hur planeringssystemet fungerar är det nödvändigt att förstå de prioriterade målen för planeringssystemet. Viktigast av allt är att se till att:  

- Alla behov uppfylls av tillräcklig tillgång.  
- All tillgång har ett syfte.  

 Allmänt kan dessa mål uppnås genom att balansera tillgång med efterfrågan.  

## <a name="demand-and-supply"></a>Tillgång och efterfrågan
 Efterfrågan är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder. Dessutom tillåter programmet mer tekniska typer av efterfrågan, till exempel negativt lagersaldo och inköpsreturer.  

  Tillgång är den term som vanligtvis används för alla typer av positivt eller ankommande antal, t.ex. inköpsöverföringar, monteringsöverföringar, produktionsöverföringar och ankommande överföringar. Dessutom kan en försäljningsretur också representera tillgång.  

  För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler. En profil innehåller efterfråganshändelser och den andra innehåller motsvarande tillgångshändelser. Varje händelse representerar en ordernätverksenhet, till exempel en försäljningsorderrad, en artikeltransaktion eller en produktionsorderrad.  

  När lagerprofiler laddas balanseras de olika uppsättningarna med efterfrågan-tillgång för att skapa ut en tillförselplan som uppfyller de angivna målen.  

  Planeringsparametrar och lagernivåer är andra typer av efterfrågan och tillgång, som genomgår integrerad motkontering för att fylla på lagerartiklar. Mer information finns i [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Begreppet motkonto i korthet
  Efterfrågan anges av ett företags kunder. Tillgång är det som företag kan skapa och ta bort för att fastställa saldo. Planeringssystemet börjar med den icke-härledda efterfrågan och spårar sedan tillbaka till tillgången.  

   Lagerprofilerna används för att innehålla information om efterfrågan och tillgång, antal och tidsplan. Dessa profiler utgör grunden för de två sidorna av den balanserande skalan.  

   Syftet med planläggningsmekanismen är att balansera efterfrågan och tillgång för en artikel för att se till att tillgång matchar efterfrågan på ett genomförbart sätt som definieras av planläggningsparametrar och regler.  

   ![Översikt över balansering av tillgång och efterfrågan](media/nav_app_supply_planning_2_balancing.png "Översikt över balansering av tillgång och efterfrågan")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Hantera order före planeringsstartdatumet
För att förhindra att en tillförselplan visar omöjliga och därför oanvändbara förslag, betraktar planeringssystemet perioden fram till planeringsstartdatumet som en fryst zon som inget planeras för. Följande regel gäller för den frysta zonen:  

All efterfrågan och tillgång före startdatumet för planeringsperioden anses vara en del av lagret eller levererat.  

Planeringssystemet föreslår inte, med ett par undantag, några ändringar av leveransorder i den frysta zonen, och inga orderspårninglänkar skapas eller underhålls för den perioden.  

Undantagen till denna regel är enligt följande:  

   * Om det planerade tillgängliga lagret, inklusive summan av efterfrågan och tillgång i den frysta zonen, är under noll.  
   * Om serie-/partinummer krävs på de bakåtdaterade beställningarna.  
   * Om uppsättningen tillgång-efterfrågan är kopplad av en order-till-order-princip.  

Om det ursprungliga tillgängliga lagret är lägre än noll föreslår planeringssystemet en nödleveransorder leveransorder på dagen före planeringsperioden för att täcka det antal som saknas. Därför kommer det planerade och tillgängliga lagret alltid att vara minst noll när planeringen för den framtida perioden börjar. Planeringsraden för leveransordern ska innehålla en nödvarningsikon och ytterligare information finns i fältet.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serie-/partinummer och Order-till-order-länkar är undantagna från den frysta zonen  
   Om serie-/partinummer krävs eller det finns en order-till-order-länk kommer planeringssystemet att ignorera den frysta zonen och ta med sådana antal som har bakåtdaterats från startdatumet, och föreslår eventuellt korrigerande åtgärder om efterfrågan och tillgång är i obalans. Affärsorsaken till den här principen är att sådana specifika uppsättningar med efterfrågan-tillgång måste matcha för att se till att den aktuella efterfrågan uppfylls.

## <a name="loading-the-inventory-profiles"></a>Läsa in lagerprofiler
För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.  

De normala typerna av efterfrågan och tillgång med förfallodatum på eller efter planeringsstartdatumet laddas i varje lagerprofil. När de laddas sorteras de olika efterfrågan- och tillgångstyperna enligt allmänna prioriteringar, till exempel förfallodatum, lågnivåkoder, lagerställe och variant. Dessutom kopplas orderprioriteter till de olika typerna för att se till att den viktigaste efterfrågan uppfylls först. Mer information finns i [Prioritera order](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Som nämndes tidigare kan efterfrågan kan även vara negativ. Det betyder att den ska hanteras som tillgång, men till skillnad från de vanliga typerna av tillgång anses negativ efterfrågan vara fast tillgång. Planeringssystemet tar hänsyn till det, men föreslår inga ändringar.  

I allmänhet betraktar planeringssystemet alla leveransorder efter planeringsstartdatumet som möjliga att ändra för att uppfylla behov. Men så snart ett antal bokförs från en leveransorder kan den inte längre ändras av planeringssystemet. Följande olika order kan inte planeras om:  

- Släppta produktionsorder där förbrukning eller utflöde har bokförts.  
- Monteringsorder där förbrukning eller utflöde har bokförts.  
- Överföring order där utleveransen har bokförts.  
- Inköpsorder där inleverans har bokförts.  

Förutom att ladda tillgångs- och efterfråganstyper, laddas vissa typer med hänsyn till speciella regler och beroenden som beskrivs i här efter.  

### <a name="item-dimensions-are-separated"></a>Artikeldimensioner är separerade  
Leveransplanen måste beräknas per kombination av artikeldimensioner, till exempel variant och lagerställe. Men det finns ingen anledning att beräkna någon teoretisk kombination. Endast de kombinationer med ett efterfrågans- och/eller tillgångsbehov måste beräknas.  

Planeringssystemet styr detta genom att gå igenom lagerprofilen. När en ny kombination hittas, skapas en internkontrollpost som innehåller den faktiska informationen om kombinationen. Programmet infogar lagerställeenheten som kontrollposten eller yttre loop. Det medför att rätt planeringsparametrar anges enligt en kombination av variant och lagerställe, och programmet kan fortsätta till den interna loopen.  

> [!NOTE]  
>  Programmet kräver inte att användaren ska ange en lagerställeenhetspost när du anger efterfrågan och/eller tillgång för en viss kombination av variant och lagerställe. Om en lagerställeenhet inte finns för en viss kombination skapar programmet därför sin egna tillfälliga lagerställeenhetspost som baseras på artikelkortdata. Om Lagerställe ska finnas har värdet Ja på sidan Lagerinställningar måste antingen lagerställeenhet skapas eller Komponenter vid lagerställe anges till Ja. Mer information finns i [Designdetaljer: Efterfrågan vid tomt lagerställe](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serie-/partinummer läses in efter specifikationsnivå  
Attribut i form av serie-/partinummer laddas in i lagerprofilerna tillsammans med efterfrågan och tillgång som de har kopplats till.  

Tillgångs- och efterfrågansattribut ordnas i prioritetsordning samt efter specifikationsnivå. Eftersom serie-/partinummermatchningar visar nivån av specifikation söker den mer specifika efterfrågan, till exempel ett partinummer som specifikt har valts för en försäljningsrad, efter en matchning före en mindre specifik efterfrågan, till exempel en försäljning från ett valfritt utvalt partinummer.  

> [!NOTE]  
>  Det finns inga tilldelade prioriteringregler för serie-/partinumrerad tillgång och efterfrågan, annat än nivån av specifikation som definieras av deras kombinationer av serie- och partinummer och artikelspårningsinställningen för de inblandade artiklarna.  

Under balanseringen ser planeringssystemet tillgång med serie-/partinummer som oböjligt och försöker inte öka eller ändra tidpunkten för sådana leveransorder (såvida de inte används i samband en relation på orderbasis). Se Order-till-order-länkar bryts aldrig). Det skyddar tillgången från att ta emot flera, eventuellt motsägande, åtgärdsmeddelanden när en leverans har varierande attribut, till exempel en samling med av olika serienummer.  

En annan anledning till att serie-/partinumrerad tillgång är inflexibel är att serie-/partinummer vanligtvis tilldelas så sent i processen att det skulle vara förvirrande om ändringar föreslås.  

Balanseringen av serienummer/partinummer beaktar inte *fryst zon*. Om att efterfrågan och tillgång är inte är synkroniserade föreslår planeringssystemet ändringar eller förslår nya order oberoende av startdatumet för planeringen.  

### <a name="order-to-order-links-are-never-broken"></a>Order-till-order-länkar bryts aldrig  
När du planerar en order-till-order-artikel får den länkade tillgången inte användas för någon annan efterfrågan än vad den ursprungligen ämnades för. Den länkade efterfrågan ska inte täckas av någon annan slumpmässig leverans, även om den för närvarande är tillgänglig vad gäller tid och antal. Exempelvis kan en monteringsorder som är kopplad till en försäljningsorder i ett scenario för montering mot kundorder inte användas för täcka annan efterfrågan.  

Order-till-order-efterfrågan och -tillgång måste balanseras korrekt. Planeringssystemet säkerställer tillgången under alla omständigheter, utan att överväga storleksparametrar för ordern, modifierare och antal i lager (annat än antal som är knutna till länkade order). Av samma anledning föreslår systemet en minskning överskjutande tillgångar om den länkade efterfrågan minskas.  

Denna motkontering påverkar också tidsplanen. Den begränsade horisonten som anges som tidsenheten beaktas inte; tillgången omplaneras om tidsplaneringen för efterfrågan har ändrats. Emellertid respekteras dämpartiden och förhindrar tillgång på orderbasis från att schemaläggas, förutom den interna tillgången i en flernivå-produktionsorder (projektorder).  

> [!NOTE]  
>  Serie-/partinummer kan också anges på order-till-order-efterfrågan. I så fall betraktas inte tillgången som inflexibel som standard, vilket vanligtvis är fallet för serienummer eller partinummer. I det här fallet ökar/minskar systemet enligt ändringarna i efterfrågan. Dessutom är det så att om en efterfrågan har varierande serie-/partinummer, till exempel mer än ett partinummer, föreslås en leveransorder per parti.  

> [!NOTE]  
>  Prognoser ska inte leda till att skapa leveransorder som är bundna av en order-till-order-länk. Om prognosen används den bör endast användas som för att skapa av härledd efterfrågan i en produktionsmiljö.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov läses in enligt produktionsorderändringar  
När du arbetar med produktionsorder måste planeringssystemet övervaka de nödvändiga komponenterna innan du laddar dem i begäranprofilen. Komponentrader som skapas från en ändrad produktionsorder ersätter de från den ursprungliga beställningen. Detta säkerställer att planeringssystemet etablerar att planeringsrader för komponentbehov aldrig kopieras.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Säkerhetslager kan förbrukas  
Antalet i säkerhetslager är primärt en efterfråganstyp och laddas därför i lagerprofilen på planeringsstartdatumet.  

Säkerhetslager är en lagerkvantitet som läggs undan för att kompensera för osäkerheter i efterfrågan under påfyllningledtiden. Den kan förbrukas om det är nödvändigt att ta från den för att uppfylla en efterfrågan. När detta sker kommer planeringssystemet att se till att säkerhetslagret snabbt ersätts genom att föreslå en leveransgsorder för att fylla på säkerhetslagret. Den här planeringsraden visar en ikon för en undantagsvarning som indikerar att säkerhetslagret delvis eller helt förbrukats och måste fyllas på genom en undantagsorder för det saknade antalet.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognostiserad efterfrågan minskas av försäljningsorder  
Efterfrågeprognosen uttrycker förutsedd framtida efterfrågan. Medan den faktiska efterfrågan anges, vanligtvis som försäljningsorder för producerade artiklar, förbrukar den prognosen.  

Själva prognosen minskas inte egentligen av försäljningsorder: den förblir densamma. Dock minskas prognosantalet som används i planeringsberäkningen (efter försäljningsorderantalet) innan det återstående antalet, om det finns något, anges i lagerprofilen för efterfrågan. När planeringssystemet undersöker faktiska försäljningar under en period, ingår både öppna försäljningsorder och artikeltransaktioner från levererade försäljningar, om de inte härrör från en avropsorder.  

En användare måste definiera en giltig prognosperiod. Datumet på det prognostiserade antalet anger startdatum för perioden, och datumet på nästa prognos definierar sedan slutet av perioden.  

Prognosen för perioder före planeringsperioden används inte, oavsett om den förbrukades eller inte. Den första prognossiffran av intresse är antingen datumet på eller det närmaste datumet före planeringsstartdatumet.  

Prognosen kan användas för icke härledd efterfrågan, t.ex. försäljningsorder, eller härledd efterfrågan, t.ex. produktionsorderkomponenter (modul-prognos). En artikel kan ha båda typerna av prognos. Under planeringen sker förbrukningen separat, först för härledd efterfrågan och sedan för icke härledd efterfrågan.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Avropsorderbegäran minskas med försäljningsorder  
Prognostisering kompletteras av avropsorder som ett sätt att ange framtida efterfrågan från en specifik kund. Som med den (ospecificerade) prognosen bör de faktiska försäljningarna förbruka den förutsedda efterfrågan, och det återstående antalet ska ingå i lagerprofilen för efterfrågan. Förbrukningen minskar inte avropsordern.  

Planeringsberäkningen beaktar öppna försäljningsorder länkade till den specifika avropsorderraden, men den beaktar inte någon giltig tidsperiod. Det tar inte heller hänsyn till den bokförda order, eftersom bokföringsproceduren redan har reducerat det utestående avropsorderantalet.

## <a name="prioritizing-orders"></a>Orderprioritera
Inom en given lagerställeenhet representerar det begärda eller tillgängliga datumet den högsta prioriteten. Dagens efterfrågan ska hanteras före nästa veckas efterfrågan. Men utöver den här allmänna prioriteten föreslår planeringssystemet också vilken typ av efterfrågan som ska uppfyllas innan övrig efterfrågan uppfylls. På samma sätt kommer det att föreslå vilken tillgångskälla som ska kopplas innan du kopplar andra tillgångskällor. Det utförs i enlighet med orderprioriteter.  

Den laddade efterfrågan och tillgången bidrar till en profil för planerade lagret enligt följande prioriteter:  

### <a name="priorities-on-the-demand-side"></a>Prioriteter på efterfråganssidan  
1. Redan levererat: Artikeltransaktion  
2. Inköpsreturorder  
3. Reservationstransaktion  
4. Tjänsteorder  
5. Produktionskomponentbehov  
6. Monteringsorderrad  
7. Avgående överföringsorder  
8. Avropsorder (som inte redan har förbrukats av motsvarande försäljningsorder)  
9. Prognos (som inte redan har förbrukats av andra försäljningsorder)  

> [!NOTE]  
>  Köpreturer ingår vanligtvis inte i tillförselplanläggning; de ska alltid reserverats från partiet som ska returneras. Om de inte har reserverats spelar inköpsreturer en roll i dispositionen och är högt prioriterade för att undvika att planeringssystemet föreslår en leveransorder bara för att hantera en inköpsretur.  

### <a name="priorities-on-the-supply-side"></a>Prioriteter på tillgångssidan  
1. Finns redan i lager: Artikeltransaktion (Planeringsflexibilitet = Ingen)  
2. Försäljningsreturorder (planeringsflexibilitet = ingen)  
3. Ankommande överföringsorder  
4. Produktionsorder  
5. Monteringsorder  
6. Inköpsorder  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioritet kopplad till status för efterfrågan och tillgång  
Förutom prioriteter som anges av typen av efterfrågan och tillgång, definierar ordrarnas aktuella status i körningsprocessen också en prioritet. Till exempel har lageraktiviteter en inverkan, och status för försäljningar, köp, överföringar, montering och produktionsorder tas med i beräkningen:  

1. Hanteras delvis (planeringsflexibilitet = ingen)  
2. Redan pågående i distributionslagret (Planeringsflexibilitet = Ingen)  
3. Släppt – alla ordertyper (Planeringsflexibilitet = Obegränsad)  
4. Fast planerad produktionsorder (Planeringsflexibilitet = Obegränsad)  
5. Planerad/öppen – alla ordertyper (Planeringsflexibilitet = Obegränsad)

## <a name="balancing-supply-with-demand"></a>Balansera tillgång med efterfrågan
Kärnan av planeringssystemet inbegriper att hantera tillgång och efterfrågan genom att föreslå användarhandlingar för att revidera leveransorder i händelse av obalans. Det sker per kombination av variant och lagerställe.  

Föreställ dig att varje lagerprofil innehåller en sträng med efterfråganshändelser (sorterade efter datum och prioritet) och en motsvarande sträng med tillgångshändelser. Varje händelse refererar tillbaka till sin ursprungstyp och sitt id. Reglerna för motkontering av artikeln är rättframma. Fyra instanser av matchande efterfrågan och tillgång kan uppstå när som helst under processen:  

1. Ingen efterfrågan eller försörjning finns för artikel =>planläggningen har slutförts (eller ska inte starta).  
2. Efterfrågan finns, men det finns inte någon tillgång =>tillgång bör föreslås.  
3. Tillgång finns, men det finns inte efterfrågan på den => tillgång bör annulleras.  
4. Både efterfrågan och tillgång finns => frågor ska ställas och besvaras innan systemet kan se till att efterfrågan kan uppfyllas och tillgången är tillräcklig.  

    Om tidpunkten för av leveransen inte passar, kanske leveransen kan omplaneras enligt följande:  

    1.  Om tillgången placeras tidigare än efterfrågan kan kanske tillgången planeras om så att lagret är så lågt som möjligt.  
    2.  Leverans placeras före efterfrågan, kan kanske leverans omplaneras. Annars kommer systemet att föreslå ny tillgång.  
    3.  Om tillgången uppfyller efterfrågan på datumet kan planeringssystemet fortsätta att undersöka om tillgångens antal kan täcka efterfrågan.  

    När tidsplanen är på plats kan det adekvata antal som ska levereras beräknas enligt följande:  

    1.  Om tillförselantalet är mindre än efterfrågan är det möjligt att tillförselantalet ska ökas (eller inte, om det begränsas av en princip om maximalt antal).  
    2.  Om tillförselantalet är större än efterfrågan är det möjligt att tillförselantalet kan minskas (eller inte, om det begränsas av en princip om lägsta antal).  

    I det här skedet finns någon av följande två situationer:  

    1.  Den aktuella efterfrågan kan täckas, i vilket fall den kan stängas och planeringen för nästa efterfrågan kan starta.  
    2.  Tillgången har nått sitt maximum, och en del av efterfråganskvantiteten täcks inte. I det här fallet kan planeringssystemet stänga den aktuella tillgången och gå vidare till nästa.  

 Du startar om med nästa efterfrågan och den aktuella tillgången eller vice versa. Den aktuella tillgången kan kanske täcka även nästa efterfrågan, eller den aktuella efterfrågan inte ännu inte har täckts helt.  

### <a name="rules-concerning-actions-for-supply-events"></a>Regler angående åtgärder för tillförselhändelser  
När planeringssystemet utför en beräkning uppifrån och ned där tillgången måste uppfylla efterfrågan tas efterfrågan för given, det vill säga den ligger utanför planeringssystemets kontroll. Men tillgångssidan kan hanteras. Därför får du i planeringssystemet ett förslag om att skapa nya leveransorder, att omplanera befintliga och/eller ändra partistorleken. Om en befintlig leveransorder blir överflödig föreslår planeringssystemet att användaren annullerar den.  

Om användaren vill exkludera en befintlig leveransorder från planeringsförslagen, kan han ange att den inte har någon planeringsflexibilitet (Planeringsflexibilitet = Ingen). Överskjutande tillgång för ordern används för att täcka efterfrågan, men ingen åtgärd föreslås.  

I allmänhet har totala tillgång en planeringsflexibilitet som begränsas av villkoren för var och en av de föreslagna åtgärderna.  

-   **Omplanera ut**: Datumet på en befintlig leveransorder kan omplaneras ut för att uppfylla efterfrågans förfallodatum om inte:  

    -   Det representerar lager (alltid på dag noll).  
    -   Den har en order-till-order som är kopplad till en annan efterfrågan.  
    -   Det ligger utanför omplaneringssidan definierat av tidsenheten.  
    -   Det finns en närmare tillgång som kan användas.  
    -   Å andra sidan kan användaren bestämma att inte ändra tidpunkten eftersom:  
    -   Leveransordern redan har kopplats till en annan efterfrågan på ett tidigare datum.  
    -   Den nödvändiga omplaneringen är så minimal att användaren anser den vara försumbar.  

-   **Omplanera in**: Datumet på en befintlig leveransorder kan omplaneras in, utom i följande villkor:  

    -   Det är direkt kopplat till vissa övriga behov  
    -   Det ligger utanför omplaneringssidan definierat av tidsenheten.  

> [!NOTE]  
>  När du planerar en artikel med hjälp av en beställningspunkt, kan leveransorder alltid planeras in om det behövs. Det är vanligt i framåtplanerade leveransorder som aktiveras av en beställningspunkt.  

-   **Öka antalet**: Antalet på en befintlig leveransorder kan ökas för att uppfylla efterfrågan, såvida inte leveransordern är kopplad direkt till en efterfrågan av order-till-order-koppling.  

> [!NOTE]  
>  Även om det är möjligt att öka leveransorder, kan den begränsas på grund av en definierad maximal partistorlek.  

-   **Minska antalet**: En befintlig leveransorder med ett överskott som jämförs med en befintlig efterfrågan kan minskas för att uppfylla efterfrågan.  

> [!NOTE]  
>  Även om antalet kan minskas kan det fortfarande finns ett överskott jämfört med efterfrågan på grund av en definierad lägsta partistorlek eller flera order.  

-   **Annullera**: Som ett specialfall av åtgärden minska antal kan leveransordern annulleras om den har minskats till noll.  
-   **Ny**: Om ingen leveransorder redan finns, eller en befintlig inte kan ändras så att den uppfyller behovskvantiteten på det efterfrågade förfallodatumet, föreslås en ny leveransorder.  

### <a name="determining-the-supply-quantity"></a>Fastställa tillgångsantalet  
Planeringsparametrar som definieras av användaren styr det föreslagna antalet för varje leveransorder.  

När planeringssystemet beräknar antalet på en ny leveransorder eller antalsändringen på en befintlig leveransorder kan det föreslagna antalet skilja sig från det som faktiskt begärdes.  

Om ett maximalt lager eller en fast orderkvantitet väljs kan det föreslagna antalet ökas för att uppfylla det fasta antalet eller det maximal lagret. Om en partiformningsmetod använder en beställningspunkt kan antalet ökas minst för att uppfylla beställningspunkten.  

 Det föreslagna antalet kan ändras i den här sekvensen:  

1. Ned till den maximala partistorleken (om en sådan finns).  
2. Upp till minsta partistorlek  
3. Upp till den närmaste ordermultipeln. (I händelse av felaktiga inställningar kan detta överträda maximal partistorlek).  

### <a name="order-tracking-links-during-planning"></a>Orderspårninglänkar under planering  
Angående orderspårning under planering är det viktigt att nämna att planeringssystemet ordnar om de dynamiskt skapade orderspårninglänkarna för kombinationerna av artikel/variant/lagerställe.  

Det finns två orsaker till detta:  

-   Planeringssystemet måste kunna motivera sina förslag: att alla behov har täckts, och att inga leveransorder är överflödiga.  
-   Dynamiskt skapade orderspårningslänkar måste balanseras om regelbundet.  

Med tiden blir dynamiska orderspårninglänkar obalanserade eftersom hela orderspårningsnätverket inte struktureras om förrän en efterfrågans- eller tillgångshändelse faktiskt stängs.  

Innan tillgången balanseras efter efterfrågan tar programmet bort alla befintliga orderspårningslänkar. Under motkonteringen, när en efterfrågans- eller en tillgångshändelse stängs skapar den nya orderspårninglänkar mellan tillgång och efterfrågan.  

> [!NOTE]  
>  Även om artikeln inte ställts in för dynamisk orderspårning skapar det planerade systemet balanserade orderspårningslänkar som förklaras ovan.
## <a name="closing-demand-and-supply"></a>Stänga tillgång och efterfrågan
När tillgångsbalanseringen har utförts finns det tre möjliga slutlägen:  

* Det begärda antalet och datumet för begäranhändelserna har uppfyllts och planeringen för dem kan stängas. Tillgångshändelsen är fortfarande öppen och kan eventuellt täcka nästa efterfrågan, så motkonteringen kan starta igen med aktuell tillgångshändelse och nästa efterfrågan.  
* Leveransordern kan inte ändras för att täcka all efterfrågan. Efterfråganshändelsen är fortfarande öppen, med visst antal som inte täckts men som kan täckas av nästa tillgångshändelse. På så sätt stängs den aktuella händelsen för efterfrågan, så att motkonteringen kan börja om igen med aktuell efterfrågan och nästa tillgångshändelse.  
* All efterfrågan har täckts. Det finns inte någon efterföljande efterfrågan (eller det har inte funnits någon efterfrågan alls). Om det finns någon överskottstillgång kan den minskas (eller annulleras) och sedan stängas. Det är möjligt att ytterligare tillförselhändelser finns längre fram i kedjan, och de bör också annulleras.  

Till sist skapar planeringssystemet en orderspårninglänk mellan tillgång och efterfrågan.  

### <a name="creating-the-planning-line-suggested-action"></a>Skapa planeringsraden (föreslagen åtgärd)  
Om åtgärder – nytt, ändra antal, ändra tidpunkt, ändra tidpunkt och ändra antal eller avbryt – föreslås för att granska leveransordern skapar planeringssystemet en planeringsrad i planeringsförslaget. På grund av orderspårning skapas planeringsraden inte bara när tillförselhändelsen stängs, utan även om efterfråganshändelsen stängs, även om tillförselhändelsen fortfarande är öppen och kan få ytterligare ändringar när nästa efterfråganshändelse behandlas. Det betyder att när planeringsraden har skapats kan den ändras på nytt.  

För att minska databasåtkomsten när du hanterar produktionsorder kan planeringsraden underhållas i tre nivåer, med målet att utföra den minst fordrande underhållsnivån:  

* Skapa endast planeringsraden med det aktuella förfallodatumet och antalet men utan verksamhetsföljden och komponenterna.  
* Inkludera verksamhetsföljd: den planerade verksamhetsföljden läggs ut inklusive beräkning av start- och slutdatum och tidpunkter. Det är fordrande i termer av databasåtkomster. För att fastställa slut- och förfallodatum kan det vara nödvändigt att beräkna detta även om tillförselhändelsen inte har stängts (om det gäller framåtplanering).  
* Ta med strukturexpansion: det kan vänta tills precis före tillgångshändelsen är avslutad.  

Detta slutför beskrivningarna av hur efterfrågan och tillgång laddas, prioriteras och balanseras av planeringssystemet. I integrering med den här tillgångsplaneringsaktiviteten måste systemet se till att önskad lagernivå för varje planerad artikel upprätthålls enligt dess partiformningsmetoder.

## <a name="see-also"></a>Se även  
 [Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)
