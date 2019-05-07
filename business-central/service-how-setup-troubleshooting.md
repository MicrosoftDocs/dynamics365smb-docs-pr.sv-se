---
title: Ställa in Felsökningsprocesser | Microsoft Docs
description: Lär dig hur du ställer in processer som hjälper servicerepresentanten att identifiera och lösa problem med serviceartiklar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2dfa02f0054cab20605281bb1cc580b522b893fd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "937487"
---
# <a name="setting-up-troubleshooting-for-service-items"></a>Ställa in felsökning av serviceartiklar.
Du kan ställa in felsökningsriktlinjer som hjälper tekniker att lösa problem när de tillhandahåller tjänster. Riktlinjer kan till exempel vara en lista över de steg som måste utföras vid en reparation eller ett antal frågor att ställa om artiklarna. När du har angett riktlinjer för felsökning kan du tilldela dem till serviceartikelgrupper, serviceartiklar eller artiklar. Det finns en arvshierarki för riktlinjer. Om du tilldelar dem till en serviceartikelgrupp ärver artiklarna som ingår i gruppen riktlinjerna om du inte anger något annat för artiklarna. På ett liknande sätt ärver serviceartiklar riktlinjer från artiklar.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Så här skapar du felsökningsriktlinjer
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Felsökning** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>För att koppla riktlinjer för felsökning till artiklar, serviceartiklar eller serviceartikelgrupper.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** eller **Serviceartiklar**, eller **Serviceartikelgrupper** och välj sedan relaterad länk.  
2. Välj relevant enhet och välj sedan åtgärden **Felsökning**.  

## <a name="see-also"></a>Se även
[Servicehantering](service-service.md)