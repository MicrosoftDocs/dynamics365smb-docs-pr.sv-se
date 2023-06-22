---
title: Använda din adata för att skapa en app | Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa en företagsapp med Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps" />Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av Power Apps

Du kan göra din [!INCLUDE[prod_short](includes/prod_short.md)]-data tillgänglig som underlag för datakälla i Power Apps.  

> [!TIP]  
> Business Central erbjuder numera utvecklings- och driftstöd för Power Platform i AL-Go och för att komma igång med att skapa egna appar med Power Apps. Dessa funktioner visas för närvarande i förhandsgranskning. Mer information finns i [Business Central och Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) i hjälpen för utvecklare och proffs.

## <a name="prerequisites" />Förutsättningar

Du måste ha ett giltigt konto med [!INCLUDE[prod_short](includes/prod_short.md)] och med Power Apps.  

## <a name="add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps" />Lägg till [!INCLUDE[prod_short](includes/prod_short.md)] som n datakälla i Power Apps

Dessa steg lägger till en Business Central-tabell, till exempel kunder eller artiklar, som data källa för en Power Apps-app.

1. I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/), och loggar in.
2. I navigerings rutan till vänster väljer du **+ Skapa** och välj sedan **Fler datakällor** på sidan **Skapa app**.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. **Anslutningar** visar alla befintliga dataanslutningar som du har.

   - Om det redan finns en **Business Central** anslutning för det företag markerar du den och väljer **Skapa**.

   - Om du inte ser en Business Central anslutning, välj **+ Ny anslutning**, sök efter och välj **Business Central** och välj sedan **Skapa**.

   > [!NOTE]
   > Om du vill ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du välja anslutningen **Business Central (lokal)**.  
  
4. Power Apps ansluter till din [!INCLUDE[prod_short](includes/prod_short.md)]. Logga in på Business Central med kontonamn och lösenord. Om du inte är administratör för ditt [!INCLUDE[prod_short](includes/prod_short.md)] måste du kanske logga in med ett annat konto.  
5. När du har loggat in visar Power Apps en lista över *Miljöer och företag* som finns på [!INCLUDE[prod_short](includes/prod_short.md)]. Välj den miljö och det företag som innehåller de data som du vill ansluta till t. ex. *PRODUKTION – Mitt företag*.  
6. Sedan visas en lista över tabeller som visas som en del av API för din miljö. Markera den tabell som du vill ansluta till och välj sedan **Anslut**.

Dessa så kallade tabeller visas som [!INCLUDE[prod_short](includes/prod_short.md)] kopplingen för Power Apps.  

> [!NOTE]
> Om du vill ta med data från andra tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i din app, måste du samarbeta med en utvecklare för att definiera en anpassad API i [!INCLUDE[prod_short](includes/prod_short.md)].  

Nu har du lyckats ansluta till dina [!INCLUDE[prod_short](includes/prod_short.md)]-data och är redo att börja skapa din Power App. Du kan lägga till ytterligare skärmar och ansluta till ytterligare data. Mer information finns i [Skapa en arbetsyteapp från ett exempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

När du har skapat och byggt ditt program kan du dela den med dina kollegor. Mer information finns i [Spara och publicera en arbetsyteapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## <a name="sample-apps-to-get-started" />Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## <a name="develop-and-maintain-apps-application-lifecycle-management" />Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## <a name="see-related-microsoft-trainingtrainingpathspower-apps-power-automate-business-central" />Se relaterad [Microsoft utbildning](/training/paths/power-apps-power-automate-business-central/)

## <a name="see-also" />Se även

[Skapa en arbetsyteapp från en mall i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Komma igång med att utveckla anslutningsprogram för Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
