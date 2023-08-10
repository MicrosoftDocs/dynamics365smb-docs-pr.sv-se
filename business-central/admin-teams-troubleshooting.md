---
title: Felsöka Microsoft Teams-integrering
description: Lär dig vad du kan göra som administratör för att styra Microsoft Teams-integreringen.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 10/01/2021
ms.author: jswymer
---

# <a name="troubleshooting-microsoft-teams-integration-with-"></a>Felsöka Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

I den här artikeln finns information om hur du identifierar och åtgärdar problem som kan uppstå när du använder Microsoft Teams med [!INCLUDE [prod_short](includes/prod_short.md)] som en typisk användare eller administratör.

## <a name="the-sign-in-link-doesnt-work"></a>Inloggningslänken fungerar inte

Om du försöker logga in på [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams direkt efter att du installerat appen och inloggningslänken inte reagerar, kan det bero på att appen inte har slutfört installationen helt. Du kan försöka åtgärda problemet genom att logga ut från Teams-klienten och sedan logga in igen.

## <a name="the-settings-page-is-empty"></a>Sidan Inställningar är tom.

Du måste först logga in för att komma åt dina inställningar. Om du vill logga in på appen kan du antingen klistra in en länk till en [!INCLUDE [prod_short.md](includes/prod_short.md)]-post eller söka efter kontakter. Båda dessa åtgärder kommer att leda dig genom en inloggningsupplevelse, där du kan använda sidan **Inställningar**.

## <a name="i-changed-company-but-it-didnt-seem-to-work"></a>Jag ändrade företaget, men det verkar inte fungera

När du har ändrat företaget på sidan **Inställningar** kanske du märker att du fortfarande söker i det föregående företaget. Problemet uppstår när du öppnar sidan **Inställningar** direkt från kommandorutan. I det här fallet har företaget ändrats och du kommer i praktiken att söka i det företag som du har växlat till. Problemet är att den nedrullningsbara kommando rutan inte har uppdaterats ännu. För att den nedrullningsbara listen ska motsvara det företag som du ska söka i, stänga eller ta bort [!INCLUDE [prod_short.md](includes/prod_short.md)] från kommandorutan och sedan öppna appen igen.


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts"></a>"Något gick fel" visas vid sökning efter kontakter

Det här felet kan uppstå när du söker i ett företag som inte har initierats eller inte svarar. Du kan till exempel inte söka i ett nytt testföretag som ännu inte accepterat användningsvillkoren. Lös problemet genom att logga in på [!INCLUDE [prod_short.md](includes/prod_short.md)] webbklienten och arbeta på eller stänga alla dialogrutor som visas.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a>Felmeddelandet "Det gick inte att hitta kontakt-/kontaktsammanfattnings-API" visas vid sökning efter kontakter

Det här problemet kan orsakas av anpassningar eller branschlösningar som påverkar eller ändrar [!INCLUDE [prod_short.md](includes/prod_short.md)] eller inte tillhandahåller en kontakt- eller kontaktsammanfattnings-API. Kontakta administratören eller supportpartnern om problemet kvarstår.

## <a name="none-of-my-links-expand-into-a-card"></a>Ingen av länkarna expanderas till ett kort

Om du har drabbats av det här problemet kan du göra följande:

1. Kontrollera först att [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams har installerats.

    Logga in på den stationära Teams-appen eller Teams i webbläsaren för att utföra kontrollen. Välj sedan **Appar** på den vänstra sidan och sök efter **[!INCLUDE [prod_short](includes/prod_short.md)]**. När du hittar appen **[!INCLUDE [prod_short](includes/prod_short.md)]** markerar du den för att öppna sidan med programinformation. Om knappen **Lägg till för mig** visas har appen [!INCLUDE [prod_short](includes/prod_short.md)] inte installerats. Mer information om hur du installerar appen finns i [Installera appen [!INCLUDE [prod_short](includes/prod_short.md)] för Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gästanvändare kan inte installera appar omedelbart. Mer information om gästanvändare finns i våra Vanliga frågor och svar om samarbete med gäster. 

2. Kontrollera sedan att du har loggat in med rätt identitet.

    Gå till valfri chatt i Teams och under meddelanderutan högerklickar du på ikonen [!INCLUDE [prod_short](includes/prod_short.md)] och väljer sedan **Inställningar**. När fönstret visas kontrollerar du om användaren det står att du är ansluten som matchar vad du använder för att ansluta till [!INCLUDE [prod_short](includes/prod_short.md)].

3. Se till att codeunit 2718 **Leverantör av sidsammanfattning** publiceras som en webbtjänst.

    Teams ansluter till [!INCLUDE [prod_short](includes/prod_short.md)] med hjälp av en slutpunkt till denna codeunit på tjänsten [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

4. Din organisation kan också begränsa dig från att klistra in länkar som utökas till kort. Kontakta administratören för att ta reda på vilka organisationspolicyer för Teams som kan gälla för dig.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Länken utökas ibland inte till ett kort

En länk utökas inte till ett kort i följande situationer:

- Länken riktar sig till en sida som (på teknisk nivå) inte är kopplad till en källtabell i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollera om sidtypen har en källtabell med hjälp av sidgranskningsfönstret i webbklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information om sidgranskning finns i [Inspektera sidor](across-inspect-page.md).
- Teams stöder inte förhandsgranskning av länkar i vissa funktioner. När du t. ex. visar en chatt eller är gäst till en annan organisation.
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

Ändringar som du gör i ett fält i informationsfönstret sparas automatiskt när du lämnar fältet. Innan du stänger fönstret när du har ändrat ett fält måste du se till att trycka på <kbd>tabb</kbd>-tangenten eller klicka/trycka utanför fältet.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>En ny panel dök upp i startprogrammet. Hur tar jag bort den?

När du visar dina appar på startsidan för Office 365 (https://home.office.com) eller i startprogrammet, visas en ny panel kallad "Tjänsteanslutning för Business Central Teams-integrering" när du har installerat appen [!INCLUDE [prod_short](includes/prod_short.md)] för Teams. Denna panel har inget värde i sig och kan döljas utan risk.

Som administratör med Azure Active Directory-administratörsbehörighet kan du dölja panelen genom att utföra följande steg:

1. Logga in på administrationscentret för [Azure Active Directory](https://aad.portal.azure.com/).
2. Välj **Företagsappar** och välj sedan **Tjänsteanslutning för Business Central Teams-integrering**.
3. Välj **Egenskaper** och ställ sedan in växeln **Synlig för användare** som **Nej**.
4. Välj **Spara**.

> [!NOTE]
> Det kommer att ta ett tag innan denna förändring träder i kraft.

## <a name="duplicate-text-in-the-share-to-teams-window"></a>Duplicera text i fönstret Dela till Teams

När du klistrar in text i meddelanderutan i fönstret **Dela till Teams**, dupliceras texten. Det här problemet är känt för Microsoft och kommer att åtgärdas i en senare uppdatering. 

## <a name="unable-to-sign-into-the-share-to-teams-window"></a>Det gick inte att logga in i fönstret Dela till Teams

Problemet kan bero på olika orsaker. Till exempel måste den identitet som du använder för att logga in ha åtkomst till Microsoft Teams, till exempel en Microsoft 365-prenumeration.

## <a name="my-cards-no-longer-have-a-popout-button"></a>Mina kort har inte längre någon popout-knapp

Från och med april 2022 kommer länkar som visas som kompaktkort i Teams inte längre att innehålla knappen **Popout**. Om du vill öppna detta kort i dess eget fönster väljer du knappen **Detaljer** och sedan **Öppna i webbläsare** i ellipsmenyn (**...**) i fönstrets övre högra hörn.

## <a name="cant-pin-a-card-to-tab"></a>Det går inte att fästa kort på fliken

Det finns några orsaker till detta problem.

- Om kortet delades från sök ME kan du inte fästa det på en flik. 

- Det går inte att fästa förrän du har lagt till fliken Business Central. Det här problemet är känt i Teams. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a>Någon har lagt till en flik, men fliken visas inte för mig

Problemet beror på att du inte har installerat BC-appen för Teams. Endast de med appen installerade kommer att se de flikarna i Business Central.

## <a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a>Andra ser annan sorterings- eller kolumnlayout än vad som författaren ser

Problemet beror förmodligen på att du har delat en listvy som är en personlig vy. I det här fallet måste du arbeta med administratören för att skapa rollbaserade listvyer som täcker de olika rollerna i kanalen/chatten, eller skapa vyn för hela organisationen så att alla kan få en enhetlig vy.


## <a name="see-also"></a>Se även

[Integreringsöversikt för [!INCLUDE [prod_short](includes/prod_short.md)] och Microsoft Teams](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams](across-search-contacts-teams.md)  
[Dela poster i Microsoft Teams](across-working-with-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Ändra företag och andra inställningar i Teams](across-teams-settings.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
