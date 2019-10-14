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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 51c8c4207d9b5311698c7c5575fc67d8c5b2df9d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310906"
---
# <a name="manage-users-and-permissions"></a>Hantera användare och behörigheter
Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://aka.ms/CreateOffice365Users)

När användare skapas i Office 365, kan de importeras till sidan **användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Användare tilldelas behörighetsuppsättningar beroende på planen som tilldelats användaren i Office 365. Mer information om licenser finns i [Microsoft Dynamics 365 Business Central licensieringsguide](https://aka.ms/BusinessCentralLicensing).

Du kan sedan tilldela behörighetsuppsättningar för användarna för att definiera vilka databasobjekt, och därmed vilka gränssnittselement, de har tillgång till och i vilka företag. Du kan lägga till användare i användargrupper. Detta gör det enklare att tilldela samma behörighetsuppsättning till flera användare.

En behörighetsuppsättning är en samling behörigheter för specifika objekt i databasen. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)].

Från sidan **användarkort** kan du öppna sidan **gällande behörigheter** för att visa vilka behörigheter som användaren har och behörighetsgrupper de ges. Här kan du också ändra behörighetsinformation om behörighetsgrupper av typen **Användaranpassade**. Mer information finns i avsnittet [Så här får du en översikt en användares behörigheter](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="users-in-on-premises-deployments"></a>Användare av lokala distributioner
Vid lokal distribution av [!INCLUDE[d365fin](includes/d365fin_md.md)], kan administratören välja mellan olika autentiseringsmetoder för användare. När du sedan skapar en användare, tillhandahåller du olika information beroende på vilken autentiseringstyp du använder i den specifika [!INCLUDE[server](includes/server.md)]-instansen. Mer information finns på [autentisering och autentisering](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i avsnittet Administration av utvecklare och ITPro-innehåll för [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="profiles"></a>Profiler
När du har lagt till användare kan du ange vad de ska se i användargränssnittet och hur de interagerar med deras tillåtna funktioner via sidor. Du gör detta genom profiler, reflekterande roller eller avdelningar, som du tilldelar olika typer av användare. Mer information finns i [Hantera profiler](admin-users-profiles-roles.md) och [anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md).

## <a name="to-add-a-user-in-business-central"></a>Lägga till en användare i Business Central
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Välj åtgärden **Skaffa användare från Office 365**.

Alla nya användare som har skapats för din Office 365-prenumerationen kommer att läggas till i sidan **användare**.

## <a name="to-edit-or-delete-a-user"></a>Så här redigerar du en användare
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Markera användaren som du vill redigera och välj åtgärden **Redigera**.
3. På sidan **användarkort** ändrar du informationen efter behov.    
4. Om du vill radera en användare, väljer du användaren du vill radera och välj sedan åtgärden **Radera**.

## <a name="to-group-users-in-user-groups"></a>Gruppera användare i användargrupper
Du kan skapa användargrupper för att hantera behörighetsuppsättningar för grupper av användare i företaget.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Användargrupper** och välj sedan relaterad länk.
2. Alternativt kan du i sidan **Användare** välja åtgärden **Användargrupper**.
3. På sidan **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.
4. På sidan **Användargrupp** väljer du åtgärden **Lägg användare**.

När användare eller användargrupper har skapats, måste du tilldela behörighetsuppsättningar till varje för att definiera vilka objekt en användare kan komma åt. Först måste du ordna de relevanta behörigheterna i behörighetsuppsättningar. Mer information finns i avsnittet [Så här får du en översikt en användares behörigheter](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Om du vill kopiera en användargrupp och dess behörighetsuppsättningar
Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..

Medlemmarna i användargruppen kopieras inte till den nya användargruppen. Du måste lägga till dem manuellt i efterhand.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Användargrupper** och välj sedan relaterad länk.
2. Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.
3. I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.

Användargruppen läggs till i sidan **Användargrupper**. Fortsätt med att lägga till användare. Mer information finns i avsnittet [För gruppanvändare i användargrupper](ui-how-users-permissions.md#to-group-users-in-user-groups).  

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare
Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad. Administratörer kan också tilldela ansvarsenheter till användare. För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användarinställning** och välj sedan relaterad länk.
2. I sidan **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="to-create-or-modify-a-permission-set"></a>Skapa eller ändra en behörighetsuppsättning
Behörighetsuppsättningar fungerar som behållare med behörigheter så att du enkelt kan hantera flera behörigheter i en post. När du har skapat en behörighetsuppsättning måste du lägga till de faktiska behörigheterna. Mer information finns i avsnittet [Att skapa eller redigera behörigheter manuellt](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> En [!INCLUDE[d365fin](includes/d365fin_md.md)]-lösning innehåller vanligtvis ett antal fördefinierade behörighetsuppsättningar som läggs till av Microsoft eller av programvaruleverantören. Dessa behörighetsuppsättningar är av typen **System** eller **Tillägg**. Du kan inte skapa eller redigera sådana behörighetsuppsättningar eller behörigheter i dem. Du kan emellertid kopiera dem för att definiera egna behörighetsuppsättningar och behörigheter. <br /><br />
Behörighetsuppsättningar som användaren skapar från nya eller som kopior, är av typen **Användardefinierade** och kan redigeras.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **behörighetsuppsättningar** och välj sedan relaterad länk.
2. För att skapa en ny behörighetsuppsättning, välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Att kopiera behörighetsuppsättning
När du skapar nya behörighetsuppsättningar kan du använda en kopieringsfunktion för att snabbt utföra alla behörigheterna till en annan behörighetsuppsättning för att lägga till en ny behörighetsuppsättning.

> [!NOTE]  
> Om en systembehörighetsuppsättning som du har kopierat ändras kommer du att meddelas (beroende på vad du väljer), så att du kan överväga om ändringarna är relevanta för att kopieras eller skrivas till dina egna behörighetsuppsättning.

1. I sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Kopiera behörighetsuppsättning**.
2. I sidan **Kopiera behörighetsuppsättning** anger du namnet på den nya behörighetsuppsättning och väljer sedan knappen **OK**.
3. Markera kryssrutan **Meddela vid ändrad behörighetsuppsättning** om du vill ha en länk mellan de ursprungliga och de kopierade behörighetsuppsättningarna. Länken används sedan för att meddela dig om namn eller innehåll för den ursprungliga behörighetsuppsättningen i en kommande version att lösningen uppgraderas till senare.

Den nya behörighetsuppsättningen innehåller alla behörigheter för de kopierade grupp, läggs till som en ny rad på sidan **behörighetsuppsättningen**. Notera att raderna sorteras i bokstavsordning inom varje typ.

## <a name="to-create-or-modify-permissions-manually"></a>Skapa eller ändra behörigheter manuellt
Denna procedur förklarar hur man lägger till eller redigerar behörigheter manuellt. Du kan också välja en behörighetuppsättningar skapas automatiskt utifrån dina åtgärder i användargränssnittet. Mer information finns i avsnittet [Att skapa eller ändra behörighetsgrupper genom att registrera åtgärderna](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. På sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Behörighet**.
2. På sidan **behörigheter**, skapa en ny rad och fyll i fälten på en befintlig rad.

I alla fält av typen de fem åtkomst **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**, kan du välja en med följande tre behörighetsalternativ:

|Alternativ|Description|Rankning|
|------|-----------|
|**Ja**|Användaren kan utföra åtgärden på det aktuella objektet.|Högsta|
|**Indirekt**|Användaren kan utföra åtgärden på det aktuella objektet, men endast via ett annat relaterat objekt som användaren har fullständig åtkomst till.|Andra högsta|
|**Tomt**|Användaren kan inte utföra åtgärden på det aktuella objektet.|Lägsta|

### <a name="example---indirect-permission"></a>Exempel - Indirekt behörighet
Du kan tilldela en indirekt behörighet för att använda en objekt endast via en annan objekt.
en användare kan till exempel har behörighet att köra Codeunit 80, försäljningspost. Kodmodulen försäljningspost utför många uppgifter, inklusive ändra tabell 37 inköpsrad. När användaren bokför ett försäljningsdokument, kontrollerar codeunit [!INCLUDE[d365fin](includes/d365fin_md.md)] om användaren har behörighet att ändra tabellen inköpsrad.  Om inte kan inte kodmodulen slutföra uppgiften, och användaren tar emot ett felmeddelande. I så fall, kör Codeunit korrekt.

Användaren behöver dock inte ha fullständig åtkomst till tabellen inköpsrad för att köra kodmodulen. Om användaren har indirekt behörighet till tabellen inköpsrad körs codeunit försäljningspost korrekt. När en användare har indirekt behörighet kan användaren endast ändra tabellen inköpsrad genom att köra kodmodulen försäljningspost eller ett annat objekt som har behörighet att ändra tabellen inköpsrad. Användaren kan endast ändra tabellen inköpsrad när det görs från moduler som stöds. Användaren kan inte köra funktionen oavsiktligt eller på ett skadligt sätt med andra metoder.

## <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Att begränsa användarens åtkomst till specifika poster i en tabell
För postnivåsäkerhet i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du använda säkerhetsfilter för att begränsa användarens åtkomst till data i en tabell. Du kan skapa säkerhetsfilter på tabelldata. Ett säkerhetsfilter beskriver en uppsättning poster i en tabell som en användare har behörighet att komma åt. Du kan till exempel ange att en användare endast kan läsa de poster som innehåller information om en viss kund. Det innebär att användaren inte kan komma åt de poster som innehåller information om andra kunder. Mer information finns i [Använda säkerhetsfilter](/dynamics365/business-central/dev-itpro/security/security-filters) i hjälpen för utvecklare och IT-proffs.


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Om du vill skapa eller ändra behörighet när du registrerar dina åtgärder
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **behörighetsuppsättningar** och välj sedan relaterad länk.
2.  Alternativt kan du i sidan **Användare** välja åtgärden **Behörighetsuppsättningar**.
3.  På sida **Behörighetsuppsättningar** väljer du åtgärden **Ny**.
4.  Fyll i fälten på en ny rad efter behov.
5.  Välj åtgärden **Behörigheter**.
6.  På sidan **behörigheter** väljer åtgärden **postbehörigheter** och välj sedan åtgärden **startar**.

    Detta startar en registreringsprocess som fångar alla dina åtgärder i användargränssnittet.
7.  Gå till olika sidor och aktiviteter i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vill att användare med denna behörighetsuppsättning ska lägga till. Du måste utföra de aktiviteter som du vill registrera behörigheter för.
8.  Om du vill avsluta registreringen går du tillbaka till sidan **behörigheter** och väljer åtgärden **stoppa**.
9.  Välj knappen **Ja** om du vill lägga till registrerade behörigheter till den nya behörighetsuppsättningen.
10. För varje objekt i den registrerade listan anger du om användarna ska kunna infoga, ändra eller ta bort poster i de registrerade tabellerna.

> [!NOTE]  
> När du redigerar en behörighet och därmed de relaterade behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Om du vill tilldela behörighetsuppsättningar till användare eller användargrupper
Du kan tilldela behörigheter till användare på två sätt:
- Definiera behörighetsuppsättningar på användarens användarkort.
- Markera kryssrutan för en användare, på en kolumn, för en relaterad behörighetsuppsättning, på en rad på sidan **Behörighetsuppsättning efter användare**.
    Med denna metod kan du också tilldela behörighetsuppsättningar till användargrupper.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Så här tilldelar du en behörighetsuppsättning till ett användarkort
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Markera den användare som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. I fönstret **Inkommande dokument** väljer du sidan **Användarkort**.
4. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. Mer information finns i avsnittet [Att skapa eller redigera en behörighetsuppsättning](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Så här tilldelar du en behörighetsuppsättning till sidan **Behörighetsuppsättning efter användare**  
I proceduren nedan beskrivs hur du tilldelar behörighetsuppsättningar till en användare på sidan **Behörighetsuppsättning efter användare**. Stegen är liknande på sidan **Behörighetsuppsättning efter användargrupp**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. På sidan **användare** markerar du den relevanta användaren och väljer sedan åtgärden **Behörighetsuppsättning efter användare**.
3. På sidan **Behörighetsuppsättning efter användare** markerar du kryssrutan **[användarnamn]** på en rad för den aktuella behörighetsuppsättningen för att tilldela uppsättningen till användaren.
4. Markera kryssrutan **alla användare** om du vill tilldela behörighetsuppsättningen till alla användare.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Så här får du en översikt en användares behörigheter
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Öppna kortet för relevant användare.
3. Välj åtgärden **Gällande behörigheter**.

    Dellistan **behörigheter** listar alla de databasobjekt som användaren har åtkomst till. Avsnittet kan inte redigeras.

    Delen **Efter behörighetsuppsättning** visar tilldelade behörighetsuppsättningarna genom vilka behörigheterna beviljas användaren, källa och typ för behörighetsuppsättningen och som utökar de olika typerna tillåts.

    För varje rad som du väljer i avsnittet **behörigheter** under avsnittet **Efter behörighetsuppsättning** visar vilken behörighetsuppsättning eller uppsättningar som har beviljats behörighet till. I detta avsnitt kan du redigera värdena i var och en av fem åtkomsttypfält **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**.   

    > [!NOTE]  
    > Endast behörighetsgrupper av typen **användardefinierade** kan redigeras.<br /><br />
    > Rader av källberättigande kommer från prenumerationsplanen. Värdena på behörighetsvärdena för berättigandet åsidosätter värden i andra behörighetsuppsättningar om de har en högre rankning. Ett värde i en icke-berättigad behörighetsuppsättning som har en högre rankning än det relaterade värdet i berättigandet ska vara inom parentes för att ange att det inte är effektivt när det åsidosätts  av berättigandet. Mer information om rankning finns i avsnittet [Att skapa eller redigera behörigheter](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. Om du vill redigera en behörighet, i **Efter behörighetsuppsättning**, på raden för en relevant behörighetsuppsättning av typen **Användardefinierad**, välj ett av fem åtkomstfält och välj ett annat värde.

5. Om du vill redigera enskilda behörigheter inom behörighetsuppsättningen väljer du värdet i fältet **behörighetsuppsättning** för att öppna sidan **behörigheter**. Följ stegen som beskrivs i avsnittet [Att skapa eller redigera behörigheter](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> När du redigerar en behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

## <a name="to-remove-a-users-access-to-the-system"></a>Så här tar du bort en användares åtkomst till systemet

Som administratör kan du ta bort en användares åtkomst till systemet genom att ställa in **status** till **inaktiverat**. Alla referenser till användaren behålls, men användaren kan inte längre logga in i systemet och aktiva sessioner för användaren avslutas. Om du vill ge användaren åtkomst igen, ställ in fältet **Status** till **Aktiveras**.

## <a name="see-also"></a>Se även
[Säkerhet och skydd i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central licensieringsguide](https://aka.ms/BusinessCentralLicensing)
