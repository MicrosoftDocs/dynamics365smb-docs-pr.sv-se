---
title: Skapa användare utifrån licenser
description: Beskriver hur du lägger till användare i Business Central Online eller lokalt baserade på licenser.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800_Primary, 9807_Primary, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173, 774_Primary'
ms.date: 05/03/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-users-according-to-licenses"></a>Skapa användare utifrån licenser

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

I den här artikeln beskrivs hur administratörer skapar användare och anger vem som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)]. Artikeln beskriver också om hur du tilldelar behörigheter till olika användare enligt dina produktlicenser.

När du skapar användare i [!INCLUDE[prod_short](includes/prod_short.md)] ger du behörighet till dem via behörighetsgrupper. Du kan även ordna användarna i användargrupper. Användargrupper gör det enklare att hantera behörigheter och andra inställningar för flera användare samtidigt. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

Mer information om olika typer av licenser och hur licensiering fungerar i [!INCLUDE[prod_short](includes/prod_short.md)], [hämta licensguiden för Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Hanteringen av användare och licenser varierar beroende på om lösningen [!INCLUDE[prod_short](includes/prod_short.md)] distribueras online eller lokalt. För [!INCLUDE [prod_short](includes/prod_short.md)] online måste du lägga till användare från Microsoft 365. I lokala distributioner kan du skapa, redigera och ta bort användare direkt.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Hantera användare och licenser i online-innehavare

Användarkonton i [!INCLUDE[prod_short](includes/prod_short.md)] måste skapas först i Microsoft 365 administrationscenter. Dessa användarkonton är inte exklusiva till [!INCLUDE [prod_short](includes/prod_short.md)]. Om du prenumererar på andra planer kan de användas för att logga in på andra program, t.ex. Power BI. Mer information om hur du skapar användare i Microsoft 365 administrationscenter finns i [Lägga till användare i Microsoft administrationscenter](/microsoft-365/admin/add-users/add-users).

Din prenumeration på [!INCLUDE[prod_short](includes/prod_short.md)] online definierar hur många [!INCLUDE[prod_short](includes/prod_short.md)] användarlicenser som är tillåtna. Användare läggs till i klientorganisationen på Microsoft Partner Center, vanligtvis av din Microsoft-partner. Mer information finns i [Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Du tilldelar licenser till användare baserat på det arbete som varje användare gör i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan tilldela licenser på flera sätt:

- Ditt företags Microsoft 365-administratör kan göra detta i [administrationscentret för Microsoft 365](https://admin.microsoft.com). Mer information finns i [Lägga till användare individuellt eller i bulk till Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- En Microsoft-partner kan tilldela licenser i administrationscentret för Microsoft 365 eller i Microsoft Partner Center. Mer information finns i [Användarhanteringsuppgifter för kundkonton](/partner-center/assign-licenses-to-users) i hjälpen för Microsoft Partner Center.

Mer information finns i [Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationshjälpen.

När användarkonton har skapats på Microsoft 365 administrationscentret finns det två sätt att importera dem till [!INCLUDE [prod_short](includes/prod_short.md)]:

- Ett användarkonto importeras automatiskt när användaren loggar in på [!INCLUDE [prod_short](includes/prod_short.md)] första gången.

   > [!NOTE]
   > När en användare har loggat in på [!INCLUDE [prod_short](includes/prod_short.md)] online kan du inte ta bort användaren.

- Administratören kan importera användare genom att välja åtgärden **Uppdatera användare från Microsoft 365** på sidan **Användare* .

Båda metoderna har sina egna fördelar och du kan använda dem samtidigt. Med varje tillvägagångssätt kan administratörerna konfigurera [!INCLUDE [prod_short](includes/prod_short.md)] proaktivt för att tilldela startbehörighet, användargrupper och användarprofiler. Med hjälp av åtgärden **Uppdatera användare från Microsoft 365** får administratörer mer kontroll att justera behörigheter, användargrupper och profiler. Det är en idealisk metod när du konfigurerar [!INCLUDE [prod_short](includes/prod_short.md)] för första gången, innan en användare loggar in eller när du lägger till en ny grupp användare.

> [!NOTE]
> När du har lagt till användare i Microsoft 365 administrationscenter rekommenderar vi att du uppdaterar användarinformationen i [!INCLUDE[prod_short](includes/prod_short.md)] så snart som möjligt. Det är enkelt att göra användarinformationen aktuell och ser till att användarna alltid kan logga in. För mer information, se [Så här lägger du till användare eller uppdaterar användarinformation och licenstilldelningar i Business Central](#adduser).<br>
>
> Att uppdatera användar information är särskilt viktigt om du har anpassat behörighetsuppsättningar för licensen. Om en ny användare försöker logga in på [!INCLUDE[prod_short](includes/prod_short.md)] innan du har lagt till dem kanske de inte kan användas. Mer information finns i [Konfigurera behörigheter baserat på licenser](#licensespermissions).
>
> Användare som upplever problemet är dock inte blockerade. Du kan antingen använda åtgärden **gå tillbaka start** eller helt enkelt logga in för att lösa problemet.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Mer information finns i [Tilldelad administratörsåtkomst till Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Konfigurera behörigheter baserat på licenser

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Administratörer kan konfigurera behörighetsgrupper och användargrupper för varje licens.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Till exempel har licensen *Dynamics 365 Business Central Teammedlem*, följande behörigheter som standardgruppmedlemmar:

- D365 LÄS
- D365 TEAMMEDLEM
- REDIGERA I EXCEL – VYN
- EXPORTERA RAPPORT EXCEL
- LOKAL

Andra behörighetsgrupper läggs till automatiskt utifrån de användargrupper som tilldelats licensen. När du skapar en ny användare utifrån denna licens tilldelar, [!INCLUDE[prod_short](includes/prod_short.md)] behörighetsgrupperna från användargrupperna och behörighetsgrupperna från licensen. Samma startbehörigheter tilldelas användaren om deras användarkonto har skapats automatiskt i [!INCLUDE[prod_short](includes/prod_short.md)] eller om administratören har använt åtgärden **Uppdatera användare från Microsoft 365** på sidan **användare**.

Om denna standardkonfiguration inte är rätt inställning för en viss miljö kan administratören ändra konfigurationen. Anpassade behörigheter påverkar dock bara nya användare som har tilldelats licensen. Behörigheter för befintliga användare som har tilldelats licensen påverkas inte.  

1. Logga in på [!INCLUDE[prod_short](includes/prod_short.md)] med ett administratörskonto.  
2. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Licenskonfiguration** och väljer sedan relaterad länk.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. På sidan **Licensskonfiguration** välj den licens som du vill anpassa och välj sedan åtgärden **Konfigurera**.  
4. Välj fältet **anpassa behörigheter** för att växla vid anpassning och gör sedan ändringar.  

    I vårt exempel vill administratören ta bort behörigheten för redigering i Excel och ta bort användargruppen för *exportåtgärder för Excel* från gruppmedlemlicensen. Efteråt kan nya användare som tilldelas Team Member-licensen inte exportera data till Excel. Om organisationen ändrar sig om detta ämne kan de bara gå tillbaka till sidan **Licenskonfiguration** och stänga av anpassningen för den licenstypen.  

> [!IMPORTANT]
> Denna anpassning av behörigheter gäller bara för nya användare som du tilldelar den aktuella licensen. Befintliga användare uppdateras inte. Vi rekommenderar att du anpassar behörigheterna innan du börjar tilldela användarlicenser i Microsoft 365 administrationscentret.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Så här lägger du till användare eller uppdaterar användarinformation och licenstilldelningar i Business Central

När du har lagt till användare eller ändrat användarinformation i administrationscentret för Microsoft 365 kan du snabbt importera användarinformationen till [!INCLUDE[prod_short](includes/prod_short.md)]. Importen inkluderar även licenstilldelning.  

> [!TIP]
> Om du behöver uppdatera användarinformationen och du har många användare kan du använda filterrutan för att begränsa listan. Du kan filtrera på grundläggande information som användarnamn eller ange mer tekniska filter, till exempel användarens säkerhets-ID.

1. Logga in på [!INCLUDE[prod_short](includes/prod_short.md)] med ett administratörskonto.
2. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.  
3. Välj **Uppdatera användare från Microsoft 365**.

> [!IMPORTANT]  
> Om du vill köra synkroniseringen av användare från Microsoft 365 med **Uppdatera användare från Microsoft 365** guide, kräver SUPER-behörighetsuppsättningen.

> [!NOTE]
>  **Uppdatera användare från Microsoft 365**  guide uppdaterar inte användare som inte har tilldelats en licens, till exempel någon som är [Dynamics 365-administratör](/entra/identity/role-based-access-control/permissions-reference#dynamics-365-administrator). Dessa användare uppdateras nästa gång de loggar in i miljön.

Nästa steg för nyligen skapade användare är att tilldela användargrupper och behörigheter. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md) Om du uppdaterar en användare med en licensändring tilldelar [!INCLUDE [prod_short](includes/prod_short.md)] användare till lämplig användargrupp och uppdaterar deras behörighetsuppsättningar. Mer information finns i [Hantera behörigheter via användargrupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Med utgivningscykel 1 för 2024 kan en Premium-licensanvändare logga in på ett företag där fältet **Användarupplevelse** är inställt på **Essentials** på sidan **Företagsinformation**. Premium-användaren kan dock inte använda någon av de funktioner som Premium-licensen tillhandahåller. Det här fungerar inte i motsatt riktning. Användare som har ett Essentials-licens kan inte logga in på ett företag där **Användarupplevelse** är inställt på **Premium** på sidan **Företagsinformation**. Mer information om licensiering finns på webbplatsen för [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till dina [!INCLUDE[prod_short](includes/prod_short.md)] så att de kan arbeta med dig med räkenskapsårets informationen. Mer information finns i [Bjud in din externa revisor till din Business Central](finance-accounting.md#inviteaccountant).

Mer information om hur du synkroniserar användarinformation med Microsoft 365 finns i avsnittet [Synkronisera med Microsoft 365](#m365).

> [!NOTE]
> Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till dina [!INCLUDE[prod_short](includes/prod_short.md)] så att de kan arbeta med dig med räkenskapsårets informationen. Mer information finns i [Bjud in din externa revisor till din Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Så här tar du bort en användares åtkomst till systemet

Du kan ta bort en användares åtkomst till [!INCLUDE[prod_short](includes/prod_short.md)] online. Alla referenser till användaren behålls. Användaren kan emellertid inte logga in och aktiva sessioner för användaren stoppas.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Öppna sidan **Användarekor** för den aktuella användaren och välj **Status** i fältet **Tillstånd**.
3. Om du vill ge användaren åtkomst igen, ställ in fältet **Status** till **Aktiveras**.

Du kan också ta bort licensen från en användare i administrationscentret för Microsoft 365. Användaren kan sedan inte logga in. Mer information finns i [Ta bort licenser från användare](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronisering med Microsoft 365

När du tilldelar en licens för [!INCLUDE[prod_short](includes/prod_short.md)] till en användare i Microsoft 365 finns det två sätt att skapa användaren på i [!INCLUDE[prod_short](includes/prod_short.md)].  

- Administratören kan lägga till användaren genom att välja åtgärden **Uppdatera användare från Microsoft 365** på sidan **Användare** enligt beskrivningen i avsnittet [Lägga till en användare eller uppdatera användarinformation i Business Central](#adduser).
- Licensinformationen uppdateras automatiskt när användaren loggar in för första gången.

I båda fallen görs flera inställningar automatiskt. Dessa inställningar visas i den andra och tredje kolumnen i följande tabell.

Om du ändrar användarinformation i Microsoft 365 kan du uppdatera [!INCLUDE[prod_short](includes/prod_short.md)] för att återspegla ändringen. Beroende på vad du vill uppdatera använder du någon av åtgärderna på sidan **Användare**. Åtgärderna beskrivs i de sista två kolumnerna i följande tabell.

|Vad händer när:|Första användaren, första inloggningen|Uppdatera användare från Microsoft 365|Återställ användarens standardanvändargrupper|
|-|-|-|-|
|Omfattning:|Aktuell användare|Flera markerade användare|Enstaka markerad användare (utom aktuell)|
|Skapa den nya användaren och tilldela behörighetsuppsättningen SUPER.<br /><br /><!--Platform-->|**INTER**|**INTER** | | 
|Uppdatera användaren baserat på information i Microsoft 365: Status, fullständigt namn, e-postadress för kontakt, e-post för autentisering.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**INTER**|**INTER**|**INTER**|
|Synkronisera användarplaner (licenser) med licenser och roller som har tilldelats i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**INTER**|**INTER**|**INTER**|
|Lägg till användaren i användargrupper enligt de aktuella användarplanerna. Ta bort behörighetsuppsättningen SUPER för alla användare som inte är den första användare att logga in och [administratörer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Minst en SUPER krävs.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**INTER**|**INTER**|**INTER**<br /><br />Tar bort manuellt tilldelade användargrupper och behörigheter.|

Användare kan bara komma åt [!INCLUDE[prod_short](includes/prod_short.md)] poster i Teams med deras Microsoft 365 licens. När åtkomst är aktiverad för en miljö, synkronisering med hjälp av åtgärden **Uppdatera användare från Microsoft 365** hoppar över användare som endast har en Microsoft 365-licens. Om du vill inkludera dessa användare i synkronisering måste du först uppdatera miljö inställningarna genom att tilldela en säkerhets grupp som innehåller användare med [!INCLUDE[prod_short](includes/prod_short.md)] licens och användare med bara en Microsoft 365 licens.

Lär dig mer om hur du skyddar åtkomsten till miljöer med hjälp av säkerhets grupper vid [ Hantera åtkomst med hjälp av Microsoft Entra grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Få en översikt över hur du får tillgång till [!INCLUDE[prod_short](includes/prod_short.md)] i Teams med Microsoft 365-licenser på [admin-access-with-m365-license](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Hantera användare och licenser i lokala distributioner

Vid lokala distributioner anges antalet licensierade användare i licensfilen (.bclicense or .flf). När en administratör eller Microsoft-partner överför licensfilen kan de ange vilka användare som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)].

Vid lokala distributioner kan administratören skapa, redigera och ta bort användare direkt från sidan **Användare**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Redigera eller ta bort en användare i en lokal distribution

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Markera användaren som du vill redigera och välj åtgärden **Redigera**.
3. På sidan **användarkort** ändrar du informationen efter behov.  
4. Om du vill radera en användare väljer du användaren du vill radera och väljer sedan åtgärden **Radera**.

> [!NOTE]
> För lokala distributioner kan en administratör ange hur användarautentiseringsuppgifter ska autentiseras i [!INCLUDE[server](includes/server.md)]-instansen. När du skapar en användare anger du vilken autentiseringstyp du använder.
>
> Mer information finns under [Autentisering och autentiseringstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrationshjälpen för [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="analyze-user-status-by-license-type"></a>Analysera användarstatus efter licenstyp

Du kan använda funktionen **Dataanalys** för att analysera data på sidan [Användare](https://businesscentral.dynamics.com/?page=9800). Du behöver inte köra en rapport eller öppna till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "Användare efter status" eller "Användare efter licenstyp" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

### <a name="user-analysis-scenarios"></a>Användaranalysscenarier

Följande avsnitt ger exempel på scenarier där analys av användarlistan kan hjälpa dig att övervaka dina användares status.

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Användare efter status](#example-users-by-status) | Visa en lista över användare baserat på deras status (aktiverad/inaktiverad). | [Användare](https://businesscentral.dynamics.com/?page=9800) | **Status**, **Användarnamn**, **Fullständigt namn**, **E-postadress för auktorisering** och **Licenstyp**. |
| [Användare efter licenstyp](#example-users-by-license-type) | Se en lista över användare baserat på deras licenstyp. | [Användare](https://businesscentral.dynamics.com/?page=9800) | **Licenstyp**, **Status**, **Användarnamn**, **Fullständigt namn** och **E-postadress för auktorisering**. |

### <a name="example-users-by-status"></a>Exempel: Användare efter status

Så här analyserar du användare efter status:

1. Öppna listan [Användare](https://businesscentral.dynamics.com/?page=9800) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: ikon för att aktivera analysläget.
1. På menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fälten **Status** (användare aktiverad/inaktiverad) och **Licenstyp** till området **Radgrupper**.
1. Välj fälten **Användarnamn**, **Fullständigt namn** och **E-postadress för auktorisering**.
1. Byt namn på analysfliken till **Användare efter status** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source=" media/data-analysis-users.png" alt-text="Exempel på hur du gör dataanalyser på sidan Ändringsloggtransaktioner (Vem ändrade vilka data när)." lightbox="media/data-analysis-users.png":::

### <a name="example-users-by-license-type"></a>Exempel: Användare efter licenstyp

För att analysera användare efter licenstyp, följ dessa steg:

1. Öppna listan [Användare](https://businesscentral.dynamics.com/?page=9800) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: ikon för att aktivera analysläget.
1. På menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fälten **Licenstyp** och **Status** (användare aktiverad/inaktiverad) till området **Radgrupper**.
1. Välj fälten **Användarnamn**, **Fullständigt namn** och **E-postadress för auktorisering**.
1. Byt namn på analysfliken till **Användare efter licenstyp** eller något som beskriver den här analysen.

## <a name="see-also"></a>Se även

[Tilldela användare och grupper behörigheter](ui-define-granular-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Licensiering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Lägg till användare till Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Säkerhet och skydd i Business Central (administrationsinnehåll)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Tilldela ett telemetri-ID till användare](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
