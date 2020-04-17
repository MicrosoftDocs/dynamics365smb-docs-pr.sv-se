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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187898"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Använda [!INCLUDE [prodlong](includes/prodlong.md)] som Power BI-datakälla för att skapa rapporter

Gör din [!INCLUDE[prodlong](includes/prodlong.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.  

Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power BI. Du måste även ladda ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Mer information finns i [snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power BI Desktop.

1. I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.
2. I fönstret **Hämta data** väljer du **onlinetjänster**, väljer **Microsoft Dynamics 365 Business Central** och sedan knappen **Anslut**.
3. Power BI isar en guide som vägleder dig genom anslutningsprocessen, inklusive hur du loggar in på [!INCLUDE [prodshort](includes/prodshort.md)]. Välj **Logga in** och välj sedan det aktuella kontot. Använd samma konto som du loggar in i [!INCLUDE [prodshort](includes/prodshort.md)] med.
4. Välj knappen **Anslut** för att fortsätta. Power BI-guiden visar en lista över Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljöer, -företag och -datakällor. Dessa datakällor motsvarar samtliga de webbtjänster som du har publicerat från [!INCLUDE [prodshort](includes/prodshort.md)].

    Du kan också skapa en ny URL för webbtjänst i [!INCLUDE [prodshort](includes/prodshort.md)] istället. Välj någon av följande metoder:

      - Använd åtgärden **Skapa datauppsättning** på sidan **Webbtjänster**
      - Använd den assisterade konfigurationsguiden **Ställa in rapportering**
      - Välj åtgärden **Redigera i Excel** i alla listor

5. Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.
6. Upprepa stegen för att lägga till ytterligare [!INCLUDE [prodshort](includes/prodshort.md)] eller andra data till Power BI-datamodellen.

> [!NOTE]  
> När du har anslutit till [!INCLUDE [prodshort](includes/prodshort.md)] kommer du inte att uppmanas att logga in på nytt.

När datan har lästs in kan du se den i den högra navigeringen på sidan. Du har nu lyckats ansluta till dina [!INCLUDE [prodshort](includes/prodshort.md)]-data, och du kan nu börja skapa din Power BI-rapport.  

Innan du skapar rapporten bör du importera [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen.  Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färger som [!INCLUDE [prodshort](includes/prodshort.md)]-appar utan att behöva definiera anpassade färger för varje bild.

Mer information finns i [Power BI dokumentation](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Aktivera affärsdata för Power BI](admin-powerbi.md)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
[Snabbstart: Ansluta till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
