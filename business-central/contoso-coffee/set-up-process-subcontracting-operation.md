---
title: Ställ in och hantera en legotillverkningsoperation
description: Genomgång för att lära dig hur du ställer in och bearbetar en underleverantörsverksamhet i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Ställ in och hantera en legotillverkningsoperation

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demodata i legotillverkning.

## Scenario

Du arbetar med produktionsplaneraren på Contoso Coffee. På grund av kapacitetsbegränsningarna planerar du att använda en underleverantör för att producera artikeln **SP-SCM1009, Airpot**.

Här skapar du en ny släppt produktionsorder för 12 enheter av artikeln SP-SCM1009, Airpot, med routing-SP-SCM1009-SUB-2. Använd arbetsbladet för underleverantörer för att generera en inköpsorder för produktionen och avsluta sedan operationen genom att ta emot och fakturera inköpsordern.

## Steg

1. Skapa den nya släppta produktionsordern för 12 enheter av artikeln SP-SCM1009, Airpot.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utsläppta produktionsorder** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Ursprungstyp** |Artikel|
        |**Ursprungsnr** |SP-SCM1009|
        |**Antal** |100|
    3. Välj åtgärden **Uppdatera produktionsorder**.  

2. Ersätt operationsföljden till SP-SCM1009-SUB-2 på produktionsorderraden och uppdatera sedan produktionsordern, men endast för flöde.  

    1. Lägg till produktionskvantitet fält till raderna i den utsläppta produktionsorderraden.<!--in code, this is marked as visible=false-->

    2. Ändra fältet **Operationsföljdsnr.** från *SP-SCM1009-SERIAL* till *SP-SCM1009-SUB-2*.  

    3. Välj åtgärden **Uppdatera produktionsorder**.  

    4. På sidan **uppdatera produktionsorder** förfrågan avmarkerar du fälten **rader** och **komponentbehov** så att aktiviteten bara kan köras för att dirigera och sedan välja **OK**.

3. Använd arbetsbladet för underleverantörer för att generera en inköpsorder för underleverantörsoperationen på produktionsordern som du skapade i steg 2.  

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Legotillverkningsförslag** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Beräkna kalkylark**.

    3. Välj fältet **Acceptera åtgärdsmeddelande** för den nya raden.

    4. Välj den **Verkställ åtgärdsmeddelande** åtgärd.  

    5. Sidan för förfrågan **Utför åtgärdsmeddelande – Req.** begäran sida, acceptera alla standardvärden och välj sedan **OK**.

    6. När batch-jobbet är klart väljer du knappen **OK** för att stänga legotillverkningsförslag.  

4. Ta emot och fakturera inköpsordern.  

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  

    2. I listan **inköpsorder** söker du upp inköps ordern från leverantör 82000 underleverantör.

    3. I fältet **Leverantörsfaktura nr.** ange *542349*.

    4. På snabbfliken **Rader** markerar du raden och ställer sedan in fältet **inköpskostnad** på *18*.

    5. Välj åtgärden **Bokföra**.  

    6. På begäran meddelande, välj **Inleverera och fakturera**.  

Utflödet från artikel SP-SCM1009 Airpot är nu registrerat.

## Se även

[Introduktion till demonstrationsdata för Contoso Coffee](contoso-coffee-intro.md)  
