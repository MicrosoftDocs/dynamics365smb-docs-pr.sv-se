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
ms.date: 07/13/2020
ms.author: jenolson
ms.openlocfilehash: 712950571d5b45680aae46bccfd8401b999993cd
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577267"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="2c62c-104">Intelligenta molntillägg för migrering av moln</span><span class="sxs-lookup"><span data-stu-id="2c62c-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="2c62c-105">Beroende på din lokala lösning måste du använda olika tillägg för att ansluta dina data till [!INCLUDE[prodshort](includes/prodshort.md)] online för att migrera din lösning till molnet.</span><span class="sxs-lookup"><span data-stu-id="2c62c-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prodshort](includes/prodshort.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="2c62c-106">Om du använder någon av de lokala produkterna som stöds kan du konfigurera den intelligenta molnmiljön utifrån ett produktspecifikt tillägg.</span><span class="sxs-lookup"><span data-stu-id="2c62c-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span><span data-ttu-id="2c62c-107"> När din molnmiljö har konfigurerats kan du kan migrera data från din lokala lösning till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2c62c-107"> Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2c62c-108">Detta gör att du kan utnyttja vad molnet har att erbjuda ditt företag till fullo, till exempel bättre insyn i verksamheten, artificiell intelligens, åtkomst av flera enheter och åtkomst när som helst, var som helst.</span><span class="sxs-lookup"><span data-stu-id="2c62c-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="2c62c-109">Mer information finns i [migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet för [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2c62c-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="2c62c-110">Business Central lokalt</span><span class="sxs-lookup"><span data-stu-id="2c62c-110">Business Central on-premises</span></span>

<span data-ttu-id="2c62c-111">Om du använder en lokal distribution av [!INCLUDE[prodshort](includes/prodshort.md)], skaffa tillägget **Intelligent moln-bas** och tillägget **Business Central Intelligent moln** och kör sedan guiden assisterad konfiguration för **Konfiguration av molnmigrering**.</span><span class="sxs-lookup"><span data-stu-id="2c62c-111">If you are using an on-premises deployment of [!INCLUDE[prodshort](includes/prodshort.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="2c62c-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="2c62c-112">Dynamics GP</span></span>

<span data-ttu-id="2c62c-113">Om du använder Dynamics GP, skaffa **Tillägget Intelligent moln-bas** och tillägget **Dynamics GP Intelligent moln** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.</span><span class="sxs-lookup"><span data-stu-id="2c62c-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="2c62c-114">Migrering från Dynamics GP med hjälp av guiden för assisterad konfiguration **Konfiguration av molnmigrering** stöds för närvarande endast på följande marknader: USA, Kanada och Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="2c62c-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="2c62c-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="2c62c-115">Dynamics SL</span></span>

<span data-ttu-id="2c62c-116">Om du använder Dynamics SL, skaffa tillägget **Intelligent moln-bas**, tillägget **Microsoft Dynamics SL Intelligent moln** och tillägget **Microsoft Dynamics SL SmartLists för historik** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.</span><span class="sxs-lookup"><span data-stu-id="2c62c-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c62c-117">Se även</span><span class="sxs-lookup"><span data-stu-id="2c62c-117">See Also</span></span>

[<span data-ttu-id="2c62c-118">Intelligenta insikter</span><span class="sxs-lookup"><span data-stu-id="2c62c-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="2c62c-119">Tillägget intelligent moln-bas</span><span class="sxs-lookup"><span data-stu-id="2c62c-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
