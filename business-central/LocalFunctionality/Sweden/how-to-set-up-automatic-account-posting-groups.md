---
title: Så här ställer du in automatiska kontobokföringsmallar
description: Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8218f35bfbbd4c1ff56d86c55598127b0ecd1fec
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676748"
---
# <a name="set-up-automatic-account-posting-groups"></a>Ställ in automatiska kontobokföringsmallar
Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Så här ställer du in automatiska kontobokföringsmallar  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Automatkontering** och välj sedan tillhörande länk.  
2.  Välj åtgärden **Ny**.  
3.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.  

    |Fält|Description|  
    |-----------|-----------------|  
    |**Nr**|Ange ett unikt alfanumeriskt nummer för den automatiska kontobokföringsmallen.|  
    |**Beskrivning**|Ange en beskrivning av den automatiska kontobokföringsmallen.|  

4.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Automatkonteringsrad**.  

    |Fält|Description|  
    |-----------|-----------------|  
    |**Allokeringsprocent**|Ange procentandelen av ursprungsradbeloppet som ska fördelas.|  
    |**Redovisningskontonr**|Ange numret på redovisningskontot som fördelningen ska bokföras på.|  

    > [!NOTE]  
    >  I fältet **Totalt saldo** summeras fältet **Allokeringsprocent** för de automatiska kontoraderna i en bokföringsmall. Om den totala fördelningsprocenten för en bokföringsmall inte blir noll visas ett felmeddelande när posten bokförs.  

5.  Välj knappen **OK**.  

## <a name="see-also"></a>Se även  
 [Automatiska kontokoder](automatic-account-codes.md)   
 [Ställa in bokföringsmallar](../../finance-posting-groups.md)  
 [Arbeta med redovisningsjournaler](../../ui-work-general-journals.md)
