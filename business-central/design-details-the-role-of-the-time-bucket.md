---
title: Designdetaljer - Tidsenhetens roll | Microsoft Docs
description: "Avsikten med tidsenheten är samla efterfråganshändelser i tidssidan för att skapa en gemensam leveransorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: ff748a192d8d1650a708ab70ec33ccc7bfd53c48
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Designdetaljer: Tidsenhetens roll
Avsikten med tidsenheten är samla efterfråganshändelser i tidssidan för att skapa en gemensam leveransorder.  

 För partiformningsmetoder som använder en beställningspunkt kan du ange en tidsenhet. Detta säkerställer att efterfrågan inom samma tidsperiod har ackumulerats innan inverkan på planerat lager kontrolleras och om beställningspunkten har passerats. Om beställningspunkten har passerats framåtplaneras en ny leveransorder från slutet av perioden som definieras av tidsenheten. Tidsenheten börjar på planeringsstartdatumet.  

 Konceptet med tidsenhet återspeglar den manuella processen för att kontrollera lagernivån ofta istället för vid varje transaktion. Användaren måste definiera frekvens (tidsenheten). Till exempel samlar användaren alla artikelbehov från en leverantör att göra en veckobeställning.  

 ![Exempel på tidsperiod i planeringen](media/nav_app_supply_planning_2_reorder_cycle.png "Exempel på tidsperiod i planeringen")  

 Tidsenhet används allmänt för att undvika en kaskadeffekt. Till exempel skapas en balanserad rad med efterfrågan och tillgång där en tidig efterfrågan annulleras, eller ny skapas. Resultatet skulle vara att varje leveransorder (utom den sista) omplaneras.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
 [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
 [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)

