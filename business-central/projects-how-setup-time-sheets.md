---
title: Konfigurera tidrapporter och deras godkännande
description: Du lägger upp tidrapporter för att spåra den tid som använts för projekt och använder resurser kan hjälpa dig med projekthantering, personal och kapacitet
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 72618aaeddae0a72a0c699f19a04a388ced0b9c1
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589213"
---
# <a name="set-up-time-sheets"></a>Så här skapar du tidrapporter

Tidrapporter i [!INCLUDE[prod_short](includes/prod_short.md)] hanterar tidregistrering veckovis, med sju dagars steg i taget. Du kan använda dem för att spåra den tid som används för projektet och du kan använda dem för att registrera enkel resurstimregistrering. Innan du kan använda tidrapporter måste du ange hur du vill att de ska registreras och konfigureras.

När du har ställt in hur organisationen ska använda tidrapporter, kan du ange om och hur tidrapporter godkänns. Beroende på organisationens behov kan du ange:

* En eller flera användare som tidrapportsadministratör och godkännare för alla tidrapporter.
* En tidrapportsgodkännare för varje resurs.

När du har konfigurerat tidrapporter, kan du skapa tidrapporter för resurser, tilldela dem till projektplaneringsrader och bokföra tidrapportrader. Mer information finns i [Så här använder du tidrapporter](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Skapa tidrapporter med hjälp av guiden för assisterad konfiguration

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Från och med 2021 utgivningscykel 2 kan du använda en assisterad installationshandbok som hjälper dig att skapa tidsrapporter.  

> [!TIP]
> Du måste aktivera **funktionsuppdateringen: ny tidrapport** på sidan [funktionshantering](https://businesscentral.dynamics.com/?page=2610) om du vill använda den här funktionen.
>
> Samma funktion gör det också enklare att hantera tidsrapporter på en mobil enhet.

Guiden assisterad konfiguration går igenom följande steg:

1. Konfigurera deltagarna i tidrapportsprocesser.
2. Ange den första dagen i en arbetsvecka i den här organisationen

    Den första dagen i en arbetsvecka är den första dagen för alla tidrapporter.
3. Ange den person som administrerar tidrapporter

    Den här personen kan redigera och ta bort alla tidrapporter. Du kan också lägga till samma roll för andra personer på sidan **användarinställningar**.
4. Ställ in de resurser som ska använda tidrapporter och de personer som ska godkänna tidrapporter

    > [!NOTE]
    > För projekt och projekt är användarna av tidrapporter *resurser*, inte anställda. För att kunna spåra medarbetarnas måste du koppla resurser till medarbetare i inställningsguiden.

I slutet av installationshandboken kan du välja att [!INCLUDE [prod_short](includes/prod_short.md)] skapa tidrapporter baserat på din konfiguration. Du kan också köra guiden assisterad konfiguration igen eller slutföra installationen manuellt.  

## <a name="set-up-time-sheets-manually"></a>Ställ in tidrapporter manuellt

I följande avsnitt beskrivs hur du ställer in tidrapporter om du inte använder guiden assisterad konfiguration **Konfigurera tidrapporter**.  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Så här anger du allmän information för tidrapporter manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurskonfiguration** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. För fältet **Tidrapport per projektgodkännande** väljer du ett av följande alternativ.

| Alternativ | Beskrivning |
| --- | --- |
| **Aldrig** |Användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet godkänner tidrapporten. |
| **Alltid** |Användaren i fältet **Ansvarig person** på projektkortet godkänner tidrapporten. |
| **Enbart maskin** |Om maskinens tidrapport är länkad till ett projekt, godkänner användaren i fältet **Ansvarig person** på projektkortet tidrapporten. Om maskinens tidrapport är länkad till en resurs, godkänner användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet tidrapporten. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Så här tilldelar du en tidrapportsadministratör manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställning** och väljer sedan relaterad länk.  
2. Lägg till en ny användare om användarlistan inte innehåller den person som du vill ska vara tidrapportsadministratören. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).
3. Välj en användare som ska vara en tidrapportadministratör och välj sedan kryssrutan **Tidrapportadmin.**  

> [!TIP]  
> Vi rekommenderar att du endast anger en användare som tidrapportsadministratör för ett företag. I följande procedur skapar du en tidrapportägare och godkännare där tidrapportgodkännaren tilldelas för varje resurs.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Så här tilldelar du en tidrapportsägare och en godkännare manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.
2. Välj den resurs som du vill ställa in möjlighet att använda tidrapporter för och markera sedan kryssrutan **Använd tidrapport**.  
3. I fältet **Användar-ID för tidrapportens ägare** anger du ID för ägaren av tidrapporten. Ägaren kan ange tidförbrukning på en tidrapport och skicka den för godkännande. Vanligtvis, när resursen är en person, är den person också ägare.  
4. I fältet **Användar-ID för tidrapportens godkännare** anger du ID för godkännaren av tidrapporten. Godkännaren kan godkänna, avvisa eller öppna en tidrapport igen.  

> [!NOTE]  
> Du kan inte ändra ID på tidrapportsgodkännaren om det finns tidrapporter som inte ännu har behandlats och har statusen **Skickad** eller **Öppen**.

## <a name="see-also"></a>Se även

[Använda tidrapporter för projekt](projects-how-use-time-sheets.md)  
[Så här skapar du tidrapporter](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrera förbrukning eller användning för projekt](projects-how-record-job-usage.md)  
[Ställa in projekthantering](projects-setup-projects.md)  
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]