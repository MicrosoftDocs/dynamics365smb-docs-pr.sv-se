---
title: Översikt över bokföring av rad i redovisningsjournalen | Microsoft Docs
description: Detta avsnitt introducerar ändringar i Kodmodul 12, **Gen. Jnl.-Post Line**, som utgör det huvudsakliga programobjektet för redovisningstransaktioner och är den enda plats där transaktioner för redovisning, moms samt kund- och leverantörsreskontra kan föras in.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215259"
---
# <a name="general-journal-post-line-overview"></a>Översikt över bokföring av rad i redovisningsjournalen

Kodmodul 12, **Redovisningsjnl – bokför rad**, är det större programobjektet för redovisningsbokföring och är den enda plats där redovisning, moms, kund- och leverantörsreskontraposter kan infogas. Den här kodmodulen används även för alla operationer av typen Verkställ, Ta bort och Återför.  
  
I Microsoft Dynamics NAV 2013 R2 har kodmodulen skapats på grund av att den hade blivit mycket stor, med cirka 7 600 kodrader. Arkitekturen ändrades och kodmodulen har gjorts enklare och mer stabil. Denna dokumentation beskriver ändringarna och tillhandahåller information som du kanske behöver för en uppgradering.  
  
## <a name="old-architecture"></a>Gammal arkitektur  
Den gamla arkitekturen hade följande funktioner:  
  
* Tidigare använder globala variabler i stor utsträckning, vilket ökade risken för dolda fel på grund av variabler med fel omfång.  
* Många långa procedurer (med mer än 100 kodrader) som även hade hög cyklomatisk komplexitet (t. ex. många kapslade instruktioner som CASE, REPEAT och IF) användes, vilket gjorde koden mycket svår att läsa och underhålla.  
* Flera procedurer som endast användes lokalt och endast var avsedda att användas lokalt var inte markerade som lokala.  
* De flesta procedurer hade inga parametrar och använde globala variabler. Vissa använda parametrar och åsidosatta globala variabler med lokaler.  
* Kodmönster för sökning av redovisningskonton och skapande av redovisnings- och momstransaktioner standardiserades inte och varierade mellan olika platser. Det fanns dessutom mycket koddubbletter och bruten symmetri mellan kund- och leverantörskoden.  
* En stor del av koden i kodmodul 12, ungefär 30 procent, är relaterad till kassarabatt och toleransberäkningar även om dessa funktioner inte behövs i många eller länder/regioner.  
* Bokföring, Koppla, Ta bort, Återför, Kassarabatt och Tolerans samt Valutakursjustering har sammanförts i kodmodul 12 med hjälp av en lång lista över globala variabler.  
  
### <a name="new-architecture"></a>Ny arkitektur  
Kodmodul 12 i [!INCLUDE[prod_short](includes/prod_short.md)] innehåller följande förbättringar:  
  
* Kodmodul 12 har omstrukturerats till mindre procedurer (alla mindre än 100 kodrader).  
* Standardiserade mönster för sökning efter redovisningskonton har implementeras genom att använda hjälpfunktioner från bokföringsmalltabeller.  
* Ett bokföringsmotorramverk har implementerats för att hantera start och avslutande av transaktioner och för att isolera skapandet i redovisningen och momstransaktioner, insamlingen av momsjustering och beräkningen av ytterligare valutabelopp.  
* Kodduplicering har eliminerats.  
* Många hjälpfunktioner har överförts till motsvarande transaktionstabeller för kund- och leverantörsreskontra.  
* Användningen av globala variabler har minimerats så att varje procedur använder parametrar och kapslar in sin programlogik.  
  
## <a name="see-also"></a>Se även

[Designdetaljer: Bokföringsgränssnittsstruktur](design-details-posting-interface-structure.md)  
[Designdetaljer: Bokföringsmotorstruktur](design-details-posting-engine-structure.md)  
[Designdetaljer: redovisningsjournalrad (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]