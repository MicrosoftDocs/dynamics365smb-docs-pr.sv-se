---
title: Lageraktiviteter | Microsoft Docs
description: "Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c8d4ee33395c18cb7755fd1877b2af813fb9da43
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="warehouse-management"></a>Lagerstyrning
Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager.

Vanliga lageraktiviteter omfattar artikelinförsel, att flytta artiklar inom eller mellan lagerställen och att plocka artiklar från montering, produktion eller utleverans. Montera artiklar för försäljning eller lager måste även ta hänsyn till lageraktiviteter, men dessa klassificeras på annat håll. Mer information finns i [Monteringshantering](assembly-assemble-items.md).  

I stora lager kan dessa olika uppgifter hanteras av olika avdelningar och integrationen hanteras med ett dirigerat arbetsflöde. I enklare installationer är dessa flöden mindre formaliserade, och lageraktiviteterna utförs med så kallad lagerinförsel och lagerplockning. Mer information om grundläggande och avancerade konfigurationer finns i [Designdetaljer: översikt över distributionslager](design-details-warehouse-overview.md).

Innan du kan utföra lageraktiviteter måste du ange systemet för relevanta komplexiteten i distributionslagerprocessen. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

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

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]

