---
title: "Skapa och publicera KPI-webbtjänster för kontouppställningar | Microsoft Docs"
description: "I fönstret **Installation av webbtjänst för KPI för kontouppställning** kan du konfigurera hur du visar kontouppställnings-kpi-data och vilka specifika kontouppställningar som du vill basera KPI-erna på."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dc1226724d1f953a3cf14a148e6d229ac0736bd3
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a><span data-ttu-id="ccd21-103">Skapa och publicera KPI-webbtjänster som baseras på kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="ccd21-103">Set Up and Publish KPI Web Services Based on Account Schedules</span></span>
<span data-ttu-id="ccd21-104">I fönstret **Installation av webbtjänst för KPI för kontouppställning** kan du konfigurera hur du visar kontouppställnings-kpi-data och vilka specifika kontouppställningar som du vill basera KPI-erna på.</span><span class="sxs-lookup"><span data-stu-id="ccd21-104">In the **Account Schedule KPI Web Service Setup** window, you set up how to show the account-schedule KPI data and which specific account schedules to base the KPIs on.</span></span> <span data-ttu-id="ccd21-105">När du väljer knappen **Publicera webbtjänst** läggs det angivna kontouppställning-kpi-data till listan över publicerade webbtjänster i fönstret **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-105">When you choose the **Publish Web Service** button, the specified account-schedule KPI data is added to the list of published web services in the **Web Services** window.</span></span>  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a><span data-ttu-id="ccd21-106">Så här: Skapar och publicerar du en KPI-webbtjänst som är baserad på kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="ccd21-106">To set up and publish a KPI web service that is based on account schedules</span></span>  

1.  <span data-ttu-id="ccd21-107">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Installation av webbtjänst för KPI för kontouppställning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ccd21-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedule KPI Web Service Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ccd21-108">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ccd21-109">Fält</span><span class="sxs-lookup"><span data-stu-id="ccd21-109">Field</span></span>|<span data-ttu-id="ccd21-110">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ccd21-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ccd21-111">**Start för prognostiserade värden**</span><span class="sxs-lookup"><span data-stu-id="ccd21-111">**Forecasted Values Start**</span></span>|<span data-ttu-id="ccd21-112">Ange vid vilken tidpunkt i prognosen som värden visas på kontouppställning-kpi-grafiken.</span><span class="sxs-lookup"><span data-stu-id="ccd21-112">Specify at what point in time forecasted values are shown on the account-schedule KPI graphic.</span></span><br /><br /> <span data-ttu-id="ccd21-113">De prognostiserade värdena hämtas från redovisningsbudgeten som du väljer i fältet **Redov.budgetnamn**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-113">The forecasted values are retrieved from the general ledger budget that you select in the **G/L Budget Name** field.</span></span> <span data-ttu-id="ccd21-114">**Obs!**  Om du vill få KPI:er att visar prognossiffror efter ett visst datum och den verkliga siffror före datumet, kan du ändra fältet **Tillåt bokföring fr.o.m.** i fönstret **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-114">**Note:**  To obtain KPIs that show forecasted figures after a certain date and actual figures before the date, you can change the **Allow Posting From** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="ccd21-115">Mer information finns också i Tillåt bokföring fr.o.m..</span><span class="sxs-lookup"><span data-stu-id="ccd21-115">For more information, see Allow Posting From.</span></span>|  
    |<span data-ttu-id="ccd21-116">**Redov.budgetnamn**</span><span class="sxs-lookup"><span data-stu-id="ccd21-116">**G/L Budget Name**</span></span>|<span data-ttu-id="ccd21-117">Ange namnet på den redovisningsbudget som ger prognostiserade värden till kontouppställning-kpi-webbtjänsten.</span><span class="sxs-lookup"><span data-stu-id="ccd21-117">Specify the name of the general ledger budget that provides forecasted values to the account-schedule KPI web service.</span></span>|  
    |<span data-ttu-id="ccd21-118">**Period**</span><span class="sxs-lookup"><span data-stu-id="ccd21-118">**Period**</span></span>|<span data-ttu-id="ccd21-119">Ange perioden som kontouppställning-KPI-webbtjänsten baseras på.</span><span class="sxs-lookup"><span data-stu-id="ccd21-119">Specify the period that the account-schedule KPI web service is based on.</span></span>|  
    |<span data-ttu-id="ccd21-120">**Visa per**</span><span class="sxs-lookup"><span data-stu-id="ccd21-120">**View By**</span></span>|<span data-ttu-id="ccd21-121">Ange vid vilket tidsintervall kontouppställning-KPI visas i.</span><span class="sxs-lookup"><span data-stu-id="ccd21-121">Specify which time interval the account-schedule KPI is shown in.</span></span>|  
    |<span data-ttu-id="ccd21-122">**Webbtjänstnamn**</span><span class="sxs-lookup"><span data-stu-id="ccd21-122">**Web Service Name**</span></span>|<span data-ttu-id="ccd21-123">Ange namnet på kontouppställningen-KPI-webbtjänsten.</span><span class="sxs-lookup"><span data-stu-id="ccd21-123">Specify the name of the account-schedule KPI web service.</span></span><br /><br /> <span data-ttu-id="ccd21-124">Det här namn visas i fältet **Servicenamn** i fönstret **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-124">This name will appear in the **Service Name** field in the **Web Services** window.</span></span>|  

    <span data-ttu-id="ccd21-125">Fortsätt genom att ange en eller flera kontouppställningar som du vill publicera som en KPI webbtjänst enligt inställningarna, som du gjorde i föregående tabellen.</span><span class="sxs-lookup"><span data-stu-id="ccd21-125">Proceed to specify one or more account schedules that you want to publish as a KPI web service according to the setup that you made in the previous table.</span></span>  

3.  <span data-ttu-id="ccd21-126">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **kontouppställningar**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-126">On the **Account Schedules** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ccd21-127">Fält</span><span class="sxs-lookup"><span data-stu-id="ccd21-127">Field</span></span>|<span data-ttu-id="ccd21-128">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ccd21-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ccd21-129">**Kontouppställningsnamn**</span><span class="sxs-lookup"><span data-stu-id="ccd21-129">**Acc. Schedule Name**</span></span>|<span data-ttu-id="ccd21-130">Ange kontouppställningen som KPI-webbtjänsten baseras på.</span><span class="sxs-lookup"><span data-stu-id="ccd21-130">Specify the account schedule that the KPI web service is based on.</span></span>|  
    |<span data-ttu-id="ccd21-131">**Beskrivning av kontouppställning**</span><span class="sxs-lookup"><span data-stu-id="ccd21-131">**Acc. Schedule Description**</span></span>|<span data-ttu-id="ccd21-132">Ange beskrivningen av kontouppställningen som KPI webbtjänsten baseras på.</span><span class="sxs-lookup"><span data-stu-id="ccd21-132">Specify the description of the account schedule that the KPI web service is based on.</span></span>|  

4.  <span data-ttu-id="ccd21-133">Upprepa moment 3 för alla kontouppställningar som du vill basera kontouppställningswebbtjänsten för kpi på.</span><span class="sxs-lookup"><span data-stu-id="ccd21-133">Repeat step 3 for all the account schedules that you want to base the account-schedule KPI web service on.</span></span>  
5.  <span data-ttu-id="ccd21-134">Välj åtgärden **Redigera kontouppställning** på snabbfliken **Kontouppställning** för att visa eller redigera den valda kontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="ccd21-134">To view or edit the selected account schedule, on the **Account Schedule** FastTab, choose the **Edit Account Schedule** action.</span></span>  
6.  <span data-ttu-id="ccd21-135">Om du vill visa kontouppställning-kpi-data som du har upprättat väljer du åtgärden **Webbtjänst för KPI för kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-135">To view the account-schedule KPI data that you have set up, choose the **Account Schedule KPI Web Service** action.</span></span>  
7.  <span data-ttu-id="ccd21-136">Om du vill publicera kontouppställningens KPI-webbtjänst väljer du åtgärden **Publicera webbtjänst**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-136">To publish the account-schedule KPI web service, choose the **Publish Web Service** action.</span></span> <span data-ttu-id="ccd21-137">Webbtjänsten läggs till i listan över publicerade webbtjänster i fönstret **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-137">The web service is added to the list of published web services in the **Web Services** window.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ccd21-138">Du kan också publicera KPI webbtjänsten genom att peka på sidobjektet **KPI Web Service kontouppställningsinställning** från fönstret **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="ccd21-138">You can also publish the KPI web service by pointing to the **Account Schedule KPI Web Service Setup** page object from the **Web Services** window.</span></span> <span data-ttu-id="ccd21-139">Mer information finns i [Publicera en webbtjänst](across-how-publish-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="ccd21-139">For more information, see [Publish a Web Service](across-how-publish-web-service.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ccd21-140">Se även</span><span class="sxs-lookup"><span data-stu-id="ccd21-140">See Also</span></span>  
[<span data-ttu-id="ccd21-141">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="ccd21-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="ccd21-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="ccd21-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="ccd21-143">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="ccd21-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="ccd21-144">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="ccd21-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="ccd21-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ccd21-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
