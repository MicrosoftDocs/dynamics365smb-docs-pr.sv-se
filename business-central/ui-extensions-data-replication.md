---
title: Business Central Intelligent moln-tillägg för molnmigrering | Microsoft Docs
description: Använd tilläggen för molnmigrering för att migrera lokala data till Business Central online. Dessa tillägg flyttar dina lokala data till molnet så att du kan använda Business Central online med befintliga data.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jenolson
ms.openlocfilehash: dde6797139f383948d72c52ca1d05298a280087b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915216"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a>Intelligenta molntillägg för migrering av moln

Beroende på din lokala lösning måste du använda olika tillägg för att ansluta dina data till [!INCLUDE[prodshort](includes/prodshort.md)] online för att migrera din lösning till molnet.  

Om du använder någon av de lokala produkterna som stöds kan du konfigurera den intelligenta molnmiljön utifrån ett produktspecifikt tillägg. När din molnmiljö har konfigurerats kan du kan migrera data från din lokala lösning till [!INCLUDE[prodshort](includes/prodshort.md)]. Detta gör att du kan utnyttja vad molnet har att erbjuda ditt företag till fullo, till exempel bättre insyn i verksamheten, artificiell intelligens, åtkomst av flera enheter och åtkomst när som helst, var som helst.  

Mer information finns i [migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet för [!INCLUDE[prodshort](includes/prodshort.md)].  

## <a name="business-central-on-premises"></a>Business Central lokalt

Om du använder en lokal distribution av [!INCLUDE[prodshort](includes/prodshort.md)], skaffa tillägget **Intelligent moln-bas** och tillägget **Business Central Intelligent moln** och kör sedan guiden assisterad konfiguration för **Konfiguration av molnmigrering**.  

## <a name="dynamics-gp"></a>Dynamics GP

Om du använder Dynamics GP, skaffa **Tillägget Intelligent moln-bas** och tillägget **Dynamics GP Intelligent moln** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.  

> [!IMPORTANT]
> Migrering från Dynamics GP med hjälp av guiden för assisterad konfiguration **Konfiguration av molnmigrering** stöds för närvarande endast på följande marknader: USA, Kanada och Storbritannien.

## <a name="dynamics-sl"></a>Dynamics SL

Om du använder Dynamics SL, skaffa tillägget **Intelligent moln-bas**, tillägget **Microsoft Dynamics SL Intelligent moln** och tillägget **Microsoft Dynamics SL SmartLists för historik** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.  

## <a name="see-also"></a>Se även

[Intelligenta insikter](about-intelligent-cloud.md)  
[Tillägget intelligent moln-bas](ui-extensions-intelligent-cloud.md)  
