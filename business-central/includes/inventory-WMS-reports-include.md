---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ac10f2efa500d1e9dc12de7ced52c4b35406e1bc
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104226"
---
I följande tabell beskrivs några av de viktigaste rapporterna inom lager- och distributionslagerrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Lagerdispositionsplan**|707|Om du vill ha en översikt över specifika artiklar/lagerställesenheter och deras tillgänglighet. I den här rapporten visas ackumulerade värden som bruttobehov, schemalagda och planerade inleveranser, lager och så vidare. |
|**Lagervärdering**|1001|Visar information om lagervärderingen för valda artiklar i lagret. Rapporten visas även information om värdet av ökningar och minskningar i lager över tid.|
|**Utgångsdatum artikel - Antal**|5809|Visar en översikt över antalet valda artiklar i lagret vars utgångsdatum infaller inom en viss period. I listan visas det antal enheter av den valda artikeln som kommer att gå ut inom en given tidsperiod. För varje artikel som du anger när du ställer in rapporten visas i det utskrivna dokumentet antalet enheter som kommer att gå ut under var och en av tre perioder med samma längd och den totala lagerkvantiteten för den valda artikeln.<br>Du kan ange vad som inkluderas i rapporten genom att ställa in filter. Om du inte ställer in några filter inkluderas alla poster i rapporten. Antalet i rapporten reflekterar endast det antal av artikeln som utgångsdatum har definierats för.|
|**Artikel åldersstruktur - antal** eller **artikel åldersstruktur - värde**|5807 eller 5808|Innehåller en överblick över åldersstrukturen för valda artiklar i lagret. I listan anges hur många enheter eller värde av den valda artikeln som har lagts till i eller tagits ur lagret och vid vilken tidpunkt. Artiklar kan läggas till i eller tas ur lagret som en följd av inköp, försäljningar och positiva eller negativa justeringar.|
|**Lagerkostnad och prislista**|716|Visar en lista med prisinformation om de valda artiklarna eller lagerställeenheterna, t.ex. direkt a-pris, senaste direkt kostnad, enhetspris, vinstprocent och vinst. |
|**Dist.lager lagerplatslista**|7319|Visar en översikt över distributionslagerplatser, deras inställningar och antalet artiklar på lagerplatsen. Rapporten kan användas för alla lagerställen, med "lagerplats" som obligatoriskt fält. |
|**Status för distributionslagerutleverans**|7313|Visar en översikt över öppna källdokument med varor som har levererats eller är redo att levereras per lagerställe. Den här rapporten kan användas för alla platser där **obligatoriska försändelser** har aktiverats. **Status för distributionslagerutleverans** visar platser, lagerplatskoder, dokumentstatus, antal.|
|**Lagerplockningslista**|813|Innehåller en lista över de försäljningsorder som innehåller en viss artikel. Följande information visas för respektive artikel: försäljningsorderrad med kundens namn, variantkod, lagerställekod, lagerplatskod, leveransdatum, antal att leverera och enhet. Antalet som ska levereras är summerat per artikel. Rapporten kan användas när artiklarna ska plockas från lagret.<br>OBS! Den här funktionen är inte tillgänglig för avancerade distributionslagerfunktioner.|
|**Justeringslagerplats för distributionslager**|7320|Denna specialrapport är endast avsedd för ett avancerat lagerställe och visar de återstående antal som fortfarande lagras på justeringslagerplatsen. Normalt bör denna specifika lagerplats vara tom. Det enda skälet till att den här lagerplatsen kommer att fyllas är som resultat av fysisk inventeringsoperation eller om antal artiklar som har tagits bort eller lagts till i distributionslagret|