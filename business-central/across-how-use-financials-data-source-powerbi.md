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
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755247"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="6a54e-103">Använda [!INCLUDE [prodlong](includes/prodlong.md)] som Power BI-datakälla för att skapa rapporter</span><span class="sxs-lookup"><span data-stu-id="6a54e-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="6a54e-104">Gör din [!INCLUDE[prodlong](includes/prodlong.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.</span><span class="sxs-lookup"><span data-stu-id="6a54e-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="6a54e-105">Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="6a54e-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="6a54e-106">Dessutom kan du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="6a54e-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span> <span data-ttu-id="6a54e-107">Mer information finns i [snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="6a54e-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="6a54e-108">Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="6a54e-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="6a54e-109">I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.</span><span class="sxs-lookup"><span data-stu-id="6a54e-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="6a54e-110">I fönstret **Hämta data** väljer du **onlinetjänster**, väljer **Microsoft Dynamics 365 Business Central** och sedan knappen **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="6a54e-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="6a54e-111">Power BI visar en guide som vägleder dig genom anslutningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="6a54e-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="6a54e-112">Du uppmanas då att logga in på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6a54e-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="6a54e-113">Välj **Logga in** och välj det konto som du vill logga in som.</span><span class="sxs-lookup"><span data-stu-id="6a54e-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="6a54e-114">Detta bör vara samma konto som du loggar in i [!INCLUDE [prodshort](includes/prodshort.md)] med.</span><span class="sxs-lookup"><span data-stu-id="6a54e-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="6a54e-115">Välj knappen **Anslut** för att fortsätta.</span><span class="sxs-lookup"><span data-stu-id="6a54e-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="6a54e-116">Power BI-guiden visar en lista över Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag och -datakällor.</span><span class="sxs-lookup"><span data-stu-id="6a54e-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="6a54e-117">Dessa datakällor motsvarar alla de webbtjänster som du har publicerat från respektive företag i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6a54e-117">These data source represent all the web services that you have published from each company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. <span data-ttu-id="6a54e-119">Du kan också skapa en ny webbtjänst-URL i [!INCLUDE [prodshort](includes/prodshort.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.</span><span class="sxs-lookup"><span data-stu-id="6a54e-119">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="6a54e-120">Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.</span><span class="sxs-lookup"><span data-stu-id="6a54e-120">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="6a54e-121">Upprepa stegen för att lägga till ytterligare [!INCLUDE [prodshort](includes/prodshort.md)] eller andra data till Power BI-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="6a54e-121">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="6a54e-122">När du har anslutit till [!INCLUDE [prodshort](includes/prodshort.md)] kommer du inte att uppmanas att logga in på nytt.</span><span class="sxs-lookup"><span data-stu-id="6a54e-122">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="6a54e-123">När data har lästs in kommer den att visas i den högra navigeringen på sidan.</span><span class="sxs-lookup"><span data-stu-id="6a54e-123">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="6a54e-124">Nu har du lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data och är redo att börja skapa Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="6a54e-124">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="6a54e-125">Innan du skapar rapporten bör du importera [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen.</span><span class="sxs-lookup"><span data-stu-id="6a54e-125">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="6a54e-126">Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färger som [!INCLUDE [prodshort](includes/prodshort.md)]-appar utan att behöva definiera anpassade färger för varje bild.</span><span class="sxs-lookup"><span data-stu-id="6a54e-126">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="6a54e-127">Mer information finns i [Power BI dokumentation](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="6a54e-127">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="6a54e-128">Se även</span><span class="sxs-lookup"><span data-stu-id="6a54e-128">See Also</span></span>

[<span data-ttu-id="6a54e-129">Aktivera affärsdata för Power BI</span><span class="sxs-lookup"><span data-stu-id="6a54e-129">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="6a54e-130">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="6a54e-130">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="6a54e-131">Komma igång</span><span class="sxs-lookup"><span data-stu-id="6a54e-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="6a54e-132">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="6a54e-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="6a54e-133">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="6a54e-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="6a54e-134">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="6a54e-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="6a54e-135">Snabbstart: Ansluta till data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="6a54e-135">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
