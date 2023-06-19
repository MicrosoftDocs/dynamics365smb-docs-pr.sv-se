---
title: 'Importera och exportera data i SIEE [SE]'
description: Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export) som förklaras i detta ämne.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 11212
ms.date: 06/24/2021
ms.author: edupont
---

# Importera och exportera data i SIE-format (Standard Import Export) i svenska versionen

Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export). Genom att ange SIE-dimensioner och -filtyper kan du ange vilken detaljnivå import- eller exporttransaktionerna ska ha. Mer information finns i [SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d).  

> [!NOTE]
> Från och med version 22.1 har den svenska lokaliseringen flyttats till tilläggen och den här funktionen är avlokaliserad. Eftersom lokaliseringen nu skapas som ett tillägg måste du aktivera funktionen för att kunna använda den. Mer information om den här metoden finns i [Importera och exportera data i SIE-format, standard import-export](how-to-use-sie-audit-files-export.md).

## Så här importerar du data i SIE-format  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **SIE-import** och väljer sedan relaterad länk.  
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

## Så här exporterar du data i SIE-format  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **SIE-export** och väljer sedan relaterad länk.  
2.  Välj lämpliga filter på snabbfliken **Redovisningskonto**.  
3.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Alternativ**.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Filtyp**|<p>Välj typen av fil du vill skapa. Välj något av följande alternativ:</p><ul><li>**År – Slutsaldon** – Innehåller årligt utgående saldo för alla konton i kontoplanen.</li><li>**Periodiska saldon** – Innehåller årligt utgående saldo och månatliga förändringar för alla konton i kontoplanen.</li><li>**Objektsaldon** – Innehåller årligt utgående kontosaldo, månatliga förändringar och saldon på objektnivån, till exempel kostnadsenheter och projekt, för alla konton i kontoplanen.</li><li>**Transaktioner** – Innehåller alla redovisningstransaktioner för perioden.</li></ul>|  
    |**Kontakt**|Ange kontaktperson. Fältet är ett tillval.|  
    |**Kommentarer**|Beskriv filens innehåll.|  
    |**Dimensioner**|Markera dimensionerna du vill exportera.|  
    |**Räkenskapsår**|Ange räkenskapsåret.|

4. Välj knappen **OK**.
5. Välj knappen **Öppna** eller **Spara** för att bestämma var den exporterade filen ska placeras.

## Se även  
 [SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d)   
 [Lokal funktionalitet för Sverige](sweden-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
