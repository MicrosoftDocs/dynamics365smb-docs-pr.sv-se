---
title: Lägg till fliken Business Central i Microsoft Teams
description: Lär dig hur du lägger till flikar i Teams som visar Business Central-sidor.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/12/2023
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# Lägg till fliken Business Central i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

I Teams visas flikarna högst upp i kanalerna och chattarna, så att deltagare snabbt kan komma åt relevant information. I den här artikeln beskrivs olika sätt att lägga till en flik som visar [!INCLUDE [prod_short](includes/prod_short.md)] data.

![Flikar i Teams](media/teams-tabs-border.png)

## Om flikar Business Central

En [!INCLUDE [prod_short](includes/prod_short.md)]-flik ger en fokuserad vy över [!INCLUDE [prod_short](includes/prod_short.md)] list- och kortsidor. Fliken visar inte hela [!INCLUDE [prod_short](includes/prod_short.md)] webbklienten. Det finns ingen webbläsargräns, [!INCLUDE [prod_short](includes/prod_short.md)] banderoll (t.ex. med Berätta, sök, hjälp) eller det övre navigeringsmenyerna&mdash;endast sidinnehåll och åtgärder. Innehållet är interaktivt, vilket innebär att du kan välja åtgärder och länkar, ändra data och mycket mer. Du är begränsad till det du ser och kan göra med samma behörighet som har tilldelats ditt konto i [!INCLUDE [prod_short](includes/prod_short.md)].

Om du vill veta mer om vem som kan visa innehållet på en [!INCLUDE [prod_short](includes/prod_short.md)] flik kan du läsa [Vem kan visa innehållet på en flik?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Är du utvecklare? Du kan också lägga till flikar programmässigt med Microsoft Graph API. Mer information finns i [Lägg till fliken Business Central i Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## Förutsättningar

För att lägga till en [!INCLUDE [prod_short](includes/prod_short.md)] flik måste följande villkor vara uppfyllda:

- Du har tillgång till Microsoft Teams.
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-licens.
- Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Team. Mer information finns i [Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md).

Om du vill visa [!INCLUDE [prod_short](includes/prod_short.md)] flik som har lagts till av en annan deltagare i kanalen eller chatten måste följande krav uppfyllas:

- Du har tillgång till Microsoft Teams.
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-licens eller begränsad åtkomst till Business Central med endast en Microsoft 365-licens. Mer information finns i [Business Central åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md).
- Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams.

## Lägg till flik med rekommenderat innehåll

Gör så här om du vill lägga till en flik genom att välja vad som ska visas från en lättillgänglig lista med rekommenderad information som bygger på ditt rollcenter&mdash;utan att du behöver lämna Teams. Mer information om vad du kan välja mellan finns i [var kommer det rekommenderade innehållet från?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Längst upp i en kanal eller chatt i Teams, välj **+ Lägg till en flik**.
2. I rutan **Sök** skriver du *business central* och markerar ikonen **[!INCLUDE [prod_short](includes/prod_short.md)]** och väntar tills [!INCLUDE [prod_short](includes/prod_short.md)] flikens konfigurationsfönster visas.

   ![Visar konfigurationsfönstret för Business Central i Teams](media/teams-bc-tab-config-window.png)

3. Med alternativet **Välj från innehåll som rekommenderas för** visas det företag i [!INCLUDE [prod_short](includes/prod_short.md)] som du arbetar med. Om du vill visa innehåll från ett annat företag markerar du det aktuella företaget och använder sedan alternativen **miljö** och **företag** för att ange företag som du vill arbeta med.
4. Klicka på nedåtpilen i alternativet **flikinnehåll** och välj det innehåll som du vill visa.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Vissa sidor kan innehålla olika vyer, d.v.s. varianter av den sida som är filtrerad för att visa specifika data. Om du vill ändra vyn för innehållet väljer du nedpilen för alternativet **önskad vy** och väljer en vy i listan.

   Mer information finns i avsnittet [Spara och anpassa vyer](ui-views.md).
6. Välj **Lägg upp på kanalen om den här fliken** för att automatiskt lägga upp ett meddelande i Teams-kanalen eller chatta för att låta deltagarna veta att du har lagt till den här fliken.
7. Välj **Spara**.

## Lägg till flik med hjälp av en sidlänk

Ett annat sätt att lägga till en flik med hjälp av en länk (URL) till sidan som du vill visa. Det här sättet är användbart när du vill visa en viss [!INCLUDE [prod_short](includes/prod_short.md)] post eller en listsida som inte har bokmärken i ditt rollcenter.

1. Längst upp i en kanal eller chatt i Teams, välj **+ Lägg till en flik**.
2. I rutan **Sök**, skriv *business central* och välj sedan ikonen **[!INCLUDE [prod_short](includes/prod_short.md)]**.
3. Vänta tills [!INCLUDE [prod_short](includes/prod_short.md)] flikkonfigurationsfönstret visas och välj sedan **Klistra in en [!INCLUDE [prod_short](includes/prod_short.md)] länk istället**.

   ![Visar konfigurationsfönstret av Business Central-flik i Teams och markerar alternativet länk](media/teams-bc-tab-config-window-page-link.png)
4. Gå till [!INCLUDE [prod_short](includes/prod_short.md)] och öppna sidan som du vill visa på fliken.
5. Kopiera länken till sidan.

   Du kan kopiera länken på två sätt: Det enklaste och bästa sättet är att välja **Dela** ![ikonen Dela i Business Central](media/share-icon.png) > **Kopiera länk**. Det andra sättet är att kopiera hela URL-adressen från webbläsarens adressfält. Mer information om det här steget finns i [dela Business Central-poster och sidlänkar](across-working-with-teams.md).

6. Gå tillbaka till Teams och klistra in länken i rutan **URL**.
7. I rutan **fliknamn** anger du ett namn som ska visas på fliken.
8. Välj **Lägg upp på kanalen om den här fliken** för att automatiskt lägga upp ett meddelande i Teams-kanalen eller chatta för att låta deltagarna veta att du har lagt till den här fliken.
9. Välj **Spara**.

## Lägg till flik genom att fästa kortinformation

Så här lägger du till en flik för en post som har delats eller klistrats in i en Teams-kanal eller chatt. Mer information om hur du delar poster och sidlänkar i Teams finns i [Dela poster och sidlänkar i Teams](across-working-with-teams.md).

1. I Teams väljer du knappen **Detaljer** på kortet.
2. I det övre högra hörnet av kortinformationen väljer du ikonen **Fäst längst upp på chatten** ![Fästikon för att lägga till Teams-flik i Business Central](media/pin-teams.png).

## Ändra en flik och dess innehåll

När en flik har lagts till kan du göra vissa ändringar av fliken. Du kan till exempel byta namn på fliken, flytta den och ta bort den. Dessa åtgärder finns i de flikalternativ som är tillgängliga genom att du väljer nedpil på fliken.

![Visar konfigurationsfönstret av Business Central-flik i Teams och menyn flikalternativ](media/teams-bc-tab-config-window-options.png)

På samma sätt som för innehållet på en flik kan du ändra informationen om du har behörighet. Om du ändrar informationen kan andra inte se ändringarna förrän de lämnar fliken och kommer tillbaka. Detsamma gäller om någon annan gör ändringar av data. Du kan inte ändra sidan som visas på fliken, så ta bara bort fliken och lägga till en annan.

Du kan också ändra vyn över sidan och dess data, som att sortera och växla mellan list- och panellägen. När du gör den här typen av ändringar påverkar de inte vad andra ser. De ser vad du ursprungligen bokförde tills de gör liknande ändringar själva.

## Se även

[Översikt över Business Central- och Microsoft Teams-integrering](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Dela Business Central-poster och sidlänkar i Microsoft Teams](across-working-with-teams.md).
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams](across-search-contacts-teams.md)  
[Ändra företag och andra inställningar i Teams](across-teams-settings.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
