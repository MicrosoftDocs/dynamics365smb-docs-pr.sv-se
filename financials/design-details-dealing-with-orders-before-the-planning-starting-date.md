---
title: "Designdetaljer: Hantera order före planeringsstartdatumet | Microsoft Docs"
description: "Det här avsnittet beskriver de regler som gäller för att planera order i den frysta zonen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5545fe1c2c8833eb1c97765f261777cbb1781098
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Designdetaljer: Hantera order före planeringsstartdatumet
För att förhindra att en tillförselplan visar omöjliga och därför oanvändbara förslag, betraktar planeringssystemet perioden fram till planeringsstartdatumet som en fryst zon som inget planeras för. Följande regel gäller för den frysta zonen:  
  
All efterfrågan och tillgång före startdatumet för planeringsperioden anses vara en del av lagret eller levererat.  
  
Planeringssystemet föreslår inte, med ett par undantag, några ändringar av leveransorder i den frysta zonen, och inga orderspårninglänkar skapas eller underhålls för den perioden.  
  
Undantagen till denna regel är enligt följande:  
  
* Om det planerade tillgängliga lagret, inklusive summan av efterfrågan och tillgång i den frysta zonen, är under noll.  
* Om serie-/partinummer krävs på de bakåtdaterade beställningarna.  
* Om uppsättningen tillgång-efterfrågan är kopplad av en order-till-order-princip.  
  
Om det ursprungliga tillgängliga lagret är lägre än noll föreslår planeringssystemet en nödleveransorder leveransorder på dagen före planeringsperioden för att täcka det antal som saknas. Därför kommer det planerade och tillgängliga lagret alltid att vara minst noll när planeringen för den framtida perioden börjar. Planeringsraden för leveransordern ska innehålla en nödvarningsikon och ytterligare information finns i fältet.  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serie-/partinummer och Order-till-order-länkar är undantagna från den frysta zonen  
Om serie-/partinummer krävs eller det finns en order-till-order-länk kommer planeringssystemet att ignorera den frysta zonen och ta med sådana antal som har bakåtdaterats från startdatumet, och föreslår eventuellt korrigerande åtgärder om efterfrågan och tillgång är i obalans. Affärsorsaken till den här principen är att sådana specifika uppsättningar med efterfrågan-tillgång måste matcha för att se till att den aktuella efterfrågan uppfylls.  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
