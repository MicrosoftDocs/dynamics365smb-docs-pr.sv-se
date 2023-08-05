---
title: Om kostnader för färdiga produktionsorder
description: Att slutföra produktionsordern är nyckeln till att slutföra kostnadslivscykeln för en produktionsartikel. Slutliga kostnader beräknas i batch-jobbet Justera kostnadsartikeltransaktioner.
author: SorenGP
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: edupont
---
# Om kostnader för färdiga produktionsorder

Att färdigställa produktionsordern är en viktig uppgift när det gäller att slutföra livscykeln för kostnadsberäkning för artikeln som tillverkas. Slutkostnader, inklusive avvikelser i standardkostnad, faktiska värden i en FIFO, genomsnittlig eller LIFO-kostnad, beräknas med hjälp av batch-jobbet **Justera kostnad – artikeltransaktioner** som används för avstämning av kostnaderna för produktionsartiklar. Om kostnadsjustering ska genomföras för en produktionsorder måste statusen vara **Färdig**. Det är därför viktigt att vid slutförande ändra statusen för en produktionsorder till **Färdig**.  

## Exempel

Vid standardkostnad, när du t. ex. förbrukar material för att producera en artikel, överförs förenklat kostnaden för artikeln plus arbets- och overheadkostnader till PIA. När artikeln tillverkas minskar PIA med beloppet för standardkostnaden för artikeln. De här kostnaderna får vanligtvis inte nollnetto. För att dessa kostnader inte ska få nollnetto måste du köra batchjobbet **Justera kostnad – artikeltransaktiner** och notera att endast produktionsorder med statusen **Färdig** ska beaktas för justering.  

## Se även

[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]