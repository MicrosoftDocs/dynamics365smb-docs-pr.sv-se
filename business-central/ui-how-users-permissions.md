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
ms.date: 05/24/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: 443c04799e9aa2b9aa4ede15006ecb5e9773ce6b
ms.contentlocale: sv-se
ms.lasthandoff: 05/28/2018

---
# <a name="manage-users-and-permissions"></a>Hantera användare och behörigheter
Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

När användare skapas i Office 365, kan de importeras till fönstret **Användare** med åtgärden **Få användare från Office 365**. Användare tilldelas behörighetsuppsättningar beroende på planen som tilldelats användaren i Office 365.

Du kan sedan tilldela behörighetsuppsättningar för användarna för att definiera vilka databasobjekt, och därmed vilka gränssnittselement, de har tillgång till och i vilka företag. Du kan lägga till användare i användargrupper. Detta gör det enklare att tilldela samma behörighetsuppsättning till flera användare.

En behörighetsuppsättning är en samling behörigheter för specifika objekt i databasen. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Flera fördefinierade behörighetsuppsättningar levereras som standard.  

Administratörer kan använda fönstret **Användarinställningar** för att definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad.

Ett annat system som definierar vilka användare kan komma åt Upplevelsemiljön. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Så här tilldelar du behörigheter till en användare
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. Markera den användare som du vill tilldela behörighet till.
Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. I fönstret **Inkommande dokument** väljer du åtgärden **Användarkort**.
4. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Gruppera användare i användargrupper
Du kan skapa användargrupper för att hantera behörighetsuppsättningar för grupper av användare i företaget.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. Alternativt kan du i fönstret **Användare** välja åtgärden **Användargrupper**.
3. I fönstret **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.
6. I fönstret **Användargrupp** väljer du åtgärden **Lägg till användare**.
7. Om du vill lägga till ytterligare behörighetsuppsättningar väljer du i fönstret **Användargrupper** åtgärden **Behörighetsuppsättningar för användargrupp**.
8. I fönstret **Behörighetsuppsättningar för användargrupp** på en ny rad fyller du i fälten efter behov genom att välja från befintliga behörighetsuppsättningar.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Om du vill kopiera en användargrupp och dess behörighetsuppsättningar
Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..

Medlemmarna i användargruppen kopieras inte till den nya användargruppen. Du måste lägga till dem manuellt i efterhand.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.
2. Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.
3. I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.

Användargruppen läggs till i fönstret **Användargrupper**. Fortsätt med att lägga till användare. Mer information finns i avsnittet ”För gruppanvändare i användargrupper”.

## <a name="to-set-up-user-time-constraints"></a>Så här ställer du in tidsbegränsningar för användare
Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad. Administratörer kan också tilldela ansvarsenheter till användare. För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.
2. I fönstret **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="see-also"></a>Se även
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

