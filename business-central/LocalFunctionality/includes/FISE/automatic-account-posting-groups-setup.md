---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0c1131d4517f71a2ad43d0ec1830fc2a486124e3
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959668"
---
Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Så här ställer du in automatiska kontobokföringsmallar  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../../media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Automatkontering** och välj sedan tillhörande länk.  
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
