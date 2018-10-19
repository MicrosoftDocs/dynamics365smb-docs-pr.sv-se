---
title: Designdetaljer - Hantera planerat negativt lagersaldo | Microsoft Docs
description: "Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln. När beställningspunkten har passerats är det dags att beställa mer. Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot. Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå."
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
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 25a2017fd91f09a9d7725c68ffaa0df48a041294
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a>Designdetaljer: Hantera planerat negativt lagersaldo
Beställningspunkten uttrycker den förutsedda efterfrågan under ledtiden för artikeln. När beställningspunkten har passerats är det dags att beställa mer. Men det planerade lagret måste vara stort nog för att täcka behovet tills den nya beställningen tas emot. Under tiden ska säkerhetslagret ta hand om förändringar i efterfrågan upp till en angiven servicenivå.  

 Därför anser planeringssystemet att det är ett nödläge om en framtida efterfrågan inte kan uppfyllas från det planerade lagret, eller uttryckt på ett annat sätt, att det planerade lagret blir negativt. Systemet hanterar ett sådant undantag genom att föreslå en ny leveransorder för att uppfylla en del av behovet som inte kan uppfyllas av lager eller annan tillgång. Orderstorleken för den nya leveransordern beaktar inte maximalt lager eller beställningsantal och beaktar inte heller ordermodifierarna Maximal partistorlek, Minsta partistorlek och Partistorleksmultipel. I stället motsvarar det den exakta bristen.  

 Planeringsraden för den här typen av leveransorder ska innehålla en nödvarningsikon och ytterligare information finns i fältet för att informera användaren om situationen.  

 I följande illustration representerar D en nödleveransorder för att justera för ett negativt lagersaldo.  

 ![Förslag på nödplanering för att undvika negativt lagersaldo](media/nav_app_supply_planning_2_negative_inventory.png "Förslag på nödplanering för att undvika negativt lagersaldo")  

1.  Tillgång **A**, initialt planerat lager, är nedanför beställningspunkt.  
2.  En ny framåtplanerad tillgång skapas (**C**).  

     (Antal = Beställningsgräns – Planerad lagernivå)  
3.  Tillgång **A** är stängd efter efterfrågan **B**, som inte täcks helt.  

     (Behov **B** kan försöka schemalägga Tillgång C, men det kommer inte att hända enligt följande tidsenhetsbegreppet.)  
4.  Ny leverans (**D**) skapas för att täcka det återstående antalet i efterfrågan **B**.  
5.  Efterfrågan **B** är stängd (och skapar en betalningspåminnelse till det planerade lagret).  
6.  Den nya tillgången **D** stängs.  
7.  Planerat lager kontrolleras; beställningspunkten har inte passerats.  
8.  Tillgång **C** är stängd (ingen mer efterfrågan finns).  
9. Sista kontroll: Inga utestående lagernivåpåminnelser finns.  

> [!NOTE]  
>  Moment 4 återspeglar hur godkännandesystemet på tidigare versioner än Microsoft Dynamics NAV 2009 SP1.  

 Detta slutför beskrivningen av centrala principer för lagerplanering baserat på partiformningsmetoder. Följande avsnitt beskriver egenskaperna för de fyra partiformningsmetoderna som stöds.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
 [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
 [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)

