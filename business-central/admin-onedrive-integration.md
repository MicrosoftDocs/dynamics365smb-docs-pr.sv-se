---
title: Hantera OneDrive-integrering med Business Central
description: Lär dig mer om vad du kan göra för att hantera en integration mellan Business Central och OneDrive för företag.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: cceb05c1ad19a95494c188cd2482b45962535c94
ms.sourcegitcommit: 99c705d160451c05b226350ff94b52fb0c3ae7a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606416"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Hantera OneDrive-integrering med Business Central 
Den här artikeln innehåller en översikt över vad en administratör kan göra som administratör för att styra OneDrive för företag-integrationen med [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] online kunder online kan dra nytta av automatisk integration, med inga ytterligare inställningar som krävs för att använda dessa funktioner. 

## <a name="minimum-requirements"></a>Minsta krav

* Varje användare måste ha en licens för [!INCLUDE[prod_short](includes/prod_short.md)] och OneDrive som en del av en Microsoft 365-plan.
* OneDrive måste ställas in för varje användare.

## <a name="governance"></a>Styrelse
Administrationscentret för SharePoint ger omfattande kontroll över principer som styr användningen av OneDrive organisationen. Globala administratörer eller användare med rollen SharePoint administratör kan konfigurera principer som avgör vem som har åtkomst till OneDrive, varifrån data finns, livscykeln för innehåll och mycket mer. Följande länkar ger information om ofta använda funktioner och inställningar som kan förbättra integrationen med [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Hantera delningsinställningar](/sharepoint/turn-external-sharing-on-or-off)
* [Använda informationshinder med SharePoint](/sharepoint/information-barriers)
* [Lär dig mer om att förhindra dataförlust](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Ange standard lagringsutrymme för OneDrive användare](/onedrive/set-default-storage-space)
* [Lägga till och ta bort administratörer för en användaresOneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Inaktivera OneDrive skapande av vissa användare](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Flera geografiska funktioner i OneDrive och SharePoint online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Vissa funktioner kan vara tillgängliga endast för vissa scheman.

## <a name="managing-privacy"></a>Hantera sekretess
Administratörer och slutanvändare styr innehållet som lagras i OneDrive, och dessa data ägs uteslutande av din organisation. Mer information finns i [så här skyddar SharePoint och OneDrive data i molnet](/sharepoint/safeguarding-your-data). Du kan också besöka vår [Sekretesspolicy för Microsoft](https://privacy.microsoft.com/en-us/privacystatement), som förklarar vilka data Microsoft behandlar, hur Microsoft behandlar den och för vilka ändamål.

## <a name="restoring-onedrive-and-prod_short"></a>Återställa OneDrive och [!INCLUDE[prod_short](includes/prod_short.md)]
Som en del av en katastrofåterställning kan administratörer behöva återställa en [!INCLUDE[prod_short](includes/prod_short.md)] miljö till en säkerhetskopia från en tidpunkt som redan har passerat och synkronisera OneDrive lagringen till samma tidpunkt. OneDrive tillhandahåller olika verktyg, t.ex. att återställa en användares OneDrive till en tidigare tidpunkt, återställa en tidigare version av en enskild fil eller återställa borttagna filer. Mer information finns i följande artiklar:

* För [!INCLUDE[prod_short](includes/prod_short.md)], se [återställa en miljö i administrationscentret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* För OneDrive, se [återställa dina OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Konfigurera Business Central lokalt

En administratör måste upprätta anslutningen mellan [!INCLUDE[prod_short](includes/prod_short.md)] lokalerna och OneDrive. Till skillnad från [!INCLUDE[prod_short](includes/prod_short.md)] online är anslutningen inte automatisk. Om anslutningen inte är konfigurerad kan användarna inte använda funktionerna OneDrive. 

[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan endast kopplas till OneDrive som finns i Microsoft i molnet. Anslutning till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till lagringsplatsen mina webbplatser för SharePoint server stöds inte.

> [!IMPORTANT]
> Genom att konfigurera den här funktionen kan du också aktivera äldre funktioner som skickar filer till OneDrive.  
>
>* Excel-filen kopieras automatiskt till funktionen öppna i Excel till OneDrive och sedan öppnas den i Excel Online. 
>* När du exporterar en rapport till en fil kopieras filen automatiskt till OneDrive och sedan öppnas den i Excel Online, Word Online eller OneDrive. 
>* Andra funktioner kan också öppnas automatiskt i OneDrive.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>För att förbereda [!INCLUDE[prod_short](includes/prod_short.md)] lokal för anslutning till OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Lägg till ett registrerat program för Business Central i din Azure AD klientorganisation av Microsoft 365-abonnemang. Precis som andra Azure-tjänster som arbetar med Business Central kräver OneDrive en appregistrering för Azure Active Directory i (Azure AD). Programregistreringen tillhandahåller autentisering och autentiseringstjänster mellan Business Central och SharePoint som används av OneDrive.

Konfigurera det registrerade programmet med följande delegerade behörigheter till SharePoint API:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Det här fungerar i Azure-portalen. Kontrollera att du kopierar det program-ID (klient) och den klienthemlighet som används av det registrerade programmet. Du behöver informationen i nästa uppgift.

Mer information om hur du registrerar ett program och konfigurerar behörigheter finns i [Registrera ett program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) i hjälpen för utvecklare och IT-proffs.

> [!TIP]
> Om du redan har registrerat ett program som en del av en integration med en annan Microsoft-produkt, till exempel Power BI, kan du återanvända programregistreringen. Om så är fallet behöver du bara ange SharePoint behörigheterna.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Så här konfigurerar du anslutningen i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Microsoft SharePoint Konfiguration av inställningen** och väljer sedan relaterad länk.
2. I fältet **Beskrivning** anger du en beskrivning för anslutningen som **OneDrive**.
3. I fältet **Mapp** anger du **Business Central**.
4. I fältet **Plats** anger du URL för din OneDrive.

    URL:en för en OneDrive har vanligtvis följande format: `https://<tenant name>-my.sharepoint.com`. Mer information finns i [OneDrive URL:er för användare i organisationen ](/onedrive/list-onedrive-urls) i OneDrive dokumentationen.
5. I fältet **klient-ID** anger du klient-ID:t från programregistreringen.
6. I fältet **klienthemlighet** anger du hemligheten från programregistreringen. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> Sidan SharePoint anslutningsinställningar används för att konfigurera flera äldre funktioner. I avsnittet **Allmänt** konfigureras anslutningen till OneDrive och avsnittet **Delade dokument** dirigerar om filer till SharePoint i stället. Äldre SharePoint funktion kommer att vara inaktuell i en snar framtid. Vi rekommenderar att du inte konfigurerar avsnittet **delade dokument**.

## <a name="see-also"></a>Se även
[Business Central och OneDrive för företag-integration](across-onedrive-overview.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)

