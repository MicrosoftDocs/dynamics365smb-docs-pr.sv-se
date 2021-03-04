---
title: Konfigurera påminnelsevillkor och nivåer
description: Lär dig hur du konfigurerar Business Central så att du kan skicka en påminnelse till en kund om en betalning som förfaller, samt hur du lägger till avgifter orsakade av förseningen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: 1bef0a7598846f0ea3fe74b03bbef70bb5c940ef
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035387"
---
# <a name="set-up-reminder-terms-and-levels"></a>Konfigurera påminnelsevillkor och nivåer

Du kan använda betalningspåminnelser för att påminna kunder om förfallna belopp. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a>Betalningspåminnelsevillkor

Om en betalning förfaller måste du bestämma när och hur betalningspåminnelsen ska skickas till kunden i fråga. Dessutom kanske du vill debitera kundens konto för ränta eller avgifter. Du kan ange valfritt antal villkor för betalningspåminnelser.  

> [!NOTE]
> Om du vill beräkna dröjsmålsränta på förfallna betalningar kan du göra detta när du skapar betalningspåminnelser. Om du däremot endast vill beräkna dröjsmålsränta och informera dina kunder om det utan att skicka betalningspåminnelser bör du använda [räntefakturor](finance-setup-finance-charges.md). Mer information finns i [Betalningspåminnelser](receivables-collect-outstanding-balances.md#reminders) samt [Ränta](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="to-set-up-reminder-terms"></a>Så här ställer du in betalningspåminnelsevillkor

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Betalningspåminnelsevillkor** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Om du vill använda fler än en uppsättning villkor, anger du en kod för varje kombination.

## <a name="reminder-levels"></a>Betalningspåminnelsenivåer

För varje påminnelsevillkorskod kan du definiera valfritt antal betalningspåminnelsenivåer. Första gången en betalningspåminnelse skapas för en kund används inställningen från nivå 1. När betalningspåminnelsen skickas ut registreras nivånumret på betalningspåminnelsetransaktionerna som skapas och kopplas till de enskilda kundreskontratransaktionerna. Om kunden måste påminnas igen kontrolleras alla betalningspåminnelsetransaktioner som är kopplade till öppna kundreskontratransaktioner så att det högsta nivånumret hittas. Villkoren från nästa nivånummer används sedan för den nya betalningspåminnelsen.

Om du skapar fler betalningspåminnelser än du har definierat nivåer för, används villkoren för den högsta nivån. Du kan skapa så många betalningspåminnelser som fältet **Max. antal påminnelser** i betalningspåminnelsevillkoren tillåter.

### <a name="to-set-up-reminder-levels"></a>Så här ställer du in nivåer för betalningspåminnelser

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Betalningspåminnelsevillkor** och välj sedan relaterad länk.  
2. På sidan **betalningspåminnelsevillkor** och välj raden med de villkor som du vill ange nivåer för och klicka sedan på åtgärden **Nivåer**.  
3. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Inställningen i fältet **Beräkna ränta** bestämmer om räntan ska visas på betalningspåminnelsen när betalningspåminnelsen utfärdas. Fältet **Bokför ränta** på sidan **Betalningspåminnelsevillkor** avgör emelelrtid om den beräknade räntan måste bokföras på redovisningskontot och kundkontot.
    >
    > Välj fältet **Beräkna ränta** om du vill ange att ränta ska beräknas.

    För varje betalningspåminnelsenivå anger du ytterligare avgifter i både BVA och utländsk valuta. Du kan definiera många räntefaktureringsavgifter i utländsk valuta för respektive kod på sidan **Betalningspåminnelsevillkor**.  

    Ytterligare avgifter kan beräknas på tre olika sätt som definieras av värdet i fältet **Ytterl. avgiftsberäkningstyp**.  

    - **Fast**

        Avgifter beräknas baserat på värdena i fälten **Ytterligare avgift** på raden för själva betalningspåminnelsenivån.  
    - **Enkel dynamik**

        Avgifter beräknas baserat på värdena i fälten i relevant rad på sidan **Inställningar för ytterligare avgifter** för den betalningspåminnelsenivån.
    - **Ackumulerad dynamik**

        Avgifter beräknas baserat på värdena i fälten i kombinerade rader på sidan **Inställningar för ytterligare avgifter** för den betalningspåminnelsenivån.

4. Välj åtgärden **Valutor**.
5. På sidan **Valutor för betalpåm.nivå** kan du definiera för varje betalningspåminnelsekod och motsvarande nivånummer en valutakod och en tilläggsavgift.

    > [!NOTE]  
    > När du skapar räntefakturor i utländsk valuta används de villkor för utländsk valuta som definieras här för att skapa betalningspåminnelser. Om det inte finns några betalningsvillkor definierade för utländsk valuta används de villkor för BVA som angetts på sidan **Betalningspåminnelsenivåer** och omvandlas till relevant valuta.

    För varje betalningspåminnelsenivå kan du ange text som ska infogas före (**Inledande text**) eller efter (**Avslutande text**) transaktionerna i betalningspåminnelsen.

6. Välj åtgärden **Inledande text** eller **Avslutande text** och fyll i på sidan **Betalningspåminnelsetext**.
7. Om du vill infoga relaterade värden i den resulterande betalningspåminnelsetexten, anger du följande platshållare i **Text**-fältet.  

    |Platshållare|Värde|  
    |-----------------|-----------|  
    |%1|Innehållet i fältet **Dokumentdatum** i betalningspåminnelsens huvud|  
    |%2|Innehållet i fältet **Förfallodatum** i betalningspåminnelsens huvud|  
    |%3|Innehållet i fältet **Räntesats** på de relaterade räntevillkor|  
    |%4|Innehållet i fältet **Återstående belopp** i betalningspåminnelsens huvud|  
    |%5|Innehållet i fältet **Räntebelopp** i betalningspåminnelsens huvud|  
    |%6|Innehållet i fältet **Avgift** i betalningspåminnelsens huvud|  
    |%7|Påminnelsens totalbelopp.|  
    |%8|Innehållet i fältet **Betalningspåminnelsenivå** i betalningspåminnelsens huvud|  
    |%9|Innehållet i fältet **Valutakod** i betalningspåminnelsens huvud|  
    |%10|Innehållet i fältet **Bokföringsdatum** i betalningspåminnelsens huvud|  
    |%11|Företagsnamnet|  
    |%12|Innehållet i fältet **Avgift per rad** i betalningspåminnelsens huvud|  

    Om du skriver exempelvis **du är skyldig %9 %7 som förfaller %2.**, innehåller den resulterande betalningspåminnelsen följande text: **du är skyldig 1 200,50 som förfaller 2014-02-02**.

    > [!NOTE]
    > Förfallodatumet beräknas enligt den formel du anger. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#using-date-formulas).

När du har angett betalningspåminnelsevillkoren (med ytterligare nivåer och text) anger du någon av koderna på vart och ett av kundkorten. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Se även

[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Konfigurera räntevillkor](finance-setup-finance-charges.md)  
[Ställa in Finance](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]