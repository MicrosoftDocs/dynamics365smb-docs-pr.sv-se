---
title: Hantera lageraktiviteter
description: Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: af975b69973eab84efcb346e98600d8b2221ecea
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971527"
---
# <a name="warehouse-management"></a>Lagerstyrning

Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager.

Vanliga lageraktiviteter omfattar artikelinförsel, att flytta artiklar inom eller mellan lagerställen och att plocka artiklar från montering, produktion eller utleverans. Montera artiklar för försäljning eller lager måste även ta hänsyn till lageraktiviteter, men dessa klassificeras på annat håll. Mer information finns i [Monteringshantering](assembly-assemble-items.md).  

I stora lager kan dessa olika uppgifter hanteras av olika avdelningar och integreringen hanteras med ett dirigerat arbetsflöde. I enklare installationer är dessa flöden mindre formaliserade, och lageraktiviteterna utförs med så kallad lagerinförsel och lagerplockning. Mer information om grundläggande och avancerade konfigurationer finns i [Designdetaljer: översikt över distributionslager](design-details-warehouse-overview.md).

Innan du kan utföra lageraktiviteter måste du ange systemet för relevanta komplexiteten i distributionslagerprocessen. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Lagerrelaterade uppgifter för inventering, justering och gruppering av artiklar kan omfatta lagerställeuppgifter som gäller för distributionslagertransaktionerna innan de kan synkroniseras med de associerade artikeltransaktionerna. Mer information finns i [Inventera, justera och gruppera om lager](inventory-how-count-adjust-reclassify.md).

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Se**|  
|------------|-------------|  
|Registrera inleveransen av artiklar (inklusive överinleveranser) på lagerställen, antingen enbart med en inköpsorder (i förenklade lagerställekonfigurationer) eller med en lagerinleverans (vid halv- eller helautomatisk distributionslagerprocess på plats).|[Ta emot artiklar](warehouse-how-receive-items.md)|
|Hoppa över artikelinförseln och välj processer för att påskynda en artikel direkt från produktion till levereras.|[Beräkna direktutleverans av artiklar](warehouse-how-to-cross-dock-items.md)|
|Införa artiklar som har inlevererats från inköp, returer, överföringar eller produktionsutflöde enligt den konfigurerade distributionslagerprocessen.|[Införa utflöde från artiklar](warehouse-put-away-items.md)|
|Flytta artiklar mellan lagerställen i distributionslagret.|[Flytta artiklar](warehouse-move-items.md)|
|Plocka artiklar som ska levereras, överföras eller förbrukas vid montering eller produktion, enligt den konfigurerade distributionslagerprocessen.|[Plocka artiklar](warehouse-pick-items.md)|
|Registrera utleverans av artiklar från lagerställen, antingen med en försäljningsorder, under enkla lagerställekonfigurationer, eller med en lagerutleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.|[Leverera artiklar](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Se även

[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)
[Monteringshantering](assembly-assemble-items.md)
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]