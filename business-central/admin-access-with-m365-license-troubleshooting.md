---
title: Felsöka åtkomst med Microsoft 365-licenser
description: Lär dig hur du kan lösa problem med att komma åt Business Central med bara en Microsoft 365-licens.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: 750a78eb32568bea07d6851ff69c0b2cfea3ab49
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745019"
---
# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Felsöka åtkomst med Microsoft 365-licenser

## <a name="symptoms"></a>Symtom

När du öppnar en post i Teams visas ett felmeddelande i en flik eller kortinformation som liknar:

"Den här sidan använder data från relaterade tabeller som du inte har åtkomst till. Kontakta administratören om du vill arbeta med alla funktioner på den här sidan."

## <a name="cause"></a>Orsak

Du saknar antagligen objektbehörigheter för tabeller som den aktuella sidan eller posten länkar till.

## <a name="symptoms"></a>Symtom

Åtkomst har aktiverats, men användare får ett behörighetsfel när de kommer åt en post.

## <a name="cause"></a>Orsak

Om du aktiverar åtkomst i administrationscentret för Business Central men inte tilldelar behörigheter på sidan licenskonfiguration, får alla som försöker komma åt Business Central-poster i Teams sina användarposter utan behörighet till några objekt. Business Central är säkert genom konstruktion: administratörer måste först konfigurera vilka data som kan användas i Teams. 

## <a name="resolution"></a>Åtgärd

När du anpassar behörigheter på sidan licenskonfiguration påverkas endast de nyss skapade användarna. Du måste också tilldela behörighet som saknas till användare som redan har skapats via sidan med användarlistor. 

## <a name="symptoms"></a>Symtom

När jag delar en länk i Teams kan andra användare få fel meddelandet "vid åtkomst till Business Central med en Microsoft 365-licens kan du bara visa data i Microsoft Teams ".

## <a name="cause"></a>Orsak

När du delar en Business Central-länk till en Teams-chatt eller -kanaler, navigerar du alltid från en länk Microsoft Teams där uppgifterna inte längre blir tillgängliga för en person som har en Microsoft 365-licens.

## <a name="resolution"></a>Åtgärd

När du delar sidor eller poster kan du antingen ta med förhands granskningen av länken som ett kort eller dela data som en flik i en chatt eller kanal.

## <a name="see-also"></a>Se även

[Business Central-åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Ställ in åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Business Central och Microsoft Teams-integrering](across-teams-overview.md)
[Dela Business Central-poster och sidlänkar i Microsoft Teams](across-working-with-teams.md)  
[Felsöka Teams-integrering](admin-teams-troubleshooting.md)  