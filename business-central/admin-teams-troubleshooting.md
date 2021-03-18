---
title: Felsöka Microsoft Teams-integrering
description: Lär dig vad du kan göra som administratör för att styra Microsoft Teams-integreringen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 7a98b53a34ddf403cf6507da7740b97924d4c81c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385205"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Felsöka Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

I den här artikeln finns information om hur du identifierar och åtgärdar problem som kan uppstå när du använder Microsoft Teams med [!INCLUDE [prod_short](includes/prod_short.md)] som en typisk användare eller administratör.

## <a name="none-of-my-links-expand-into-a-card"></a>Ingen av länkarna expanderas till ett kort 

Om du har drabbats av det här problemet kan du göra följande:

1. Kontrollera först att [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams har installerats.

    Logga in på den stationära Teams-appen eller Teams i webbläsaren för att utföra kontrollen. Välj sedan **Appar** på den vänstra sidan och sök efter **[!INCLUDE [prod_short](includes/prod_short.md)]**. När du hittar appen **[!INCLUDE [prod_short](includes/prod_short.md)]** markerar du den för att öppna sidan med programinformation. Om knappen **Lägg till för mig** visas har appen [!INCLUDE [prod_short](includes/prod_short.md)] inte installerats. Mer information om hur du installerar appen finns i [Installera appen [!INCLUDE [prod_short](includes/prod_short.md)] för Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gästanvändare kan inte installera appar omedelbart. Mer information om gästanvändare finns i våra Vanliga frågor och svar om samarbete med gäster. 

2. Kontrollera sedan att du har loggat in med rätt identitet.

    Gå till valfri chatt i Teams och välj sedan ikonen [!INCLUDE [prod_short](includes/prod_short.md)] under meddelanderutan. När fönstret visas kontrollerar du om användaren det står att du är ansluten som matchar vad du använder för att ansluta till [!INCLUDE [prod_short](includes/prod_short.md)].

3. Se till att codeunit 2718 **Leverantör av sidsammanfattning** publiceras som en webbtjänst.

    Teams ansluter till [!INCLUDE [prod_short](includes/prod_short.md)] med hjälp av en slutpunkt till denna codeunit på tjänsten [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

4. Din organisation kan också begränsa dig från att klistra in länkar som utökas till kort. Kontakta administratören för att ta reda på vilka organisationspolicyer för Teams som kan gälla för dig.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Länken utökas ibland inte till ett kort 

En länk utökas inte till ett kort i följande situationer:

- Länken riktar sig till en sidtyp som inte representerar någon post. Det kan till exempel vara en länk till rollcentret för [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollera sidtypen med hjälp av sid granskningsfönstret i webbklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information om sidgranskning finns i [Inspektera sidor](across-inspect-page.md).
- Länken riktar sig till en sida som (på teknisk nivå) inte är kopplad till en källtabell i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollera om sidtypen har en källtabell med hjälp av sidgranskningsfönstret i webbklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information om sidgranskning finns i [Inspektera sidor](across-inspect-page.md). 
- Teams stöder inte förhandsgranskning av länkar i vissa funktioner. När du t. ex. visar en chatt, är på ett möte eller är gäst till en annan organisation.
- Teams överger tyst sina försök att visa kortet efter 15 sekunder, till exempel på grund av nätverksproblem.
- Teams expanderar eventuellt inte länken om du redan har klistrat in en länk i samma meddelanderuta och tagit bort kortet.

Länken måste också innehålla all nödvändig information för att posten ska kunna hittas och visa motsvarande kort. Denna information omfattar:

- Miljönamnet, genom att inkludera det i URL-sökvägen. Om du inte anger miljönamnet antar Teams att du försöker nå miljön kallad "Produktion".
- Företagsnamnet, genom att använda parametern *company=*
- Sididentifieraren, genom att använda parametern *page=*
- Bokmärket till posten, genom att använda parametern *bokmärke=*

Som exempel:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

För teknisk information om [!INCLUDE [prod_short](includes/prod_short.md)]-URL-adresser, se [Webbklientens URL-adress](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) i [!INCLUDE [prod_short](includes/prod_short.md)]-hjälpen för utvecklare och IT-proffs.

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>Kortet visas i meddelanderutan, men om du markerar knappen Detaljer händer ingenting 

När en länk expanderas till ett kort i meddelanderutan måste du skicka meddelandet till chatten innan du kan använda knappen **Dtaljer**.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Informationsfönstret öppnas, men visar ett fel innan informationen visas

Detta problem kan orsakas av ett antal olika saker: brist på behörighet i [!INCLUDE [prod_short](includes/prod_short.md)]- eller webbläsarinställningarna (när du använder Teams i webbläsaren).

1. Kontrollera din behörighet i [!INCLUDE [prod_short](includes/prod_short.md)].

    Om du vill visa information om ett kort kontrollerar [!INCLUDE [prod_short](includes/prod_short.md)] du licens och behörighet att visa just den posten och sidan i det specifika företaget och miljön. Om du inte har behörighet för något av detta, visas standardfelmeddelandena om behörighet för [!INCLUDE [prod_short](includes/prod_short.md)] i informationsfönstret. 

    Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)

2. Kontrollera dina webbläsarinställningar om du använder Teams i webbläsaren.

    - Webbläsarens popup-blockerare måste antingen vara avstängd eller inställd på att tillåta popup-fönster från domänerna *businesscentral.dynamics.com* eller *bc.dynamics.com*. Information om hur du tillåter popup-fönster för [!INCLUDE [prod_short](includes/prod_short.md)] finns i [Konfigurera webbläsaren](across-browser-settings.md#popup).
    - Webbläsaren måste ha åtkomst till lokal webbläsarlagring för cookies och inställningar när du arbetar.
    - Undvik att använda gäst- eller privat bläddring om detta inte är absolut nödvändigt, detta eftersom dessa typer av bläddring ignorerar eller blockerar visst innehåll i vissa webbläsare.

    Mer information om minimikraven för webbläsare finns i [Minimikrav för användning av [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Jag har problem med kameran eller platsen i Teams 

När du använder [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner i informationsfönstret som kräver åtkomst till din plats eller din enhets kamera, måste du först ge Teams åtkomst till dessa enhetsfunktioner.  

- För Teams i webbläsaren måste du se till att webbläsarinställningarna ger https://teams.microsoft.com åtkomst till kamera och plats. 

- För Teams för iOS eller Android måste du se till att enhetsinställningarna ger åtkomst till kamera och plats för Teams-mobilappen. 

Mer information om hur du ändrar dessa inställningar finns i [Min kamera fungerar inte i Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) på Microsoft Support.

[!INCLUDE [prod_short](includes/prod_short.md)]-appen stöder inte platsindikering i den stationära Teams-appen. Mer information om platser finns i [Vanliga frågor och svar om Teams](teams-faq.md#location).

Vissa webbläsare, t. ex nya Microsoft Edge, gör att du kan välja vilken kamera som ska användas när enheten har stöd för flera kameror. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams visar blandade språk för mina kort och kortuppgifter

För att kort och kortinformation ska kunna visas konsekvent på samma språk i Teams måste språket i din Teams-klient stämma överens med det språk som du använder i [!INCLUDE [prod_short](includes/prod_short.md)]-webbklienten.

- Information om hur du byter språk i Teams finns i [Ändra inställningar i Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) på Microsoft Support. 

- Mer information om hur du byter språk i [!INCLUDE [prod_short](includes/prod_short.md)]finns i avsnittet [Ändra grundläggande inställningar – Språk](ui-change-basic-settings.md#language).

Mer information om hur språk fungerar mellan Teams och [!INCLUDE [prod_short](includes/prod_short.md)] finns i [Vanliga frågor och svar om Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Jag har redigerat ett fält i informationsfönstret, men ändringen sparades inte

Ändringar som du gör i ett fält i informationsfönstret sparas automatiskt när du lämnar fältet. Innan du stänger fönstret när du har ändrat ett fält måste du se till att trycka på tabbtangenten eller klicka/trycka utanför fältet.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>En ny panel dök upp i startprogrammet. Hur tar jag bort den?

När du visar dina appar på startsidan för Office 365 (https://home.office.com) eller i startprogrammet, visas en ny panel kallad "Tjänsteanslutning för Business Central Teams-integrering" när du har installerat appen [!INCLUDE [prod_short](includes/prod_short.md)] för Teams. Denna panel har inget värde i sig och kan döljas utan risk.

Som administratör med Azure Active Directory-administratörsbehörighet kan du dölja panelen genom att utföra följande steg:

1. Logga in på administrationscentret för [Azure Active Directory](https://aad.portal.azure.com/).
2. Välj **Företagsappar** och välj sedan **Tjänsteanslutning för Business Central Teams-integrering**.
3. Välj **Egenskaper** och ställ sedan in växeln **Synlig för användare** som **Nej**.
4. Välj **Spara**.

> [!NOTE]
> Det kommer att ta ett tag innan denna förändring träder i kraft.


## <a name="see-also"></a>Se även

[Integreringsöversikt för [!INCLUDE [prod_short](includes/prod_short.md)] och Microsoft Teams](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Utveckling för Team-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]