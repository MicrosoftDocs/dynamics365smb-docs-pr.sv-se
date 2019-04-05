---
title: Använda och ändra inställningarna i rapporter | Microsoft Docs
description: Beskriver hur du använder fördefinierade alternativ och filter för att anpassa en rapport och för att generera korrekta data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: cbbb072c4be3ec41684e426451c394cfa978c390
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/19/2019
ms.locfileid: "853123"
---
# <a name="managing-saved-settings-on-reports"></a>Hantering av sparade inställningar i rapporter
När användaren kör en rapport visas vanligtvis en sida där han eller hon kan ange vissa alternativ och filter för att ändra den data som inkluderas i den genererade rapporten. Denna sida kallas sidan för rapportförfrågan. En rapport kan omfatta en eller flera *sparade(e) inställning(ar)* som användarna kan tillämpa på rapporten från sidan för förfrågan. *Sparade inställningar* är i grunden fördefinierade alternativ och filter. Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data. Mer information om hur sparade anställningar används finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).

Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget. Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Skapa och ändra inställningarna för alla användare
Du hanterar sparade inställningar från sidan **1560 Rapportinställningar**. Det finns två sätt att öppna denna sida:
-   Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportinställningar** och välj sedan relaterad länk.
-   Öppna en rapport, välj söktexten bredvid rutan **Använda standardvärden från:** och sedan **Välj från komplett lista**.

Denna sida visar samtliga befintliga poster för sparade inställningar för samtliga användare. Om det finns ett användarnamn i kolumnen **Tilldelad till** kan endast denna användare använda de sparade inställningarna för associerad rapport. Om det finns en bock i kolumnen **Dela med samtliga användare** kan samtliga användare använda de sparade inställningarna för rapporten.

Via sidan **Rapportinställningar** kan du:
-   Välja **Nytt** för att skapa en ny post för sparade inställningar från grunden.
-   Välja en post för sparade inställningar i listan och sedan välja **Kopiera** för att skapa en kopia.
-   Välja en post för sparade inställningar i listan och sedan välja **Redigera** för att ändra en post för sparade inställningar.


> [!Important]
> Var noggrann när du väljer namn för en post för sparade inställningar. Om du skapar en post för sparade inställningar för samtliga användare, och du ger denna post samma namn som en befintlig post för sparade inställningar som endas tilldelats en specifik användare, så kommer denna användare inte att kunna använda posten för sparade inställningar som tilldelats alla.  Under **Sparade inställningar** på sidan för rapportförfrågan kommer användaren att se två sparade poster för sparade inställningar med samma namn. Oavsett vilket alternativ han eller hon väljer kommer emellertid posten för användarspecifika sparade inställningar att användas.

> [!NOTE]
> Funktionen för sparade inställningar finns bara för rapporter där [värdet SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) på sidan för rapportförfrågan har angetts som `Yes`. Egenskapen **SaveValues** anges i utvecklingsmiljön.  

## <a name="see-also"></a>Se även
[Arbeta med rapporter och batch-jobb](ui-work-report.md)  
