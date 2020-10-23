---
title: Designdetaljer - Artikelspårning och reservationer | Microsoft Docs
description: Det här avsnittet handlar om artikelspårning och reservationer och beskriver koncepten bakom de två.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cb79b0538f4f55b2841815c23c4446d7c6278fb1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922098"
---
# <a name="design-details-item-tracking-and-reservations"></a>Designdetaljer: Artikelkoppling och reservationer

Samtidigt användning av reservation och specifik artikelspårning är ovanlig, eftersom de båda skapar en koppling mellan tillgång och efterfrågan. Förutom i situationer där en kund eller en produktionsplanerare begär ett visst parti, är det sällan meningsfullt att reservera lagerartiklar som har redan artikelspårningsnummer för viss koppling. Även om det är möjligt att reservera artiklar som kräver särskild artikelspårning, krävs särskilda funktioner för att undvika konflikter mellan orderhandläggare som begär samma spårade artiklar.  
  
Begreppet Sen bindning säkerställer att en icke-specifik reservation av serienummer eller partinummer förblir löst kopplad till bokföringen. Vid bokföringstiden kan reservationsystemet blanda om icke-specifika reservationer för att se till att fasta kopplingar är möjliga för det serie- eller partinummer som faktiskt plockas. Under tiden görs serie- eller partinumret tillgängligt för specifik reservation i andra dokument som begär just det serie- eller partinumret.  
  
En icke-specifik reservation är en där användaren inte att bry sig om vilken specifik artikel som plockas, och en specifik reservation är en där användaren att bryr sig.  
  
> [!NOTE]  
> Funktionen Sen bindning gäller endast för artiklar som ställs in med specifik artikelspårning och den gäller endast för reservationer mot lager, inte mot den ankommande leveransorder.  
  
Reservation av artikelspårningsnummer är uppdelad i två kategorier, som visas i följande tabell.  
  
|Reservation|Description|  
|-----------------|---------------------------------------|  
|Specifik|Du väljer ett visst serie- eller partinummer när du reserverar lagerartikeln från ett behov, t.ex. en försäljningsorder.<br /><br /> Detta är en reguljär reservation. Det är en fast länk mellan tillgång och efterfrågan som båda har serie- eller partinummer. **Obs:**  Efterfrågan har serie- eller partinummer. <br /><br /> Till exempel, du vill reservera en burk med blå färg från parti A eftersom kunden begär det. En burk med blå färg från ett Parti A levereras till kunden.|  
|Icke-specifik|Du väljer inte ett visst serie- eller partinummer när du reserverar lagerartikeln från ett behov, t.ex. en försäljningsorder.<br /><br /> Detta är läge som läggs på en reservationstransaktion för serie- eller partinummer som inte har har valts specifikt. **Obs:** Efterfrågan har inte serie- eller partinummer. <br /><br /> Till exempel, du vill reservera en burk med blå färg från ett valfritt parti för din försäljningsorder. En burk med blå färg från ett slumpmässigt serie- eller partinumret levereras till kunden.|  
  
Den huvudsakliga skillnaden mellan specifika och icke-specifika reservationer definieras av förekomsten av serie- eller partinummer på efterfråganssidan, så som visas i följande tabell.  

| Typ            | Tillgång                | Behov                   |
|-----------------|-----------------------|--------------------------|
| **Specifik**    | Serie- eller partinummer. | Serie- eller partinummer.    |
| **Icke-specifik** | Serie- eller partinummer. | Inget serie- eller partinummer |
  
När du reserverar lagerkvantiteter från en avgående dokumentrad för en artikel som har artikelspårningsnummer tilldelade och är inställd för särskild artikelspårning, leder sidan **Reservation** dig via olika arbetsflöden beroende på vad du behöver för serie- eller partinumren.  
  
## <a name="specific-reservation"></a>Specifik reservation  
När du väljer **Reservera** på den utgående dokumentraden visas en dialogruta där du tillfrågas om du vill reservera specifika serie- eller partinummer. Om du väljer **Ja** visas en lista med alla serie- och partinummer som tilldelats dokumentraden. Sidan **Reservation** öppnas när du har valt en av serie- eller partinumren, och du kan då reservera bland de valda serie- eller partinumren på ett typiskt sätt.  
  
Om några av de specifika artikelspårningsnumren som du försöker reservera finns i icke-specifika reservationer får du ett meddelande längst ned på sidan **Reservation** om att många av det totala reserverade antalet finns i icke-specifika reservationer och om de är fortfarande tillgängliga.  
  
## <a name="nonspecific-reservation"></a>Icke-specifik reservation  
Om du väljer **Nr** i dialogrutan som visas öppnas sidan **Reservation** och du kan reservera bland alla serie- och partinummer i lagret.  
  
På grund av strukturen i reservationsystemet måste systemet välja specifika artikeltransaktioner att reservera mot när du gör en icke-specifik reservation för en artikelspårad artikel. Eftersom artikeltransaktionerna har artikelspårningsnumren, reserverar reservationen indirekt specifika serie- eller partinummer, även om du inte avsåg att göra det. För att hantera den här situationen försöker reservationssystemet ombilda icke-specifika reservationstransaktioner före bokföring.  
  
Systemet reserverar faktiskt fortfarande mot specifika transaktioner, men det använder sedan en ombildningsmekanism när som helst det finns en viss efterfrågan för parti- eller serienumret i den icke-specifika reservationen. Det kan vara fallet när du bokför en efterfråganstransaktion, t.ex. en försäljningsorder, förbrukningsjournal eller överföringsorder för serie- eller partinumret, eller när du försöker att reservera ett specifikt serie- eller partinummer. Systemet ombildar reservationerna för att göra parti- eller serienumret tillgängliga för efterfrågan eller den specifika reservationen och därmed ange ett annat parti- eller serienummer i den icke-specifika reservationen. Om det finns otillräckliga antal i lager stuvar systemet om så mycket som möjligt och du får ett dispositionsfel om det fortfarande finns otillräckliga antal vid bokföringstidpunkten.  
  
> [!NOTE]  
>  På en icke-specifik reservation är partinummer- eller serienummerfältet tomt i reservationstransaktionen som pekar på efterfrågan, till exempel försäljningen.  
  
## <a name="reshuffle"></a>Ombildning  
När en användare bokför ett utgående dokument när han har valt fel serie- eller partinummer ombildas andra icke-specifika reservationer för att visa faktiskt serie- eller partinummer plockas. Det uppfyller bokföringsmotorn med en fast koppling mellan tillgång och efterfrågan.  
  
För alla affärsscenarion som stöds är det endast möjligt att blanda om mot positiva artikeltransaktioner med reservation och serie- eller partinummer, men utan definierade serie- eller partinummer på efterfråganssidan.  
  
## <a name="supported-business-scenarios"></a>Affärsscenarion som stöds  
Funktionen Sen bindning stöder följande affärsscenarion:  
  
* Ange ett specifikt serie- eller partinummer för ett avgående dokument med icke-specifik reservation av ett felaktigt serie- eller partinummer.  
* Reservera ett visst serie- eller partinummer.  
* Bokför ett avgående dokument med icke-specifik reservation av serie- eller partinummer.  
  
### <a name="entering-serial-or-lot-numbers-on-an-outbound-document-with-wrong-nonspecific-reservation"></a>Ange serie- eller partinummer för ett avgående dokument med fel icke-specifik reservation  
Det här är det vanligaste det av de tre scenarierna som stöds. I det här fallet säkerställer funktionen Sen bindning att en användare kan ange ett serie- eller partinummer, som faktiskt plockas, på ett avgående dokument som redan har en icke-specifik reservation av ett annat serie- eller partinummer.  
  
Till exempel uppstår behovet när en orderhandläggare först skapade en icke-specifik reservation för ett serie- eller partinummer. Senare, när artikeln faktiskt plockas från lagret, måste det plockade serie- eller partinumret anges på ordern innan den bokförs. Den icke-specifika reservationen ombildas vid bokföringen för att se till att det valda serie- eller partinumret kan anges utan att förlora reservationen och se till att det valda serie- eller partinumret kan kopplas helt och bokföras.  
  
### <a name="reserve-specific-serial-or-lot-numbers"></a>Reservera specifika serie- eller partinummer  
I affärsscenariot säkerställer funktionen Sen bindning att en användare som försöker att reservera ett visst serienummer eller partinummer som för närvarande har reserverats icke-specifikt kan göra det. En icke-specifik reservation stuvas om vid tidpunkten för reservation för att släppa serie- eller partinumret i för den specifika förfrågan.  
  
Ombildningen sker automatiskt, men inbäddad hjälp visas längst ned på sidan **Reservation** och visar följande text:  
  
**XX av totalt reserverat antal är icke-specifikt och kan vara tillgängligt.**  
  
Dessutom visar fältet **Icke-specifik reserverat antal** hur många reservationstransaktioner som är icke-specifika. Som standard visas detta fält inte för användaren.  
  
### <a name="posting-an-outbound-document-with-nonspecific-reservation-of-serial-or-lot-numbers"></a>Bokför ett avgående dokument med icke-specifik reservation av serie- eller partinummer.  
Affärsscenariot stöds med funktionen Sen bindning som möjliggör fast koppling och avgående bokföring av det som faktiskt plockas genom att ombilda en annan icke-specifik reservation av ett serie- eller partinummer. Om det inte är möjligt att stuva om visas följande standardmeddelande när användaren försöker bokföra utleveransen:  
  
**Artikel XX kan inte kopplas helt.**  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Objektspårning](design-details-item-tracking.md)