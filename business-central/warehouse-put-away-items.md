---
title: Införa artiklar
description: Införa artiklar efter att de har inlevererats eller producerats utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5770, 5783, 5784, 5786, 5795, 7334, 7352, 7354, 7356, 7375, 7379, 7390, 7394, 7396, 9312, 9315, 9343
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 668655e5452d36ef460c9bfcbc409986d20215b0
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533058"
---
# <a name="putting-items-away"></a>Införa utflöde från artiklar

Lageraktiviteten att införa artiklar efter att de har inlevererats eller producerats utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats. Hur komplex det är kan sträcka sig från inga lagerkonfigurationer, till grundläggande lagerstyrning med hantering av order för order i en eller flera aktiviteter samt avancerade konfigurationer där alla lageraktiviteter måste utförs i ett dirigerat arbetsflöde. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Om du vill organisera och registrera införselaktiviteter med distributionslagerdokument markerar du fältet **Begär artikelinförsel** på lagerställekortet. Det indikerar att om du har artiklar som kommer till lagerstället via ett inkommande källdokument, ska införseln av artiklarna hanteras via, och kontrolleras av programmet. Det inkommande källdokumentet kan vara in inköpsorder, en försäljningsreturorder, en inkommande överföringsorder eller en produktionsorder vars utflöde är klart för artikelinförsel.  

Om lagerstället kräver artikelinförselbearbetning, men inte kräver inleveransbearbetning, använder du sidan **Lagerartikelinförsel** om du vill organisera eller skriva ut information om artikelinförseln, ange resultat av faktisk artikelinförsel eller bokföra artikelinförselinformation. Om du bokför artikelinförselinformation bokförs i sin tur inleveransinformationen för källdokumentet.

Om lagerstället kräver både inleveransbearbetning och artikelinförselbehandling, så att du har placerat markeringar i både **Begär inleveranser** och **Begär artikelinförsel** på lagerställekortet, finns det en annan process som används för att införa artiklar. I det här fallet ska du använda sidan **Dist.lager artikelinförsel** för att hantera artikelinförsel. Dist.lager artikelinförsel fungerar på samma sätt som Lagerartikelinförsel, förutom att du registrerar artikelinförseln istället för att bokföra informationen. Observera att registrering av artikelinförsel inte bokför inleveransen för artiklarna. Den uppdateras bara lagerställesinnehåll. Du lagerchef kan du använda ett artikelinförselkalkylark för att organisera artikelinförselinformationen innan du skapar de individuella artikelinförselinstruktionerna.

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Bokför inleveransen av artiklar direkt från det inkommande orderdokumentet och därmed registrera införseln, eftersom det finns någon lagerkonfiguration.|[Ta emot artiklar](warehouse-how-receive-items.md)|  
|Införa artiklar order för order och bokföra inleveransen i samma aktivitet, i en grundläggande lagerkonfiguration.|[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Införa artiklar för flera order i en avancerad lagerkonfiguration.|[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Införa producerade eller monterade artiklar i en grundläggande eller avancerad lagerkonfiguration.|[Föra in produktions- eller monteringsutflöde](warehouse-how-to-put-away-production-output.md)|
|Planera optimerade införselinstruktioner för ett antal bokförda lagerinleveranser i stället för att lagerarbetare agerar direkt på inleveranser.|[Planera artikelinförsel i kalkylark](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Lägga tillbaka artiklar som har plockats tekniskt med en intern plockning, till exempel för en produktionsorder som inte förbrukat det förväntade antalet.|[Plocka och lagra utan källdokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Dela upp en införselrad för att placera en del av införselantalet på tillgängliga lagerställen eftersom den bestämda lagerstället är full.|[Dela rader för dist.lageraktivitet](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få direkt tillgång till införslar som tilldelats dig som lagerarbetare.|[Hitta distributionslagerfördelningar](warehouse-how-to-find-your-warehouse-assignments.md)|

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/receive-put-away-items/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
