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
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: fcf97328900bb21a85be51452b9e86da8398d195
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808200"
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
