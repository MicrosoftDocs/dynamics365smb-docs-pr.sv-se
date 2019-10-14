---
title: Använda din adata för att skapa en app | Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa en företagsapp med PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305035"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="2d348-103">Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av PowerApps</span><span class="sxs-lookup"><span data-stu-id="2d348-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="2d348-104">Du kan göra din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tillgänglig som underlag för datakälla i PowerApps.</span><span class="sxs-lookup"><span data-stu-id="2d348-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="2d348-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med PowerApps.</span><span class="sxs-lookup"><span data-stu-id="2d348-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="2d348-106">Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i PowerApps.</span><span class="sxs-lookup"><span data-stu-id="2d348-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="2d348-107">I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), och loggar in.</span><span class="sxs-lookup"><span data-stu-id="2d348-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="2d348-108">På startsidan, välj **Appar**, **Skapa en app** och **Arbetsyta** för att skapa en ny arbetsyteapp.</span><span class="sxs-lookup"><span data-stu-id="2d348-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="2d348-109">Det här programmet kommer att vara konstruerat för användning på en mobil enhet, men du kan även välja att använda en annan mall.</span><span class="sxs-lookup"><span data-stu-id="2d348-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="2d348-110">Nästa steg för att skapa en PowerApp är att välja data.</span><span class="sxs-lookup"><span data-stu-id="2d348-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="2d348-111">Välj pilikonen och välj sedan alternativet **ny anslutning** i det övre vänstra delen på sidan.</span><span class="sxs-lookup"><span data-stu-id="2d348-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="2d348-112">Välj **Business Central** i listan över tillgängliga anslutningar och välj sedan knappen **skapa**.</span><span class="sxs-lookup"><span data-stu-id="2d348-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="2d348-113">PowerApps kommer att ansluta till [!INCLUDE [prodshort](includes/prodshort.md)] med hjälp av autentiseringsuppgifterna som du har loggat in med.</span><span class="sxs-lookup"><span data-stu-id="2d348-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="2d348-114">Om du inte är administratör för ditt [!INCLUDE [prodshort](includes/prodshort.md)] måste du kanske logga in med ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="2d348-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="2d348-115">PowerApps visar en lista över *Miljöer och företag* som finns på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2d348-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2d348-116">Välj den miljö och det företag som innehåller de data som du vill ansluta till.</span><span class="sxs-lookup"><span data-stu-id="2d348-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="2d348-117">Sedan visas en lista med API:er.</span><span class="sxs-lookup"><span data-stu-id="2d348-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="2d348-118">Markera den **API** som du vill ansluta till.</span><span class="sxs-lookup"><span data-stu-id="2d348-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="2d348-119">De s.k. tabellerna är en del av [!INCLUDE [prodshort](includes/prodshort.md)] API.</span><span class="sxs-lookup"><span data-stu-id="2d348-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="2d348-120">Du behöver inte konfigurera slutpunkterna själv, [!INCLUDE [prodshort](includes/prodshort.md)]-kopplingen för PowerApps gör det åt dig.</span><span class="sxs-lookup"><span data-stu-id="2d348-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="2d348-121">Nu har du lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data och är redo att börja skapa din Power BI.</span><span class="sxs-lookup"><span data-stu-id="2d348-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="2d348-122">Du kan lägga till ytterligare skärmar och ansluta till ytterligare data från [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2d348-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2d348-123">Mer information finns i [Skapa en arbetsyteapp från en mall i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="2d348-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="2d348-124">När du har skapat och byggt ditt program kan du dela den med dina kollegor.</span><span class="sxs-lookup"><span data-stu-id="2d348-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="2d348-125">Mer information finns i [Spara och publicera en arbetsyteapp i PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="2d348-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="2d348-126">Om du vill ansluta till [!INCLUDE [prodshort](includes/prodshort.md)] lokalt måste du välja anslutningen **Business Central (lokal)** i steg 3.</span><span class="sxs-lookup"><span data-stu-id="2d348-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d348-127">Se även</span><span class="sxs-lookup"><span data-stu-id="2d348-127">See Also</span></span>

[<span data-ttu-id="2d348-128">Skapa en arbetsyteapp från en mall i PowerApps</span><span class="sxs-lookup"><span data-stu-id="2d348-128">Create a canvas app from a template in PowerApps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="2d348-129">Komma igång</span><span class="sxs-lookup"><span data-stu-id="2d348-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="2d348-130">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="2d348-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="2d348-131">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="2d348-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="2d348-132">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="2d348-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="2d348-133">Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="2d348-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
