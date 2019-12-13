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
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881006"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av Power Apps

Du kan göra din [!INCLUDE[prodshort](includes/prodshort.md)]-data tillgänglig som underlag för datakälla i Power Apps.  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power Apps.  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a>Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power Apps.

1. I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/), och loggar in.
2. På startsidan, välj **Appar**, **Skapa en app** och **Arbetsyta** för att skapa en ny arbetsyteapp. Det här programmet kommer att vara konstruerat för användning på en mobil enhet, men du kan även välja att använda en annan mall.

    Nästa steg för att skapa en Power App är att välja data. Välj pilikonen och välj sedan alternativet **ny anslutning** i det övre vänstra delen på sidan.
3. Välj **Business Central** i listan över tillgängliga anslutningar och välj sedan knappen **skapa**.

    Power Apps kommer att ansluta till [!INCLUDE [prodshort](includes/prodshort.md)] dina med hjälp av autentiseringsuppgifterna som du har loggat in med. Om du inte är administratör för ditt [!INCLUDE [prodshort](includes/prodshort.md)] måste du kanske logga in med ett annat konto.  

4. Power Apps visar en lista över *Miljöer och företag* som finns på [!INCLUDE [prodshort](includes/prodshort.md)]. Välj den miljö och det företag som innehåller de data som du vill ansluta till. Sedan visas en lista med API:er. Markera den **API** som du vill ansluta till.

De s.k. tabellerna är en del av [!INCLUDE [prodshort](includes/prodshort.md)] API. Du behöver inte konfigurera slutpunkterna själv, [!INCLUDE [prodshort](includes/prodshort.md)]-kopplingen för Power Apps gör det åt dig.  

> [!NOTE]
> Om du vill ta med data från andra tabeller i [!INCLUDE [prodshort](includes/prodshort.md)]-appen måste du arbeta med en utvecklare för att definiera en anpassad API i [!INCLUDE [prodshort](includes/prodshort.md)] och sedan använda denna anpassade API via en anpassad anslutning i Power Apps. Mer information finns i [skapa en egen anslutning från början.](/connectors/custom-connectors/define-blank)  

Nu har du lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data och är redo att börja skapa din Power BI. Du kan lägga till ytterligare skärmar och ansluta till ytterligare data från [!INCLUDE [prodshort](includes/prodshort.md)]. Mer information finns i [Skapa en arbetsyteapp från en mall i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  

När du har skapat och byggt ditt program kan du dela den med dina kollegor. Mer information finns i [Spara och publicera en arbetsyteapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Om du vill ansluta till [!INCLUDE [prodshort](includes/prodshort.md)] lokalt måste du välja anslutningen **Business Central (lokal)** i steg 3.  

## <a name="see-also"></a>Se även

[Skapa en arbetsyteapp från en mall i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
[Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
