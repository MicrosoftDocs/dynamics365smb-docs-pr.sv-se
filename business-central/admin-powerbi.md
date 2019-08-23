---
title: Aktivera affärsdata för Power BI | Microsoft Docs
description: Det är enkelt att få insikter, affärsinformation och KPI:er från dina Business Central-data med Business Central-appar för Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 07/08/2019
ms.author: bmeier
ms.openlocfilehash: 4223d3eba6253f87aee3f86b3a9dfe4107d48947
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755270"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivera affärsdata för Power BI

Att få insikter om dina [!INCLUDE[prodshort](includes/prodshort.md)]-data är enkelt med [!INCLUDE[prodshort](includes/prodshort.md)]-appar för Power BI. Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.  

Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power BI. Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) om du vill skapa dina egna Power BI-rapporter. Power BI -appar kräver behörighet till de tabeller som data ska hämtas ifrån. Mer information om kraven beskrivs nedan.  

> [!IMPORTANT]
> De Power BI-appar som beskrivs i den här artikeln har utformats för att använda Azure Active Directory som verifieringsmekanism om inget annat anges. Om du vill installera en Power BI- app måste du också ha en Power BI Pro-licens.  När Power BI-appen installerats kan det delas med användare med valfri licenstyp.

Microsoft har publicerat följande apparför Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)] (lokal) - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] (lokal) - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] (lokal) - Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Använda [!INCLUDE [prodshort](includes/prodshort.md)]-instrumentpanelerna i Power BI

Varje app ger rapporter som du kan söka i:

- Välj något visuellt på instrumentbrädan för att få upp en av de underliggande rapporterna.  
- Filtrera rapporten eller lägg till fält som du vill övervaka.  
- Sätt fast den här vyn på instrumentbrädan om du vill fortsätta spårningen.  
  Du kan uppdatera data manuellt och du kan ställa in ett schema för uppdatering. Mer information finns i [konfigurera schemalagd uppdatering](/power-bi/refresh-scheduled-refresh).  

Apparna har utformats för att fungera med data från alla företag som du har i [!INCLUDE[prodshort](includes/prodshort.md)]. När du installerar Power BI-appen anger du en eller flera parametrar för att ansluta till [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Du kan också skapa egna rapporter och instrumentpaneler i Power BI utifrån dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Mer information finns i [ansluta din affärsdata till Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Så här ansluter du data i Power BI

1. Öppna webbläsaren, gå till https://powerbi.microsoft.com och logga in på kontot.
2. Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.  

    ![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Du kan också komma igång från [!INCLUDE [prodshort](includes/prodshort.md)]. Från startsidan går du till **rapportval** i avsnittet Power BI. Välj antingen **Service** eller **Min organisation** i menyfliken. När något av ovanstående åtgärder är markerade förs du till antingen galleriet Organisation i Power BI eller till Microsoft AppSource, vilket även filtreras att bara visa appar relaterade till [!INCLUDE[prodshort](includes/prodshort.md)].

3. I rutan **Tjänster**, markera **Hämta**. Då öppnas en sida som visar **AppSource** och **Appar för Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Markera **Appar** från fliken **Appar för Power BI**, välj den **Microsoft Dynamics 365 Business Central**-app som du vill använda och välj sedan **Hämta nu**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Ange namnet på det företag i din [!INCLUDE[prodshort](includes/prodshort.md)] som du vill ansluta till när du ombeds göra det. Detta är inte visningsnamnet. Du kan hitta företagsnamnet på sidan **Företag** i din [!INCLUDE[prodshort](includes/prodshort.md)]-instans.  

    > [!NOTE]
    > Om du ansluter till [!INCLUDE [prodshort](includes/prodshort.md)] lokalt måste du ange parametern *webbtjänst-URL*. Sök efter detta på sidan **webbtjänster** i [!INCLUDE [prodshort](includes/prodshort.md)]. Din [!INCLUDE [server](includes/server.md)]-instans måste vara konfigurerad för grundläggande autentisering och du måste ange en användare och den användarens webbåtkomstnyckel som lösenord. I följande exempel ersätter du *myserver:7048* med ditt [!INCLUDE [server](includes/server.md)] namn och *CRONUS%20US* med ditt företags namn.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. När du är ansluten läggs en instrumentpanel och rapporter till i din Power BI-arbetsyta. När den är slutförd visas information från ditt [!INCLUDE[prodshort](includes/prodshort.md)]-företag.

    ![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Vad nu?

- Försök med att [ställa en fråga i rutan Frågor och svar](/power-bi/service-q-and-a-tips) högst upp i instrumentpanelen.
- [Ändra panelerna](/power-bi/service-dashboard-edit-tile) på instrumentpanelen.  
- [Välj en panel](/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.  
- Som standard är din datauppsättning inte schemalagd att uppdateras. Du kan ändra uppdateringsschema eller försöka uppdatera på begäran med **uppdatera nu**. Mer information finns i [konfigurera schemalagd uppdatering](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI i [!INCLUDE [prodshort](includes/prodshort.md)]

Din startsida i [!INCLUDE [prodshort](includes/prodshort.md)] kan innehålla ett Power BI kontrollelement som kan konfigureras så att det visar Power BI rapporter på din startsida.

> [!IMPORTANT]
> Du måste ha ett giltigt konto med [!INCLUDE [prodshort](includes/prodshort.md)] och med Power BI. Om du vill ändra någon rapport måste du också hämta Power BI Desktop. Mer information finns i [Använda Business Central som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Vid första inloggningen

När du först loggar in på [!INCLUDE [prodshort](includes/prodshort.md)] kommer du att märka en tom Power BI del på startsidan. Om du ska kunna visa rapporterna måste du först ansluta till Power BI genom att välja länken *kom igång med Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)] kommunicerar sedan med Power BI-tjänsten för att avgöra om du har ett giltigt Power BI-konto. När din licens har kontrollerats visas Power BI-standardrapporterna på din startsida.

### <a name="selecting-power-bi-reports"></a>Välja Power BI-rapporter

Power BI-kontrollen på startsidan kan visa vilken Power BI-rapport som helst. Om du vill visa en befintlig rapport väljer du åtgärden **Markera rapport** i Power BI kommandolistrutan.  

På sidan för rapportval visas en lista över alla Power BI-rapporter som du har tillgång till. Den här listan hämtas från Power BI arbetsytan. Aktivera varje rapport som du vill visa på startsidan och välj sedan OK. Du kommer tillbaka till din startsida och den sista rapporten som du aktiverade visas. Använd den nedrullningsbara kommandolistan och använd föregående och nästa kommando för att navigera mellan rapporter.  

### <a name="get-reports"></a>Hämta rapporter

Om inga rapporter visas på sidan Välj rapporter, eller om du inte ser någon rapport som du vill ha. Du kan välja att hämta rapporter från *min organisation* eller från *tjänster*.
Välj *min organisation* för att gå till de Power BI-tjänster där du kan visa de rapporter inom organisationen som du har varit rättigheter att visa och lägga till i arbetsytan. Välj *tjänster* för att gå till Microsoft AppSource där du kan installera Power BI-appar.  

Du kan också välja att skapa nya Power BI-rapporter. När dessa rapporter har publicerats på Power BI arbetsytan visas de på den här sidan.  

### <a name="managing-reports"></a>Hantera rapporter

I Power BI-avsnittet på startsidan kan du välja åtgärden **hantera rapport** i kommandolistrutan så att du kan ändra den rapport som ingick i rollcentret.  

Ändringar kan göras i rapporten och sparas.  Alla ändringar som du gör i rapporten kommer att ändras för alla användare som rapporten delas med eftersom du ändrar rapporten som är lagrad i Power BI-tjänsten.  

När du är klar med ändringarna väljer du spara. Om det är en delad rapport vill du kanske Spara som om du inte vill göra ändringen för alla användare.
Gå tillbaka till rollcentret så visas den uppdaterade rapporten. Om du gjorde kommandot Spara som måste du öppna den valda rapportsidan och aktivera den nya rapporten.

### <a name="uploading-reports"></a>Överför rapporter

Du kan överföra nya Power BI-rapporter och dela dem med alla användare av [!INCLUDE [prodshort](includes/prodshort.md)]. Rapporterna delas i respektive företag i [!INCLUDE [prodshort](includes/prodshort.md)].  

Om du vill ladda upp en rapport väljer du åtgärden **Ladda upp rapport** från kommandolistrutan. Du kan sedan överföra en .pbix-fil som definierar de rapporter som du vill dela. Du kan ändra standardnamn på filen.  

När rapporten har överförts till Power BI arbetsytan överförs den automatiskt till Power BI arbetsytorna för alla andra användare på företaget när nästa loggar in på [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Systemkrav

För att importera dina [!INCLUDE[prodshort](includes/prodshort.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data. De webbtjänster som krävs för respektive Power BI-app är:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Försäljningsmöjligheter
- Excel-mallen för Visa företagsinformation
- Power BI Rapportetiketter

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- Power BIFinance
- Excel-mallen för Visa företagsinformation
- Power BI Rapportetiketter

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central – Sales

- Artikelförsäljning efter kund
- Instrumentbräda för försäljning
- Excel-mallen för Visa företag
- Power BI Rapportetiketter

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] lokalt använder samma webbtjänst slutpunkter som [!INCLUDE [prodshort](includes/prodshort.md)] online.

## <a name="web-services"></a>Webbtjänster

Ett enkelt sätt att hitta webbtjänsterna är att söka efter *webbtjänster* i [!INCLUDE[prodshort](includes/prodshort.md)]. På sidan **webbtjänster** ser du till att fältet **publicera** är markerat för de webbtjänster som visas ovan.

## <a name="troubleshooting"></a>Felsökning

Instrumentbrädan för Power BI förlitar sig på de publicerade webbtjänsterna som visas ovan, och kommer att innehålla data från demonstrationsföretaget eller ditt eget företag om du importerar data från den aktuella finanslösningen. Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.  

### <a name="you-do-not-have-a-power-bi-account"></a>Du har inte något Power BI-konto

Inget Power BI-konto har angetts. För att du ska kunna använda ett giltigt Power BI-konto måste du ha en licens och du måste du ha loggat in på Power BI tidigare för att Power BI arbetsytan ska kunna skapas.  

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Du behöver en Power BI Pro-licens för att installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen i Power BI

Power BI-appar kan endast installeras av användare som har en Power BI Pro-licens. När Power BI-appen installerats kan du dela den med användare som inte har en Power BI Pro-licens.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Parametervalidering misslyckades. Se till att alla parametrar är giltiga"

Det här felet indikerar att den andra parametern är ogiltig.

- Den angivna företagsparametern matchar inte några befintliga [!INCLUDE [prodshort](includes/prodshort.md)]-företag. Kontrollera företagsnamnet på sidan **företag** i [!INCLUDE [prodshort](includes/prodshort.md)].
- Vid anslutning till [!INCLUDE [prodshort](includes/prodshort.md)] lokal. Du har angett en ogiltig URL. Du kan kontrollera URL på sidan **webbtjänster** i [!INCLUDE [prodshort](includes/prodshort.md)]  
- En port är inte öppen för att tillåta begäran att gå igenom brandväggen.

### <a name="login-failed"></a>Inloggningen misslyckades

Om du får felet Inloggningen misslyckades när du har loggat med dina [!INCLUDE [prodshort](includes/prodshort.md)] användarautentiseringsuppgifter upplever du förmodligen något av följande problem:

- Kontot som du använder har inte behörighet att hämta [!INCLUDE [prodshort](includes/prodshort.md)]-data från ditt konto. Kontrollera att du har behörighet för de data som krävs i [!INCLUDE [prodshort](includes/prodshort.md)] och försök igen.
- Du har valt en annan autentiseringstyp än grundläggande vid anslutning till [!INCLUDE [prodshort](includes/prodshort.md)] lokalt.
- Du har inte angett ett giltigt användarnamn eller lösenord.

### <a name="incorrect-company-name"></a>Felaktigt företagsnamn

Ett vanligt fel är att ange företagets visningsnamn i stället för namnet på företaget. Söka efter **Företag** för att hitta företagsnamnet. Använda fältet **Namn** när du anger företagets namn.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nyckeln matchade inte några rader i tabellen

Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”Nyckeln matchar inga rader i tabellen”. Ange rätt företagsnamn och försök ansluta igen.

### <a name="historical-data-appears-to-be-missing"></a>Historiska data saknas

När Power BI-appen har installerats och dina data visas i Power BI kan det hända att inte alla data visas. Datauppsättningar filtreras endast för att returnera föregående 365 dagar av data. Standardvärdet är på plats för att göra rapporterna snabbare.  

### <a name="i-only-see-data-for-a-single-company"></a>Jag ser endast data för ett enskilt företag

I Power BI-appen visas endast data från [!INCLUDE [prodshort](includes/prodshort.md)]-företaget som definierades när Power BI-appen installerades. Data från ytterligare företag kan läggas till i rapporterna genom att lägga till nya frågor som använder olika företag som datakälla.  

## <a name="see-also"></a>Se även

[Komma igång med Power BI](/power-bi/service-get-started)  
[Power BI- Grundläggande begrepp](/power-bi/service-basic-concepts)  
[Appar i Power BI](/power-bi/consumer/end-user-app)  
[Snabbstart: Ansluta till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)  
[Med hjälp av [!INCLUDE[d365fin](includes/d365fin_md.md)] som en PowerApps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
