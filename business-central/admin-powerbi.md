---
title: Introduktion till Business Central och Power BI| Microsoft Docs
description: Få en användningsöversikt för Power BI i syfte att få insikter, business intelligence och KPI:er från dina Business Central-data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 9768fca2bea274a8124c34e151d399baa23f9f03
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493123"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] och Power BI

Att få insikter i dina [!INCLUDE[prod_short](includes/prod_short.md)]-data är enkelt med [Power BI](https://powerbi.microsoft.com) – ett system för datavisualisering från Microsoft. Power BI hämtar [!INCLUDE[prod_short](includes/prod_short.md)]-data som gör det möjligt för dig att skapa instrumentpaneler och rapporter baserade på denna data. Power BIutgör ett flexibelt alternativ till rapporter som skapas med [!INCLUDE[prod_short](includes/prod_short.md)] genom att göra det möjligt för dig att öka detaljnivån i och anpassa visualiseringen, samt till och med att sammanslå data från olika företag i [!INCLUDE[prod_short](includes/prod_short.md)]. Vissa Power BI-rapporter kan också bäddas in i Business Central och visas utan att du behöver lämna systemet. Upplevelsen av mer komplexa instrumentpaneler blir bättre från Power BI-webbplatsen.

![Power BI och Business Central](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Vad kan du göra med Power BI och [!INCLUDE[prod_short](includes/prod_short.md)]

Det finns olika funktioner för att arbeta med [!INCLUDE[prod_short](includes/prod_short.md)] och Power BI. Vissa saker kan du göra från Power BI, medan andra saker görs via [!INCLUDE[prod_short](includes/prod_short.md)]. Vissa funktioner är dessutom endast tillgängliga med [!INCLUDE[prod_short](includes/prod_short.md)] online, inte lokalt. Följande tabell ger dig en översikt.

|Funktion|Beskrivning|Online|Lokalt|Mer information|
|-------|-----------|--------------|-----------|----------------|
|Visa [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI|Du kan visa dina [!INCLUDE[prod_short](includes/prod_short.md)]-data i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online omfattar vissa fördefinierade Power BI-rapporter. Det kan också vara så att din organisation har gjort vissa anpassade rapporter tillgängliga för dig.|![Arbetar online](media/check.png)|![Arbetar på plats](media/check.png)|[Se...](across-working-with-business-central-in-powerbi.md)|
|Visa Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter som visar [!INCLUDE[prod_short](includes/prod_short.md)]-data kan bäddas in direkt i delar på [!INCLUDE[prod_short](includes/prod_short.md)]-sidor. Du kan låta delen visa valfri rapport som gjorts tillgänglig för dig. |![arbetar online](media/check.png)|![Arbetar på plats](media/check.png)<sup>[*](#onprem)</sup>|[Se...](across-working-with-powerbi.md)|
|Skapa rapporter och instrumentpaneler i Power BI som visar [!INCLUDE[prod_short](includes/prod_short.md)]-data.|Använd Power BI Desktop för att skapa dina egna rapporter och instrumentpaneler. Du kan publicera rapporterna i din egen Power BI-tjänst eller dela dem med andra inom din organisation.|![Arbetar online](media/check.png)|![arbetar på plats](media/check.png)|[Se...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-appar i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publicerar tre appar för Power BI i Microsoft AppSource. Dessa appar framställer detaljerade rapporter och instrumentpaneler i din Power BI-tjänst som låter dig visa [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tillgängliga appar inkluderar bland annat: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Arbetar online](media/check.png)||[Se...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Denna funktion kräver ett registrerat program för Business Central i Microsoft Azure. Mer information finns i [Registrera Business Central lokalt i Azure AD för integrering med andra tjänster](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Komma igång med Power BI

Det finns några uppgifter som måste utföras innan du kan börja använda Power BI med [!INCLUDE[prod_short](includes/prod_short.md)]. Vissa uppgifter utförs som regel endast av administratörer eller så kallade "super users".

1. Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt bör du se till att din distribution uppfyler de krav som anges i [Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för Power BI-integrering](admin-powerbi-setup.md#setup). Denna uppgift utförs vanligtvis av en administratör.

2. Publicera data som webbtjänster.

    Kodenheter, sidor och frågor som du vill använda som datakälla i Power BI-rapporter måste publiceras som webbtjänster. Många webbtjänster publiceras som standard. Ett enkelt sätt att hitta webbtjänsten är att söka efter *webbtjänster* i [!INCLUDE[prod_short](includes/prod_short.md)].

    Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

3. Skaffa ett Power BI-konto.

    För att kunna använda Power BI och [!INCLUDE[prod_short](includes/prod_short.md)] på något som helst sätt krävs ett Power BI-tjänstekonto – detta gäller oavsett om du är administratör eller endast konsument. Gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com) för att skaffa ett konto. Se till att använda din e-postadress för arbetet samt ditt lösenord när du registrerar dig för ett konto. En registrering kräver en licens, men i de flesta fall för du redan ha en gratislicens. Mer information finns i [Power BI-licensiering](admin-powerbi-setup.md#license).

4. Om du vill skapa egna Power BI-rapporter skaffar du Power BI Desktop.

    Du kan ladda ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Mer information finns i [Hämta Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Ansluta till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]