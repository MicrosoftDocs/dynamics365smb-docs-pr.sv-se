---
title: Visa tabellinformation
description: Lär dig mer om hur du kan visa information om databaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 72e220aa310515c665ce85bd43f4ebd3aac157d0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922273"
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
|Poststorlek|Den genomsnittliga poststorleken i KB/post. Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(No. av poster). |

## <a name="see-also"></a>Se även

[Kontrollera sidor](across-inspect-page.md)  
[Prestandaartiklar för utvecklare](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]