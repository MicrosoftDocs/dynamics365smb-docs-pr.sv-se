---
title: Arbeta med Business Central-data i Microsoft Teams| Microsoft Docs
description: Lär dig att använda Business Central-appen för Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989433"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbeta med Business Central-data i Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] erbjuder en app som ansluter Microsoft Teams till dina affärsdata i [!INCLUDE [prodshort](includes/prodshort.md)], så att du snabbt kan dela information mellan teammedlemmar och reagera snabbare på frågor. I den här artikeln lär du dig hur du använder appen för att dela [!INCLUDE [prodshort](includes/prodshort.md)]-data med kollegor i en Team-konversation.

## <a name="overview"></a>Översikt

I [!INCLUDE [prodshort](includes/prodshort.md)]-appen kan du:

- Kopiera en länk till en Business Central-post och klistra in den i en Team-konversation så att den kan delas med dina medarbetare. Länken leder till ett kompakt, interaktivt kort som visar information om posten.
- När du har gått igenom konversationen kan du och dina medarbetare visa mer information om posten, redigera data och utföra åtgärder utan att lämna Team.

[![Team-integrering med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Förutsättningar

- Du har tillgång till Microsoft Teams.
- Du har installerat [!INCLUDE [prodshort](includes/prodshort.md)]-appen i Team. Mer information finns i [Installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Alla deltagare i en Team-konversation kommer att kunna se kort för Business Central-poster som du skickar till konversationen. Men om du vill visa mer information om poster med hjälp av knapparna **Detaljer** eller **Öppna i nytt fönster** på ett kort måste du ha tillgång till [!INCLUDE [prodshort](includes/prodshort.md)]. Mer information finns i [Hantera Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Ta med ett Business Central-kort i en Team-konversation

1. Logga in på [!INCLUDE [prodshort](includes/prodshort.md)] genom webbläsaren.
2. Öppna posten som du vill dela.

    Appen är utformad för att visa sidor med korttypen från [!INCLUDE [prodshort](includes/prodshort.md)]. Öppna en sida som visar en enskild post, t.ex. en artikel, kund eller försäljningsorder. Du kan inte använda den för rollcenter eller sidor som visar flera poster i en lista.

3. Kopiera hela URL-adressen från webbläsarens adressfält.

   ![Kopiera URL-adress för Business Central från webbläsare](media/teams-url.png)
4. Gå till Team och starta en konversation, som kan vara chatt med en person, en grupp personer eller en teamkanal.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Klistra in URL-adressen i rutan där du lägger till ett meddelande.

   ![Klistra in Business Central-URL i Team](media/teams-paste-url.png)
6. Första gången du klistrar in en länk i en konversation ombeds du logga in på [!INCLUDE [prodshort](includes/prodshort.md)] och ge appen tillstånd att hämta data. Följ bara instruktionerna på skärmen.

    > [!NOTE]
    > Du behöver bara utföra detta steg en enda gång.

7. Vänta ett tag medan ett kort genereras i meddelanderutan.

8. När kortet visas granskar du innehållet på kortet noggrant för känslig information innan du skickar meddelandet. Det här steget är viktigt eftersom alla i konversationen kan se kortet när du har skickat meddelandet.

9. Om kortet verkar vara bra väljer du **Skicka** för att skicka det till konversationen.

    > [!TIP]
    > När kortet visas och innan du väljer **Skicka** kan du ta bort den inklistrade URL:en om du vill.

10. Om du vill visa information om eller ändra posten väljer du **Detaljer**.

    Sidan Detaljer liknar det du ser i [!INCLUDE [prodshort](includes/prodshort.md)]. Men informationen är något nedtrimmad för Team. När du är klar med att visa och göra ändringar kan du stänga fönstret och återgå till Team-konversationen.

    > [!NOTE]
    > Alla ändringar som du gör återspeglas på kortet tills nästa gång du klistrar in länken i en konversation.

## <a name="see-also"></a>Se även

[Översikt över Business Central- och Microsoft Teams-integrering](across-teams-overview.md)  
[Installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Utveckling för Team-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Komma igång](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
