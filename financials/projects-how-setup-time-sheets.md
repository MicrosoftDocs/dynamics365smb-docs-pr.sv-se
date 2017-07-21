---
title: "Ställa in tidrapporter och deras godkännande | Microsoft Docs"
description: "Du lägger upp tidrapporter för att spåra den tid som använts för projekt och använder resurser kan hjälpa dig med projekthantering, personal och kapacitet"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3e85168709eb8e96b2ee2aea516189c2cf88d426
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-time-sheets"></a>Så här kan du skapa tidrapporter
Tidrapporter i [!INCLUDE[d365fin](includes/d365fin_md.md)] hanterar tidregistrering veckovis, med sju dagars steg i taget. Du kan använda dem för att spåra den tid som används för projektet och du kan använda dem för att registrera enkel resurstimregistrering. Innan du kan använda tidrapporter måste du ange hur du vill att de ska registreras och konfigureras.

När du har ställt in hur organisationen ska använda tidrapporter, kan du ange om och hur tidrapporter godkänns. Beroende på organisationens behov kan du ange:

* En eller flera användare som tidrapportsadministratör och godkännare för alla tidrapporter.
* En tidrapportsgodkännare för varje resurs.

När du har konfigurerat tidrapporter, kan du skapa tidrapporter för resurser, tilldela dem till projektplaneringsrader och bokföra tidrapportrader. Mer information finns i [Så här använder du tidrapporter](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Så här anger du allmän information för tidrapporter
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. För fältet **Tidrapport per projektgodkännande** väljer du ett av följande alternativ.

| Alternativ | Beskrivning |
| --- | --- |
| **Aldrig** |Användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet godkänner tidrapporten. |
| **Alltid** |Användaren i fältet **Ansvarig person** på projektkortet godkänner tidrapporten. |
| **Enbart maskin** |Om maskinens tidrapport är länkad till ett projekt, godkänner användaren i fältet **Ansvarig person** på projektkortet tidrapporten. Om maskinens tidrapport är länkad till en resurs, godkänner användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet tidrapporten. |

## <a name="to-assign-a-time-sheet-administrator"></a>Så här tilldelar du en tidrapportsadministratör
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.  
2. Lägg till en ny användare om användarlistan inte innehåller den person som du vill ska vara tidrapportsadministratören. Mer information finns i [Så här hanterar du användare och behörigheter](ui-how-users-permissions.md).
3. Välj en användare som ska vara en tidrapportadministratör och välj sedan kryssrutan **Tidrapportadmin.** .  

> [!TIP]  
>   Vi rekommenderar att du endast anger en användare som tidrapportsadministratör för ett företag. I följande procedur skapar du en tidrapportägare och godkännare där tidrapportgodkännaren tilldelas för varje resurs.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Så här tilldelar du en tidrapportsägare och en godkännare
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Resurser** och välj sedan relaterad länk.
2. Välj den resurs som du vill ställa in möjlighet att använda tidrapporter för och markera sedan kryssrutan **Använd tidrapport**.  
3. I fältet **Användar-ID för tidrapportens ägare** anger du ID för ägaren av tidrapporten. Ägaren kan ange tidförbrukning på en tidrapport och skicka den för godkännande. Vanligtvis, när resursen är en person, är den person också ägare.  
4. I fältet **Användar-ID för tidrapportens godkännare** anger du ID för godkännaren av tidrapporten. Godkännaren kan godkänna, avvisa eller öppna en tidrapport igen.  

> [!NOTE]  
>   Du kan inte ändra ID på tidrapportsgodkännaren om det finns tidrapporter som inte ännu har behandlats och har statusen **Skickad** eller **Öppen**.

## <a name="see-also"></a>Se även
[Ställ in projekthantering](projects-setup-projects.md)  
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

