---
title: Designdetaljer - Avrundning | Microsoft Docs
description: "Avrundningsrester kan uppstå när du värderar kostnaden för en lagerminskning som har angetts i ett annat antal än motsvarande lagerökning. Avrundningsrester beräknas för alla värderingsprinciper när du kör batch-jobbet **Justera kost. artikeltrans**."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 39d4bdc430fc74452e7f089c38b28b3214304725
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-rounding"></a>Designdetaljer: Avrundning
Avrundningsrester kan uppstå när du värderar kostnaden för en lagerminskning som har angetts i ett annat antal än motsvarande lagerökning. Avrundningsrester beräknas för alla värderingsprinciper när du kör batch-jobbet **Justera kost. artikeltrans**.  

 När du använder värderingsprincipen Genomsnitt beräknas avrundningsresten och registreras enligt en ackumulerad, transaktion-för-transaktion-utgångspunkt.  

 När du använder en annan värderingsprincip än Genomsnitt beräknas avrundningsresten när lagerökningen har kopplats fullständigt, d.v.s när återstående antal för lagerökningen är lika med noll. En separat transaktion skapas sedan för den avrundningsresten, och bokföringsdatumet på avrundningsresten är bokföringsdatumet för den senast fakturerade värdetransaktion för lagerökningen.  

## <a name="example"></a>Exempel  
 Följande exempel visar hur olika avrundningsrester hanteras för genomsnittsvärderingsprincipen och icke-genomsnittvärderingsprincipen. I båda fallen har batch-jobbet **Justera kost - artikeltransaktioner** körts.  

 Följande tabell visas de artikeltransaktioner som exemplet baseras på.  

|Bokföringsdatum|Antal|Löpnr|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|02-01-20|-1|2|  
|03-01-20|-1|3|  
|04-01-20|-1|4|  

 För en artikel med värderingsprincipen Genomsnitt, beräknas återstående avrundning (1/300) med den första minskningen (löpnummer 2) och förs vidare till nummer 3. Löpnummer 3 är därför värderade till –3,34.  

 Följande tabell visar de resulterande värdetransaktionerna.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3.33|2|2|  
|03-01-20|-1|-3.34|3|3|  
|04-01-20|-1|-3.33|4|4|  

 För en artikel som använder en annan värderingsprincip än Genomsnitt beräknas avrundningsresten (0,01) när det återstående antalet för lagerökningen är noll. Avrundningsresten har en separat transaktion (nummer 5).  

 Följande tabell visar de resulterande värdetransaktionerna.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3.33|2|2|  
|03-01-20|-1|-3.33|3|3|  
|04-01-20|-1|-3.33|4|4|  
|01-01-20|0|-0.01|1|5|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)   
 [Designdetaljer: värderingsprinciper](design-details-costing-methods.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

