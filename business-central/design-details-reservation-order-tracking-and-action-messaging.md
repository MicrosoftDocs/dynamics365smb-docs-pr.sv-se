---
title: 'Designdetaljer – reservation, orderspårning och åtgärdsmeddelanden | Microsoft Docs'
description: Reservationsystemet är omfattande och innehåller de korrelativa och parallella funktionerna i orderspårning och åtgärdsmeddelanden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 07/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-reservation-order-tracking-and-action-messaging"></a>Designdetaljer: Reservation orderspårning och åtgärdsmeddelanden

Reservationsystemet är omfattande och innehåller de korrelativa och parallella funktionerna i orderspårning och åtgärdsmeddelanden.  

Kärnan i reservationssystemet är sammankopplingen av en efterfrågetransaktion och en motsvarande tillgångstransaktion, antingen genom reservation eller orderspårning. En reservation är användargenererad koppling, och en orderspårningpost är systemgenererad koppling. Ett artikelantal som anges i reservationsystemet kan antingen reserveras eller orderspåras, men inte båda på samma gång. Hur en artikel hanteras i systemen beror på hur artikeln är upplagd.  

Reservationsystemet kommunicerar med planeringssystemet genom att skapa åtgärdsmeddelanden på planeringsrader under planeringskörningar. Ett åtgärdsmeddelande kan ses som en bilaga till en orderspårningpost. Åtgärdsmeddelanden, oavsett om de skapas dynamiskt i orderspårning eller under planeringskörningen, ger ett praktiskt verktyg för effektiv leveransplanering.  

> [!NOTE]  
> Det reserverade antalet ignoreras av planeringssystemet, det vill säga, den fasta länken mellan tillgång och efterfrågan kan inte ändra via planering.  

 Reservationsystemet utgör även strukturella grunden för artikelspårningsystemet. Mer information finns i [Designdetaljer: Artikelspårning](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## <a name="reservation"></a>Reservation

 En reservation är en fast koppling som ansluter en viss efterfrågan och tillgång till varandra. Den här länken påverkar direkt den efterföljande lagertransaktionen och säkerställer rätt koppling av artikeltransaktioner för kostnadsskäl. En reservation åsidosätter standardvärderingsprincipen för en artikel. Mer information finns i [Designdetaljer: Artikelspårning](design-details-item-tracking.md).  

 Sidan **Reservation** kan nås från alla orderrader av både tillgångs- och efterfråganstyp. På den här sidan kan du ange vilka efterfråganstransaktioner eller tillgångstransaktioner att skapa en reservationslänk till. Reservationen består av ett par poster som har samma löpnummer. En post har ett negativt tecken och pekar på efterfrågan. Den andra posten har ett plustecken och pekar mot tillgången. Dessa poster lagras i tabellen Reservationstransaktion *med* statusvärdet *Reservation*. Användaren kan visa alla reservationer på sidan **Reservationstransaktioner**.  

### <a name="offsetting-in-reservations"></a>Motkontering i reservationer

 Reservationer görs mot tillgängligt antal artiklar. Artikeldispositionen beräknas i grundläggande villkor enligt följande:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Följande tabell visar detaljerna för ordernätverksenheterna som ingår i dispositionsberäkningen.  

||Fält i T27-artikel|Källtabell|Tabellfilter|Källfält|  
|-|------------------|------------------|------------------|------------------|  
|**Lager**|Lagersaldo|Artikeltransaktion|Inte tillämpligt|Antal|  
|**Planenliga inleveranser**|Fast plan. orderinlevns (ant.)|Prod.orderrad|=Fast planerad|Återstående ant. (bas)|  
|**Planenliga inleveranser**|Släppt orderinlevns (ant.)|Prod.orderrad|=Släppt|Återstående ant. (bas)|  
|**Planenliga inleveranser**|Ant. på monteringsorder|Monteringsrubrik|=Order|Återstående ant. (bas)|  
|**Planenliga inleveranser**|Antal på inköpsorder|Inköpsrad|=Order|Restnoterat antal (bas)|  
|**Planenliga inleveranser**|Trans.order inlevns (ant.)|Överföringsrad|Inte tillämpligt|Restnoterat antal|  
|**Bruttobehov**|Antal på förs.order|Försäljningsrad|=Order|Restnoterat antal (bas)|  
|**Bruttobehov**|Planerat behov (antal)|Prod.orderkomponent|<>Simulerad|Återstående ant. (bas)|  
|**Bruttobehov**|Ant. vid komponentmontering|Monteringsrad|=Order|Återstående ant. (bas)|  
|**Bruttobehov**|Trans.order utleverans (ant.)|Överföringsrad|Inte tillämpligt|Restnoterat antal|  

 Mer information finns i [Designdetaljer: disposition i distributionslagret](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation"></a>Manuell reservation

När en användare med vilje skapar en reservation får användaren fullständig äganderätt och ansvar för dessa artiklar. Det betyder att användaren också måste ändra numret manuellt eller annullera en reservation. Sådana manuella ändringar kan orsaka automatisk ändring av de berörda reservationerna.  

I följande tabell visas när och vilka ändringar som kan göras:  

|Användaråtgärd|Systemreaktion|  
|-----------------|---------------------|  
|Minska det reserverade antalet|Projektspecifika antalsfält uppdateras därefter.|  
|Ändra datumfält|Projektspecifika datumfält uppdateras.<br /><br /> **Obs!** Om förfallodatum för en efterfrågan ändras för att föregå utleveransdatumet eller förfallodatumet för leveransen, annulleras reservationen.|  
|Ta bort ordern|Reservationen har annullerats.|  
|Ändra lagerställe, lagerplats, variant, serienumret eller partinummer|Reservationen har annullerats.|  

> [!NOTE]  
> Funktionen Sen bindning kan också ändra reservationer utan att informera användaren, genom att ombilda icke-specifika reservationer av serie- eller partinummer. Mer information finns i  [Designdetaljer: artikelspårning och reservationer](design-details-item-tracking-and-reservations.md).  

### <a name="automatic-reservations"></a>Automatiska reservationer

 Artikelkortet kan ställas in att alltid vara reserverat automatiskt från efterfrågan, till exempel försäljningsorder. I så fall skapas en reservation mot lager, inköpsorder, monteringsorder och produktionsorder. En varning skickas ut om tillgången inte räcker.  

 Dessutom reserveras artiklar automatiskt av olika planeringsfunktioner för att hålla ett behov kopplat till en viss tillgång. Orderspårningstransaktionerna för sådana planeringslänkar innehåller **Reservation i fältet** Reservationsstatus **i tabellen Reservationstransaktion**  *.*  Automatiska reservationer skapas i följande situationer:  

- En produktionsorder med flera nivåer där fältet **Produktionsprincip** för de berörda överordnade och underordnade artiklarna anges till **Tillverka-Mot-Order**. Planeringssystemet skapar reservationer mellan den överordnade produktionsordern och de underliggande produktionsordrarna för att säkerställa att de bearbetas tillsammans. Sådan reservationsbindning åsidosätter artikelns standardmetod för värdering och koppling.  

- En produktion, en montering eller inköpsorder där fältet **Partiformningsmetod** för den berörda artikeln anges till **Inköpsorder**. Planeringssystemet skapar reservationer mellan efterfrågan och den planerade tillgången för att se till att den aktuella tillgången skapas. För mer information, se [Order](design-details-handling-reordering-policies.md#order).  

- En produktionsorder som skapats från en försäljningsorder med funktionen **Försäljningsorderplanering** länkas till försäljningsordern med en automatisk reservation.  

- En sammansättningsorder som skapas automatiskt för en försäljningsorderrad för att uppfylla kvantiteten **i fältet Ant. att montera mot order** . Den automatiska reservationen länkar försäljningsbegäran och monteringtillförseln, så att försäljningsorderhandläggare kan anpassa och lova monteringsartikeln direkt till kunden. Dessutom länkar reservationen monteringsutflöde på försäljningsorderraden till utleveransaktiviteten som uppfyller kundordern.  

Om tillgång eller behov inte fördelas tilldelas automatiskt en reservationsstatus av typen **Överskott**. Detta kan bero på en efterfrågan på grund av ett prognostiserat antal eller användarangivna planeringsparametrar. Detta är legitimt överskott, som systemet känner igen, och det ger inte upphov till åtgärdsmeddelanden. Överskott kan också vara äkta, överflödig tillgång eller efterfrågan som inte har spårats. Detta är en indikation på obalans i ordernätverket som gör att systemet skickar åtgärdsmeddelanden. Observera att ett åtgärdsmeddelande som föreslår en ändring i antal alltid refererar till typen **Överskott**. Mer information finns [i avsnittet Exempel: Orderspårning i försäljning, produktion och överföringar](#example-order-tracking-in-sales-production-and-transfers) i den här artikeln.  

Automatiska reservationer som upprättas under planeringskörningen hanteras på följande sätt:  

- De tillämpas på artikelkvantiteter som ingår i tillgänglighetsberäkningen, liksom manuella reservationer. Mer information finns i avsnittet "Kvittning vid bokningar" i den här artikeln.  

- De inkluderas och kan ändras i efterföljande planeringskörningar, i motsats till manuellt reserverade artiklar.  

## <a name="order-tracking"></a>Orderspårning

Orderspårning hjälper planeraren att upprätthålla en giltigt leveransplan genom att visa en översikt över motkontering mellan efterfrågan och tillgång i ordernätverket. Orderspårningposterna fungerar som grund för att skapa dynamiska åtgärdsmeddelanden och planeringsradförslag vid planeringskörningar.  

> [!NOTE]  
> Orderspårningssystemet avräknar det disponibla materialet när order anges i ordernätverket. Det betyder att systemet inte prioriterar order som kan vara mer brådskande i termer av förfallodatum. Det är därför upp till logiken för planeringssystemet eller visheten hos planeraren att ordna om prioriteringarna på ett meningsfullt sätt.  

> [!NOTE]  
> Orderspårningsprincipen och funktionen Hämta åtgärdsmeddelanden är inte integrerade med Projekt. Det betyder att efterfrågan som hör till ett projekt inte spåras automatiskt. Eftersom den inte spåras kan det orsaka att användningen av en befintlig återanskaffning med projektinformation spåras för en annan efterfrågan, till exempel en försäljningsorder. Du kan därför hamna i en situation där din information om disponibelt lager inte är synkroniserad.  

### <a name="the-order-network"></a>Ordernätverket

Orderspårningsystemet baseras på principen att ordernätverket alltid måste vara i ett balanserat tillstånd där varje efterfrågan som kommer in i systemet räknas av mot en motsvarande tillgång och vice versa. Systemet gör det genom att identifiera logiska länkar mellan alla efterfrågans- och tillgångstransaktioner i ordernätverket.  

Principen betyder att en ändring i efterfrågan leder till motsvarande obalans på tillgångssidan av ordernätverket. En ändring i tillgång leder till en motsvarande obalans på efterfråganssidan av ordernätverket. I verkligheten är ordernätverket i ett tillstånd av konstant förändring när användare anger, ändrar och tar bort beställningar. Orderspårningsprocesser beställer dynamiskt och reagerar på varje ändring vid den tidpunkt då den kommer in i systemet och blir en del av ordernätverket. Så snart som nya orderspårningposter skapas, är ordernätverket balanserat, men endast tills nästa ändring inträffar.  

Om du vill öka översikten över beräkningar i planeringssystemet visar sidan **Ej spårade planeringselement** antal som inte spårats, och som representerar skillnaden i antal mellan det kända behovet och den föreslagna tillförseln. Varje rad på sidan refererar till orsaken för överskottsantalet, till exempel **Avropsorder**, **Säkerhetslagernivå**, **Fast orderkvantitet**, **Min. partistorlek**, **Avrundning**eller **Dämpare**.  

### <a name="offsetting-in-order-tracking"></a>Motkontering i orderspårning

I motsats till reservationer, som kan bara utföras mot tillgängliga artikelantal, är orderspårning möjlig mot alla ordernätverksenheter som ingår i beräkningen av nettobehov i planeringssystemet. Nettobehoven beräknas enligt följande:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> Efterfrågan som är kopplad till prognoser eller planeringsparametrar inte är orderspårad.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a>Exempel: Orderspårning i försäljningar, produktion och överföringar

I följande scenario visas vilka orderspårningstransaktioner som skapas i tabellen Reservationstransaktion *till* följd av olika ändringar i ordernätverket.  

Anta att följande data finns för två artiklar som har angetts för orderspårning.  

|Artikel|Parameter|Detaljer|
|-|-|-|
|Artikel 1|Name|Komponent|
||Disposition|100 enheter i ÖST läge<br /><br />- 30 enheter av LOTA<br />- 70 enheter av LOTB|  
|Artikel 2|Name|Producerad artikel|
||Produktionsstruktur|1 kvantitet per komponent|  
||Efterfrågan|Försäljning för 100 st på plats WEST|  
||Tillgång|Släppt produktionsorder (skapad med *funktionen Förs.orderplanering* för försäljning av 100 enheter)|  

 **På sidan Produktionsinställningar** anges fältet **Komponenter vid lagerställe** till *ÖST.*

Följande orderspårningstransaktioner finns i tabellen Reservationstransaktion *baserat* på data i tabellen.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Reservationstransaktioner**

|Transaktionsnr|Positivt|Art.nr|Platskod|Kvantitet|Reservationsstatus|Description|Partinummer|Källtyp|Ursprungs-ID|Bindning|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENT|ÖSTRA|-70|Spårning|Komponent|-|5407|101004|-|
|8|Ja|KOMPONENT|ÖSTRA|70|Spårning|Komponent|LOTB|32|-|-| 
|9|-|KOMPONENT|ÖSTRA|-30|Spårning|Komponent|-|5407|1001004|-| 
|9|Ja|KOMPONENT|ÖSTRA|30|Spårning|Komponent|LOTA|32|-|-| 
|10|-|PRODUCERAD ARTIKEL|VÄSTRA|-100|Reservation|Producerad artikel|-|37|1001|Order-till-Order|
|10|Ja|PRODUCERAD ARTIKEL|VÄSTRA|100|Reservation|Producerad artikel|-|5406|101004|Order-till-Order|


#### <a name="entry-numbers-8-and-9"></a>Löpnummer 8 och 9

För komponentbehovet för LOTA respektive LOTB skapas orderspårningslänkar från efterfrågan i tabell 5407, *Prod.orderkomponent*, till leveransen i tabell 32, *Artikeltransaktion*. Fältet **Reservationsstatus** innehåller *spårning* för att ange att dessa transaktioner är dynamiska orderspårningslänkar mellan tillgång och efterfrågan.  

> [!NOTE]  
> Fältet **Partinr** är tomt på behovsraderna, eftersom partinumren inte har specificerats på komponentraderna för den släppta produktionsordern.  

#### <a name="entry-number-10"></a>Löpnummer 10

Från försäljningsbehovet i tabell 37, *Försäljningsrader*, skapas en orderspårningslänk till tillgången i tabell 5406, *Prod.orderrad*. Fältet **Reservationsstatus** innehåller *Reservation* och fältet **Bindning** innehåller *Order-till-order*. Detta beror på att den släppta produktionsordern genererades specifikt för försäljningsordern och måste förbli länkad till skillnad från orderspårningslänkar med reservationsstatusen Spårning, som skapas och ändras dynamiskt. Mer information finns i avsnittet Automatiska bokningar [i den](#automatic-reservations) här artikeln.  

 I det här skedet i scenariot överförs de 100 enheterna av LOTA och LOTB till lagerstället WEST genom en överföringsorder.  

> [!NOTE]  
> Endast överföringsorderleveransen bokförs i det här läget, inte inleveransen.  

 Nu finns följande orderspårningstransaktioner i tabellen *Reservationstransaktion* .  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Reservationstransaktioner**

|Transaktionsnr|Positivt|Art.nr|Platskod|Kvantitet|Reservationsstatus|Description|Partinummer|Källtyp|Ursprungs-ID|Bindning|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|KOMPONENT|ÖSTRA|-30|Överskott|Komponent|-|5407|1001004|-| 
|10|-|PRODUCERAD ARTIKEL|VÄSTRA|-100|Reservation|Producerad artikel|-|37|1001|Order-till-Order|
|10|Ja|PRODUCERAD ARTIKEL|VÄSTRA|100|Reservation|Producerad artikel|-|5406|101004|Order-till-Order|
|12|Ja|KOMPONENT|VÄSTRA|70|Överskott|Komponent|LOTB|5741|1011|-| 
|14|Ja|KOMPONENT|VÄSTRA|30|Överskott|Komponent|LOTA|5741|1011|-| 
|15|Ja|KOMPONENT|UT. LOGG.|70|Överskott|Komponent|LOTB|32|-|-| 
|16|Ja|KOMPONENT|UT. LOGG.|30|Överskott|Komponent|LOTA|32|-|-| 

#### <a name="entry-numbers-8-and-9-1"></a>Löpnummer 8 och 9

Orderspårningstransaktioner för de två partierna av komponenten som återspeglar efterfrågan i tabell 5407 ändras från reservationsstatusen *Spårning* till *Överskott*. Anledningen är att tillgång som de var kopplade till tidigare, i tabell 32, har använts av utleveransen på överföringsordern.  

Äkta överskott, som i det här fallet, återspeglar överskjutande tillgång eller efterfrågan som inte har spårats. Det är en indikation på obalans i ordernätverket, som genererar ett åtgärdsmeddelande från planeringssystemet om det inte löses dynamiskt.  

#### <a name="entry-numbers-12-to-16"></a>Löpnummer 12 till 16

Eftersom komponentens två partier bokförs på överföringsordern som levererade men inte inlevererade, är alla relaterade positiva orderspårningstransaktioner av reservationstypen *Surplus*, vilket indikerar att de inte allokeras till några krav. För varje partinummer avser en transaktion tabell 5741, *Överföringsrad*, och en transaktion avser artikeltransaktionen på den transitplats där artiklarna nu finns.  

I det här läget i scenariot bokförs överföringsordern för komponenterna från *ÖST* till *VÄST* som inlevererad.  

Nu finns följande orderspårningstransaktioner i tabellen *Reservationstransaktion* .  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Reservationstransaktioner**

|Transaktionsnr|Positivt|Art.nr|Platskod|Kvantitet|Reservationsstatus|Description|Partinummer|Källtyp|Ursprungs-ID|Bindning|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENT|ÖSTRA|-70|Överskott|Komponent|-|5407|101004|-| 
|9|-|KOMPONENT|ÖSTRA|-30|Överskott|Komponent|-|5407|1001004|-|
|10|-|PRODUCERAD ARTIKEL|VÄSTRA|-100|Reservation|Producerad artikel|-|37|1001|Order-till-Order|
|10|Ja|PRODUCERAD ARTIKEL|VÄSTRA|100|Reservation|Producerad artikel|-|5406|101004|Order-till-Order|
|17|Ja|KOMPONENT|VÄSTRA|70|Överskott|Komponent|LOTB|32|-|-| 
|18|Ja|KOMPONENT|VÄSTRA|30|Överskott|Komponent|LOTA|32|-|-| 

Orderspårningstransaktionerna liknar nu den första punkten i scenariot, innan överföringsordern bokfördes som endast levererad, förutom att transaktionerna för komponenten nu har reservationsstatusen *Överskott*. Detta beror på att komponentbehovet fortfarande finns på *lagerstället ÖST*, vilket återspeglar att **fältet Lagerställekod** på produktionsorderkomponentraden innehåller *ÖST* som inställningarna i **fältet Komponenter vid lagerställe** . Den tillgång som tidigare allokerades till det här behovet har överförts till *lagerstället VÄST* och kan nu inte spåras helt om inte komponentbehovet på produktionsorderraden ändras till *lagerstället VÄST* .  

I det här läget i scenariot **har lagerställekoden** på produktionsorderkomponentraden värdet *VÄST.* På sidan Artikelspårningsrader **tilldelas dessutom** 30 enheter av LOTA och 70 enheter av LOTB till produktionsorderkomponentraden.  

Nu finns följande orderspårningstransaktioner i tabellen *Reservationstransaktion* .  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Reservationstransaktioner**

|Transaktionsnr|Positivt|Art.nr|Platskod|Kvantitet|Reservationsstatus|Description|Partinummer|Källtyp|Ursprungs-ID|Bindning|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|PRODUCERAD ARTIKEL|VÄSTRA|-100|Reservation|Producerad artikel|-|37|1001|Order-till-Order|
|10|Ja|PRODUCERAD ARTIKEL|VÄSTRA|100|Reservation|Producerad artikel|-|5406|101004|Order-till-Order|
|21|-|KOMPONENT|VÄSTRA|-70|Spårning|Komponent|LOTB|5407|101004|-| 
|21|Ja|KOMPONENT|VÄSTRA|70|Spårning|Komponent|LOTB|32|-|-| 
|22|-|KOMPONENT|VÄSTRA|-30|Spårning|Komponent|LOTA|5407|1001004|-| 
|22|Ja|KOMPONENT|VÄSTRA|30|Spårning|Komponent|LOTA|32|-|-| 

#### <a name="entry-numbers-21-and-22"></a>Löpnummer 21 och 22

Eftersom komponentbehovet har ändrats till *lagerstället VÄST* och tillgången är tillgänglig som artikeltransaktioner på *lagerstället VÄST*, spåras nu alla orderspårningstransaktioner för de två partinumren fullständigt, vilket indikeras av reservationsstatusen *Spårning*.  

Fältet **Partinr** fylls nu på i orderspårningstransaktionen för tabell 5407, eftersom partinummer har tilldelats produktionsorderkomponentraderna.  

## <a name="action-messaging"></a>Åtgärdsmeddelanden

När orderspårningsystemet identifierar en obalans i ordernätverket skapar det automatiskt ett åtgärdsmeddelande för att meddela användaren. Åtgärdsmeddelanden är systemgenererade uppmaningar till användaren som anger detaljerna för obalansen och förslag på hur du återställer balansen i ordernätverket. De visas som planeringsrader på sidan **Planeringsförslag** när du väljer **åtgärden Hämta åtgärdsmeddelanden** . Dessutom visas åtgärdsmeddelanden på planeringsrader som skapas genom planeringskörningen för att återspegla planeringssystemets förslag på hur du återställer balansen i ordernätverket. I båda fallen körs förslagen i ordernätverket när du väljer **åtgärden Verkställ åtgärdsmeddelande** .  

Ett åtgärdsmeddelande gäller en strukturnivå åt gången. Om användaren acceptera åtgärdsmeddelandet, kan det ge upphov till ytterligare åtgärdsmeddelanden på nästa strukturnivå.  

Följande tabell visar de åtgärdsmeddelanden som finns.  

|Åtgärdsmeddelande|Description|  
|--------------------|---------------------------------------|  
|**Ändra antal**|Ändrar antalet på en befintlig leveransorder för att täcka en ny eller ändrad efterfrågan.|  
|**Omplanera**|Omplanerar förfallodatum på en befintlig order.|  
|**Omplanera & ändra antal**|Omplanerar förfallodatum och ändrar antalet på en befintlig order.|  
|**Ny**|Skapar en ny order om behovet inte kan uppfyllas av något av de tidigare åtgärdsmeddelandena.|  
|**Annullera**|Annullerar en befintlig order.|  

Orderspårningsystemet försöker alltid att lösa obalans i det befintliga ordernätverket. Om detta inte är möjligt skickas ett åtgärdsmeddelande för att skapa en ny order. Följande är den prioriterade listan som orderspårningssystemet använder när det fastställer saldot återställs. Om ytterligare efterfrågan har angett i beställningsnätverket försöker systemet att orderspåra genom följande kontroller:  

1. Kontrollera om det finns överskjutande tillgång i den befintliga orderspårningposten för den här efterfrågan.  
2. Kontrollera om det finns planerade och planenliga inleveranser i ordning efter inleveransdatum. Det senast möjliga datumet väljs.  
3. Kontrollera om det finns tillgängliga material.  
4. Kontrollera om en leveransorder finns i den aktuella orderspårningposten. I så fall skickas ett åtgärdsmeddelande av typen *Ändra* för att öka ordern.  
5. Kontrollera att ingen leveransorder finns i den aktuella orderspårningposten. I så fall skickas ett åtgärdsmeddelande av typen *Ny* för att skapa en ny order.  

En öppen efterfrågan går genom listan och påverkar den tillgängliga tillgången vid varje tidpunkt. All återstående efterfrågan täcks alltid av kontroll 4 eller 5.  

Om en minskning av efterfrågan inträffar försöker orderspårningsystemet att lösa obalansen genom att utföra föregående kontroller i omvänd ordning. Detta innebär att befintliga åtgärdsmeddelanden kan ändras eller tas bort, om det behövs. Orderspårningsystemet visar alltid nettoresultatet från beräkningar för användaren.  

## <a name="order-tracking-and-planning"></a>Orderspårning och planering

När planeringssystemet körs tar det bort alla befintliga orderspårningposter och åtgärdsmeddelandeposter och återskapar dem som planeringsradförslag enligt par med tillgång/efterfrågan och prioriteringar. När planläggningskörningen har avslutats har ordernätverket balanserats.  

### <a name="planning-system-versus-order-tracking-and-action-messaging"></a>Planeringssystemet kontra orderspårning och åtgärdsmeddelanden

 Följande jämförelse visar skillnaderna mellan metoder som används i planeringssystemet för att skapa planeringsradförslag och metoderna som används av orderspårningsystemet för att skapa orderspårningsposter och åtgärdsmeddelanden.  

- Planeringssystemet hanterar hela tillgångs- och efterfråganmönstret för en viss artikel, medan orderspårning hanterar ordern som aktiverade den.  

- Planeringssystemet hanterar alla nivåer av strukturhierarkin, medan orderspårning hanterar en struktur åt gången.  

- Planeringssystemet skapar länkar mellan efterfrågan och tillgång enligt det prioriterade förfallodatumet. Orderspårning skapa länkar mellan efterfrågan och tillgång enligt ordertransaktionssekvensen.  

- Planeringssystemet tar hänsyn till planeringsparametrar, medan orderspårning inte gör det.  

- Planeringssystemet skapar kopplingar i ett användaraktiverat batchläge när det balanserar tillgång och efterfrågan, medan orderspårning skapar länkarna automatiskt och dynamiskt när användaren anger order.  

## <a name="see-also"></a>Se även

[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
