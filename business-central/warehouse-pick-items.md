---
title: Plocka artiklar | Microsoft Docs
description: Lageraktiviteten att plocka artiklar innan de har levererats eller förbrukats utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats. Hur komplexa inställningarna är kan sträcka sig från inga lagerfunktioner, till grundläggande lagerkonfigurationer med enbart hantering av order för order i en eller flera aktiviteter och vidare till avancerade konfigurationer där alla lageraktiviteter måste utföras i ett dirigerat arbetsflöde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2020
ms.author: sgroespe
ms.openlocfilehash: a19496eafcacb3a2c021d78da5e5b7130300154a
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529294"
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
|Bokföra utleveransen av artiklar direkt på det avgående orderdokumentet eftersom det inte finns några lagerfunktioner. (Fungerar på samma sätt för en försäljningsorder, en utgående överföringsorder och returutleveranser.)|[Leverera artiklar](warehouse-how-ship-items.md)|  
|Plocka artiklar order för order och bokföra utleveransen i samma aktivitet, i en grundläggande lagerkonfiguration.|[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Plocka artiklar för flera order i en avancerad lagerkonfiguration.|[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Plocka komponenter för produktion eller montering i en grundläggande lagerkonfiguration.|[Plocka för produktion eller montering i grundläggande distributionslagerkonfiguration](warehouse-how-to-pick-for-production.md)|
|Plocka komponenter för produktion eller montering i en avancerad lagerkonfiguration.|[Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)|  
|Planera optimerade plockinstruktioner för ett antal utleveranser i stället för att låta lagerarbetare agera direkt på bokförda utleveranser.|[Planera plockningar i kalkylark](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Plocka artiklar tekniskt för ett visst syfte, till exempel en produktionsenhet som behöver extra komponenter, så att artiklarna inte lämnar distributionslagret tekniskt.|[Plocka och lagra utan källdokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Förstå hur du automatiskt plockar artiklar enligt deras utgångsdatum, till exempel ömtåliga varor.|[Plockning med FEFO](warehouse-picking-by-fefo.md)|
|En plockningsrad delas upp i flera rader, till exempel eftersom det inte finns tillräckligt många artiklar som ska tas från den bestämda lagerplatsen.|[Dela rader för dist.lageraktivitet](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få direkt tillgång till plockningar som tilldelats dig som lagerarbetare.|[Hitta distributionslagerfördelningar](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
