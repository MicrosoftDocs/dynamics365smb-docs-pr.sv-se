---
title: Översikt över dimensionsuppsättningstransaktioner | Microsoft Docs
description: I det här avsnittet beskrivs hur dimensionsuppsättningstransaktioner lagras och bokförs i Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 40f6a55adc0c2ade279638b43136475d81cb2c58
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751686"
---
# <a name="dimension-set-entries-overview"></a>Översikt över dimensionsuppsättningstransaktioner
I det här avsnittet beskrivs hur dimensionsuppsättningstransaktioner lagras och bokförs i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="dimension-sets"></a>Dimensionsuppsättningar  
En dimensionsuppsättning en är en unik kombination av dimensionsvärden. Den lagras som dimensionsuppsättningstransaktioner i databasen. Varje dimensionsuppsättningstransaktion representerar ett enstaka dimensionsvärde. Dimensionsuppsättningen identifieras av ett gemensamt dimensionsuppsättnings-ID som tilldelats varje dimensionsuppsättningstransaktion som tillhör dimensionsuppsättningen.  

Följande exempel visar när en dimensionsuppsättning som har tre dimensionsuppsättningstransaktioner. Dimensionsuppsättningen identifieras av ett dimensionsuppsättnings-ID som är 108.  

|Dimensionsuppsättnings-ID|Dimensionskod|Dimensionsvärdekod|Dimensionsvärdesnamn|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|OMRÅDE|70|Nordamerika|  
|108|RÖRELSEMALL|Home|Start|  
|108|AVDELNING|FÖRSÄLJNING|FÖRS|  

## <a name="dimension-set-entries"></a>Dimensionsuppsättningstrans.  
Dimensionsuppsättningar lagras i tabellen **Dimensionsuppsättnings transaktion** som dimensionsuppsättningstransaktioner med samma dimensionsuppsättnings-ID.  

![Flöde för dimensionsuppsättningstransaktioner](media/dimensionentrynav7.png "Flöde för dimensionsuppsättningstransaktioner")  

När du skapar en ny journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden. I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.  

När du redigerar och stänger sidan **Redigera dimensionsuppsättningstrans.** utförs en kontroll för att se om kombinationen av dimensionsvärden finns som en dimensionsuppsättning i tabellen. Om kombinationen finns i tabellen tilldelas motsvarande dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden. Annars läggs en ny dimensionsuppsättning till tabellen och det nya dimensionsuppsättnings-ID:t tilldelats journalraden, dokumenthuvudet eller dokumentraden.

## <a name="codeunit-408-dimension-management"></a>Codeunit 408 Dimensionshantering
Codeunit 408, Dimensionshantering, är ett funktionsbibliotek som hanterar gemensamma uppgifter som är kopplade till dimensioner, till exempel kopiering från en tabell till en annan eller från ett dokument till ett annat.

## <a name="performance-improvement"></a>Prestandaförbättring  
Genom att lagra dimensionsuppsättningar en gång i databasen bevaras databasplats och allmänna prestanda förbättras.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
[Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md)   
