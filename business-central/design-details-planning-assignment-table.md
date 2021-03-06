---
title: Designdetaljer - Planeringsfördelningstabell | Microsoft Docs
description: Det här avsnittet innehåller information om vad som händer när du ändrar hur du planerar för en artikel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 621e747cbdf4b7ba19ad900c4c91eb3edfd8480f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770894"
---
# <a name="design-details-planning-assignment-table"></a>Designdetaljer: Planeringsfördelningstabell
Alla artiklar ska planeras för, men det finns ingen anledning att beräkna en plan för en artikel om det inte har skett någon ändring i efterfråge- eller tillgångsmönstret sedan senaste gången som en plan beräknades.  

Om användaren har angett en ny försäljningsorder eller har ändrat en befintlig finns det anledning att beräkna om planen. Andra anledningar är en ändring i prognos eller önskat antal i säkerhetslagret. När du ändrar en struktur genom att lägga till eller ta bort en komponent indikerar det troligtvis en ändring, men endast för komponentartikeln.  

För flera lagerställen sker fördelningen på nivån med kombinationen av artikel per lagerställe. Om till exempel en försäljningsorder har skapats vid endast ett lagerställe, kommer programmet att tilldela artikeln vid det specifika lagerstället för planeringen.  

Anledningen för att välja artikel för planeringen är en fråga om systemprestanda. Om ingen ändring i en artikels efterfrågans-/tillgångsmönster har skett kommer planeringssystemet inte att föreslå några åtgärder som ska vidtas. Utan planeringsfördelningen måste systemet utföra beräkningarna för alla artiklar för att avgöra vad som ska planeras för, och det skulle dränera systemresurser.  

Tabellen **Planeringsfördelning** övervakar behovs- och försörjningshändelser och tilldelar lämpliga artiklar för planeringen. Följande händelser övervakas:  

* En ny försäljningsorder, prognos, komponent, inköpsorder, produktionsorder, monteringsorder eller överföringsorder.  
* Ändring av artikel, antal, lagerställe, variant eller datum på en försäljningsorder, prognos, komponent, inköpsorder, produktionsorder, monteringsorder eller överföringsorder.  
* Annullering av en försäljningsorder, prognos, komponent, inköpsorder, produktionsorder, monteringsorder eller överföringsorder.  
* Förbrukning av artiklar annat än planerade.  
* Utflöde av andra artiklar än planerade.  
* Oplanerade ändringar i lagret.  

För dessa direkta efterfrågan/tillgång-förflyttningar underhåller orderspårnings- och åtgärdsmeddelandesystemet tabellen Planeringsfördelning och anger en planeringsorsak som ett åtgärdsmeddelande.  

Följande ändringar av huvuddata kan också orsaka en planeringsobalans:  

* Ändring av status till Certifierat i produktionsstrukturhuvudet (för alla artiklar som använder huvudet).  
* Tagit bort rad (underordnat objekt).  
* Ändring av status till Certifierat i verksamhetsföljdhuvudet (för alla artiklar som använder verksamhetsföljden).  
* Ändringar i följande artikelkortfält.  
* Säkerhetslager eller säkerhetsledtid.  
* Ledtidsberäkning.  
* Beställningspunkt.  
* Produktionstrukturnr. (och alla underordnade till gammal strukturreferens).  
* Operationsföljdsnr  
* Partiformningsmetod.  

I de här fallen underhåller en ny funktion, Planera fördelningshantering, tabellen och ange planeringsanledningen som Nettoförändring.  

Följande ändringar orsakar ingen planeringsfördelning:  

* Kalendrar  
* Andra planeringsparametrar på artikelkortet  

När att prod.program eller ett nettobehov beräknas gäller inga begränsningar:  

* Prod.program: Planeringssystemet kontrollerar att artikeln har en efterfrågeprognos eller en försäljningsorder. Om inte, ingår artikeln inte i planen.  
* Nettobehov: Om planeringssystemet identifierar att artikeln fylls på av en nettoplaneringsrad eller nettoleveransorder ska artikeln inte användas i planeringen. Dock inkluderas all efterfrågan från relevanta komponenter.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Överföringar i planering](design-details-transfers-in-planning.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]