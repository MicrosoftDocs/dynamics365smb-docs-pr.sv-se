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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c1ea1c4a5ea4b917243d60981ec35050895f82a7
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="warehouse-management"></a>Lagerstyrning
Efter att varor har inlevererats och innan varor har levererats, sker en serie interna lageraktiviteter som säkerställer ett effektivt flöde genom lagerstället och strukturerar och underhåller företagets lager.

Vanliga lageraktiviteter omfattar artikelinförsel, att flytta artiklar inom eller mellan lagerställen och att plocka artiklar från montering, produktion eller utleverans. Montera artiklar för försäljning eller lager måste även ta hänsyn till lageraktiviteter, men dessa klassificeras på annat håll. Mer information finns i [Monteringshantering](assembly-assemble-items.md).  

I stora lager kan dessa olika uppgifter hanteras av olika avdelningar och integrationen hanteras med ett dirigerat arbetsflöde. I enklare installationer är dessa flöden mindre formaliserade, och lageraktiviteterna utförs med så kallad lagerinförsel och lagerplockning. Mer information om grundläggande och avancerade konfigurationer finns i [Designdetaljer: översikt över distributionslager](design-details-warehouse-overview.md).

Innan du kan utföra lageraktiviteter måste du ange systemet för relevanta komplexiteten i distributionslagerprocessen. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Registrera inleveransen av artiklar på lagerställen, antingen med en inköpsorder, under enkla lagerställekonfigurationer, eller med en lagerinleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.|[Så här inlevererar du artiklar](warehouse-how-receive-items.md)|
|Hoppa över artikelinförseln och välj processer för att påskynda en artikel direkt från produktion till levereras.|[Så här: Artiklar för direktutleverans](warehouse-how-to-cross-dock-items.md)|    
|Införa artiklar som har inlevererats från inköp, returer, överföringar eller produktionsutflöde enligt den konfigurerade distributionslagerprocessen.|[Införa utflöde från artiklar](warehouse-put-away-items.md)|
|Flytta artiklar mellan lagerplatser i distributionslagret.|[Flytta artiklar](warehouse-move-items.md)|
|Plocka artiklar som ska levereras, överföras eller förbrukas vid montering eller produktion, enligt den konfigurerade distributionslagerprocessen.|[Plocka artiklar](warehouse-pick-items.md)|
|Registrera utleverans av artiklar från lagerställen, antingen med en försäljningsorder, under enkla lagerställekonfigurationer, eller med en lagerutleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.|[Så här levererar du artiklar](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Se även  
 [Lagersaldo](inventory-manage-inventory.md)  
 [Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
 [Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

