---
title: "Tilldela användarbehörigheter och skapa eller ändra behörighetsgrupper | Microsoft Docs"
description: "Beskriver hur du lägger till Office 365-användare till Dynamics 365 Business edition och tilldelar dem behörigheter, åtkomstbehörigheter och säkerhetsinställningar."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f1b43879d6dafd238b593c6d17d2322943d75a89
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-manage-users-and-permissions"></a>Så här hanterar du användare och behörigheter
Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

När användare skapas i Office 365, kan de importeras till fönstret **Användare** med åtgärden **Få användare från Office 365**. Användare tilldelas behörighetsuppsättningar beroende på planen som tilldelats användaren i Office 365.

Du kan sedan tilldela behörighetsuppsättningar för användarna för att definiera vilka databasobjekt, och därmed vilka gränssnittselement, de har tillgång till och i vilka företag.

En behörighetsuppsättning är en samling behörigheter för specifika objekt i databasen. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Flera fördefinierade behörighetsuppsättningar levereras som standard. Du kan använda dessa behörighetsuppsättningar som redan har definierats, ändra standardbehörighetsuppsättningarna eller skapa ytterligare behörighetsuppsättningar.

Du kan lägga till användare i användargrupper. Detta gör det enklare att tilldela samma behörighetsuppsättning till flera användare.

Administratörer kan använda fönstret **Användarinställningar** för att definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad.

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på Suite. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

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

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare
Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad. Administratörer kan också tilldela ansvarsenheter till användare. För mer information, se [Så här: arbeta med Ansvarsenheter](inventory-responsibility-centers.md).

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.
2. I fönstret **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="see-also"></a>Se även
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Installation och administration i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](admin-setup-and-administration.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeta med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  

