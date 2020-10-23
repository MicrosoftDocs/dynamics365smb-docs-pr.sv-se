---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: a62a1a628f22ff47fa86a64a72f5b1834960dc72
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3931277"
---
Innan du kan konfigurera e-postloggning måste du förbereda Exchange Online med [offentliga mappar](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). Det kan du göra i [administrationscenter för Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) eller använda [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Om du vill använda [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) kan du hitta inspiration för hur du konfigurerar skriptet i ett exempelskript som vi publicerat på [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

I följande lista beskrivs de viktigaste stegen med länkar för att få mer information.  

- Skapa en administratörsroll för gemensamma mappar baserat på informationen i följande tabell:

  |Egenskap        |Värde                     |
  |----------------|--------------------------|
  |Name            |Hantering av delade mappar |
  |Valda roller  |Gemensamma mappar            |
  |Valda medlemmar|E-postmeddelandet för användar kontot som Business Central använder för att köra e-postloggningsjobbet|

  Mer information finns i [Hantera rollgrupper](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Skapa en ny postmapp för allmän mapp baserad på informationen i följande tabell:

  |Egenskap        |Värde                     |
  |----------------|--------------------------|
  |Name            |Offentlig postlåda            |

  Mer information finns i [Skapa en offentlig postmapp i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Skapa nya offentliga mappar

  - Skapa en ny offentlig mapp med namnet *e-postloggning* i roten så att den fullständiga sökvägen till mappen blir ```\Email Logging\```
  - Skapa två undermappar så att resultatet blir följande fullständiga sökvägar till mapparna:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Mer information finns i [Skapa en offentlig mapp](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Postaktivera den offentliga mappen *Kö*

  Mer information finns i [postaktivera eller skicka e-post-inaktivera en offentlig mapp](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Postaktivera utskick av e-post till den offentliga mappen *Kö* med Outlook eller Exchange Management Shell

  Mer information finns i [tillåta anonyma användare att skicka e-post till en offentlig mapp i e-postfunktionen](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Ange e-postloggning som ägare till både offentliga mappar *Kö* och *Lager* med Outlook eller Exchange Management Shell baserat på informationen i följande tabell:

  |Egenskap        |Värde                     |
  |----------------|--------------------------|
  |Användare            |E-postmeddelandet för användar kontot som Business Central använder för att köra e-postloggningsjobbet|
  |Behörighetsnivå|Ägare                     |

  Mer information finns i [Tilldela behörigheter till den offentliga mappen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Skapa två postflödesregler baserad på informationen i följande tabell

  |Syfte  |Name |Villkor                        |Åtgärd                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |En regel för inkommande e-post |Logga e-post som skickats till den här organisationen|*Avsändaren* finns *utanför organisationen* och *mottagaren* finns *inne i organisationen*|Skicka hemlig kopia det e-postkonto som har angetts för den offentliga mappen *kö*|
  |En regel för utgående e-post | Logga e-post som skickats från den här organisationen |*Avsändaren* finns *inne i organisationen* och *mottagaren* finns *utanför organisationen*|Skicka hemlig kopia det e-postkonto som har angetts för den offentliga mappen *kö*|
  
  Mer information finns i [Hantera postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) och [åtgärder för postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Om du gör ändringar i Exchange Management Shell blir ändringarna synliga i Exchange Admin Center efter en fördröjning. Dessutom kommer de ändringar som gjorts i Exchange att vara tillgängliga [!INCLUDE[prodshort](prodshort.md)] efter en fördröjning.
