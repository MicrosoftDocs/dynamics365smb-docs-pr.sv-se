---
title: "Tilldela användarbehörigheter och skapa eller ändra behörighetsgrupper | Microsoft Docs"
description: "Beskriver hur du lägger till Office 365-användare till Financials och tilldelar dem behörigheter, åtkomstbehörigheter och säkerhetsinställningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 564ef68a1571611efee32db1cf3759cda6a04c80
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Så här hanterar du användare och behörigheter
Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

När användare skapas i Office 365, kan de importeras till fönstret **användare** med åtgärden **Få användare från Office 365**. Användare tilldelas behörighetsuppsättningar beroende på planen som tilldelats användaren i Office 365.

Du kan sedan tilldela behörighetsuppsättningar för användarna för att definiera vilka databasobjekt, och därmed vilka gränssnittselement, de har tillgång till och i vilka företag.

En behörighetsuppsättning är en samling behörigheter för specifika objekt i databasen. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Flera fördefinierade behörighetsuppsättningar levereras som standard. Du kan använda dessa behörighetsuppsättningar som redan har definierats, ändra standardbehörighetsuppsättningarna eller skapa ytterligare behörighetsuppsättningar.

Du kan lägga till användare i användargrupper. Detta gör det enklare att tilldela samma behörighetsuppsättning till flera användare.

Administratörer kan använda fönstret **Användarinställningar** för att definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad.

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på Paket. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Så här tilldelar du behörigheter till en användare
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. Markera den användare som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. I fönstret **Inkommande dokument** väljer du åtgärden **Användarkort**.
4. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Gruppera användare i användargrupper
Du kan skapa användargrupper för att hantera behörighetsuppsättningar för grupper av användare i företaget. Du kan använda en funktion för att kopiera alla behörighetsuppsättningar från en befintlig grupp i den nya användargruppen. Användargruppmedlemmar kopieras emellertid inte.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. Alternativt kan du i fönstret **Användare** välja åtgärden **Användargrupper**.
3. I fönstret **användargrupper** väljer du en befintlig grupp som du vill kopiera och väljer sedan åtgärden **kopiera användargrupp** åtgärd.
4. I fältet **Ny användarkod** anger du namnet på den nya gruppen och väljer sedan knappen **OK**.

    I stället för att kopiera, kan du välja den åtgärden Ny för att skapa en ny rad för en tom användargrupp, som du sedan fyller i manuellt.
5. Om du villl lägga till ytterligare användare väljer du i fönstret **Användargrupp** åtgärden **Medlemmar i användargrupp**.
6. I fönstret **Medlemmar i användargrupp** på en ny rad fyller du i fälten efter behov genom att välja från befintliga användare.
7. Om du villl lägga till ytterligare behörighetsuppsättningar väljer du i fönstret **Användargrupp** åtgärden **Behörighetsuppsättningar för användargrupp**.
8. I fönstret **Behörighetsuppsättningar för användargrupp** på en ny rad fyller du i fälten efter behov genom att välja från befintliga behörighetsuppsättningar.

## <a name="to-create-or-modify-permission-sets"></a>Skapa eller ändra behörighetsuppsättningar
Om standardbehörighetsuppsättningarna, som tillhandahålls av [!INCLUDE[d365fin](includes/d365fin_md.md)] inte är tillräckliga eller inte lämpliga för organisationen, kan du skapa nya behörighetsuppsättningar. Och om enskilda objektbehörigheter, som definierar en behörighetsuppsättning, inte är lämplig, kan du ändra en behörighetsuppsättning. Du kan skapa en behörighetsuppsättning manuellt eller använda en registreringsfunktion som registrerar dina åtgärder när du navigerar genom ett scenario och sedan skapar den krävda behörighetsuppsättningen.

### <a name="to-create-or-modify-permission-sets-manually"></a>Skapa eller ändra behörighetsuppsättningar manuellt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. I fönstret **Användare** väljer du åtgärden **Behörighetsuppsättningar**.
3. I fönstret **Behörighetsuppsättningar** väljer du åtgärden **Ny**.
4. Fyll i fälten på en ny rad efter behov.
5. Välj åtgärden **Behörigheter**.
6. I fönstret **Behörigheter** fyller du i fälten på rubriken efter behov.
7. På en ny rad fyller du i de fem fälten för de olika behörighetstyperna enligt beskrivningen i följande tabell.

    |Alternativ|Beskrivning|
    |------|-----------|
    |Tomt|Anger vilken behörighetstyp som inte beviljas för objektet.|
    |**Ja**|Anger vilken behörighetstyp som inte beviljas med direkt åtkomst till objektet.|
    |**Indirekt**|Anger vilken behörighetstyp som inte beviljas med indirekt åtkomst till objektet.|

    Indirekt behörighet till en tabell innebär att du inte kan öppna tabellen och läsa från den, men du kan visa informationen i tabellen genom ett annat objekt, som till exempel en sida som du har direkt åtkomst till. Mer information finns i avsnittet “Exempel - indirekta behörigheter” i den här artikeln.

8. I fältet **säkerhetsfilter** anger du ett filter som du vill koppla till behörigheten genom att markera fältet när du vill begränsa en användares behörighet.

    Om du till exempel vill skapa ett säkerhetsfilter så att en användare endast kan visa försäljning med en viss säljarkod väljer du fältnumret för fälet **Säljarkod**. Sedan i fältet **Fältfilter** anger du värdet som du vill använda för att begränsa åtkomsten. Om du till exemepl vill begränsa en användares behörighet till endast Annette Hill försäljning, anger du AH.
9. Upprepa steg 7 och 8 om du vill lägga till behörigheter för extra objekt i behörighetsuppsättningen.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Om du vill skapa eller ändra behörighet när du registrerar dina åtgärder
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. I fönstret **Användare** väljer du åtgärden **Behörighetsuppsättningar**.
3. I fönstret **Behörighetsuppsättningar** väljer du åtgärden **Ny**.
4. Fyll i fälten på en ny rad efter behov.
5. Välj åtgärden **Behörigheter**.
6. I fönstret **Behörigheter** väljer du åtgärden **Starta**.

    En registreringsprocess börjar fånga in dina åtgärder i användargränssnittet.
7. Gå till olika fönster och aktiviteter i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vill att användare med denna behörighetsuppsättning ska lägga till. Du måste utföra de aktiviteter som du vill registrera behörigheter för.
8. Om du vill avsluta registreringen går du tillbaka till fönstret **behörigheter** och väljer åtgärden **stoppa**.
9. Välj knappen **Ja** om du vill lägga till registrerade behörigheter till den nya behörighetsuppsättningen.
10. För varje objekt i den registrerade listan anger du om användarna ska kunna infoga, ändra eller ta bort poster i de registrerade tabellerna. Se steg 7 i "Att skapa eller ändra behörighetsupsättningar manuellt".

### <a name="example---indirect-permission"></a>Exempel - Indirekt behörighet
Du kan tilldela en indirekt behörighet för att använda en objekt endast via en annan objekt.
en användare kan till exempel har behörighet att köra Kodmodul 80 **försäljningspost**. Kodmodulen **försäljningspost** utför många uppgifter, inklusive ändra tabell 37 **inköpsrad**. När användaren bokför ett försäljningsdokument, kontrollerar kodmodulen**försäljningspost**, [!INCLUDE[d365fin](includes/d365fin_md.md)] om användaren har behörighet att ändra tabellen **inköpsrad**. Om inte kan inte kodmodulen slutföra uppgiften, och användaren tar emot ett felmeddelande. I så fall, kör Codeunit korrekt.

Användaren behöver dock inte ha fullständig åtkomst till tabellen **inköpsrad** för att köra kodmodulen. Om användaren har indirekt behörighet till tabellen **inköpsrad** körs kodmodulen **försäljningspost** korrekt. När en användare har indirekt behörighet kan användaren endast ändra tabellen **inköpsrad** genom att köra kodmodulen **försäljningspost** eller ett annat objekt som har behörighet att ändra tabellen **inköpsrad**. Användaren kan endast ändra tabellen **inköpsrad** när det görs från moduler som stöds. Användaren kan inte köra funktionen oavsiktligt eller på ett skadligt sätt med andra metoder.

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare
Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad. Administratörer kan också tilldela ansvarsenheter till användare.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.
2. I fönstret **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="see-also"></a>Se även
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Välkommen till [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

