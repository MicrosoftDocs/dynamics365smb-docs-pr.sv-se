---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 636cbbd2e20dd357fba734187195f64d8ccaa754
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440050"
---
Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Så här ställer du in automatiska kontobokföringsmallar  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Automatkontering** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.  

    |Fält|Description|  
    |-----------|-----------------|  
    |**Nr**|Ange ett unikt alfanumeriskt nummer för den automatiska kontobokföringsmallen.|  
    |**Beskrivning**|Ange en beskrivning av den automatiska kontobokföringsmallen.|  

4. Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Automatkonteringsrad**.  

    |Fält|Description|  
    |-----------|-----------------|  
    |**Allokeringsprocent**|Ange procentandelen av ursprungsradbeloppet som ska fördelas.|  
    |**Redovisningskontonr**|Ange numret på redovisningskontot som fördelningen ska bokföras på.|  

    > [!NOTE]  
    >  I fältet **Totalt saldo** summeras fältet **Allokeringsprocent** för de automatiska kontoraderna i en bokföringsmall. Om den totala fördelningsprocenten för en bokföringsmall inte blir noll visas ett felmeddelande när posten bokförs.  

5. Välj **OK**.  
