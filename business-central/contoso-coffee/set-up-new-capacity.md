---
title: Skapa en ny kapacitet
description: En genomgång för att lära dig hur du lägger upp en ny produktionsgrupp med en kapacitetskalender för ett enda skift i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Genomgång: Skapa en ny kapacitet

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demodata i hur du hanterar kapacitet.  

## Scenario

Du arbetar med produktionsplaneraren på Contoso Coffee. Som svar på förändringar på verkstadsgolvet måste du skapa ett nytt arbetscenter, Testavdelningen. Den nya produktionsgruppen har en maskingrupp, test. De nya centren måste ha en kapacitetskalender för ett enstaka skift från 08:00:00 till 16:00:00, måndag till fredag.  

## Steg

1. Så här skapar du produktionsgrupper.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **produktionsgrupper** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Nr** |700|
        |**Namn** |Testavdelning|
        |**Produktionsgruppskod** |1. Produktionsavdelningen|
        |**A-pris senaste inköp**|3.25|
        |**Styckkost. beräkningstyp**|Tid|
        |**Bokföringsmetod**|Manuell|
        |**Produktbokföringsmall**|INGEN MOMS</br></br>Observera att den här markeringen beror på redovisningsinställningar och land.|
        |**Måttenhetskod** |MINUTER|
        |**Kapacitet** |1|
        |**Effektivitet** |90|
        |**Fabrikskalenderkod** |1|

        I fältet **Fabrikskalenderkod** innebär inställning 1 ett skift från måndag till fredag.

    3. Stäng produktionsgruppskortet.

2. Så här skapar du maskingrupper.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **maskingrupper** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Nr** |760|
        |**Namn** |Testning|
        |**Prod.gruppsnr.** |700, Testavdelning|
        |**A-pris senaste inköp**|3.25|
        |**Bokföringsmetod**|Manuell|
        |**Produktbokföringsmall**|INGEN MOMS</br></br>Observera att den här markeringen beror på redovisningsinställningar och land.|
        |**Kapacitet** |1|
        |**Effektivitet** |90|
    3. Expandera snabbfliken **operationsföljd** och skriv **inställningstid** ange *10*.  

3. Beräkna kapacitetskalender för maskingrupp.  

    1. Välj åtgärden **Kalender**.  

    2. På sidan **maskingruppskalender** på snabbfliken **matrisalternativ** ange fältet **Visa efter** till *Månad*.  

    3. Välj åtgärden **Visa matris**.  

    4. På sidan **Matris för maskingruppskalender** väljer du åtgärden **Beräkna**.  

    5. På sidan **Beräkna maskingruppskalender** på snabbfliken **alternativ** ange fältet **Startdatum** till *januari 01*.  

    6. Ställ in **slutdatum** fältet till 31 december.  

    7. Fyll i fältet **maskingrupp** på snabbfliken **Nr.** Filtrera fält, välja *760, test*.  

    8. Välj **OK**. När batch-jobbet är klart kommer du tillbaka till sidan **Matris för maskingruppskalender**.  

    9. Välj åtgärden **Uppdatera**.  

    10. På raden för maskingrupp 760, test, detaljgranska ned till värdet i kolumnen januari.  

På sidan **kalendertransaktioner** är de dagliga kapacitets transaktionerna i fältet **kapacitet (total)** är 480 minuter. Detta återspeglar ett åtta timmars skift för varje arbetsdag. Dessutom visar fältet **kapacitet (effektiv)** visar 432 minuter. Detta motsvarar den 90 procents effektivitetsgrad som du har tilldelat maskingruppen.  

## Se även

[Introduktion till demonstrationsdata för Contoso Coffee](contoso-coffee-intro.md)  
