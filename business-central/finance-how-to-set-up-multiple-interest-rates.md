---
title: Så här ställer du in flera räntesatser
description: Du kan beräkna dröjsmålsränta med flera räntesatser för en särskild period. Ränteberäkningen görs på samma sätt för alla dröjsmålsräntor, men räntan kan variera under en viss period.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96098ca669dd5001f334cf464d8e3a37de5dbf03
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387280"
---
# <a name="set-up-multiple-interest-rates"></a>Ställ in flera räntesatser
Flera räntesatser används för olika perioder för försenade betalningar i handelstransaktioner. En myndighet anger till exempel den högsta räntan som kan tas ut för en kund. Den räntan kan ändras två gånger per år, den 1 januari och den 1 juli. Räntesatsen mellan företag avtalas av parterna och det finns ingen gräns för den kundgruppen. Den räntesatsen ligger vanligtvis 4 procent över den normala bankräntan.

När du skapar villkor och betalningspåminnelsevillkor för räntefakturor, så kan du för avgiften för försenad betalning ange flera räntesatser så att avgiften beräknas utifrån olika räntesatser under olika perioder. Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Så här ställer du in flera räntesatser  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Räntevillkor** och välj sedan relaterad länk.  
2.  Gå till sidan **Räntevillkor** välj räntevillkoret och välj sedan åtgärden **Räntesatser**.  
3.  Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Välj **OK**.  
5.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Betalningspåminnelsevillkor** och välj sedan relaterad länk.  
6.  Gå till sidan **Betalningspåminnelsevillkor** välj villkoret och välj sedan åtgärden **Nivåer**.  
7.  Markera fältet **Beräkna ränta** på sidan **Betalningspåminnelsenivåer**.  

När du skickar ut en räntefaktura, visar fakturan dröjsmålsräntan med flera räntesatser för en viss tidsperiod. Räntefakturan innehåller även kontaktinformation för kunden, företaget som skickar räntefakturan, det ytterligare beloppet och totalt belopp. Den ingående transaktionen på räntefakturan visas i fet stil. Dröjsmålsräntan beräknas med flera räntesatser för en viss tidsperiod och skrivs ut efter den ingående transaktionen på räntefakturan.  

## <a name="see-also"></a>Se även  
[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Ställa in Finance](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]