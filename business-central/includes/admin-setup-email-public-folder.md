---
author: brentholtorf
ms.topic: include
ms.date: 02/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!NOTE]
> I följande avsnitt antas du att du har administratörsbehörighet för Exchange Online.

Innan du kan konfigurera e-postloggning måste du förbereda Office 365 [offentliga mappar](/exchange/collaboration-exo/public-folders/public-folders). Det kan du göra i [administrationscenter för Exchange](/exchange/exchange-admin-center?preserve-view=true) eller använda [Exchange Online Shell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Om du vill använda [Exchange Online Shell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) kan du hitta inspiration för hur du konfigurerar skriptet i ett exempelskript som vi publicerat i [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Följ stegen nedan för att konfigurera Exchange Online, med länkar till var du kan läsa mer.

### <a name="create-an-admin-role-group"></a>Skapa en administratörsrollgrupp

Skapa en administratörsrollgrupp för gemensamma mappar baserat på informationen i följande tabell:

|Egenskap        |Värde                     |
|----------------|--------------------------|
|Name            |Hantering av delade mappar |
|Valda roller  |Gemensamma mappar            |
|Valda användare  |E-postmeddelandet för användar kontot som Business Central använder för att köra e-postloggningsjobbet|

Mer information finns i [Hantera rollgrupper i Exchange Online](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox"></a>Skapa en ny gemensam mappinkorg

Skapa en ny postmapp för allmän mapp baserad på informationen i följande tabell:

|Egenskap        |Värde                     |
|----------------|--------------------------|
|Name            |Offentlig postlåda            |

Mer information finns i [Skapa en offentlig mappinkorg](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### <a name="create-new-public-folders"></a>Skapa nya offentliga mappar

1. Skapa en ny gemensam mapp med namnet **e-postloggning** i roten så att den fullständiga sökvägen till mappen blir `\Email Logging\`
2. Skapa två undermappar så att resultatet blir följande fullständiga sökvägar till mapparna:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Mer information finns i [Skapa en offentlig mapp](/exchange/collaboration-exo/public-folders/create-public-folder).

### <a name="set-public-folder-ownership"></a>Ange ägarskap för gemensam mapp

Ange e-postloggningsanvändaren som ägare till båda gemensamma mapparna *Kö* och *Lagring*.

Mer information finns i [Tilldela behörigheter till den offentliga mappen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder"></a>Postaktivera den offentliga mappen *Kö*

  Mer information finns i [postaktivera eller post-inaktivera en offentlig mapp](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### <a name="mail-enable-sending-emails-to-the-queue-public-folder"></a>Postaktivera utskick av e-post till gemensamma mappen *Kö*

Postaktivera utskick av e-post till den gemensamma mappen *Kö* med Outlook eller Exchange Management Shell.

Mer information finns i [Tillåta anonyma användare att skicka e-post till en postaktiverad gemensam mapp](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### <a name="create-mail-flow-rules"></a>Skapa regler för e-postflöde

Skapa två postflödesregler baserad på informationen i följande tabell:

|Syfte  |Name |Använd regeln om …             |Gör följande …                          |
|---------|-----|----------------------------------|---------------------------------------------|
|En regel för inkommande e-post |Logga e-post som skickats till den här organisationen|*Avsändaren* finns *utanför organisationen* och *mottagaren* finns *inne i organisationen*|Skicka hemlig kopia det e-postkonto som har angetts för den offentliga mappen *kö*|
|En regel för utgående e-post | Logga e-post som skickats från den här organisationen |*Avsändaren* finns *inne i organisationen* och *mottagaren* finns *utanför organisationen*|Skicka hemlig kopia det e-postkonto som har angetts för den offentliga mappen *kö*|

Mer information finns i [Hantera postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) och [Åtgärder för postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Om du gör ändringar i Exchange Management Shell blir ändringarna synliga i Exchange Admin Center efter en fördröjning. Dessutom kommer de ändringar som gjorts i Exchange att vara tillgängliga [!INCLUDE[prod_short](prod_short.md)] efter en fördröjning. Förseningen kan vara i flera timmar.
