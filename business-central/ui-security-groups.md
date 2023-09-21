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

# <a name="control-access-to-business-central-using-security-groups"></a>Styra åtkomsten till Business Central med hjälp av säkerhetsgrupper

Säkerhetsgrupper gör det enklare för administratörer att hantera användarbehörigheter. Till exempel för [!INCLUDE [prod_short](includes/prod_short.md)] online kan de återanvändas över Dynamics 365-program, t.ex.  SharePoint Online, CRM Online och [!INCLUDE [prod_short](includes/prod_short.md)]. Administratörer lägger till behörigheter i deras [!INCLUDE [prod_short](includes/prod_short.md)] säkerhetsgrupper och när de lägger till användare i gruppen behörigheten gäller för alla medlemmar. En administratör kan till exempel skapa en [!INCLUDE [prod_short](includes/prod_short.md)] säkerhetsgrupp som ger säljare möjlighet att skapa och bokföra försäljningsorder. Eller låta inköpare göra samma sak för inköpsorder.

## <a name="business-central-online-and-on-premises"></a>Business Central Online och lokalt

Du kan använda säkerhetsgrupper för online- och lokala versioner av [!INCLUDE [prod_short](includes/prod_short.md)]. Beroende på din version skapar du grupper på något av följande sätt:

* För onlineversionen använder du Microsoft Entra säkerhetsgrupper. Om du vill veta mer om hur du skapar en grupp går du till [Skapa, redigera eller ta bort en säkerhetsgrupp i Microsoft 365 administrationscenter](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* För lokala platser använder du Windows Active Directory-grupper. Om du vill ha mer information går du till [Skapa ett gruppkonto i Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory).

Skapa sedan en motsvarande säkerhetsgrupp i [!INCLUDE [prod_short](includes/prod_short.md)] och länka den sedan till gruppen du skapade. Om du vill veta mer går du till [Lägg till en säkerhetsgrupp i Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Om du har skapat en speciell typ av användare med en licens typ för Windows-grupper i en version av [!INCLUDE [prod_short](includes/prod_short.md)] lokal som är äldre än 2023 utgivningscykel 1 när du uppgraderar [!INCLUDE [prod_short](includes/prod_short.md)] konverterar användaren till en säkerhetsgrupp. Den nya säkerhetsgruppen har samma namn som Windows-gruppnamnet. Säkerhetsgruppen ger dig en bättre översikt över grupp medlemmarna och deras gällande behörigheter.

## <a name="add-a-security-group-in-business-central"></a>Lägg till en säkerhetsgrupp i Business Central

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Säkerhetsgrupper** och väljer sedan relaterad länk.
1. Välj **Ny** för att skapa en grupp.
1. Skapa länken till gruppen enligt följande:

    * För [!INCLUDE [prod_short](includes/prod_short.md)] online, välj gruppen i fältet **Namn på AAD-säkerhetsgrupp**.
    * För [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, välj gruppen i fältet **Windows-gruppnamn**.

> [!NOTE]
> De användare som visas på kortet **Medlemmar** i rutan Faktabox eller på sidan **Medlemmar i säkerhetsgrupp** endast om de har lagts till som användare i [!INCLUDE [prod_short](includes/prod_short.md)]. För mer information om att lägga till användare se [Så här lägger du till användare eller uppdaterar användarinformation och licenstilldelningar i Business Central](ui-how-users-permissions.md#adduser).  

### <a name="assign-permissions-to-a-security-group"></a>Tilldela behörigheter till en säkerhetsgrupp

1. På sidan **Säkerhetsgrupper** väljer du gruppen och sedan åtgärden **Behörigheter**.
1. Tilldela behörigheter på följande sätt:

    * Om du vill tilldela behörighetslistor individuellt väljer du de behörigheter som du vill tilldela i fältet **behörighetsuppsättning**.
    * Om du vill tilldela flera behörighetsuppsättningar väljer du åtgärden **Välj behörighetsuppsättningar** och väljer vilka uppsättningar som ska tilldelas.

## <a name="review-the-permissions-in-a-security-group"></a>Granska behörigheter i en säkerhetsgrupp

På sidan **Säkerhetsgrupper** visar rutan faktabox de **behörighetsuppsättningar** som har tilldelats till gruppen. Varje användare som anges på kortet **Medlemmar** har dessa behörigheter. Åtgärden **Behörighetsuppsättning efter säkerhetsgrupp** ger en mer detaljerad vy. Där kan du också utforska de enskilda behörigheterna i varje säkerhetsgrupp.

Behörigheter finns också på sidan **användare**. I rutan faktabox visas korten **Behörighetsuppsättningar från säkerhetsgrupper** och **Medlemskap i säkerhetsgrupp** för den markerade användaren.

## <a name="security-groups-and-user-groups"></a>Säkerhetsgrupper och användargrupper

> [!NOTE]
> Användargrupper kommer inte längre att vara tillgängliga i framtida versioner.

Säkerhetsgrupper liknar de användargrupper som är tillgängliga för tillfället. Användargrupper är dock bara relevanta för [!INCLUDE [prod_short](includes/prod_short.md)]. Säkerhets grupper är baserade på grupper i Azure Active Directory eller Windows Active Directory, beroende på om du använder [!INCLUDE [prod_short](includes/prod_short.md)] online eller lokalt. Grupper gynnar administratörer eftersom de kan använda dem med andra Dynamics 365-appar. Om till exempel säljare använder [!INCLUDE [prod_short](includes/prod_short.md)] och SharePoint-administratörer behöver inte skapa gruppen och dess medlemmar.

### <a name="optional-convert-user-groups-to-permission-sets"></a>Valfritt: Konvertera användargrupper till behörighetsuppsättningar

I 2023 utgivningscykel 1 och senare kan du konvertera användargrupper till behörighetsgrupper i din klientorganisation. Behörighetsgrupperna ger samma funktioner som användargrupperna. Här följer några exempel:

* Du kan använda faktaboxen **användare** för att hantera behörigheter för användare.
* Du kan detaljgranska behörighetsgruppens namn om du vill lägga till andra behörighetsgrupper i den uppsättning som du arbetar med. Mer information finns i [Lägga till andra behörighetsuppsättningar](ui-define-granular-permissions.md#to-add-other-permission-sets).

Använd **Migrering av användargrupper** användargrupper för att konvertera grupper. För att starta guiden, på sidan **Funktionshantering** sök efter **Funktion: Konvertera behörigheter för användargrupper** och välj **Alla användare** i fältet **Aktiverad för**. I guiden för assisterad konfiguratio finns följande alternativ för konverteringen:

|Alternativ  |Beskrivning  |
|---------|---------|
|Tilldela användare     | Tilldela behörigheterna i användargrupper direkt till de användare som tilldelats gruppen och ta bort deras användargruppstilldelningar.        |
|Konvertera till en behörighetsuppsättning     | Skapa en ny behörighet för behörigheterna i varje användargrupp. Den nya behörighetsuppsättningen tilldelas alla medlemmar i varje användargrupp.          |

### <a name="license-configurations-still-apply"></a>Licenskonfigurationer gäller fortfarande

Du kan konfigurera behörigheter i [!INCLUDE [prod_short](includes/prod_short.md)] baserat på licenser. Dessa behörigheter tilldelas direkt till nya användare. Dessa konfigurationer gäller fortfarande, även om du börjar använda säkerhetsgrupper.

Om du enbart vill använda säkerhetsgrupper rekommenderar vi att du tar bort licenskonfigurationerna. Mer information om licenskonfigurationer finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).

Du kan ta bort licenskonfigurationer på sidan **Licenskonfiguration**. Välj en licens och ta sedan bort alla behörighetsgrupper som tilldelats den.

## <a name="see-also"></a>Se även

[Skapa användare utifrån licenser](ui-how-users-permissions.md)  
[Konfigurera Business Central Access i Teams med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Lär dig mer om grupper och åtkomsträttigheter i Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory-säkerhetsgrupper](/windows-server/identity/ad-ds/manage/understand-security-groups)  
