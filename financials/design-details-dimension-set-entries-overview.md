---
title: "Översikt över dimensionsuppsättningstransaktioner | Microsoft Docs"
description: "Det här avsnittet beskriver hur dimensionsuppsättningstransaktioner lagras och bokförs i [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53c85ecbb42db92e95921203d24781bcb82f942d
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="dimension-set-entries-overview"></a>Översikt över dimensionsuppsättningstransaktioner
I det här avsnittet beskrivs hur dimensionsuppsättningstransaktioner lagras och bokförs i [!INCLUDE[d365fin](includes/d365fin_md.md)].  
  
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
  
![Dimension – översikt](media/dimensionentrynav7.png "DimensionEntryNAV7")  
  
När du skapar en ny journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden. I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.  
  
När du redigerar och stänger fönstret **Redigera dimensionsuppsättningstrans.**utförs en kontroll för att se om kombinationen av dimensionsvärden finns som en dimensionsuppsättning i tabellen. Om kombinationen finns i tabellen tilldelas motsvarande dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden. Annars läggs en ny dimensionsuppsättning till tabellen och det nya dimensionsuppsättnings-ID:t tilldelats journalraden, dokumenthuvudet eller dokumentraden.  
  
## <a name="performance-improvement"></a>Prestandaförbättring  
Genom att lagra dimensionsuppsättningar en gång i databasen bevaras databasplats och allmänna prestanda förbättras.  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
[Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
[Designdetaljer: Kodenhet 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
[Designdetaljer: Kodexempel på ändrade mönster i ändringar](design-details-code-examples-of-changed-patterns-in-modifications.md)   
[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md)   

