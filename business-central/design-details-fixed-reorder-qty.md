---
title: Designdetaljer - Fast orderkvantitet | Microsoft Docs
description: Metoden Fast orderkvantitet är relaterad till lagerplaneringen av typiska C-objekt (lagerkostnad låg, låg risk för åldrande och/eller många artiklar). Metoden används vanligtvis i samband med en beställningspunkt som återspeglar den förutsedda efterfrågan under artikelns ledtid.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: dd8c4b8cdae3e004e30551798e5a68058b5c38fe
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307233"
---
# <a name="design-details-fixed-reorder-qty"></a>Designdetaljer: Fast orderkvantitet
Metoden Fast orderkvantitet är relaterad till lagerplaneringen av typiska C-objekt (lagerkostnad låg, låg risk för åldrande och/eller många artiklar). Metoden används vanligtvis i samband med en beställningspunkt som återspeglar den förutsedda efterfrågan under artikelns ledtid.  

## <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet  
 Om planeringssystemet identifierar att beställningspunkten har uppnåtts eller passerats i en viss tidsperiod (beställningscykeln) – över eller vid beställningspunkten i början av perioden, och under eller vid beställningspunktem i slutet av perioden – får du ett förslag om att skapa en ny leveransorder för angivet beställningsantal och framåtplanera den från det första datumet efter slutet av tidsenheten.  

 Beställningspunktsbegreppet minskar antalet leveransförslag. Det beskriver en manuell process av att ofta gå genom distributionslagret för att kontrollera det faktiska innehållet på de olika lagerplatserna.  

## <a name="creates-only-necessary-supply"></a>Skapar bara nödvändigt tillgång  
 Innan en ny leveransorder föreslås för att uppfylla en beställningspunkt kontrollerar planeringssystemet om leveransen redan har beställts och ska tas emot inom artikelns ledtid. Om en befintlig leveransorder löser problemet genom att ta det planerade lagret till eller över beställningspunkten inom ledtiden, kommer systemet inte att föreslå en ny leveransorder.  

 Leveransorder som skapas specifikt för att uppfylla en beställningspunkt utesluts från vanlig tillgångsbalansering, och kommer inte ändras på något sätt efteråt. Om en artikel som använder beställningspunkt ska fasas ut (inte fyllas på) bör du därför granska utestående leveransorder manuellt eller ändra partiformningsmetoden till Parti-för-parti, varigenom systemet minskar eller att annullerar överflödig tillgång.  

## <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare  
 Ordermodifierarna Minsta partistorlek, Maximal partistorlek och Partistorleksmultipel ska inte spela en större roll när den fasta partiformningsmetoden Fast orderkvantitet används. Planeringssystemet beaktar ända dessa ändringsfält och minskar antalet till den angivna partistorleken (och skapar två eller flera leveranser för att uppnå den totala partistorleken), ökar ordern till den angivna lägsta partistorleken eller avrundar partistorleken upp till en angiven ordermultipel.  

## <a name="combines-with-calendars"></a>Kombineras med kalendrar  
 Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

 Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.  

## <a name="should-not-be-used-with-forecast"></a>Ska inte användas med prognos  
 Eftersom den förutsedda efterfrågan redan uttrycks på beställningspunktsnivån, är det inte nödvändigt att ta med en prognos i planeringen av en artikel med hjälp av en beställningspunkt. Om det är relevant att basera planen på en prognos använder du metoden Parti-för-parti.  

## <a name="must-not-be-used-with-reservations"></a>Får inte användas med reservationer  
 Om har användaren reserverat ett antal, till exempel kommer ett antal i lager, för ett avlägset behov, störs planeringsgrunden. Även om den planerade lagernivån är godtagbar i förhållande till beställningspunkten, kan det hända att antalet inte är tillgängligt. Systemet kan försöka att kompensera för det genom att skapa undantagsorder, men du rekommenderas att ange fältet Reservera till Aldrig för artiklar som planeras med hjälp av en beställningspunkt.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
 [Designdetaljer: Maximalt antal](design-details-maximum-qty.md)   
 [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
 [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)
