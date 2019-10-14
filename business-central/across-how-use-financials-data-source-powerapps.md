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
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av PowerApps
Du kan göra din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tillgänglig som underlag för datakälla i PowerApps.  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med PowerApps.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i PowerApps.
1. I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), och loggar in.
2. På startsidan, välj **Appar**, **Skapa en app** och **Arbetsyta** för att skapa en ny arbetsyteapp. Det här programmet kommer att vara konstruerat för användning på en mobil enhet, men du kan även välja att använda en annan mall.

    Nästa steg för att skapa en PowerApp är att välja data. Välj pilikonen och välj sedan alternativet **ny anslutning** i det övre vänstra delen på sidan.
3. Välj **Business Central** i listan över tillgängliga anslutningar och välj sedan knappen **skapa**.

    PowerApps kommer att ansluta till [!INCLUDE [prodshort](includes/prodshort.md)] med hjälp av autentiseringsuppgifterna som du har loggat in med. Om du inte är administratör för ditt [!INCLUDE [prodshort](includes/prodshort.md)] måste du kanske logga in med ett annat konto.  

4.  PowerApps visar en lista över *Miljöer och företag* som finns på [!INCLUDE [prodshort](includes/prodshort.md)]. Välj den miljö och det företag som innehåller de data som du vill ansluta till. Sedan visas en lista med API:er. Markera den **API** som du vill ansluta till.

De s.k. tabellerna är en del av [!INCLUDE [prodshort](includes/prodshort.md)] API. Du behöver inte konfigurera slutpunkterna själv, [!INCLUDE [prodshort](includes/prodshort.md)]-kopplingen för PowerApps gör det åt dig.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

Nu har du lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data och är redo att börja skapa din Power BI. Du kan lägga till ytterligare skärmar och ansluta till ytterligare data från [!INCLUDE [prodshort](includes/prodshort.md)]. Mer information finns i [Skapa en arbetsyteapp från en mall i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

När du har skapat och byggt ditt program kan du dela den med dina kollegor. Mer information finns i [Spara och publicera en arbetsyteapp i PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Om du vill ansluta till [!INCLUDE [prodshort](includes/prodshort.md)] lokalt måste du välja anslutningen **Business Central (lokal)** i steg 3.  

## <a name="see-also"></a>Se även

[Skapa en arbetsyteapp från en mall i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
[Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
