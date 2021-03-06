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
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av Power Apps

Du kan göra din [!INCLUDE[prod_short](includes/prod_short.md)]-data tillgänglig som underlag för datakälla i Power Apps.  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[prod_short](includes/prod_short.md)] och med Power Apps.  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a>Att lägga till [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla i Power Apps.

1. I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/), och loggar in.
2. På startsidan, i avsnittet **Starta från data** välj panelen **Andra datakällor**.  

    Då öppnas Power Apps Studio. Vid första inloggningen måste du ange land/region.  
3. Välj **Business Central** i listan över tillgängliga anslutningar och välj sedan knappen **skapa**.

    Power Apps kommer att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av autentiseringsuppgifterna som du har loggat in med. Om du inte är administratör för ditt [!INCLUDE[prod_short](includes/prod_short.md)] måste du kanske logga in med ett annat konto.  

4. Power Apps visar en lista över *Miljöer och företag* som finns på [!INCLUDE[prod_short](includes/prod_short.md)]. Välj den miljö och det företag som innehåller de data som du vill ansluta till t. ex. *PRODUKTION – Mitt företag*.  

5. Sedan visas en lista över tabeller som visas som en del av API för din miljö. Markera den tabell som du vill ansluta till och välj sedan **Anslut**.

Dessa så kallade tabeller visas som [!INCLUDE[prod_short](includes/prod_short.md)] kopplingen för Power Apps.  

> [!NOTE]
> Om du vill ta med data från andra tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i din app, måste du samarbeta med en utvecklare för att definiera en anpassad API i [!INCLUDE[prod_short](includes/prod_short.md)] och sedan använda denna anpassade API via en anpassad anslutning i Power Apps. Mer information finns i [skapa en egen anslutning från början.](/connectors/custom-connectors/define-blank)  

Nu har du lyckats ansluta till dina [!INCLUDE[prod_short](includes/prod_short.md)]-data och är redo att börja skapa din Power BI. Du kan lägga till ytterligare skärmar och ansluta till ytterligare data från [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Skapa en arbetsyteapp från ett exempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

När du har skapat och byggt ditt program kan du dela den med dina kollegor. Mer information finns i [Spara och publicera en arbetsyteapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Om du vill ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du välja anslutningen **Business Central (lokal)** i steg 3.  

## <a name="see-also"></a>Se även

[Skapa en arbetsyteapp från en mall i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]