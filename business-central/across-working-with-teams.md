---
title: Dela Business Central-poster i Microsoft Teams
description: Lär dig att använda Business Central-appen för Microsoft Teams.
author: jswymer
ms.topic: how-to
ms.service: dynamics365-business-central
ms.reviewer: jswymer
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 16/18/2023
ms.author: jswymer
ms.custom: bap-template
---

# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams" />Dela Business Central-poster och sidlänkar i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] erbjuder ett par sätt att dela data från Business Central direkt i en Microsoft Teams konversation:

<!-- 
## <a name="overview" />Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Med [!INCLUDE [prod_short](includes/prod_short.md)] appen installerad i Teams kan du inkludera ett interaktivt visitkort med Business Central i en Teams-konversation.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Med eller utan [!INCLUDE [prod_short](includes/prod_short.md)] appen installerad kan du dela en länk från sidor i Business Central till ett Teams-samtal.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

Följande avsnitt beskriver de olika sätten i detalj.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation" />Inkludera och visa ett Business Central-kort i en Teams-konversation

Med Business Central-appen för Teams kan du kopiera en länk från valfri Business Central-post, till exempel en kund- eller försäljningsorder, och klistra in länken i en Teams-konversation. Appen ansluter Microsoft Teams till dina affärsdata i [!INCLUDE [prod_short](includes/prod_short.md)]\. Det utökar sedan länken ett kompakt, interaktivt kort som visar information om posten. När ni väl befinner er i konversationen kan du och dina medarbetare visa mer information om posten, redigera data och vidta åtgärder &mdash; utan att lämna Teams.

[![Team-integrering med Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites" />Förutsättningar

- Du har tillgång till Microsoft Teams.
- Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Team. Mer information finns i [Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Alla deltagare i en Team-konversation kommer att kunna se kort för Business Central-poster som du skickar till konversationen. Men för att visa mer information om poster med hjälp av knapparna **Detaljer** eller **Öppna** på ett kort, behöver de tillgång till [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Hantera Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation" />Ta med ett Business Central-kort i en Team-konversation

1. Logga in på [!INCLUDE [prod_short](includes/prod_short.md)] genom webbläsaren.
2. Öppna posten som du vill dela.

    Appen är utformad för att visa ett kort för i stort sett samtliga typer av [!INCLUDE [prod_short](includes/prod_short.md)]-sidor. Den ger emellertid den bästa upplevelsen när den används för sidor som visar en enskild post, till exempel en artikel, kund eller försäljningsorder.
3. Kopiera länken till sidan.

    Du kan kopiera länken på två sätt: Det enklaste och bästa sättet är att välja **Dela** ![ikonen Dela i Business Central](media/share-icon.png) > **Kopiera länk**. Deta andra sättet är att kopiera hela URL-adressen från webbläsarens adressfält.

    [![Kopiera URL-adress för Business Central från webbläsare.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Gå till Team och starta en konversation, som kan vara chatt med en person, en grupp personer eller en teamkanal.
5. Klistra in länken (URL-adressen) i meddelanderutan där du skriver ett meddelande.

    ![Klistra in Business Central-URL i Team.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Om du får ett meddelande som: *Busines Central vill visa en förhandsgranskning av den här länken* betyder det att du inte har installerat Business Central-appen för Teams. Om du vill installera appen väljer du **Visa förhandsgranskning** och följer instruktionerna.

    > [!NOTE]
    > Beroende på din Business Central-version, första gången du klistrar in en länk i en konversation blir du kanske ombedd att logga in på [!INCLUDE [prod_short](includes/prod_short.md)] och ge appen tillstånd att hämta data. Följ bara instruktionerna på skärmen. Du behöver bara göra detta steg en gång.
6. Vänta ett tag medan ett kort genereras i meddelanderutan.
7. När kortet visas granskar du innehållet på kortet noggrant för känslig information innan du skickar meddelandet. Det här steget är viktigt eftersom alla i konversationen kan se kortet när du har skickat meddelandet.
8. Om kortet verkar vara bra väljer du **Skicka** för att skicka det till konversationen.

    > [!TIP]
    > När kortet visas och innan du väljer **Skicka** kan du ta bort den inklistrade URL:en om du vill.
9. Om du vill visa mer information om eller ändra den post somvisas på kortet väljer du **Detaljer**. Mer information finns i nästa avsnitt.

### <a name="view-card-details" />Visa kortinformation

När ett kort har skickats till en konversation kan alla deltagare med [rätt behörighet](admin-teams-integration.md#permissions) välja **Detaljer** för att öppna ett fönster som visar mer information om posten &mdash; och eventuellt ändra posten. Det spelar ingen roll om du är den som skickar kortet eller den som tar emot det. Funktionen **Detaljer** är särskilt användbar för mottagare eftersom den snabbt förser dem med koncis, riktad information om posten.

Informationsfönstret liknar det som du ser i [!INCLUDE [prod_short](includes/prod_short.md)], men är fokuserat på sidan eller posten som kortet handlar om. När du är klar med att visa och göra ändringar kan du stänga fönstret och återgå till Team-konversationen.

Här följer några saker som du bör tänka på när du arbetar med kortinformationen:

- För att kunna öppna kortinformationen måste en användare ha behörighet till sidan och dess data i [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Korten i Teams-chattar uppdateras inte automatiskt till ändringar. Ändringar som du sparar i en post i informationsfönstret sparas i [!INCLUDE [prod_short](includes/prod_short.md)]\. Kortet i Teams visar emellertid inte ändringarna i konverteringen förrän du klistrar in länken igen.

Mer information om hur du arbetar med kort och kortinformation finns i [Vanliga frågor och svar om Teams](teams-faq.md).

## <a name="share-a-link-to-page-from-business-central-to-teams" /><a name="share-link"></a>Dela en länk till sidan i Business Central till Teams

Direkt från de flesta samlingssidor, på samma sätt som på **Artiklar** sida och detaljsidor, som kort **Artiklar** du kan skicka en länk till sidan till specifika mottagare i en Teams-konversation. Du kan t.ex. dela en länk till en filtrerad vy över posterna. Mottagarna kan sedan markera länken så att sidan öppnas i [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![!Menyn Dela visas på ett kort.](media/teams-share-link-v2.png "Menyn Dela visas på ett kort.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites-1" />Förutsättningar

- Du har tillgång till Microsoft Teams.
- (Valfritt) Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. 

  Med appen installerad kommer även de meddelanden du skickar med länken att innehålla ett kompakt kort för sidan. Mer information om hur du installerar appen finns i [Installera appen [!INCLUDE [prod_short](includes/prod_short.md)] för Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link" />Dela en länk

1. I [!INCLUDE [prod_short](includes/prod_short.md)]\, öppna sidan som du vill dela.
2. Välj det du vill ha högst upp på sidan ![Åtgärden dela till andra program på sidor.](media/share-icon.png) sedan **dela med Teams**.
3. Logga in på Teams med ditt användarnamn och lösenord om du uppmanas till det.
4. I sidan **Delat till Teams**, skriv ett namn på en person, grupp eller kanal som du vill skicka meddelandet till.
5. Meddelanderutan innehåller en länk till sidan. Om [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams är installerad visas även ett kort för den länkade posten eller sidan i meddelanderutan.

   Lägg till mer information om du vill, välj sedan **Dela**.
6. Länken har nu delats. Om du vill gå till konversationen väljer du **gå till Teams**.

## <a name="see-also" />Se även

[Översikt över Business Central- och Microsoft Teams-integrering](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams](across-search-contacts-teams.md)  
[Ändra företag och andra inställningar i Teams](across-teams-settings.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
