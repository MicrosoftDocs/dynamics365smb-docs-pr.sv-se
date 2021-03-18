---
title: Designdetaljer - Lagerperioder | Microsoft Docs
description: Bakåtdaterade transaktioner eller kostnadsjusteringar påverkar ofta saldon och lagervärderingar för bokföringsperioder som kanske anses vara stängda. Det kan ha negativ effekt på exakt rapportering, särskilt i globala företag. Funktionen Lagerperioder kan användas för att undvika sådana problem genom att öppna eller att stänga lagerperioder för att begränsa bokföring i en fastställd tidsperiod.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a38c82772d13ec2075bf3e2661126049c543eca
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389880"
---
# <a name="design-details-inventory-periods"></a>Designdetaljer: Lagerperioder
Bakåtdaterade transaktioner eller kostnadsjusteringar påverkar ofta saldon och lagervärderingar för bokföringsperioder som kanske anses vara stängda. Det kan ha negativ effekt på exakt rapportering, särskilt i globala företag. Funktionen Lagerperioder kan användas för att undvika sådana problem genom att öppna eller att stänga lagerperioder för att begränsa bokföring i en fastställd tidsperiod.  

 En lagerperiod är en period som definieras av ett slutdatum, där du bokför lagringstransaktioner. När du stänger en lagerperiod kan inga värdeändringar bokföras i den stängda perioden. Det innefattar nya värdebokföringar, förväntade eller fakturerade bokföringar, ändringar i befintliga värden och kostnadsjusteringar. Du kan dock fortfarande koppla till en öppen artikeltransaktion som återfinns inom den stängda perioden. Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md).  

 För att se till att alla transaktionsartiklar i en stängd period är slutliga, måste följande villkor uppfyllas innan en lagerperiod kan stängas:  

-   Alla avgående artikeltransaktioner under perioden måste avslutas (inget negativt lager).  
-   Alla objektkostnader i perioden måste justeras.  
-   Alla utsläppta och färdiga produktionsorder i perioden måste kostnadsjusteras.  

 När du stänger en lagerperiod skapas en lagerperiodtransaktion genom att använda numret på den sista artikeljournalen i lagerperioden. Dessutom registreras tiden, datumet och användarkoden för den användare som avslutar perioden i lagerperiodtransaktionen. Genom att använda information tillsammans med den sista artikeljournalen för föregående period kan du se vilka lagertransaktioner som bokfördes under lagerperioden. Det är också möjligt att öppna lagerperioder igen om du behöver bokföra i en stängd period. När du öppnar en lagerperiod igen skapas en lagerperiodtransaktion.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lager och kostnadskalkylering](design-details-inventory-costing.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md) [Ekonomi](finance.md)  
 [Arbeta med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]