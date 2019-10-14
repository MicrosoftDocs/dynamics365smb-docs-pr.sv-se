---
title: Skapa filter för dynamiska fördelningsbaser | Microsoft Docs
description: Den dynamiska fördelningsmetoden bygger på värden som kan ändras. Till exempel antalet anställda i ett kostnadsställe eller artiklar som säljs på en kostnadsbärare för en viss tidsperiod. Det finns nio fördefinierade fördelningsbaser och tolv dynamiska datumintervall. Du kan ange olika filter baserade på fördelningsbasen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 1ae73e7808db2f0c9ab9bd4c2567b109ef245490
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305554"
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
|Inköpta artiklar (belopp)|Artikelnummer|Ja|Ja|Ja|Lagerbokföringsmall|  

## <a name="see-also"></a>Se även  
[Definiera och fördela kostnader](finance-define-and-allocate-costs.md)
