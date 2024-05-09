---
title: Anslut till Power BI från Business Central lokalt | Microsoft Docs
description: 'Använda insikter, business intelligence och KPI:er från dina Business Central-data med hjälp av Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Anslut till Power BI från Business Central lokalt

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## Kom i gång

Om du använder [!INCLUDE [prod_short](includes/prod_short.md)] lokalt måste det aktiveras för Power BI-integrering. Denna uppgift utförs vanligtvis av en administratör. Mer information om hur du aktiverar Power BI integrering med Business Central online finns i [Konfigurera Business Central lokalt för Power BI-integrering](admin-powerbi-setup.md).

Vissa funktioner är dessutom endast tillgängliga med Business Central Online, inte lokalt. Mer information finns i [Introduktion till Business Central och Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="setup"></a>Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för Power BI-integrering

I detta avsnitt beskrivs kraven för en lokal [!INCLUDE[prod_short](includes/prod_short.md)]-distribution i syfte att integrera med Power BI.

1. Konfigurera antingen [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) eller [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) som autentiseringsmetod för fördelningen.  
    
    > [!NOTE]
    > Power BI integrationen stöder inte Windows-autentisering och stöds inte på Windows-klienten.

2. Aktivera OData-webbtjänster och ODataV4-slutpunkten.

    OData-webtjänsten måste vara aktiverad på [!INCLUDE[server](includes/server.md)] och OData-porten öppen i brandväggen. Mer information finns i [Konfigurera Business Central Server – OData-webbtjänster](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Den lokala servern måste kunna nås via Internet.

3. Ge [!INCLUDE[prod_short](includes/prod_short.md)]-användarkonton en åtkomstnyckel till webbtjänster.

    En åtkomstnyckel för webbtjänst krävs endast för att visa [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI. Du kan tilldela en åtkomstnyckel för webbtjänst till respektive användarkonto. Alternativt kan du skapa ett specifikt konto med en åtkomstnyckel för webbtjänst som samtliga användare kan använda. Mer information finns i [Autentisering för webbtjänster](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Skapa en kopplingsregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure.

    För att Power BI-rapporter som har bäddats in på [!INCLUDE[prod_short](includes/prod_short.md)]-sidor ska kunna visas måste ett program registreras för [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure. Det registrerade programmet behöver behörighet för Power BI-tjänster. Appen måste åtminstone ha **User.ReadWrite.All** behörighet. För att användarna ska kunna visa rapporter från delade Power BI arbetsytor kräver programmet **Workspace.Read.All** behörighet. Mer information finns i [Registrera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt i Microsoft Entra ID för integrering med andra tjänster](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Om din distribution använder NavUserPassword-autentisering kommer [!INCLUDE[prod_short](includes/prod_short.md)] att ansluta till samma Power BI-tjänst för samtliga användare. Du ange detta tjänstekonto som ett led i att registrera programmet. Med Microsoft Entra-autentisering kan [!INCLUDE[prod_short](includes/prod_short.md)] ansluta till den Power BI-tjänst som är kopplad till de enskilda användarkontona.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Skapa den första anslutningen från Business Central till Power BI.

    Innan slutanvändare kan använda Power BI i [!INCLUDE[prod_short](includes/prod_short.md)] måste en Azure-programadministratör ge sitt samtycke till Power BI-tjänsten.

    Om du vill skapa den första anslutningen öppnar du [!INCLUDE[prod_short](includes/prod_short.md)] och kör **Kom igång med Power BI** från startsidan. Denna åtgärd leder dig genom samtyckesprocessen och kontrollerar din Power BI-licens. När du uppmanas att göra så, loggar du in med ett Microsoft Entra-administratörskonto. Mer information finns i [Anslut till Power BI – endast en gång](across-working-with-powerbi.md#connect).

## Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)]-data

Gör din Dynamics 365 Business Central-data tillgänglig som datakälla i Power BI Desktop och bygga kraftfulla rapporter av din verksamhets status.

Använd Power BI Desktop för att skapa rapporter som visar Dynamics 365 Business Central data. När du har skapat en rapport kan du publicera den i din Power BI-tjänst eller dela den med samtliga användare i din organisation. När rapporten väl har publicerats i Power BI-tjänsten kan användare som konfigurerats för det se rapporten i Dynamics 365 Business Central.

- För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt hämtar du följande information:

  - OData-URL för [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Denna URL har vanligtvis formatet `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, till exempel `https://localhost:7048/BC190/ODataV4`. Om du har en distribution med flera klientorganisationer bör du inkludera klientorganisationen i URL:en, till exempel `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Att användarnamn och en åtkomstnyckel till en webbtjänst tillhörande ett [!INCLUDE[prod_short](includes/prod_short.md)]-konto.

    I syfte att hämta data från [!INCLUDE[prod_short](includes/prod_short.md)] använder Power BI grundläggande autentisering. Du behöver därför ett användarnamn och en åtkomstnyckel till en webbtjänst för att ansluta. Kontot kan vara ditt eget användarkonto, eller också kanske din organisation har ett specifikt konto i detta syfte.

## <a name="getdata"></a>Lägg till [!INCLUDE[prod_short](includes/prod_short.md)] som en datakälla i Power BI Desktop

Den första uppgiften i samband med att skapa rapporter är att lägga till [!INCLUDE[prod_short](includes/prod_short.md)] som en datakälla i Power BI Desktop. När du väl är ansluten kan du börja skapa rapporten.

1. Starta Power BI Desktop.
2. Välj **Hämta data**.

    Om du inte ser **Hämta data** väljer du menyn **Arkiv** och sedan **Hämta data**.
3. På sidan **Hämta data** väljer du **Onlinetjänster**.
4. I rutan **Onlinetjänster** ansluter du till [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, välj **Dynamics 365 Business Central (lokalt)**, sedan **Anslut**.
5. Logga in till [!INCLUDE [prod_short](includes/prod_short.md)] (endast en gång).

    Om du inte har loggat in på [!INCLUDE [prod_short](includes/prod_short.md)] från Power BI desktop förut ombeds du att logga in.

   - För [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, ange först OData URL för [!INCLUDE[prod_short](includes/prod_short.md)], och välj sedan **OK**. Därefter anger du (på uppmaning) användarnamn och lösenord för det konto som ska användas för att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)]. I rutan **Lösenord** anger du åtkomstnyckeln för webbtjänsten. När du är klar, välj **Anslut**.
   
    > [!NOTE]  
    > När du väl har anslutit till [!INCLUDE[prod_short](includes/prod_short.md)] kommer du inte uppmanas att logga in en gång till. [Hur ändrar jag eller avmarkerar jag det konto som jag använder för att ansluta till Business Central från Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. När ansluten Power BI kontakten är till Business Central-tjänsten. **Navigator** fönstren visas och visar tillgängliga data källor för att skapa rapporter. Markera en mapp för att expandera den och se tillgängliga datakällor. 

   Dessa datakällor representerar samtliga de webbtjänster och AP-sidor som har publicerats för [!INCLUDE [prod_short](includes/prod_short.md)]. Datakällorna grupperas enligt de Business Central-miljöerna och företagen.

   > [!NOTE]
    > Strukturen för Business Central lokalt skiljer sig åt eftersom den inte stöder API-sidor.

7. Välj datakälla eller källor som du vill lägga till i din datamodell och välj knappen **Läs in**.
8. Om du senare vill lägga till fler Business Central-data kan du upprepa föregående steg.

När datan har lästs in kan du se den i den högra navigeringen på sidan. Vid denna tidpunkt har du anslutit till dina [!INCLUDE[prod_short](includes/prod_short.md)]-data och kan börja skapa din Power BI-rapport.  

> [!TIP]
> Mer information om hur du använder Power BI Desktop finns i [Komma igång med Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## Hantera och ändra rapporter

> [!NOTE]
> DU kan inte hantera och ändra rapporter. 

## Ladda upp rapporter

För [!INCLUDE [prod_short](includes/prod_short.md)] lokalt finns det inga demorapporter tillgängliga, så du måste börja från början med hjälp av Power BI Desktop. Alternativt kan Power BI-rapporter distribueras som uppladdningsbara filer direkt från Power BI onlinetjänst. Mer information finns i [Ladda upp rapporten till tjänsten](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## Se även

[Business Central och Power BI](admin-powerbi.md)  
[Ladda upp rapporten från filer](across-working-with-powerbi.md#upload-reports)  
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
