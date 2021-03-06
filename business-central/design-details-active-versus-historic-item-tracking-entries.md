---
title: Designdetaljer - Aktiva kontra historiska artikelspårningstransaktioner | Microsoft Docs
description: När delar av ett dokumentradantal bokförs överförs endast det aktuella antalet till artikeltransaktionerna och dess artikelspårningsnummer. Emellertid kommer du att vilja få tillgång till all relevant information om artikelspårning direkt från den aktiva dokumentraden. Det vill säga, du vill inte bara visa transaktionerna som är relaterade till återstående antal, du vill även ha information om de enheter som har bokförts. När du visar eller ändrar sidan **Artikelspårningsrader** visas det samlade innehållet i tabellen **Spårningsspecifikation** (T336) och tabellen **Reservationstransaktion** (T337) i en tillfällig version av T336. Detta säkerställer att historiska och aktiva artikelspårningsdata nås som en.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 587c396bece9437e170912dc523bebb04a39e1e4
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216034"
---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner
När delar av ett dokumentradantal bokförs överförs endast det aktuella antalet till artikeltransaktionerna och dess artikelspårningsnummer. Emellertid kommer du att vilja få tillgång till all relevant information om artikelspårning direkt från den aktiva dokumentraden. Det vill säga, du vill inte bara visa transaktionerna som är relaterade till återstående antal, du vill även ha information om de enheter som har bokförts. När du visar eller ändrar sidan **Artikelspårningsrader** visas det samlade innehållet i tabellen **Spårningsspecifikation** (T336) och tabellen **Reservationstransaktion** (T337) i en tillfällig version av T336. Detta säkerställer att historiska och aktiva artikelspårningsdata nås som en.  

 Följande tabell visar hur T336 och T337 används i ett inköpsscenario. De fetstilta siffrorna representerar värden som användaren skriver in manuellt på sidan **Artikelspårningsrader**.  

 Moment 1: Skapa en inköpsorderrad med sju stycken med artikelspårningsnummer.  

||**Antal (bas)**|**Ant. att hantera**|**Ant. att faktureras (bas)**|**Antal hanterat (bas)**|**Antal fakturerat (bas)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Moment 2: Ta emot fyra stycken.  

||**Antal (bas)**|**Ant. att hantera**|**Ant. att faktureras (bas)**|**Antal hanterat (bas)**|**Antal fakturerat (bas)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Sidan **artikelspårningsrader**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Moment 3: Ta emot två stycken och fakturera två stycken.  

||**Antal (bas)**|**Ant. att hantera**|**Ant. att faktureras (bas)**|**Antal hanterat (bas)**|**Antal fakturerat (bas)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Sidan **artikelspårningsrader**|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Moment 4: Ta emot ett stycke.  

||**Antal (bas)**|**Ant. att hantera**|**Ant. att faktureras (bas)**|**Antal hanterat (bas)**|**Antal fakturerat (bas)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Sidan **artikelspårningsrader**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fakturera 5 stycken.  

||**Antal (bas)**|**Ant. att hantera**|**Ant. att faktureras (bas)**|**Antal hanterat (bas)**|**Antal fakturerat (bas)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Sidan **artikelspårningsrader**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Objektspårning](design-details-item-tracking.md)   
 [Designdetaljer - Sida för artikelspårningsrader](design-details-item-tracking-lines-window.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]