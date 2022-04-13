---
title: Kombinera automatisk och manuell "flushing"
description: Genomgång för en produktionsplanerare på Contoso Coffee som vill kombinera automatisk och manuell "flushing".
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 6b128f79cb8e629147bdd5ae77f2545ad0f7025c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525183"
---
# <a name="walkthrough-combine-automatic-and-manual-flushing"></a>Genomgång: Kombinera automatisk och manuell "flushing"

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demonstrationsdata inom "flushing".  

## <a name="scenario"></a>Scenario

Du arbetar med produktionsplaneraren på Contoso Coffee. Du måste skapa den nya produktionsordern för tio enheter av artikeln SP-SCM1004, AutoDrip. Vissa komponenter och åtgärder "flushas" framåt, andra bakåt baserat på olika villkor.

## <a name="steps"></a>Steg

1. Skapa en fast planerad produktionsorder för fem enheter av artikeln **SP-SCM1004, AutoDrip**. Mer information finns i avsnittet [Genomgång: Skapa en fast planerad produktionsorder och ändra den](create-firm-planned-production-order-change.md).  

2. Frisläpp produktionsordern.

    1. Välj åtgärden **Ändra status**.  

    2. På sidan som visas anger du fältet **Ny Status** som *Utsläppt* och väljer sedan knappen **Ja**.  

        Ett meddelande med ett statusfält visas och refererar till automatisk förbrukning. Detta följs av ett bekräftelsemeddelande om att ordern ändras till statusen *Utsläppt*.  

    3. Välj knappen **OK** att stänga bekräftelsemeddelandet.

3. Granska artikel- och kapacitetstransaktionerna för produktionsordern.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utsläppta produktionsorder** och väljer sedan relaterad länk.  

    2. Öppna produktionsordern med 5 enheter av kaffemaskinen AutoDrip.  

    3. Välj åtgärden **Artikeltransaktioner**.  

        Artikeln **SP-BOM1305 skruv hex M3 zink** "flushas" omedelbart med den fullständiga förväntade kvantiteten. Stäng sidan **Artikeltransaktioner**.  

    4. Välj åtgärden **Kapacitetstransaktioner**.  Observera att en åtgärdstransaktion för sammansättning också slutfördes när ordern släpptes. Stäng fönstret **Kapacitetstransaktioner**.

    Du kan "flusha" komponentartiklar manuellt med hjälp av förbruknings- eller produktionsjournalen. Med manuell "flushing" kan du justera kvantiteten före bokföring. Till exempel om ytterligare kvantitet behövs för att täcka råmaterial med låg kvalitet.
4. "Flusha" komponenter manuellt.  
    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **förbrukningsjournal** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Beräkna förbrukning**.  

    3. På begärandesidan **Beräkna förbrukning**, på snabbfliken **Produktionsorder** anger du ett filter för den angivna ordern i fältet **Ordernr.** och väljer sedan knappen **OK**. När sidan för begäran om batch-jobb stängs, kommer sidan **Förbrukningsjournal** att fyllas i med komponenterna som kräver manuell förbrukning.

    4. Välj åtgärden **Bokför**. Stäng förbrukningsjournalen.

5. Registrera utdata för elledningar manuellt.  

    Du måste fylla i fälten **Konfigurationstid** och **Bearbetningstid**. Du kan också ange den faktiskt producerade kvantiteten och kassationen. Ange *3* som utflödeskvantitet och bokför utflödet.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **utflödesjournal** och väljer sedan relaterad länk.  

    2. På sidan **Utflödesjournal** skapar du en ny journalrad.  

    3. I fältet **Ordernr.** anger du ordningen.  

    4. Välj åtgärden **Expandera operationsföljd**.  

        Sidan **Utflödesjournaler** fylls i med endast driftsraden för den elektriska kabeln.

    5. Ange fältet **Bearbetningstid** som *10*.  

    6. Ändra fältet **Kvantiet** från *5* till *3*.

    7. Välj **Bokför**.  
    8. Stäng utflödesjournalen.

6. Granska artikeltransaktionerna för produktionsordern.

    1. Välj åtgärden **artikeltransaktioner** på sidan för produktionsordern.  

    Artikeln **SP-BOM1302, Kontrollpanelskärm** bokförs med antalet *3*, baserat på faktiskt utflöde, medan **SP-BOM1303, Knapp** med det fullständiga förväntade antalet. Stäng sidan **Artikeltransaktioner**.

7. Avsluta produktionsordern.  

    1. Välj åtgärden **Ändra status**.
    2. På sidan som visas anger du fältet **Ny Status** som *Avslutad* och väljer sedan knappen **Ja**.  

        Ett meddelande visas med ett statusfält som visar den automatiska förbrukningen. Detta åtföljs av ett bekräftelsemeddelande om att ordern ändrats till en order med statusen *Avslutad*. Den färdiga produktionsordern har samma nummer som den hade med statusen *Frisläppt*.
    3. Välj knappen **OK** att stänga bekräftelsemeddelandet.

8. Granska artikel- och kapacitetstransaktionerna för produktionsordern igen.

    1. Välj åtgärden **Kapacitetstransaktioner**.  

        Förpackningsåtgärdstransaktionen slutfördes i det ögonblick då ordern frisläpptes. Den producerade kvantiteten (utflödet) är *5*, oavsett resultatet av föregående steg. Stäng sidan **Kapacitetstransaktioner**.

    2. Välj åtgärden **Artikeltransaktioner**.  

        Antalet i artikeltransaktionen av typen *utflöde* är lika med utflödesantalet i kapacitetstransaktionsposten. Det förbrukade antalet **SP-BOM1301, Housing AutoDrip** och **SP-BOM1304, Rostfri termoskanna** är 5 för båda eftersom förväntat utflöde och faktiskt utflöde är detsamma. 

    3. Stäng sidan **Artikeltransaktioner**.  

Det var allt för manuell och automatisk "flushing" av komponenter.

## <a name="see-also"></a>Se även

["Flusha" komponenter utifrån verksamhetens utflöde](../production-how-to-flush-components-according-to-operation-output.md)  
[Introduktion till demonstrationsdata för Contoso Coffee](contoso-coffee-intro.md)  
