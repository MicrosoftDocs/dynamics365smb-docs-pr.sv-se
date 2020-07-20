---
title: Använda din adata för att skapa en app | Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa en företagsapp med Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 8f0eb7a1562a8300bd7181ef6470c70f60934470
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528644"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="af809-103">Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av Power Apps</span><span class="sxs-lookup"><span data-stu-id="af809-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="af809-104">Du kan göra din [!INCLUDE[prodshort](includes/prodshort.md)]-data tillgänglig som underlag för datakälla i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="af809-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="af809-105">Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power Apps.</span><span class="sxs-lookup"><span data-stu-id="af809-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="af809-106">Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="af809-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="af809-107">I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/), och loggar in.</span><span class="sxs-lookup"><span data-stu-id="af809-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="af809-108">På startsidan, i avsnittet **Starta från data** välj panelen **Andra datakällor**.</span><span class="sxs-lookup"><span data-stu-id="af809-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="af809-109">Då öppnas Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="af809-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="af809-110">Vid första inloggningen måste du ange land/region.</span><span class="sxs-lookup"><span data-stu-id="af809-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="af809-111">Välj **Business Central** i listan över tillgängliga anslutningar och välj sedan knappen **skapa**.</span><span class="sxs-lookup"><span data-stu-id="af809-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="af809-112">Power Apps kommer att ansluta till [!INCLUDE[prodshort](includes/prodshort.md)] med hjälp av autentiseringsuppgifterna som du har loggat in med.</span><span class="sxs-lookup"><span data-stu-id="af809-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="af809-113">Om du inte är administratör för ditt [!INCLUDE[prodshort](includes/prodshort.md)] måste du kanske logga in med ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="af809-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="af809-114">Power Apps visar en lista över *Miljöer och företag* som finns på [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="af809-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="af809-115">Välj den miljö och det företag som innehåller de data som du vill ansluta till t.ex. *PRODUKTION - Mitt företag*.</span><span class="sxs-lookup"><span data-stu-id="af809-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="af809-116">Sedan visas en lista över tabeller som visas som en del av API för din miljö.</span><span class="sxs-lookup"><span data-stu-id="af809-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="af809-117">Markera den tabell som du vill ansluta till och välj sedan **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="af809-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="af809-118">Dessa så kallade tabeller visas som [!INCLUDE[prodshort](includes/prodshort.md)] kopplingen för Power Apps.</span><span class="sxs-lookup"><span data-stu-id="af809-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="af809-119">Om du vill ta med data från andra tabeller i [!INCLUDE[prodshort](includes/prodshort.md)] i din app, måste du samarbeta med en utvecklare för att definiera en anpassad API i [!INCLUDE[prodshort](includes/prodshort.md)] och sedan använda denna anpassade API via en anpassad anslutning i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="af809-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="af809-120">Mer information finns i [skapa en egen anslutning från början.](/connectors/custom-connectors/define-blank)</span><span class="sxs-lookup"><span data-stu-id="af809-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="af809-121">Nu har du lyckats ansluta till dina [!INCLUDE[prodshort](includes/prodshort.md)]-data och är redo att börja skapa din Power BI.</span><span class="sxs-lookup"><span data-stu-id="af809-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="af809-122">Du kan lägga till ytterligare skärmar och ansluta till ytterligare data från [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="af809-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="af809-123">Mer information finns i [Skapa en arbetsyteapp från ett exempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="af809-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="af809-124">När du har skapat och byggt ditt program kan du dela den med dina kollegor.</span><span class="sxs-lookup"><span data-stu-id="af809-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="af809-125">Mer information finns i [Spara och publicera en arbetsyteapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="af809-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="af809-126">Om du vill ansluta till [!INCLUDE[prodshort](includes/prodshort.md)] lokalt måste du välja anslutningen **Business Central (lokal)** i steg 3.</span><span class="sxs-lookup"><span data-stu-id="af809-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af809-127">Se även</span><span class="sxs-lookup"><span data-stu-id="af809-127">See Also</span></span>

[<span data-ttu-id="af809-128">Skapa en arbetsyteapp från en mall i Power Apps</span><span class="sxs-lookup"><span data-stu-id="af809-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="af809-129">Importera affärsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="af809-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="af809-130">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="af809-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="af809-131">Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="af809-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
