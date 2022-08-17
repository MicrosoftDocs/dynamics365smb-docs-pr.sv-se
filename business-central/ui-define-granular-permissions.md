---
title: Definiera detaljerade behörigheter
description: I den här artikeln beskrivs hur du definierar detaljerade behörigheter och tilldelar varje användare de behörighetsgrupper som de behöver för att utföra sina jobb.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 1, 119, 8930, 9800, 9807, 9808, 9830, 9831
ms.date: 07/27/2022
ms.author: edupont
ms.openlocfilehash: 2b5bba12afb2fbb05dbfd3240088c2726f5d8337
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227506"
---
# <a name="assign-permissions-to-users-and-groups"></a>Tilldela behörigheter till användare och grupper

[!INCLUDE[prod_short](includes/prod_short.md)]-säkerhetssystemet kontrollerar vilka objekt som en användare har åtkomst till i varje databas eller miljö, i kombination med användarens licens. Du kan ange för varje användare om de kan läsa, ändra eller ange data i de valda databasobjekten. Mer detaljerad information finns i [Datasäkerhet](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i hjälpen för utvecklare och administrationsinnehåll för [!INCLUDE[prod_short](includes/prod_short.md)].

Innan du tilldelar behörigheter till användare och användargrupper måste du ange vem som kan logga in genom att skapa användare enligt licensen. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).

I [!INCLUDE[prod_short](includes/prod_short.md)] finns det två behörighetsnivåer för databasobjekt:

- De övergripande behörigheterna enligt licensen, som också kallas för berättigandet.

  I licenserna ingår standard behörighets uppsättningar. Från och med 2022 utgivningscykel 1 kan administratörer anpassa standard behörigheterna för de licenstyper som krävs. Mer information finns i [Konfigurera behörigheter baserat på licenser](ui-how-users-permissions.md#licensespermissions).  

- Mer detaljerad behörighet som tilldelades inifrån [!INCLUDE[prod_short](includes/prod_short.md)]i.

  I den här artikeln beskrivs hur du kan definiera, använda och tillämpa behörigheter i [!INCLUDE [prod_short](includes/prod_short.md)] för att ändra standard konfigurationen.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Mer information finns i [Tilldelad administratörsåtkomst till Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] Online innehåller standard användargrupper som tilldelas användare automatiskt baserat på deras licens. Du kan ändra standardkonfigurationen genom att ändra eller lägga till användargrupper, behörighetsgrupper och behörigheter. I följande tabell beskrivs viktiga scenarier för ändring av standardbehörigheterna.  

|Om du vill  |Gå till  |
|---------|---------|
|För att göra det enklare att hantera behörigheter för flera användare kan du ordna dem i användargrupper och sedan tilldela eller ändra en behörighetsuppsättning för många användare med en åtgärd.| [Hantera behörigheter via användargrupper](#to-manage-permissions-through-user-groups) |
|Så här hanterar du behörighetsgrupper för specifika användare | [Så här tilldelar behörighetsuppsättningar till användare](#to-assign-permission-sets-to-users) |
|Så här definierar du behörighetsuppsättningen|[Skapa eller ändra en behörighetsuppsättning](#to-create-or-modify-a-permission-set)|
|Så här hanterar du särskilda behörigheter|[Skapa eller ändra behörigheter manuellt](#to-create-or-modify-permissions-manually)|
|För att visa eller felsöka en användares behörigheter|[Så här får du en översikt en användares behörigheter](#to-get-an-overview-of-a-users-permissions)|
|Information om säkerhet på postnivå|[Säkerhetsfilter begränsar användarens åtkomst till specifika poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> En ytterligare metod för att definiera vilka funktioner en användare har åtkomst till är att ställa in fältet **Upplevelse** på sidan **Företagsinformation**. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).
>
> Du kan också ange vad användare ska se i användargränssnittet och hur de interagerar med deras tillåtna funktioner via sidor. Du gör detta genom profiler som du tilldelar olika typer av användare enligt deras jobbroll eller avdelning. Mer information finns i [Hantera profiler](admin-users-profiles-roles.md) och [anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-manage-permissions-through-user-groups"></a>Hantera behörigheter via användargrupper

Med användargrupper kan du hantera behörighetsgrupper i företaget. [!INCLUDE [prod_short](includes/prod_short.md)] Online innehåller standard användargrupper som tilldelas användare automatiskt baserat på deras licens. Du kan lägga till användare manuellt i en användargrupp, och du kan skapa nya användargrupper som kopior av befintliga.  

Du börjar med att skapa en användargrupp. Sedan tilldelar du gruppen behörighetsuppsättningar för att definiera vilka objekt som användare av gruppen ska få åtkomst till. När du lägger till användare i gruppen gäller de behörighetsuppsättningar som har definierats för gruppen för användaren.

Behörighetsuppsättningar som tilldelas en användare via en användargrupp förblir synkroniserade. En ändring av användargruppsbehörigheter sprids automatiskt till användarna. Om du tar bort en användare från en användargrupp återkallas de berörda behörigheterna automatiskt.

### <a name="to-add-users-to-a-user-group"></a>Så här lägger du till användare i en användargrupp

I proceduren nedan beskrivs hur du skapar användargrupper manuellt. Information om hur du skapar användargrupper automatiskt finns i [Kopiera en användargrupp och dess behörighetsuppsättningar](#to-copy-a-user-group-and-all-its-permission-sets).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Användargrupper** och väljer sedan relaterad länk.

    1. Alternativt kan du i sidan **Användare** välja åtgärden **Användargrupper**.
2. På sidan **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.
3. På sidan **Användargrupp** väljer du åtgärden **Lägg användare**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Om du vill kopiera en användargrupp och dess behörighetsuppsättningar

Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..

> [!NOTE]
> Medlemmarna i användargruppen kopieras inte till den nya användargruppen. Du måste lägga till dem manuellt i efterhand. Mer information finns i avsnittet [För att lägga till användare i en användargrupp](#to-add-users-to-a-user-group).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Användargrupper** och väljer sedan relaterad länk.
2. Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.
3. I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.

Användargruppen läggs till i sidan **Användargrupper**. Fortsätt med att lägga till användare. Mer information finns i avsnittet [För att lägga till användare i en användargrupp](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Du får ett meddelande om verifieringsfel om du försöker tilldela en användargrupp en användare som refererar till en behörighetsgrupp som har definierats i ett tillägg som inte avinstallerats. Detta beror på att app-ID tillägget verifieras när det refereras. Om du vill tilldela en användare en användargrupp kan du antingen installera tillägget på nytt, ta bort referensen för det avinstallerade tillägget från behörighetsgruppen eller ta bort behörighetsuppsättningen från användargruppen.


### <a name="to-assign-permission-sets-to-user-groups"></a>Tilldela behörighetsuppsättningar till användargrupper

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Användargrupper** och väljer sedan relaterad länk.
2. Markera den användargrupp som du vill tilldela behörighet till.  

    Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. Välj åtgärden **Användarbehörighetsuppsättning** för att öppna sidan **Användarbehörighetsuppsättning**.
4. På sidan **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Tilldela en behörighetsuppsättning på sidan **Behörighetsuppsättning efter användargrupp**

I proceduren nedan beskrivs hur du tilldelar behörighetsuppsättningar till en användargrupp på sidan **Behörighetsuppsättning efter användargrupp**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. På sidan **Användare** väljer du den relevanta användaren och väljer sedan åtgärden **Behörighetsuppsättning efter användargrupp**.
3. På sidan **Behörighetsuppsättning efter användargrupp** väljer du fältet **[användargruppsnamn]** på en rad för den relevanta behörighetsuppsättningen för att tilldela uppsättningen till användargruppen.
4. Markera kryssrutan **Alla användargrupper** om du vill tilldela behörighetsuppsättningen till alla användargrupper.

Du kan också tilldela behörighetsuppsättningar direkt till en användare.

## <a name="to-assign-permission-sets-to-users"></a>Så här tilldelar behörighetsuppsättningar till användare

En behörighetsuppsättning är en samling behörigheter för specifika databasobjekt. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[prod_short](includes/prod_short.md)].  

En [!INCLUDE[prod_short](includes/prod_short.md)]-lösning innehåller fördefinierade behörighetsuppsättningar som läggs till av Microsoft eller av lösningsleverantören. Du kan också lägga till nya behörighetsuppsättningar som är skräddarsydda efter företagets behov. Mer information finns i avsnittet [Att skapa eller redigera en behörighetsuppsättning](#to-create-or-modify-a-permission-set).

> [!NOTE]
> Om du inte vill begränsa en användares behörighet mer än vad som har definierats av licensen kan du tilldela en särskild behörighetsuppsättning som kallas SUPER för användaren. Den här behörighetsuppsättningen gör att användaren kan komma åt alla objekt som anges i licensen.
>
> En användare med Essential-licensen och SUPER behörighetsuppsättningen har tillgång till fler funktioner än användare med Team Member-licensen och behörighetsuppsättningen SUPER.

Du kan tilldela behörighetsuppsättningar till användare på två sätt:

- På sidan **Användarkort** genom att välja behörighetsuppsättningar att tilldela användaren.
- På sidan **Behörighetsuppsättning efter användare** genom att välja användare som en behörighetsuppsättning är tilldelad till.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Så här tilldelar du en behörighetsuppsättning till ett användarkort

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Markera den användare som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. I fönstret **Inkommande dokument** väljer du sidan **Användarkort**.
4. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. Mer information finns i avsnittet [Att skapa eller redigera en behörighetsuppsättning](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Så här tilldelar du en behörighetsuppsättning till sidan Behörighetsuppsättning efter användare

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. På sidan **Användare** välja åtgärden **Behörighetsuppsättning för användare**.
3. På sidan **Behörighetsuppsättning efter användare** markerar du kryssrutan **[användarnamn]** på en rad för den aktuella behörighetsuppsättningen för att tilldela uppsättningen till användaren.

    Markera kryssrutan **alla användare** om du vill tilldela behörighetsuppsättningen till alla användare.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Så här får du en översikt en användares behörigheter

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Öppna kortet för relevant användare.
3. Välj åtgärden **Gällande behörigheter**.

    Dellistan **behörigheter** listar alla de databasobjekt som användaren har åtkomst till. Avsnittet kan inte redigeras.

    Delen **Efter behörighetsuppsättning** visar tilldelade behörighetsuppsättningarna genom vilka behörigheterna beviljas användaren, källa och typ för behörighetsuppsättningen och som utökar de olika typerna tillåts.

    För varje rad som du väljer i avsnittet **behörigheter** under avsnittet **Efter behörighetsuppsättning** visar vilken behörighetsuppsättning eller uppsättningar som har beviljats behörighet till. I detta avsnitt kan du redigera värdena i var och en av fem åtkomsttypfält **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**.

    > [!NOTE]  
    > Endast behörighetsgrupper av typen **användardefinierade** kan redigeras.
    >
    > Rader med källberättigande kommer från prenumerationslicensen. Värdena på behörighetsvärdena för berättigandet åsidosätter värden i andra behörighetsuppsättningar om de har en högre rankning. Ett värde i en icke-berättigad behörighetsuppsättning som har en högre rankning än det relaterade värdet i berättigandet ska vara inom parentes för att ange att det inte är effektivt när det åsidosätts av berättigandet.
    >
    > Mer information om rankning finns i avsnittet [Att skapa eller redigera behörigheter](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Om du vill redigera en behörighet, i **Efter behörighetsuppsättning**, på raden för en relevant behörighetsuppsättning av typen **Användardefinierad**, välj ett av fem åtkomstfält och välj ett annat värde.

5. Om du vill redigera enskilda behörigheter inom behörighetsuppsättningen väljer du värdet i fältet **behörighetsuppsättning** för att öppna sidan **behörigheter**. Följ stegen som beskrivs i avsnittet [Att skapa eller redigera behörigheter](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> När du redigerar en behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Säkerhetsfilter – begränsa användarens åtkomst till specifika poster i en tabell

För postnivåsäkerhet i [!INCLUDE[prod_short](includes/prod_short.md)] kan du använda säkerhetsfilter för att begränsa användarens åtkomst till data i en tabell. Du kan skapa säkerhetsfilter på tabelldata. Ett säkerhetsfilter beskriver en uppsättning poster i en tabell som en användare har behörighet att komma åt. Du kan till exempel ange att en användare endast kan läsa de poster som innehåller information om en viss kund. På så sätt kan användaren inte kan komma åt de poster som innehåller information om andra kunder. Mer information finns i [Använda säkerhetsfilter](/dynamics365/business-central/dev-itpro/security/security-filters) i administrationsinnehållet.


## <a name="to-create-or-modify-a-permission-set"></a>Skapa eller ändra en behörighetsuppsättning

Behörighetsuppsättningar fungerar som behållare med behörigheter så att du enkelt kan hantera flera behörigheter i en post.

> [!NOTE]  
> En [!INCLUDE[prod_short](includes/prod_short.md)]-lösning innehåller vanligtvis ett antal fördefinierade behörighetsuppsättningar som läggs till av Microsoft eller av programvaruleverantören. Dessa behörighetsuppsättningar är av typen **System** eller **Tillägg**. Du kan inte skapa eller redigera sådana behörighetsuppsättningar eller behörigheter i dem. Du kan emellertid kopiera dem för att definiera egna behörighetsuppsättningar och behörigheter.
>
> Behörighetsuppsättningar som användaren skapar från nya eller som kopior, är av typen **Användardefinierade** och kan redigeras.

### <a name="to-create-new-permission-set-from-scratch"></a>Så här skapar du en ny behörighetsuppsättning från början

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Behörighetsuppsättning** och väljer sedan relaterad länk.
2. För att skapa en ny behörighetsuppsättning, välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] När du har skapat en behörighetsuppsättning måste du lägga till de faktiska behörigheterna. Mer information finns i avsnittet [Skapa eller ändra behörigheter manuellt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Att kopiera behörighetsuppsättning

Du kan också använda en kopieringsfunktion för att snabbt kopiera alla behörigheterna från en annan behörighetsuppsättning till en ny behörighetsuppsättning.

> [!NOTE]  
> Om en systembehörighetsuppsättning som du har kopierat ändras kommer du att meddelas (beroende på vad du väljer), så att du kan överväga om ändringarna är relevanta för att kopieras eller skrivas till dina egna behörighetsuppsättning.

1. I sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Kopiera behörighetsuppsättning**.
2. I sidan **Kopiera behörighetsuppsättning** anger du namnet på den nya behörighetsuppsättning och väljer sedan knappen **OK**.
3. Markera kryssrutan **Meddela vid ändrad behörighetsuppsättning** om du vill ha en länk mellan de ursprungliga och de kopierade behörighetsuppsättningarna. På så sätt får du ett meddelande om namnet eller innehållet i den ursprungliga behörighetsuppsättningen ändras i en framtida version.

Den nya behörighetsuppsättningen innehåller alla behörigheter för de kopierade grupp, läggs till som en ny rad på sidan **behörighetsuppsättningen**. Nu kan du ändra behörigheten i den nya behörighetsuppsättningen. 

> [!TIP]
> Raderna sorteras i bokstavsordning inom varje typ.

### <a name="to-export-and-import-a-permission-set"></a>Så här exporterar och importerar du en behörighetsgrupp

Om du snabbt vill ställa in behörigheter kan du importera behörighetsuppsättningar som du har exporterat från en annan [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation.

I miljöer med flera klientorganisationer importeras en behörighetsuppsättning till en särskild klientorganisation. Med andra ord är omfattningen för importen *Klientorganisation*.

1. I klientorganisation 1, på **Behörighetsuppsättningar** Välj raden eller linjerna för behörighetsuppsättningarna att exportera och välj sedan **Exportera behörighetsuppsättning**.

    En XML-fil skapas i hämtningsmappen på datorn. Som standard är namnet *Exportera behörighetsuppsättningar.xml*.

2. I klientorganisation 2, på sidan **behörighetsuppsättning** välj åtgärden **Importera behörighetsuppsättning**.
3. I dialogrutan **Importera behörighetsuppsättningar**, överväg om du vill slå ihop befintliga behörighetsuppsättningar med några nya behörighetsuppsättningar i XML-filen.

    Om du markerar kryssrutan **Uppdatera befintliga behörigheter** kommer befintliga behörighetsuppsättningar som matchar namnen i XML-filen att slås samman med de importerade behörighetsuppsättningarna.

    Om du inte markerar kryssrutan **Uppdatera befintliga behörigheter** kommer behörighetsuppsättningar som matchar namnen i XML-filen att hoppas över under importen. I så fall får du ett meddelande om behörighetsuppsättningar som hoppas över.

4. I dialogrutan **Import** hittar du och väljer den XML-fil som ska importeras och väljer sedan åtgärden **Öppna**.

Behörighetsgrupperna importeras.

## <a name="to-create-or-modify-permissions-manually"></a>Skapa eller ändra behörigheter manuellt

Denna procedur förklarar hur man lägger till eller redigerar behörigheter manuellt. Du kan också få behörigheter genererade automatiskt utifrån dina åtgärder i användargränssnittet. Mer information finns i [Skapa eller ändra behörigheter genom att registrera dina åtgärder](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> När du redigerar en behörighet och därmed de relaterade behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

1. På sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Behörighet**.
2. På sidan **behörigheter**, skapa en ny rad och fyll i fälten på en befintlig rad.

I alla fält av typen de fem åtkomst **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**, kan du välja en med följande tre behörighetsalternativ:

|Alternativ|Description|Rankning|
|------|-----------|-------|
|**Ja**|Användaren kan utföra åtgärden på det aktuella objektet.|Högsta|
|**Indirekt**|Användaren kan utföra åtgärden på det aktuella objektet, men endast via ett annat relaterat objekt som användaren har fullständig åtkomst till. Mer information om indirekta behörigheter finns i [Behörighetsegenskap](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) i Hjälp för utvecklare och IT-proffs|Andra högsta|
|**Tomt**|Användaren kan inte utföra åtgärden på det aktuella objektet.|Lägsta|

> [!IMPORTANT]
> Var försiktig när du tilldelar **infoga behörighet** eller **ändra behörighet** till **9001 användargruppmedlem** eller **9003 behörighetsuppsättning för användargrupp**. Alla användare som tilldelats behörighetsgruppen kan eventuellt tilldela sig själva till andra användargrupper, som i sin tur kan ge dem oavsiktliga behörigheter.

### <a name="example---indirect-permission"></a>Exempel – Indirekt behörighet

Du kan tilldela en indirekt behörighet för att använda en objekt endast via en annan objekt.
en användare kan till exempel har behörighet att köra Codeunit 80, försäljningspost. Kodmodulen försäljningspost utför många uppgifter, inklusive ändra tabell 37 inköpsrad. När användaren bokför ett försäljningsdokument, kontrollerar codeunit [!INCLUDE[prod_short](includes/prod_short.md)] om användaren har behörighet att ändra tabellen inköpsrad. Om inte kan inte codeuniten slutföra uppgiften och användaren tar emot ett felmeddelande. I så fall, kör Codeunit korrekt.

Användaren behöver dock inte ha fullständig åtkomst till tabellen Inköpsrad för att köra codeuniten. Om användaren har indirekt behörighet till tabellen inköpsrad körs codeunit försäljningspost korrekt. När en användare har indirekt behörighet kan användaren endast ändra tabellen inköpsrad genom att köra kodmodulen försäljningspost eller ett annat objekt som har behörighet att ändra tabellen inköpsrad. Användaren kan endast ändra tabellen inköpsrad när det görs från moduler som stöds. Användaren kan inte köra funktionen oavsiktligt eller på ett skadligt sätt med andra metoder.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Skapa eller ändra behörigheter genom att registrera dina åtgärder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Behörighetsuppsättning** och väljer sedan relaterad länk.

    Alternativt kan du i sidan **Användare** välja åtgärden **Behörighetsuppsättningar**.
2. På sida **Behörighetsuppsättningar** väljer du åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov.
4. Välj åtgärden **Behörigheter**.
5. På sidan **behörigheter** väljer åtgärden **postbehörigheter** och välj sedan åtgärden **startar**.

    En registreringsprocess startar som fångar alla dina åtgärder i användargränssnittet.
6. Gå till olika sidor och aktiviteter i [!INCLUDE[prod_short](includes/prod_short.md)] som du vill att användare med denna behörighetsuppsättning ska lägga till. Du måste utföra de aktiviteter som du vill registrera behörigheter för.
7. Om du vill avsluta registreringen går du tillbaka till sidan **behörigheter** och väljer åtgärden **stoppa**.
8. Välj knappen **Ja** om du vill lägga till registrerade behörigheter till den nya behörighetsuppsättningen.
9. För varje objekt i den registrerade listan anger du om användarna ska kunna infoga, ändra eller ta bort poster i de registrerade tabellerna.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Ta bort föråldrade behörigheter från alla behörighetsgrupper

1. På sidan **Behörighetsuppsättningar**, välj åtgärden **Ta bort inaktuella behörigheter**.

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare

Administratörer kan definiera tidsperioder under vilka angivna användare kan bokföra. Administratörer kan också ange om systemet loggar hur mycket tid användare är inloggade. På liknande sätt kan administratörer tilldela ansvarsenheter till användare. För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställning** och väljer sedan relaterad länk.
2. I sidan **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="viewing-permission-changes-telemetry"></a>Visa telemetri över behörighetsförändringar

Du kan låta [!INCLUDE[prod_short](includes/prod_short.md)] skicka ändringar som har gjorts i behörighet för en Application Insights-resurs i Microsoft Azure. Med hjälp av Azure Monitor kan du sedan skapa rapporter och aviseringar för insamlade data. Mer information finns i följande artiklar i [!INCLUDE[prod_short](includes/prod_short.md)]-hjälpen för utvecklare och administratörer:

- [Övervaka och analysera telemetri – Aaktivera Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysera telemetri för fältövervakning](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Utsedda adminanvändare

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a>Se även

[Skapa användare enligt licenser](ui-how-users-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Säkerhet och skydd i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjälpen för utvecklare och IT-proffs  
[Tilldela ett telemetri-ID till användare](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]