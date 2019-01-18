---
title: "Konfigurera Rapportering för Business Central i Power BI | Microsoft Docs"
description: "Gör din data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ca4c27eaa1fe66e9bee678d6ec197fee7b928bdd
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Använda [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som Power BI-datakälla för att skapa rapporter
Du kan göra din [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.  

Du måste ha ett giltigt konto med [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] och med Power BI. Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Att lägga till [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som datakälla i Power BI Desktop
1. I Power BI Desktop i den vänstra navigeringsrutan väljer du **hämta data**.
2. På sidan **Hämta data** väljer du **Onlinetjänster**, **Microsoft Dynamics 365 Business Central** och sedan knappen **Anslut**.
3. Power BI visar en guide som vägleder dig genom [anslutningsprocessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Du uppmanas då att logga in på tjänsten. Välj **Logga in** och välj det konto som du vill logga in som. Detta bör vara samma konto som du loggar in i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] med.
4. Välj knappen **Anslut** för att fortsätta. Power BI-guiden visar en lista över Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag och -datakällor. Dessa datakällor motsvarar alla de webbtjänster som du har publicerat från respektive företag i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.
6. Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.
7. Upprepa stegen för att lägga till ytterligare Microsof [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] eller andra data till Power BI-datamodellen.

> [!NOTE]  
> När du har anslutit till Microsof [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] kommer du inte att uppmanas att logga in på nytt.

När data har lästs in kommer den att visas i den högra navigeringen på sidan. Du har nu lyckats ansluta till dina Microsof [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data och är redo att börja skapa Power BI-rapporten. 

Innan du skapar rapporten bör du importera Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-temafilen.  Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färger som Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehållspaketen utan att behöva definiera anpassade färger för varje bild.

Mer information finns i [Power BI dokumentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Ekonomi](finance.md)  
[Ansluta Power BI till [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

