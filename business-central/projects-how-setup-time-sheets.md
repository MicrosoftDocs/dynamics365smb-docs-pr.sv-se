---
title: Ställa in tidrapporter och deras godkännande | Microsoft Docs
description: Du lägger upp tidrapporter för att spåra den tid som använts för projekt och använder resurser kan hjälpa dig med projekthantering, personal och kapacitet
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7851966211a666e6569bffa3082d05b7c3765434
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388405"
---
# <a name="set-up-time-sheets"></a>Så här skapar du tidrapporter
Tidrapporter i [!INCLUDE[prod_short](includes/prod_short.md)] hanterar tidregistrering veckovis, med sju dagars steg i taget. Du kan använda dem för att spåra den tid som används för projektet och du kan använda dem för att registrera enkel resurstimregistrering. Innan du kan använda tidrapporter måste du ange hur du vill att de ska registreras och konfigureras.

När du har ställt in hur organisationen ska använda tidrapporter, kan du ange om och hur tidrapporter godkänns. Beroende på organisationens behov kan du ange:

* En eller flera användare som tidrapportsadministratör och godkännare för alla tidrapporter.
* En tidrapportsgodkännare för varje resurs.

När du har konfigurerat tidrapporter, kan du skapa tidrapporter för resurser, tilldela dem till projektplaneringsrader och bokföra tidrapportrader. Mer information finns i [Så här använder du tidrapporter](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Så här anger du allmän information för tidrapporter
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Resursinställningar** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. För fältet **Tidrapport per projektgodkännande** väljer du ett av följande alternativ.

| Alternativ | Beskrivning |
| --- | --- |
| **Aldrig** |Användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet godkänner tidrapporten. |
| **Alltid** |Användaren i fältet **Ansvarig person** på projektkortet godkänner tidrapporten. |
| **Enbart maskin** |Om maskinens tidrapport är länkad till ett projekt, godkänner användaren i fältet **Ansvarig person** på projektkortet tidrapporten. Om maskinens tidrapport är länkad till en resurs, godkänner användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet tidrapporten. |

## <a name="to-assign-a-time-sheet-administrator"></a>Så här tilldelar du en tidrapportsadministratör
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användarinställningar** och välj sedan relaterad länk.  
2. Lägg till en ny användare om användarlistan inte innehåller den person som du vill ska vara tidrapportsadministratören. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).
3. Välj en användare som ska vara en tidrapportadministratör och välj sedan kryssrutan **Tidrapportadmin.**  

> [!TIP]  
>   Vi rekommenderar att du endast anger en användare som tidrapportsadministratör för ett företag. I följande procedur skapar du en tidrapportägare och godkännare där tidrapportgodkännaren tilldelas för varje resurs.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Så här tilldelar du en tidrapportsägare och en godkännare
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Resurser** och välj sedan relaterad länk.
2. Välj den resurs som du vill ställa in möjlighet att använda tidrapporter för och markera sedan kryssrutan **Använd tidrapport**.  
3. I fältet **Användar-ID för tidrapportens ägare** anger du ID för ägaren av tidrapporten. Ägaren kan ange tidförbrukning på en tidrapport och skicka den för godkännande. Vanligtvis, när resursen är en person, är den person också ägare.  
4. I fältet **Användar-ID för tidrapportens godkännare** anger du ID för godkännaren av tidrapporten. Godkännaren kan godkänna, avvisa eller öppna en tidrapport igen.  

> [!NOTE]  
>   Du kan inte ändra ID på tidrapportsgodkännaren om det finns tidrapporter som inte ännu har behandlats och har statusen **Skickad** eller **Öppen**.

## <a name="see-also"></a>Se även
[Ställa in projekthantering](projects-setup-projects.md)  
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]