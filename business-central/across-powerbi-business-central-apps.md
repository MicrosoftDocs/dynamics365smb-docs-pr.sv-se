---
title: Använda Business Central-appar i Power BI
description: 'Använda insikter, business intelligence och KPI:er från dina Business Central-data är enkelt med Business Central-apparna för Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# Använda [!INCLUDE [prod_short](includes/prod_short.md)]-apparna i Power BI

> **GÄLLER:** [!INCLUDE [prod_long](includes/prod_long.md)] online 

[!INCLUDE [prod_long](includes/prod_long.md)] publicerar följande Power BI-appar som tillhandahåller detaljerade instrumentpaneler för datavisning:

- [!INCLUDE [prod_long](includes/prod_long.md)] – CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Sales

## Översikt

Varje app innehåller ett flertal rapporter som du kan bearbeta för data, inklusive följande funktioner:

- Välj något visuellt på instrumentbrädan för att få upp en av de underliggande rapporterna.  
- Filtrera rapporten eller lägg till fält som du vill övervaka.  
- Fäst en anpassad vy på instrumentpanelen om du vill fortsätta spåra.  
  Du kan uppdatera data manuellt och du kan ställa in en uppställning för uppdatering. Mer information finns i [konfigurera schemalagd uppdatering](/power-bi/refresh-scheduled-refresh).  

Apparna har utformats för att arbeta med data från valfritt företag i [!INCLUDE[prod_short](includes/prod_short.md)]. När du installerar Power BI-appen anger du en eller flera parametrar för att ansluta till [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Du kan också skapa egna rapporter och instrumentpaneler i Power BI utifrån dina [!INCLUDE[prod_short](includes/prod_short.md)]-data. Mer information finns i [ansluta din affärsdata till Power BI](across-how-use-financials-data-source-powerbi.md). 

## Förutsättningar

Power BI-appar kräver behörighet till de tabeller där datan hämtas ifrån samt till de webbtjänster som används för att hämta data. Följande tabell anger de webbtjänster som krävs för respektive Power BI-app:
    
|App | Webbtjänster|
|----|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Försäljningsmöjligheter</li><li>Excel-mallen för Visa företagsinformation</li><li>Power BI Rapportetiketter</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Ekonomi| <ul><li>Power BIFinance</li><li>Excelmallsvy, företagsinformation</li><li>Power BI Rapportetiketter</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Försäljning| <ul><li>Artikelförsäljning efter kund</li><li>Instrumentbräda för försäljning</li><li>Excelmallsvy, företagsinformation</li><li>Power BI Rapportetiketter</li></ul>|

> [!TIP]
> Ett enkelt sätt att hitta webbtjänsten är att söka efter *webbtjänster* i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **webbtjänster** ser du till att fältet **publicera** är markerat för de webbtjänster som visas ovan. Mer information finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

## Gör dig redo

Registrera dig frö Power BI-tjänsten. Gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com) om du inte redan har registrerat dig. När du registrerar dig använder du din e-postadress för arbetet samt ditt lösenord.

## Installera en [!INCLUDE[prod_short](includes/prod_short.md)]-app i Power BI

1. Öppna din webbläsare, gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com) och logga in på ditt konto.
2. Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.  

    ![Navigera för att hämta data.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Du kan också komma igång från [!INCLUDE [prod_short](includes/prod_short.md)]. Från startsidan går du till **rapportval** i avsnittet Power BI. Välj antingen **Service** eller **Min organisation** i menyfliken. Organisationsgalleriet i antingen Power BI eller Microsoft AppSource öppnas, filtrerat att endast visa appar relaterade till [!INCLUDE[prod_short](includes/prod_short.md)].

3. I rutan **Tjänster**, markera **Hämta**.

    Detta steg öppnar sidan **Power BI-appar** och låter dig bläddra efter Power BI-appar som finns tillgängliga i **AppSource**.  

4. I rutan **Sök** anger du **Dynamics 365 Business Central**.
5. Välj den app du vill använda, välj **Hämta nu** och sedan **Installera**.  

    Efter slutförd installation finns appen tillgänglig via **Appar** i navigeringsmenyn i Power BI.

## Ansluta [!INCLUDE[prod_short](includes/prod_short.md)]-appen till dina data

1. Under **Appar** väljer du appen Business Central och sedan **Anslut**.
2. När du uppmanas till det fyller du i **Företagets namn** och **Miljö** med information om den [!INCLUDE[prod_short](includes/prod_short.md)]-instans som du vill ansluta till.

    - Se till att fylla i det fullständiga namnet för **Företagsnamn** inte enbart visningsnamnet. Företagsnamnet hittar du på sidan **Företag** i [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Ange **Produktion** för **Miljö** om du inte har skapat flera olika miljöer.

3. Välj **Nästa**.
4. Välj **Inloggning**.
5. När du uppmanas till det anger du användarnamn och lösenord för att logga in i [!INCLUDE[prod_short](includes/prod_short.md)].
6. När du är ansluten läggs en instrumentpanel och rapporter till i din Power BI-arbetsyta. När den är slutförd visas information från ditt [!INCLUDE[prod_short](includes/prod_short.md)]-företag.

    ![Välj Dynamics 365 Business Central och välj Hämta nu.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## Åtgärda problem

Power BI-instrumentpanelen vilar på de publicerade webbtjänster som anges ovan. Om du importerar data från din nuvarande ekonomilösning visar den data från demonstrationsföretaget eller från ditt eget företag. Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.  

### Du har inget Power BI-konto

Inget Power BI-konto har konfigurerats. Du måste ha en licens för att få ett giltigt Power BI-konto. Du måste dessutom redan ha loggat in i Power BI för att skapa din Power BI-arbetsyta.  

### Meddelande: det finns inga aktiverade rapporter. Visa en lista med rapporter du kan visa med Välj rapport.

Detta meddelande visas om den förvalda rapporten inte lyckas distribuera din Power BI-arbetsyta. Alternativt har rapporten distribuerats men inte uppdaterats korrekt. Om detta problem uppstår går du till rapporten på din Power BI-arbetsyta, väljer **Datauppsättning**, **Inställningar** och uppdaterar sedan autentiseringsuppgifterna manuellt. När datauppsättningen har uppdaterats går du tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)] och väljer rapporten manuellt på sidan **Välj rapporter**.

### Du behöver en Power BI Pro-licens för att installera [!INCLUDE[prod_short](includes/prod_short.md)]-appen i Power BI

För att kunna dela ditt innehåll behöver såväl du som de personer du delar med en [Power BI Pro-licens](/power-bi/service-features-license-type). Innehållet måste ligga på en arbetsyta med [Premium-kapacitet](/power-bi/service-premium-what-is). Mer information finns i [Så här delar du ditt arbete i Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### "Parametervalidering misslyckades. Se till att alla parametrar är giltiga"

Detta fel indikerar ett ytterligare en parameter är ogiltig.

- Angiven miljöparameter matchar ingen befintlig produktions- eller sandbox-miljö i [!INCLUDE[prod_short](includes/prod_short.md)].
- Angiven företagsparameter matchar inga befintliga [!INCLUDE[prod_short](includes/prod_short.md)]-företag. Kontrollera företagsnamnet på sidan **företag** i [!INCLUDE[prod_short](includes/prod_short.md)].
- Om du ansluter till [!INCLUDE[prod_short](includes/prod_short.md)]-lokalt har du angett en ogiltig URL. Du kan kontrollera URL på sidan **webbtjänster** i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Det finns ingen öppen port som möjliggör din begäran via din brandvägg.

### Det går inte att logga in

Om du får felet ”Inloggningen misslyckades” när du försöker logga in med dina [!INCLUDE[prod_short](includes/prod_short.md)]-autentiseringsuppgifter har du troligtvis råkat ut för något av följande problem:

- Det konto som du använder har inte behörighet att hämta [!INCLUDE[prod_short](includes/prod_short.md)]-data från ditt konto. Kontrollera att du har behörighet för de data som krävs i [!INCLUDE[prod_short](includes/prod_short.md)] och försök igen.
- Om du ansluter till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt har du valt en autentiseringstyp som inte är Grundläggande.
- Du har inte angett ett giltigt användarnamn eller lösenord.

### Meddelande: Din datakälla kan inte uppdateras eftersom autentiseringsuppgifterna är ogiltiga. Uppdatera dina autentiseringsuppgifter och försök igen

För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan felet bestå i att OData-URL:en endast visas för det lokala nätverket.

### Felaktigt företagsnamn

Ett vanligt fel är att ange företagets visningsnamn i stället för namnet på företaget. Söka efter **Företag** för att hitta företagsnamnet. Använda fältet **Namn** när du anger företagets namn.

### Nyckeln matchade inte några rader i tabellen

Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”Nyckeln matchar inga rader i tabellen”. Ange rätt företagsnamn och försök ansluta igen.

### Historiska data saknas

När Power BI-appen installerats och dina data syns i Power BI noterar du att inte samtliga dina data visas. Datauppsättningar filtreras endast för att returnera föregående 365 dagar av data. Standardvärdet är på plats för att göra rapporterna snabbare.  

### Jag ser endast data för ett enskilt företag

I Power BI-appen visas endast data från [!INCLUDE[prod_short](includes/prod_short.md)]-företaget som definierades när Power BI-appen installerades. Data från ytterligare företag kan läggas till i rapporterna genom att lägga till nya frågor som använder olika företag som datakälla.  

### Vad nu?

- Försök med att [ställa en fråga i rutan Vanliga frågor och svar](/power-bi/service-q-and-a-tips) högst upp i instrumentpanelen.
- [Ändra panelerna](/power-bi/service-dashboard-edit-tile) på instrumentpanelen.  
- [Välj en panel](/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.  
- Din datauppsättning har inte schemalagts att uppdateras som standard. Du kan ändra uppdateringsuppställningen eller försöka uppdatera den på begäran med **Uppdatera nu**. Mer information finns i [Konfigurera schemalagd uppdatering](/power-bi/refresh-scheduled-refresh).

## Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Se även

[Business Central och Power BI](admin-powerbi.md)  
[Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbeta med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)  
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
