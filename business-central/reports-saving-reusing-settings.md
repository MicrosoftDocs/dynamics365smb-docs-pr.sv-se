---
title: Använda och ändra inställningarna i rapporter | Microsoft Docs
description: Beskriver hur du använder fördefinierade alternativ och filter för att anpassa en rapport och för att generera korrekta data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784615"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Hantera sparade inställningar för rapporter och batch-jobb
När användaren kör en rapport visas vanligtvis en sida där han eller hon kan välja alternativ och ange filter för att ändra den data som inkluderas i den genererade rapporten. Denna sida kallas sidan för förfrågan. En rapport kan omfatta en eller flera *sparade(e) inställning(ar)* som användarna kan tillämpa på rapporten från sidan för förfrågan. *Sparade inställningar* är i grunden fördefinierade alternativ och filter. Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data. Mer information finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).

> [!NOTE]
> Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb.

Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget. Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>För att skapa och ändra inställningarna för alla användare
Du hanterar sparade inställningar från sidan **Rapportinställningar**. Det finns två sätt att öppna denna sida:
-   Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rapportinställningar** och välj sedan relaterad länk.
-   Öppna en rapport, välj söktexten bredvid fältet **Använda standardvärden från** och sedan välja åtgärden **Välj från komplett lista**.

Denna sida visar samtliga befintliga poster för sparade inställningar för samtliga användare. Om det finns ett användarnamn i fältet **Tilldelad till** kan endast denna användare använda de sparade inställningarna för associerad rapport. Om det finns en bock i fältet **Dela med samtliga användare** kan samtliga användare använda de sparade inställningarna för rapporten.

Via sidan **Rapportinställningar** kan du:
-   Välj åtgärden **Nytt** för att skapa en ny post för sparade inställningar från grunden.
-   Välja en post för sparade inställningar i listan och sedan välja åtgärden **Kopiera** för att skapa en kopia.
-   Välja en post för sparade inställningar i listan och sedan välja åtgärden **Redigera** för att ändra en post för sparade inställningar.

> [!Important]
> Var noggrann när du väljer namn för en post för sparade inställningar. Om du skapar en post för sparade inställningar för samtliga användare, och du ger denna post samma namn som en befintlig post för sparade inställningar som endas tilldelats en specifik användare, så kommer denna användare inte att kunna använda posten för sparade inställningar som tilldelats alla.  I avsnittet **Sparade inställningar** på sidan för rapportförfrågan kommer användaren att se två sparade poster för sparade inställningar med samma namn. Oavsett vilket alternativ han eller hon väljer kommer emellertid posten för användarspecifika sparade inställningar att användas.

> [!NOTE]
> Funktionen för sparade inställningar finns bara för rapporter där värdet [egenskapen SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property)  på sidan för rapportförfrågan har angetts som **Ja**. Egenskapen **SaveValues** anges i utvecklingsmiljön.  

## <a name="see-also"></a>Se även
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
