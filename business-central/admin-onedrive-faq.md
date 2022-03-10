---
title: Vanliga frågor och svar om OneDrive för företag
description: Få svar på några vanliga frågor om att arbeta med OneDrive för företag och Business Central.
author: bholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: f54e8b6290e9dd653180b3ea05246255b84dc2ae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144056"
---
# <a name="onedrive-for-business-faq"></a>Vanliga frågor och svar om OneDrive för företag

[!INCLUDE [online_only](includes/online_only.md)]

I den här artikeln besvaras några frågor som du kanske har kring arbetet med OneDrive och [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all-prod_short-clients"></a>Fungerar detta hos alla [!INCLUDE[prod_short](includes/prod_short.md)] klienter?

Ja. Du kan öppna filer OneDrive från [!INCLUDE[prod_short](includes/prod_short.md)] mobilappar när du visar kort information i Microsoft Teams eller till och med från Outlook-tillägget.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Är OneDrive det samma som SharePoint för att lagra filer?

Som en del av din Microsoft 365-prenumeration tillhandahåller organisationen dig OneDrive, din fillagring i molnet. OneDrive är privat som standard, där du strukturerar innehållet och väljer vilka filer eller mappar som ska delas och vem som ska delas. SharePoint å andra sidan, visas en fildatabas i molnet som delas med andra i organisationen.  

## <a name="does-prod_short-support-consumer-onedrive"></a>Stöder [!INCLUDE[prod_short](includes/prod_short.md)] kund OneDrive?

Nr Integrationen är uteslutande avsedd för OneDrive för företag och har endast stöd för ditt arbetskonto. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Stöds alla OneDrive för affärsplaner?

[!INCLUDE[prod_short](includes/prod_short.md)] stöder inte fristående planer för OneDrive för företag. OneDrive måste köpas som en del av en affärs- eller företagsplan för Microsoft 365. Mer information finns i [jämföra OneDrive priser och planer för molnlagring](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Var kan jag se en OneDrive tjänsthälsa?

Administratörer kan komma åt instrumentpanelen för tjänsthälsa som en del av administrationscentret för Microsoft 365. Instrumentpanelen innehåller OneDrive tjänsttillgänglighet. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>Är OneDrive integrering tillgänglig för [!INCLUDE[prod_short](includes/prod_short.md)] lokala platser?

Ja, men till skillnad från [!INCLUDE[prod_short](includes/prod_short.md)] online, krävs ytterligare inställningar. Mer information finns i [Konfigurera Business Central lokalt](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a>Ansluter [!INCLUDE[prod_short](includes/prod_short.md)] lokal med SharePoint server?

Nr Den här distributionskombinationen stöds inte även om SharePoint servern har aktiverat mina webbplatser.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a>Ansluter [!INCLUDE[prod_short](includes/prod_short.md)] online med SharePoint server?

Nr Den här distributionskombinationen stöds inte även om SharePoint servern har aktiverat mina webbplatser.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Hur fungerar det här i en organisation med flera miljöer?

Integrationen förutsätter att företagsnamn är unika i olika [!INCLUDE[prod_short](includes/prod_short.md)] miljöer. När företags namn är unika i hela organisationen OneDrive kommer filen att kopieras till en mapp som namnges efter det aktuella företaget när du öppnar filen i. Om företagsnamn inte är unika i olika miljöer kommer filer från identiska företagsnamn att placeras i samma mapp.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Vi har bytt företagsnamn. Vad händer med mina tidigare filer?

[!INCLUDE[prod_short](includes/prod_short.md)] flyttar inte automatiskt över filer som du har öppnat tidigare i OneDrive till den nya mappen. När du har bytt namn på företaget kommer Öppna åtgärden OneDrive kopierar filerna till en mapp med det nya företagsnamnet.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>När filer bifogas till [!INCLUDE[prod_short](includes/prod_short.md)], hur väljer jag en fil från OneDrive? 
[!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller inte någon molnfilväljare. Du måste hämta filen från OneDrive till enheten och sedan överföra den till [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Jag vill öppna filer i SharePoint i stället. Hur gör jag detta?

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller inte funktioner för att kopiera filer till SharePoint och öppna dem från ett SharePoint bibliotek. Kontakta din Microsoft-partner för att förstå dina alternativ eller sök efter appar på AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Hur stänger jag av integreringen OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] online ger inget sätt för att aktivera eller inaktivera integration till OneDrive.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Ska jag använda sidan SharePoint anslutningsinställningar för att ansluta till SharePoint?

Det här är en äldre funktion där alla [!INCLUDE[prod_short](includes/prod_short.md)] filer från alla användare skickas till en enda SharePoint mapp. Vi rekommenderar att du inte konfigurerar snabbfliken delade dokument på SharePoint anslutningskonfigurationen eftersom vi arbetar mot att ta den gamla funktionen.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>Vilken version av [!INCLUDE[prod_short](includes/prod_short.md)] support OneDrive?

Integrationen med OneDrive blev tillgänglig i 2021 utgivningscykel 2.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Kommer Microsoft att fortsätta att förbättra integrationen till OneDrive?

På Microsoft lyssnar vi ständigt på feedback från våra olika användargrupper och agerar utifrån de bästa förslagen. Om du vill veta mer om vad som stundar för integreringar med Microsoft 365-appar läser du [versionsplanen för Dynamics 365](/dynamics365-release-plan/2021wave1).  

Om du vill delta i att förbättra OneDrive integrationen, eller ha en idé som förbättrar fildelningen och samarbetet [!INCLUDE[prod_short](includes/prod_short.md)], lägger du till en idé eller röst för befintliga idéer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Felsökning

I det här avsnittet finns information om hur du identifierar och korrigerar problem som kan uppstå vid användning av OneDrive med [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Jag måste logga in varje gång jag öppnar en fil

Det är tyvärr ett känt problem och vi arbetar på det. Vi räknar med att ge en smidigare erfarenhet av en kommande uppdatering.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central kan inte hitta mitt OneDrive

När meddelandet visas "kunde inte avgöra var ditt OneDrive för företag finns, kontakta din partner för att konfigurera detta", kontrollera om användaren har åtkomst OneDrive minst en gång. Om de inte gör det ber du personen att gå till portal.office.com/onedrive där du kan ställa in den. Det kan ta en stund. Kontakta supporten om meddelandet fortfarande visas efter 24 timmar.  
 

## <a name="see-also"></a>Se även
[Business Central och OneDrive integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
