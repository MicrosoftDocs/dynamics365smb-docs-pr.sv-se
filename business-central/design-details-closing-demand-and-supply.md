---
title: Designdetaljer - Stänga efterfrågan och tillgång | Microsoft Docs
description: Det här avsnittet innehåller förslag på vad du ska göra när du utför tillgångsbalansering.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, planning, example, closing, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: aa2a5e11f8b669a097a472bab1bda8f7fadc565f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922559"
---
# <a name="design-details-closing-demand-and-supply"></a>Designdetaljer: Stänga efterfrågan och tillgång
När tillgångsbalanseringen har utförts finns det tre möjliga slutlägen:  

* Det begärda antalet och datumet för begäranhändelserna har uppfyllts och planeringen för dem kan stängas. Tillgångshändelsen är fortfarande öppen och kan eventuellt täcka nästa efterfrågan, så motkonteringen kan starta igen med aktuell tillgångshändelse och nästa efterfrågan.  
* Leveransordern kan inte ändras för att täcka all efterfrågan. Efterfråganshändelsen är fortfarande öppen, med visst antal som inte täckts men som kan täckas av nästa tillgångshändelse. På så sätt stängs den aktuella händelsen för efterfrågan, så att motkonteringen kan börja om igen med aktuell efterfrågan och nästa tillgångshändelse.  
* All efterfrågan har täckts. Det finns inte någon efterföljande efterfrågan (eller det har inte funnits någon efterfrågan alls). Om det finns någon överskottstillgång kan den minskas (eller annulleras) och sedan stängas. Det är möjligt att ytterligare tillförselhändelser finns längre fram i kedjan, och de bör också annulleras.  

Till sist skapar planeringssystemet en orderspårninglänk mellan tillgång och efterfrågan.  

## <a name="creating-the-planning-line-suggested-action"></a>Skapa planeringsraden (föreslagen åtgärd)  
Om åtgärder – nytt, ändra antal, ändra tidpunkt, ändra tidpunkt och ändra antal eller avbryt – föreslås för att granska leveransordern skapar planeringssystemet en planeringsrad i planeringsförslaget. På grund av orderspårning skapas planeringsraden inte bara när tillförselhändelsen stängs, utan även om efterfråganshändelsen stängs, även om tillförselhändelsen fortfarande är öppen och kan få ytterligare ändringar när nästa efterfråganshändelse behandlas. Det betyder att när planeringsraden har skapats kan den ändras på nytt.  

För att minska databasåtkomsten när du hanterar produktionsorder kan planeringsraden underhållas i tre nivåer, med målet att utföra den minst fordrande underhållsnivån:  

* Skapa endast planeringsraden med det aktuella förfallodatumet och antalet men utan verksamhetsföljden och komponenterna.  
* Inkludera verksamhetsföljd: den planerade verksamhetsföljden läggs ut inklusive beräkning av start- och slutdatum och tidpunkter. Det är fordrande i termer av databasåtkomster. För att fastställa slut- och förfallodatum kan det vara nödvändigt att beräkna detta även om tillförselhändelsen inte har stängts (om det gäller framåtplanering).  
* Ta med strukturexpansion: det kan vänta tills precis före tillgångshändelsen är avslutad.  

Detta slutför beskrivningarna av hur efterfrågan och tillgång laddas, prioriteras och balanseras av planeringssystemet. I integration med den här tillgångsplaneringsaktiviteten måste systemet se till att önskad lagernivå för varje planerad artikel upprätthålls enligt dess partiformningsmetoder.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
