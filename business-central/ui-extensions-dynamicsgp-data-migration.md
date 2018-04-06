---
title: "Migrera Data från Dynamics GP med tillägget Data Migration | Microsoft Docs"
description: "Använd filnamnstillägget Dynamics GP-datamigrering för att flytta över kunder, leverantörer, lagerartiklar och konton från Dynamics GP till Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5d689a43e3debe51cfbb9306252d0c9f75e7bb70
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a>Tillägget Dynamics GP-datamigrering för Business Central 
Detta tillägg gör det enkelt att migrera kunder, leverantörer, lagerartiklar och konton från Dynamics GP till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om ditt företag använder Dynamics GP i dag, kan du exportera nödvändiga huvudposter och sedan öppna guiden för assisterad konfiguration för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Migrera företagsdata från ett annat finanssystem](upload-data.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportera data från Dynamics GP
Du måste ha exporterat några av dina befintliga kunder, leverantörer, lagerartiklar och konton till en fill med hjälp av funktionen dataexport i Dynamics GP. För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande typer av data:

* Konto  
* Kund  
* Artikel  
* Leverantör  

Tillägget Datamigrering för Dynamics GP mappas automatiskt den exporterade informationen så att dina data är snabbt tillgängliga i ditt nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag. Under processen skapas stödjande installationsinformation, som till exempel bokföringsmallar. Lagerartiklar kommer att tas med i systemet med FIFO som kostadsvärderingsmetod. Konton ska ställas in som ett segment för huvudkontot från Dynamics GP med dimensioner, eftersom [!INCLUDE[d365fin](includes/d365fin_long_md.md)] inte har kontosegment.

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  

