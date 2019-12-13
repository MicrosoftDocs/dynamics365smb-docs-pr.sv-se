---
title: Tilldela eller redigera användarbehörigheter | Microsoft Docs
description: Beskriver hur du lägger till Office 365-användare till Business Central och tilldelar dem behörigheter, åtkomstbehörigheter och säkerhetsinställningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 12/03/2019
ms.author: sgroespe
ms.openlocfilehash: 1d0b7b7363df88e52631b4ba6e2f495be13f7397
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896163"
---
# <a name="create-users-according-to-licenses"></a>Skapa användare enligt licenser
Nedan beskrivs hur du som administratör skapar användare och definierar vem som kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] och vilka grundläggande rättigheter olika användartyper har enligt licenserna.

När användare skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du fortsätta att tilldela specifika behörigheter till användare via behörighetsuppsättningar och att ordna användare i användargrupper så att de blir lätta att hantera. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Hanteringen av användare och licenser varierar beroende på om lösningen distribueras online eller lokalt. I online-distributioner kan du till exempel bara inaktivera och aktivera en användare när den lagts till i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I lokala distributioner kan du skapa, redigera och ta bort användare.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Hantera användare och licenser i online-distributioner
I [!INCLUDE[d365fin](includes/d365fin_md.md)] online definieras antalet användare av prenumerationen och läggs till i klientorganisationen i Microsoft Partner Center, vanligtvis av din Microsoft-partner. Mer information finns i [Lägga till en ny kund](https://docs.microsoft.com/partner-center/add-a-new-customer) och [Skapa, pausa eller avbryta kundprenumerationer](https://docs.microsoft.com/partner-center/create-a-new-subscription) i hjälpen till Microsoft Partner Center.

För att du ska kunna definiera vem som kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] måste produktlicenserna tilldelas till användarna enligt de roller de ska utföra i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan göras på följande sätt:
- Ditt företags Office 365-administratör kan göra detta i [Microsoft 365 administrationscenter](https://admin.microsoft.com). Mer information finns i [Lägga till användare individuellt eller i bulk till Office 365](https://aka.ms/CreateOffice365Users)  
- En Microsoft-partner kan tilldela licenser i Microsoft 365 Admin Center eller i Microsoft Partner Center. Mer information finns i [Användarhanteringsuppgifter för kundkonton](https://docs.microsoft.com/partner-center/assign-licenses-to-users) i hjälpen för Microsoft Partner Center.

Mer information finns i [Administration av Business Central online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjälpen för utvecklare och IT-proffs.

När användare med en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens skapas i Office 365 kan de importeras till sidan **Användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att använda åtgärden **Hämta nya användare från Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Lägga till en användare i Business Central
Om du vill lägga till användare från Microsoft 365 Admin Center i [!INCLUDE[d365fin](includes/d365fin_md.md)] online använder du en dedikerad importfunktion.  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Välj åtgärden **Skaffa nya användare från Office 365**.

Alla nya användare som har skapats för din Office 365-prenumerationen kommer att läggas till i sidan **användare**. Användare tilldelas behörighetsuppsättningar enligt den licens som tilldelats användaren i Office 365. Sedan kan du fortsätta med att tilldela mer detaljerade behörigheter till användare och att ordna dem i användargrupper för enkel behörighetshantering. Mer information finns i [Tilldela behörighetsuppsättningar till användare](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till din Business Central så att de kan arbeta med dig med räkenskapsårets informationen. Mer information finns i [Bjud in din externa revisor till din Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Så här tar du bort en användares åtkomst till systemet
I online-distributioner kan du ta bort en användares åtkomst till systemet genom att ställa in fältet **Status** till **Inaktiverat**. Alla referenser till användaren behålls, men användaren kan inte längre logga in i systemet och aktiva sessioner för användaren avslutas.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Öppna sidan **Användarekor** för den aktuella användaren och välj **Inaktiverad** i fältet **Tillstånd**.
3. Om du vill ge användaren åtkomst igen, ställ in fältet **Status** till **Aktiveras**.

Förutom att inaktivera en användare kan du ta bort tilldelningen av licensen från en användare av administrationscenter för Microsoft 365. Användaren kan sedan inte logga in. Mer information finns i [Ta bort tilldelning av licenser från användare](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Ändra den tilldelade licensen för en användare
Ibland kan du behöva ändra licensen som tilldelats en användare. Om du till exempel bestämmer dig för att använda modulen Tjänstehantering och därför behöver uppgradera alla Essential-licenser till Premium. Eller om en användares ansvar har ändrats och du måste byta ut en Team Member-licens till Essential.

1. Ändra licensen i Microsoft 365 administrationscenter. Mer information finns i [Lägga till användare individuellt eller i bulk till Office 365](https://aka.ms/CreateOffice365Users)
2. Logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som administratör.
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
4. Alternativt kan du på sidan **Användare** välja åtgärden **Uppdatera all användargrupper**.

Användarna flyttas till rätt användargrupp och behörighetsuppsättningarna uppdateras. Mer information finns i [Hantera behörigheter via användargrupper](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Alla vanliga användare i en lösning måste tilldelas samma licens, Essential eller Premium.
> Mer information om licenser finns i [Microsoft Dynamics 365 Business Central licensieringsguide](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Synkronisering med Office 365
När en licens tilldelas en användare i Office 365 finns det två sätt att skapa användaren i [!INCLUDE[d365fin](includes/d365fin_md.md)] Systemet kommer att göra det automatiskt när användaren loggar in för första gången, eller också kan administratören lägga till användaren genom att välja åtgärden **Hämta användare från Office 365** på sidan **användare**.

I båda fallen görs ett antal ytterligare inställningar automatiskt. Dessa visas i den andra och tredje kolumnen i tabellen nedan.

Om du ändrar användaren i Office 365 i efterhand och du behöver synkronisera ändringarna till [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du använda olika åtgärder på sidan **användare** beroende på vad exakt du vill synkronisera. Dessa visas i de sista tre kolumnerna i tabellen nedan.

|Vad händer när:|Första inloggningen|Hämta användare från Office 365|Uppdatera användare från Office 365|Återställ användarens standardanvändargrupper|Uppdatera användargrupper|
|-|-|-|-|-|-|
|Omfattning:|Aktuell användare|Nya användare i Office 365|Flera markerade användare|Enstaka markerad användare (utom aktuell)|Flera markerade användare|
|Skapa den nya användaren och tilldela behörighetsuppsättningen SUPER.<br /><br />Plattform|**INTER**|**INTER**| | | |
|Uppdatera användarposten baserat på aktuell information i Office 365: tillstånd, fullständigt namn, e-postkontakt, e-postautentisering.<br /><br />Codeunit "Azure AD Graph-användare". UpdateUserFromAzureGraph|**INTER**|**INTER**|**INTER**|**INTER**| |
|Synkronisera användarplaner (licenser) med licenser och roller som har tilldelats i Office 365.<br /><br />Codeunit "Azure AD Graph-användare". UpdateUserPlans|**INTER**|**INTER**| |**INTER**|**INTER**|
|Lägg till användaren i användargrupper enligt de aktuella användarplanerna. Återkalla behörighetsuppsättningen SUPER. Minst en SUPER krävs. Återkalla inte från [administratörer](/dynamics365/business-central/dev-itpro/administration/tenant-administration).<br /><br />Codeunit "behörighetshanteraren". AddUserToDefaultUserGroups|**INTER**|**INTER**| |**INTER**<br /><br />Skriva över: ta bort användaren från andra grupper. Ta bort manuellt tilldelade behörighetsgrupper.|**INTER**<br /><br />Tillsats: Behåll det aktuella medlemskapet i användargruppen och tilldelade behörighetsgrupper intakta. Lägg endast till användare till grupper om det behövs.|

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Hantera användare och licenser i lokala distributioner
Vid lokala distributioner anges ett antal licensierade användare i licensfilen (.flf). När en administratör eller Microsoft-partner överför licensfilen kan administratören ange vilka användare som kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)].

Vid lokala distributioner kan administratören skapa, redigera och ta bort användare direkt från sidan **Användare**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Redigera en användare lokalt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Markera användaren som du vill redigera och välj åtgärden **Redigera**.
3. På sidan **användarkort** ändrar du informationen efter behov.    
4. Om du vill radera en användare, väljer du användaren du vill radera och välj sedan åtgärden **Radera**.

> [!NOTE]
> Vid lokal distribution av [!INCLUDE[d365fin](includes/d365fin_md.md)], kan administratören välja mellan olika autentiseringsmetoder för användare. När du sedan skapar en användare, tillhandahåller du olika information beroende på vilken autentiseringstyp du använder i den specifika [!INCLUDE[server](includes/server.md)]-instansen.<br /><br />
> Mer information finns på [autentisering och autentisering](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i avsnittet Administration av utvecklare och ITPro-innehåll för [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se även
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central licensieringsguide](https://aka.ms/BusinessCentralLicensing)  
[Säkerhet och skydd i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjälpen för utvecklare och IT-proffs
