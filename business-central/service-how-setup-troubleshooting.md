---
title: Ställa in Felsökningsprocesser | Microsoft Docs
description: Lär dig hur du ställer in processer som hjälper servicerepresentanten att identifiera och lösa problem med serviceartiklar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7fdbc30e20e7d5a8feeb17a97ccdee3688fa7607
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380412"
---
# <a name="setting-up-troubleshooting-for-service-items"></a>Ställa in felsökning av serviceartiklar.
Du kan ställa in felsökningsriktlinjer som hjälper tekniker att lösa problem när de tillhandahåller tjänster. Riktlinjer kan till exempel vara en lista över de steg som måste utföras vid en reparation eller ett antal frågor att ställa om artiklarna. När du har angett riktlinjer för felsökning kan du tilldela dem till serviceartikelgrupper, serviceartiklar eller artiklar. Det finns en arvshierarki för riktlinjer. Om du tilldelar dem till en serviceartikelgrupp ärver artiklarna som ingår i gruppen riktlinjerna om du inte anger något annat för artiklarna. På ett liknande sätt ärver serviceartiklar riktlinjer från artiklar.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Så här skapar du felsökningsriktlinjer
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Felsökning** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>För att koppla riktlinjer för felsökning till artiklar, serviceartiklar eller serviceartikelgrupper.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") gå till **Artiklar** eller **Tjänsteartiklar** eller **Tjänstartikelgrupper** och välj sedan relaterad länk.  
2. Välj relevant enhet och välj sedan åtgärden **Felsökning**.  

## <a name="see-also"></a>Se även
[Servicehantering](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]