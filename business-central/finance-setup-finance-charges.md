---
title: Konfigurera räntevillkor
description: Läs om hur du konfigurerar Business Central så att du kan informera kunder om extra avgifter genom att skicka räntefakturor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: aba5ca8eb9425c11c7f8a55a08a153ee18821632
ms.sourcegitcommit: 06bfb3aa59de50d983175e68e681b9d206423242
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672006"
---
# <a name="set-up-finance-charge-terms"></a>Konfigurera räntevillkor

Om en kund inte har betalat på förfallodatumet kan du låta beräkna dröjsmålsränta automatiskt och lägga på den på de förfallna beloppen på kundens konto. Du kan informera kunder om debiterade dröjsmålsräntor genom att skicka räntefakturor. Först måste du emellertid upprätta en kod som representerar respektive ränteberäkning. Du kan sedan ange denna kod i fältet Räntevillkorskod på kundkorten.  

## <a name="finance-charge-terms"></a>Räntevillkor

Du måste ange räntevillkor för respektive ränteberäkning och sedan tilldela villkoren till kunden i fältet **Räntevillkorskod** på sidan **Kund**.

Räntor kan antingen beräknas med metoden genomsnittligt saldo per dag eller metoden förfallet saldo.

* Genomsnittligt saldo per dag  
  
  Hur många dagar som har passerat sedan betalningen förföll beaktas:  
  *Metod för genomsnittligt saldo per dag* - *Räntefaktura* = *Förfallet belopp* x *(antal dagar försenat / ränteperiod)* x *(ränta/100)*

* Förfallet saldo  
  
  Räntan innebär helt enkelt en procentandel av det förfallna beloppet:  
  *Metod för förfallet saldo* - *Räntefaktura* = *Förfallet belopp* x *(ränta / 100)*

Dessutom är varje villkor i tabellen Räntevillkor kopplad till en undertabell, nämligen Räntetext. För respektive uppsättning av räntevillkor kan du definiera en inledande och/eller avslutande text som kan inkluderas på räntefakturan.

### <a name="to-set-up-finance-charge-terms"></a>Ange räntevillkoren

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Räntevillkor** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.
3. Om du vill använda fler än en uppsättning räntevillkor, anger du en kod för varje kombination.

    För varje räntevillkor kan du ange särskilda villkor, som kan inkludera ytterligare avgifter i både BVA och i utländsk valuta. Du kan definiera ytterliga avgifter i utländsk valuta för respektive villkor på sidan **Räntevillkor**.
4. Välj åtgärden **Valutor**.
5. På sidan **Valutor för räntevillkor** ange för varje villkor en valutakod och en tilläggsavgift.

    > [!NOTE]  
    > När du skapar dröjsmålsränta i utländsk valuta används de villkor som angett här för att skapa räntefakturor. Om det inte finns några räntevillkor definierade för utländsk valuta används de dröjsmålsräntevillkor för BVA som angetts på sidan **Räntevillkor** och omvandlas till relevant valuta.

    För varje räntevillkor kan du ange text som ska infogas före (**Inledande text**) eller efter (**Avslutande text**) transaktionerna i räntefakturan.  
6. Välj åtgärden **inledande text** eller **avslutande text** och fyll i på sidan **Räntetext**.
7. Om du vill infoga relaterade värden i den resulterande Räntetext, anger du följande platshållare i **Text**-fältet.

|Platshållare|Värde|  
|-----------------|-----------|  
|%1|Innehållet i fältet **Dokumentdatum** i räntefakturans huvud|  
|%2|Innehållet i fältet **Förfallodatum** i räntefakturans huvud|  
|%3|Innehållet i fältet **Räntesats** på de relaterade räntevillkor|  
|%4|Innehållet i fältet **Återstående belopp** i räntefakturans huvud|  
|%5|Innehållet i fältet **Räntebelopp** i räntefakturans huvud|  
|%6|Innehållet i fältet **Avgift** i räntefakturans huvud|  
|%7|Påminnelsens totalbelopp.|  
|%8|Innehållet i fältet **Valutakod** i räntefakturans huvud|  
|%9|Innehållet i fältet **Bokföringsdatum** i räntefakturans huvud|  

## <a name="see-also"></a>Se även

[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Konfigurera påminnelsevillkor och nivåer](finance-setup-reminders.md)  
[Ställa in Finance](finance-setup-finance.md)  
