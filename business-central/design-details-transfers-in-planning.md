---
title: Designdetaljer – Överföringar i planering
description: Lär dig hur du använder överföringsorder som en tillgång när du planerar lagernivåer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
ms.service: dynamics-365-business-central
---
# <a name="design-details-transfers-in-planning"></a>Designdetaljer: Överföringar i planering

Överföringsorder är också en källa till tillgång när de arbetar på nivån med lagerställeenheter. När du använder flera lagerställen (distributionslager) kan återanskaffningssystemet för lagerställeenheter ställas in till Överföring, vilket anger att lagerstället fylls på genom att varor överförs från ett annat lagerställe. I en situation med fler lagerställen kanske du har en kedja med överföringar. Leverans till GRÖN plats överförs från GULT, till exempel GULT överförs från RÖTT och så vidare. I början av kedjan finns återanskaffningssystemet **Prod. order** eller **Inköp**.  

![Exempel på överföringsflöde.](media/nav_app_supply_planning_7_transfers1.png "Exempel på överföringsflöde")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Om du jämför följande situationer är det uppenbart att planeringsuppgiften i den senare kan bli komplex:

* En leveransorder är direkt riktad mot en efterfrågeorder
* En försäljningsorder levereras via en kedja med SKU-överföringar

Om efterfrågan ändras kan det orsaka en dominoeffekt genom kedjan. Alla överföringsorder, plus inköps- och produktionsorder i den motsatta änden av kedjan, måste uppdateras för att balansera efterfrågan och tillgång.  

![Exempel på tillgång/efterfrågan på överföringar.](media/nav_app_supply_planning_7_transfers2.png "Exempel på tillgång/efterfrågan på överföringar")  

## <a name="why-is-a-transfer-a-special-case"></a>Varför är överföring ett specialfall?

Överföringsordrar liknar andra order som inköps- och produktionsorder. Men bakom kulisserna det är mycket annorlunda.  

En skillnad är att en överföringsrad representerar både efterfrågan och tillgång. Den utgående del som har levererats är efterfrågan. Den inkommande delen som inlevereras till det nya lagerstället, är tillgång på det lagerstället.  

![Innehåll på sidan överföringsorder.](media/nav_app_supply_planning_7_transfers3.png "Innehåll på sidan överföringsorder")  

När [!INCLUDE [prod_short](includes/prod_short.md)] ändrar tillgångssidan för överföringen måste den göra en liknande ändring på efterfrågesidan.  

## <a name="transfers-are-dependent-demand"></a>Överföringar är härledd efterfrågan

Relationen tillgång och efterfrågan liknar komponenterna på produktionsorderraderna. Skillnaden är att komponenter på produktionsorderrader är på nästa planeringsnivå och har en annan artikel. De båda delarna av överföringen finns på samma nivå för samma artikel.  

En viktig likhet är att komponenter och överföringar är härledda efterfrågan. Efterfrågan från en överföringsrad styrs av överföringens tillgångssida. Om leveransen ändras, påverkas efterfrågan direkt.

Om inte planläggningsflexibiliteten är Ingen ska en överföringsrad aldrig hanteras som oberoende behov i planeringen.  

I planeringsproceduren ska överföringsbegäran endast beaktas när tillgångssidan har behandlats av planeringssystemet. Innan bearbetningen sker är den verkliga efterfrågan inte känd. Ordningen på ändringar är viktig för överföringsorder.  

## <a name="planning-sequence"></a>Planera sekvens

I följande bild visas ett exempel på en sträng med överföringar.  

![Exempel på enkelt överföringsflöde.](media/nav_app_supply_planning_7_transfers4.png "Exempel på enkelt överföringsflöde")  

I det här exemplet beställer en kund artikeln på lagerställe GRÖN. Lagerställer GRÖN försörjs via överföring från det centrala distributionslagret RÖD. Det centrala distributionslagret RÖD försörjs via överföring från produktion på lagerstället BLÅ.  

I det här exemplet kommer planeringssystemet starta på kundefterfrågan och arbeta sig bakåt via kedjan. Tillgång och efterfrågan kommer att behandlas på ett lagerställe åt gången.  

![Leveransplanering med överföringar.](media/nav_app_supply_planning_7_transfers5.png "Leveransplanering med överföringar")  

## <a name="transfer-level-code"></a>Överföringsnivåkod

Överföringsnivåkoden för lagerställeenheten bestämmer i vilken sekvens planeringssystemet bearbetar lagerställen.  

Överföringsnivåkoden är ett internt fält. Fältet beräknas och lagras på lagerställeenheten när du skapar eller ändrar lagerställeenheten. Beräkningen körs över alla lagerställeenheter för en viss kombination av artikel och artikelvariant. Beräkningen använder lagerställekoden och överför-från-koden för att bestämma vilken väg som ska användas för lagerställeenheterna. Beräkningen säkerställer att all efterfrågan bearbetas.  

Överföringsnivåkoden ska vara 0 för lagerställeenhet med påfyllningssystem Inköp eller Pryd.order och ska vara -1 för den första överföringsnivån, -2 för den andra, o.s.v. I exemplet som beskrevs i föregående avsnitt skulle nivåerna därför vara -1 för RÖD och -2 för GRÖN, som visas i följande illustration.  

![Sida för innehåll på kort på lagerställeenhet.](media/nav_app_supply_planning_7_transfers6.gif "Sida för innehåll på kort på lagerställeenhet")  

När du uppdaterar en lagerställeenhet identifierar om återanskaffningssystemet för lagerställeenheter har cirkulära referenser.  

## <a name="planning-transfers-without-sku"></a>Planera överföringar utan lagerställeenhet

För mindre avancerade distributionslagerinställningar kan du använda lagerställen och göra manuella överföringar mellan lagerställen, även om du inte använder lagerställeenheter. Överföringen kan till exempel täcka en försäljningsorder på det lagerstället. Planeringssystemet svarar på ändringar i efterfrågan.  

För manuella överföringar analyserar planeringssystemet överföringsorder och planerar vilken ordning lagerställena ska bearbetas i. Internt kommer planeringssystemet att använda tillfälliga lagerställeenheter som har överföringsnivåkoder.  

![Överföringsnivåkod.](media/nav_app_supply_planning_7_transfers7.png "Överföringsnivåkod")  

Om det finns fler överföringar till ett lagerställe finns kommer det första överföringsordern att definiera planeringsriktningen. Överföringar i den motsatta riktningen annulleras.  

## <a name="changing-quantity-with-reservations"></a>Ändra antal med reservationer

När du ändrar kvantiteter för en leverans tar det hänsyn till reservationer i planeringssystemet. Reserverad kvantitet representerar den undre gränsen för hur mycket du bör minska tillgången.  

När du ändrar kvantiteten på en överföringsorderrad bör du behålla den nedre gränsen i åtanke. Den nedre gränsen är den högsta reserverade kvantiteten för raderna för avgående och ankommande överföringar.

En överföringsorderrad på 117 stycken är till exempel reserverad för följande rader:

* En försäljningsrad på 46
* En inköpsrad på 24

Även om den ankommande sidan kan ha extra tillgångar kan du inte minska överföringsraden under 46.  

![Reservationer i överföringsplanering.](media/nav_app_supply_planning_7_transfers8.png "Reservationer i överföringsplanering")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Ändra antal i en överföringskedja

Här följer ett exempel på vad som händer när du ändrar en kvantitet i en överföringsändring.

Startpunkten är en balanserad situation med en överföringskedja som levererar en försäljningsorder på 27 vid lagerstället RÖD. Det finns en motsvarande inköpsorder på lagerstället BLÅ. Båda överföringarna går igenom lagerstället ROSA. Det finns två överföringsorder, BLÅ-ROSA OCH ROSA-RÖD.  

![Ändrar kvantiteten i överföringsplanering 1.](media/nav_app_supply_planning_7_transfers9.png "Ändrar kvantiteten i överföringsplanering 1")  

Nu väljer planeraren vid lagerställe ROSA att reservera för inköpet.  

![Ändrar kvantiteten i överföringsplanering 2.](media/nav_app_supply_planning_7_transfers10.png "Ändrar kvantiteten i överföringsplanering 2")  

Reservationen innebär vanligtvis att planeringssystemet ignorerar inköpsordern och överföringsbegäran. Så länge det finns saldo är det inga problem. Men vad händer om ordningen på det RÖDA lagerstället ändras från 27 till 22?  

![Ändrar kvantiteten i överföringsplanering 3.](media/nav_app_supply_planning_7_transfers11.png "Ändrar kvantiteten i överföringsplanering 3")  

När planeringssystemet körs igen ska det avlägsna den överskjutande tillgången. Men reservationen låser inköpet och överföring till antalet 27.  

![Ändrar kvantiteten i överföringsplanering 4.](media/nav_app_supply_planning_7_transfers12.png "Ändrar kvantiteten i överföringsplanering 4")  

Överföringen ROSA-RÖD har minskat till 22. Den inkommande delen av den BLÅ-ROSA överföringen reserveras inte, men den avgående delen gör det. Reservationen innebär att du inte kan minska kvantiteten under 27.  

## <a name="lead-time-calculation"></a>Ledtidsberäkning

När förfallodatumet beräknas för en överföringsorder beaktas olika typer av ledtid.  

Följande ledtider är aktiva när en överföringsorder planeras:  

* Utgående lagerhanteringstid  
* Leveranstid  
* Inkommande lagerhanteringstid  

På planeringsraden används följande fält för att ge information om beräkningen:  

* Överföringsutleveransdatum  
* Startdatum  
* Slutdatum  
* Förfallodatum  

Leveransdatumet för överföringsraden visas i fältet **Överföringsutleveransdatum**. Leveransdatumet för överföringsraden visas i fältet **Förfallodatum**.  

Start – och slutdatum beskriver den faktiska transportperioden.  

Följande bild visar tolkningen av startdatum-tid och slutdatum-tid på planeringsrader som hör till överföringsorder.  

![Centrala datum-tider i överföringsplanering.](media/nav_app_supply_planning_7_transfers13.png "Centrala datum-tider i överföringsplanering")  

Exemplet visar följande beräkningar:  

* Utleveransdatum + utgående hantering = Startdatum  
* Startdatum + Leveranstid = Slutdatum  
* Slutdatum + inkommande hanteringstid = Inleveransdatum  

## <a name="safety-lead-time"></a>Säkerhetsledtid

Fältet **Standard säkerhetsledtid** på sidan **Produktionsinställningar** och det relaterade fältet **Säkerhetsledtid** på sidan **Artikelkort** ska inte beaktas vid beräkningen av en överföringsorder. Säkerhetsledtiden påverkar dock hela planen. Säkerhetsledtiden påverkar återanskaffningsordern (inköp eller produktion) i början av överföringskedjan. Det är den punkt där artiklarna placerades på det lagerställe som de ska överföras från.  

![Element på förfallodatumet för överföringen.](media/nav_app_supply_planning_7_transfers14.png "Element på förfallodatumet för överföringen")  

På produktionsorderraden är Slutdatum + Säkerhetsledtid + inkommande Dist.lag. hanteringstid = Förfallodatum.  

På inköpsorderraden är Planerat inleveransdatum + Säkerhetsledtid + inkommande Lagerhanteringstid = Förväntat inleveransdatum.  

## <a name="reschedule"></a>Omplanera

När du planerar om en befintlig överföringsrad söker planeringssystemet efter den utgående artikeln och ändrar datum och tid.

> [!NOTE]
> Om en ledtid har definierats kommer det uppstå en lucka mellan utleveransen och inleveransen. Ledtid kan bestå av fler element, till exempel transporttid och lagerhanteringstid. På en tidslinje kommer planeringssystemet att flytta till bakåt i tid medan den balanserar elementen.  

![Ändrar förfallodatum i överföringsplanering.](media/nav_app_supply_planning_7_transfers15.png "Ändrar förfallodatum i överföringsplanering")  

När du ändrar förfallodatumet på en överföringsrad måste därför ledtiden beräknas för att uppdatera den utgående sidan av överföringen.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a>Serie- och partinummer i överföringskedjor

Om efterfrågan använder serie- eller partinummer och du kör planeringsmotorn kommer den att skapa överföringsorder. Se Artikelattribut för mer information om begreppet. Om däremot serie- eller partinummer tas bort från efterfrågan kommer de skapade överföringsorderna fortfarande använda serie- eller artikelnummer och planeringen ignorerar dem (inte tas bort).  

## <a name="order-to-order-links"></a>Order-till-order-länkar

I det här exemplet ställs en BLÅ SKU in med partiformningsmetoden **Order**. De ROSA och RÖDA lagerställeenheterna har partiformningsmetoden **Parti-för-parti**. Om du skapar en försäljningsorder för 27 vid lagerställe RÖTT leder det till en kedja av överföringar. Den sista överföringen sker vid lagerstället BLÅ och är reserverad med bindning. I det här fallet är reservationerna inte fasta reservationer som skapats av planeraren på lagerställe ROSA. I planeringssystemet skapas bindningarna. Den viktiga skillnaden är att planeringssystemet kan ändra det sistnämnda.  

![Länkar med order till order i överföringsplaneringen.](media/nav_app_supply_planning_7_transfers16.png "Länkar med order till order i överföringsplaneringen")  

Om efterfrågan ändras från 27 till 22 kommer planeringssystemet att minska antalet nedåt genom kedjan. Den bindande reservationen minskas också.  

## <a name="see-also"></a>Se även

[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Planera med och utan lagerställen](production-planning-with-without-locations.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
