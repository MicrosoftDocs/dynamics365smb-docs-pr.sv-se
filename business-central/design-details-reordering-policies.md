---
title: Designdetaljer - Partiformningsmetoder | Microsoft Docs
description: I det här avsnittet ger en översikt över metoder för artikelåteranskaffning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 1212c6f2f7e9da03a15c7fb39496d85869ef3e73
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238653"
---
# <a name="design-details-reordering-policies"></a>Designdetaljer: Partiformningsmetoder
Partiformningsmetoder anger hur mycket som ska beställas när artikeln behöver fyllas på. Fyra olika partiformningsmetoder finns.  

## <a name="fixed-reorder-qty"></a>Fast orderkvantitet
Metoden Fast orderkvantitet är relaterad till lagerplaneringen av typiska C-objekt (lagerkostnad låg, låg risk för åldrande och/eller många artiklar). Metoden används vanligtvis i samband med en beställningspunkt som återspeglar den förutsedda efterfrågan under artikelns ledtid.  

### <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet  
 Om planeringssystemet identifierar att beställningspunkten har uppnåtts eller passerats i en viss tidsperiod (beställningscykeln) – över eller vid beställningspunkten i början av perioden, och under eller vid beställningspunktem i slutet av perioden – får du ett förslag om att skapa en ny leveransorder för angivet beställningsantal och framåtplanera den från det första datumet efter slutet av tidsenheten.  

 Beställningspunktsbegreppet minskar antalet leveransförslag. Det beskriver en manuell process av att ofta gå genom distributionslagret för att kontrollera det faktiska innehållet på de olika lagerplatserna.  

### <a name="creates-only-necessary-supply"></a>Skapar bara nödvändigt tillgång  
 Innan en ny leveransorder föreslås för att uppfylla en beställningspunkt kontrollerar planeringssystemet om leveransen redan har beställts och ska tas emot inom artikelns ledtid. Om en befintlig leveransorder löser problemet genom att ta det planerade lagret till eller över beställningspunkten inom ledtiden, kommer systemet inte att föreslå en ny leveransorder.  

 Leveransorder som skapas specifikt för att uppfylla en beställningspunkt utesluts från vanlig tillgångsbalansering, och kommer inte ändras på något sätt efteråt. Om en artikel som använder beställningspunkt ska fasas ut (inte fyllas på) bör du därför granska utestående leveransorder manuellt eller ändra partiformningsmetoden till Parti-för-parti, varigenom systemet minskar eller att annullerar överflödig tillgång.  

### <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare  
 Ordermodifierarna Minsta partistorlek, Maximal partistorlek och Partistorleksmultipel ska inte spela en större roll när den fasta partiformningsmetoden Fast orderkvantitet används. Planeringssystemet beaktar ända dessa ändringsfält och minskar antalet till den angivna partistorleken (och skapar två eller flera leveranser för att uppnå den totala partistorleken), ökar ordern till den angivna lägsta partistorleken eller avrundar partistorleken upp till en angiven ordermultipel.  

### <a name="combines-with-calendars"></a>Kombineras med kalendrar  
 Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

 Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.  

### <a name="should-not-be-used-with-forecast"></a>Ska inte användas med prognos  
 Eftersom den förutsedda efterfrågan redan uttrycks på beställningspunktsnivån, är det inte nödvändigt att ta med en prognos i planeringen av en artikel med hjälp av en beställningspunkt. Om det är relevant att basera planen på en prognos använder du metoden Parti-för-parti.  

### <a name="must-not-be-used-with-reservations"></a>Får inte användas med reservationer  
 Om har användaren reserverat ett antal, till exempel kommer ett antal i lager, för ett avlägset behov, störs planeringsgrunden. Även om den planerade lagernivån är godtagbar i förhållande till beställningspunkten, kan det hända att antalet inte är tillgängligt. Systemet kan försöka att kompensera för det genom att skapa undantagsorder, men du rekommenderas att ange fältet Reservera till Aldrig för artiklar som planeras med hjälp av en beställningspunkt.

## <a name="maximum-qty"></a>Maximalt antal
Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.  

Allt som gäller metoden Fast orderkvantitet gäller även för den här metoden. Den enda skillnaden är antalet på i den föreslagna tillgången. När du använder principen för högsta antal definieras beställningsantalet dynamiskt baserat på den planerade lagernivån och kommer därför vanligtvis att skilja sig åt från order till order.  

### <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet  
Orderkvantitet bestäms vid tidpunkten (slutet av en tidsenhet) när planeringssystemet identifierar att beställningspunkten har passerats. Vid den här tidpunkten mäter systemet luckan mellan den aktuella planerade lagernivån fram till den angivna beställningsgränsen. Det här fältet utgör antalet som ska beställas. Systemet kontrollerar sedan om tillgång redan har beställts någon annanstans för att tas emot under ledtiden och i så fall minskar antalet på den nya leveransorder genom redan beställda antal.  

Systemet kontrollerar att det planerade lagret minst når beställningspunktnivån – i händelse användaren har glömt att ange en beställningsgränsnivå.  

### <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare  
Beroende på inställningarna kan det vara bra att kombinera principen Max. ant. med ordermodifierare för att säkerställa en minsta partistorlek eller för att avrunda den till ett heltalsnummer av inköpsenheter, eller dela den i flera partier enligt vad som anges av den maximala orderkvantiteten.  

### <a name="combines-with-calendars"></a>Kombineras med kalendrar  
Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.

## <a name="order"></a>Order
I tillverka-mot-order-miljö köps en artikel in eller produceras för att exklusivt täcka en viss efterfrågan. Vanligtvis gäller det A-artiklar och motiveringen för att välja partiformningsmetoden Order kan vara att efterfrågan är ovanlig, ledtiden är oansenlig eller de obligatoriska attributen varierar.  

Programmet skapar order-till-order-länk som fungerar som ett preliminärt samband mellan tillgången, en leveransorder eller lagret och efterfrågan som ska uppfyllas.  

Förutom att använda orderprincipen kan order-till-order-kopplingen användas på följande sätt vid planeringen:  

* När du använder produktionsprincipen Tillverka-Mot-Order för att skapa produktionsorder på flera nivåer eller av projekttyp (som producerar nödvändiga komponenter på samma produktionsorder).  
* När du använder funktionen Försäljningsorderplanering för att skapa en produktionsorder från en försäljningsorder.  

Även om ett produktionsföretag anser sig vara en miljö som tillverkar mot order, kan det vara bra att använda en partiformningsmetod av typen Parti-för-parti om artiklarna är standardartiklar med attribut utan variation. Det medför att systemet använder oplanerat lager och endast ackumulerar försäljningsorder med samma utleveransdatum eller inom en definierad tidsenhet.  

### <a name="order-to-order-links-and-past-due-dates"></a>Order-till-order-länkar och utgångna förfallodatum  
Till skillnad från de flesta uppsättningar med tillgång-efterfrågan planeras länkade order med förfallodatum före planeringsstartdatumet helt automatiskt. Affärsorsaken till undantaget är att de specifika uppsättningarna med efterfrågan-tillgång måste synkroniseras till körning. För mer information om den frysta zonen som gäller de flesta typerna av efterfrågan-tillgång, se [Designdetaljer: Hantera order före planeringsstartdatumet](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Parti-för-parti
Parti-för-parti-policyn är den mest flexibla eftersom systemet bara reagerar på faktisk efterfrågan, plus att den agerar på förutsedd efterfrågan från prognos och avropsorder, och sedan avräknar orderantalet baserat på efterfrågan. Parti-för-parti-principen gäller A-och B-artiklar där lager kan accepteras men ska undvikas.  

På vissa sätt liknar parti-för-parti-principen som orderprincipen, men den har en generisk inställning till artiklar: den kan ta emot antal i lager, och den samlar ihop efterfrågan och motsvarande tillgång i tidsenheter som definieras av användaren.  

Tidsenheten definieras i fältet **Tidsenhet**. Systemet arbetar med en lägsta tidsenhet av en dag, eftersom det är den minsta tidsenheten för efterfrågan- och tillgångshändelser i systemet (fast i praktiken kan tidsenheten för produktionsorder och komponentbehov vara sekunder).  

Tidsenheten anger också gränser för när en befintlig leveransorder ska omplaneras för att uppfylla en viss efterfrågan. Om tillgången ligger inom tidsenheten kommer den att planeras om framåt eller bakåt för att uppfylla efterfrågan. Annars, om det ligger tidigare, kommer det att orsaka onödig uppbyggnad av lagersaldot och ska avbrytas. Om det ligger senare, kommer en ny leveransorder att skapas i stället.  

Med den här metoden det är också möjligt att definiera ett säkerhetslager för att kompensera för möjliga variationer i tillgången, eller för att uppfylla plötslig efterfrågan.  

Eftersom leveranspartistorleken baseras på faktiskt behov, kan det vara praktiskt att använda ordermodifierare: avrunda partistorleken uppåt för att uppfylla en viss partistorleksmultipel (eller inköpsenhet), öka beställningen till en viss lägsta partistorlek eller minska partistorleken till det angivna högsta antalet (och skapa därmed två eller flera leveranser för att erhålla den totala behovskvantiteten).

## <a name="see-also"></a>Se även  
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
