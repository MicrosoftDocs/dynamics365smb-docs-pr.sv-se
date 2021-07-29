---
title: Aktivera Power BI-integrering med Business Central
description: Lär dig hur du konfigurerar anslutningen till Power BI. Med Power BI-raporter kan du hämta insikter, Business Intelligence och KPI:er från dina Business Central-data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a9d8479ad1caddef3ac640ba49a8fe101f96a375
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440705"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Aktivera Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)]

I denna artikel beskrivs hur du gör [!INCLUDE[prod_short](includes/prod_short.md)] redo för integrering med Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online är redan färdigkonfigurerat för integrering – dock finns viss licensinformation som du bör läsa igenom. För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du konfigurera din miljö för anslutning till Power BI innan användarna kan använda det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-licenser

Med [!INCLUDE[prod_short](includes/prod_short.md)] får användarna en gratis Power BI-licens som ger åtkomst till de vanligaste funktionerna i [!INCLUDE[prod_short](includes/prod_short.md)] och Power BI. Du kan även köpa en Power BI Pro-licens som ger åtkomst till ytterligare funktioner. Följande tabell sammanfattar de funktioner som medföljer respektive licens.

|Power-licens|Visa rapporter|Skapa rapporter|Dela rapporter|Uppdatera rapporter| [!INCLUDE[prod_short](includes/prod_short.md)]-appar|
|-------------|--------||
|Power BI kostnadsfritt|![en bock.](media/check.png)|![en bock till](media/check.png)|(begränsat)|(begränsat)||
|Power BI Pro|![ytterligare en bock.](media/check.png)|![det är en bock](media/check.png)|![återigen en bock](media/check.png)|(utökat)|![sista bocken](media/check.png)|

mer information finns i [Licensiera Power BI-tjänsten för användare i din organisation](/power-bi/admin/service-admin-licensing-organization) eller [Registrera dig för Power BI-tjänsten som privatperson](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-pages-or-odata-web-services"></a><a name="exposedata"></a>Visa data via API-sidor eller OData-webbtjänster

Med Business Central finns det två sätt att visa data som kan konsumeras av Power BI-rapporter: API-sidor och OData-webbtjänster (Open Data Protocol).

### <a name="api-pages"></a>API-sidor

> **GÄLLER:** endast Business Central online 

En API-sida är en specifik sidtyp som skapats i AL-kod som ger åtkomst till databastabeller via en REST-tjänst som stöds av webhook, OData v4-aktiverad. Den här typen av sida kan inte visas i användargränssnittet, men är avsedd att bygga pålitliga integreringstjänster.

Business Central online finns med en uppsättning inbyggda API:er som du kan använda för att hämta data för de vanligaste affärsentiteterna, till exempel kunder, artiklar, försäljningsorder med mera. Det krävs inga extra arbete eller inställningar för att använda dessa API:er som data källa för Power BI-rapporter. Mer information om dessa API:er finns i [Business Central API v 2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online stöder också anpassade API:er. Program utvecklare av Business Central-lösningar kan skapa egna API-sidor och paketera dem i tillägg. Du kan installera tilläggen på klientorganisationen. När du har installerat kan du använda API-sidorna för dina Power BI-rapporter, som du gör med de inbyggda API:erna (v 2.0). Mer information om hur du skapar API-sidor finns i [utveckla en anpassad API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

### <a name="odata-web-services"></a>OData-webbtjänst

Du kan publicera Business Central-appobjekt, till exempel kodmoduler, sidor och frågor, som [OData-webbtjänster](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Med Business Central online finns många webbtjänster som standard publicerade. Ett enkelt sätt att hitta webbtjänsterna är att söka efter *webbtjänster* i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Webbtjänster** ser du till att fältet **Publicera** har valts för de webbtjänster som anges ovan. Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

Om du vill få veta mer om vad du kan göra för att säkerställa en maximal webbtjänstprestanda – ur ett Business Central server-perspektiv (slutpunkten) samt ur ett konsumentperspektiv (klienten), läs då [Skapa effektiva webbtjänster](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Välja om API-sidor eller OData-webbtjänster ska användas

När det är möjligt rekommenderas du att använda API-sidor i stället för OData-webbtjänster. API-sidor är oftast snabbare när data läses in i Power BI-rapporter än OData-webbtjänster. Dessutom är de mer flexibla eftersom de gör att du kan hämta data från tabellfält som inte är definierade i ett sidobjekt.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för Power BI-integrering

I detta avsnitt beskrivs kraven för en lokal [!INCLUDE[prod_short](includes/prod_short.md)]-distribution i syfte att integrera med Power BI.

1. Konfigurera antingen NavUserPassword- eller Azure Active Directory-autentisering för distributionen.

    Power BI-integrering stöder inte Windows-autentisering.  

2. Aktivera OData-webbtjänster och ODataV4-slutpunkten.

    OData-webtjänsten måste vara aktiverad på [!INCLUDE[server](includes/server.md)] och OData-porten öppen i brandväggen. Mer information finns i [Konfigurera Business Central Server – OData-webbtjänster](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Den lokala servern måste kunna nås via Internet.

3. Ge [!INCLUDE[prod_short](includes/prod_short.md)]-användarkonton en åtkomstnyckel till webbtjänster.

    En åtkomstnyckel för webbtjänst krävs endast för att visa [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI. Du kan tilldela en åtkomstnyckel för webbtjänst till respektive användarkonto. Alternativt kan du skapa ett specifikt konto med en åtkomstnyckel för webbtjänst som samtliga användare kan använda. Mer information finns i [Autentisering för webbtjänster](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](../upgrade/deprecated-features-w1.md#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Using OAuth to Authorize Business Central Web Services](../webservices/authenticate-web-services-using-oauth.md).-->

4. Skapa en kopplingsregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure.

    Om du vill visa Power BI-rapporter på [!INCLUDE[prod_short](includes/prod_short.md)]-sidor måste ett program registreras för [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure Det registrerade programmet behöver behörighet till Power BI-tjänster. Mer information finns i [Registrera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt i Azure AD för integrering med andra tjänster](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Om din distribution använder NavUserPassword-autentisering kommer [!INCLUDE[prod_short](includes/prod_short.md)] att ansluta till samma Power BI-tjänst för samtliga användare. Du ange detta tjänstekonto som ett led i att registrera programmet. Med Azure AD-autentisering kan [!INCLUDE[prod_short](includes/prod_short.md)] ansluta till den Power BI-tjänst som är kopplad till de enskilda användarkontona.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Skapa den första anslutningen från Business Central till Power BI.

    Innan slutanvändare kan använda Power BI i [!INCLUDE[prod_short](includes/prod_short.md)] måste en Azure-programadministratör ge sitt samtycke till Power BI-tjänsten.

    Om du vill skapa den första anslutningen öppnar du [!INCLUDE[prod_short](includes/prod_short.md)] och kör **Kom igång med Power BI** från rollcentret. Denna åtgärd leder dig genom samtyckesprocessen och kontrollerar din Power BI-licens. När du uppmanas att göra så, loggar du in med ett Azure-administratörskonto. Mer information finns i [Anslut till Power BI - endast en gång](across-working-with-powerbi.md#connect).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Business Central och Power BI](admin-powerbi.md)  
[Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]