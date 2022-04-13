---
title: Designdetaljer – Avrundning
description: Avrundningsrester kan uppstå när du värderar kostnaden för en lagerminskning som har angetts i ett annat antal än motsvarande lagerökning.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 864b7854593fe0b0d8ecb739f580daa7bd035c58
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519283"
---
# <a name="design-details-rounding"></a>Designdetaljer: Avrundning
Avrundningsrester kan uppstå när du värderar kostnaden för en lagerminskning som har angetts i ett annat antal än motsvarande lagerökning. Avrundningsrester beräknas för alla värderingsprinciper när du kör batch-jobbet **Justera kost. artikeltrans**.  

 När du använder värderingsprincipen Genomsnitt beräknas avrundningsresten och registreras enligt en ackumulerad, transaktion-för-transaktion-utgångspunkt.  

 När du använder en annan värderingsprincip än Genomsnitt beräknas avrundningsresten när lagerökningen har kopplats fullständigt, d.v.s när återstående antal för lagerökningen är lika med noll. En separat transaktion skapas sedan för den avrundningsresten, och bokföringsdatumet på avrundningsresten är bokföringsdatumet för den senast fakturerade värdetransaktion för lagerökningen.  

## <a name="example"></a>Exempel  
 Följande exempel visar hur olika avrundningsrester hanteras för genomsnittsvärderingsprincipen och icke-genomsnittvärderingsprincipen. I båda fallen har batch-jobbet **Justera kost – artikeltransaktioner** körts.  

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
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]