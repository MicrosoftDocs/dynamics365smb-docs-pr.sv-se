---
title: Konfigurera produktionsprocesser | Microsoft Docs
description: "För att material ska kunna omvandlas till tillverkade slutartiklar måste produktionsresurser som t.ex. strukturer, operationsföljder, maskinoperatörer och maskiner ställas in i systemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: de493a4697c3a5c2fb8581545a29ee832fe1c3dc
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-manufacturing"></a>Ställa in Produktion
För att material ska kunna omvandlas till tillverkade slutartiklar måste produktionsresurser som t.ex. strukturer, operationsföljder, maskinoperatörer och maskiner ställas in i systemet.

I systemet representeras operatörer och maskiner som maskingrupper, vilka i sin tur kan organiseras i produktionsgrupper. När dessa resurser upprättats kan de laddas med operationer enligt den material- (struktur) och processtruktur (operationsföljd) som definierats för artikeln samt utifrån maskin- eller produktionsgruppens kapacitet. Du kan även ställa in produktionskapaciteten för varje resurs. Kapaciteten definieras av den arbetstid som finns tillgänglig i maskin- och produktionsgrupperna, och den styrs av kalendrar på alla nivåer. I en produktionsgruppkalender anges de arbetsdagar/arbetstimmar, skift, helgdagar och frånvaro som avgör den tillgängliga bruttokapaciteten (och som vanligtvis mäts i minuter). Allt detta avgörs utifrån de effektivitets- och kapacitetsvärden som har definierats.  

När du har lagt upp produktion kan du planera och utföra produktionsorder. Mer information finns i [Planering](production-planning.md) och [Produktion](production-manage-manufacturing.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Konfigurera produktionsfunktionerna, till exempel definiera arbetstimmar för en fabrik eller välja planeringsprinciper.|Sidan **Produktionsinställningar**.|  
|Definiera en standardarbetsvecka i modulen Produktion med start- och sluttider för varje arbetsdag samt tillhörande arbetsskiften.|[Så här skapar du fabrikskalendrar](production-how-to-create-work-center-calendars.md)|  
|Organisera fasta värden och krav för produktionsresurser som t.ex. produktionsgrupper eller maskingrupper till att styra deras tillverkningsutflöde i maskingruppen.|[Så här: ställa in produktionsgrupper och maskingrupper](production-how-to-set-up-work-and-machine-centers.md)|
|Ordna produktionsoperationer i krävd ordningen och tilldela dem till produktions- eller maskingrupper med nödvändiga arbetstider.|[Så här skapar du operationsföljder](production-how-to-create-routings.md)|
|Ordna produktionskomponenter eller underenheter under en producerad artikel och godkänn strukturlistan utförs vid produktionsgrupper.|[Så här skapar du nya produktionsstrukturer](production-how-to-create-production-boms.md)|
|Kontrollera att rätt komponentkvantitet är tillgänglig när tillverkade artiklar lagerförs med en enhet men tillverkas med en annan.|[Så här kan du arbeta med enheter för produktionsbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definiera familjer av produktionsartiklar som har liknande produktionsprocesser för att minska förbrukning. Till exempel kan fyra enheter av en artikel produceras av ett ark och tio enheter av en annan artikel av samma ark.|[Så här: arbeta med produktionsfamiljer](production-how-work-family.md)|
|Använd standarduppgifter om du vill förenkla operationsföljder genom att snabbt lägga till extra information för återkommande transaktioner.|[Så här skapar du standardoperationsföljdrader](production-how-set-up-standard-routing-lines.md)|  
|Förbered produktionsgrupper och operationsföljder för att representera legotillverkning.|[Så här lägger du ut legotillverkning för produktion](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Se även
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

