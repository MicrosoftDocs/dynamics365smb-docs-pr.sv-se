---
title: "Designdetaljer - Övervaka den planerade lagernivån och beställningspunkten | Microsoft Docs"
description: "Lär dig hur lagerplanering skiljer mellan planerat lager och planerade tillgängliga lagernivåer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a0e64d96389739c67a9e9f548958fac12e3aca2a
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Designdetaljer: Övervaka den planerade lagernivån och beställningspunkten
Lager är en typ av tillgång, men för lagerplanering skiljer planeringssystemet mellan två lagernivåer:  

* Planerat lager  
* Planerat tillgängligt lager  

## <a name="projected-inventory"></a>Planerat lager  
Från början är planerat lager antalet i bruttolager, inklusive tidigare tillgång och efterfrågan även om den inte är bokförd, när planeringsprocessen startas I framtiden blir det en rörlig planerad lagernivå som underhålls av bruttoantal från framtida tillgång och efterfrågan, eftersom de introduceras längs tidslinjen (reserverade eller fördelade på andra sätt).  

Det planerade lagret används i planeringssystemet för att övervaka beställningspunkt och för att bestämma beställningsantal när du använder partiformningsmetoden Maximalt antal.  

## <a name="projected-available-inventory"></a>Planerat tillgängligt lager  
Det planerade tillgängliga lagret är en del av det planerade lagret som vid en viss tidpunkt är tillgängligt för att uppfylla behov. Det planerade tillgängliga lagret används av planeringsmotorn när du övervakar säkerhetslagernivån.  

Det planerade tillgängliga lagret används i planeringssystemet för att övervaka säkerhetslagernivån, eftersom säkerhetslagret alltid måste vara tillgänglig för att uppfylla oväntad efterfrågan.  

## <a name="time-buckets"></a>Tidsenheter  
Om du vill ha en noggrann styrning planerat lager är det avgörande att identifiera när beställningspunkten överstigs och att beräkna rätt partistorlek när du använder partiformningsmetoden Maximalt antal.  

Som angavs tidigare beräknas den planerade lagernivån i början av planeringsperioden. Det är en bruttonivå som inte beaktar reservationer och liknande fördelningar. För att övervaka den här lagernivån under planeringsföljden övervakar systemet de samlade ändringarna över en tidsperiod, en tidsenhet. Systemet ser till att tidsenheten är minst en dag, eftersom det är mest den exakta tidsenheten för en efterfrågan- eller tillgångshändelse.  

## <a name="determining-the-projected-inventory-level"></a>Fastställa den planerade lagernivån  
Följande sekvens beskriver hur den planerade lagernivån fastställs:  

* När en tillförselhändelse, t.ex. en inköpsorder har planerats fullständigt kommer det att öka det planerade lagret på förfallodatumet.  
* När en begäranhändelse har blivit fullständigt uppfylld kommer den inte att minska det planerade lagret direkt. I stället bokförs en minska-påminnelse, vilket är en intern post som innehåller datumet och antalet som läggs till i det planerade lagret.  
* När en efterföljande tillförselhändelse planeras och placeras på tidslinjen, utforskas de bokförda minska-påminnelserna en och en fram tills det planerade datumet för leveransen, medan det planerade lagret uppdateras. Under processen kan beställningspunktsnivån för den interna ökningspåminnelsen ha nåtts eller passerats.  
* Om en ny leveransorder introduceras kontrollerar systemet om den har angetts före den aktuella tillgången. Om det är det, blir den nya tillgången aktuell tillgång och balanseringsproceduren börjar om.  

Följande visar en grafisk illustration av den här principen:  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. Tillgång **Sa** of 4 (fast) stänger Efterfrågan **Da** of -3.  
2. CloseDemand: Skapa en minska-påminnelse på -3 (visas inte).  
3. Tillgång **Sa** har stängts med ett överskott på 1 (inget mer behov finns).  

     Det här ökar den planerade lagernivån till +4, medan det planerade **tillgängliga** lagret blir -1.  

4. Nästa tillgång **Sb** av 2 (en annan order) redan har placerats på tidsplanen.  
5. Systemet kontrollerar om det finns någon minska-påminnelse som föregår **Sb** (det finns det inte, så ingen åtgärd vidtas).  
6. Systemet stänger tillgång **Sb** (ingen mer efterfrågan finns)—antingen A: genom att minska den till 0 (annullera) eller B: genom att låta den vara som den är.  

     Ökar den planerade lagernivån (A: +0 => +4 or B: +2 = +6).  

7. System gör en sista kontroll: Finns det någon minska-påminnelse? Ja, det finns ett på datumet för **Da**.  
8. Programmet lägger till minska-påminnelsen på -3 påminnelse till den planerade lagernivån, antingen A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I händelse av A skapas automatiskt framåtplanerad order som startar på datumet **Da**.  

     I händelse av B når vi beställningspunkten och en ny order skapas.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)

