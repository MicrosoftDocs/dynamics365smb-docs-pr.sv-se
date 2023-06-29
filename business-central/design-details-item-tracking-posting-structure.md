---
title: Designdetaljer – Bokföringsstruktur för artikelspårning
description: Lär dig att använda artikeltransaktioner som den primära bäraren av artikelspårningsnummer i Bokföringsstruktur för artikelspårning.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-posting-structure"></a><a name="design-details-item-tracking-posting-structure"></a>Designdetaljer: Bokföringsstruktur för artikelspårning
För att anpassas till funktionen för lagervärdering och för att få en enklare och mer robust lösning används artikeltransaktioner som den primära bäraren av artikelspårningsnummer.  
  
Artikelspårningsnummer i ordernätverksenheter och icke orderrelaterade nätverksenheter anges i fältet **Reservationstransaktion** tabell (T337). Artikelspårningsnummer som är kopplade till historisk information hämtas direkt från de artikeltransaktioner som hör till transaktionen i fråga. Det betyder att artikeltransaktioner återspeglar artikelspårningspecifikationen för den bokförda orderraden.  
  
Sidan **Artikelspårningsrader** hämtar informationen från T337 och artikeltransaktionerna och visar den via den tillfälliga tabellen, **Spårningsspecifikation** (T336). T336 innehåller också de temporära data på sidan **Artikelspårningsrader** för artikelspårning av antal som återstår att faktureras.  
  
## <a name="one-to-many-relation"></a><a name="one-to-many-relation"></a>En-till-många-relation
Tabellen **Artikeltrans. relation** som används för att koppla en bokförd dokumentrad med dess relaterade artikeltransaktioner, består av två delar:  
  
* En pekare till den bokförda dokumentraden, fältet **Orderradnr**. .  
* Ett löpnummer som pekar på en artikeltransaktion, fältet **Artikellöpnr**.  
  
Funktionen för det befintliga fältet **Löpnr**, som gäller en artikeltransaktion till en bokförd dokumentrad, hanterar den typiska ett-till- ett-relationen när inget artikelspårningsnummer finns på den bokförda dokumentraden. Om artikelspårningsnummer finns är fältet **Löpnr** tom och en-till-flera-relationen hanteras av tabellen **Artikeltrans. relation**. Om den bokförda dokumentraden har artikelspårningsnummer men endast är knuten till en enda artikeltransaktion, hanterar fältet **Löpnr** relationen och ingen transaktion skapas i tabellen **Artikeltrans. relation**.  
  
## <a name="codeunits-80-and-90"></a><a name="codeunits-80-and-90"></a>Kodenhet 80 och 90
Om du vill dela artikeltransaktionerna vid bokföring omringas koden i kodenhet 80 och kodenhet 90 med loopar som körs via globala, tillfälliga postvariabler. Koden anropar kodenhet 22 med en artikeljournalrad. Dessa variabler aktiveras när artikelspårningsnummer finns för dokumentraden. För att hålla koden enkel används alltid den här loopstrukturen. Om inga artikelspårningsnummer finns för dokumentraden infogas en enda post, och loopen körs bara en gång.  
  
## <a name="posting-the-item-journal"></a><a name="posting-the-item-journal"></a>Bokför artikeljournalen
Artikelspårningsnummer överförs via de Reservationstransaktioner som är relaterade till den aktuella artikeltransaktionen och upprepa format i artikelspårningsnummer automatiskt i kodmodul 22. Detta fungerar på samma sätt när en artikeljournalrad indirekt för att bokföra en försäljning eller inköp som när du använder en artikeljournalrad direkt. När artikeljournalen används direkt pekar fältet **Källrad-ID** på själva artikeljournalraden.  
  
## <a name="code-unit-22"></a><a name="code-unit-22"></a>Kodenhet 22
Kodenhet 80 och 90 tar anropet i kodenhet 22 i en loop under fakturabokföringen av artikelspårningsnummer och vid faktureringen av befintliga leveranser eller kvitton.  
  
Under antalsbokföring av artikelspårningsnummer hämtar kodenhet 22 artikelspårningsnummer från transaktionerna i T337 som avser bokföringen. Dessa transaktioner placeras direkt på artikeljournalraden.  
  
Kodenhet 22 går i en loop via artikelspårningsnumren och delar upp bokföringen i de artikeltransaktioner som har artikelspårningsnumren. Information om vilka artikeltransaktioner skapas tillbaka till T337 med hjälp av en temporär T336 post som anropas av en procedur i kodmodul 22. Den här proceduren utfärdas när kodmodul 22 är klar att köras eftersom samtidigt, kodmodul 22-objekt innehåller information. När det tillfälliga T336-posten hämtas skapar kodmodulerna 80 och 90 poster i tabellen **Artikeltrans. relation** för att koppla de skapade artikeltransaktionerna till den skapade utleverans- eller inleveransraden. Kodenhet 80 eller 90 omvandla sedan de temporära T336-posterna till riktiga T336-poster som är kopplade till raden i fråga. Denna konvertering inträffar bara om den bokförda dokumentraden inte tas bort, eftersom det endast har bokförts delvis.  
  
## <a name="see-also"></a><a name="see-also"></a>Se även
[Designdetaljer: Objektspårning](design-details-item-tracking.md)   
[Designdetaljer: Artikelkopplingsdesign](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
