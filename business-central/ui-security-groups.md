---
title: Kontrollera åtkomst med hjälp av säkerhetsgrupper
description: I den här artikeln beskrivs hur du använder säkerhetsgrupper för att definiera användarbehörigheter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Styra åtkomsten till Business Central med hjälp av säkerhetsgrupper

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Säkerhetsgrupper gör det enklare för administratörer att hantera användarbehörigheter i sina Dynamics 365-program, till exempel SharePoint Online, CRM Online och onlineversionen av [!INCLUDE [prod_short](includes/prod_short.md)]. Administratörer lägger till behörigheter i sina säkerhetsgrupper och när de lägger till användare i gruppen behörigheten gäller för alla medlemmar. En administratör kan till exempel skapa en säkerhetsgrupp som ger säljare möjlighet att skapa och bokföra försäljningsorder. Eller låta inköpare göra samma sak för inköpsorder.

Skapa säkerhetsgrupperna i Microsoft 365 administrationscentret eller Azure Active Directory. I den här artikeln beskrivs hur du gör i Microsoft 365 administrationscentret, men stegen är liknande i båda.

## Lägg till en säkerhetsgrupp i Microsoft 365 administrationscenter

1. I Microsoft 365 administrationscenter, gå till sidan **Aktiva team och grupper**.
2. Välj **Lägg till en grupp**.
3. Välj typ av grupp **Säkerhet** och välj **Nästa**.
4. Ange grunderna för din grupp.
5. Valfritt: gör medlemmarna i gruppen tillgängliga för rolltilldelning. Om du vill veta mer om tilldelningarna går du till [Använd Azure AD-grupper för att hantera rolltilldelningar](/azure/active-directory/roles/groups-concept).
6. Öppna gruppen och använd fliken **Lägg till medlemmar** för att inkludera personer i gruppen.

## Lägg till en säkerhetsgrupp i Business Central

I [!INCLUDE [prod_short](includes/prod_short.md)], skapa en säkerhetsgrupp och länka den sedan till säkerhetsgruppen i Microsoft 365 administrationscenter. Den nya gruppen innehåller de medlemmar som du lade till i Microsoft 365 administrationscentret.

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Säkerhetsgrupper** och väljer sedan relaterad länk.
2. Välj **Ny** för att skapa en grupp.
3. I fältet **Namn** anger du ett namn på gruppen.
4. I fältet **Namn på AAD-säkerhetsgrupp** anger du namnet på säkerhetsgruppen exakt så som det visas i Microsoft 365 administrationscenter. [!INCLUDE [prod_short](includes/prod_short.md)] kommer att hitta den gruppen och länka den till den här gruppen.

> [!NOTE]
> De användare som visas på kortet **Medlemmar** i rutan Faktabox eller på sidan **Medlemmar i säkerhetsgrupp** endast om de har lagts till som användare i [!INCLUDE [prod_short](includes/prod_short.md)]. För mer information om att lägga till användare se [Så här lägger du till användare eller uppdaterar användarinformation och licenstilldelningar i Business Central](ui-how-users-permissions.md#adduser).  

### Tilldela behörigheter till gruppen

1. På sidan **Säkerhetsgrupper** väljer du gruppen och sedan åtgärden **Behörigheter**.
1. Tilldela behörigheter på följande sätt:
    * Om du vill tilldela behörighetslistor individuellt väljer du de behörigheter som du vill tilldela i fältet **behörighetsuppsättning**.
    * Om du vill tilldela flera behörighetsuppsättningar väljer du åtgärden **Välj behörighetsuppsättningar** och väljer vilka uppsättningar som ska tilldelas.

## Granska behörigheter i en säkerhetsgrupp

På sidan **Säkerhetsgrupper** visar rutan faktabox de **behörighetsuppsättningar** som har tilldelats till gruppen. Varje användare som anges på kortet **Medlemmar** har dessa behörigheter. Åtgärden **Behörighetsuppsättning efter säkerhetsgrupp** ger en mer detaljerad vy. Där kan du också utforska de enskilda behörigheterna i varje säkerhetsgrupp.

Behörigheter finns också på sidan **användare**. I rutan faktabox visas korten **Behörighetsuppsättningar från säkerhetsgrupper** och **Medlemskap i säkerhetsgrupp** för den markerade användaren.

## Säkerhetsgrupper och användargrupper

Om du har användargrupper kan du konvertera grupperna till behörighetsgrupper i klientorganisationen med hjälp av guiden för assisterad konfiguration för **migrering av användargrupp**. För att starta guiden, på sidan **Funktionshantering** sök efter **Funktion: Konvertera behörigheter för användargrupper** och välj **Alla användare** i fältet **Aktiverad för**. I guiden för assisterad konfiguratio finns följande alternativ för konverteringen:

|Alternativ  |Beskrivning  |
|---------|---------|
|Tilldela användare     | Tilldela behörigheterna i användargrupper direkt till de användare som tilldelats gruppen och ta bort deras användargruppstilldelningar.        |
|Konvertera till en behörighetsuppsättning     | Skapa en ny behörighet för behörigheterna i varje användargrupp. Den nya behörighetsuppsättningen tilldelas alla medlemmar i varje användargrupp.          |

## Se även

[Skapa användare enligt licenser](ui-how-users-permissions.md)  
[Konfigurera Business Central Access i Teams med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Lär dig mer om grupper och åtkomsträttigheter i Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory-säkerhetsgrupper](/windows-server/identity/ad-ds/manage/understand-security-groups)  