---
title: Skapa en ny produktionsstruktur och strukturversion
description: En genomgång för att lära dig hur du lägger till en ny kaffemaskin i Contoso Coffees produktlinje i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---
# Genomgång: Skapa en ny produktionsstruktur och strukturversion

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demonstrationsdata för att arbeta med strukturlistor i produktionsprocesser.  

## Scenario

Contoso Coffee har beslutat att lägga till ytterligare en kaffemaskin i sin produktlinje: **SP-SCM1008 Airpot lite**. Denna kaffemaskin är identisk med den befintliga artikeln **SP-SCM1009 Airpot**, förutom att värmeplattan, **SP-BOM1104**, inte ingår. I ett separat steg tas på/av-ljuset, **SP-BOM1106**, bort för en bersion av Airpot Lite-strukturen.

Oscar, processteknikern på Contoso Coffee, måste skapa en ny produktionsstruktur för att definiera de ursprungliga komponentbehoven för Airpot Lite. Oscar måste sedan skapa en ny sturkturversion med startdatumet 1 juli för att matcha ytterligare planer för släpp av en kommande utgåva.

## Steg

1. Skapa en ny produktionsstruktur för Airpot Lite.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Prod.struktur** och välj sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Nr** |SP-SCM1008|
        |**Beskrivning** |Airpot Lite|
        |**Måttenhetskod**|STYCK  |

2. Kopiera strukturkomponenterna från produktionsstrukturen **SP-SCM1009**.

    1. Välj åtgärden **Kopieringsstruktur**.

    2. På sidan **Produktionsstrukturer** väljer du raden för **SP-SCM1009, Airpot** och sedan knappen **OK**.

3. Ändra komponenterna för den nya produktionsstrukturen enligt beskrivningen i scenariot.

    1. På snabbfliken **Rader** väljer du raden för artikeln **SP-BOM1104** och sedan åtgärden **Radera rad**.  

4. Godkänn den nya strukturen.  

    1. Markera *Certifierad* i fältet **Status** .  

5. Skapa en ny produktionsstrukturversion för Airpot Lite.

    1. Välj åtgärden **Versioner**.

    2. På sidan **Versionslista för prod-struktur** väljer du åtgärden **Ny** och fyller sedan i fälten enligt beskrivet i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Versionskod** |02|
        |**Beskrivning** |Airpot Lite, v2|
        |**Måttenhetskod**|STYCK  |  
        |**Fr.o.m.-datum**|Juli 01  |  

6. Kopiera komponentraderna från produktionsstrukturen till den nya strukturversionen.

    1. Välj åtgärden **Kopiera struktur** och klicka sedan på knappen **Ja** för att kopiera komponenterna från den ursprungliga produktionsstrukturen.

7. Ta bort artikeln **SP-BOM1106, ljus På/Av** från versionskomponenterna.

8. Godkänn den nya strukturversionen.

    1. Markera *Certifierad* i fältet **Status** .  

    2. Stäng stukturversionen

Den nya kaffemaskinen har nu konfigurerats som en produktionsstruktur med en enda version.  

## Se även

[Introduktion till demonstrationsdata för Contoso Coffee](../contoso-coffee-intro.md)  
