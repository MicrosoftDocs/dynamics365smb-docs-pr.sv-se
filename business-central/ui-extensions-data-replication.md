---
title: Tillägget Molnmigrering
description: Använd tilläggen för molnmigrering för att migrera lokala data till Business Central online. Dessa tillägg flyttar dina lokala data till molnet.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: f76241497eea8a53dfc054c895bf4a788e2226a4
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6322303"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a>Tillägg för molnflyttning för migrering till Business Central Online

Beroende på din lokala lösning måste du använda olika tillägg för att ansluta dina data till [!INCLUDE[prod_short](includes/prod_short.md)] online för att migrera din lösning till molnet.  

Om du använder någon av de lokala produkterna som stöds kan du konfigurera den intelligenta molnmiljön utifrån ett produktspecifikt tillägg. När din molnmiljö väl har konfigurerats kan du kan migrera data från din lokala lösning till [!INCLUDE[prod_short](includes/prod_short.md)]. Detta gör att du kan utnyttja vad molnet har att erbjuda ditt företag till fullo, till exempel bättre insyn i verksamheten, artificiell intelligens, åtkomst av flera enheter och åtkomst när som helst, var som helst.  

Mer information finns i [migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet för [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="business-central-on-premises"></a>Business Central lokalt

Om du använder en lokal distribution av [!INCLUDE[prod_short](includes/prod_short.md)], skaffa tillägget **Intelligent moln-bas** och tillägget **Business Central Intelligent moln** och kör sedan guiden assisterad konfiguration för **Konfiguration av molnmigrering**.  

## <a name="dynamics-gp"></a>Dynamics GP

Om du använder Dynamics GP, skaffa **Tillägget Intelligent moln-bas** och tillägget **Dynamics GP Intelligent moln** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.  

> [!IMPORTANT]
> Migrering från Dynamics GP med hjälp av guiden för assisterad konfiguration **Konfiguration av molnmigrering** stöds för närvarande endast på följande marknader: USA, Kanada och Storbritannien.

## <a name="dynamics-sl"></a>Dynamics SL

Om du använder Dynamics SL, skaffa tillägget **Intelligent moln-bas**, tillägget **Microsoft Dynamics SL Intelligent moln** och tillägget **Microsoft Dynamics SL SmartLists för historik** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.  

## <a name="see-also"></a>Se även

[Tillägget Bas för molnmigrering](ui-extensions-intelligent-cloud.md)  
[Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]