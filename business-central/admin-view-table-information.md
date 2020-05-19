---
title: Visa tabellinformation
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275324"
---
# <a name="viewing-table-information"></a>Visa tabellinformation

Sidan **8700 tabellInformation** innehåller information om alla system- och affärstabeller i en Business Central-lösning. I synnerhet visar sidan information om mängden data som tabellerna innehåller.

Den här informationen är användbar för att felsöka prestandaproblem, eftersom du kan se fördelningen av datastorlek över tabeller.

## <a name="viewing-table-information"></a>Visa tabellinformation

Du öppnar den här sidan genom att välja ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **tabellinformation** och sedan välja relaterad länk.

I följande tabell beskrivs de olika tabellerna som anges:

|Kolumn|Beskrivning|
|------|-----------|
|Företagsnamn|Namnet på företaget, om det finns något, som tabellen tillhör.|
|Tabellnamn|Tabellens namn.|
|Tabellnr|ID:t för tabellen.|
|Nr av poster|Det totala antalet poster som lagras i tabellen.|
|Poststorlek|Den genomsnittliga poststorleken i KB/post. Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(antal poster). |

## <a name="see-also"></a>Se även

[Kontrollera sidor](across-inspect-page.md)  
[Prestandaartiklar för utvecklare](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
