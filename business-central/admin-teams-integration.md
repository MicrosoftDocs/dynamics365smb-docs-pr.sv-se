---
title: Hantera Microsoft Teams-integrering med Business Central| Microsoft Docs
description: Hantera Business Central-integrering med Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 2d86e96b1778df47f0ead9845e2585905087adae
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046486"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Hantera Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Den här artikeln innehåller en översikt över vad du kan göra som administratör för att styra Microsoft Teams-integrationen med [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minsta krav

I det här avsnittet beskrivs minimikraven för att [!INCLUDE [prod_short](includes/prod_short.md)]-appen ska fungera i Team.

- Nödvändiga licenser

    I den här tabellen får du en översikt över de licenser som behövs för att [!INCLUDE [prod_short](includes/prod_short.md)]-appen ska fungera i Team.

    |Vad|Team-licens|[!INCLUDE [prod_short](includes/prod_short.md)]-licens|
    |----|---|---|
    |Klistra in en länk till en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en konversation och skicka den som ett kort.|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|
    |Visa ett kort i en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en konversation.|![bock](media/check.png "kontroll")||
    |Visa mer information för ett kort i en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en konversation.|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|

- Tillåt förhandsgranskning av URL

    Principinställningen **Tillåt förhandsgranskning av URL** måste vara på. I annat fall kan ett kort inte genereras för [!INCLUDE [prod_short](includes/prod_short.md)]-länkar som klistrats in i en Teams-konversation. Mer information om den här inställningen finns i [Hantera meddelandeprinciper i Team](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Hantera [!INCLUDE [prod_short](includes/prod_short.md)]-appen (valfritt)

Som Team-administratör kan du hantera alla appar för organisationen, inklusive [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Du kan godkänna eller installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för organisationen, hindra användare från att installera appen med mera.

Mer information finns i följande artiklar i Microsoft Teams-dokumentationen:

- [Hantera dina appar i Microsoft Teams administratörscenter](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Hantera principer för appkonfiguration i Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>I [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Minsta krav

- [!INCLUDE [prod_short](includes/prod_short.md)]-version:

    [!INCLUDE [prod_short](includes/prod_short.md)] utgivningscykel 2 år 2020, uppdatering 17.3 eller senare. Team-integration stöds endast för [!INCLUDE [prod_short](includes/prod_short.md)] online, inte lokalt.

- Codeunit **2718 sidan sammanfattning leverantör** är publicerad som en webbtjänst:

    Denna codeunit publiceras som en webbtjänst som standard. Denna codeunit ingår i [!INCLUDE [prod_short](includes/prod_short.md)]-systemprogrammet. Den används för att hämta fältdata för en [!INCLUDE [prod_short](includes/prod_short.md)]-sida som har lagts till i en Team-konversation. Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

- <a name="permissions"></a>Användarbehörigheter:

    De sidor och data som användare kan visa och redigera i en Team-konversation styrs oftast av deras behörighet i [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - Om du vill klistra in en [!INCLUDE [prod_short](includes/prod_short.md)]-länk i en Team-konversation och låta den utökas till ett kort måste användarna åtminstone ha läsbehörighet på sidan och dess data.
    - När ett kort har skickats till en konversation kan alla användare i konversationen se det kortet utan behörighet till [!INCLUDE [prod_short](includes/prod_short.md)].
    - Om du vill visa mer information om ett kort eller öppna posten i [!INCLUDE [prod_short](includes/prod_short.md)] måste användarna ha läsbehörighet på sidan och dess data.
    - Användare måste ändra behörigheter för att kunna ändra data.
    
    Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Hantera sekretess och kompatibilitet 

Microsoft Teams innehåller omfattande kontroller för kompatibilitet och hantering av känsliga eller personligt identifierbara data  &mdash; inklusive data som lagts till i chattar och kanaler av [!INCLUDE [prod_short](includes/prod_short.md)]-appen.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Förstå var [!INCLUDE [prod_short](includes/prod_short.md)]-kort lagras 

När ett kort har skickats till en chatt kopieras kortet och de fält som visas på kortet till Teams. Denna information är underkastad Teams policyer för organisationen, till exempel policyer för bevarande av data. När kortinformation visas lagras ingen information i informationsfönstret i Teams. Informationen förblir lagrad i [!INCLUDE [prod_short](includes/prod_short.md)] och kommer bara att hämtas av Teams när användaren väljer att visa informationen. 

- Om du vill veta mer om var Teams lagrar data, se [Var informationen finns i Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Mer information om bevarandepolicyer i Teams finns i [Bevarandepolicyer i Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Begränsa delning av kort 

Du hindrar vissa användare eller grupper från att skicka kort till chattar eller kanaler genom att konfigurera meddelandepolicyer som inaktiverar inställningen **URL-förhandsgranskning**. Mer information om den här inställningen finns i [Hantera meddelandeprinciper i Team](/microsoftteams/messaging-policies-in-teams). 

Du kan också använda informationshinder för att förhindra att användare eller grupper kommunicerar med varandra. Mer information finns i [Informationshinder i Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funktionerna för dataförlustskydd i säkerhets- och efterlevnadscentret för Microsoft 365r kan inte användas specifikt för kort. De kan emellertid tillämpas på de chattmeddelanden som innehåller korten. Information om hur du spårar kommande avancerade funktioner som innefattar att aktivera DLP för kort finns i [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Svara på dataförfrågningar

Du tillåter gruppmedlemmar och gruppägare att ta bort meddelanden som innehåller känsliga kort genom att ställa in meddelandepolicye, t. ex. **Ägare kan ta bort skickade meddelanden** och **Användare kan ta bort skickade meddelanden**. Mer information finns i [Hantera meddelandepolicyer i Teams](/microsoftteams/messaging-policies-in-teams).

Funktionerna för innehållssökning och eDiscovery-efterlevnad i säkerhets- och efterlevnadscentret för Microsoft 365r kan inte tillämpas specifikt på kort. De kan emellertid tillämpas på de chattmeddelanden som innehåller korten. Information om hur du spårar de kommande funktionerna för regelefterlevnad för kort finns i [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Eftersom kortdata i Teams är en kopia av data i [!INCLUDE [prod_short](includes/prod_short.md)] kan du också använda [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner för att exportera en kunds data vid behov. Mer information om sekretess i [!INCLUDE [prod_short](includes/prod_short.md)] finns i avsnittet [Vanliga frågor och svar om sekretess för Business Central-kunder](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Se även
[Integreringsöversikt för [!INCLUDE [prod_short](includes/prod_short.md)] och Microsoft Teams](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]