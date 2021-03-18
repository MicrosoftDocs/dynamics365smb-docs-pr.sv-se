---
title: Skapa rapporter i Power BI Desktop för att visa Business Central-data | Microsoft Docs
description: Gör din data tillgänglig som datakälla i Power BI och bygga kraftfulla rapporter av din verksamhets status.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 7226a8b8c1acd624890cd668cd9a8437e7bd08b7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384180"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)]-data

Gör din [!INCLUDE[prod_long](includes/prod_long.md)]-data tillgänglig som datakälla i Power BI Desktop och bygga kraftfulla rapporter av din verksamhets status.

I den här artikeln beskrivs hur du kommer gång med att använda Power BI Desktop för att skapa rapporter som visar [!INCLUDE[prod_long](includes/prod_long.md)]-data.  När du har skapat en rapport kan du publicera den i din Power BI-tjänst eller dela den med samtliga användare i din organisation. När rapporten väl har publicerats i Power BI-tjänsten kan användare som konfigurerats för det se rapporten i [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Gör dig redo

- Registrera dig frö Power BI-tjänsten.

    Gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com) om du inte redan har registrerat dig. När du registrerar dig använder du din e-postadress för arbetet samt ditt lösenord.

- Hämta [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop är ett kostnadsfritt program som du installerar lokalt på din dator. Mer information finns i [snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Se till att den data du vill inkludera i rapporten publiceras som en webbtjänst.
    
    Många webbtjänster publiceras som standard. Ett enkelt sätt att hitta webbtjänsten är att söka efter *webbtjänster* i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Webbtjänster** ser du till att fältet **Publicera** har valts. Denna uppgift utförs vanligtvis av en administratör.
    
    Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

- För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt hämtar du följande information:

    - OData-URL för [!INCLUDE[prod_short](includes/prod_short.md)]. Denna URL har vanligtvis formatet `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, till exempel `https://localhost:7048/BC160/ODataV4`. Om du har en distribution med flera klientorganisationer bör du inkludera klientorganisationen i URL:en, till exempel `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Att användarnamn och en åtkomstnyckel till en webbtjänst tillhörande ett [!INCLUDE[prod_short](includes/prod_short.md)]-konto.

      I syfte att hämta data från [!INCLUDE[prod_short](includes/prod_short.md)] använder Power BI grundläggande autentisering. Du behöver därför ett användarnamn och en åtkomstnyckel till en webbtjänst för att ansluta. Kontot kan vara ditt eget användarkonto, eller också kanske din organisation har ett specifikt konto i detta syfte.

- Ladda ned [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemat (valfritt).

    Mer information finns i [Använda [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemat](#theme) i denna artikel.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a>Lägg till [!INCLUDE[prod_short](includes/prod_short.md)] som n datakälla i Power BI Desktop

Den första uppgiften i samband med att skapa rapporter är att lägga till [!INCLUDE[prod_short](includes/prod_short.md)] som en datakälla i Power BI Desktop. När du väl är ansluten kan du börja skapa rapporten.

1. Starta Power BI Desktop.
2. Välj **Hämta data**.

    Om du inte ser **Hämta data** väljer du menyn **Arkiv** och sedan **Hämta data**.
2. På sidan **Hämta data** väljer du **Onlinetjänster**.
3. I fönstret **Onlinetjänster** utför du ett av följande steg:

    1. Om du vill ansluta till [!INCLUDE [prod_short](includes/prod_short.md)] online väljer du **Dynamics 365 Business Central** och sedan **Anslut**.
    2. Om du ansluter till [!INCLUDE [prod_short](includes/prod_short.md)] lokalt väljer du **Dynamics 365 Business Central (lokalt)** och sedan **Anslut**.

4. Power BI isar en guide som vägleder dig genom anslutningsprocessen, inklusive hur du loggar in på [!INCLUDE [prod_short](includes/prod_short.md)].

    För online väljer du **Logga in** och sedan tillhörande konto. Använd samma konto som du använder för att logga in på [!INCLUDE [prod_short](includes/prod_short.md)].
    
    För lokala varianter anger du OData-URL:en för [!INCLUDE[prod_short](includes/prod_short.md)] och företagsnamnet (valfritt). Därefter anger du (på uppmaning) användarnamn och lösenord för det konto som ska användas för att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)]. I rutan **Lösenord** anger du åtkomstnyckeln för webbtjänsten.

    > [!NOTE]  
    > När du väl har anslutit till [!INCLUDE[prod_short](includes/prod_short.md)] kommer du inte uppmanas att logga in en gång till.
    
5. Välj **Anslut** för att fortsätta.

    Power BI-guiden visar en lista över Microsoft [!INCLUDE[prod_short](includes/prod_short.md)]-miljöer, -företag och -datakällor. Dessa datakällor representerar samtliga de webbtjänster som du har publicerat från [!INCLUDE [prod_short](includes/prod_short.md)].
6. Ange de data som du vill lägga till i din datamodell och välj knappen **Läs in**.
7. Upprepa stegen för att lägga till ytterligare [!INCLUDE [prod_short](includes/prod_short.md)] eller andra data till Power BI-datamodellen.

När datan har lästs in kan du se den i den högra navigeringen på sidan. Vid denna tidpunkt har du anslutit till dina [!INCLUDE[prod_short](includes/prod_short.md)]-data och kan börja skapa din Power BI-rapport.  

> [!TIP]
> Mer information om hur du använder Power BI Desktop finns i [Komma igång med Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Skapa rapporter för att visa data kopplade till en lista

Du kan skapa rapporter som visas i en FactBox tillhörande en [!INCLUDE [prod_short](includes/prod_short.md)]-listsida. Rapporterna kan innehålla data om den post som har valts i listan. Du skapar dessa rapporter på i princip samma sätt som du skapar andra rapporter, förutom att det finns några saker som du måste göra för att rapporten ska visas på avsett sätt. Mer information finns i [Skapa Power BI-rapporter som ska visa listdata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Använda [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemat (tillval)

Innan du skapar din rapport rekommenderar vi att du laddar ned samt importerar [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen. Temafilen skapar en färgpalett så att du kan skapa rapporter med samma färgdesign som [!INCLUDE [prod_short](includes/prod_short.md)]-apparna utan att du behöver ange färger för respektive grafik.

> [!NOTE]
> Denna uppgift är valfri. Du kan alltid skapa dina rapporter och sedan ladda ned och tillämpa designmallen senare.

### <a name="download-the-theme"></a>Hämta temat

Temafilen finns som json-fil i temagalleriet för Microsoft Power BI Community. Utför följande steg för att ladda ned temafilen:

1. Gå till [Temagalleriet för Microsoft Power BI Community för Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Välj nedladdningsbilagan **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Importera temat i en rapport

När du har laddat ned [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemat kan du importera det i din rapport. Om du vill importera schemat väljer du **Visa** > **Teman** > **Bläddra efter scheman**. Mer information finns i [Power BI Desktop – Importera anpassade rapportscheman](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Publicera rapporter

När du har skapat eller ändrat en rapport kan du publicera rapporten i din Power BI-tjänst samt dela den med andra i din organisation. När rapporten har publicerats kan du se den i Power BI. Rapporten görs också tillgänglig för val i [!INCLUDE[prod_short](includes/prod_short.md)].

Om du vill publicera en rapport väljer du **Publicera** i fliken **Start** i menyfliksområdet eller i menyn **Arkiv**. Om du har loggat in på Power BI-tjänsten publiceras rapporten i denna tjänst. I annat fall uppmanas du att logga in. 

## <a name="distribute-or-share-a-report"></a>Distribuera eller dela en rapport

Det finns ett antal olika sätt att skicka rapporter till dina medarbetare och andra:

- Distribuera rapporter som .pbix-filer.

    Rapporter lagras som .pbix-filer på din dator. Du kan distribuera .pbix-rapportfilen till användarna precis som vilken fil som helst. Därefter kan användarna ladda upp filen till sin Power BI-tjänst. Se [Ladda upp rapporter från filer](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Att distribuera rapporter på detta sätt innebär att datauppdateringen för rapporter utförs individuellt av respektive användare. Denna situation kan komma att påverka [!INCLUDE[prod_short](includes/prod_short.md)]-prestandan.

- Dela rapport från din Power BI-tjänst

    Om du har en Power BI Pro-licens kan du dela rapporten med andra direkt från din Power BI-tjänst. Mer information finns i [Power BI – Dela en instrumentpanel eller rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Aktivera dina affärsdata för Power BI](admin-powerbi.md)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomi](finance.md)  
[Snabbstart: Ansluta till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]