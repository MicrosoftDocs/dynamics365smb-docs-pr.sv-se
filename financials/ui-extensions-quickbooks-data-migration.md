---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera kunder, leverantörer, artiklar och konton från QuickBooks Desktop till Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Tillägget QuickBooks datamigrering för Dynamics 365 for Financials
Detta tillägg gör det enkelt att migrera kunder, leverantörer, artiklar och konton från QuickBooks Desktop till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om ditt företag använder QuickBooks i dag, kan du exportera nödvändig information och sedan öppna guiden för assisterad installation för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Mer information finns i [Importera företagsdata från ett annat finanssystem](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Exportera data från QuickBooks Desktop
Du måste ha exporterat en del eller alla av dina befintliga kunder, leverantörer, lagerartiklar och konton till en Intuit Interchange Format-fil (IIF ). Tillägget QuickBooks datamigrering innehåller en standardmappning avQuickBooks data så att du kan använda dina befintliga data för att testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget. Standardmappningen ska vara tillräcklig i de flesta fall, men du kan ändra mappningen i guiden för assisterad installation.  
I QuickBooks innehåller arkiv-menyn verktyg till exportlistor. För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande listor:

* Kundlista  
* Leverantörslista  
* Artikellista  
* Redov.kontolista  

Exporterade data sparas som en IIF-fil som du sedan kan överföra [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Hitta tillägget QuickBooks datamigrering
Tillägget QuickBooks datamigrering är installerat och klart som en integrerad del av guiden för assisterad konfiguration av datamigrering. Om du är redo att sätta igång nu, och har exporterat data från QuickBooks, väljer du ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), anger **Assisterad konfiguration** och väljer sedan relaterad länk. Välj **Migrera affärsdata** och följ sedan anvisningarna i guiden.  

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  

