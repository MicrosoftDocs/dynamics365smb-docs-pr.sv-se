---
title: Designdetaljer – Överföringar i planering | Microsoft Docs
description: Det här avsnittet beskriver hur du använder överföringsorder som en tillgång när du planerar lagernivåer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, transfer, sku, locations, warehouse
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 829594fa196758502c67f52c4a7277d3b63aa41f
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035587"
---
# <a name="design-details-transfers-in-planning"></a>Designdetaljer: Överföringar i planering
Överföringsorder är också en källa till tillgång när de arbetar på nivån med lagerställeenheter. När du använder flera lagerställen (distributionslager) kan återanskaffningssystemet för lagerställeenheter ställas in till Överföring, vilket anger att lagerstället fylls på genom att varor överförs från ett annat lagerställe. I en sådan situation med flera distributionslager kan företag ha en kedja av överföringar där tillgång till lagerställe GRÖN överförs från GUL, och tillgång till GUL överförs från RÖD och så vidare. I början av kedjan finns återanskaffningssystemet Prod.order eller Inköp.  

![Exempel på överföringsflöde](media/nav_app_supply_planning_7_transfers1.png "Exempel på överföringsflöde")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

När du jämför situationen när en leveransorder återförs direkt mot en begäranorder med en situation där försäljningsordern levereras via en kedja av lagerställeenhetsöverföringar, är det uppenbart att planeringsuppgiften i den senare situationen kan bli mycket komplex. Om efterfrågan ändras kan det orsaka en dominoeffekt genom kedjan, eftersom alla överföringsorder plus inköps-/produktionsorder i den motsatta änden av kedjan måste ändras för att återställa balansen mellan efterfrågan och tillgång.  

![Exempel på tillgång/efterfrågan på överföringar](media/nav_app_supply_planning_7_transfers2.png "Exempel på tillgång/efterfrågan på överföringar")  

## <a name="why-is-transfer-a-special-case"></a>Varför är överföring ett specialfall?  
En överföringsorder liknar andra order i programmet. Men bakom kulisserna det är mycket annorlunda.  

En vanlig aspekt som gör att överföringar i planeringen skiljer sig från inköps- och produktionsorder är att en överföringsrad representerar efterfrågan och tillgång samtidigt. Den utgående del som skickas från den gamla lagerstället, är efterfrågan. Den inkommande delen som ska inlevereras till det nya lagerstället, är tillgång på det lagerstället.  

![Innehåll på sidan överföringsorder](media/nav_app_supply_planning_7_transfers3.png "Innehåll på sidan överföringsorder")  

Det betyder att när systemet hanterar tillförselsidan för överföringen måste systemet göra en liknande ändring i på begärandesidan.  

## <a name="transfers-are-dependent-demand"></a>Överföringar är härledd efterfrågan  
Den relaterade efterfrågan och tillgången har en viss likhet med komponenterna för en produktionsorderrad, men skillnaden är att komponenter kommer att vara på nästa planeringsnivå och med annan artikel, medan de två delarna av överföringen finns på samma nivå, för samma artikel.  

En viktig likhet är att precis som komponenter är härledd efterfrågan, så är även överföringsbegäran. Efterfrågan från en överföringsrad föreskrivs av tillgångssidan av överföringen på så sätt att om tillgången ändras, så påverkas efterfrågan direkt.  

Om inte planläggningsflexibiliteten är Ingen ska en överföringsrad aldrig hanteras som oberoende behov i planeringen.  

I planeringsproceduren ska överföringsbegäran endast beaktas när tillgångssidan har behandlats av planeringssystemet. Innan dess är den faktiska efterfrågan inte känd. Sekvensen av de gjorda ändringarna kan därför vara mycket viktig när det gäller överföringsorder.  

## <a name="planning-sequence"></a>Planera sekvens  
Följande illustration visar hur en sträng med överföringar kan se ut.  

![Exempel på enkelt överföringsflöde](media/nav_app_supply_planning_7_transfers4.png "Exempel på enkelt överföringsflöde")  

I det här exemplet beställer en kund artikeln på lagerställe GRÖN. Lagerställer GRÖN försörjs via överföring från det centrala distributionslagret RÖD. Det centrala distributionslagret RÖD försörjs via överföring från produktion på lagerstället BLÅ.  

I det här exemplet kommer planeringssystemet starta på kundefterfrågan och arbeta sig bakåt via kedjan. Tillgång och efterfrågan kommer att behandlas på ett lagerställe åt gången.  

![Leveransplanering med överföringar](media/nav_app_supply_planning_7_transfers5.png "Leveransplanering med överföringar")  

## <a name="transfer-level-code"></a>Överföringsnivåkod  
Sekvensen som lagerställena som behandlas i inom planeringssystemet bestäms av överföringsnivåkoden för lagerställeenheten.  

Överföringsnivåkoden är ett internt fält som beräknas automatiskt och lagras på lagerställeenheter, när lagerställeenheten registreras eller ändras. Beräkningen körs för alla lagerställeenheter för en viss kombination av artikeln/variant, och använder lagerställekoden och överföring-från-koden för att fastställa verksamhetsföljden som planeringen måste använda när den korsar lagerställeenheterna för att se till att alla behov behandlas.  

Överföringsnivåkoden ska vara 0 för lagerställeenhet med påfyllningssystem Inköp eller Pryd.order och ska vara -1 för den första överföringsnivån, -2 för den andra, o.s.v. I överföringskedjan som beskrevs ovan skulle nivåerna därför vara -1 för RÖD och -2 för GRÖN, som visas i följande illustration.  

![Sida för innehåll på kort på lagerställeenhet](media/nav_app_supply_planning_7_transfers6.gif "Sida för innehåll på kort på lagerställeenhet")  

När du uppdaterar en lagerställeenhet undersöker planeringssystemet om lagerställeenheter med återanskaffningssystemet Överföring har ställts in med cirkulära referenser.  

## <a name="planning-transfers-without-sku"></a>Planera överföringar utan lagerställeenhet  

Även om funktionen för lagerställeenhet inte används är det möjligt att använda lagerställen och göra manuella överföringar mellan lagerställen. För företag med mindre avancerad distributionslagerinställning stöder planeringssystemet scenarier där det befintliga lagret överförs manuellt till en annan plats, t.ex för att täcka en försäljningsorder vid det aktuella lagerstället. Samtidigt ska planeringssystemet svara på ändringar i efterfrågan.  

För att stödja manuella överföringar analyserar planeringen befintliga överföringsorder och planerar sedan vilken ordning lagerställena ska hanteras i. Internt kommer planeringssystemet att arbeta med tillfälliga lagerställeenheter som har överföringsnivåkoder.  

![Överföringsnivåkod](media/nav_app_supply_planning_7_transfers7.png "Överföringsnivåkod")  

Om fler överföringar till en viss lagerställe finns kommer det första överföringsordern att definiera planeringsriktningen. Överföringar som körs i den motsatta riktningen annulleras.  

## <a name="changing-quantity-with-reservations"></a>Ändra antal med reservationer  
När du ändrar antal på befintlig leverans, beaktar planeringssystemet reservationer på så sätt att det reserverade antalet representerar den lägre gränsen för hur mycket tillgången kan minskas.  

När antalet ändras på en befintlig överföringsorderrad ska du tänka på att den lägre gränsen definieras som det högsta reserverade antalet för den utgående och inkommande överföringsraden.  

Om t.ex en överföringsorderrad med 117 enheter har reserverats mot en försäljningsrad med 46 och en inköpsrad med 24, är det inte möjligt att minska överföringsraden nedanför 46 enheter även om det kan utgöra överskjutande tillgång på den inkommande sidan.  

![Reservationer i överföringsplanering](media/nav_app_supply_planning_7_transfers8.png "Reservationer i överföringsplanering")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Ändra antal i en överföringskedja  
I följande exempel är utgångspunkten en balanserad situation med en överföringskedja som inlevererar en försäljningsorder på 27 till lagerställe RÖD med en motsvarande inköpsorder på lagerställe BLÅ som har överförts via lagerställe ROSA. Förutom för försäljningar och inköp finns det därför två överföringsorder: BLÅ-ROSA och ROSA-RÖD.  

![Ändrar kvantiteten i överföringsplanering 1](media/nav_app_supply_planning_7_transfers9.png "Ändrar kvantiteten i överföringsplanering 1")  

Nu väljer planeraren vid lagerställe ROSA att reservera mot inköpet.  

![Ändrar kvantiteten i överföringsplanering 2](media/nav_app_supply_planning_7_transfers10.png "Ändrar kvantiteten i överföringsplanering 2")  

Det innebär vanligtvis att planeringssystemet ignorerar inköpsordern och överföringsbegäran. Så länge det finns saldo är det inga problem. Men vad händer när kunden vid lagerställe RÖD delvis ångrar sin beställning och ändrar den till 22?  

![Ändrar kvantiteten i överföringsplanering 3](media/nav_app_supply_planning_7_transfers11.png "Ändrar kvantiteten i överföringsplanering 3")  

När planeringssystemet körs igen ska det avlägsna den överskjutande tillgången. Men reservationen låser inköpet och överföring till antalet 27.  

![Ändrar kvantiteten i överföringsplanering 4](media/nav_app_supply_planning_7_transfers12.png "Ändrar kvantiteten i överföringsplanering 4")  

Överföringen ROSA-RÖD har minskat till 22. Den ingående delen av BLÅ-ROSA överföringen är inte reserverade, men eftersom den utgående del reserveras det går inte att minska kvantiteten under 27.  

## <a name="lead-time-calculation"></a>Ledtidsberäkning  
När förfallodatumet beräknas för en överföringsorder beaktas olika typer av ledtid.  

Ledtiderna som är aktiva när en överföringsorder planeras är:  

* utgående lagerhanteringstid  
* Leveranstid  
* inkommande lagerhanteringstid  
* På planeringsraden används följande fält för att ge information om beräkningen.  
* Överföringsutleveransdatum  
* Startdatum  
* Slutdatum  
* Förfallodatum  

Utleveransdatumet på överföringsraden visas i överföringsutleveransdatumfältet, och inleveransdatum på överföringsraden ska i förfallodatumfältet.  

Start – och slutdatum ska användas för att beskriva den faktiska transportperioden.  

Följande illustration visar tolkningen av startdatum-tid och slutdatum-tid på planeringsrader som hör till överföringsorder.  

![Centrala datum-tider i överföringsplanering](media/nav_app_supply_planning_7_transfers13.png "Centrala datum-tider i överföringsplanering")  

I det här exemplet betyder det att:  

* Utleveransdatum +  utgående hantering =  Startdatum  
* Startdatum + Leveranstid = Slutdatum  
* Slutdatum + inkommande hanteringstid = Inleveransdatum  

## <a name="safety-lead-time"></a>Säkerhetsledtid  
Fältet Standard säkerhetsledtid på sidan Produktionsinställningar och det relaterade fältet Säkerhetsledtid på artikelkortet ska inte beaktas vid beräkningen av en överföringsorder. Emellertid påverkar säkerhetsledtiden fortfarande den totala planeringen så som den påverkar återanskaffningsordern (inköp eller produktion) i början av överföringskedjan när artiklarna placeras på lagerstället som de ska överföras från.  

![Element på förfallodatumet för överföringen](media/nav_app_supply_planning_7_transfers14.png "Element på förfallodatumet för överföringen")  

På produktionsorderraden är Slutdatum + Säkerhetsledtid + inkommande Dist.lag. hanteringstid = Förfallodatum.  

På inköpsorderraden är Planerat inleveransdatum + Säkerhetsledtid + inkommande Lagerhanteringstid = Förväntat inleveransdatum.  

## <a name="reschedule"></a>Omplanera  
När du planerar om en befintlig överföringsrad måste planeringssystemet söka efter den utgående artikeln och ändra datum och tid på den. Det är viktigt att observera att om ledtid har definierats kommer det uppstå en lucka mellan utleveransen och inleveransen. Som nämndes kan ledtid bestå av fler element, till exempel transporttid och lagerhanteringstid. På en tidslinje kommer planeringssystemet att flytta till bakåt i tid medan den balanserar elementen.  

![Ändrar förfallodatum i överföringsplanering](media/nav_app_supply_planning_7_transfers15.png "Ändrar förfallodatum i överföringsplanering")  

När du ändrar förfallodatumet på en överföringsrad måste därför ledtiden beräknas för att uppdatera den utgående sidan av överföringen.  

## <a name="seriallot-numbers-in-transfer-chains"></a>Serie-/partinummer i överföringskedjor  
Om efterfrågan har serie-/partinummer och planeringsmotorn körs, kommer den att skapa några direkt skapade överföringsorder. Se Artikelattribut för mer information om begreppet. Om däremot serie-/partinummer tas bort från efterfrågan kommer de skapade överföringsorderna i kedjan fortfarande att ha serie-/artikelnummer och ignoreras därför av planeringen (inte tas bort).  

## <a name="order-to-order-links"></a>Order-till-Order-länkar  
I det här exemplet ställa lagerställeenhet BLÅ in med partiformningsmetoden Order, medan ROSA och RÖD använder Parti-för-parti. När en försäljningsorder med 27 skapas för lagerställe RÖD kommer det leda till en kedja av överföringar med den sista skarven i lagerställe BLÅ som har reserverats med bindning. I det här fallet är reservationerna inte fasta reservationer som skapats av planeraren på lagerställe ROSA lagerställe, utan bindningar som skapats av planeringssystemet. Den viktiga skillnaden är att planeringssystemet kan ändra det sistnämnda.  

![Länkar med order till order i överföringsplaneringen](media/nav_app_supply_planning_7_transfers16.png "Länkar med order till order i överföringsplaneringen")  

Om efterfrågan ändras från 27 till 22 kommer systemet att minska antalet nedåt genom kedjan, och den bindande reservationen minskas också.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Efterfrågan vid tomt lagerställe](design-details-demand-at-blank-location.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
