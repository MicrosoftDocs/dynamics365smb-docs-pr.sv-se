---
title: Inköpsrapporter och -analyser
description: Se vilka inköpsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på din verksamhet.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 3f818e556b2ebe3f50189b0057f1302a5598d904
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543176"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Inköpsrapporter och analys i Business Central

Med inköpsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] kan inköps- och affärspersonal få insikter och statistik om aktuella och tidigare inköpsaktiviteter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom inköpsrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Inköpsstatistik**|312|[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]|
|**10 i topp-leverantörer**|311|Visar information om inköp från leverantörer under en vald period. Du kan välja antalet leverantörer som ska tas med i rapporten.<br>Leverantörerna sorteras efter belopp och du kan välja om de ska sorteras per inköpsbelopp eller saldo. Rapporten ger en snabb överblick över leverantörerna som du har köpt mest av, eller som du är skyldig mest.|
|**Leverantörs artikelkatalog** eller **artikel-/leverantörskatalog**|320 eller 720|Visar en lista över leverantörerna för valda artiklar eller artiklar för valda leverantörer. För varje kombination av artikel och leverantör visar rapporten a-pris vid senaste inköp, leveranstidsberäkning och leverantörens artikelnummer.<br>I USA, Kanada och Mexiko är inte den här rapporten tillgänglig. Använd i stället tabellen **artikel-/leverantörskatalog** (10164).|
|**Lev./artikelinköp**|313|Visar en lista över artikeltransaktioner per leverantör under en vald period. Rapporten innehåller information om fakturerat antal, belopp och möjlig rabatt. Rapporten kan t.ex. användas för att analysera ett företags artikelinköp och för att visa om det finns ett samband mellan rabatter och artikelinköp.|
|**Lagerkostnad och prislista**|716|Visar en lista med prisinformation om de valda artiklarna eller lagerställeenheterna, t.ex. direkt a-pris, senaste direkt kostnad, enhetspris, vinstprocent och vinst.|
|**Lagerdispositionsplan**|707|Om du vill ha en översikt över specifika artiklar/lagerställesenheter och deras tillgänglighet. I den här rapporten visas ackumulerade värden som bruttobehov, schemalagda och planerade inleveranser, lager och så vidare. |
|**Lager - leverantörsinköp**|714|Innehåller en lista över leverantörerna som ditt företag har köpt artiklar från under en bestämd period. Rapporten visar fakturerat antal, belopp och rabatt. Rapporten kan användas för att analysera ett företags artikelinköp.|
|**Lager - inköpsorder**|709|Innehåller en lista över artiklar på order från leverantörer. Den visar även förväntat inleveransdatum samt antal och belopp för restorder. Rapporten kan t.ex. användas för att se när man kan förvänta sig leverans av artiklar och om det ska utfärdas en påminnelse för restorder|
|**Inköp - reservationstillgänglighet**|409|Visar artiklar i inköpsdokument som är disponibla för leverans, t.ex. returorder. Du bestämmer om rapporten ska visa status för varje dokument eller för varje inköpsrad. <br>När du skriver ut rapporten kan du också uppdatera disponibelt antal för leverans i fältet **Inlevereras antal** på inköpsraderna. På inköpskreditnotor och negativa inköpsorderrader innehåller fältet **Inlevereras antal** det antal som ska skickas. Sedan kan du med rapportens hjälp bestämma vilka dokument som ska levereras. **OBS!** Den här rapporten är inte tillgänglig för avancerade distributionslagerfunktioner.|
<!--|**Leverantör - åldersdetaljerad**|11006| DACH-specifik: en rapport som kan användas av gruppledaren för inköpsavdelningen samt redovisningsavdelningen. Här får du en översikt över obetalda leverantörsfakturor med förfallodatum, valutor och belopp. Grunden är de öppna leverantörsreskontraposterna.| -->




## <a name="tasks"></a>Uppgifter

I följande artiklar beskrivs några av de viktigaste uppgifterna för att analysera verksamhetens tillstånd:

* [Skapa analysrapporter](bi-how-create-analysis-views-reports.md)  
* [Visa artikeldisposition](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Se även

[Ställa in inköp](purchasing-setup-purchasing.md)  
[Inköp](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
