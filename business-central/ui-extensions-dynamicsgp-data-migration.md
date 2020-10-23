---
title: Migrera data från Dynamics GP före 15.3 | Microsoft Docs
description: Innan uppdateringen 15.3 kan du använda tillägget Dynamics GP-datamigrering för att flytta över kunder, leverantörer, lagerartiklar, redovisningskonton, öppna leverantörs- och kundreskontratransaktioner från Dynamics GP till Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: 7c17c5f54553e7960f4386918bda640fa2e0380e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915191"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="dc3a1-103">Tillägget Dynamics GP datamigrering</span><span class="sxs-lookup"><span data-stu-id="dc3a1-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="dc3a1-104">Det här tillägget kommer att vara inaktuellt i 15.3-uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="dc3a1-105">Vi rekommenderar användare som vill migrera från Dynamics GP att börja använda guiden **molnmigrering** i stället.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="dc3a1-106">Tillägget **Molnmigrerin** har stabilare funktionalitet och tar mer data till Business Central från Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="dc3a1-107">Mer information finns i [migrera till Business Central Online från Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) i administrationsinnehållet för [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="dc3a1-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="dc3a1-108">Se även</span><span class="sxs-lookup"><span data-stu-id="dc3a1-108">See Also</span></span>

[<span data-ttu-id="dc3a1-109">Intelligenta molntillägg för migrering av moln</span><span class="sxs-lookup"><span data-stu-id="dc3a1-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="dc3a1-110">Importera affärsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="dc3a1-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="dc3a1-111">[Anpassa [!INCLUDE[prodshort](includes/prodshort.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="dc3a1-111">[Customizing [!INCLUDE[prodshort](includes/prodshort.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="dc3a1-112">Migrera till Business Central Online från Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="dc3a1-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
