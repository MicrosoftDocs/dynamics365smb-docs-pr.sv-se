---
title: "Konfigurera Rapportering för Business Central i Power BI | Microsoft Docs"
description: "Du kan göra din Financials-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42939e97d121bd3a2abff91671d9f9571faffbfd
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="f4bb7-103">Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakälla för att skapa rapporter</span><span class="sxs-lookup"><span data-stu-id="f4bb7-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as Power BI Data Source for Building Reports</span></span>
<span data-ttu-id="f4bb7-104">Du kan göra din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

> [!NOTE]  
> <span data-ttu-id="f4bb7-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="f4bb7-106">Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="f4bb7-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="f4bb7-107">Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f4bb7-107">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Power BI Desktop</span></span>
1. <span data-ttu-id="f4bb7-108">I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-108">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="f4bb7-109">I fönstret **Hämta data** väljer du **Onlinetjänster**, **Dynamics 365 Business Central** och sedan knappen **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-109">In the **Get Data** window, choose **Online Services**, choose **Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="f4bb7-110">Power BI visar en guide som vägleder dig genom [anslutningsprocessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md).</span><span class="sxs-lookup"><span data-stu-id="f4bb7-110">Power BI displays a wizard that will guide you through the [connection process](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md).</span></span> <span data-ttu-id="f4bb7-111">Det första steget är att logga in på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-111">The first step will be to sign into the service.</span></span> <span data-ttu-id="f4bb7-112">Välj **Logga in** och välj det konto som du vill logga in som.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-112">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="f4bb7-113">Detta bör vara samma konto som du loggar in i [!INCLUDE[d365fin](includes/d365fin_md.md)] med.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-113">This should be the same account you sign into [!INCLUDE[d365fin](includes/d365fin_md.md)] with.</span></span>
4. <span data-ttu-id="f4bb7-114">Välj knappen **Anslut** för att fortsätta.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="f4bb7-115">Power BI-guiden visar en lista över [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag och -datakällor.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-115">The Power BI wizard shows a list of [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="f4bb7-116">Dessa datakällor motsvarar alla de webbtjänster som du har publicerat från respektive företag i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f4bb7-116">These data source represent all the web services that you have published from each company in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
5. <span data-ttu-id="f4bb7-117">Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **Skapa datauppsättning** på sidan **Webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering** eller genom att välja åtgärden **Redigera i Excel** i valfri lista.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-117">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="f4bb7-118">Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-118">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="f4bb7-119">Upprepa stegen för att lägga till ytterligare [!INCLUDE[d365fin](includes/d365fin_md.md)]-data till Power BI-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-119">Repeat the previous steps to add additional [!INCLUDE[d365fin](includes/d365fin_md.md)] data to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="f4bb7-120">När du har anslutit till [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer du inte att uppmanas att logga in på nytt.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-120">Once you have successfully connected to [!INCLUDE[d365fin](includes/d365fin_md.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="f4bb7-121">När data har lästs in kommer den att visas i den högra navigeringen på sidan.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-121">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="f4bb7-122">Du har nu lyckats ansluta till dina Business Central-data och kan börja skapa din Power BI-rapport.</span><span class="sxs-lookup"><span data-stu-id="f4bb7-122">At this point, you have successfully connected to your Business Central data and are ready to begin building your Power BI report.</span></span> <span data-ttu-id="f4bb7-123">Mer information finns i [Power BI dokumentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).</span><span class="sxs-lookup"><span data-stu-id="f4bb7-123">For more information, see the [Power BI documentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).</span></span>

## <a name="see-also"></a><span data-ttu-id="f4bb7-124">Se även</span><span class="sxs-lookup"><span data-stu-id="f4bb7-124">See Also</span></span>
[<span data-ttu-id="f4bb7-125">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="f4bb7-125">Business Intelligence</span></span>](bi.md)  
<span data-ttu-id="f4bb7-126">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="f4bb7-126">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="f4bb7-127">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="f4bb7-127">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="f4bb7-128">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md) </span><span class="sxs-lookup"><span data-stu-id="f4bb7-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md) </span></span>  
[<span data-ttu-id="f4bb7-129">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="f4bb7-129">Finance</span></span>](finance.md)  
<span data-ttu-id="f4bb7-130">[Ansluta Power BI till [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)</span><span class="sxs-lookup"><span data-stu-id="f4bb7-130">[Connecting Power BI to [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)</span></span>  

