---
title: Power BI-integreringskomponent och arkitekturöversikt för Business Central| Microsoft Docs
description: Använda insikter, business intelligence och KPI:er från dina Business Central-data är enkelt med Business Central-apparna för Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753776"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a><span data-ttu-id="a0cf4-103">Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="a0cf4-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="a0cf4-104">I denna artikel lär du dig mer om olika aspekter av Power BI-integreringen med [!INCLUDE[prod_short](includes/prod_short.md)] i syfte att hjälpa dig förstå dess implementering och användning.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prod_short](includes/prod_short.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="a0cf4-105">Komponenter</span><span class="sxs-lookup"><span data-stu-id="a0cf4-105">Components</span></span>

<span data-ttu-id="a0cf4-106">Följande tabell beskriver de större komponenter som är involverade i Power BI-integreringen.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="a0cf4-107">Komponent</span><span class="sxs-lookup"><span data-stu-id="a0cf4-107">Component</span></span>|<span data-ttu-id="a0cf4-108">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a0cf4-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="a0cf4-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="a0cf4-109">Power BI</span></span>|<span data-ttu-id="a0cf4-110">En molnbaserad tjänst för att lagra och hantera rapporter.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="a0cf4-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a0cf4-111">Power BI Desktop</span></span>|<span data-ttu-id="a0cf4-112">Ett auktoriseringsverktyg för att skapa rapporter och instrumentpaneler som dessutom gör det möjligt för dig att köra rapporter.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="a0cf4-113">Det finns tillgängligt som kostnadsfri nedladdning från Microsoft Store oh installeras lokalt.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prod_short](includes/prod_short.md)]|<span data-ttu-id="a0cf4-114">Online- eller lokal lösning med anslutningsprogram synliga för Power BI och möjlighet för att bädda in en Power BI-del.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="a0cf4-115">Vad finns tillgängligt från början?</span><span class="sxs-lookup"><span data-stu-id="a0cf4-115">What's available from the start</span></span>

<span data-ttu-id="a0cf4-116">Följande tabell beskriver tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-116">The following table describes available features.</span></span>

|<span data-ttu-id="a0cf4-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="a0cf4-117">Feature</span></span>|[!INCLUDE[prod_short](includes/prod_short.md)]<span data-ttu-id="a0cf4-118">-support online eller lokalt</span><span class="sxs-lookup"><span data-stu-id="a0cf4-118">online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="a0cf4-119">Power BI-anslutningsprogram</span><span class="sxs-lookup"><span data-stu-id="a0cf4-119">Power BI connectors</span></span>|<span data-ttu-id="a0cf4-120">Båda.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-120">Both.</span></span> <span data-ttu-id="a0cf4-121">Olika anslutningsprogram för online och lokalt.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="a0cf4-122">Samma anslutningsprogram används för Power BI Desktop och Power BI Service</span><span class="sxs-lookup"><span data-stu-id="a0cf4-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="a0cf4-123">Inbäddad upplevelse för att visa en specifik rapport inuti en FactBox i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="a0cf4-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="a0cf4-124">Båda.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-124">Both.</span></span> <span data-ttu-id="a0cf4-125">Kräver konfigurering för att visa rapporter för lokala versioner.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="a0cf4-126">Hantering av Power BI-rapporter från [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="a0cf4-126">Power BI report management from [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="a0cf4-127">Online</span><span class="sxs-lookup"><span data-stu-id="a0cf4-127">Online</span></span>|
|<span data-ttu-id="a0cf4-128">Power BI-standardrapporter om rollcentran som distribuerats till Power BI</span><span class="sxs-lookup"><span data-stu-id="a0cf4-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="a0cf4-129">Online</span><span class="sxs-lookup"><span data-stu-id="a0cf4-129">Online</span></span>|
|<span data-ttu-id="a0cf4-130">Power BI-appar i Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="a0cf4-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="a0cf4-131">Online.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="a0cf4-132">Arkitektur</span><span class="sxs-lookup"><span data-stu-id="a0cf4-132">Architecture</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a0cf4-133">integreras med Power BI via ett anslutningsprogram som använder OData.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="a0cf4-134">Datakällan för Power BI-rapporter anges som OData-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI-arkitektur för integrering med Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="a0cf4-136">Allmänt flöde</span><span class="sxs-lookup"><span data-stu-id="a0cf4-136">General Flow</span></span>

<span data-ttu-id="a0cf4-137">Följande diagram illustrerar det grundläggande arbetsflödet för användare när [!INCLUDE[prod_short](includes/prod_short.md)] ansluts till Power BI.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prod_short](includes/prod_short.md)] to Power BI.</span></span>

![Power BI-arbetsflöde för integrering med Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="a0cf4-139">Användare registrerar sig för ett Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="a0cf4-140">Användare ansluter till Power BI från [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a0cf4-140">User connects to Power BI from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
3. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a0cf4-141">bekräftar licensen.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-141">verifies the license.</span></span>
4. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a0cf4-142">distribuerar standardrapporter till Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="a0cf4-143">Detta steg sker enbart för [!INCLUDE[prod_short](includes/prod_short.md)] online.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-143">This step only happens for [!INCLUDE[prod_short](includes/prod_short.md)] online.</span></span>
5. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a0cf4-144">gör rapporter i Power BI tillgängliga för val i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a0cf4-144">makes reports in Power BI available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a0cf4-145">Standardrapporter visas automatiskt i Power BI-delar.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="a0cf4-146">Användaren skapar en rapport i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="a0cf4-147">Användaren publicerar rapporten i Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="a0cf4-148">Rapporterna blir därefter tillgängliga för urval i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a0cf4-148">The reports are then available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="a0cf4-149">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="a0cf4-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="a0cf4-150">Se även</span><span class="sxs-lookup"><span data-stu-id="a0cf4-150">See Also</span></span>

[<span data-ttu-id="a0cf4-151">Business Central och Power BI</span><span class="sxs-lookup"><span data-stu-id="a0cf4-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="a0cf4-152">Power BI för konsumenter</span><span class="sxs-lookup"><span data-stu-id="a0cf4-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="a0cf4-153">Power BI-tjänstens "nya utseende"</span><span class="sxs-lookup"><span data-stu-id="a0cf4-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="a0cf4-154">Snabbstart: Anslut till data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a0cf4-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="a0cf4-155">Dokumentation om Power BI</span><span class="sxs-lookup"><span data-stu-id="a0cf4-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="a0cf4-156">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="a0cf4-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="a0cf4-157">Komma igång</span><span class="sxs-lookup"><span data-stu-id="a0cf4-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="a0cf4-158">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="a0cf4-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="a0cf4-159">[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="a0cf4-159">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
<span data-ttu-id="a0cf4-160">[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="a0cf4-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="a0cf4-161">[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps datakälla](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="a0cf4-161">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="a0cf4-162">[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="a0cf4-162">[Using [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
