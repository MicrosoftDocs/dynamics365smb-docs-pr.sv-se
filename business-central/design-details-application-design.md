---
title: Designdetaljer för program
description: Innehållet består av detaljerad teknisk information om komplexa programfunktioner i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/26/2021
ms.author: edupont
---
# <a name="application-design-details"></a>Designdetaljer för program

Artiklarna i detta avsnitt innehåller detaljerad teknisk information om komplexa programfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)].  

Designdetaljinnehåll är avsett för genomförare, utvecklare och super users, som behöver en djupare insikt för att implementera, anpassa, eller ställa in funktionerna i fråga.  

|**Om du vill**|**Se**|  
|------------|-------------|  
|Förstå mekanismer i värderingsmotorn, till exempel värderingsprincip och kostnadsjustering och vilka redovisningsprinciper de har utformats för.|[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)|  
|Lär dig hur batch-jobbet Justera Kostnad – Artikeltransaktioner används för att identifiera och tilldela ett bokföringsdatum till de värdetransaktioner som batchjobbet håller på att skapa.|[Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen](design-details-inventory-adjustment-value-entry-posting-date.md)|
|Lär dig mer om designen för att lagra och bokföra dimensioner, inklusive kodexempel på hur du migrerar och uppgraderar dimensionskod.|[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md)|
|Lär dig hur planeringssystemet fungerar och hur du justerar algoritmerna för att uppfylla planeringskrav i olika miljöer.|[Designdetaljer: Leveransplanering](design-details-supply-planning.md)|  
|Lär dig systemet måste ha en konstant kontroll på artikeltillgänglighet i distributionslagret, så att avgående beställningar kan flöda effektivt och ge bästa möjliga leveranser.|[Designdetaljer: Disposition i distributionslagret](design-details-availability-in-the-warehouse.md)|
|Lär dig mer om historisk och aktuella utformning av artikelspårningfunktionen och hur den integreras med reservationssystemet för ta med serie-/partinummer i dispositionsberäkningarna.|[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)|  
|Lära dig mer om funktionen för bokföringsrad för redovisningsjournal.|[Designdetaljer: Bokföring av rad i redovisningsjournalen](design-details-general-journal-post-line.md)|

## <a name="see-also"></a>Se även

[Planerad](production-planning.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Ställa in komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]
