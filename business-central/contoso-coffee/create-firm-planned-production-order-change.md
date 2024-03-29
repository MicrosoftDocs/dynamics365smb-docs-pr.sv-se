---
title: Skapa en fast planerad produktionsorder och ändra den
description: Genomgången för en produktionsplanerare på Contoso Coffee som vill skapa en fast planerad produktionsorder och sedan ändra den.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Genomgång: Skapa en fast planerad produktionsorder och ändra den

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demodata för att arbeta med produktionsorder.  

## Scenario

Eduardo, produktionsplanerare på Contoso Coffee, måste skapa en ny produktionsorder för 10 enheter av artikeln **SP-SCM1009, Airpot** som måste betalas den 28 april. Han bakåtplanerar detta och bekräftar att han kan starta ordern den 27 april.  

Kort efter att han är klar med denna uppgift ombeds han att öka ordern till 50 enheter. När han gör det, flyttar funktionen för bakåtplanering startdatumet för ordern till en för tidig tidpunkt. Han framåtbokar då ordern från den 23 april för att fastställa ett mer realistiskt slutdatum.  

## Steg

1. Skapa den första produktionsordern för 10 enheter av artikeln **SP-SCM1009, Airpot**.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **fast planeradw prod.order** och välj sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Ursprungstyp** |Artikel|
        |**Ursprungsnr** |SP-SCM1009|
        |**Antal** |10|
        |**Förfallodatum**|April 28  |

    3. Välj åtgärden **Uppdatera produktionsorder**.  

    4. På sidan **Uppdatera produktionsorder** accepterar du alla standardvärden och väljer sedan knappen **OK** för att starta bearbetningen.  

        I den aktuella konfigurationen använder processen bakåtplanering. På den nya raden i produktionsordern är startdatumet 26 april.  

2. Ändra antalet i produktionsordern till 50 enheter och tidsplanera ordern.  

    1. På snabbfliken **Rader** i **produktionsstrukturen** markerar du den nyligen tillagda raden och anger i fältet **Kvantitet** därefter värdet *50*.  

3. Välj åtgärden **Uppdatera produktionsorder**.  

    Startdatumet har nu flyttats tillbaka till 20 april. Detta är inte ett acceptabelt datum för Eduardo.

4. Utlös en framåtplanering av produktionsordern.

    1. På snabbfliken **Schema** anger du fältet **Startdatum** som den *23 april*.

    Starten för ordern är nu 25 april och slutdatum är 2 maj. Förfallodatumet för ordern anges som en dag senare, d.v.s. 3 maj. Eduardo vet nu att det tar tills 3 maj 3 att leverera den utökade ordern.

> [!NOTE]
> När du planerar en order genom att ändra dess start-eller slutdatum krävs inte batchjobbet **Uppdatera produktionsorder** eftersom alla datum räknas om automatiskt.

Den nya produktionsordern har nu skapats, och Eduardos krav har uppfyllts.  

## Se även

[Introduktion till demonstrationsdata för Contoso Coffee](contoso-coffee-intro.md)  
