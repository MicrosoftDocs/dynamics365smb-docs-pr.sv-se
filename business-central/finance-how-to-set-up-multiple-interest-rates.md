---
title: Ställa in flera räntesatser för fördröjd betalning
description: Det här ämnet berättar hur du beräknar dröjsmålsränta med flera räntesatser för en särskild period.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 6, 431, 432, 572
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 6d90f8e042899495bfc8e171d7e69f7e5b4fdb36
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971609"
---
# <a name="set-up-multiple-interest-rates-for-delayed-payment"></a>Ställa in flera räntesatser för fördröjd betalning

Du kan använda olika räntesatser för olika perioder för försenade betalningar i handelstransaktioner. [!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]

En myndighet anger till exempel den högsta räntan som kan tas ut för en kund. Den räntan kan ändras två gånger per år, den 1 januari och den 1 juli. Räntesatsen mellan företag avtalas av parterna och det finns ingen gräns för den kundgruppen. Den räntesatsen ligger vanligtvis 4 procent över den normala bankräntan.

När du skapar villkor och betalningspåminnelsevillkor för räntefakturor, så kan du för avgiften för försenad betalning ange flera räntesatser så att avgiften beräknas utifrån olika räntesatser under olika perioder.  

## <a name="to-set-up-multiple-interest-rates"></a>Så här ställer du in flera räntesatser

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **räntevillkor** och väljer sedan relaterad länk.  
2. Gå till sidan **Räntevillkor** välj räntevillkoret och välj sedan åtgärden **Räntesatser**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj **OK**.  
5. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **påminnelsevillkor** och väljer sedan relaterad länk.  
6. Gå till sidan **Betalningspåminnelsevillkor** välj villkoret och välj sedan åtgärden **Nivåer**.  
7. På sidan **Påminnelsenivåer** väljer du fältet **Beräkna ränta** för relevanta påminnelsenivåer.  

När du skickar ut en räntefaktura, visar fakturan dröjsmålsräntan med flera räntesatser för en viss tidsperiod. Räntefakturan innehåller även kontaktinformation för kunden, företaget som skickar räntefakturan, det ytterligare beloppet och totalt belopp. Den ingående transaktionen på räntefakturan visas i fet stil. Dröjsmålsräntan beräknas med flera räntesatser för en viss tidsperiod och skrivs ut efter den ingående transaktionen på räntefakturan.  

## <a name="see-also"></a>Se även

[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Ställa in Finance](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]