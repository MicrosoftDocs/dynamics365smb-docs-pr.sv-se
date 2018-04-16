---
title: "Designdetaljer - Läsa in lagerprofilerna | Microsoft Docs"
description: "För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d2a2ee196be4562f62604afd4faed608ff07411f
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-loading-the-inventory-profiles"></a>Designdetaljer: Läsa in lagerprofilerna
För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.  

 De normala typerna av efterfrågan och tillgång med förfallodatum på eller efter planeringsstartdatumet laddas i varje lagerprofil. När de laddas sorteras de olika efterfrågan- och tillgångstyperna enligt allmänna prioriteringar, till exempel förfallodatum, lågnivåkoder, lagerställe och variant. Dessutom kopplas orderprioriteter till de olika typerna för att se till att den viktigaste efterfrågan uppfylls först. Mer information finns i [Designdetaljer: prioritera order](design-details-prioritizing-orders.md)  

 Som nämndes tidigare kan efterfrågan kan även vara negativ. Det betyder att den ska hanteras som tillgång, men till skillnad från de vanliga typerna av tillgång anses negativ efterfrågan vara fast tillgång. Planeringssystemet tar hänsyn till det, men föreslår inga ändringar.  

 I allmänhet betraktar planeringssystemet alla leveransorder efter planeringsstartdatumet som möjliga att ändra för att uppfylla behov. Men så snart ett antal bokförs från en leveransorder kan den inte längre ändras av planeringssystemet. Följande olika order kan inte planeras om:  

- Släppta produktionsorder där förbrukning eller utflöde har bokförts.  

- Monteringsorder där förbrukning eller utflöde har bokförts.  

- Överföring order där utleveransen har bokförts.  

- Inköpsorder där inleverans har bokförts.  

  Förutom att ladda tillgångs- och efterfråganstyper, laddas vissa typer med hänsyn till speciella regler och beroenden som beskrivs i här efter.  

## <a name="item-dimensions-are-separated"></a>Artikeldimensioner är separerade  
 Leveransplanen måste beräknas per kombination av artikeldimensioner, till exempel variant och lagerställe. Men det finns ingen anledning att beräkna någon teoretisk kombination. Endast de kombinationer med ett efterfrågans- och/eller tillgångsbehov måste beräknas.  

 Planeringssystemet styr detta genom att gå igenom lagerprofilen. När en ny kombination hittas, skapas en internkontrollpost som innehåller den faktiska informationen om kombinationen. Programmet infogar lagerställeenheten som kontrollposten eller yttre loop. Det medför att rätt planeringsparametrar anges enligt en kombination av variant och lagerställe, och programmet kan fortsätta till den interna loopen.  

> [!NOTE]  
>  Programmet kräver inte att användaren ska ange en lagerställeenhetspost när du anger efterfrågan och/eller tillgång för en viss kombination av variant och lagerställe. Om en lagerställeenhet inte finns för en viss kombination skapar programmet därför sin egna tillfälliga lagerställeenhetspost som baseras på artikelkortdata. Om Lagerställe ska finnas har värdet Ja i fönstret Lagerinställningar måste antingen lagerställeenhet skapas eller Komponenter vid lagerställe anges till Ja. Mer information finns i [Designdetaljer: Efterfrågan vid tomt lagerställe](design-details-demand-at-blank-location.md).  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serie-/partinummer läses in efter specifikationsnivå  
 Attribut i form av serie-/partinummer laddas in i lagerprofilerna tillsammans med efterfrågan och tillgång som de har kopplats till.  

 Tillgångs- och efterfrågansattribut ordnas i prioritetsordning samt efter specifikationsnivå. Eftersom serie-/partinummermatchningar visar nivån av specifikation söker den mer specifika efterfrågan, till exempel ett partinummer som specifikt har valts för en försäljningsrad, efter en matchning före en mindre specifik efterfrågan, till exempel en försäljning från ett valfritt utvalt partinummer.  

> [!NOTE]  
>  Det finns inga tilldelade prioriteringregler för serie-/partinumrerad tillgång och efterfrågan, annat än nivån av specifikation som definieras av deras kombinationer av serie- och partinummer och artikelspårningsinställningen för de inblandade artiklarna.  

 Under balanseringen ser planeringssystemet tillgång med serie-/partinummer som oböjligt och försöker inte öka eller ändra tidpunkten för sådana leveransorder (såvida de inte används i samband en relation på orderbasis). Se Order-till-order-länkar bryts aldrig). Det skyddar tillgången från att ta emot flera, eventuellt motsägande, åtgärdsmeddelanden när en leverans har varierande attribut, till exempel en samling med av olika serienummer.  

 En annan anledning till att serie-/partinumrerad tillgång är inflexibel är att serie-/partinummer vanligtvis tilldelas så sent i processen att det skulle vara förvirrande om ändringar föreslås.  

 Motkonteringen av serienummer/partinummer respekterar inte [Fryst zon](design-details-dealing-with-orders-before-the-planning-starting-date.md). Om att efterfrågan och tillgång är inte är synkroniserade föreslår planeringssystemet ändringar eller förslår nya order oberoende av startdatumet för planeringen.  

## <a name="order-to-order-links-are-never-broken"></a>Order-till-order-länkar bryts aldrig  
 När du planerar en order-till-order-artikel får den länkade tillgången inte användas för någon annan efterfrågan än vad den ursprungligen ämnades för. Den länkade efterfrågan ska inte täckas av någon annan slumpmässig leverans, även om den för närvarande är tillgänglig vad gäller tid och antal. Exempelvis kan en monteringsorder som är kopplad till en försäljningsorder i ett scenario för montering mot kundorder inte användas för täcka annan efterfrågan.  

 Order-till-order-efterfrågan och -tillgång måste balanseras korrekt. Planeringssystemet säkerställer tillgången under alla omständigheter, utan att överväga storleksparametrar för ordern, modifierare och antal i lager (annat än antal som är knutna till länkade order). Av samma anledning föreslår systemet en minskning överskjutande tillgångar om den länkade efterfrågan minskas.  

 Denna motkontering påverkar också tidsplanen. Den begränsade horisonten som anges som tidsenheten beaktas inte; tillgången omplaneras om tidsplaneringen för efterfrågan har ändrats. Emellertid respekteras dämpartiden och förhindrar tillgång på orderbasis från att schemaläggas, förutom den interna tillgången i en flernivå-produktionsorder (projektorder).  

> [!NOTE]  
>  Serie-/partinummer kan också anges på order-till-order-efterfrågan. I så fall betraktas inte tillgången som inflexibel som standard, vilket vanligtvis är fallet för serienummer eller partinummer. I det här fallet ökar/minskar systemet enligt ändringarna i efterfrågan. Dessutom är det så att om en efterfrågan har varierande serie-/partinummer, till exempel mer än ett partinummer, föreslås en leveransorder per parti.  

> [!NOTE]  
>  Prognoser ska inte leda till att skapa leveransorder som är bundna av en order-till-order-länk. Om prognosen används den bör endast användas som för att skapa av härledd efterfrågan i en produktionsmiljö.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov läses in enligt produktionsorderändringar  
 När du arbetar med produktionsorder måste planeringssystemet övervaka de nödvändiga komponenterna innan du laddar dem i begäranprofilen. Komponentrader som skapas från en ändrad produktionsorder ersätter de från den ursprungliga beställningen. Detta säkerställer att planeringssystemet etablerar att planeringsrader för komponentbehov aldrig kopieras.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> Säkerhetslager kan förbrukas  
 Antalet i säkerhetslager är primärt en efterfråganstyp och laddas därför i lagerprofilen på planeringsstartdatumet.  

 Säkerhetslager är en lagerkvantitet som läggs undan för att kompensera för osäkerheter i efterfrågan under påfyllningledtiden. Den kan förbrukas om det är nödvändigt att ta från den för att uppfylla en efterfrågan. När detta sker kommer planeringssystemet att se till att säkerhetslagret snabbt ersätts genom att föreslå en leveransgsorder för att fylla på säkerhetslagret. Den här planeringsraden visar en ikon för en undantagsvarning som indikerar att säkerhetslagret delvis eller helt förbrukats och måste fyllas på genom en undantagsorder för det saknade antalet.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognostiserad efterfrågan minskas av försäljningsorder  
 Produktionsprognosen uttrycker förutsedd framtida efterfrågan. Medan den faktiska efterfrågan anges, vanligtvis som försäljningsorder för producerade artiklar, förbrukar den prognosen.  

 Själva prognosen minskas inte egentligen av försäljningsorder: den förblir densamma. Dock minskas prognosantalet som används i planeringsberäkningen (efter försäljningsorderantalet) innan det återstående antalet, om det finns något, anges i lagerprofilen för efterfrågan. När planeringssystemet undersöker faktiska försäljningar under en period, ingår både öppna försäljningsorder och artikeltransaktioner från levererade försäljningar, om de inte härrör från en avropsorder.  

 En användare måste definiera en giltig prognosperiod. Datumet på det prognostiserade antalet anger startdatum för perioden, och datumet på nästa prognos definierar sedan slutet av perioden.  

 Prognosen för perioder före planeringsperioden används inte, oavsett om den förbrukades eller inte. Den första prognossiffran av intresse är antingen datumet på eller det närmaste datumet före planeringsstartdatumet.  

 Prognosen kan användas för icke härledd efterfrågan, t.ex. försäljningsorder, eller härledd efterfrågan, t.ex. produktionsorderkomponenter (modul-prognos). En artikel kan ha båda typerna av prognos. Under planeringen sker förbrukningen separat, först för härledd efterfrågan och sedan för icke härledd efterfrågan.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Avropsorderbegäran minskas med försäljningsorder  
 Prognostisering kompletteras av avropsorder som ett sätt att ange framtida efterfrågan från en specifik kund. Som med den (ospecificerade) prognosen bör de faktiska försäljningarna förbruka den förutsedda efterfrågan, och det återstående antalet ska ingå i lagerprofilen för efterfrågan. Förbrukningen minskar inte avropsordern.  

 Planeringsberäkningen beaktar öppna försäljningsorder länkade till den specifika avropsorderraden, men den beaktar inte någon giltig tidsperiod. Det tar inte heller hänsyn till den bokförda order, eftersom bokföringsproceduren redan har reducerat det utestående avropsorderantalet.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
 [Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
 [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)

