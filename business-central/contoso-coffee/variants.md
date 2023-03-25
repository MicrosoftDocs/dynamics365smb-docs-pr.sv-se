---
title: Varianter
description: I genomgången för att lära dig hur du uppdaterar efter frågeprognosen för varje variant av en produkt i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Genomgång: varianter

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demodata för att lära dig om varianter.

## Scenario

Du arbetar med produktionsplaneraren på Contoso Coffee. Du måste uppdatera efter fråge prognosen för varje variant av artikeln SP-SCM1006, AutoDripLite. Eftersom de har olika färger måste du se till att rätt struktur används för varje variant. Kör planeringsarbetsbladet för att beräkna utbudet.  

## Steg

1. Ställ in lagerställeenheter för artikeln SP-SCM1006, AutoDripLite. Tilldela en strukturlista för SKU med varianterna rött och vitt.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du *Artiklar* och väljer sedan relaterad länk.  

    2. Öppna objektet **SP-SCM1006, AutoDripLite**.

    3. Välj åtgärden **Skapa lagerställeenhet**.  

    4. Ställ in fältet **Skapa per** på *Plats och variant*.

    5. Ange ett filter för platsen till *norr* och klicka sedan på **OK**.

    6. Välj åtgärden **lagerställeenheter**.  

    7. Uppdatera produktionsstrukturer för följande lagerställeenheter:

        1. RÖD på NORR, ange SP-SCM1006-RED  

        2. VIT på NORR, ange SP-SCM1006-WHITE  

        3. Håll produktionstrukturnr. tomt för SVART på NORR  

2. Uppdatera produktionsinställningar och respektera efter frågeprognos på lagerställen och varianter.  

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du *Produktionsinställningar* och väljer sedan relaterad länk.  

    2. Växla till fältet **Använd prognos vid lagerställe**.

    3. Växla till fältet **Använd prognos på varianter**.

    4. Stäng fönstret **Produktionsinställningar**.

3. Skapa en ny månatlig efter frågeprognos, *AUTODRIP*. Filtrera artikeln efter SP-SCM1006 och plats NORD. Ställ in efterfrågan för maj för varje variant. 

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du *efterfrågeprognos* och väljer sedan relaterad länk.

    2. Skapa en ny efterfrågeprognos med namnet *AUTODRIP*.

    3. Välj åtgärden **Redigera efterfrågeprognos**.

    4. I fältet **Visa** som väljer du *Månad*.

    5. I fältet **Artikelfilter** väljer du *SP-SCM1006*

    6. Växla till fältet **Använd prognos vid lagerställe**.

    7. I fältet **Artikelfilter** väljer du *NORR*.

    8. Växla till fältet **Använd prognos på varianter**.

    9. För varje rad uppdateras värden i kolumnen maj

        1. RÖD på NORR, ange 100

        2. VIT på NORR, ange 200

        3. SVART på NORR, ange 300

    10. Stäng fönstret efterfrågeprognos

4. Kör MPS-plan i maj för skapade efterfrågeprognoser. Granska komponenter för att se att artikelfärgen är korrelerad med variant.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du *planeringsförslag* och väljer sedan relaterad länk.

    2. Välj åtgärden **Beräkna fullständig plan**.

    3. Växla på fältet **MPS**.

    4. Växla av fältet **MPS**.

    5. I fältet **Startdatum** välj *1 maj*

    6. I fältet **Slutdatum** välj *31 maj*

    7. I fältet **Använd prognos**, välj *AUTODRIP*

    8. Välj åtgärden **OK**.

    9. För varje skapad rad väljer du **komponent**-åtgärden och kontrollerar vilken färg som används.  

## Se även

[Introduktion till demonstrationsdata för Contoso Coffee](contoso-coffee-intro.md)  
