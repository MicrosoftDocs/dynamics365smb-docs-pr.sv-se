---
title: "Så här ställer du in automatiska kontobokföringsmallar"
description: "Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2a12aebaba66bffd5ce6f4ae017b3a7f6121cf27
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-automatic-account-posting-groups"></a>Ställ in automatiska kontobokföringsmallar
Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Så här ställer du in automatiska kontobokföringsmallar  

1.  Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Automatkontering** och välj sedan relaterad länk.  
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

