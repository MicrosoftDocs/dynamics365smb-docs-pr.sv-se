---
title: Tabellen Reservationstransaktion - Funktioner som uppdaterar tabellen Reservationstransaktion | Microsoft Docs
description: Detta ger vägledning som hjälper dig att förstå och felsöka problem med inkonsekvens i data i tabellen Reservationstransaktion.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Tabellen Reservationstransaktion - Introduktion

Det här tekniska faktabladet innehåller vägledning som hjälper dig att förstå och felsöka problem med datainkonsekvens i tabellen *Reservationstransaktion* (tabell 337) i Microsoft Dynamics NAV. Den första delen är en introduktion till de funktioner som genererar eller ändrar data i den här tabellen. Den täcker också flera fält i tabellen Reservationstransaktion *som* är värda att påpeka i samband med dessa funktioner. Den andra delen visar med exempel hur transaktioner i *tabellen Reservationstransaktion* genereras, tas bort eller ändras när överföringsorder bearbetas eller planeringsfunktioner körs.

Tabellen *Reservationstransaktion* används för att hantera och lagra information om reservationer, artikelspårning och orderspårning.

När du hanterar artikelspårning med partiell bokföring fungerar tabellen tillsammans med *tabellen Spårningsspecifikation* (tabell 336). Data som användaren anger på **sidan Artikelspårningsrader** skapas i en tillfällig version av tabell 336 och överförs till tabell 337 och spårningsspecifikationstabellen när sidan stängs.

Generellt sett beror de data som genereras i tabellen Reservationstransaktion *på* vilka funktioner du använder och vilka parametrar du har valt för artikeln kort. Dessa inkluderar:

- Policy för orderspårning
- Policy för bokning
- Planeringsfunktioner utförda
- Beställnings- och tillverkningspolicy
- Planeringsparametrar för artikeln eller lagerställeenheten kort
- Artikelspårningskod

## Funktioner som uppdaterar tabellen Reservationstransaktion

### Policy för orderspårning

 **Om fältet Orderspårningsprincip** för en artikel är inställt på Ingen, Microsoft Dynamics NAV  skapas aldrig reservationstransaktioner i *tabellen Reservationstransaktion*, såvida inte nettoförändringsplanen eller den generativa planen, reservationen eller artikelspårningen utförs. Utan att orderspårning är aktiverad kan du dessutom ha reservationstransaktioner när du använder policyerna Manufacturing-to-Order eller Assembly-to-Order.

Du kan överväga att ange **orderspårningsprincipen** till Ingen om du inte behöver spåra en efterfrågan direkt mot en tillgång eller vice versa. Spårning av tillgång mot ett behov hanteras av orderspårningsfunktionen eller planeringsmotorn. Vi rekommenderar inte att du använder orderspårning tillsammans med planeringsfunktioner.

När du anger **fältet Orderspårningsprincip** till Endast Microsoft Dynamics NAV  spårning skapas alltid transaktioner i tabell 337 när en order skapas för artikeln, men reservationsstatusen **i** tabell 337 är inte alltid strikt inställd på Spårning. Tänk dig följande scenario:

> [!NOTE]  
> Arbetsdatumet är satt till 2014-01-23 (MM/DD/ÅÅÅÅ) för alla exempel. 
  
1. Skapa en artikel med **fältet Orderspårningsprincip** inställt på Endast spårning.  
1. Skapa en inköpsorder. Microsoft Dynamics NAV skapar en reservationstransaktion med reservationsstatusen **Överskott**, eftersom inköpsordern ännu inte har allokerats till ett behov.
1. Skapa en försäljningsorder. Microsoft Dynamics NAV skapar nu ytterligare en reservationstransaktion med reservationsstatusen **Spårning**.

 **Reservationsstatusen** som skapades i steg 2 uppdateras till Spårning, den hanteras Microsoft Dynamics NAV automatiskt. Detta koncept kallas dynamisk spårning.
Genom att ange **fältet Orderspårningsprincip** för artikeln till Endast spårning kan en slutanvändare använda orderspårningsfunktionen för att få en översikt över vilken tillgång behovet fördelas till och vice versa.

> [!NOTE]  
> Spårningsfunktionen ersätter inte planeringsfunktionen, som tar hänsyn till alla artiklar, behov och leveranser tillsammans för att ge optimala planeringsförslag för att optimera kundservicenivåer och balansera lagernivåer.

### Policy för bokning

En reservation består av ett par poster i tabellen Reservationstransaktion *med* reservationsstatusen **Reservation**, som delar samma postnummer. En post har fältet Positiv aktiverat och pekar på tillgången. Den andra posten har fältet **Positiv** inte aktiverat och pekar på efterfrågan. Fälten **Ursprungstyp**, **Källref.nr** och **Käll-ID** markerar reservationslänken mellan tillgång och efterfrågan.

Informationen i fältet **Ursprungstyp** är tabellen reservationslöpnr **.** är relaterat till. Om det till exempel är en behovstransaktion (negativ) kan det vara *tabellen Förs.order* (tabell 37) eller *planeringskomponenten*  (tabell 99000829).

Fältet Käll-ID **innehåller** ID:t för dokumentet i tabellen som refereras av Källtyp.

Källans **ref.nr.** Innehåller ett referensnummer för raden, som reservationslöpnr **.** är relaterad till. Om transaktionen är kopplad till en försäljningsrad, inköpsrad, journalrad eller rekvisitionsrad kopieras informationen i det här fältet från radnumret **.** . Om informationen i det *här fältet är relaterad till en transaktion i tabellen Artikeltransaktion* (tabell 32) kopieras den från **transaktionsnumret.** i *tabellen Artikeltransaktion* .

När du använder reservationsvillkorsalternativet Alltid i kombination med orderspårning är båda normalt synkroniserade. När reservationen tas bort eller när inleveransdatumet flyttas fram efter förfallodatumet för efterfrågan tas orderspårningen bort. Du kan också stöta på ett felmeddelande där Microsoft Dynamics NAV du får frågan vad du ska göra med befintliga reservationer. Det här scenariot illustreras i följande exempel:

1. Skapa ett nytt objekt med namnet COMP. Ange följande fält:
  - **Återanskaffningssystem**: Inköp
  - **Orderspårningspolicy**: Endast spårning
  - **Boka**: Alltid
2. Skapa ett andra objekt med namnet FG. Ange följande fält:
  - **Återanskaffningssystem**: Prod.order
  - **Orderspårningspolicy**: Endast spårning
  - **Boka**: Alltid
3. Skapa ett andra objekt med namnet FG. Ange följande fält:
  - **Artikel**: COMP
  - **Antal per**: 1
4. Certifiera produktionsstrukturns nummer. BOM FG och tilldela mot Artikel FG.
5. Skapa en inköpsorder. Ange följande fält:
  - **Artikel**: COMP
  - **Kvantitet**: 10
  - **Lagerställekod**: BLÅ
  - **Förväntat inleveransdatum**: 01/24/2014
6. Skapa en försäljningsorder. Ange följande fält:
  - **Leveransdatum**: 02/14/2014
  - **Lagerställekod**: BLÅ
  - **Artikel**: COMP
  - **Kvantitet**: 10

> [!NOTE]  
> Automatisk reservation har utförts mellan inköps- och försäljningsordern. Dessutom har orderspårning skapats mellan inköps- och försäljningsorder.

7. Skapa en manuellt släppt produktionsorder. Ange följande fält:
  - **Artikel**: 2014-02-14
  - **Kvantitet**: 10
  - **Plats**: BLÅ
  - **Förfallodatum**: 02/01/2014
8.  **På fliken Start** i gruppen Process väljer du **Uppdatera produktionsorder**.
9. Öppna komponentlistan och leta upp Artikelkomposition.

> [!NOTE]  
> Ingen reservations- eller orderspårning skapas av Microsoft Dynamics NAV. Anledningen är att det redan finns en reservation mot försäljningsordern som skapades i steg 6.

Antag att artikeln på grund av affärsskäl behövs mer brådskande på den släppta produktionsordern som skapades i steg 7. Så i följande steg annullerar vi reservationen från försäljningsordern som skapades i steg 6 och märker hur orderspårning hanteras.

10. Sök efter försäljningsordern för artikel-COMP från den 6 steg och annullera reservationen.
11. Öppna inköpsordern från steg 5 och lägg märke till att orderspårning nu skapas mellan inköpsordern och den komponent som behövs från den släppta produktionsordern.
12. Återskapa reservationen mellan den komponent som behövs från den släppta produktionsordern och leveransen från inköpsordern i steg 5.

> [!NOTE]  
> Reservationen återskapas inte, vilket måste göras manuellt.

13. Ändra fältet **Förväntat inleveransdatum** i inköpsorderhuvudet vid 5 steg från 2014-01-24 till 2014-05-02.

Microsoft Dynamics NAV visar följande varningsmeddelande:

   Reservationer finns för denna order. Dessa reservationer annulleras om en datakonflikt orsakas av ändringen. Vill du fortsätta?

14. Välj Ja. Slå upp reservations- och orderspårningstransaktionerna från inköpsordern.

> [!NOTE]  
> Den befintliga reservationen annulleras och måste återskapas manuellt. Ordern är emellertid dynamisk och har återskapats genom Microsoft Dynamics NAV att finnas mellan inköpsordern och försäljningsordern. Anledningen är att efterfrågan på den släppta produktionsordern (2014-01-02) finns före leveransens förväntade inleveransdatum.

Detta avslutar demonstrationen av interaktionen mellan att använda automatiska reservationer och orderspårning. Exemplen visar också vad som händer när du ändrar förfallodatum och felmeddelandet som utlöses när Dit är en reservationskonflikt.

### Planering beräknad

Planering som görs med orderplanering, inköpsförslag eller planeringsförslag genererar transaktioner i *tabellen Reservationstransaktion* med **fältet Reservationsstatus** inställt på Spårning, Reservation eller Överskott. Dit ska alltid vara ett matchande par med samma löpnummer med positivt och negativt värde i **Antal (bas)** -fält när statusen är Spårning eller Reservation. Fältet Ursprungstyp **blir** behovstypen, d.v.s. tabell 37 för den negativa kvantiteten och en planeringstabell, till exempel tabell 246, för den positiva kvantiteten. Fältet Käll-ID **blir** PLANERING.

Om det gäller icke-fördelad tillgång eller efterfrågan Microsoft Dynamics NAV  anges fältet Reservationsstatus **till** Överskott. Du kan till exempel ha reservationsstatusen Överskott när det befintliga lagret är lägre än säkerhetslagret eller om efterfrågan är kopplad till prognosen.

Tabellen *Planeringselement* utan spårning (tabell 99000855) innehåller information om ej spårade kvantiteter som visas när användaren gör en sökning från orderspårningssidan för att se ej spårade kvantiteter eller väljer en varningsikon i planeringsförslaget. Tabellen innehåller poster som redogör för en överskottskvantitet i orderspårningsnätverket.

Dessa poster skapas under planeringen och förklarar var den ej spårade överskottskvantiteten på orderspårningsraderna kommer ifrån. Överskottet som inte har spårats kan komma från:

- Produktionsprognos
- Avropsorder
- Säkerhetslager
- Beställningspunkt
- Beställningsgräns
- Beställningsantal
- Max. partistorlek
- Min. partistorlek
- Partistorleksmultipel
- Dämpare (% partistorlek)

 *I tabellen Reservationstransaktion*, liksom på inköps-, överförings- och produktionsorder, är Dit ett **fält för planeringsflexibilitet** . I det här alternativfältet anges om leveransen som representeras av dessa leveransorder beaktas av planeringssystemet när åtgärdsmeddelanden beräknas. Om fältet innehåller alternativet Obegränsat, inkluderar planeringssystemet raden när åtgärdsmeddelanden beräknas. Om fältet innehåller alternativet Ingen är raden fast och går inte att ändra, och planeringssystemet inkluderar inte raden när åtgärdsmeddelanden beräknas. Funktionen hanteras i *tabellen Reservationstransaktion* av fältet med samma namn.

### Beställnings- och tillverkningspolicy

Om en planeringsfunktion körs för en artikel som angetts med Partiformningsprincipen inställd på Order, Microsoft Dynamics NAV  skapas transaktioner i *tabellen Reservationstransaktion* med reservationsstatusen Reservation i stället för Spårning.

Fälten Ursprungstyp **och** **Käll-ID** behandlas på samma sätt som andra partiformningsprinciper. I fältet **Bindning** i *tabellen Reservationstransaktion*  Microsoft Dynamics NAV  anges dock Order-till-order.

Fältet **Bindning** fylls i för att styra leveransorder som är bundna till en viss efterfrågan, till exempel produktionsorder som skapas direkt från en försäljningsorder. I fältet visas Order-till-order när transaktionen är knuten till en efterfrågan eller en leverans (Automatisk reservation). Behovet kan vara relaterat till försäljning eller komponentbehov.

### Artikelspårning och reservationstransaktion för potentiella kunder

Reservationsstatusen för potentiell kund kan skapas i Microsoft Dynamics NAV  *tabellen Reservationstransaktion* när du inte använder några ordernätverksentiteter, det vill säga orderspårning. På en förbrukningsjournalrad tilldelar du till exempel komponenten Artikelspårning. Om artikeln redan har orderspårats kan det Microsoft Dynamics NAV  dock skapa fler reservationstransaktioner för potentiella kunder. Detta visas i EXEMPEL 2 som rör överföringsorder i den andra delen av detta dokument.

När du visar eller ändrar **sidan Artikelspårningsrader** visas det samlade innehållet i tabellerna *Spårningsspecifikation* (tabell 336) och *Reservationstransaktion* i en tillfällig version av tabell 336. Detta säkerställer att historiska och aktiva artikelspårningsdata nås som en.

Reservationer kan delas in i två kategorier: Ospecifika reservationer, där parti- och serienummer inte anges vid bokningstillfället, och Specifika reservationer, där du reserverar specifika parti- eller serienummer från lagret.

Vid en ospecifik bokning visas **partinr.** eller **serienr.** är tomt i fältet **Löpnr.** i tabell 337 som pekar på efterfrågan (t.ex. försäljningen). På grund av reservationslogikens struktur i Microsoft Dynamics NAV måste du ändå Välj specifika artikeltransaktioner att reservera mot när du placerar en ospecifik reservation för en artikelspårad artikel i lagret Microsoft Dynamics NAV .

Eftersom artikeltransaktionerna innehåller artikelspårningsinformation reserveras indirekt specifika parti- eller serienummer, även om användaren inte avsåg detta. Men med sen bindning reserverar sig fortfarande mot specifika transaktioner, Microsoft Dynamics NAV  men använder sedan en omblandningsmekanism Microsoft Dynamics NAV vid bokföring.

Mer information finns i de Microsoft Dynamics NAV tekniska faktablad som anges i Ytterligare resurser i slutet av det här dokumentet.

### Fälten Källsubtyp, Undertryckt åtgärdsmeddelande, Justering av åtgärdsmeddelande och Tillåt inte annullering

Fälten Källsubtyp **,** Undertryckt åtgärdsmeddelande **,** Justering **av åtgärdsmeddelande och** Tillåt inte annullering **i tabellen Reservationstransaktion** beskrivs i det *här avsnittet* . Scenarier tillhandahålls för att demonstrera användningen av fälten **Undertryckt åtgärdsmeddelande**, **Justering** av åtgärdsmeddelande och **Tillåt inte annullering** . Fältet **Justering** av åtgärdsmeddelande används för orderspårningspolicyfunktionen Spårning och Åtgärdsmeddelande. Fältet **Tillåt inte annullering** används för funktionen Montering mot order under Microsoft Dynamics NAV 2013.

#### Ursprungssubtyp

I fältet Källundertyp **visas** vilken källundertyp reservationstransaktionen är relaterad till. Om transaktionen är kopplad till en inköpsrad eller försäljningsrad kopieras fältet från **fältet Dokumenttyp** på raden. Om den är relaterad till en journalrad kopieras fältet från **fältet Transaktionstyp** på journalraden.

#### Undertryckt åtgärdsmedd.

Den **undertryckta åtgärden msg.** Fältposter när en befintlig leverans redan har bearbetats delvis, till exempel när en inköpsorder redan har inlevererats delvis eller när förbrukning bokförts mot en produktionsorder.

När planeringen är utförd Microsoft Dynamics NAV  markerar du det här fältet och anger **fältet Reservationstransaktionsstatus** till *Överskott8. Följande exempel fungerar som en illustration:

1. Öppna artikel 80001. Ange följande fält:
  - **Partiformningspolicy**: Parti-för-parti
  - **Reservera**: Valfritt
  - **Orderspårningspolicy**: Ingen
2. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: 80001
  - **Plats**: Tom/Ingen
  - **Kvantitet**: 10
  - **Leveransdatum**: 2014-02-15
3.  **Öppna inköpsförslagen** och kör batch-jobbet **Beräkna plan** för artikel 80001.
  - **Tillträde**: 2014-01-23
  - **Slutdatum**: 03/01/2014
4. Ett planeringsförslag ges för att fylla på 10 med ny inköpsorder och **förfallodatum** 2014-02-15.
5.  **På fliken Åtgärder** i gruppen Funktioner väljer du **Verkställ åtgärdsmeddelande** för att skapa en inköpsorder med **förväntat inleveransdatum** 2014-02-15.
6. Öppna inköpsordern från 5 steg och ställ in **Inlevererat** antal till 2 och bokför endast Inleverans.
7. Öppna försäljningsordern från 2 steg och ändra **Utleveransdatum** till 2014-02-10.
8.  **Öppna inköpsförslagen** och kör **Beräkna plan** för artikel 80001
  - **Tillträde**: 2014-01-23
  - **Slutdatum**: 03/01/2014
9. Ett planeringsförslag ges för att fylla på 8 med ny inköpsorder och **förfallodatum** 2014-10-02.

Statusinformationen i tabell 337 visas i följande bild.

Transaktion nr 28 i tabell 337 har reservationsstatusen Spårning för att matcha det befintliga lagret som registrerats i artikeltransaktion 318 för 2 enheter och den utestående efterfrågan i tabellen Förs.order 37. Den efterföljande transaktionen nr 29 har också reservationsstatusen Spårning och länkar den återstående kvantiteten på 8 enheter mellan behovet i försäljningsordertabell 37 och den föreslagna leveransen i tabellen Rekvisitionsrad 246.

Transaktion nr 30 är den befintliga inköpsorder som delvis har inlevererats med kvantitet 2.  **Därför är fältet Reservationsstatus** Överskott och Microsoft Dynamics NAV anger **fältet Antal (bas)**  till *8*  (återstående saldo) och Undertryckt **åtgärdsmeddelande.** är aktiverat.

#### Åtgärdsmedd.justering

I **fältet Justering** av åtgärdsmeddelande visas den ändring på orderspårningssidan som uppstår när du accepterar relaterade åtgärdsmeddelanden. Ett värde visas bara Hit när funktionerna för både orderspårning och åtgärdsmeddelanden är aktiva (Orderspårningsprincip inställd på Spårning &; Åtgärdsmeddelande). Värdet beräknas baserat på data i *tabellen Åtgärdsmeddelandetransaktion* (tabell 99000849). Följande exempel fungerar som en illustration:
1. Öppna artikel 80002. Ange följande fält:
 - **Orderspårningsprincip**: Spårning och åtgärdsmeddelande
2. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: 80002
  - **Plats**: BLÅ
  - **Kvantitet**: 100
3. Öppna sidan **Orderplanering** och kör batch-jobbet **Beräkna plan** .
4. Välj försäljningsordern från 2 steg och kör batch-jobbet **Skapa order** .
5. På försäljningsordern från 2 steg ändrar du **fältet Antal** från 100 till 105.
Statusinformationen i tabell 337 visas i följande bild.
6. Transaktion nr 34 har fältet **Åtgärdsmeddelandejustering** i tabell 337 aktiverat för 5 enheter med reservationsstatus Surplus. Eftersom försäljningsordern ökades till 5 Microsoft Dynamics NAV  steg skapades den här reservationen eftersom mer tillgång krävs.
7. Öppna sidan **Planeringsförslag** och välj **Hämta åtgärdsmeddelanden i** gruppen **Process** på fliken **Start**. Microsoft Dynamics NAV föreslår att inköpsorderantalet ökas från 100 till 105.

#### Tillåt inte annullering

I **fältet Tillåt inte annullering** anges att reservationstransaktionen utgör länken mellan en försäljningsorderrad och en monteringsorder. Du kan inte ta bort den här reservationen eftersom den krävs för att upprätthålla synkroniseringen som sker när en artikel sätts ihop på beställning. Följande exempel fungerar som en illustration:

1. Skapa en inköpsorder. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Montering
  - **Monteringspolicy**: Montera på beställning
  - **Orderspårningspolicy**: Endast spårning
2. Skapa en ny artikel med namnet Montera COMP. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Inköp
  - **Orderspårningspolicy**: Endast spårning
3. Öppna artikeln Montera FG, välj Montering i **gruppen Montering/produktion** på fliken Analysera **och välj** sedan **Monteringsstruktur**. **·** Ange följande fält i monteringsstrukturen:
  - **Typ**: Artikel
  - **Nr**: Montera COMP
  - **Antal per**: 1 Välj OK **knapp**.
4. Öppna en artikeljournal och öka lagret för Assemble COMP till kvantitet 10 mot lagerställe BLÅ och bokför journalraden.
5. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: Montera FG
  - **Plats**: BLÅ
  - **Antal**: 1 Statusinformationen i tabell 337 visas i följande bild.

Transaktion nr 82 har reservationsstatusöverskott som 9 enheter av monteringskompet i lager och har ingen efterfrågan. Transaktion nr 84 spårar reservationstransaktioner mellan behovet i monteringsradtabell *901* och tillgången i artikeltransaktion 346.

Löpnr 86 har bindande order-till-order med reservationsstatusreservation. Dessutom är fältet **Tillåt inte annullering** aktiverat eftersom monteringsprincipen är inställd som Montera mot order för artikelmontering FG. Slutligen **anges fältet Planeringsflexibilitet** till Ingen, eftersom Microsoft Dynamics NAV planeringslogiken inte tillåter att reservationen tas bort.

#### Antal tillgängliga för plockning och reservation

Det **reserverade plock- och leveransantalet.** Fältet i tabell 337 som finns i versioner före Microsoft Dynamics NAV 2013 styr artikeltillgängligheten i ett hanterat lagerställe. I alla installationer av Microsoft Dynamics NAV lagerstyrning finns artikelkvantiteter både som lagertransaktioner och som artikeltransaktioner. Dessa två transaktionstyper innehåller olika information om var artiklar finns och om de är tillgängliga. Distributionslagertransaktioner definierar en artikels tillgänglighet per lagerplats och lagerplatstyp, vilket kallas lagerplatsinnehåll. Artikeltransaktioner definierar en artikels disposition genom dess reservation till avgående dokument. Det finns särskilda funktioner i plockningsalgoritmen för att beräkna den kvantitet som är tillgänglig för plockning när lagerplatsinnehåll kombineras med reservationer. Plockningsalgoritmen subtraherar kvantiteter som är reserverade för andra utgående dokument, kvantiteter i befintliga plockningsdokument och kvantiteter som har plockats men ännu inte levererats eller förbrukats. Resultatet visas i **fältet Disponibelt antal att plocka** på sidan **Plockningsförslag**, där fältet beräknas dynamiskt. Värdet beräknas också när en användare skapar distributionslagerplockningar direkt från utgående dokument, till exempel försäljningsorder, produktionsförbrukning eller utgående överföringar.

*Antal tillgängligt för plockning = antal på plocklagerplatser – antal på plockning och transport – (reserverat antal på plocklagerplatser + reserverat antal på plockning och transport).*

Följande exempel illustrerar hur värdet i den kvantitet som är tillgänglig för plockning beräknas i Microsoft Dynamics NAV:

1. Skapa en ny artikel med namnet Lagerartikel. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Inköp
  - **Reservpolicy**: Alltid
  - **Orderspårningspolicy**: Endast spårning
2. Skapa en inköpsorder mot leverantör 60000. Ange följande fält:
  - **Artikel**: Lagerartikel
  - **Plats**: VIT
  - **Kvantitet**: 100
3. Släpp inköpsordern och skapa lagerinleveransen.
4. Bokför lagerinleveransen och registrera lagerartikelinförseln för kvantitet 100.
5. Skapa en andra inköpsorder mot leverantör 60000. Ange följande fält:
  - **Artikel**: Lagerartikel
  - **Plats**: VIT
  - **Kvantitet**: 10
6. Släpp inköpsordern och skapa lagerinleveransen.
7. Bokför ENDAST lagerinleveransen. Registrera inte artikelinförseln i distributionslagret.
8. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: Lagerartikel
  - **Plats**: VIT
  - **Antal**: 10 Reserverat antal anges automatiskt till 10 på grund av att reservationsprincipen anges till Alltid.
9. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: Lagerartikel
  - **Plats**: VIT
  - **Antal**: 100 Reserverat antal anges automatiskt till 100 på grund av att reservprincipen anges till Alltid.
10. Släpp den första försäljningsordern från 8 steg och skapa en lagerutleverans.
11. Släpp distributionslagerutleveransen och välj Skapa plockning på **fliken Åtgärder**  **.**
Följande felmeddelande visas: *Inget att hantera.*
  Anledningen är att tillgängligt antal att plocka är noll. Detta beräknas så här: Antal i lager = 110 Antal tillgängligt att plocka = 100

> [!NOTE]  
> Antal vid artikelinförsel eller inleverans är inte tillgängligt för plockning.
   
   Total reserverad mot försäljningsorder är 110 Antal tillgängligt för plockning = 100 – 110 = noll.

När lagerartikelinförseln registreras i steg 7 kan lagerplockningen skapas i steg 11. I versioner före Microsoft Dynamics NAV 2013 har Reserved **Pick &; Ship Qty.** Fältet i tabell 337 fylls i mot reservationen för kvantitet 10.

Följande illustration är hämtad från Microsoft Dynamics NAV 2009 R2.

## Illustrationer med överföringsorder och planering

### Överföringsorder

När du använder överföringsorder och artikeln är levererad men inte helt mottagen, får du reservationsstatusen *Överskott i tabellen Reservationstransaktion* . Lagerställekoden blir Överföring till lagerställe.

Källans **ref.nr.** Beräknas med det sista radlöpnumret + radpostnumret för artikeln i den bokförda överföringsutleveransen.

När orderspårning är aktiverad och Dit inte finns någon efterfrågan (försäljningsorder eller förbrukning) Microsoft Dynamics NAV  skapas två transaktioner i tabell 337 med reservationsstatusen Överskott. Den ena är mot överföringsradtabell *5741* och den andra mot artikeltransaktionstabell 32.

Detta visas i det första exemplet.

#### Exempel 1

1. Öppna artiklarna 80003 och 80004 och ställ in fältet **Spårningsprincip** på *Endast* spårning. Lämna de andra fälten som standard.
2. Öppna en artikeljournal och öka lagret av dessa artiklar till kvantiteten 10 vardera mot lagerställe RÖD och bokför journalraderna.
3. Skapa en överföringsorder från lagerstället RÖD till BLÅ för följande två artiklar: artikel 80003 på överföringsorderrad 10000 och artikel 80004 på andra raden 20000, båda för 10 enheter.
4. Bokför endast utleveransdelen av överföringsordern utan några lagerfunktioner.
Den bokförda överföringsutleveransen visas i följande illustration.
Statusinformationen i tabell 337 visas i följande bild.
5. Jämför resultaten för den bokförda överföringsutleveransen med transaktionerna i tabell 337.

I följande tabell beskrivs vad som händer i vissa fält med reservationstransaktion 40.

|Fält|Description|  
|---------------------------------|---------------------------------------|  
|**Status för bokning**|Överskott som artikel 80003 ställs in med orderspårning, men det finns ingen efterfrågan.|  
|**Platskod**|Överföringsplats BLÅ.|  
|**Ursprungstyp**|Överföringsradbord 5741.|  
|**Käll-ID**|Verifikationsnr av överföringsordern 1011.|
|**Källa ref. nr.**|Totalt radnr 20000 + radnr. 10000 mot artikel 80003 = 30000.|

Förklaringen till följande fält mot reservationstransaktion 43 är följande:

|Fält|Description|  
|---------------------------------|---------------------------------------|  
|**Status för bokning**|Överskott som artikel 80003 ställs in med orderspårning, men det finns ingen efterfrågan.|  
|**Platskod**|Transitlagerställe EGEN LOGG är det lagerställe där artikeln finns.|  
|**Ursprungstyp**|Tabellen Artikeltransaktion 32.|  
|**Källa ref. nr.**|Det öppna artikeltransaktionsnumret 322.|

#### Exempel 2

I nästa exempel visas vad som händer när en komponent överförs mellan lagerställen, men samtidigt spåras mellan ett behovsbehov och ett tillgängligt utbud. Komponenterna överförs från lagerställe RÖD till BLÅ, som ska förbrukas på en släppt produktionsorder. Komponenten använder orderspårning, orderplanering och artikelspårning.

I exemplet visas det identifierade flödet i tabell 337 i förhållande till fälten Reservationsstatus, Lagerställekod **·**, **Källtyp,** Käll-ID **·**, **Källreferensnr** och Typ av **bindning**. **·**

1.  **På sidan Produktionsinställningar** anger du fältet **Komponenter vid lagerställe** till RÖD.
2. Skapa en ny artikelkomponent. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Inköp
  - **Tillverkningspolicy**: Tillverka-till-lager
  - **Orderspårningspolicy**: Endast spårning
  - **Artikelspårningskod**: LOTALL
3. Med hjälp av artikeljournalen ökar du lagret för artikelkomponenten mot lagerställe RÖD till 100 enheter. Ange följande partinummer:
  - Partinummer: Del A, kvantitet 30
  - Partinummer: Del B, kvantitet 70
4. Skapa en ny artikel Producerad. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Produktion
  - **Tillverkningspolicy**: Tillverka-till-lager
  - **Orderspårningspolicy**: Endast spårning
5. Skapa **en produktionsstruktur** med 1 kvantitet per av artikelkomponenten.
6. Tilldela produktionsstrukturen mot producerad artikel.
7. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: Producerad
  - **Plats**: BLÅ
  - **Kvantitet**: 100
8.  **På fliken Åtgärder** i försäljningsordern i **gruppen Plan** väljer du **Planera** för att skapa en länkad släppt produktionsorder mot försäljningsordern.
9. Öppna den släppta produktionsordern/komponentbehovet och lägg märke till att lagerstället är inställt som RÖTT.
Anledningen är **att Komponenter på plats** är RÖD i **produktionsinställningarna**  kort.
Den producerade artikeln får utdata mot lagerstället BLÅ.

Statusinformationen i tabell 337 visas i följande bild.

##### Reservationstransaktioner med nummer 55 och 56

För komponentbehovet för del A respektive parti B skapas orderspårningslänkar från efterfrågan i tabell 5407, Prod.orderkomponent, till tillgången i tabell 32, Artikeltransaktion. Fältet **Reservationsstatus** innehåller spårning för alla fyra transaktionerna för att indikera att dessa dynamiska orderspårningslänkar mellan tillgång och efterfrågan.

Efterfrågan i tabell 5407, Prod.orderkomponent, är kopplad till käll-ID för den släppta produktionsordern 101006. Tillgången i tabell 32, Artikeltransaktion, är kopplad till Källref.nr. är artikeltransaktionerna 325 och 326 där enheterna finns.

> [!NOTE]  
> Fältet **Partinr** är tomt på behovsraderna, eftersom partinumren inte har specificerats på komponentraderna för den släppta produktionsordern.

##### Reservationstransaktion med nummer 57

Från försäljningsbehovet i tabell 37, Försäljningsrad, skapas en orderspårningslänk till tillgången i tabell 5406, Prod.orderrad. Fältet **Reservationsstatus** innehåller Reservation och fältet **Bindning** innehåller Order-till-order. Detta beror på att den släppta produktionsordern genererades specifikt för försäljningsordern och måste förbli länkad till skillnad från orderspårningslänkar med reservationsstatus Spårning, som skapas och ändras dynamiskt.

> [!NOTE]  
> Fältet **Bindning** kan också innehålla *Order mot order* när Tillverka-mot-order används som Tillverkningsprincip och/eller Order som Beställningsprincip.

10. I det här läget i scenariot överförs komponentens 100 enheter från lagerstället RÖD till lagerstället BLÅ med hjälp av en överföringsorder.

Välj parti A och del B för sändningen.

Bokför det totala utestående antalet som ENDAST levererat.

> [!NOTE]  
> Komponenter kan förbrukas vid lagerställe RÖD, men för att exempelvis illustrera flödet av reservationstransaktioner överförs enheterna manuellt till lagerställe BLÅ.

Statusinformationen i tabell 337 visas i följande bild.

##### Reservationstransaktioner med nummer 55 och 56

Orderspårningstransaktioner för de två partierna av komponenten som återspeglar efterfrågan i tabell 5407 ändras från reservationsstatusen Spårning till Överskott. Anledningen är att tillgång som de var kopplade till tidigare, i tabell 32, har använts av utleveransen på överföringsordern. Äkta överskott, som i det här fallet, återspeglar överskjutande tillgång eller efterfrågan som inte har spårats. Det är en indikation på obalans i ordernätverket, som genererar ett åtgärdsmeddelande från planeringssystemet om det inte löses dynamiskt.

##### Bokningsnummer 59 till 63

Eftersom komponentens två partier bokförs på överföringsordern som levererade men inte inlevererade, är alla relaterade positiva orderspårningstransaktioner av reservationstypen Surplus, vilket indikerar att de inte allokeras till några krav. För varje partinummer avser en transaktion tabell 5741, Överföringsrad, och en transaktion avser artikeltransaktionen på det transitlagerställe där artiklarna nu finns.

Tabell 5741, **Överföringsrad**, är ursprungstypen. **Käll-ID** är överföringsorderns dokumentnummer 1012 och **källref.nr.** är 20000 = 10000 + 10000 enligt beskrivningen i exempel 1. Lagerstället anges som BLÅ för koden för överföring till lagerställe.

De återstående två transaktionerna med **Reservationsstatusöverskott** har tabell 32, **Artikeltransaktion**, som Ursprungstyp och **Källreferensnr.** 328 och 330, inklusive deras partinummer som för närvarande finns i transitplatsen OUT LOG.

11. Bokför den utestående överföringsordern som Inlevererad.

Statusinformationen i tabell 337 visas i följande bild.

Orderspårningstransaktionerna liknar nu den första punkten i scenariot, innan överföringsordern bokfördes som endast levererad, förutom att transaktionerna för komponenten nu har reservationsstatusen Överskott i stället för Spårning. Detta beror på att komponentbehovet fortfarande finns på lagerstället RÖD, vilket återspeglar att **fältet Lagerställekod** på produktionsorderkomponentraden innehåller RÖTT enligt inställningen i **fältet Komponenter vid lagerställeinställningar** .

Den tillgång som tidigare allokerades till det här behovet har överförts till lagerstället BLÅ och kan nu inte spåras helt om inte komponentbehovet på produktionsorderraden ändras till lagerstället BLÅ. Detta registreras i de två sista reservationstransaktionerna med partinumren ifyllda, **fältet Ursprungstyp är tabell 32 och** Källreferensnr **.** är artikeltransaktionerna 333 och 334.

12. På komponentlistan som tilldelats den släppta produktionsordern ändrar du lagerstället till BLÅ för komponenten.

12. Öppna förbrukningsjournalen **och** kör batch-jobbet **Beräkna förbrukning** .
Tilldela parti A kvantitet 30 och parti B kvantitet 70.

Stäng formuläret Artikelspårning.

Statusinformationen i tabell 337 visas i följande bild.

##### Reservationstransaktioner med nummer 68 och 69

Eftersom komponentbehovet har ändrats till lagerstället BLÅ och tillgången är tillgänglig som artikeltransaktioner på lagerstället BLÅ, är alla orderspårningstransaktioner för de två partinumren nu helt spårade, vilket indikeras av reservationsstatusen Spårning. Partinumren fylls inte i på **partinumret.** mot efterfrågan i tabell 5406,Prod.orderrad **·**, eftersom vi inte angav partinummer för komponenten på den släppta produktionsordern.

##### Reservationstransaktioner med nummer 70 och 71

Transaktioner med reservationsstatus Potentiell kund genereras i tabell 337. Anledningen är att båda partinumren tilldelas komponenten i förbrukningsjournalen, men journalen har inte bokförts.

Detta avslutar avsnittet om hur orderspårningstransaktioner i **tabellen Reservationstransaktion** genereras, ändras och tas bort när flera funktioner används i kombination med överföringsorder.

### Planering beräknad

När du använder planeringsfunktioner, det vill säga **inköpsförslaget** **, planeringsförslaget** eller **orderplaneringen**, kan reservationsposterna i **tabellen Reservationstransaktion** 337 ändras eller läggas till beroende på planeringsförslaget i logiken i Microsoft Dynamics NAV. Exempel 3 använder **Ändra ordning på principorder** med **Tillverkningsorder för tillverkningsprincip** för en producerad artikel. Komponenten använder **Partiformningsprincip** Fast orderkvantitet.

#### Exempel 3

1. I **Produktionsinställningar**  kort **är Komponent vid lagerställe** RÖD från föregående exempel.
2. Skapa ny överordnad artikel 70061. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Prod.order
  - **Tillverkningspolicy**: Tillverka-mot-order
  - **Partiformningsprincip**: Ordning
  - **Reservpolicy**: Valfritt
  - **Orderspårning**: Ingen
3. Skapa ny komponentartikel 70062. Ange följande fält:
  - **Basenhet**: PCS
  - Eventuella standardbokföringsmallar
  - **Återanskaffningssystem**: Inköp
  - **Partiformningsmetod**: Fast beställningsantal
  - **Reservpolicy**: Valfritt
  - **Orderspårningspolicy**: Ingen
  - **Säkerhetslager:** 10
  - **Beställningspunkt**: 25
  - **Beställningsantal**: 50
4. Skapa en ny produktionsstruktur och ange komponentartikel 70062 med antal per 1.
Tilldela produktionsstrukturen till den överordnade artikeln 70061.
5. Skapa en försäljningsorder. Ange följande fält:
  - **Artikel**: Fast beställningsantal
  - **Plats**: RÖD
  - **Kvantitet**: 40
  - **Leveransdatum**: 2014-02-15
6. Öppna sidan **Planeringsförslag** och kör batch-jobbet **Beräkna generativ plan** .
  - **MPS/MRP**: aktiverad
  - **Tillträde**: 2014-01-23
  - **Slutdatum**: 03/01/2014
  - Filtrera på artiklarna 70061 och 70062
  - Ingen prognos

Följande planeringsförslag ges.

Det första planeringsförslaget är att skapa en ny planerad produktionsorder för att tillgodose försäljningsorderns utestående behov av kvantitet 40 i den överordnade artikeln 70061. Granska orderspårningen så Microsoft Dynamics NAV visas den utestående försäljningsordern. Orderspårning aktiveras när den genereras av planeringsmotorn.

Den andra raden är att föra inventeringen ovanför beställningspunkten (25). Med hänsyn till Beställningsantal (50) föreslås därför en kvantitet på 50 enheter av planeringslogiken. Den tredje raden är att föra inventeringen till säkerhetslagernivå (10).

Den fjärde raden är att fylla på lagret när försäljningsordern levereras. Vid den tidpunkten är lagret 20 och så under beställningspunkt. Därför föreslår planeringsmotorn att ytterligare 50 komponenter köps in med hänsyn till beställningskvantiteten. Det här är Ospårat antal, så i tabellen Reservationstransaktion *337* markeras detta med reservationsstatus Överskott.

Statusinformationen i tabell 337 visas i följande bild.

Fältet **Reservationsstatus** är Reservation och en Order-till-order-bindning skapas. Anledningen är att Artikeltillverkningsprincip är Tillverka-mot-Order och Beställningsprincip anges som Order. Om en av de två är inställd på Order blir reservationsstatusen Reservation istället för Spårning och Bindning anges till Order-till-order.

Behovet på 40 enheter i fältet **Käll-ID** är försäljningsordernummer 1005 och Ursprungstyp är *Försäljningsrad* tabell 37. Reservationstransaktionen justeras med planeringsförslaget, Källreferensnr. 10000, Käll-ID är PLANERING och Källtyp är *Rekvisitionsrad* tabell 246. Så Dit är en balans mellan behovet från försäljningsordern och det utbud som föreslås av planeringsmotorn.

##### Reservationsnummer 73 och 74

Genom att köra batch-jobbet Beräkna plan genereras de följande fyra transaktionerna med reservationsstatusen Spårning på grund av inställningen för ombeställningsprincipen Fast beställningskvantitet för komponenten. Den försörjning som krävs för komponentartikel 70062 fylls på med de planeringsförslag som ges, Källref.nr. 20000 och 30000, med Käll-ID satt till PLANERING och Källtyp från *tabell 246 Rekvisitionsrad* . Komponentbehovet skapas för att uppfylla behovet mot den överordnade artikeln 70061 för totalt antal (bas) 40. Som ett resultat av denna efterfrågan är fältet **Källa prod.orderrad** 10000, med Källtyp tabellen *Komponentbehov* 99000829.

Reservationsstatusen är inte Överskott, eftersom det finns orderspårning mellan behovet av den överordnade artikeln 70061 och tillgången av komponentartikel 70062.

##### Reservationsnummer 75 och 76

De två sista transaktionerna har reservationsstatusen Överskott, eftersom dessa är Ospårade kvantiteter som genereras i planeringsförslaget och som är relaterade till beställningsparametrarna Beställningspunkt och Beställningskvantitet.

## Se även  
[Designdetaljer: Design för artikelspårning](design-details-item-tracking-design.md)  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]