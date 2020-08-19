---
title: Skapa användare enligt licenser | Microsoft Docs
description: Beskriver hur du lägger till användare i Business Central Online eller lokalt baserade på licenser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 07/14/2020
ms.author: edupont
ms.openlocfilehash: 35819d7db3e22059738c6738d998319d0eb6691c
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577234"
---
# <a name="create-users-according-to-licenses"></a>Skapa användare enligt licenser

Denna artikel beskriver hur administratörer skapar användare och definierar vem som kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)], samt vilka behörigheter som tilldelas olika användartyper beroende på licens.

När du skapar användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du tilldela specifika behörigheter till dem via behörighetsuppsättningar och ordna användare i användargrupper. Användargrupper gör det enklare att hantera behörigheter för flera användare samtidigt. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Hanteringen av användare och licenser varierar beroende på om lösningen [!INCLUDE[d365fin](includes/d365fin_md.md)] distribueras online eller lokalt. För [!INCLUDE [prodshort](includes/prodshort.md)] online måste du lägga till användare från Office 365. I lokala distributioner kan du skapa, redigera och ta bort användare direkt.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Hantera användare och licenser i online-distributioner

I onlineversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] definieras antalet användare av prenumerationen och läggs till i klientorganisationen i Microsoft Partner Center, vanligtvis av din Microsoft-partner. Mer information finns i [Lägga till en ny kund](/partner-center/add-a-new-customer) och [Skapa, pausa eller avbryta kundprenumerationer](/partner-center/create-a-new-subscription) i hjälpen till Microsoft Partner Center.

För att du ska kunna definiera vem som kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du tilldela produktlicenserna till användarna enligt de roller dessa ska utföra i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan göras på följande sätt:

- Ditt företags Office 365-administratör kan göra detta i [Microsoft 365 administrationscenter](https://admin.microsoft.com). Mer information finns i [Lägga till användare individuellt eller i bulk till Office 365](https://aka.ms/CreateOffice365Users)  
- En Microsoft-partner kan tilldela licenser i Microsoft 365 Admin Center eller i Microsoft Partner Center. Mer information finns i [Användarhanteringsuppgifter för kundkonton](/partner-center/assign-licenses-to-users) i hjälpen för Microsoft Partner Center.

Mer information finns i [Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationshjälpen.

När användare tilldelas en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens i Office 365 kan du importera dem till sidan **Användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att använda åtgärden **Hämta nya användare från Office 365**.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Så här lägger du till en användare i Business Central

Använd dedikeradeimport funktioner för att lägga till nya användare eller uppdatera information i [!INCLUDE[d365fin](includes/d365fin_md.md)] från Microsoft 365 administrationscenter.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.  
2. Välj åtgärden **Uppdatera användare från Office 365**.

    Om det är första gången du lägger till användare från Office 365 väljer du åtgärden **Hämta nya användare från Office 365**.  
3. Följ stegen i guiden som visas.

De nya användarna och den nya användarinformationen i din Office 365-prenumeration läggs till på sidan **Användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan nu tilldela användargrupper och behörigheter. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

Mer information om hur du synkroniserar användarinformation med Office 365 finns i avsnittet [Synkronisera med Office 365](#synchronization-with-office-365).

> [!NOTE]
> Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till din Business Central så att de kan arbeta med dig med räkenskapsårets informationen. Mer information finns i [Bjud in din externa revisor till din Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-change-the-assigned-license-for-a-user"></a>Ändra den tilldelade licensen för en användare

Ibland kan du behöva ändra licensen som tilldelats en användare. Om du till exempel bestämmer dig för att använda modulen Tjänstehantering och därför behöver uppgradera alla Essential-licenser till Premium. Eller om en användares ansvar har ändrats och du måste byta ut en Team Member-licens till Essential.

1. Ändra licensen i Microsoft 365 administrationscenter. Mer information finns i [Lägga till användare individuellt eller i bulk till Office 365](https://aka.ms/CreateOffice365Users)
2. Logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som administratör.
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
4. På sidan **Användare**, välj åtgärden **Återställ användarens standardanvändargrupper**.

Användarna flyttas till rätt användargrupp och behörighetsuppsättningarna uppdateras. Mer information finns i [Hantera behörigheter via användargrupper](ui-define-granular-permissions.md).

> [!NOTE]
> Alla användare måste tilldelas samma licens, antingen Essential eller Premium. Mer information finns i Licensieringsguiden för Microsoft Dynamics 365 Business Central. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/business-central/overview/).

### <a name="to-remove-a-users-access-to-the-system"></a>Så här tar du bort en användares åtkomst till systemet

I online-distributioner kan du ta bort en användares åtkomst till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Alla referenser till användaren behålls, men användaren kan inte logga in och aktiva sessioner för användaren stoppas.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Öppna sidan **Användarekor** för den aktuella användaren och välj **Inaktiverad** i fältet **Tillstånd**.
3. Om du vill ge användaren åtkomst igen, ställ in fältet **Status** till **Aktiveras**.

Du kan också ta bort licensen från en användare i administrationscentret för Microsoft 365. Användaren kan sedan inte logga in. Mer information finns i [Ta bort licenser från användare](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-office-365"></a>Synkronisering med Office 365

När du tilldelar en licens för [!INCLUDE[d365fin](includes/d365fin_md.md)] till en användare i Office 365 finns det två sätt att skapa användaren på i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- Administratören kan lägga till användaren genom att välja åtgärden **Uppdatera användare från Office 365** på sidan **Användare** enligt beskrivningen i avsnittet [Lägga till en användare eller uppdatera användarinformation i Business Central](#adduser).
- Licensinformationen uppdateras automatiskt när användaren loggar in för första gången.

I båda fallen görs ytterligare ett antal inställningar automatiskt. Dessa visas i den andra och tredje kolumnen i tabellen nedan.

Om du ändrar användarinformation i Office 365 kan du uppdatera [!INCLUDE[d365fin](includes/d365fin_md.md)] för att återspegla ändringen. Beroende på vad du vill uppdatera använder du någon av åtgärderna på sidan **Användare**. Åtgärderna beskrivs i de sista tre kolumnerna i tabellen nedan.

|Vad händer när:|Första användaren, första inloggningen|Hämta användare från Office 365|Uppdatera användare från Office 365|Återställ användarens standardanvändargrupper|Uppdatera användargrupper|
|-|-|-|-|-|-|
|Omfattning:|Aktuell användare|Nya användare i Office 365|Flera markerade användare|Enstaka markerad användare (utom aktuell)|Flera markerade användare|
|Skapa den nya användaren och tilldela behörighetsuppsättningen SUPER.<br /><br /><!--Platform-->|**INTER**|| | | |
|Uppdatera användarposten baserat på aktuell information i Office 365: tillstånd, fullständigt namn, e-postkontakt, e-postautentisering.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**INTER**|**INTER**|**INTER**|**INTER**| |
|Synkronisera användarplaner (licenser) med licenser och roller som har tilldelats i Office 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**INTER**|**INTER**| |**INTER**|**INTER**|
|Lägg till användaren i användargrupper enligt de aktuella användarplanerna. Ta bort behörighetsuppsättningen SUPER för alla användare som inte är den första användare att logga in och [administratörer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Minst en SUPER krävs.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**INTER**|**INTER**| |**INTER**<br /><br />Tar bort manuellt tilldelade användargrupper och behörigheter.|**INTER**<br /><br />Uppdatera användargruppstilldelningar.|

## <a name="the-device-license"></a>Enhetslicensen

Med Dynamics 365 Business Central-enhetslicensen kan flera användare samtidigt använda en enhet som täcks av licensen. Detta kan till exempel vara en butikskassa, ett butiksgolv eller en lagerenhet. När du har köpt ett visst antal enhetslicenser kan upp till detta antal användare som tilldelats gruppen Dynamics 365 Business Central-enhetsanvändare logga in samtidigt. Mer information finns i Licensieringsguiden för Microsoft Dynamics 365 Business Central. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Företagets Office 365-administratör eller Microsoft-partner kan skapa Dynamics 365 Business Central-enhetsanvändargruppen och lägga till enhetsanvändare som medlemmar i [Microsoft 365-administrationscentret](https://admin.microsoft.com/) eller på [Azure-portalen](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Begränsningar för enhetsanvändare

Användare med enhetslicensen kan inte utföra följande uppgifter i [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Ställa in jobb som ska köras som schemalagda aktiviteter i jobbkön. Enhetsanvändare är samtidiga användare och vi kan därför inte säkerställa att den berörda användaren finns i systemet när en uppgift körs, vilket krävs.

- En enhetsanvändare kan inte vara den första användaren som loggar in. En användare av typen administratör, fullständig användare eller extern revisor måste vara den första att logga in så att de kan ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationshjälpen.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Så här skapar du en enhetsanvändargrupp för Dynamics 365 Business Central

1. Gå till sidan **Grupper** i administrationscentret för Microsoft 365.
2. Välj åtgärden **Lägg till en grupp**.
3. På sidan **Välj en grupptyp** väljer du åtgärden **Säkerhet** och sedan åtgärden **Lägg till**.
4. På sidan **Grunder** anger du **Dynamics 365 Business Central-enhetsanvändare** som namnet på gruppen.
  
   >[!NOTE]
   >Namnet på gruppen måste stavas på engelska exakt så som visas i steg 4, även om du använder ett annat språk.
5. Välj knappen **Stäng**.

> [!NOTE]
> Du kan också skapa en grupp av typen Office 365. Mer information finns i [Jämför grupper](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Så här lägger du till medlemmar i gruppen

1. I administrationscentret för Microsoft 365 uppdaterar du sidan **Grupper** så att din nya grupp visas.
2. Välj gruppen **Dynamics 365 Business Central-enhetsanvändare** och välj sedan åtgärden **Visa alla och hantera medlemmar**.
3. Välj åtgärden **Lägg till medlemmar**.
4. Markera de användare som du vill lägga till, och välj sedan knappen **Spara**.
5. Välj knappen **Stäng** tre gånger.

Du kan lägga till så många användare i Dynamics 365 Business Central-enhetsgruppen som du behöver. Antalet enheter som användare kan logga in på samtidigt definieras emellertid av antalet köpta enhetslicenser.

> [!NOTE]
> Du behöver inte tilldela en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens till användare som är medlemmar i gruppen Dynamics 365 Business Central-enhetsanvändare.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Hantera användare och licenser i lokala distributioner

Vid lokala distributioner anges antalet licensierade användare i licensfilen (.flf). När en administratör eller Microsoft-partner överför licensfilen kan administratören ange vilka användare som kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)].

Vid lokala distributioner kan administratören skapa, redigera och ta bort användare direkt från sidan **Användare**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Redigera eller ta bort en användare i en lokal distribution

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Markera användaren som du vill redigera och välj åtgärden **Redigera**.
3. På sidan **användarkort** ändrar du informationen efter behov.  
4. Om du vill radera en användare väljer du användaren du vill radera och väljer sedan åtgärden **Radera**.

> [!NOTE]
> För lokala distributioner kan en administratör ange hur användarautentiseringsuppgifter ska autentiseras i [!INCLUDE[server](includes/server.md)]-instansen. När du skapar en användare anger du vilken autentiseringstyp du använder.
>
> Mer information finns under [Autentisering och autentiseringstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrationshjälpen för [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se även

[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Säkerhet och skydd i Business Central (administrationsinnehåll)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
