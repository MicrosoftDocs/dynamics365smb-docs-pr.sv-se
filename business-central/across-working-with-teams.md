---
title: Dela Business Central-poster i Microsoft Teams
description: Lär dig att använda Business Central-appen för Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: fb134ce04cb6b53f2432f0f371d7ca82411f0cee
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444024"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a>Dela Business Central-poster i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] erbjuder en app som ansluter Microsoft Teams till dina affärsdata i [!INCLUDE [prod_short](includes/prod_short.md)], så att du snabbt kan dela information mellan teammedlemmar och reagera snabbare på frågor. I den här artikeln får du lära dig att använda appen för att dela [!INCLUDE [prod_short](includes/prod_short.md)]-poster, som en kund, försäljningsorder eller faktura, med kollegor i en Team-konversation.

## <a name="overview"></a>Översikt

I [!INCLUDE [prod_short](includes/prod_short.md)]-appen kan du:

- Kopiera en länk till en Business Central-post och klistra in den i en Teams-konversation så att den kan delas med dina medarbetare. Appen kommer sedan att utöka länken till ett kompakt, interaktivt kort som visar information om posten.
- När ni väl befinner er i konversationen kan du och dina medarbetare visa mer information om posten, redigera data och vidta åtgärder &mdash; utan att lämna Teams.

[![Team-integrering med Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Förutsättningar

- Du har tillgång till Microsoft Teams.
- Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Team. Mer information finns i [Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Alla deltagare i en Team-konversation kommer att kunna se kort för Business Central-poster som du skickar till konversationen. Men för att visa mer information om poster med hjälp av knapparna **Detaljer** eller **Öppna** på ett kort, behöver de tillgång till [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Hantera Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Ta med ett Business Central-kort i en Team-konversation

1. Logga in på [!INCLUDE [prod_short](includes/prod_short.md)] genom webbläsaren.
2. Öppna posten som du vill dela.

    Appen är utformad för att visa sidor med korttypen från [!INCLUDE [prod_short](includes/prod_short.md)]. Öppna en sida som visar en enskild post, t. ex. en artikel, kund eller försäljningsorder. Du kan inte använda den för rollcenter eller sidor som visar flera poster i en lista.

3. Kopiera hela URL-adressen från webbläsarens adressfält.

   ![Kopiera URL-adress för Business Central från webbläsare.](media/teams-url-v2.png)
4. Gå till Team och starta en konversation, som kan vara chatt med en person, en grupp personer eller en teamkanal.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Klistra in URL-adressen i meddelanderutan där du skriver ett meddelande.

   ![Klistra in Business Central-URL i Team.](media/teams-paste-url-v2.png)
6. Första gången du klistrar in en länk i en konversation ombeds du logga in på [!INCLUDE [prod_short](includes/prod_short.md)] och ge appen tillstånd att hämta data. Följ bara instruktionerna på skärmen.

    > [!NOTE]
    > Du behöver bara utföra detta steg en enda gång.

7. Vänta ett tag medan ett kort genereras i meddelanderutan.

8. När kortet visas granskar du innehållet på kortet noggrant för känslig information innan du skickar meddelandet. Det här steget är viktigt eftersom alla i konversationen kan se kortet när du har skickat meddelandet.

9. Om kortet verkar vara bra väljer du **Skicka** för att skicka det till konversationen.

    > [!TIP]
    > När kortet visas och innan du väljer **Skicka** kan du ta bort den inklistrade URL:en om du vill.

10. Om du vill visa mer information om eller ändra den post somvisas på kortet väljer du **Detaljer**. Mer information finns i nästa avsnitt.

## <a name="view-card-details"></a>Visa kortinformation

När ett kort har skickats till en konversation kan alla deltagare med [rätt behörighet](admin-teams-integration.md#permissions) välja **Detaljer** för att öppna ett fönster som visar mer information om posten &mdash; och eventuellt ändra posten. Det spelar ingen roll om du är den som skickar kortet eller den som tar emot det. Funktionen **Detaljer** är särskilt användbar för mottagare eftersom den snabbt förser dem med koncis, riktad information om posten, i stället för att behöva söka igenom hela posten.

Fönstret Detaljer liknar det du ser i [!INCLUDE [prod_short](includes/prod_short.md)] posten. Men informationen är något nedtrimmad för Team. När du är klar med att visa och göra ändringar kan du stänga fönstret och återgå till Team-konversationen.

Här följer några saker som du bör tänka på när du arbetar med kortinformationen:

- För att kunna öppna kortinformationen måste en användare ha behörighet till sidan och dess data i [!INCLUDE [prod_short](includes/prod_short.md)].
- Korten i Teams-chattar uppdateras inte automatiskt till ändringar. Ändringar som du sparar i en post i informationsfönstret sparas i [!INCLUDE [prod_short](includes/prod_short.md)]. Kortet i Teams visar emellertid inte ändringarna i konverteringen förrän du klistrar in länken igen.

Mer information om hur du arbetar med kort och kortinformation finns i [Vanliga frågor och svar om Teams](teams-faq.md).

## <a name="see-also"></a>Se även

[Översikt över Business Central- och Microsoft Teams-integrering](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams](across-search-contacts-teams.md)  
[Ändra företag och andra inställningar i Teams](across-teams-settings.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]