---
title: Vanliga frågor och svar om OneDrive för företag
description: Få svar på några vanliga frågor om att arbeta med OneDrive för företag och Business Central.
author: brentholtorf
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="onedrive-for-business-faq"></a>Vanliga frågor och svar om OneDrive för företag

[!INCLUDE [online_only](includes/online_only.md)]

I den här artikeln besvaras några frågor som du kanske har kring arbetet med OneDrive och [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all--clients"></a>Fungerar detta hos alla [!INCLUDE[prod_short](includes/prod_short.md)] klienter?

Ja. Du kan öppna filer OneDrive från [!INCLUDE[prod_short](includes/prod_short.md)] mobilappar när du visar kort information i Microsoft Teams eller till och med från Outlook-tillägget.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Är OneDrive det samma som SharePoint för att lagra filer?

Som en del av din Microsoft 365-prenumeration tillhandahåller organisationen dig OneDrive, din fillagring i molnet. OneDrive är privat som standard, där du strukturerar innehållet och väljer vilka filer eller mappar som ska delas och vem som ska delas. SharePoint å andra sidan, visas en fildatabas i molnet som delas med andra i organisationen.  

## <a name="does--support-consumer-onedrive"></a>Stöder [!INCLUDE[prod_short](includes/prod_short.md)] kund OneDrive?

Nr. Integrationen är uteslutande avsedd för OneDrive för företag och har endast stöd för ditt arbetskonto. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Stöds alla OneDrive för affärsplaner?

[!INCLUDE[prod_short](includes/prod_short.md)] stöder inte fristående planer för OneDrive för företag. OneDrive måste köpas som en del av en affärs- eller företagsplan för Microsoft 365. Mer information finns i [jämföra OneDrive priser och planer för molnlagring](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Var kan jag se en OneDrive tjänsthälsa?

Administratörer kan komma åt instrumentpanelen för tjänsthälsa som en del av administrationscentret för Microsoft 365. Instrumentpanelen innehåller OneDrive tjänsttillgänglighet. Gå till [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## <a name="is-onedrive-integration-available-to--on-premises"></a>Är OneDrive integrering tillgänglig för [!INCLUDE[prod_short](includes/prod_short.md)] lokala platser?

Ja, men till skillnad från [!INCLUDE[prod_short](includes/prod_short.md)] online, krävs ytterligare inställningar. Mer information finns i [Konfigurera Business Central lokalt](admin-onedrive-integration-onpremises.md).  

## <a name="does--on-premises-connect-with-sharepoint-server"></a>Ansluter [!INCLUDE[prod_short](includes/prod_short.md)] lokal med SharePoint server?

Nr. Den här distributionskombinationen stöds inte även om SharePoint-servern har aktiverat Mina webbplatser.  

## <a name="does--online-connect-with-sharepoint-server"></a>Ansluter [!INCLUDE[prod_short](includes/prod_short.md)] online med SharePoint server?

Nr. Den här distributionskombinationen stöds inte även om SharePoint-servern har aktiverat Mina webbplatser.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Hur fungerar det här i en organisation med flera miljöer?

Integrationen förutsätter att företagsnamn är unika i olika [!INCLUDE[prod_short](includes/prod_short.md)] miljöer. När företags namn är unika i hela organisationen OneDrive kommer filen att kopieras till en mapp som namnges efter det aktuella företaget när du öppnar filen i. Om företagsnamn inte är unika i olika miljöer kommer filer från identiska företagsnamn att placeras i samma mapp.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Vi har bytt företagsnamn. Vad händer med mina tidigare filer?

[!INCLUDE[prod_short](includes/prod_short.md)] flyttar inte automatiskt över filer som du har öppnat tidigare i OneDrive till den nya mappen. När du har bytt namn på företaget kommer Öppna åtgärden OneDrive kopierar filerna till en mapp med det nya företagsnamnet.   

## <a name="when-attaching-files-to--how-do-i-pick-a-file-from-onedrive"></a>När filer bifogas till [!INCLUDE[prod_short](includes/prod_short.md)], hur väljer jag en fil från OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller inte någon molnfilväljare. Du måste hämta filen från OneDrive till enheten och sedan överföra den till [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Jag vill öppna filer i SharePoint i stället. Hur gör jag detta?

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller inte funktioner för att kopiera filer till SharePoint och öppna dem från ett SharePoint-bibliotek. Kontakta din Microsoft-partner för att förstå dina alternativ eller sök efter appar på AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Hur stänger jag av integreringen OneDrive?

Kör guiden för assisterad konfiguration **OneDrive-konfiguration** och inaktivera **Använd OneDrive för appfunktioner** och **Använd OneDrive för systemfunktioner**. 

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Ska jag använda sidan SharePoint anslutningsinställningar för att ansluta till SharePoint?

Det här är en äldre funktion där alla [!INCLUDE[prod_short](includes/prod_short.md)] filer från alla användare skickas till en enda SharePoint mapp. Vi rekommenderar att du inte konfigurerar snabbfliken Delade dokument på sidan **SharePoint-anslutningskonfigurationen** eftersom sidan är [inaktuell](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) och kommer att tas bort i utgivningscykel 2 år 2023, version 23.0.  Vi rekommenderar att du använder **OneDrive-konfiguration** istället.  

## <a name="which-version-of--supports-onedrive"></a>Vilken version av [!INCLUDE[prod_short](includes/prod_short.md)] support OneDrive?

Integrationen med OneDrive blev tillgänglig i 2021 utgivningscykel 2.  

## <a name="which-features-are-affected-by-onedrive-integration"></a><a name="features"></a>Vilka funktioner påverkas av OneDrive-integrationen?

I guiden för assisterad konfiguration **OneDrive-konfiguration** för konfiguration av OneDrive-integrationen kan du aktivera eller inaktivera funktioner för hantering av Business Central-filer i OneDrive. Funktionerna är uppdelade i två alternativ:

|Alternativ|Description|
|------|----------|
|**Använd OneDrive för appfunktioner**|Om du aktiverar det här alternativet tillgängliggörs åtgärderna **Öppna i OneDrive** och **Dela** för filer i Business Central, som filer som bifogas dokument eller i rapportinkorgen. Med dessa åtgärder kan användare kopiera, öppna och dela filer i OneDrive. Mer information finns i [Öppna och dela Business Central-filer i OneDrive](across-share-onedrive.md).
|**Använd OneDrive för systemfunktioner**|När du aktiverar det här alternativet aktiveras följande funktioner:<ul><li> Åtgärderna **Öppna i Excel** och **Redigera i Excel** på listsidor kopierar automatiskt Excel-filen till OneDrive och öppnar den sedan i Excel Online. Mer information finns i [Visa och redigera i Excel](across-work-with-excel.md).</li><li> När du skickar en rapport till en Excel- eller Word-fil kopieras filen automatiskt till OneDrive och öppnas sedan i Excel eller Word online. Mer information finns i [Spara en rapport till en fil](ui-work-report.md#saving-a-report-to-a-file).|

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Kommer Microsoft att fortsätta att förbättra integrationen till OneDrive?

På Microsoft lyssnar vi ständigt på feedback från våra olika användargrupper och agerar utifrån de bästa förslagen. Om du vill veta mer om vad som stundar för integreringar med Microsoft 365-appar läser du [versionsplanen för Dynamics 365](/dynamics365-release-plan/2021wave1).  

Om du vill delta i att förbättra OneDrive integrationen, eller ha en idé som förbättrar fildelningen och samarbetet [!INCLUDE[prod_short](includes/prod_short.md)], lägger du till en idé eller röst för befintliga idéer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Felsökning

I det här avsnittet finns information om hur du identifierar och korrigerar problem som kan uppstå vid användning av OneDrive med [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central kan inte hitta mitt OneDrive

När meddelandet visas "kunde inte avgöra var ditt OneDrive för företag finns, kontakta din partner för att konfigurera detta", kontrollera om användaren har åtkomst OneDrive minst en gång. Om de inte gör det ber du personen att gå till portal.office.com/onedrive där du kan ställa in den. Det kan ta en stund. Kontakta supporten om meddelandet fortfarande visas efter 24 timmar.  
 
### <a name="im-having-problems-sharing-from-outlook"></a>Jag får problem när jag delar från Outlook

Se [Kan inte dela OneDrive-filer från Outlook.com](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) på Microsoft support.

### <a name="actions-open-in-onedrive-and-share-are-missing"></a>Åtgärderna Öppna i OneDrive och Dela saknas

Du kan kontrollera ett par saker:

- Kontrollera att programfunktionerna för OneDrive är aktiverade i guiden för assisterad konfiguration **OneDrive-konfiguration**. Se [Konfigurera OneDrive med OneDrive-konfiguration](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Kontrollera att Microsoft OneDrive är inställt på **Godkänn** på sidan **Status för sekretessmeddelanden**. Se [Status för sekretessmeddelanden](privacy-notices-status.md).

## <a name="see-also"></a>Se även

[Business Central- och OneDrive-integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
