---
title: Designdetaljer - Hantera partiformningsmetoder | Microsoft Docs
description: "Översikt över aktiviteter för att definiera en ombeställningsmetod inom leveransplanering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a>Designdetaljer: Hantera partiformningsmetoder
För att en artikel ska ingå i leveransplanering måste en ombeställningsmetod definieras. Följande fyra partiformningsmetoder finns:  
  
* Fast orderkvantitet  
* Maximalt antal  
* Order  
* Parti-för-parti  
  
Metoderna Fast orderkvantitet och Maximalt antal avser lagerplanering. Även om lagerplaneringen är tekniskt enklare än motkonteringen, måste de här metoderna finnas samtidigt som steg-för-steg-motkontering av tillgångs- och orderspårning. För att kontrollera integrering mellan de två och ge insyn i den komplicerade planeringslogiken finns strikta principer för hur partiformningsmetoder hanteras.  
  
## <a name="in-this-section"></a>I det här avsnittet  
[Designdetaljer: Beställningspunktens roll](design-details-the-role-of-the-reorder-point.md)  
[Designdetaljer: Övervaka den planerade lagernivån och beställningspunkten](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Designdetaljer: Tidsenhetens roll](design-details-the-role-of-the-time-bucket.md)  
[Designdetaljer: Hålla sig under överflödesnivån](design-details-staying-under-the-overflow-level.md)  
[Designdetaljer: Hantera planerat negativt lagersaldo](design-details-handling-projected-negative-inventory.md)  
[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Planeringsfördelningstabell](design-details-planning-assignment-table.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
