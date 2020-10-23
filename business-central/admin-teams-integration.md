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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989364"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Hantera Microsoft Teams-integrering med Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Den här artikeln innehåller en översikt över vad du kan göra som administratör för att styra Microsoft Teams-integrationen med [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minsta krav

I det här avsnittet beskrivs minimikraven för att [!INCLUDE [prodshort](includes/prodshort.md)]-appen ska fungera i Team.

- Nödvändiga licenser

    I den här tabellen får du en översikt över de licenser som behövs för att [!INCLUDE [prodshort](includes/prodshort.md)]-appen ska fungera i Team.

    |Vad|Team-licens|Business Central-licens|
    |----|---|---|
    |Klistra in en länk till en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en konversation och skicka den som ett kort.|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|
    |Visa ett kort i en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en konversation.|![bock](media/check.png "kontroll")||
    |Visa mer information för ett kort i en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en konversation.|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|

- Tillåt förhandsgranskning av URL

    Principinställningen **Tillåt förhandsgranskning av URL** måste vara på. Annars kan ett kort inte genereras för Business Central-länkar som klistrats in i en Team-konversation. Mer information om den här inställningen finns i [Hantera meddelandeprinciper i Team](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Hantera Business Central-appen (valfritt)

Som Team-administratör kan du hantera alla appar för organisationen, inklusive [!INCLUDE [prodshort](includes/prodshort.md)]-appen. Du kan godkänna eller installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen för organisationen, hindra användare från att installera appen med mera.

Mer information finns i följande artiklar i Microsoft Teams-dokumentationen:

- [Hantera dina appar i Microsoft Teams administratörscenter](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Hantera principer för appkonfiguration i Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>I [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Minsta krav

- [!INCLUDE [prodshort](includes/prodshort.md)]-version:

    [!INCLUDE [prodshort](includes/prodshort.md)] utgivningscykel 2 år 2020 (version 17) eller senare. Team-integration stöds endast för [!INCLUDE [prodshort](includes/prodshort.md)] online, inte lokalt.

- Codeunit **2718 sidan sammanfattning leverantör** är publicerad som en webbtjänst:

    Denna codeunit publiceras som en webbtjänst som standard. Denna codeunit ingår i [!INCLUDE [prodshort](includes/prodshort.md)]-systemprogrammet. Den används för att hämta fältdata för en [!INCLUDE [prodshort](includes/prodshort.md)]-sida som har lagts till i en Team-konversation. 

- Användarbehörigheter:

    De sidor och data som användare kan visa och redigera i en Team-konversation styrs oftast av deras behörighet i [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Om du vill klistra in en [!INCLUDE [prodshort](includes/prodshort.md)]-länk i en Team-konversation och låta den utökas till ett kort måste användarna åtminstone ha läsbehörighet på sidan och dess data.
    - När ett kort har skickats till en konversation kan alla användare i konversationen se det kortet utan behörighet till Business Central.
    - Om du vill visa mer information om ett kort eller öppna posten i [!INCLUDE [prodshort](includes/prodshort.md)] måste användarna ha läsbehörighet på sidan och dess data.
    - Användare måste ändra behörigheter för att kunna ändra data.
    
    Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

## <a name="see-also"></a>Se även
[Översikt över Business Central- och Microsoft Teams-integrering](across-teams-overview.md)  
[Installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Utveckling för Team-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Komma igång](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
