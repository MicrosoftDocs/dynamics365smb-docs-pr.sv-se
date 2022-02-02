---
title: Skapa användare enligt licenser
description: Beskriver hur du lägger till användare i Business Central Online eller lokalt baserade på licenser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9173
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2c81046828e6be26683853d2c9cb7836ed939fb1
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029172"
---
# <a name="create-users-according-to-licenses"></a>Skapa användare enligt licenser

Denna artikel beskriver hur administratörer skapar användare och definierar vem som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)], samt vilka behörigheter som tilldelas olika användartyper beroende på licens.

När du skapar användare i [!INCLUDE[prod_short](includes/prod_short.md)] kan du tilldela specifika behörigheter till dem via behörighetsuppsättningar och ordna användare i användargrupper. Användargrupper gör det enklare att hantera behörigheter för flera användare samtidigt. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

Mer information om olika typer av licenser och hur licensiering fungerar i [!INCLUDE[prod_short](includes/prod_short.md)], [hämta licensguiden för Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Hanteringen av användare och licenser varierar beroende på om lösningen [!INCLUDE[prod_short](includes/prod_short.md)] distribueras online eller lokalt. För [!INCLUDE [prod_short](includes/prod_short.md)] online måste du lägga till användare från Microsoft 365. I lokala distributioner kan du skapa, redigera och ta bort användare direkt.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Hantera användare och licenser i online-distributioner

I onlineversionen av [!INCLUDE[prod_short](includes/prod_short.md)] definieras antalet användare av prenumerationen och läggs till i klientorganisationen i Microsoft Partner Center, vanligtvis av din Microsoft-partner. Mer information finns i [Lägga till en ny kund](/partner-center/add-a-new-customer) och [Skapa, pausa eller avbryta kundprenumerationer](/partner-center/create-a-new-subscription) i hjälpen till Microsoft Partner Center.

För att du ska kunna definiera vem som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)] måste du tilldela produktlicenserna till användarna enligt de roller dessa ska utföra i [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan göras på följande sätt:

- Ditt företags Microsoft 365-administratör kan göra detta i [administrationscentret för Microsoft 365](https://admin.microsoft.com). Mer information finns i [Lägga till användare individuellt eller i bulk till Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- En Microsoft-partner kan tilldela licenser i administrationscentret för Microsoft 365 eller i Microsoft Partner Center. Mer information finns i [Användarhanteringsuppgifter för kundkonton](/partner-center/assign-licenses-to-users) i hjälpen för Microsoft Partner Center.

Mer information finns i [Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationshjälpen.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Så här lägger du till användare eller uppdaterar användarinformation och licenstilldelningar i Business Central
När du har lagt till användare eller ändrat användarinformation i administrationscentret för Microsoft 365 kan du snabbt importera användarinformationen till [!INCLUDE[prod_short](includes/prod_short.md)]. Här ingår även licenstilldelning. 

1. Logga in på [!INCLUDE[prod_short](includes/prod_short.md)] med ett administratörskonto.
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **användare** och väljer sedan relaterad länk.  
3. Välj **Uppdatera användare från Microsoft 365**.

Om du lägger till nya användare är nästa steg att tilldela användargrupper och behörigheter. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md). Om du uppdaterar användarinformation och uppdateringen innehåller en licensförändring, kommer användarna att tilldelas rätt användargrupp och deras behörighetsuppsättningar uppdateras. Mer information finns i [Hantera behörigheter via användargrupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Alla användare måste tilldelas samma licens, antingen Essential eller Premium. Mer information finns i Licensieringsguiden för Microsoft Dynamics 365 Business Central. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Mer information om hur du synkroniserar användarinformation med Microsoft 365 finns i avsnittet [Synkronisera med Microsoft 365](#m365).

> [!NOTE]
> Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till din Business Central så att de kan arbeta med dig med räkenskapsårets informationen. Mer information finns i [Bjud in din externa revisor till din Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Så här tar du bort en användares åtkomst till systemet

I online-distributioner kan du ta bort en användares åtkomst till [!INCLUDE[prod_short](includes/prod_short.md)]. Alla referenser till användaren behålls, men användaren kan inte logga in och aktiva sessioner för användaren stoppas.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Öppna sidan **Användarekor** för den aktuella användaren och välj **Status** i fältet **Tillstånd**.
3. Om du vill ge användaren åtkomst igen, ställ in fältet **Status** till **Aktiveras**.

Du kan också ta bort licensen från en användare i administrationscentret för Microsoft 365. Användaren kan sedan inte logga in. Mer information finns i [Ta bort licenser från användare](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronisering med Microsoft 365

När du tilldelar en licens för [!INCLUDE[prod_short](includes/prod_short.md)] till en användare i Microsoft 365 finns det två sätt att skapa användaren på i [!INCLUDE[prod_short](includes/prod_short.md)].  

- Administratören kan lägga till användaren genom att välja åtgärden **Uppdatera användare från Microsoft 365** på sidan **Användare** enligt beskrivningen i avsnittet [Lägga till en användare eller uppdatera användarinformation i Business Central](#adduser).
- Licensinformationen uppdateras automatiskt när användaren loggar in för första gången.

I båda fallen görs ytterligare ett antal inställningar automatiskt. Dessa visas i den andra och tredje kolumnen i tabellen nedan.

Om du ändrar användarinformation i Microsoft 365 kan du uppdatera [!INCLUDE[prod_short](includes/prod_short.md)] för att återspegla ändringen. Beroende på vad du vill uppdatera använder du någon av åtgärderna på sidan **Användare**. Åtgärderna beskrivs i de sista tre kolumnerna i tabellen nedan.

> [!NOTE]
> Åtgärderna som beskrivs i följande register är korrekta, men den enda du behöver är **Uppdatera användare från Microsoft 365**, som har lagts till i syfte att förenkla processen. Övriga åtgärder kommer att tas bort i framtida versioner av [!INCLUDE[prod_short](includes/prod_short.md)].

|Vad händer när:|Första användaren, första inloggningen|Hämta användare från Microsoft 365|Uppdatera användare från Microsoft 365|Återställ användarens standardanvändargrupper|Uppdatera användargrupper|Uppdatera användarinformation från Microsoft 365|
|-|-|-|-|-|-|-|
|Omfattning:|Aktuell användare|Nya användare i Microsoft 365|Flera markerade användare|Enstaka markerad användare (utom aktuell)|Flera markerade användare|Flera markerade användare|
|Skapa den nya användaren och tilldela behörighetsuppsättningen SUPER.<br /><br /><!--Platform-->|**INTER**||**INTER** | | | |
|Uppdatera användaren baserat på information i Microsoft 365: Status, fullständigt namn, e-postadress för kontakt, e-post för autentisering.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**INTER**|**INTER**|**INTER**|**INTER**||**INTER**|
|Synkronisera användarplaner (licenser) med licenser och roller som har tilldelats i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**INTER**|**INTER**|**INTER**|**INTER**|**INTER**| |
|Lägg till användaren i användargrupper enligt de aktuella användarplanerna. Ta bort behörighetsuppsättningen SUPER för alla användare som inte är den första användare att logga in och [administratörer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Minst en SUPER krävs.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**INTER**|**INTER**|**INTER**|**INTER**<br /><br />Tar bort manuellt tilldelade användargrupper och behörigheter.|**INTER**<br /><br />Uppdatera användargruppstilldelningar.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Hantera användare och licenser i lokala distributioner

Vid lokala distributioner anges antalet licensierade användare i licensfilen (.flf). När en administratör eller Microsoft-partner överför licensfilen kan administratören ange vilka användare som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)].

Vid lokala distributioner kan administratören skapa, redigera och ta bort användare direkt från sidan **Användare**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Redigera eller ta bort en användare i en lokal distribution

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Markera användaren som du vill redigera och välj åtgärden **Redigera**.
3. På sidan **användarkort** ändrar du informationen efter behov.  
4. Om du vill radera en användare väljer du användaren du vill radera och väljer sedan åtgärden **Radera**.

> [!NOTE]
> För lokala distributioner kan en administratör ange hur användarautentiseringsuppgifter ska autentiseras i [!INCLUDE[server](includes/server.md)]-instansen. När du skapar en användare anger du vilken autentiseringstyp du använder.
>
> Mer information finns under [Autentisering och autentiseringstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrationshjälpen för [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se även

[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Licensiering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Lägg till användare till Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Säkerhet och skydd i Business Central (administrationsinnehåll)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]