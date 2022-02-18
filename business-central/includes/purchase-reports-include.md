---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ae96e5a3fc1cc7f4b17e5ef208650248cbe0b3c2
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104263"
---
I följande tabell beskrivs några av de viktigaste rapporterna inom inköpsrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Inköpsstatistik**|312|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|
|**10 i topp-leverantörer**|311|Visar information om inköp från leverantörer under en vald period. Du kan välja antalet leverantörer som ska tas med i rapporten.<br>Leverantörerna sorteras efter belopp och du kan välja om de ska sorteras per inköpsbelopp eller saldo. Rapporten ger en snabb överblick över leverantörerna som du har köpt mest av, eller som du är skyldig mest.|
|**Leverantörs artikelkatalog** eller **artikel-/leverantörskatalog**|320 eller 720|Visar en lista över leverantörerna för valda artiklar eller artiklar för valda leverantörer. För varje kombination av artikel och leverantör visar rapporten a-pris vid senaste inköp, leveranstidsberäkning och leverantörens artikelnummer.<br>I USA, Kanada och Mexiko är inte den här rapporten tillgänglig. Använd i stället tabellen **artikel-/leverantörskatalog** (10164).|
|**Lev./artikelinköp**|313|Visar en lista över artikeltransaktioner per leverantör under en vald period. Rapporten innehåller information om fakturerat antal, belopp och möjlig rabatt. Rapporten kan t.ex. användas för att analysera ett företags artikelinköp och för att visa om det finns ett samband mellan rabatter och artikelinköp.|
|**Lagerkostnad och prislista**|716|Visar en lista med prisinformation om de valda artiklarna eller lagerställeenheterna, t.ex. direkt a-pris, senaste direkt kostnad, enhetspris, vinstprocent och vinst.|
|**Lagerdispositionsplan**|707|Om du vill ha en översikt över specifika artiklar/lagerställesenheter och deras tillgänglighet. I den här rapporten visas ackumulerade värden som bruttobehov, schemalagda och planerade inleveranser, lager och så vidare. |
|**Lager - leverantörsinköp**|714|Innehåller en lista över leverantörerna som ditt företag har köpt artiklar från under en bestämd period. Rapporten visar fakturerat antal, belopp och rabatt. Rapporten kan användas för att analysera ett företags artikelinköp.|
|**Lager - inköpsorder**|709|Innehåller en lista över artiklar på order från leverantörer. Den visar även förväntat inleveransdatum samt antal och belopp för restorder. Rapporten kan t.ex. användas för att se när man kan förvänta sig leverans av artiklar och om det ska utfärdas en påminnelse för restorder|
|**Inköp - reservationstillgänglighet**|409|Visar artiklar i inköpsdokument som är disponibla för leverans, t.ex. returorder. Du bestämmer om rapporten ska visa status för varje dokument eller för varje inköpsrad. <br>När du skriver ut rapporten kan du också uppdatera disponibelt antal för leverans i fältet **Inlevereras antal** på inköpsraderna. På inköpskreditnotor och negativa inköpsorderrader innehåller fältet **Inlevereras antal** det antal som ska skickas. Sedan kan du med rapportens hjälp bestämma vilka dokument som ska levereras. **OBS!** Den här rapporten är inte tillgänglig för avancerade distributionslagerfunktioner.|
<!--|**Leverantör - åldersdetaljerad**|11006| DACH-specifik: en rapport som kan användas av gruppledaren för inköpsavdelningen samt redovisningsavdelningen. Här får du en översikt över obetalda leverantörsfakturor med förfallodatum, valutor och belopp. Grunden är de öppna leverantörsreskontraposterna.| -->

