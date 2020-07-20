---
title: Använd Business Central i Power BI-rapporter | Microsoft Docs
description: Gör din data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528468"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="bcedd-103">Använda [!INCLUDE[prodlong](includes/prodlong.md)] som Power BI-datakälla för att skapa rapporter</span><span class="sxs-lookup"><span data-stu-id="bcedd-103">Using [!INCLUDE[prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="bcedd-104">Gör din [!INCLUDE[prodlong](includes/prodlong.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.</span><span class="sxs-lookup"><span data-stu-id="bcedd-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="bcedd-105">Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="bcedd-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="bcedd-106">Du måste även ladda ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="bcedd-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="bcedd-107">Mer information finns i [snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="bcedd-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="bcedd-108">Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="bcedd-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="bcedd-109">I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.</span><span class="sxs-lookup"><span data-stu-id="bcedd-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="bcedd-110">I fönstret **Hämta data** väljer du **onlinetjänster**, väljer **Microsoft Dynamics 365 Business Central** och sedan knappen **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="bcedd-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="bcedd-111">Power BI isar en guide som vägleder dig genom anslutningsprocessen, inklusive hur du loggar in på [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="bcedd-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="bcedd-112">Välj **Logga in** och välj sedan det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="bcedd-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="bcedd-113">Använd samma konto som du loggar in i [!INCLUDE[prodshort](includes/prodshort.md)] med.</span><span class="sxs-lookup"><span data-stu-id="bcedd-113">Use the same account that you sign into [!INCLUDE[prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="bcedd-114">Välj knappen **Anslut** för att fortsätta.</span><span class="sxs-lookup"><span data-stu-id="bcedd-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="bcedd-115">Power BI-guiden visar en lista över Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljöer, -företag och -datakällor.</span><span class="sxs-lookup"><span data-stu-id="bcedd-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="bcedd-116">Dessa datakällor motsvarar samtliga de webbtjänster som du har publicerat från [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="bcedd-116">These data sources represent all the web services that you have published from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="bcedd-117">Du kan också skapa en ny URL för webbtjänst i [!INCLUDE[prodshort](includes/prodshort.md)] istället.</span><span class="sxs-lookup"><span data-stu-id="bcedd-117">You can also create a new web service URL in [!INCLUDE[prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="bcedd-118">Välj någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="bcedd-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="bcedd-119">Använd åtgärden **Skapa datauppsättning** på sidan **Webbtjänster**</span><span class="sxs-lookup"><span data-stu-id="bcedd-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="bcedd-120">Använd den assisterade konfigurationsguiden **Ställa in rapportering**</span><span class="sxs-lookup"><span data-stu-id="bcedd-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="bcedd-121">Välj åtgärden **Redigera i Excel** i alla listor</span><span class="sxs-lookup"><span data-stu-id="bcedd-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="bcedd-122">Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.</span><span class="sxs-lookup"><span data-stu-id="bcedd-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="bcedd-123">Upprepa stegen för att lägga till ytterligare [!INCLUDE[prodshort](includes/prodshort.md)] eller andra data till Power BI-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="bcedd-123">Repeat the previous steps to add additional [!INCLUDE[prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="bcedd-124">När du har anslutit till [!INCLUDE[prodshort](includes/prodshort.md)] kommer du inte att uppmanas att logga in på nytt.</span><span class="sxs-lookup"><span data-stu-id="bcedd-124">Once you have successfully connected to [!INCLUDE[prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="bcedd-125">När datan har lästs in kan du se den i den högra navigeringen på sidan.</span><span class="sxs-lookup"><span data-stu-id="bcedd-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="bcedd-126">Du har nu lyckats ansluta till dina [!INCLUDE[prodshort](includes/prodshort.md)]-data, och du kan nu börja skapa din Power BI-rapport.</span><span class="sxs-lookup"><span data-stu-id="bcedd-126">You have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="bcedd-127">Innan du skapar rapporten bör du importera [!INCLUDE[prodshort](includes/prodshort.md)]-temafilen.</span><span class="sxs-lookup"><span data-stu-id="bcedd-127">Before building your report, we recommend that you import the [!INCLUDE[prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="bcedd-128">Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färger som [!INCLUDE[prodshort](includes/prodshort.md)]-appar utan att behöva definiera anpassade färger för varje bild.</span><span class="sxs-lookup"><span data-stu-id="bcedd-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE[prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="bcedd-129">Mer information finns i [Power BI dokumentation](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="bcedd-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="bcedd-130">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="bcedd-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="bcedd-131">Se även</span><span class="sxs-lookup"><span data-stu-id="bcedd-131">See Also</span></span>

[<span data-ttu-id="bcedd-132">Aktivera affärsdata för Power BI</span><span class="sxs-lookup"><span data-stu-id="bcedd-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="bcedd-133">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="bcedd-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="bcedd-134">Komma igång</span><span class="sxs-lookup"><span data-stu-id="bcedd-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="bcedd-135">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="bcedd-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="bcedd-136">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="bcedd-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="bcedd-137">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="bcedd-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="bcedd-138">Snabbstart: Ansluta till data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bcedd-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
