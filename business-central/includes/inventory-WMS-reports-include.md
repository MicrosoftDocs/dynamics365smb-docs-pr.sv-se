---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c99520c40098f568df543ccda2996639e22dcb8
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334746"
---
I följande tabell beskrivs några av de viktigaste rapporterna inom lager- och distributionslagerrapportering.

| Rapportera | Beskrivning | Id | 
|---------|---------|---------|
|[Lagerdispositionsplan](https://businesscentral.dynamics.com?report=707)|Om du vill ha en översikt över specifika artiklar/lagerställesenheter och deras tillgänglighet. I den här rapporten visas ackumulerade värden som bruttobehov, schemalagda och planerade inleveranser, lager och så vidare. |707|
|[Lagervärdering](https://businesscentral.dynamics.com?report=1001)|Visar information om lagervärderingen för valda artiklar i lagret. Rapporten visas även information om värdet av ökningar och minskningar i lager över tid.|1001|
|[Utgångsdatum för artikel – Antal](https://businesscentral.dynamics.com?report=5809)|Visar en översikt över antalet valda artiklar i lagret vars utgångsdatum infaller inom en viss period. I listan visas det antal enheter av den valda artikeln som kommer att gå ut inom en given tidsperiod. För varje artikel som du anger när du ställer in rapporten visas i det utskrivna dokumentet antalet enheter som kommer att gå ut under var och en av tre perioder med samma längd och den totala lagerkvantiteten för den valda artikeln.<br>Du kan ange vad som inkluderas i rapporten genom att ställa in filter. Om du inte ställer in några filter inkluderas alla poster i rapporten. Antalet i rapporten reflekterar endast det antal av artikeln som utgångsdatum har definierats för.|5809|
|[Åldersstruktur för artikel – antal](https://businesscentral.dynamics.com?report=5807)|Innehåller en överblick över åldersstrukturen för valda artiklar i lagret. I listan anges hur många enheter eller värde av den valda artikeln som har lagts till i eller tagits ur lagret och vid vilken tidpunkt. Artiklar kan läggas till i eller tas ur lagret som en följd av inköp, försäljningar och positiva eller negativa justeringar.|5807|
|[Åldersstruktur för artikel – värde](https://businesscentral.dynamics.com?report=5808)|Innehåller en överblick över åldersstrukturen för valda artiklar i lagret. I listan anges hur många enheter eller värde av den valda artikeln som har lagts till i eller tagits ur lagret och vid vilken tidpunkt. Artiklar kan läggas till i eller tas ur lagret som en följd av inköp, försäljningar och positiva eller negativa justeringar.|5808|
|[Lagerkostnad och prislista](https://businesscentral.dynamics.com?report=716)|Visar en lista med prisinformation om de valda artiklarna eller lagerställeenheterna, t.ex. direkt styckkostnad, senaste direkta styckkostnad, enhetspris, vinstprocent och vinst. |716|
|[Lagerplatslista för distr.lager](https://businesscentral.dynamics.com?report=7319)|Visar en översikt över distributionslagerplatser, deras inställningar och antalet artiklar på lagerplatsen. Rapporten kan användas för alla lagerställen, med "lagerplats" som obligatoriskt fält. |7319|
|[Status för distributionslagerutleverans](https://businesscentral.dynamics.com?report=7313)|Visar en översikt över öppna källdokument med varor som har levererats eller är redo att levereras per lagerställe. Den här rapporten kan användas för alla platser där **obligatoriska försändelser** har aktiverats. **Status för distributionslagerutleverans** visar platser, lagerplatskoder, dokumentstatus, antal.|7313|
|[Lagerplockningslista](https://businesscentral.dynamics.com?report=813)|Innehåller en lista över de försäljningsorder som innehåller en viss artikel. Följande information visas för respektive artikel: försäljningsorderrad med kundens namn, variantkod, lagerställekod, lagerplatskod, leveransdatum, antal att leverera och enhet. Antalet som ska levereras är summerat per artikel. Rapporten kan användas när artiklarna ska plockas från lagret.<br>OBS! Den här funktionen är inte tillgänglig för avancerade distributionslagerfunktioner.|813|
|[Justeringslagerplats för distributionslager](https://businesscentral.dynamics.com?report=7320)|Denna specialrapport är endast avsedd för ett avancerat lagerställe och visar de återstående antal som fortfarande lagras på justeringslagerplatsen. Normalt bör denna specifika lagerplats vara tom. Det enda skälet till att den här lagerplatsen kommer att fyllas är som resultat av fysisk inventeringsoperation eller om antal artiklar som har tagits bort eller lagts till i distributionslagret|7320|