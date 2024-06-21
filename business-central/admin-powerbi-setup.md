---
title: Aktivera Power BI-integrering med Business Central
description: 'Lär dig hur du konfigurerar anslutningen till Power BI. Med Power BI-raporter kan du hämta insikter, Business Intelligence och KPI:er från dina Business Central-data.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/28/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
---
# <a name="enabling-power-bi-integration-with-"></a>Aktivera Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I denna artikel beskrivs hur du gör [!INCLUDE[prod_short](includes/prod_short.md)] redo för integrering med Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online är redan färdigkonfigurerat för integrering – dock finns viss licensinformation som du bör läsa igenom. För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du konfigurera din miljö för anslutning till Power BI innan användarna kan använda det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-licenser

Med [!INCLUDE[prod_short](includes/prod_short.md)] får användarna en gratis Power BI-licens som ger åtkomst till de vanligaste funktionerna i [!INCLUDE[prod_short](includes/prod_short.md)] och Power BI. Du kan även köpa en Power BI Pro-licens som ger åtkomst till ytterligare funktioner. Följande tabell sammanfattar de funktioner som medföljer respektive licens.

|Power-licens|Visa rapporter|Skapa rapporter|Dela rapporter|Uppdatera rapporter| [!INCLUDE[prod_short](includes/prod_short.md)]-appar|
|-------------|--------||
|Power BI kostnadsfritt|![en bock.](media/check.png)|![en bock till](media/check.png)|(begränsat)|(begränsat)||
|Power BI Pro|![ytterligare en bock.](media/check.png)|![det är en bock](media/check.png)|![återigen en bock](media/check.png)|(utökat)|![sista bocken](media/check.png)|

mer information finns i [Licensiera Power BI-tjänsten för användare i din organisation](/power-bi/admin/service-admin-licensing-organization) eller [Registrera dig för Power BI-tjänsten som privatperson](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-or-odata-web-services"></a><a name="exposedata"></a>Visa data via API eller OData-webbtjänster

Med Business Central finns det två sätt att visa data som kan konsumeras av Power BI-rapporter: API-sidor eller frågor och OData-webbtjänster (Open Data Protocol).

### <a name="api-pages-and-queries"></a>API-sidor och frågor

> **GÄLLER:** endast Business Central online

Utvecklare kan definiera sidobjekt och frågeord som är av typen *API*. På så sätt kan de Visa data från databastabeller via en webhook-stödd, REST-tjänst med OData v4. Den här typen av data kan inte visas i användargränssnittet, men är avsedd att bygga pålitliga integreringstjänster.

Business Central online finns med en uppsättning inbyggda API:er som du kan använda för att hämta data för de vanligaste affärsentiteterna, till exempel kunder, artiklar, försäljningsorder med mera. Det krävs inga extra arbete eller inställningar för att använda dessa API:er som data källa för Power BI-rapporter. Mer information om dessa API:er finns i [Business Central API v 2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online stöder också anpassade API:er. Program utvecklare av Business Central-lösningar kan skapa egna API-sidor och frågor och paketera dem i appar. Du installerar sedan appar på klientorganisationen. När du har installerat använder du API-sidorna för dina Power BI-rapporter, som du gör med de inbyggda API:erna (v 2.0). Mer information om hur du skapa ett API genom att exponera sidor eller frågor, se [utveckla en anpassad API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Från och med februari 2022 hämtas Power BI-rapporter för [!INCLUDE[prod_short](includes/prod_short.md)] online från en sekundär, skrivskyddad databaskopia av prestandaskäl. Som en följd av detta bör inte AL-utvecklare utforma API-sidor som gör databasändringar medan sidorna öppnar eller läser in poster. Överväg i synnerhet koden för AL-utlösare: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord och OnAfterGetCurrRecord. Dessa databasändringar kan i vissa fall orsaka prestandaproblem och förhindra att rapporten uppdaterar data. Mer information finns i [Prestandaartiklar för utvecklare](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) i innehållet för Business Central-utveckling.
>
> I sällsynta fall orsakar beteendet ett fel när en användare försöker hämta data från API för en rapport i Power BI Desktop. Om databasändringar krävs på den anpassade API kan Power BI Desktop-användare tvinga fram beteendet. Mer information finns i [Skapa Power BI-rapporter för att visa Business Central-data](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>OData-webbtjänst

Du kan publicera Business Central-appobjekt, till exempel kodmoduler, sidor och frågor, som [OData-webbtjänster](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Med Business Central online finns många webbtjänster som standard publicerade. Ett enkelt sätt att hitta webbtjänsterna är att söka efter *webbtjänster* i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Webbtjänster** ser du till att fältet **Publicera** har valts för de webbtjänster som anges ovan. Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

Om du vill få veta mer om vad du kan göra för att säkerställa en maximal webbtjänstprestanda – ur ett Business Central server-perspektiv (slutpunkten) samt ur ett konsumentperspektiv (klienten), läs då [Skapa effektiva webbtjänster](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Välja om API-sidor eller OData-webbtjänster ska användas

När det är möjligt rekommenderas du att använda API-sidor i stället för OData-webbtjänster. API-sidor är snabbare när data läses in i Power BI-rapporter än OData-webbtjänster. Dessutom är de mer flexibla eftersom de gör att du kan hämta data från tabellfält som inte är definierade i ett sidobjekt.

<!--## <a name="setup"></a>Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration

This section explains the requirements for a [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment to integrate with Power BI.

1. Configure either [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) or [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) as the authentication method for the deployment.  
    
    > [!NOTE]
    > Power BI integration doesn't support Windows authentication and is not supported on Windows Client.

2. Enable OData web services and the ODataV4 endpoint.

    OData web service must be enabled on the [!INCLUDE[server](includes/server.md)], and OData port opened in firewall. For more information, see [Configuring Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    The local server must be accessible from the Internet.

3. Give [!INCLUDE[prod_short](includes/prod_short.md)] user accounts a web service access key.

    A web service access key is only needed to view [!INCLUDE[prod_short](includes/prod_short.md)] data in Power BI. You can assign a web service access key to each user account. Or instead, create a specific account with a web service access key for use by all users. For more information, see [Web Services Authentication](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

<!--4. Create an application registration for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    To view Power BI reports embedded in [!INCLUDE[prod_short](includes/prod_short.md)] pages, an application must be registered for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. The registered application needs permission to Power BI services. At a minimum, the app requires  **User.ReadWrite.All** permission. For users to view reports from shared Power BI workspaces, the app requires **Workspace.Read.All** permission. For more information, see [Registering [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Microsoft Entra ID for Integrating with Other Services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > If your deployment uses NavUserPassword authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the same Power BI service for all users. You'll specify this service account as part of registering the application. With Microsoft Entra authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the Power BI service associated with the individual user accounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
<!--5. Make the initial connection from Business Central to Power BI.

    Before end-users can use Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], an Azure application administrator will have to give consent to the Power BI service.

    To make the initial connection, open [!INCLUDE[prod_short](includes/prod_short.md)], and run **Get Started with Power BI** from the Home page. This action will lead you through the consent process, and check your Power BI license. When prompted sign in using an Microsoft Entra admin account. For more information, see [Connect to Power BI - one time only](across-working-with-powerbi.md#connect).-->

## <a name="setting-up-dataflows"></a>Konfigurera dataflöden

Med dataflöden kan du mata in, transformera och läsa in data till en Power BI arbetsyta och sedan använda data som grund för dina rapporter. Dessa dataflöden kan i vissa fall uppleva tillfälliga fel när du gör en schemalagd uppdatering. Felmeddelandet ser ut så här: `DataSource.Error: OData: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.` 

Med PowerAutomate kan du konfigurera nya försök för den här situationen. Mer information finns i [Försök automatiskt igen med ett dataflöde vid fel](/power-query/dataflows/automatically-retry-dataflow).

## <a name="see-also"></a>Se även

[Business Central och Power BI](admin-powerbi.md)  
[Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
