---
title: "Skapa filter för dynamiska fördelningsbaser | Microsoft Docs"
description: "Den dynamiska fördelningsmetoden bygger på värden som kan ändras. Till exempel antalet anställda i ett kostnadsställe eller artiklar som säljs på en kostnadsbärare för en viss tidsperiod. Det finns nio fördefinierade fördelningsbaser och tolv dynamiska datumintervall. Du kan ange olika filter baserade på fördelningsbasen."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cd6aaf4ca0c1de1cea400ce5abe434f7c37040f9
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Skapa filter för dynamiska fördelningsbaser
Den dynamiska fördelningsmetoden bygger på värden som kan ändras. Till exempel antalet anställda i ett kostnadsställe eller artiklar som säljs på en kostnadsbärare för en viss tidsperiod. Det finns nio fördefinierade fördelningsbaser och tolv dynamiska datumintervall. Du kan ange olika filter baserade på fördelningsbasen.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Skapa filter för dynamiska fördelningsbaser  
 Följande tabell visar vilka filter är möjliga för olika fördelningsbaser och vilka värden som gäller i fälten **Nummerfilter** och **Gruppfilter**. Tryck på F1 i fälten **Kod för datumfilter** om du vill läsa detaljerad beskrivningar.  

|**Bas**|**Nummerfilter**|**Kod för datumfilter**|**Filter för kostnadsställe**|**Filter för kostnadsbärare**|**Gruppfilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Redovisningstransaktioner|Redovisningskonto|Ja|Ja|Ja|Inte tillämpligt|  
|Redov.budgettransaktioner|Redovisningskonto|Ja|Ja|Ja|Redov.budgetnamn|  
|Kostnadstypstransaktioner|Kostnadstyp|Ja|Ja|Ja|Inte tillämpligt|  
|Kostnadsbudgettransaktioner|Kostnadstyp|Ja|Ja|Ja|Budgetnamn|  
|Antal anställda|Inte tillämpligt|Ja|Ja|Ja|Inte tillämpligt|  
|Sålda artiklar (antal)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  
|Inköpta artiklar (antal)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  
|Sålda artiklar (belopp)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  
|Inköpta artiklar (belopp)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  

## <a name="see-also"></a>Se även  
 [Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Skapa fördelningskälla och mål](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definiera och fördela kostnader](finance-define-and-allocate-costs.md)

