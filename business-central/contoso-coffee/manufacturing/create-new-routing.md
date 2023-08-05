---
title: Skapa en ny operationsföljd
description: En genom gång för att lära dig att ange all information för en ny operationsföljd manuellt i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# Genomgång: Skapa en ny operationsföljd

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demonstrationsdata för att konfigurera en ny operationsföljd för produktion manuellt i [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## Scenario

Oscar, processteknikern på Contoso Coffee, bestämmer sig för att skapa en ny operationsföljd med namnet *Ny sökväg*. Eftersom operationsföljden inte fungerar som någon annan operationsföljd på Contoso Coffee måste Oscar manuellt ange all information för operationsföljden.  

## Steg

1. Skapa huvudet för operationsföljden.  

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Operationsföljder** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Nr** |1099|
        |**Beskrivning** |Ny sökväg|
2. Skapa operationsföljdsraderna.

    1. På snabbfliken **Rader** lägger du till en ny rad innan du fyller i fälten enligt beskrivet i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Operationsnr** |10|
        |**Radtyp** |Produktionsgrupp|
        |**Nr** |100|
        |**Omställningstid** |20|
        |**Bearbetningstid** |15|

    2. Lägg till en ny rad innan du fyller i fälten enligt beskrivet i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Operationsnr** |20|
        |**Radtyp** |Produktionsgrupp|
        |**Nr** |200|
        |**Omställningstid** |30|
        |**Bearbetningstid** |5|
3. Godkänn verksamhetsföljden.

    1. Markera *Certifierad* i fältet **Status** .  

Den nya operationsföljden har nu konfigurerats.  

## Se även

[Introduktion till demonstrationsdata för Contoso Coffee](../contoso-coffee-intro.md)  
