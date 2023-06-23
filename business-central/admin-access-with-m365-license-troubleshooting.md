---
title: Felsöka åtkomst med Microsoft 365-licenser
description: Lär dig hur du kan lösa problem med att komma åt Business Central med bara en Microsoft 365-licens.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="troubleshoot-access-with-microsoft-365-licenses" />Felsöka åtkomst med Microsoft 365-licenser

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message" />"Den här sidan använder data från relaterade tabeller som du inte har åtkomst till" felmeddelande

### <a name="symptoms" />Symtom

När du öppnar en post i Teams visas ett felmeddelande i en flik eller kortinformation som liknar:

"Den här sidan använder data från relaterade tabeller som du inte har åtkomst till. Kontakta administratören om du vill arbeta med alla funktioner på den här sidan."

### <a name="cause" />Orsak

Du saknar antagligen objektbehörigheter för tabeller som den aktuella sidan eller posten länkar till.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error" />Microsoft 365 åtkomst har aktiverats, men användare får ett behörighetsfel

### <a name="symptoms" />Symtom

Åtkomst med Microsoft 365 har aktiverats i administrationscenter för Business Central men användare får ett behörighetsfel när de kommer åt en post.

### <a name="cause" />Orsak

Om du aktiverar åtkomst i administrationscentret för Business Central men inte tilldelar behörigheter på sidan **licenskonfiguration**, får alla som försöker komma åt Business Central-poster i Teams sina användarposter utan behörighet till några objekt. Business Central är säkert genom konstruktion: administratörer måste först konfigurera vilka data som kan användas i Teams. 

### <a name="resolution" />Åtgärd

När du anpassar behörigheter på sidan licenskonfiguration påverkas endast de nyss skapade användarna. Du måste också tilldela behörighet som saknas till användare som redan har skapats via sidan med användarlistor. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data" />Du har delat en länk i Teams, men användarna får ett meddelande om att de endast kan visa information

### <a name="symptoms" />Symtom

När jag delar en länk i Teams som Business Central-användare kan andra användare få fel meddelandet "vid åtkomst till Business Central med en Microsoft 365-licens kan du bara visa data i Microsoft Teams".

### <a name="cause" />Orsak

När du delar en Business Central-länk till en Teams-chatt eller -kanaler, navigerar du alltid från en länk Microsoft Teams där uppgifterna inte längre blir tillgängliga för en person som har en Microsoft 365-licens.

### <a name="resolution" />Åtgärd

När du delar sidor eller poster kan du antingen ta med förhands granskningen av länken som ett kort eller dela data som en flik i en chatt eller kanal.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button" />Kortet från den delade länken är minimalt och innehåller inte knappen Detaljer

### <a name="symptoms" />Symtom

När en Microsoft 365-licensinnehavare utan en Business Central-licens delar en Business Central-länk i Teams, utökas den automatiskt till ett kort som inte har någon värdefull information och som bara visar Business Central utan knappen **Detaljer**.

### <a name="cause" />Orsak

Användare som har en  Microsoft 365- licens men saknar Business Central-licens kan inte dela länkar som kort. Om användaren har Business Central-appen för Teams installerad och klistrar in en länk i skrivområdet visas bara ett minimalt kort. 

## <a name="see-also" />Se även

[Business Central-åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Ställ in åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Business Central och Microsoft Teams-integrering](across-teams-overview.md)
[Dela Business Central-poster och sidlänkar i Microsoft Teams](across-working-with-teams.md)  
[Felsöka Teams-integrering](admin-teams-troubleshooting.md)  
