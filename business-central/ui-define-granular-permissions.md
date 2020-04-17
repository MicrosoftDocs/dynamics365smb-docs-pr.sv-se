---
title: Definiera detaljerade behörigheter | Microsoft Docs
description: Beskriver hur du ger användare åtkomst till objekt genom att tilldela dem behörighetsuppsättningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c71b56812b67c4ec51ea8d48d095cabc79c585fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194481"
---
# <a name="assign-permissions-to-users-and-groups"></a>Tilldela behörigheter till användare och grupper
Med säkerhetssystemet [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du kontrollera vilka objekt som en användare har åtkomst till i varje databas eller miljö. Du kan ange för varje användare om de kan läsa, ändra eller ange data i de valda databasobjekten. Mer detaljerad information finns i [Datasäkerhet](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i hjälpen för utvecklare och IT-proffs för [!INCLUDE[d365fin](includes/d365fin_md.md)].

Innan du tilldelar behörigheter till användare och användargrupper måste du ange vem som kan logga in genom att skapa användare enligt licensen såsom definierats i Microsoft 365 administrationscenter. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).

I [!INCLUDE[d365fin](includes/d365fin_md.md)] finns det två behörighetsnivåer för databasobjekt:
- De övergripande behörigheterna enligt licensen, som också kallas för berättigandet.
- Mer detaljerad behörighet som tilldelades inifrån [!INCLUDE[d365fin](includes/d365fin_md.md)]i.

För att göra det enklare att hantera behörigheter för flera användare kan du ordna dem i användargrupper och därmed tilldela eller ändra en behörighetsuppsättning för många användare med en åtgärd. Mer information finns i [Hantera behörigheter via användargrupper](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> En ytterligare metod för att definiera vilka funktioner en användare har åtkomst till är att ställa in fältet **Upplevelse** på sidan **Företagsinformation**. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).
>
> Du kan också ange vad användare ska se i användargränssnittet och hur de interagerar med deras tillåtna funktioner via sidor. Du gör detta genom profiler som du tilldelar olika typer av användare enligt deras jobbroll eller avdelning. Mer information finns i [Hantera profiler](admin-users-profiles-roles.md) och [anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Så här tilldelar behörighetsuppsättningar till användare
En behörighetsuppsättning är en samling behörigheter för specifika databasobjekt. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)].

En [!INCLUDE[d365fin](includes/d365fin_md.md)]-lösning innehåller ett antal fördefinierade behörighetsuppsättningar som läggs till av Microsoft eller av lösningsleverantören. Du kan också lägga till nya behörighetsuppsättningar som är skräddarsydda efter företagets behov. Mer information finns i avsnittet [Att skapa eller redigera en behörighetsuppsättning](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Om du inte vill begränsa en användares behörighet mer än vad som har definierats av licensen kan du tilldela en särskild behörighetsuppsättning som kallas SUPER för användaren. Den här behörighetsuppsättningen gör att användaren kan komma åt alla objekt som anges i licensen.<br /><br />
> En användare med Essential-licensen och SUPER behörighetsuppsättningen har tillgång till fler funktioner än användare med Team Member-licensen och behörighetsuppsättningen SUPER.

Du kan tilldela behörighetsuppsättningar till användare på två sätt:
- På sidan **Användarkort** genom att välja behörighetsuppsättningar att tilldela användaren.
- På sidan **Behörighetsuppsättning efter användare** genom att välja användare som en behörighetsuppsättning är tilldelad till.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Så här tilldelar du en behörighetsuppsättning till ett användarkort
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Markera den användare som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. I fönstret **Inkommande dokument** väljer du sidan **Användarkort**.
4. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. Mer information finns i avsnittet [Att skapa eller redigera en behörighetsuppsättning](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Så här tilldelar du en behörighetsuppsättning till sidan **Behörighetsuppsättning efter användare**  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. På sidan **användare** markerar du den relevanta användaren och väljer sedan åtgärden **Behörighetsuppsättning efter användare**.
3. På sidan **Behörighetsuppsättning efter användare** markerar du kryssrutan **[användarnamn]** på en rad för den aktuella behörighetsuppsättningen för att tilldela uppsättningen till användaren.
4. Markera kryssrutan **alla användare** om du vill tilldela behörighetsuppsättningen till alla användare.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Så här får du en översikt en användares behörigheter
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. Öppna kortet för relevant användare.
3. Välj åtgärden **Gällande behörigheter**.

    Dellistan **behörigheter** listar alla de databasobjekt som användaren har åtkomst till. Avsnittet kan inte redigeras.

    Delen **Efter behörighetsuppsättning** visar tilldelade behörighetsuppsättningarna genom vilka behörigheterna beviljas användaren, källa och typ för behörighetsuppsättningen och som utökar de olika typerna tillåts.

    För varje rad som du väljer i avsnittet **behörigheter** under avsnittet **Efter behörighetsuppsättning** visar vilken behörighetsuppsättning eller uppsättningar som har beviljats behörighet till. I detta avsnitt kan du redigera värdena i var och en av fem åtkomsttypfält **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**.

    > [!NOTE]  
    > Endast behörighetsgrupper av typen **användardefinierade** kan redigeras.<br /><br />
    > Rader med källberättigande kommer från prenumerationslicensen. Värdena på behörighetsvärdena för berättigandet åsidosätter värden i andra behörighetsuppsättningar om de har en högre rankning. Ett värde i en icke-berättigad behörighetsuppsättning som har en högre rankning än det relaterade värdet i berättigandet ska vara inom parentes för att ange att det inte är effektivt när det åsidosätts av berättigandet.<br /><br />
    > Mer information om rankning finns i avsnittet [Att skapa eller redigera behörigheter](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Om du vill redigera en behörighet, i **Efter behörighetsuppsättning**, på raden för en relevant behörighetsuppsättning av typen **Användardefinierad**, välj ett av fem åtkomstfält och välj ett annat värde.

5. Om du vill redigera enskilda behörigheter inom behörighetsuppsättningen väljer du värdet i fältet **behörighetsuppsättning** för att öppna sidan **behörigheter**. Följ stegen som beskrivs i avsnittet [Att skapa eller redigera behörigheter](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> När du redigerar en behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

## <a name="to-create-or-modify-a-permission-set"></a>Skapa eller ändra en behörighetsuppsättning
Behörighetsuppsättningar fungerar som behållare med behörigheter så att du enkelt kan hantera flera behörigheter i en post.

> [!NOTE]  
> En [!INCLUDE[d365fin](includes/d365fin_md.md)]-lösning innehåller vanligtvis ett antal fördefinierade behörighetsuppsättningar som läggs till av Microsoft eller av programvaruleverantören. Dessa behörighetsuppsättningar är av typen **System** eller **Tillägg**. Du kan inte skapa eller redigera sådana behörighetsuppsättningar eller behörigheter i dem. Du kan emellertid kopiera dem för att definiera egna behörighetsuppsättningar och behörigheter. <br /><br />
Behörighetsuppsättningar som användaren skapar från nya eller som kopior, är av typen **Användardefinierade** och kan redigeras.

### <a name="to-create-new-permission-set-from-scratch"></a>Så här skapar du en ny behörighetsuppsättning från början
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Behörighetsuppsättningar** och välj sedan relaterad länk.
2. För att skapa en ny behörighetsuppsättning, välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] När du har skapat en behörighetsuppsättning måste du lägga till de faktiska behörigheterna. Mer information finns i avsnittet [Skapa eller ändra behörigheter manuellt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Att kopiera behörighetsuppsättning
Du kan också använda en kopieringsfunktion för att snabbt kopiera alla behörigheterna från en annan behörighetsuppsättning till en ny behörighetsuppsättning.

> [!NOTE]  
> Om en systembehörighetsuppsättning som du har kopierat ändras kommer du att meddelas (beroende på vad du väljer), så att du kan överväga om ändringarna är relevanta för att kopieras eller skrivas till dina egna behörighetsuppsättning.

1. I sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Kopiera behörighetsuppsättning**.
2. I sidan **Kopiera behörighetsuppsättning** anger du namnet på den nya behörighetsuppsättning och väljer sedan knappen **OK**.
3. Markera kryssrutan **Meddela vid ändrad behörighetsuppsättning** om du vill ha en länk mellan de ursprungliga och de kopierade behörighetsuppsättningarna. Länken används sedan för att meddela dig om namn eller innehåll för den ursprungliga behörighetsuppsättningen i en kommande version att lösningen uppgraderas till senare.

Den nya behörighetsuppsättningen innehåller alla behörigheter för de kopierade grupp, läggs till som en ny rad på sidan **behörighetsuppsättningen**. Nu kan du ändra behörigheten i den nya behörighetsuppsättningen. Notera att raderna sorteras i bokstavsordning inom varje typ.

## <a name="to-create-or-modify-permissions-manually"></a>Skapa eller ändra behörigheter manuellt
Denna procedur förklarar hur man lägger till eller redigerar behörigheter manuellt. Du kan också få behörigheter genererade automatiskt utifrån dina åtgärder i användargränssnittet. Mer information finns i [Skapa eller ändra behörigheter genom att registrera dina åtgärder](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> När du redigerar en behörighet och därmed de relaterade behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

1. På sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Behörighet**.
2. På sidan **behörigheter**, skapa en ny rad och fyll i fälten på en befintlig rad.

I alla fält av typen de fem åtkomst **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**, kan du välja en med följande tre behörighetsalternativ:

|Alternativ|Description|Rankning|
|------|-----------|
|**Ja**|Användaren kan utföra åtgärden på det aktuella objektet.|Högsta|
|**Indirekt**|Användaren kan utföra åtgärden på det aktuella objektet, men endast via ett annat relaterat objekt som användaren har fullständig åtkomst till. Mer information om indirekta behörigheter finns i [Behörighetsegenskap](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) i Hjälp för utvecklare och IT-proffs|Andra högsta|
|**Tomt**|Användaren kan inte utföra åtgärden på det aktuella objektet.|Lägsta|

### <a name="example---indirect-permission"></a>Exempel - Indirekt behörighet
Du kan tilldela en indirekt behörighet för att använda en objekt endast via en annan objekt.
en användare kan till exempel har behörighet att köra Codeunit 80, försäljningspost. Kodmodulen försäljningspost utför många uppgifter, inklusive ändra tabell 37 inköpsrad. När användaren bokför ett försäljningsdokument, kontrollerar codeunit [!INCLUDE[d365fin](includes/d365fin_md.md)] om användaren har behörighet att ändra tabellen inköpsrad.  Om inte kan inte kodmodulen slutföra uppgiften, och användaren tar emot ett felmeddelande. I så fall, kör Codeunit korrekt.

Användaren behöver dock inte ha fullständig åtkomst till tabellen inköpsrad för att köra kodmodulen. Om användaren har indirekt behörighet till tabellen inköpsrad körs codeunit försäljningspost korrekt. När en användare har indirekt behörighet kan användaren endast ändra tabellen inköpsrad genom att köra kodmodulen försäljningspost eller ett annat objekt som har behörighet att ändra tabellen inköpsrad. Användaren kan endast ändra tabellen inköpsrad när det görs från moduler som stöds. Användaren kan inte köra funktionen oavsiktligt eller på ett skadligt sätt med andra metoder.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Skapa eller ändra behörigheter genom att registrera dina åtgärder
1.    Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Behörighetsuppsättningar** och välj sedan relaterad länk.
2.    Alternativt kan du i sidan **Användare** välja åtgärden **Behörighetsuppsättningar**.
3.    På sida **Behörighetsuppsättningar** väljer du åtgärden **Ny**.
4.    Fyll i fälten på en ny rad efter behov.
5.    Välj åtgärden **Behörigheter**.
6.    På sidan **behörigheter** väljer åtgärden **postbehörigheter** och välj sedan åtgärden **startar**.

    Detta startar en registreringsprocess som fångar alla dina åtgärder i användargränssnittet.
7.    Gå till olika sidor och aktiviteter i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vill att användare med denna behörighetsuppsättning ska lägga till. Du måste utföra de aktiviteter som du vill registrera behörigheter för.
8.    Om du vill avsluta registreringen går du tillbaka till sidan **behörigheter** och väljer åtgärden **stoppa**.
9.    Välj knappen **Ja** om du vill lägga till registrerade behörigheter till den nya behörighetsuppsättningen.
10.    För varje objekt i den registrerade listan anger du om användarna ska kunna infoga, ändra eller ta bort poster i de registrerade tabellerna.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Säkerhetsfilter – begränsa användarens åtkomst till specifika poster i en tabell
För postnivåsäkerhet i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du använda säkerhetsfilter för att begränsa användarens åtkomst till data i en tabell. Du kan skapa säkerhetsfilter på tabelldata. Ett säkerhetsfilter beskriver en uppsättning poster i en tabell som en användare har behörighet att komma åt. Du kan till exempel ange att en användare endast kan läsa de poster som innehåller information om en viss kund. Det innebär att användaren inte kan komma åt de poster som innehåller information om andra kunder. Mer information finns i [Använda säkerhetsfilter](/dynamics365/business-central/dev-itpro/security/security-filters) i hjälpen för utvecklare och IT-proffs.

## <a name="to-manage-permissions-through-user-groups"></a>Hantera behörigheter via användargrupper
Du kan skapa användargrupper för att hantera behörighetsuppsättningar för grupper av användare i företaget.

Du börjar med att skapa en användargrupp. Sedan tilldelar du gruppen behörighetsuppsättningar för att definiera vilka objekt som användare av gruppen ska få åtkomst till. När du lägger till användare i gruppen gäller de behörighetsuppsättningar som har definierats för gruppen för användaren.

Behörighetsuppsättningar som tilldelats till en användare via en användargrupp förblir synkroniserade så att en ändring av användargruppens behörigheter sprids automatiskt till användaren. Om du tar bort en användare från en användargrupp återkallas de berörda behörigheterna automatiskt.

### <a name="to-group-users-in-user-groups"></a>Gruppera användare i användargrupper
I proceduren nedan beskrivs hur du skapar användargrupper manuellt. Information om hur du skapar användargrupper automatiskt finns i [Kopiera en användargrupp och dess behörighetsuppsättningar](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användargrupper** och välj sedan relaterad länk.
2. Alternativt kan du i sidan **Användare** välja åtgärden **Användargrupper**.
3. På sidan **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.
4. På sidan **Användargrupp** väljer du åtgärden **Lägg användare**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Om du vill kopiera en användargrupp och dess behörighetsuppsättningar
Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..

> [!NOTE]
> Medlemmarna i användargruppen kopieras inte till den nya användargruppen. Du måste lägga till dem manuellt i efterhand. Mer information finns i avsnittet [För gruppanvändare i användargrupper](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användargrupper** och välj sedan relaterad länk.
2. Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.
3. I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.

Användargruppen läggs till i sidan **Användargrupper**. Fortsätt med att lägga till användare. Mer information finns i avsnittet [För gruppanvändare i användargrupper](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Tilldela behörighetsuppsättningar till användargrupper
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användargrupper** och välj sedan relaterad länk.
2. Markera den användargrupp som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. Välj åtgärden **Användarbehörighetsuppsättning** för att öppna sidan **Användarbehörighetsuppsättning**.
4. På sidan **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Tilldela en behörighetsuppsättning på sidan **Behörighetsuppsättning efter användargrupp**  
I proceduren nedan beskrivs hur du tilldelar behörighetsuppsättningar till en användargrupp på sidan **Behörighetsuppsättning efter användargrupp**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
2. På sidan **Användare** väljer du den relevanta användaren och väljer sedan åtgärden **Behörighetsuppsättning efter användargrupp**.
3. På sidan **Behörighetsuppsättning efter användargrupp** markerar du kryssrutan **[användarnamn]** på en rad för den relevanta behörighetsuppsättningen för att tilldela uppsättningen till användargruppen.
4. Markera kryssrutan **Alla användargrupper** om du vill tilldela behörighetsuppsättningen till alla användargrupper.

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare
Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad. Administratörer kan också tilldela ansvarsenheter till användare. För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användarinställningar** och välj sedan relaterad länk.
2. I sidan **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="see-also"></a>Se även
[Skapa användare enligt licenser](ui-how-users-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Säkerhet och skydd i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjälpen för utvecklare och IT-proffs
