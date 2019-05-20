---
title: Designdetaljer - Prioritera order | Microsoft Docs
description: Mer information om hur du prioriterar för att täcka både krav för efterfrågan och tillgång.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 06eb5221369d8777330ae844adfb5d87658d591d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238630"
---
# <a name="design-details-prioritizing-orders"></a>Designdetaljer: Prioritera order
Inom en given lagerställeenhet representerar det begärda eller tillgängliga datumet den högsta prioriteten. Dagens efterfrågan ska hanteras före nästa veckas efterfrågan. Men utöver den här allmänna prioriteten föreslår planeringssystemet också vilken typ av efterfrågan som ska uppfyllas innan övrig efterfrågan uppfylls. På samma sätt kommer det att föreslå vilken tillgångskälla som ska kopplas innan du kopplar andra tillgångskällor. Det utförs i enlighet med orderprioriteter.  
  
Den laddade efterfrågan och tillgången bidrar till en profil för planerade lagret enligt följande prioriteter:  
  
## <a name="priorities-on-the-demand-side"></a>Prioriteter på efterfråganssidan  
1. Redan levererat: Artikeltransaktion  
2. Inköpsreturorder  
3. Reservationstransaktion  
4. Tjänsteorder  
5. Produktionskomponentbehov  
6. Monteringsorderrad  
7. Avgående överföringsorder  
8. Avropsorder (som inte redan har förbrukats av motsvarande försäljningsorder)  
9. Prognos (som inte redan har förbrukats av andra försäljningsorder)  
  
> [!NOTE]  
>  Köpreturer ingår vanligtvis inte i tillförselplanläggning; de ska alltid reserverats från partiet som ska returneras. Om de inte har reserverats spelar inköpsreturer en roll i dispositionen och är högt prioriterade för att undvika att planeringssystemet föreslår en leveransorder bara för att hantera en inköpsretur.  
  
## <a name="priorities-on-the-supply-side"></a>Prioriteter på tillgångssidan  
1. Finns redan i lager: Artikeltransaktion (Planeringsflexibilitet = Ingen)  
2. Försäljningsreturorder (planeringsflexibilitet = ingen)  
3. Ankommande överföringsorder  
4. Produktionsorder  
5. Monteringsorder  
6. Inköpsorder  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioritet kopplad till status för efterfrågan och tillgång  
Förutom prioriteter som anges av typen av efterfrågan och tillgång, definierar ordrarnas aktuella status i körningsprocessen också en prioritet. Till exempel har lageraktiviteter en inverkan, och status för försäljningar, köp, överföringar, montering och produktionsorder tas med i beräkningen:  
  
1. Hanteras delvis (planeringsflexibilitet = ingen)  
2. Redan pågående i distributionslagret (Planeringsflexibilitet = Ingen)  
3. Släppt – alla ordertyper (Planeringsflexibilitet = Obegränsad)  
4. Fast planerad produktionsorder (Planeringsflexibilitet = Obegränsad)  
5. Planerad/öppen – alla ordertyper (Planeringsflexibilitet = Obegränsad)  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)