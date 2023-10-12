---
title: Söka efter kontakter från Microsoft Teams
description: 'Mer information om hur du upprättar Business Central kunder, leverantörer och andra kontakter från Microsoft Teams.'
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions'
ms.date: 04/12/2021
ms.author: jswymer
---

# Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]. Infört i 2021 utgivningscykel 1.

[!INCLUDE [prod_short](includes/prod_short.md)] har ett omfattande system för hantering av affärskontakt som är väsentligt för användare i försäljning, operationer eller andra avdelningsroller. Om du är en användare i en av dessa roller behöver du ofta slå upp, möta eller starta en konversation med leverantörerna, kunderna och andra kontakter. Med [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams kan du utföra de här uppgifterna direkt från Teams utan att behöva växla till [!INCLUDE [prod_short](includes/prod_short.md)]. I Teams kan du:

- Slå upp [!INCLUDE [prod_short](includes/prod_short.md)] kontakter från Teams-kommandorutan eller från meddelandeområdet. Kontakter kan inkludera potentiella kunder, leverantörer, kunder eller andra affärsrelationer.
- Dela en kontakt som ett kort i en Teams-konversation.
- Visa information om kontakten, interaktionshistorik och andra insikter som utestående betalningar eller öppna dokument.

## Förutsättningar

- Du har tillgång till Microsoft Teams.
- Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Team. Mer information finns i [Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)
- Du har ett [!INCLUDE [prod_short](includes/prod_short.md)]-konto som har tillgång till kontakter i minst ett företag.

> [!NOTE]
> Oavsett om du söker från kommandorutan eller meddelanderutan, kan du uppmanas att logga in eller ställa in appen första gången. Det här steget måste du söka efter kontakter på rätt Business Central-företag. Information om hur du ställer in appen för att välja företag finns i [ändra företag och andra inställningar i Teams](across-teams-settings.md).

## Slå upp kontakter från kommandorutan

Kommandorutan visas högst upp på varje skärm i Teams. Du kan söka, ta snabb åtgärder eller starta appar, som [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Sökning från kommandorutan är praktiskt när du snabbt vill söka efter kontakter och relaterade data för egen användning. Anta att du vill slå upp en e-postadress till en leverantör för att skapa ett kalendermöte. Eller kanske vill du slå upp interaktionshistorik under ett möte med en kund.

1. I kommandorutan, skriv **@Business Central** och välj sedan Business Central-appen från resultatet.

    ![Öppna Business Central-app för att söka efter kontakter från kommandorutan.](media/teams-contacts-command-1.png)

2. I rutan **Business Central**, börja skriva söktext, som ett namn, adress eller telefonnummer.

    När du skriver visas matchande resultat.

    ![Sök Business Central-kontakter från Teams-kommandorutan.](media/teams-contacts-command-2.png)
3. Välj en kontakt från resultatet.

    Kontaktkortet visas under kommandorutan.

4. Om du vill lägga till kontaktkortet i en konversation går du till det övre högra hörnet på kortet, väljer **... (Fler alternativ)** > **Kopierar**. Klistra sedan in kopian i meddelanderutan i en konversation.  

Mer allmän information om kommandorutan i Teams finns i [Teams – Använd kommandorutan](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).

## Slå upp kontakter från meddelanderutan

Fördelen med att använda meddelanderutan är att du kan lägga till ett kontaktkort direkt till en konversation så att andra kan se det.

1. Nedanför meddelandeskrivningen, välj ikonen **Business Central** för att starta appen.

    Om du inte ser ikonen **Business Central**, välj **... (Meddelandenstillägg)**.

    ![Öppna Business Central-app för att söka efter kontakter från meddelanderutan.](media/teams-contacts-message-box.png)

2. I rutan **Business Central**, börja skriva söktext, som ett namn, adress eller telefonnummer.

    När du skriver visas matchande resultat.

    ![Sök Business Central-kontakter från meddelanderutan.](media/teams-contacts-5.png)
3. Välj en kontakt från resultatet.

    Kontaktkortet visas i meddelanderutan.

    > [!NOTE]
    > Kontaktkortet skickas inte till konversationen direkt för andra att se. Du har möjlighet att granska innehållet på kortet och lägga till text före eller efter det du vill. Skicka sedan meddelandet till chatten när det är klart.

### Det finns också ett annat sätt

1. I stället för att använda **Business Central**-ikonen skriver du **@Business Central** direkt i meddelanderutan.
2. Ange dina söktermer i rutan.
3. Välj en kontakt med upp- och nedpilarna på tangentbordet och tryck sedan på <kbd>retur</kbd>.

## Visa information om kontaktkort

Kontakt kortet i Teams ger dig en snabb överblick över kunden, leverantören eller kontakten. Kortet är interaktivt &mdash;vilket innebär att du kan visa mer information eller till och med ändra en kontakt med hjälp av knapparna **Detaljer** eller **Öppna i nytt fönster**.

Knappen **Detaljer** öppnas ett fönster i Teams som visar mer information om kontakten, men inte så mycket som visas i [!INCLUDE [prod_short](includes/prod_short.md)]. Om du vill se all information om en kontakt i [!INCLUDE [prod_short](includes/prod_short.md)] väljer du **Öppna i nytt fönster**.

Kontaktkortet fungerar precis som kort för poster, t.ex. artiklar, kunder eller försäljningsorder. Mer information om kort finns i [Visa kortdetaljer](across-working-with-teams.md#view-card-details).

> [!NOTE]
> Alla deltagare i en Team-konversation kommer att kunna se kort för Business Central-kontakt som du skickar till konversationen. Men för att visa mer information om poster med hjälp av knapparna **Detaljer** eller **Öppna** på ett kort, behöver de tillgång till [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Hantera Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).

## Se även

[Översikt över Business Central- och Microsoft Teams-integrering](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Ändra företag och andra inställningar i Teams](across-teams-settings.md)  
[Dela poster i Microsoft Teams](across-working-with-teams.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]