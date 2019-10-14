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
ms.openlocfilehash: b57b87dd8cdc9390ed5b1b7136107639f689c192
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305002"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>Använda [!INCLUDE [prodlong](includes/prodlong.md)] som Power BI-datakälla för att skapa rapporter

Gör din [!INCLUDE[prodlong](includes/prodlong.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.  

Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power BI. Dessutom kan du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Mer information finns i [snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power BI Desktop.

1. I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.
2. I fönstret **Hämta data** väljer du **onlinetjänster**, väljer **Microsoft Dynamics 365 Business Central** och sedan knappen **Anslut**.
3. Power BI visar en guide som vägleder dig genom anslutningsprocessen. Du uppmanas då att logga in på [!INCLUDE [prodshort](includes/prodshort.md)]. Välj **Logga in** och välj det konto som du vill logga in som. Detta bör vara samma konto som du loggar in i [!INCLUDE [prodshort](includes/prodshort.md)] med.
4. Välj knappen **Anslut** för att fortsätta. Power BI-guiden visar en lista över Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljöer, -företag och -datakällor. Dessa datakällor motsvarar alla de webbtjänster som du har publicerat från respektive klientorganisation/företag i [!INCLUDE [prodshort](includes/prodshort.md)].
5. Du kan också skapa en ny webbtjänst-URL i [!INCLUDE [prodshort](includes/prodshort.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.
6. Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.
7. Upprepa stegen för att lägga till ytterligare [!INCLUDE [prodshort](includes/prodshort.md)] eller andra data till Power BI-datamodellen.

> [!NOTE]  
> När du har anslutit till [!INCLUDE [prodshort](includes/prodshort.md)] kommer du inte att uppmanas att logga in på nytt.

När data har lästs in kommer den att visas i den högra navigeringen på sidan. Nu har du lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data och är redo att börja skapa Power BI-rapporten.  

Innan du skapar rapporten bör du importera [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen.  Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färger som [!INCLUDE [prodshort](includes/prodshort.md)]-appar utan att behöva definiera anpassade färger för varje bild.

Mer information finns i [Power BI dokumentation](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-also"></a>Se även

[Aktivera affärsdata för Power BI](admin-powerbi.md)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
[Snabbstart: Ansluta till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
