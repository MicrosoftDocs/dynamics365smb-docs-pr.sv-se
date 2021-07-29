---
title: Visa tabellinformation
description: Lär dig mer om hur du kan visa information om databaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 581d92010fa566c33775ffd6238ca6e0cfca0837
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443085"
---
# <a name="viewing-table-information"></a>Visa tabellinformation

Sidan **8700 tabellInformation** innehåller information om alla system- och affärstabeller i en Business Central-lösning. I synnerhet visar sidan information om mängden data som tabellerna innehåller.

Den här informationen är användbar för att felsöka prestandaproblem, eftersom du kan se fördelningen av datastorlek över tabeller.

## <a name="viewing-table-information"></a>Visa tabellinformation

Om du vill öppna sidan markerar du ![Sök på sidan eller rapporten.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Tabellinformation** och väljer sedan relaterad länk.

I följande tabell beskrivs de olika tabellerna som anges:

|Kolumn|Beskrivning|
|------|-----------|
|Företagsnamn|Namnet på företaget, om det finns något, som tabellen tillhör.|
|Tabellnamn|Tabellens namn.|
|Tabellnr|ID:t för tabellen.|
|Nr av poster|Det totala antalet poster som lagras i tabellen.|
|Poststorlek|Den genomsnittliga poststorleken i KB/post. Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(No. av poster). |

## <a name="see-also"></a>Se även

[Kontrollera sidor](across-inspect-page.md)  
[Prestandaartiklar för utvecklare](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]