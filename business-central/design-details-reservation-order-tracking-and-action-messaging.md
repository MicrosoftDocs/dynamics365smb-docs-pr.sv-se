---
title: 'Designdetaljer – Reservation, orderspårning och åtgärdsmeddelanden | Microsoft Docs'
description: Reservationsystemet är omfattande och innehåller de korrelativa och parallella funktionerna i orderspårning och åtgärdsmeddelanden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-reservation-order-tracking-and-action-messaging"></a>Designdetaljer: Reservation orderspårning och åtgärdsmeddelanden

Reservationsystemet är omfattande och innehåller de korrelativa och parallella funktionerna i orderspårning och åtgärdsmeddelanden.  

I kärnan av reservationsystemet finns kopplingen mellan en efterfråganspost och en motsvarande tillgångspost, antingen via reservation eller orderspårning. En reservation är användargenererad koppling, och en orderspårningpost är systemgenererad koppling. Ett artikelantal som anges i reservationsystemet kan antingen reserveras eller orderspåras, men inte båda på samma gång. Hur systemen hanterar en artikel beror på hur artikeln har ställts in.  

Reservationsystemet kommunicerar med planeringssystemet genom att skapa åtgärdsmeddelanden på planeringsrader under planeringskörningar. Ett åtgärdsmeddelande kan ses som en bilaga till en orderspårningpost. Åtgärdsmeddelanden, oavsett om de skapas dynamiskt i orderspårning eller under planeringskörningen, ger ett praktiskt verktyg för effektiv leveransplanering.  

> [!NOTE]  
> Det reserverade antalet ignoreras av planeringssystemet, det vill säga, den fasta länken mellan tillgång och efterfrågan kan inte ändra via planering.  

 Reservationsystemet utgör även strukturella grunden för artikelspårningsystemet. Mer information finns i [Designdetaljer: Artikelspårning](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="reservation"></a>Reservation

 En reservation är en fast koppling som ansluter en viss efterfrågan och tillgång till varandra. Den här länken påverkar direkt den efterföljande lagertransaktionen och säkerställer rätt koppling av artikeltransaktioner för kostnadsskäl. En reservation åsidosätter standardvärderingsprincipen för en artikel. Mer information finns i [Designdetaljer: Artikelspårning](design-details-item-tracking.md).  

 Sidan **Reservation** kan nås från alla orderrader av både tillgångs- och efterfråganstyp. På den här sidan kan du ange vilka efterfråganstransaktioner eller tillgångstransaktioner att skapa en reservationslänk till. Reservationen består av ett par poster som har samma löpnummer. En post har ett negativt tecken och pekar på efterfrågan. Den andra posten har ett plustecken och pekar mot tillgången. Dessa transaktioner lagras i tabellen **Reservationstransaktion** med statusvärdet **Reservation**. Användaren kan visa alla reservationer på sidan **Reservationstransaktioner**.  

### <a name="offsetting-in-reservations"></a>Motkontering i reservationer

 Reservationer görs mot tillgängligt antal artiklar. Artikeldispositionen beräknas i grundläggande villkor enligt följande:  

 disponibelt antal = lager + planenliga inleveranser – bruttobehov  

 Följande tabell visar detaljerna för ordernätverksenheterna som ingår i dispositionsberäkningen.  

||Fält i T27|Källtabell|Tabellfilter|Källfält|  
|-|------------------|------------------|------------------|------------------|  
|**Lager**|Lager|Artikeltransaktion|Inte tillämpligt|Antal|  
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

När en användare med vilje skapar en reservation får användaren fullständig äganderätt och ansvar för dessa artiklar. Det betyder att användaren också måste ändra numret manuellt eller annullera en reservation. Sådana manuella ändringar kan leda till automatisk ändring av de berörda reservationerna.  

Följande tabell visar när och vilka ändringar som kan uppstå:  

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

 Dessutom reserveras artiklar automatiskt av olika planeringsfunktioner för att hålla ett behov kopplat till en viss tillgång. Orderspårningposterna för sådana planeringslänkar innehåller **Reservation** i fältet **Reservationsstatus** i tabellen **Reservationstransaktion**. Automatiska reservationer skapas i följande situationer:  

- En produktionsorder med flera nivåer där fältet **Produktionsprincip** för de berörda överordnade och underordnade artiklarna anges till **Tillverka-Mot-Order**. Planeringssystemet skapar reservationer mellan överordnad produktionsorder och underliggande produktionsorder för att se till att de behandlas tillsammans. Sådan reservationsbindning åsidosätter artikelns standardmetod för värdering och koppling.  

- En produktion, en montering eller inköpsorder där fältet **Partiformningsmetod** för den berörda artikeln anges till **Inköpsorder**. Planeringssystemet skapar reservationer mellan efterfrågan och den planerade tillgången för att se till att den aktuella tillgången skapas. För mer information, se [Order](design-details-handling-reordering-policies.md#order).  

- En produktionsorder som skapats från en försäljningsorder med funktionen **Försäljningsorderplanering** länkas till försäljningsordern med en automatisk reservation.  

- En monteringsorder skapas automatiskt för en försäljningsorderrad för att uppfylla antalet i fältet **($ T_37_900 Qty. to Assemble to Order $)**. Den automatiska reservationen länkar försäljningsbegäran och monteringtillförseln, så att försäljningsorderhandläggare kan anpassa och lova monteringsartikeln direkt till kunden. Dessutom länkar reservationen monteringsutflöde på försäljningsorderraden till utleveransaktiviteten som uppfyller kundordern.  

Om det gäller tillgång eller efterfrågan som inte har fördelats tilldelar planeringssystemet automatiskt en reservationsstatus av typen **Överskott**. Detta kan bero på en efterfrågan på grund av ett prognostiserat antal eller användarangivna planeringsparametrar. Det är legitimt överskott som programmet känner igen, och det ger inte upphov till åtgärdsmeddelanden. Överskott kan också vara äkta, överflödig tillgång eller efterfrågan som inte har spårats. Detta är en indikation på obalans i ordernätverket som gör att systemet skickar åtgärdsmeddelanden. Observera att ett åtgärdsmeddelande som föreslår en ändring i antal alltid refererar till typen **Överskott**. Mer information finns i avsnittet "Exempel: Orderspårning inom försäljning, produktion och överföring" i detta ämne.  

Automatiska reservationer som upprättas under planeringskörningen hanteras på följande sätt:  

- De kopplas mot artikelantal som ingår i dispositionsberäkningarna, liksom manuella reservationer. Mer information finns i avsnittet “Motkonteringar i reservationer” i detta ämne.  

- De tas med och ändras eventuellt i följande planeringskörningar, i motsats till manuellt reserverade artiklar.  

## <a name="order-tracking"></a>Orderspårning

Orderspårning hjälper planeraren att upprätthålla en giltigt leveransplan genom att visa en översikt över motkontering mellan efterfrågan och tillgång i ordernätverket. Orderspårningposterna fungerar som grund för att skapa dynamiska åtgärdsmeddelanden och planeringsradförslag vid planeringskörningar.  

> [!NOTE]  
> Orderspårningssystemet avräknar det disponibla materialet när order anges i ordernätverket. Det betyder att systemet inte prioriterar order som kan vara mer brådskande i termer av förfallodatum. Det är därför upp till logiken för planeringssystemet eller visheten hos planeraren att ordna om prioriteringarna på ett meningsfullt sätt.  

> [!NOTE]  
> Orderspårningsprincipen och funktionen Hämta åtgärdsmeddelanden är inte integrerade med projekt. Det betyder att efterfrågan som hör till ett projekt inte spåras automatiskt. Eftersom den inte spåras kan det orsaka att användningen av en befintlig återanskaffning med projektinformation spåras för en annan efterfrågan, till exempel en försäljningsorder. Du kan därför hamna i en situation där din information om disponibelt lager inte är synkroniserad.  

### <a name="the-order-network"></a>Ordernätverket

Orderspårningsystemet baseras på principen att ordernätverket alltid måste vara i ett balanserat tillstånd där varje efterfrågan som kommer in i systemet räknas av mot en motsvarande tillgång och vice versa. Systemet gör det genom att identifiera logiska länkar mellan alla efterfrågans- och tillgångstransaktioner i ordernätverket.  

Principen betyder att en ändring i efterfrågan leder till motsvarande obalans på tillgångssidan av ordernätverket. En ändring i tillgång leder till en motsvarande obalans på efterfråganssidan av ordernätverket. I verkligheten är ordernätverket i ett tillstånd av konstant förändring när användare anger, ändrar och tar bort beställningar. Orderspårningsprocesser beställer dynamiskt och reagerar på varje ändring vid den tidpunkt då den kommer in i systemet och blir en del av ordernätverket. Så snart som nya orderspårningposter skapas, är ordernätverket balanserat, men endast tills nästa ändring inträffar.  

Om du vill öka översikten över beräkningar i planeringssystemet visar sidan **Ej spårade planeringselement** antal som inte spårats, och som representerar skillnaden i antal mellan det kända behovet och den föreslagna tillförseln. Varje rad på sidan refererar till orsaken för överskottsantalet, till exempel **Avropsorder**, **Säkerhetslagernivå**, **Fast orderkvantitet**, **Min. partistorlek**, **Avrundning**eller **Dämpare**.  

### <a name="offsetting-in-order-tracking"></a>Motkontering i orderspårning

I motsats till reservationer, som kan bara utföras mot tillgängliga artikelantal, är orderspårning möjlig mot alla ordernätverksenheter som ingår i beräkningen av nettobehov i planeringssystemet. Nettobehoven beräknas enligt följande:  

*nettobehoven = bruttobehov + beställningspunkt – planenliga inleveranser – planerade inleveranser – planerat tillgängligt saldo  

> [!NOTE]  
> Efterfrågan som är kopplad till prognoser eller planeringsparametrar inte är orderspårad.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a>Exempel: Orderspårning i försäljningar, produktion och överföringar

Följande scenario visar vilka orderspårningstransaktioner som skapas i tabellen **Reservationstransaktion** som resultat av olika ändringar i ordernätverket.  

Anta att följande data finns för två artiklar som har angetts för orderspårning.  

|Artikel 1|Name|"Komponent"|
|-|-|-|
||Disposition|100 enheter i lagerställe VÄST<br /><br />- 30 enheter av LOTA<br />- 70 enheter av LOTB|  
|Artikel 2|Name|“Producerad artikel”|
||Prod.struktur|1 ant. av "Komponent”|  
||Behov|Försäljning av 100 enheter på lagerställe ÖST|  
||Tillgång|Släppta produktionsorder (som skapas med funktionen **Försäljningsorderplanering** för försäljningen av 100 enheter)|  

På sidan **Produktionsinställningar** har fältet **Komp. vid lagerställe** värdet **RÖD**.

Följande orderspårningstransaktioner finns i tabellen **Reservationstransaktion** baserat på data i tabellen.  

 ![Första exempel på orderspårningstransaktioner i registret Reservationstransaktion.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### <a name="entry-numbers-8-and-9"></a>Löpnummer 8 och 9

För komponentbehovet för PARTIA och PARTIB skapas orderspårningslänkar från efterfrågan i tabell 5407, **Prod.orderkomponent** till tillgången i tabell 32, **Artikeltransaktion**. Fältet **Reservationsstatus** innehåller **Spårning** för att ange att dessa transaktioner är dynamiska orderspårninglänkar mellan tillgång och efterfrågan.  

> [!NOTE]  
> Fältet **Partinr** är tomt på behovsraderna, eftersom partinumren inte har specificerats på komponentraderna för den släppta produktionsordern.  

### <a name="entry-number-10"></a>Löpnummer 10

Från försäljningsbegäran i tabell 37, **Försäljningsrad**, skapas en orderspårningslänk till leveransen i tabell 5406, **Prod.orderrad**. Fältet **Reservationsstatus** innehåller **Reservation** och fältet **Bindning** innehåller **Order-till-order**. Det beror på att den släppta produktionsordern genererats specifikt för försäljningsordern och måste förbli kopplad, till skillnad från orderspårninglänkar med reservationsstatusen **Spårning**, som skapas och ändras dynamiskt. Mer information finns i avsnittet “Automatiska reservationer” i detta ämne.  

 I det här skedet av scenariet överförs de 100 enheterna i PARTIA och PARTIB till lagerställe ÖST genom en överföringsorder.  

> [!NOTE]  
> Endast överföringsorderleveransen bokförs i det här läget, inte inleveransen.  

 Nu finns följande orderspårningsposter i tabellen **Reservationstransaktion**.  

 ![Andra exempel på orderspårningstransaktioner i registret Reservationstransaktion.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### <a name="entry-numbers-8-and-9-1"></a>Löpnummer 8 och 9

Orderspårningstransaktioner för de två partierna av komponenten visar att efterfrågan i tabell 5407 ändras från reservationsstatusen **Spårning** till **Överskott**. Anledningen är att tillgång som de var kopplade till tidigare, i tabell 32, har använts av utleveransen på överföringsordern.  

Äkta överskott, som i det här fallet, återspeglar överskjutande tillgång eller efterfrågan som inte har spårats. Det är en indikation på obalansen i ordernätverket som skapar ett åtgärdsmeddelande från planeringssystemet såvida det inte löses dynamiskt.  

### <a name="entry-numbers-12-to-16"></a>Löpnummer 12 till 16

Eftersom de två partierna för komponenten bokförs på överföringsordern som levererade men inte inlevererade, är alla relaterade positiva orderspårningstransaktioner av reservationstypen **Överskott**, vilket anger att de inte är kopplade till några behov. För varje partinummer är en transaktion knuten till tabell 5741, **Överföringsrad**, och en transaktion är knuten till artikeltransaktionen på transitlagerstället där artiklarna finns nu.  

I det här skedet av scenariet bokförs överföringsordern för komponenterna från lagerställe ÖST till VÄST som inlevererad.  

Nu finns följande orderspårningsposter i registret **Reservationstransaktion**.  

 ![Tredje exempel på orderspårningstransaktioner i registret Reservationstransaktion.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

Orderspårningsposterna är nu liknande till den första punkten i scenariet, före överföringsordern har bokförts som endast utlevererad, förutom att transaktioner för komponenten nu har reservationstatus **Överskott**. Detta beror på att komponentbehovet fortfarande finns vid lagerställe VÄST och visar att fältet **Lagerställekod** på produktionsorderkomponentraden innehåller **VÄST** enligt inställt i konfigurationsfältet **Komponenter vid lagerställe**. Leveransen som har tilldelats detta behov har överförts till lagerställe ÖST och kan nu inte spåras fullständigt om inte komponentbehovet på produktionsorderraden ändras till lagerställe ÖST.  

I det här skedet i scenariet anges **Lagerställekod** på produktionsorderraden som **ÖST**. På sidan **Artikelspårningsrader** tilldelas dessutom de 30 enheterna i PARTIA och de 70 enheterna i PARTIB till produktionsorderraden.  

Nu finns följande orderspårningsposter i registret **Reservationstransaktion**.  

 ![Fjärde exempel på orderspårningstransaktioner i registret Reservationstransaktion.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### <a name="entry-numbers-21-and-22"></a>Löpnummer 21 och 22

Eftersom komponentbehovet har ändrats till lagerställe ÖST och tillgången finns tillgänglig som artikeltransaktioner vid lagerställe ÖST, är alla orderspårningsposter för de två partinumren nu fullständigt spårade, vilket anges av reservationsstatusen **Spårning**.  

Fältet **Partinr** fylls nu på i orderspårningstransaktionen för tabell 5407, eftersom partinummer har tilldelats produktionsorderkomponentraderna.  

## <a name="action-messaging"></a>Åtgärdsmeddelanden

När orderspårningsystemet identifierar en obalans i ordernätverket skapar det automatiskt ett åtgärdsmeddelande för att meddela användaren. Åtgärdsmeddelanden är systemgenererade uppmaningar till användaren som anger detaljerna för obalansen och förslag på hur du återställer balansen i ordernätverket. De visas som planeringsrader på sidan **Planeringsförslag** när du väljer **Hämta åtgärdsmeddelanden**. Dessutom visas åtgärdsmeddelanden på planeringsrader som skapas genom planeringskörningen för att återspegla planeringssystemets förslag på hur du återställer balansen i ordernätverket. I båda fallen körs förslagen i ordernätverket när du väljer **Verkställ åtgärdsmeddelanden**.  

Ett åtgärdsmeddelande gäller en strukturnivå åt gången. Om användaren acceptera åtgärdsmeddelandet, kan det ge upphov till ytterligare åtgärdsmeddelanden på nästa strukturnivå.  

Följande tabell visar de åtgärdsmeddelanden som finns.  

|Åtgärdsmeddelande|Description|  
|--------------------|---------------------------------------|  
|**Ändra antal**|Ändrar antalet på en befintlig leveransorder för att täcka en ny eller ändrad efterfrågan.|  
|**Omplanera**|Omplanerar förfallodatum på en befintlig order.|  
|**Omplanera & ändra antal**|Omplanerar förfallodatum och ändrar antalet på en befintlig order.|  
|**Ny**|Skapar en ny order om efterfrågan inte kan uppfyllas av något av de föregående åtgärdsmeddelandena.|  
|**Annullera**|Annullerar en befintlig order.|  

Orderspårningsystemet försöker alltid att lösa obalans i det befintliga ordernätverket. Om det inte är möjligt skickas ett åtgärdsmeddelande för att skapa en ny order. Följande är den prioriterade listan som orderspårningssystemet använder när det fastställer saldot återställs. Om ytterligare efterfrågan har angett i beställningsnätverket försöker systemet att orderspåra genom följande kontroller:  

1. Kontrollera om det finns överskjutande tillgång i den befintliga orderspårningposten för den här efterfrågan.  
2. Kontrollera om det finns planerade och planenliga inleveranser i ordning efter inleveransdatum. Det senast möjliga datumet väljs.  
3. Kontrollera om det finns tillgängliga material.  
4. Kontrollera om en leveransorder finns i den aktuella orderspårningposten. I så fall skickas ett åtgärdsmeddelande av typen **Ändra** för att öka ordern.  
5. Kontrollera att ingen leveransorder finns i den aktuella orderspårningposten. I så fall skickas ett åtgärdsmeddelande av typen **Ny** för skapa en ny order.  

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
