---
title: "Använda och ändra inställningarna i rapporter | Microsoft Docs"
description: "Beskriver hur du använder fördefinierade alternativ och filter för att anpassa en rapport och för att generera korrekta data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="saved-settings-on-reports"></a>Sparade inställningar i rapporter
Beroende på rapporten som körs, kan du presenteras med en sida som gör att du kan ange vissa alternativ och filter för att ändra data som ingår i den skapade rapporten. Den här sidan är känd som sidan för rapportbegäran. En rapport kan innehålla en eller flera *sparade inställningar* som du kan tillämpa till rapporten från sidan för begäran. *Sparade inställningar* är i grunden fördefinierade alternativ och filter. Att använda sparade inställningar är ett snabbt och pålitligt sätt att konsekvent skapa rapporter som innehåller korrekta data.

Du kan se de sparade inställningar som är tillgängliga för dig för en rapport i avsnittet **Sparade inställningar** på sidan för rapportbegäran.  

## <a name="to-apply-saved-settings-to-a-report"></a>Om du vill ange sparade inställningar till en rapport
1. Öppna rapporten.

   Sidan för rapportbegäran visas.    
2. I avsnittet **Sparade inställningar** på sidan anger du fältet **Namn** till de sparade inställningar som du vill använda.

   Avsnittet **Sparade inställningar** visas bara om rapporten har körts tidigare eller om det finns befintliga poster med sparade inställningar. Posten vid namn **Senast använda alternativ och filter** med sparade inställningar är alltid tillgänglig. Dessa inställningar är de alternativ- och filtervärden som användes förra gången som du körde rapporten.

## <a name="administer-saved-report-settings-for-users"></a>Administrera sparade rapportinställningar för användare
Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget. Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.

Du hanterar sparade inställningar från sidan 1506 **rapportinställningar**. För att öppna denna sida väljer du ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rappor"), ange **Rapporinställningar**, och väljer sedan relaterad länk.

Från sidan **Rapporinställningar** kan du skapa nya inställningar från noll, eller så kan du göra en kopia och ändra befintliga inställningar. För att ändra alternativ och filter för inställningar väljer du åtgärden **Redigera**.

**Anteckningar**:

* Funktionen för sparade inställningar i rapporter är bara relevant när egenskapen SaveValues på sidan för begäran är inställd på Ja. Egenskapen SaveValues anges i utvecklingsmiljön.
* Om du skapar en artikel med sparade inställningar för alla användare och denna artikel har samma namn som befintliga sparade inställningar för en viss användare, kan den användaren inte använda de sparade inställningar som har tilldelats alla.  I fältet Sparade inställningar på sidan för rapportbegäran visas två alternativ för sparade inställningar med samma namn. Oavsett vilket alternativ användaren väljer kommer de användarspecifika sparade inställningarna att tillämpas.

## <a name="see-also"></a>Se även
[Så här schemalägger du en rapportkörning](ui-schedule-report.md)  

