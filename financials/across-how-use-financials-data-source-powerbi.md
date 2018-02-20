---
title: Konfigurera rapportering till Finance and Operations, Business edition i Power BI | Microsoft Docs
description: "Du kan göra din Financials-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 056761b398737bd052b68488756198051f0cdb9a
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakälla för att skapa rapporter
Du kan göra din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Power BI. Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Power BI Desktop
1. I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.
2. I fönstret **Hämta data** väljer du **Onlinetjänster**, **Dynamics 365 for Finance and Operations, Business edition** och sedan knappen **Anslut**.
3. Power BI visar en guide som vägleder dig genom [anslutningsprocessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Det första steget är att logga in på tjänsten. Välj **Logga in** och välj det konto som du vill logga in som. Detta bör vara samma konto som du loggar in i [!INCLUDE[d365fin](includes/d365fin_md.md)] med.
4. Välj knappen **Anslut** för att fortsätta. Power BI-guiden visar en lista över [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag och -datakällor. Dessa datakällor motsvarar alla de webbtjänster som du har publicerat från respektive företag i [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **Skapa datauppsättning** på sidan **Webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering** eller genom att välja åtgärden **Redigera i Excel** i valfri lista.
6. Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.
7. Upprepa stegen för att lägga till ytterligare [!INCLUDE[d365fin](includes/d365fin_md.md)]-data till Power BI-datamodellen.

> [!NOTE]  
> När du har anslutit till [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer du inte att uppmanas att logga in på nytt.

När data har lästs in kommer den att visas i den högra navigeringen på sidan. Du har nu lyckats ansluta till dina Finance and Operations, Business edition-data och är redo att börja skapa din Power BI-rapport. Mer information finns i [Power BI dokumentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Ekonomi](finance.md)  
[Ansluta Power BI till [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

