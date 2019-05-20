---
title: Översikt över bokföring av rad i redovisningsjournalen | Microsoft Docs
description: Detta avsnitt introducerar ändringar i Kodmodul 12, **Gen. Jnl.-Post Line**, som utgör det huvudsakliga programobjektet för redovisningstransaktioner och är den enda plats där transaktioner för redovisning, moms samt kund- och leverantörsreskontra kan föras in.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5fac91190e5a4cea0648f618ea2a9af0afc65fb6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246553"
---
# <a name="general-journal-post-line-overview"></a>Översikt över bokföring av rad i redovisningsjournalen
Kodmodul 12, **Redovisningsjnl – bokför rad**, är det större programobjektet för redovisningsbokföring och är den enda plats där redovisning, moms, kund- och leverantörsreskontraposter kan infogas. Den här kodmodulen används även för alla operationer av typen Verkställ, Ta bort och Återför.  
  
Kodmodulen har förbättrats i varje utgåva under de senaste tio åren, men dess grundläggande arkitektur har förblivit nästan oförändrad. Kodmodulen blev mycket stor, med ungefär 7 600 kodrader. I den här versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] har arkitekturen ändrats och kodmodulen har gjorts enklare och mer stabil. Denna dokumentation introducerar ändringarna och tillhandahåller information som du kanske behöver för en uppgradering.  
  
## <a name="old-architecture"></a>Gammal arkitektur  
Den gamla arkitekturen hade följande funktioner:  
  
* Tidigare använder globala variabler i stor utsträckning, vilket ökade risken för dolda fel på grund av variabler med fel omfång.  
* Många långa procedurer (med mer än 100 kodrader) som även hade hög cyklomatisk komplexitet (t.ex. många kapslade instruktioner som CASE, REPEAT och IF) användes, vilket gjorde koden mycket svår att läsa och underhålla.  
* Flera procedurer som endast användes lokalt och endast var avsedda att användas lokalt var inte markerade som lokala.  
* De flesta procedurer hade inga parametrar och använde globala variabler. Vissa använda parametrar och åsidosatta globala variabler med lokaler.  
* Kodmönster för sökning av redovisningskonton och skapande av redovisnings- och momstransaktioner standardiserades inte och varierade mellan olika platser. Det fanns dessutom mycket koddubbletter och bruten symmetri mellan kund- och leverantörskoden.  
* En stor del av koden i kodmodul 12, ungefär 30 procent, är relaterad till kassarabatt och toleransberäkningar även om dessa funktioner inte behövs i många eller länder/regioner.  
* Bokföring, Koppla, Ta bort, Återför, Kassarabatt och Tolerans samt Valutakursjustering har sammanförts i kodmodul 12 med hjälp av en lång lista över globala variabler.  
  
### <a name="new-architecture"></a>Ny arkitektur  
Kodmodul 12 i [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller följande förbättringar:  
  
* Kodmodul 12 har omstrukturerats till mindre procedurer (alla mindre än 100 kodrader).  
* Standardiserade mönster för sökning efter redovisningskonton har implementeras genom att använda hjälpfunktioner från bokföringsmalltabeller.  
* Ett bokföringsmotorramverk har implementerats för att hantera start och avslutande av transaktioner och för att isolera skapandet i redovisningen och momstransaktioner, insamlingen av momsjustering och beräkningen av ytterligare valutabelopp.  
* Kodduplicering har eliminerats.  
* Många hjälpfunktioner har överförts till motsvarande transaktionstabeller för kund- och leverantörsreskontra.  
* Användningen av globala variabler har minimerats så att varje procedur använder parametrar och kapslar in sin programlogik.  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Bokföringsgränssnittsstruktur](design-details-posting-interface-structure.md)   
[Designdetaljer: Bokföringsmotorstruktur](design-details-posting-engine-structure.md)
