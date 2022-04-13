---
title: Hantera sparade inställningar för rapporter och batch-jobb
description: Beskriver vem administratören kan ange fördefinierade alternativ och filter för en rapport och dela dessa inställningar med en eller alla användare.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 12/21/2021
ms.author: edupont
ms.openlocfilehash: 901f3899ef164d3d24dbc5c4e2226b840c97c945
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522648"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Hantera sparade inställningar för rapporter och batch-jobb

När användaren kör en rapport visas vanligtvis en sida där han eller hon kan välja alternativ och ange filter för att ändra den data som inkluderas i den genererade rapporten. Denna sida kallas *sidan för förfrågan*. En rapport kan omfatta en eller flera *sparade(e) inställning(ar)* som användarna kan tillämpa på rapporten från sidan för förfrågan. *Sparade inställningar* är i grunden fördefinierade alternativ och filter. Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data. Mer information finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).

> [!NOTE]
> Det här avsnittet avser *rapport*, men liknande information gäller för *batch-jobb*.

Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget. Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.

## <a name="manage-saved-settings"></a>Hantera sparade inställningar

Du hanterar sparade inställningar från sidan **Rapportinställningar**. Det finns två sätt att öppna denna sida:

- Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Rapportinställningar** och väljer sedan relaterad länk.
- Öppna en rapports sida för begäran, välj söktexten bredvid fältet **Använda standardvärden från** och sedan välja åtgärden **Välj från komplett lista**.

    Fältet visas bara om du har kört rapporten minst en gång i taget. I listan visas endast inställningar som du kan välja mellan, antingen för de egna inställningarna eller för att inställningarna ska delas med dig.

Denna sida för **rapportinställningar** visar samtliga befintliga poster för sparade inställningar för samtliga användare. Om det finns ett användarnamn i fältet **Tilldelad till** kan endast denna användare använda de sparade inställningarna för associerad rapport. Om det finns en bock i fältet **Dela med samtliga användare** kan samtliga användare använda de sparade inställningarna för rapporten.  

> [!TIP]
> När en användare har kört en rapport som stöder delade inställningar sparas och läggs inställningarna till i listan. I de flesta fall kan administratören redigera dessa inställningar och välja att dela inställningarna med alla användare.
>
> I vissa fall kan inställningarna emellertid inte delas, och administratören kan inte ändra dem. De flesta batch-jobb stöder inte delade inställningar.  

## <a name="create-or-modify-saved-settings-for-all-users"></a>Skapa eller ändra inställningarna för alla användare

Via sidan **Rapportinställningar** kan du:

- Välj åtgärden **Nytt** för att skapa en ny post för sparade inställningar från grunden.
- Välja en post för sparade inställningar i listan och sedan välja åtgärden **Kopiera** för att skapa en kopia.
- Välja en post för sparade inställningar i listan och sedan välja åtgärden **Redigera** för att ändra en post för sparade inställningar.

> [!Important]
> Var noggrann när du väljer namn för en post för sparade inställningar. Om du skapar en post för sparade inställningar för samtliga användare, och du ger denna post samma namn som en befintlig post för sparade inställningar som endas tilldelats en specifik användare, så kommer denna användare inte att kunna använda posten för sparade inställningar som tilldelats alla.  I avsnittet **Sparade inställningar** på sidan för rapportförfrågan kommer användaren att se två sparade poster för sparade inställningar med samma namn. Oavsett vilket alternativ han eller hon väljer kommer emellertid posten för användarspecifika sparade inställningar att användas.

> [!NOTE]
> Förmågan att spara inställningar finns bara för rapporter där värdet [egenskapen SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) på sidan för rapportförfrågan har angetts som **Ja**. Egenskapen **SaveValues** anges i utvecklare.  

## <a name="see-also"></a>Se även

[Arbeta med rapporter, batch-jobb och XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]