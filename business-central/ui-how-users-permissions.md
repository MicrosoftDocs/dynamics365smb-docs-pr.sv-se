---
title: "Tilldela eller redigera användarbehörigheter | Microsoft Docs"
description: "Beskriver hur du lägger till Office 365-användare till Business Central och tilldelar dem behörigheter, åtkomstbehörigheter och säkerhetsinställningar."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 58077ae917d7943e6dd2da06847dfbb0eef5defd
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="managing-users-and-permissions"></a>Hantera användare och behörigheter
Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://aka.ms/CreateOffice365Users)

När användare skapas i Office 365, kan de importeras till fönstret **användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Användare tilldelas behörighetsuppsättningar beroende på planen som tilldelats användaren i Office 365. Mer information om licenser finns i [Licensieringsguide för Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Du kan sedan tilldela behörighetsuppsättningar för användarna för att definiera vilka databasobjekt, och därmed vilka gränssnittselement, de har tillgång till och i vilka företag. Du kan lägga till användare i användargrupper. Detta gör det enklare att tilldela samma behörighetsuppsättning till flera användare.

En behörighetsuppsättning är en samling behörigheter för specifika objekt i databasen. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)].

Från fönstret **användarkort** kan du öppna fönstret **gällande behörigheter** för att visa vilka behörigheter som användaren har och behörighetsgrupper de ges. Här kan du också ändra behörighetsinformation om behörighetsgrupper av typen **Användaranpassade**. Mer information finns i avsnittet ”Att visa eller redigera en användares behörigheter”.

Administratörer kan använda fönstret **Användarinställningar** för att definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad.

Ett annat system som definierar vilka användare kan komma åt Upplevelsemiljön. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Lägga till en användare i Business Central
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Välj åtgärden **Skaffa användare från Office 365**.

Alla nya användare som har skapats för din Office 365-prenumerationen kommer att läggas till i fönstret **användare**.

## <a name="to-group-users-in-a-user-group"></a>Gruppera användare i en användargrupp
Du kan skapa användargrupper för att hantera behörighetsuppsättningar för grupper av användare i företaget.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Användargrupper** och välj sedan relaterad länk.
2. Alternativt kan du i fönstret **Användare** välja åtgärden **Användargrupper**.
3. I fönstret **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.
4. I fönstret **Användargrupp** väljer du åtgärden **Lägg till användare**.

När användare eller användargrupper har skapats, måste du tilldela behörighetsuppsättningar till varje för att definiera vilka objekt en användare kan komma åt. Först måste du ordna de relevanta behörigheterna i behörighetsuppsättningar. Mer information finns i avsnittet ”Att skapa eller redigera en behörighetsuppsättning”.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Om du vill kopiera en användargrupp och dess behörighetsuppsättningar
Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..

Medlemmarna i användargruppen kopieras inte till den nya användargruppen. Du måste lägga till dem manuellt i efterhand.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Användargrupper** och välj sedan relaterad länk.
2. Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.
3. I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.

Användargruppen läggs till i fönstret **Användargrupper**. Fortsätt med att lägga till användare. Mer information finns i avsnittet ”För gruppanvändare i användargrupper”.  

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare
Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad. Administratörer kan också tilldela ansvarsenheter till användare. För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användarinställning** och välj sedan relaterad länk.
2. I fönstret **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="to-create-or-edit-a-permission-set"></a>Att skapa eller redigera en behörighetsuppsättning
Behörighetsuppsättningar fungerar som behållare med behörigheter så att du enkelt kan hantera flera behörigheter i en post. När du har skapat en behörighetsuppsättning måste du lägga till de faktiska behörigheterna. Mer information finns i avsnittet ”Att skapa eller redigera behörigheter”.

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

1. I fönstret **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Kopiera behörighetsuppsättning**.
2. I fältet **Kopiera behörighetsuppsättning** anger du namnet på den nya behörighetsuppsättning och väljer sedan knappen **OK**.
3. Markera kryssrutan **Meddela vid ändrad behörighetsuppsättning** om du vill ha en länk mellan de ursprungliga och de kopierade behörighetsuppsättningarna. Länken används sedan för att meddela dig om namn eller innehåll för den ursprungliga behörighetsuppsättningen i en kommande version att lösningen uppgraderas till senare.

Den nya behörighetsuppsättningen innehåller alla behörigheter för de kopierade grupp, läggs till som en ny rad i fönstret **behörighetsuppsättningen**. Notera att raderna sorteras i bokstavsordning inom varje typ.

## <a name="to-create-or-edit-permissions"></a>Att skapa eller redigera en behörigheter
1. I fönstret **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Behörighet**.
2. I fönstret **behörigheter**, skapa en ny rad och fyll i fälten på en befintlig rad.

I alla fält av typen de fem åtkomst **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**, kan du välja en med följande tre behörighetsalternativ:

|Alternativ|Description|Rankning|
|------|-----------|
|**Ja**|Användaren kan utföra åtgärden på det aktuella objektet.|Högsta|
|**Indirekt**|Användaren kan utföra åtgärden på det aktuella objektet, men endast via ett annat relaterat objekt som användaren har fullständig åtkomst till.|Andra högsta|
|**Tomt**|Användaren kan inte utföra åtgärden på det aktuella objektet.|Lägsta|

> [!NOTE]  
> När du redigerar en behörighet och därmed de relaterade behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Om du vill tilldela behörighetsuppsättningar till användare eller användargrupper
Du kan tilldela behörigheter till användare på två sätt:
- Definiera behörighetsuppsättningar på användarens användarkort.
- Markera kryssrutan för en användare, på en kolumn, för en relaterad behörighetsuppsättning, på en rad i fönstret **Behörighetsuppsättning efter användare**.
    Med denna metod kan du också tilldela behörighetsuppsättningar till användargrupper.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Så här tilldelar du en behörighetsuppsättning till ett användarkort
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Markera den användare som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. I fönstret **Inkommande dokument** väljer du åtgärden **Användarkort**.
4. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. Mer information finns i avsnittet ”Att skapa eller redigera en behörighetsuppsättning”.

### <a name="to-assign-a-permission-set-in-the-permission-set-by-user-window"></a>Så här tilldelar du en behörighetsuppsättning till fönstret **Behörighetsuppsättning efter användare**  
I proceduren nedan beskrivs hur du tilldelar behörighetsuppsättningar till en användare i fönstret **Behörighetsuppsättning efter användare**. Stegen är liknande i fönstret **Behörighetsuppsättning efter användargrupp**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. I fönstret **användare** markerar du den relevanta användaren och väljer sedan åtgärden **Behörighetsuppsättning efter användare**.
3. I fönstret **Behörighetsuppsättning efter användare** markerar du kryssrutan **[användarnamn]** på en rad för den aktuella behörighetsuppsättningen för att tilldela uppsättningen till användaren.
4. Markera kryssrutan **alla användare** om du vill tilldela behörighetsuppsättningen till alla användare.

## <a name="to-view-or-edit-a-users-permissions"></a>Visa eller redigera en användares behörigheter
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
2. Öppna kortet för relevant användare.
3. Välj åtgärden **Gällande behörigheter**.

    Dellistan **behörigheter** listar alla de databasobjekt som användaren har åtkomst till. Avsnittet kan inte redigeras.

    Delen **Efter behörighetsuppsättning** visar tilldelade behörighetsuppsättningarna genom vilka behörigheterna beviljas användaren, källa och typ för behörighetsuppsättningen och som utökar de olika typerna tillåts.

    För varje rad som du väljer i avsnittet **behörigheter** under avsnittet **Efter behörighetsuppsättning** visar vilken behörighetsuppsättning eller uppsättningar som har beviljats behörighet till. I detta avsnitt kan du redigera värdena i var och en av fem åtkomsttypfält **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**.   

    > [!NOTE]  
    > Endast behörighetsgrupper av typen **användardefinierade** kan redigeras.<br /><br />
    > Rader av källberättigande kommer från prenumerationsplanen. Värdena på behörighetsvärdena för berättigandet åsidosätter värden i andra behörighetsuppsättningar om de har en högre rankning. Ett värde i en icke-berättigad behörighetsuppsättning som har en högre rankning än det relaterade värdet i berättigandet ska vara inom parentes för att ange att det inte är effektivt när det åsidosätts  av berättigandet. Mer information om rankning finns i avsnittet ”Att skapa eller redigera behörigheter”.  

4. Om du vill redigera en behörighet, i **Efter behörighetsuppsättning**, på raden för en relevant behörighetsuppsättning av typen **Användardefinierad**, välj ett av fem åtkomstfält och välj ett annat värde.

5. Om du vill redigera enskilda behörigheter inom behörighetsuppsättningen väljer du värdet i fältet **behörighetsuppsättning** för att öppna fönstret **behörigheter**. Följ stegen som beskrivs i avsnittet ”Att skapa eller redigera behörigheter”.  

> [!NOTE]  
> När du redigerar en behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

## <a name="see-also"></a>Se även
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)   
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central – Licencieringsguide](https://aka.ms/BusinessCentralLicensing)

