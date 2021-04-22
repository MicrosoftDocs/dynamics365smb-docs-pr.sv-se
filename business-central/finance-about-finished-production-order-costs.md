---
title: Om kostnader för färdiga produktionsorder | Microsoft Docs
description: Att färdigställa produktionsordern är en viktig uppgift när det gäller att slutföra livscykeln för kostnadsberäkning för artikeln som tillverkas. Slutkostnader (inklusive avvikelser i standardkostnad, faktiska värden i en FIFO, genomsnittskostnader eller LIFO-kostnader) beräknas med hjälp av batch-jobbet Justera kostnad – Artikeltrans.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b250a495504272b93565752043c23e1988ca1dab
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781067"
---
# <a name="about-finished-production-order-costs"></a>Om kostnader för färdiga produktionsorder
Att färdigställa produktionsordern är en viktig uppgift när det gäller att slutföra livscykeln för kostnadsberäkning för artikeln som tillverkas. Slutkostnader, inklusive avvikelser i standardkostnad, faktiska värden i en FIFO, genomsnittlig eller LIFO-kostnad, beräknas med hjälp av batch-jobbet **Justera kostnad – artikeltransaktioner** som används för avstämning av kostnaderna för produktionsartiklar. Om kostnadsjustering ska genomföras för en produktionsorder måste statusen vara **Färdig**. Det är därför viktigt att vid slutförande ändra statusen för en produktionsorder till **Färdig**.  

## <a name="example"></a>Exempel  
 Vid standardkostnad, när du t. ex. förbrukar material för att producera en artikel, överförs förenklat kostnaden för artikeln plus arbets- och overheadkostnader till PIA. När artikeln tillverkas minskar PIA med beloppet för standardkostnaden för artikeln. De här kostnaderna får vanligtvis inte nollnetto. För att dessa kostnader inte ska få nollnetto måste du köra batchjobbet **Justera kostnad – artikeltransaktiner** och notera att endast produktionsorder med statusen **Färdig** ska beaktas för justering.  

## <a name="see-also"></a>Se även  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]