---
title: Introduktion till Business Central och Power BI
description: Få en användningsöversikt för Power BI i syfte att få insikter, business intelligence och KPI:er från dina Business Central-data.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.search.form: 6316, 6317
ms.reviewer: edupont
ms.date: 08/30/2022
ms.author: jswymer
ms.openlocfilehash: 0742320b4cb334b3c01c86ec0e10ec82114bd215
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460737"
---
# <a name="introduction-to-prod_short-and-power-bi"></a>Introduktion till [!INCLUDE[prod_short](includes/prod_short.md)] och Power BI

Det är enkelt att få insikter i dina [!INCLUDE[prod_short](includes/prod_short.md)]-data är enkelt med [Power BI](https://powerbi.microsoft.com) – ett system för datavisualisering från Microsoft. Power BI hämtar [!INCLUDE[prod_short](includes/prod_short.md)]-data som gör det möjligt för dig att skapa instrumentpaneler och rapporter baserade på denna data. Power BIutgör ett flexibelt alternativ till rapporter som skapas med [!INCLUDE[prod_short](includes/prod_short.md)] genom att göra det möjligt för dig att öka detaljnivån i och anpassa visualiseringen, samt till och med att sammanslå data från olika företag i [!INCLUDE[prod_short](includes/prod_short.md)]. Vissa Power BI-rapporter kan också bäddas in i Business Central och visas utan att du behöver lämna systemet. Upplevelsen av mer komplexa instrumentpaneler blir bättre från Power BI-webbplatsen.

![Power BI och Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Vad kan du göra med Power BI och [!INCLUDE[prod_short](includes/prod_short.md)]

Det finns olika funktioner för att arbeta med [!INCLUDE[prod_short](includes/prod_short.md)] och Power BI. Vissa saker kan du göra från Power BI, medan andra saker görs via [!INCLUDE[prod_short](includes/prod_short.md)]. Vissa funktioner är dessutom endast tillgängliga med [!INCLUDE[prod_short](includes/prod_short.md)] online, inte lokalt. Följande tabell ger dig en översikt.

|Funktion|Description|Online|Lokalt|Läs mer|
|-------|-----------|--------------|-----------|----------------|
|Visa [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI|Du kan visa dina [!INCLUDE[prod_short](includes/prod_short.md)]-data i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online omfattar vissa fördefinierade Power BI-rapporter. Det kan också vara så att din organisation har gjort vissa anpassade rapporter tillgängliga för dig.|![Arbetar online.](media/check.png)|![Arbetar på plats](media/check.png)|[Här...](across-working-with-business-central-in-powerbi.md)|
|Visa Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter som visar [!INCLUDE[prod_short](includes/prod_short.md)]-data kan bäddas in direkt i delar på [!INCLUDE[prod_short](includes/prod_short.md)]-sidor. Du kan låta delen visa valfri rapport som gjorts tillgänglig för dig. |![arbetar online.](media/check.png)|![Arbetar på plats](media/check.png)<sup>[*](#onprem)</sup>|[Här...](across-working-with-powerbi.md).|
|Skapa rapporter och instrumentpaneler i Power BI som visar [!INCLUDE[prod_short](includes/prod_short.md)]-data.|Använd Power BI Desktop för att skapa dina egna rapporter och instrumentpaneler. Du kan publicera rapporterna i din egen Power BI-tjänst eller dela dem med andra inom din organisation.|![Arbetar online.](media/check.png)|![arbetar på plats](media/check.png)|[Här...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)]-appar i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publicerar tre appar för Power BI i Microsoft AppSource. Dessa appar framställer detaljerade rapporter och instrumentpaneler i din Power BI-tjänst som låter dig visa [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tillgängliga appar inkluderar bland annat: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Arbetar online.](media/check.png)||[Här...](across-powerbi-business-central-apps.md)|
|Arbeta med [!INCLUDE [prod_short](includes/prod_short.md)] data i dataförråd och dataflöden|Från och med den 2022 juli kan du använda [!INCLUDE [prod_short](includes/prod_short.md)] kopplingen i Power Query online för dataflöden du delar över olika rapporter och instrumentpaneler.|[Här...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Denna funktion kräver ett registrerat program för Business Central i Microsoft Azure. Mer information finns i [Registrera Business Central lokalt i Azure AD för integrering med andra tjänster](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="get-ready-to-use-power-bi"></a>Komma igång med Power BI

Det finns några uppgifter som måste utföras innan du kan börja använda Power BI med [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> Uppgifterna beror på din roll i organisationen och vad du vill göra med Power BI:

- Som *företagsanvändare* vill du visa Power BI-rapporter, antingen i Power BI-tjänsten eller Business Central
- Som *administratör* ansvarar du för hanteringen av de organisationsomfattande inställningarna som styr hur Business Central och Power BI fungerar.
- Som *rapportskapare* vill du skapa anpassade Power BI-rapporter som du kan dela med andra användare.

|Uppgift|Affärsanvändare|Administratör|Skapare av rapporter|Mer information|
|----|-------------|-------------|-----------------------|----------------|
|Skaffa ett Power BI-konto.|![ytterligare en bock.](media/check.png)|![det är en bock](media/check.png)|![återigen en bock](media/check.png)|Gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Se till att använda din e-postadress för arbetet samt ditt lösenord när du registrerar dig för ett konto. <br /><br/>En registrering kräver en licens, men i de flesta fall för du redan ha en gratislicens. För mer information, se [Power BI-licensiering](admin-powerbi-setup.md#license).|
|Hämta Power BI Desktop|||![återigen en bock.](media/check.png)|Om du vill ladda ned går du till [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Mer information finns i [Hämta Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Exponera Business Central-data för Power BI||![det är en bock.](media/check.png)|![återigen en bock](media/check.png)|[Visa data via API-sidor eller OData-webbtjänster](admin-powerbi-setup.md#exposedata)
|Aktivera integrering med Power BI<br />(endast lokalt)||![det är en bock.](media/check.png)||[Konfigurera Business Central lokalt för Power BI-integration](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Affärsstöd](bi.md)  
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  
[Dokumentation om Power BI](/power-bi/)  
[Vad är Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Introduktion till dataförråd](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introduktion till dataflöden och dataförberedelser via självbetjäning](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  



[!INCLUDE[footer-include](includes/footer-banner.md)]