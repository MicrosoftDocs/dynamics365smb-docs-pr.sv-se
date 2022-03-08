---
title: Så här importerar och exporterar du data i SIE-format (Standard Import Export)
description: Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2c4088b1ac5fd6e7c599bcdb8a4a897f4dc876c0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925234"
---
# <a name="import-and-export-data-in-standard-import-export-format"></a>Importera och exportera data i SIE-format (Standard Import Export)
Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export). Genom att ange SIE-dimensioner och -filtyper kan du ange vilken detaljnivå import- eller exporttransaktionerna ska ha. Mer information finns i [SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d).  

## <a name="to-import-data-in-sie-format"></a>Så här importerar du data i SIE-format  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../media/ui-search/search_small.png "Berätta vad du vill göra"), ange **SIE-import** och välj sedan relaterad länk.  
2.  Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Redovisningsjournalmall**|Välj en redovisningsjournalmall.|  
    |**Redovisningsjournal**|Välj en redovisningsjournal.|  
    |**Dimensioner**|Markera SIE-dimensionerna du vill importera.|  
    |**Infoga redovisningskonto**|Välj det här alternativet om redovisningskontot i importfilen saknas i kontoplanen och måste skapas under importprocessen.|  
    |**Använd nummerserie för dok.nr**|Välj det här alternativet om det inte finns något dokumentnummer i importfilen.|  

3. Välj knappen **OK**.
4. Välj en fil att importera.  

## <a name="to-export-data-in-sie-format"></a>Så här exporterar du data i SIE-format  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../media/ui-search/search_small.png "Berätta vad du vill göra"), ange **SIE-export** och välj sedan relaterad länk.  
2.  Välj lämpliga filter på snabbfliken **Redovisningskonto**.  
3.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Alternativ**.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Filtyp**|Välj typen av fil du vill skapa. Välj något av följande alternativ:<br /><br /> -   **År - Slutsaldon** - Innehåller årligt utgående saldo för alla konton i kontoplanen.<br />-   **Periodiska saldon** - Innehåller årligt utgående saldo och månatliga förändringar för alla konton i kontoplanen.<br />-   **Objektsaldon** - Innehåller årligt utgående kontosaldo, månatliga förändringar och saldon på objektnivån, till exempel kostnadsenheter och projekt, för alla konton i kontoplanen.<br />-   **Transaktioner** - Innehåller alla redovisningstransaktioner för perioden.|  
    |**Kontakt**|Ange kontaktperson. Fältet är ett tillval.|  
    |**Kommentarer**|Beskriv filens innehåll.|  
    |**Dimensioner**|Markera dimensionerna du vill exportera.|  
    |**Räkenskapsår**|Ange räkenskapsåret.|

4. Välj knappen **OK**.
5. Välj knappen **Öppna** eller **Spara** för att bestämma var den exporterade filen ska placeras.

## <a name="see-also"></a>Se även  
 [SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d)   
 [Lokal funktionalitet för Sverige](sweden-local-functionality.md)
