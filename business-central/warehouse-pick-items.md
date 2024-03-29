---
title: Plocka artiklar
description: Aktiviteten att plocka artiklar innan de har levererats eller förbrukats utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5779, 5798, 7343, 7345, 7357, 7359, 7377, 7392, 7395, 7397, 9313, 9316, 9344
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 07cb13480146496c7186cef2d845c4a799eb699a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535590"
---
# <a name="pick-items"></a>Plocka artiklar

Lageraktiviteten att plocka artiklar innan de har levererats eller förbrukats utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats. Hur komplex det är kan sträcka sig från inga lagerkonfigurationer, till grundläggande lagerstyrning med hantering av order för order i en eller flera aktiviteter samt avancerade konfigurationer där alla lageraktiviteter måste utförs i ett dirigerat arbetsflöde. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Om du vill organisera och registrera plockningsaktiviteter med distributionslagerdokument, markerar du fältet **Begär plockning** på lagerställekortet. Det indikerar att artiklar som ska plockas för ett utgående källdokument, ska hanteras via, och kontrolleras av systemet. Ett utgående källdokument kan vara en försäljningsorder, en inköpsreturorder, en utgående överföringsorder, en serviceorder eller en produktionsorder med komponenter som ska plockas.

> [!NOTE]
> Även om inställningarna kallas **Begär plockning**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.

Om lagerstället kräver plockningsbearbetning, men inte kräver utleveransbehandling, använder du sidan **Lagerplockning** om du vill organisera eller skriva ut information om artikelplockning, ange resultat av plockningen eller bokföra plockningsinformation, som i sin tur bokför leverans av artiklarna. Om det gäller att plocka komponenter för en produktionsorder, bokför bokföringen av plockning också förbrukningen.

Om lagerstället kräver både plocknings- och utleveransbearbetning, det vill säga om både fältet **Begär plockning** och fältet **Kräv utleverans** har markerats på lagerställekortet, använder du sidan **Dist.lager plockning** för att hantera plockningen. Dist.lagerplockning fungerar på samma sätt som lagerplockning, förutom att plockningen registreras i stället för att plockningsinformationen bokförs. I den här registreringsprocessen bokförs inte leveransen, men artiklarna blir tillgängliga för leverans. Du lagerchef kan du använda ett plockningskalkylark för att organisera plockninginformation innan du skapar de individuella plockningsinstruktionerna för lager.

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|
|------------|-------------|  
|Bokföra utleveransen av artiklar direkt på det utgående orderdokumentet eftersom det inte finns några lagerfunktioner. (Fungerar på samma sätt för en försäljningsorder, en utgående överföringsorder och returutleveranser.)|[Leverera artiklar](warehouse-how-ship-items.md)|  
|Plocka artiklar order för order och bokföra utleveransen i samma aktivitet, i en grundläggande lagerkonfiguration.|[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Plocka artiklar för flera order i en avancerad lagerkonfiguration.|[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Plocka komponenter för produktion eller montering i en grundläggande lagerkonfiguration.|[Plocka för produktion eller montering i grundläggande distributionslagerkonfiguration](warehouse-how-to-pick-for-production.md)|
|Plocka komponenter för produktion eller montering i en avancerad lagerkonfiguration.|[Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)|  
|Planera optimerade plockinstruktioner för ett antal utleveranser i stället för att låta lagerarbetare agera direkt på bokförda utleveranser.|[Planera plockningar i kalkylark](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Plocka artiklar tekniskt för ett visst syfte, till exempel en produktionsenhet som behöver extra komponenter, så att artiklarna inte lämnar distributionslagret tekniskt.|[Plocka och lagra utan källdokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Förstå hur du automatiskt plockar artiklar enligt deras utgångsdatum, till exempel ömtåliga varor.|[Plockning med FEFO](warehouse-picking-by-fefo.md)|
|En plockningsrad delas upp i flera rader, till exempel eftersom det inte finns tillräckligt många artiklar som ska tas från den bestämda lagerstället.|[Dela rader för dist.lageraktivitet](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få direkt tillgång till plockningar som tilldelats dig som lagerarbetare.|[Hitta distributionslagerfördelningar](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
