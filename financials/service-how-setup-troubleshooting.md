---
title: "Ställa in Felsökningsprocesser | Microsoft Docs"
description: "Lär dig hur du ställer in processer som hjälper servicerepresentanten att identifiera och lösa problem med serviceartiklar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5876bf5d959d106eefb9b0f765e42e74dd13ab07
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---

# <a name="setting-up-troubleshooting-for-service-items"></a>Ställa in felsökning av serviceartiklar.
Du kan ställa in felsökningsriktlinjer som hjälper tekniker att lösa problem när de tillhandahåller tjänster. Riktlinjer kan till exempel vara en lista över de steg som måste utföras vid en reparation eller ett antal frågor att ställa om artiklarna. När du har angett riktlinjer för felsökning kan du tilldela dem till serviceartikelgrupper, serviceartiklar eller artiklar. Det finns en arvshierarki för riktlinjer. Om du tilldelar dem till en serviceartikelgrupp ärver artiklarna som ingår i gruppen riktlinjerna om du inte anger något annat för artiklarna. På ett liknande sätt ärver serviceartiklar riktlinjer från artiklar.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Så här skapar du felsökningsriktlinjer
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Felsökning** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>För att koppla riktlinjer för felsökning till artiklar, serviceartiklar eller serviceartikelgrupper.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar**, **Serviceartiklar**, eller **Serviceartikelgrupp** och välj sedan relaterad länk.  
2. Välj relevant enhet och välj sedan åtgärden **Felsökning**.  

## <a name="see-also"></a>Se även
[Servicehantering](service-service.md)
