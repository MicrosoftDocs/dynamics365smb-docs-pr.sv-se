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
ms.openlocfilehash: d02740b0f4c73b96be9268cfdf5e4c3de157d5d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924534"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a><span data-ttu-id="59a56-103">Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="59a56-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="59a56-104">I denna artikel lär du dig mer om olika aspekter av Power BI-integreringen med [!INCLUDE[prodshort](includes/prodshort.md)] i syfte att hjälpa dig förstå dess implementering och användning.</span><span class="sxs-lookup"><span data-stu-id="59a56-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prodshort](includes/prodshort.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="59a56-105">Komponenter</span><span class="sxs-lookup"><span data-stu-id="59a56-105">Components</span></span>

<span data-ttu-id="59a56-106">Följande tabell beskriver de större komponenter som är involverade i Power BI-integreringen.</span><span class="sxs-lookup"><span data-stu-id="59a56-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="59a56-107">Komponent</span><span class="sxs-lookup"><span data-stu-id="59a56-107">Component</span></span>|<span data-ttu-id="59a56-108">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="59a56-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="59a56-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="59a56-109">Power BI</span></span>|<span data-ttu-id="59a56-110">En molnbaserad tjänst för att lagra och hantera rapporter.</span><span class="sxs-lookup"><span data-stu-id="59a56-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="59a56-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="59a56-111">Power BI Desktop</span></span>|<span data-ttu-id="59a56-112">Ett auktoriseringsverktyg för att skapa rapporter och instrumentpaneler som dessutom gör det möjligt för dig att köra rapporter.</span><span class="sxs-lookup"><span data-stu-id="59a56-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="59a56-113">Det finns tillgängligt som kostnadsfri nedladdning från Microsoft Store oh installeras lokalt.</span><span class="sxs-lookup"><span data-stu-id="59a56-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prodshort](includes/prodshort.md)]|<span data-ttu-id="59a56-114">Online- eller lokal lösning med anslutningsprogram synliga för Power BI och möjlighet för att bädda in en Power BI-del.</span><span class="sxs-lookup"><span data-stu-id="59a56-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="59a56-115">Vad finns tillgängligt från början?</span><span class="sxs-lookup"><span data-stu-id="59a56-115">What's available from the start</span></span>

<span data-ttu-id="59a56-116">Följande tabell beskriver tillgängliga funktioner.</span><span class="sxs-lookup"><span data-stu-id="59a56-116">The following table describes available features.</span></span>

|<span data-ttu-id="59a56-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="59a56-117">Feature</span></span>|[!INCLUDE[prodshort](includes/prodshort.md)]<span data-ttu-id="59a56-118">-support online eller lokalt</span><span class="sxs-lookup"><span data-stu-id="59a56-118">online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="59a56-119">Power BI-anslutningsprogram</span><span class="sxs-lookup"><span data-stu-id="59a56-119">Power BI connectors</span></span>|<span data-ttu-id="59a56-120">Båda.</span><span class="sxs-lookup"><span data-stu-id="59a56-120">Both.</span></span> <span data-ttu-id="59a56-121">Olika anslutningsprogram för online och lokalt.</span><span class="sxs-lookup"><span data-stu-id="59a56-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="59a56-122">Samma anslutningsprogram används för Power BI Desktop och Power BI Service</span><span class="sxs-lookup"><span data-stu-id="59a56-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="59a56-123">Inbäddad upplevelse för att visa en specifik rapport inuti en FactBox i [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="59a56-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="59a56-124">Båda.</span><span class="sxs-lookup"><span data-stu-id="59a56-124">Both.</span></span> <span data-ttu-id="59a56-125">Kräver konfigurering för att visa rapporter för lokala versioner.</span><span class="sxs-lookup"><span data-stu-id="59a56-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="59a56-126">Hantering av Power BI-rapporter från [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="59a56-126">Power BI report management from [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="59a56-127">Online</span><span class="sxs-lookup"><span data-stu-id="59a56-127">Online</span></span>|
|<span data-ttu-id="59a56-128">Power BI-standardrapporter om rollcentran som distribuerats till Power BI</span><span class="sxs-lookup"><span data-stu-id="59a56-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="59a56-129">Online</span><span class="sxs-lookup"><span data-stu-id="59a56-129">Online</span></span>|
|<span data-ttu-id="59a56-130">Power BI-appar i Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="59a56-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="59a56-131">Online.</span><span class="sxs-lookup"><span data-stu-id="59a56-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="59a56-132">Arkitektur</span><span class="sxs-lookup"><span data-stu-id="59a56-132">Architecture</span></span>

[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="59a56-133">integreras med Power BI via ett anslutningsprogram som använder OData.</span><span class="sxs-lookup"><span data-stu-id="59a56-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="59a56-134">Datakällan för Power BI-rapporter anges som OData-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="59a56-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI-arkitektur för integrering med Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="59a56-136">Allmänt flöde</span><span class="sxs-lookup"><span data-stu-id="59a56-136">General Flow</span></span>

<span data-ttu-id="59a56-137">Följande diagram illustrerar det grundläggande arbetsflödet för användare när [!INCLUDE[prodshort](includes/prodshort.md)] ansluts till Power BI.</span><span class="sxs-lookup"><span data-stu-id="59a56-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prodshort](includes/prodshort.md)] to Power BI.</span></span>

![Power BI-arbetsflöde för integrering med Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="59a56-139">Användare registrerar sig för ett Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="59a56-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="59a56-140">Användare ansluter till Power BI från [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="59a56-140">User connects to Power BI from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>
3. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="59a56-141">bekräftar licensen.</span><span class="sxs-lookup"><span data-stu-id="59a56-141">verifies the license.</span></span>
4. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="59a56-142">distribuerar standardrapporter till Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="59a56-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="59a56-143">Detta steg sker enbart för [!INCLUDE[prodshort](includes/prodshort.md)] online.</span><span class="sxs-lookup"><span data-stu-id="59a56-143">This step only happens for [!INCLUDE[prodshort](includes/prodshort.md)] online.</span></span>
5. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="59a56-144">gör rapporter i Power BI tillgängliga för val i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="59a56-144">makes reports in Power BI available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="59a56-145">Standardrapporter visas automatiskt i Power BI-delar.</span><span class="sxs-lookup"><span data-stu-id="59a56-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="59a56-146">Användaren skapar en rapport i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="59a56-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="59a56-147">Användaren publicerar rapporten i Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="59a56-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="59a56-148">Rapporterna blir därefter tillgängliga för urval i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="59a56-148">The reports are then available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="59a56-149">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="59a56-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="59a56-150">Se även</span><span class="sxs-lookup"><span data-stu-id="59a56-150">See Also</span></span>

[<span data-ttu-id="59a56-151">Business Central och Power BI</span><span class="sxs-lookup"><span data-stu-id="59a56-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="59a56-152">Power BI för konsumenter</span><span class="sxs-lookup"><span data-stu-id="59a56-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="59a56-153">Power BI-tjänstens "nya utseende"</span><span class="sxs-lookup"><span data-stu-id="59a56-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="59a56-154">Snabbstart: Anslut till data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="59a56-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="59a56-155">Dokumentation om Power BI</span><span class="sxs-lookup"><span data-stu-id="59a56-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="59a56-156">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="59a56-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="59a56-157">Komma igång</span><span class="sxs-lookup"><span data-stu-id="59a56-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="59a56-158">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="59a56-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="59a56-159">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="59a56-159">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
<span data-ttu-id="59a56-160">[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="59a56-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="59a56-161">[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power Apps datakälla](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="59a56-161">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="59a56-162">[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="59a56-162">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
