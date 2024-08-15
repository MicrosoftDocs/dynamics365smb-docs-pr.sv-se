---
title: Hantera Microsoft Teams-integrering med Business Central| Microsoft Docs
description: Hantera Business Central-integrering med Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Hantera Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Den här artikeln innehåller en översikt över vad du kan göra som administratör för att styra Microsoft Teams-integrationen med [!INCLUDE [prod_short](includes/prod_short.md)].

## I Microsoft Teams

### Minsta krav

I det här avsnittet beskrivs minimikraven för att [!INCLUDE [prod_short](includes/prod_short.md)]-appen ska fungera i Team.

- Nödvändiga licenser

    Appen [!INCLUDE[prod_short](includes/prod_short.md)] kräver en Teams-licens genom ett Microsoft 365 Business- eller Enterprise-abonnemang. Fristående Teams-abonnemang som Microsoft Teams (gratis) eller Microsoft Teams Essentials stöds inte.

    De flesta funktioner i [!INCLUDE[prod_short](includes/prod_short.md)] appen för Teams kräver också en [!INCLUDE [prod_short](includes/prod_short.md)] licens enligt följande tabell.

    |Vad|[!INCLUDE [prod_short](includes/prod_short.md)]-licens|
    |----|---|
    |Söka efter [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter|![bock](media/check.png "kontroll")|
    |Klistra in en länk till en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en konversation och skicka den som ett kort.|![bock](media/check.png "kontroll")|
    |Dela en länk från en sida i [!INCLUDE [prod_short](includes/prod_short.md)] till en Teams-konversation.|![bock](media/check.png "kontroll")|
    |Visa ett kort i en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en konversation.||
    |Visa mer information för ett kort i en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en konversation.|![bock](media/check.png "kontroll")|
    |Öppna en sid länk i [!INCLUDE [prod_short](includes/prod_short.md)] från en konversation.|![bock](media/check.png "kontroll")|

- Tillåt förhandsgranskning av URL

    Principinställningen **Tillåt förhandsgranskning av URL** måste vara på. I annat fall kan ett kort inte genereras för [!INCLUDE [prod_short](includes/prod_short.md)]-länkar som klistrats in i en Teams-konversation. Mer information om den här inställningen finns i [Hantera meddelandeprinciper i Team](/microsoftteams/messaging-policies-in-teams).

### Hantera [!INCLUDE [prod_short](includes/prod_short.md)]-appen (valfritt)

Som Team-administratör kan du hantera alla appar för organisationen, inklusive [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Du kan godkänna eller installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för organisationen, hindra användare från att installera appen med mera.

Mer information finns i följande artiklar i Microsoft Teams-dokumentationen:

- [Hantera dina appar i Microsoft Teams administratörscenter](/MicrosoftTeams/manage-apps)
- [Hantera principer för appkonfiguration i Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## I [!INCLUDE [prod_short](includes/prod_short.md)]

### Minsta krav

- [!INCLUDE [prod_short](includes/prod_short.md)]-version:

    [!INCLUDE [prod_short](includes/prod_short.md)] utgivningscykel 1 år 2021 eller senare. Team-integration stöds endast för [!INCLUDE [prod_short](includes/prod_short.md)] online, inte lokalt.

- Codeunit **2718 sidan sammanfattning leverantör** är publicerad som en webbtjänst:

    Denna codeunit publiceras som en webbtjänst som standard. Denna codeunit ingår i [!INCLUDE [prod_short](includes/prod_short.md)]-systemprogrammet. Den används för att hämta fältdata för en [!INCLUDE [prod_short](includes/prod_short.md)]-sida som har lagts till i en Team-konversation. Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

- <a name="permissions"></a>Användarbehörigheter:

    Kontaktsökning, sidor och data som användare kan visa och redigera i en Team-konversation styrs oftast av deras behörighet i [!INCLUDE [prod_short](includes/prod_short.md)].

    - Om användaren vill söka efter kontakter måste de ha minst läsbehörighet i tabellen **kontakter** . 
    - Om du vill klistra in en [!INCLUDE [prod_short](includes/prod_short.md)]-länk i en Team-konversation och låta den utökas till ett kort måste användarna åtminstone ha läsbehörighet på sidan och dess data.
    - När ett kort har skickats till en konversation kan alla användare i konversationen se det kortet utan behörighet till [!INCLUDE [prod_short](includes/prod_short.md)].
    - Om du vill visa mer information om ett kort eller öppna posten i [!INCLUDE [prod_short](includes/prod_short.md)] måste användarna ha läsbehörighet på sidan och dess data.
    - Användare måste ändra behörigheter för att kunna ändra data.
    
    Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

## Installera Business Central-appen med hjälp av centraliserad distribution

Microsoft Teams administratörscentret konfigurerar Teams principer för programinställningar för organisationen. I administrations centret för team kan du använda funktionen centraliserad distribution för att automatiskt installera Business Central-appen i Teams för alla användare i organisationen, specifika grupper eller enskilda användare.

> [!NOTE]
> Om du vill konfigurera centraliserad distribution måste ditt Teams-konto minst ha rollen [Teamadministratör](/entra/identity/role-based-access-control/permissions-reference#teams-administrator].

1. I Business Central, välj ![Förstoringsglas som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **Teams-app centraliserad distribution** och sedan väljer du relaterad länk. Du kan även klicka [här](https://businesscentral.dynamics.com/?page=1833) om du vill öppna sidan direkt.
2. Läs informationen i **ställa in Business Central-appen för Teams** och välj sedan **Nästa** när du är klar.
3. Öppna [administrationscentret Teams](https://go.microsoft.com/fwlink/?linkid=2163970) och utför följande steg.
    1. Gå till **Teams-appar** > **inställningsprinciper**.
    2. Skapa en ny princip eller välj den princip som du vill använda för att installera Business Central-appen och välj sedan **Lägg till program**.
    3. På sidan **Lägg till installera**de appar söker du efter och väljer **Business Central**.
    4. Välj **Lägg till**.

       Business Central ska nu visas under **installerade appar** för principen.
    5. Konfigurera ytterligare inställningar efter behov och välj **Spara**.

    Mer information om inställningsprinciper i Teams finns i [Hantera principer för programkonfiguration i Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) i Teams-dokumentationen.
4. Gå tillbaka till **Teams-app centraliserad distribution** i Business Central och välj **klar**.

> [!IMPORTANT]
> Det kan ta upp till 24 timmar innan appinställningsprincipen tillämpas och appen distribueras till användarna.

## Hantera sekretess och kompatibilitet 

Microsoft Teams innehåller omfattande kontroller för kompatibilitet och hantering av känsliga eller personligt identifierbara data  &mdash; inklusive data som lagts till i chattar och kanaler av [!INCLUDE [prod_short](includes/prod_short.md)]-appen.

### Förstå var [!INCLUDE [prod_short](includes/prod_short.md)]-kort lagras

När ett kort har skickats till en chatt kopieras kortet och de fält som visas på kortet till Teams. Denna information är underkastad Teams policyer för organisationen, till exempel policyer för bevarande av data. När kortinformation visas lagras ingen information i informationsfönstret i Teams. Informationen förblir lagrad i [!INCLUDE [prod_short](includes/prod_short.md)] och kommer bara att hämtas av Teams när användaren väljer att visa informationen. 

- Om du vill veta mer om var Teams lagrar data, se [Var informationen finns i Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Mer information om bevarandepolicyer i Teams finns i [Bevarandepolicyer i Microsoft Teams](/microsoftteams/retention-policies).

### Begränsa delning av kort 

Du hindrar vissa användare eller grupper från att skicka kort till chattar eller kanaler genom att konfigurera meddelandepolicyer som inaktiverar inställningen **URL-förhandsgranskning**. Mer information om den här inställningen finns i [Hantera meddelandeprinciper i Team](/microsoftteams/messaging-policies-in-teams). 

Du kan också använda informationshinder för att förhindra att användare eller grupper kommunicerar med varandra. Mer information finns i [Informationshinder i Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funktionerna för dataförlustskydd i säkerhets- och efterlevnadscentret för Microsoft 365 kan inte användas specifikt för kort. De kan emellertid tillämpas på de chattmeddelanden som innehåller korten. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### Svara på dataförfrågningar

Du tillåter gruppmedlemmar och gruppägare att ta bort meddelanden som innehåller känsliga kort genom att ställa in meddelandepolicye, t. ex. **Ägare kan ta bort skickade meddelanden** och **Användare kan ta bort skickade meddelanden**. Mer information finns i [Hantera meddelandepolicyer i Teams](/microsoftteams/messaging-policies-in-teams).

Funktionerna för innehållssökning och eDiscovery-efterlevnad i säkerhets- och efterlevnadscentret för Microsoft 365 kan också tillämpas på kort.

Eftersom kortdata i Teams är en kopia av data i [!INCLUDE [prod_short](includes/prod_short.md)] kan du också använda [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner för att exportera en kunds data vid behov. Mer information om sekretess i [!INCLUDE [prod_short](includes/prod_short.md)] finns i avsnittet [Vanliga frågor och svar om sekretess för Business Central-kunder](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## Visa eller dölja postdata på kort

När en post delas med andra i en Teams-chatt eller kanal visas ett kort med fält som innehåller information om posten. Alla mottagare kan visa dessa data (eller postsammanfattning) som standard, oavsett licens eller behörigheter i Business Central. Om du är administratör kan du använda guiden för assisterad konfiguration **Kortinställningar** för att dölja postsammanfattningen så att den inte visas på kort i Teams. Om du döljer postsammanfattningen tas alla fält och bilder bort, men knappen **information** och annan information som inte rör posten visas fortfarande på kortet.

|Postsammanfattning aktiverad|Postsammanfattning inaktiverad|
|-|-|
|![Bild som visar ett kort i Teams när postsammanfattning har aktiverats.](media/card-settings-example-on.png)|![Bild som visar ett kort i Teams när postsammanfattning har inaktiverats.](media/card-settings-example-off.png)|

Du konfigurerar inställningen per miljö. När du aktiverar eller inaktiverar postsammanfattningen påverkar det alla företag i miljön.

1. Öppna den miljö som du vill ändra i Business Central.

   > [!TIP]
   > För att växla miljö, välj <kbd>Ctrl</kbd>+<kbd>O</kbd>.
2. Välj den ![Förstoringsglas som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kortinställningar** och väljer sedan relaterad länk. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Läs informationen om **Kortinställningar** och välj **Nästa** när du är klar.
4. På sidan **Datasynlighet** aktiverar du knappen **Visa postsammanfattning** för att visa data på korten eller inaktiverar du den för att dölja data.
5. Klicka på **Nästa** och följ instruktionerna för att slutföra inställningsguiden.

## Se även

[Integreringsöversikt för [!INCLUDE [prod_short](includes/prod_short.md)] och Microsoft Teams](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Vanliga frågor och Svar om Teams](teams-faq.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
