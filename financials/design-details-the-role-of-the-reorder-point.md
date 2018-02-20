---
title: "Designdetaljer - Beställningspunktens roll | Microsoft Docs"
description: "Det här avsnittet beskriver vikten av att ställa in en beställningspunkt, så att du vet när du ska beställa flera lager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-the-role-of-the-reorder-point"></a>Designdetaljer: Beställningspunktens roll
Förutom allmän balansering av efterfrågan och tillgång måste planeringssystemet också övervaka lagernivåer för de påverkade artiklarna för att respektera de definierade partiformningsmetoderna.  
  
En beställningspunkt representerar efterfrågan under ledtid. När det planerade lagret hamnar under lagernivån som definieras av beställningspunkten är det dags att beställa ytterligare antal. Under tiden förväntas lagret minska gradvis och eventuellt nå noll (eller säkerhetslagernivån), tills återanskaffning anländer.  
  
Planeringssystemet föreslår en framåtplanerad leveransorder när planerat lager hamnar under beställningspunkten.  
  
Beställningspunkten beskriver en viss lagernivå. Lagernivåer kan förändras markant under tidsenheten, och därför måste planeringssystemet ständigt övervaka det planerade tillgängliga lagret.  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
