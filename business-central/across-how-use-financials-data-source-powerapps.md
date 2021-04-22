---
title: Använda din adata för att skapa en app | Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa en företagsapp med Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 25607473e20bca8cec8cd65e2e808e12dda47869
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774542"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="a22ef-103">Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av Power Apps</span><span class="sxs-lookup"><span data-stu-id="a22ef-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="a22ef-104">Du kan göra din [!INCLUDE[prod_short](includes/prod_short.md)]-data tillgänglig som underlag för datakälla i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a22ef-104">You can make your [!INCLUDE[prod_short](includes/prod_short.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="a22ef-105">Du måste ha ett giltigt konto med [!INCLUDE[prod_short](includes/prod_short.md)] och med Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a22ef-105">You must have a valid account with [!INCLUDE[prod_short](includes/prod_short.md)] and with Power Apps.</span></span>  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a><span data-ttu-id="a22ef-106">Att lägga till [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a22ef-106">To add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="a22ef-107">I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/), och loggar in.</span><span class="sxs-lookup"><span data-stu-id="a22ef-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="a22ef-108">På startsidan, i avsnittet **Starta från data** välj panelen **Andra datakällor**.</span><span class="sxs-lookup"><span data-stu-id="a22ef-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="a22ef-109">Då öppnas Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="a22ef-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="a22ef-110">Vid första inloggningen måste du ange land/region.</span><span class="sxs-lookup"><span data-stu-id="a22ef-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="a22ef-111">Välj **Business Central** i listan över tillgängliga anslutningar och välj sedan knappen **skapa**.</span><span class="sxs-lookup"><span data-stu-id="a22ef-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="a22ef-112">Power Apps kommer att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av autentiseringsuppgifterna som du har loggat in med.</span><span class="sxs-lookup"><span data-stu-id="a22ef-112">Power Apps will connect to your [!INCLUDE[prod_short](includes/prod_short.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="a22ef-113">Om du inte är administratör för ditt [!INCLUDE[prod_short](includes/prod_short.md)] måste du kanske logga in med ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="a22ef-113">If you are not an administrator of your [!INCLUDE[prod_short](includes/prod_short.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="a22ef-114">Power Apps visar en lista över *Miljöer och företag* som finns på [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a22ef-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a22ef-115">Välj den miljö och det företag som innehåller de data som du vill ansluta till t. ex. *PRODUKTION – Mitt företag*.</span><span class="sxs-lookup"><span data-stu-id="a22ef-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="a22ef-116">Sedan visas en lista över tabeller som visas som en del av API för din miljö.</span><span class="sxs-lookup"><span data-stu-id="a22ef-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="a22ef-117">Markera den tabell som du vill ansluta till och välj sedan **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="a22ef-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="a22ef-118">Dessa så kallade tabeller visas som [!INCLUDE[prod_short](includes/prod_short.md)] kopplingen för Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a22ef-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prod_short](includes/prod_short.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="a22ef-119">Om du vill ta med data från andra tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i din app, måste du samarbeta med en utvecklare för att definiera en anpassad API i [!INCLUDE[prod_short](includes/prod_short.md)] och sedan använda denna anpassade API via en anpassad anslutning i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a22ef-119">If you want to include data from other tables in [!INCLUDE[prod_short](includes/prod_short.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prod_short](includes/prod_short.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="a22ef-120">Mer information finns i [skapa en egen anslutning från början.](/connectors/custom-connectors/define-blank)</span><span class="sxs-lookup"><span data-stu-id="a22ef-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="a22ef-121">Nu har du lyckats ansluta till dina [!INCLUDE[prod_short](includes/prod_short.md)]-data och är redo att börja skapa din Power BI.</span><span class="sxs-lookup"><span data-stu-id="a22ef-121">At this point, you have successfully connected to your [!INCLUDE[prod_short](includes/prod_short.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="a22ef-122">Du kan lägga till ytterligare skärmar och ansluta till ytterligare data från [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a22ef-122">You can add additional screens and connect to additional data from your [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a22ef-123">Mer information finns i [Skapa en arbetsyteapp från ett exempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="a22ef-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="a22ef-124">När du har skapat och byggt ditt program kan du dela den med dina kollegor.</span><span class="sxs-lookup"><span data-stu-id="a22ef-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="a22ef-125">Mer information finns i [Spara och publicera en arbetsyteapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="a22ef-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="a22ef-126">Om du vill ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du välja anslutningen **Business Central (lokal)** i steg 3.</span><span class="sxs-lookup"><span data-stu-id="a22ef-126">If you want to connect to [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a22ef-127">Se även</span><span class="sxs-lookup"><span data-stu-id="a22ef-127">See Also</span></span>

[<span data-ttu-id="a22ef-128">Skapa en arbetsyteapp från en mall i Power Apps</span><span class="sxs-lookup"><span data-stu-id="a22ef-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="a22ef-129">Importera affärsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="a22ef-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="a22ef-130">[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="a22ef-130">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="a22ef-131">Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="a22ef-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]