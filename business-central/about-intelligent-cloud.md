---
title: Intelligenta insikter och migrering av moln | Microsoft Docs
description: Anslut dig till intelligenta insikter med Business Central, till och med från din lokala lösning. Lär dig hur du migrerar till molnet.
author: bmeier94
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms. search.keywords: cloud, edge
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca7fd910e70deaebbf8912eecfe6d9c25ddfcc4e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385130"
---
# <a name="intelligent-insights-with-prod_short-online"></a><span data-ttu-id="8fe40-104">Intelligenta insikter med [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="8fe40-104">Intelligent Insights with [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="8fe40-105">Som användare av [!INCLUDE[prod_short](includes/prod_short.md)] online har du fullständig behörighet för scenarier som baseras på intelligent moln, till exempel KPI:er baserade på maskininlärning när du visar data i Power BI.</span><span class="sxs-lookup"><span data-stu-id="8fe40-105">As a user of [!INCLUDE[prod_short](includes/prod_short.md)] online, you have full access to scenarios that are based on the intelligent cloud, such as KPIs that are based on machine learning, or when you view your data in Power BI.</span></span> <span data-ttu-id="8fe40-106">Men även om [!INCLUDE[prod_short](includes/prod_short.md)] framför allt är en molntjänst, kan även kunder som behöver köra sin arbetsbelastning helt lokalt eller på intelligent gränsenhet ansluten till molnet kan göra detta.</span><span class="sxs-lookup"><span data-stu-id="8fe40-106">However, while [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud-first service, also those customers who need to run their workloads fully on-premises or on the intelligent edge connected to the cloud can do so.</span></span>  

<span data-ttu-id="8fe40-107">Om du är intresserad av [!INCLUDE[prod_short](includes/prod_short.md)] kan du registrera dig online, eller så kan du arbeta med en partner för att distribuera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt med maskinvara av eget val.</span><span class="sxs-lookup"><span data-stu-id="8fe40-107">If you are interested in [!INCLUDE[prod_short](includes/prod_short.md)], you can sign up for a free trial online, or you can choose to work with a partner to deploy [!INCLUDE[prod_short](includes/prod_short.md)] locally to your own choice of hardware.</span></span> <span data-ttu-id="8fe40-108">Du kan sedan bestämma dig för att få intelligenta insikter genom att ansluta till en klientorganisation i molnet.</span><span class="sxs-lookup"><span data-stu-id="8fe40-108">You can then decide to get intelligent insights by connecting to a tenant in the cloud.</span></span> <span data-ttu-id="8fe40-109">Som ett resultat kommer data från din lokalt distribuerade [!INCLUDE[prod_short](includes/prod_short.md)] att replikeras till molnet för scenarier med intelligent moln.</span><span class="sxs-lookup"><span data-stu-id="8fe40-109">As a result, the data from your [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment replicates to the cloud for intelligent cloud scenarios.</span></span>  

<span data-ttu-id="8fe40-110">Anslutning till intelligent moln från en lokal lösning kräver att administratören anger information om databasen.</span><span class="sxs-lookup"><span data-stu-id="8fe40-110">Connecting to the intelligent cloud from an on-premises solution requires your administrator to specify information about your database.</span></span> <span data-ttu-id="8fe40-111">De verktyg som används för att ansluta lokal distribution till [!INCLUDE[prod_short](includes/prod_short.md)] online är desamma som också används för migrering från lokala platser till online.</span><span class="sxs-lookup"><span data-stu-id="8fe40-111">The tools used to connect your on-premises deployment to [!INCLUDE[prod_short](includes/prod_short.md)] online are the same that are also used to migration from on-premises to online.</span></span> <span data-ttu-id="8fe40-112">Mer information finns i [migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet för [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8fe40-112">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="viewing-intelligent-cloud-insights-in-prod_short-online"></a><span data-ttu-id="8fe40-113">Visa insikter för intelligent moln i [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="8fe40-113">Viewing Intelligent Cloud Insights in [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="8fe40-114">I ditt [!INCLUDE[prod_short](includes/prod_short.md)] onlineföretag visar sidan **Insikter för intelligent moln** fyra viktiga punkter av intresse för de flesta företag:</span><span class="sxs-lookup"><span data-stu-id="8fe40-114">In your [!INCLUDE[prod_short](includes/prod_short.md)] online company, the **Intelligent Cloud Insights** page shows four key points of interest for most businesses:</span></span>

- <span data-ttu-id="8fe40-115">Kassatillgänglighet</span><span class="sxs-lookup"><span data-stu-id="8fe40-115">Cash availability</span></span>
- <span data-ttu-id="8fe40-116">Lönsamhet för försäljning</span><span class="sxs-lookup"><span data-stu-id="8fe40-116">Sales profitability</span></span>
- <span data-ttu-id="8fe40-117">Nettointäkt</span><span class="sxs-lookup"><span data-stu-id="8fe40-117">Net income</span></span>
- <span data-ttu-id="8fe40-118">Lagervärde</span><span class="sxs-lookup"><span data-stu-id="8fe40-118">Inventory value</span></span>

<span data-ttu-id="8fe40-119">Bredvid ett KPI-diagram kan du få insyn i potentiella viktiga områden, inklusive förfallna betalningar.</span><span class="sxs-lookup"><span data-stu-id="8fe40-119">Next to the KPI charts, you get insights into potential areas of concern, including overdue payments.</span></span> <span data-ttu-id="8fe40-120">Välj varje insikt för att se informationen.</span><span class="sxs-lookup"><span data-stu-id="8fe40-120">Choose each insight to drill into the data.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="8fe40-121">![Insikter för intelligent moln](media/across-intelligent-cloud/intelligentcloudApril19.png "Insikter för intelligent moln i Business Central")</span><span class="sxs-lookup"><span data-stu-id="8fe40-121">![Intelligent cloud insights](media/across-intelligent-cloud/intelligentcloudApril19.png "Shows the Intelligent Cloud Insights page in Business Central")</span></span>

<span data-ttu-id="8fe40-122">Sidan ansluter också till Power BI för ytterligare insikter.</span><span class="sxs-lookup"><span data-stu-id="8fe40-122">The page also connects to Power BI for even more insights.</span></span>

## <a name="viewing-intelligent-insights-on-premises"></a><span data-ttu-id="8fe40-123">Visa intelligenta insikter lokalt</span><span class="sxs-lookup"><span data-stu-id="8fe40-123">Viewing Intelligent Insights On-Premises</span></span>

<span data-ttu-id="8fe40-124">När din Dynamics 365 återförsäljare har fått rätt licens för den lokala lösningen för att ansluta till molnet genom [!INCLUDE[prod_short](includes/prod_short.md)], kan din IT-administratör konfigurera anslutningen.</span><span class="sxs-lookup"><span data-stu-id="8fe40-124">When your Dynamics 365 reselling partner has acquired the right license for your on-premises solution to connect to the cloud through [!INCLUDE[prod_short](includes/prod_short.md)], your administrator can set up the connection.</span></span> <span data-ttu-id="8fe40-125">När detta är klart kan visa du samma insikter från molnet i din lokala applikation.</span><span class="sxs-lookup"><span data-stu-id="8fe40-125">Once that is done, you can view the same insights from the cloud in your on-premises application.</span></span> <span data-ttu-id="8fe40-126">Beroende på den lokala lösningen kan sidan **Insikter för intelligent moln** vara inbäddad på startsidan eller på en separat sida i [!INCLUDE[prod_short](includes/prod_short.md)] online och lokalt.</span><span class="sxs-lookup"><span data-stu-id="8fe40-126">Depending on the on-premises solution, the **Intelligent Cloud Insights** page can be embedded in the Home page or be a separate page as in [!INCLUDE[prod_short](includes/prod_short.md)] online and on-premises.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8fe40-127">Se även</span><span class="sxs-lookup"><span data-stu-id="8fe40-127">See Also</span></span>

[<span data-ttu-id="8fe40-128">Välkommen till Business Central</span><span class="sxs-lookup"><span data-stu-id="8fe40-128">Welcome to Business Central</span></span>](index.md)  
[<span data-ttu-id="8fe40-129">Intelligenta molntillägg för migrering av moln</span><span class="sxs-lookup"><span data-stu-id="8fe40-129">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="8fe40-130">Migrera lokala data till Business Central Online</span><span class="sxs-lookup"><span data-stu-id="8fe40-130">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]