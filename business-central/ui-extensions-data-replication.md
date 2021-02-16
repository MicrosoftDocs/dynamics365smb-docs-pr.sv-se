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
ms.author: edupont
ms.openlocfilehash: f2d8d556ca4628a66c10f323f47137cd35732a68
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757298"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="29f7b-104">Intelligenta molntillägg för migrering av moln</span><span class="sxs-lookup"><span data-stu-id="29f7b-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="29f7b-105">Beroende på din lokala lösning måste du använda olika tillägg för att ansluta dina data till [!INCLUDE[prod_short](includes/prod_short.md)] online för att migrera din lösning till molnet.</span><span class="sxs-lookup"><span data-stu-id="29f7b-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="29f7b-106">Om du använder någon av de lokala produkterna som stöds kan du konfigurera den intelligenta molnmiljön utifrån ett produktspecifikt tillägg.</span><span class="sxs-lookup"><span data-stu-id="29f7b-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="29f7b-107">När din molnmiljö väl har konfigurerats kan du kan migrera data från din lokala lösning till [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="29f7b-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="29f7b-108">Detta gör att du kan utnyttja vad molnet har att erbjuda ditt företag till fullo, till exempel bättre insyn i verksamheten, artificiell intelligens, åtkomst av flera enheter och åtkomst när som helst, var som helst.</span><span class="sxs-lookup"><span data-stu-id="29f7b-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="29f7b-109">Mer information finns i [migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet för [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="29f7b-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="29f7b-110">Business Central lokalt</span><span class="sxs-lookup"><span data-stu-id="29f7b-110">Business Central on-premises</span></span>

<span data-ttu-id="29f7b-111">Om du använder en lokal distribution av [!INCLUDE[prod_short](includes/prod_short.md)], skaffa tillägget **Intelligent moln-bas** och tillägget **Business Central Intelligent moln** och kör sedan guiden assisterad konfiguration för **Konfiguration av molnmigrering**.</span><span class="sxs-lookup"><span data-stu-id="29f7b-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="29f7b-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="29f7b-112">Dynamics GP</span></span>

<span data-ttu-id="29f7b-113">Om du använder Dynamics GP, skaffa **Tillägget Intelligent moln-bas** och tillägget **Dynamics GP Intelligent moln** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.</span><span class="sxs-lookup"><span data-stu-id="29f7b-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="29f7b-114">Migrering från Dynamics GP med hjälp av guiden för assisterad konfiguration **Konfiguration av molnmigrering** stöds för närvarande endast på följande marknader: USA, Kanada och Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="29f7b-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="29f7b-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="29f7b-115">Dynamics SL</span></span>

<span data-ttu-id="29f7b-116">Om du använder Dynamics SL, skaffa tillägget **Intelligent moln-bas**, tillägget **Microsoft Dynamics SL Intelligent moln** och tillägget **Microsoft Dynamics SL SmartLists för historik** och kör sedan den assisterade konfigurationsguiden **Konfiguration av molnmigrering**.</span><span class="sxs-lookup"><span data-stu-id="29f7b-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="29f7b-117">Se även</span><span class="sxs-lookup"><span data-stu-id="29f7b-117">See Also</span></span>

[<span data-ttu-id="29f7b-118">Intelligenta insikter</span><span class="sxs-lookup"><span data-stu-id="29f7b-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="29f7b-119">Tillägget intelligent moln-bas</span><span class="sxs-lookup"><span data-stu-id="29f7b-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
