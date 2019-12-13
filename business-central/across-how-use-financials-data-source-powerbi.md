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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: c843f0fb6c8017817ada9dc5bf2af0ef68a5cc5a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878754"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="01452-103">Använda [!INCLUDE [prodlong](includes/prodlong.md)] som Power BI-datakälla för att skapa rapporter</span><span class="sxs-lookup"><span data-stu-id="01452-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="01452-104">Gör din [!INCLUDE[prodlong](includes/prodlong.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.</span><span class="sxs-lookup"><span data-stu-id="01452-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="01452-105">Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="01452-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="01452-106">Dessutom kan du hämta [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="01452-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="01452-107">Mer information finns i [snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="01452-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="01452-108">Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="01452-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="01452-109">I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.</span><span class="sxs-lookup"><span data-stu-id="01452-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="01452-110">I fönstret **Hämta data** väljer du **onlinetjänster**, väljer **Microsoft Dynamics 365 Business Central** och sedan knappen **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="01452-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="01452-111">Power BI visar en guide som vägleder dig genom anslutningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="01452-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="01452-112">Du uppmanas då att logga in på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="01452-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="01452-113">Välj **Logga in** och välj det konto som du vill logga in som.</span><span class="sxs-lookup"><span data-stu-id="01452-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="01452-114">Detta bör vara samma konto som du loggar in i [!INCLUDE [prodshort](includes/prodshort.md)] med.</span><span class="sxs-lookup"><span data-stu-id="01452-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="01452-115">Välj knappen **Anslut** för att fortsätta.</span><span class="sxs-lookup"><span data-stu-id="01452-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="01452-116">Power BI-guiden visar en lista över Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljöer, -företag och -datakällor.</span><span class="sxs-lookup"><span data-stu-id="01452-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies and data sources.</span></span> <span data-ttu-id="01452-117">Dessa datakällor motsvarar alla de webbtjänster som du har publicerat från respektive klientorganisation/företag i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="01452-117">These data source represent all the web services that you have published from each tenant/company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
5. <span data-ttu-id="01452-118">Du kan också skapa en ny webbtjänst-URL i [!INCLUDE [prodshort](includes/prodshort.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.</span><span class="sxs-lookup"><span data-stu-id="01452-118">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="01452-119">Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.</span><span class="sxs-lookup"><span data-stu-id="01452-119">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="01452-120">Upprepa stegen för att lägga till ytterligare [!INCLUDE [prodshort](includes/prodshort.md)] eller andra data till Power BI-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="01452-120">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="01452-121">När du har anslutit till [!INCLUDE [prodshort](includes/prodshort.md)] kommer du inte att uppmanas att logga in på nytt.</span><span class="sxs-lookup"><span data-stu-id="01452-121">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="01452-122">När data har lästs in kommer den att visas i den högra navigeringen på sidan.</span><span class="sxs-lookup"><span data-stu-id="01452-122">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="01452-123">Nu har du lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data och är redo att börja skapa Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="01452-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="01452-124">Innan du skapar rapporten bör du importera [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen.</span><span class="sxs-lookup"><span data-stu-id="01452-124">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="01452-125">Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färger som [!INCLUDE [prodshort](includes/prodshort.md)]-appar utan att behöva definiera anpassade färger för varje bild.</span><span class="sxs-lookup"><span data-stu-id="01452-125">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="01452-126">Mer information finns i [Power BI dokumentation](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="01452-126">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="01452-127">Se även</span><span class="sxs-lookup"><span data-stu-id="01452-127">See Also</span></span>

[<span data-ttu-id="01452-128">Aktivera affärsdata för Power BI</span><span class="sxs-lookup"><span data-stu-id="01452-128">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="01452-129">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="01452-129">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="01452-130">Komma igång</span><span class="sxs-lookup"><span data-stu-id="01452-130">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="01452-131">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="01452-131">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="01452-132">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="01452-132">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="01452-133">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="01452-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="01452-134">Snabbstart: Ansluta till data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="01452-134">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
