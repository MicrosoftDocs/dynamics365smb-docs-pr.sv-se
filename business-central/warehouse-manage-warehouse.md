---
title: Lageraktiviteter | Microsoft Docs
description: Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 98cb79b14ac8bd4610bf14af8344213f87f7f170
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248232"
---
# <a name="warehouse-management"></a>Lagerstyrning
Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager.

Vanliga lageraktiviteter omfattar artikelinförsel, att flytta artiklar inom eller mellan lagerställen och att plocka artiklar från montering, produktion eller utleverans. Montera artiklar för försäljning eller lager måste även ta hänsyn till lageraktiviteter, men dessa klassificeras på annat håll. Mer information finns i [Monteringshantering](assembly-assemble-items.md).  

I stora lager kan dessa olika uppgifter hanteras av olika avdelningar och integrationen hanteras med ett dirigerat arbetsflöde. I enklare installationer är dessa flöden mindre formaliserade, och lageraktiviteterna utförs med så kallad lagerinförsel och lagerplockning. Mer information om grundläggande och avancerade konfigurationer finns i [Designdetaljer: översikt över distributionslager](design-details-warehouse-overview.md).

Innan du kan utföra lageraktiviteter måste du ange systemet för relevanta komplexiteten i distributionslagerprocessen. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Lagerrelaterade uppgifter för inventering, justering och gruppering av artiklar kan omfatta lagerställeuppgifter som gäller för distributionslagertransaktionerna innan de kan synkroniseras med de associerade artikeltransaktionerna. Mer information finns i [Inventera, justera och gruppera om lager](inventory-how-count-adjust-reclassify.md).

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Registrera inleveransen av artiklar på lagerställen, antingen med en inköpsorder, under enkla lagerställekonfigurationer, eller med en lagerinleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.|[Ta emot artiklar](warehouse-how-receive-items.md)|
|Hoppa över artikelinförseln och välj processer för att påskynda en artikel direkt från produktion till levereras.|[Beräkna direktutleverans av artiklar](warehouse-how-to-cross-dock-items.md)|    
|Införa artiklar som har inlevererats från inköp, returer, överföringar eller produktionsutflöde enligt den konfigurerade distributionslagerprocessen.|[Införa utflöde från artiklar](warehouse-put-away-items.md)|
|Flytta artiklar mellan lagerplatser i distributionslagret.|[Flytta artiklar](warehouse-move-items.md)|
|Plocka artiklar som ska levereras, överföras eller förbrukas vid montering eller produktion, enligt den konfigurerade distributionslagerprocessen.|[Plocka artiklar](warehouse-pick-items.md)|
|Registrera utleverans av artiklar från lagerställen, antingen med en försäljningsorder, under enkla lagerställekonfigurationer, eller med en lagerutleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.|[Leverera artiklar](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Se även  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
