---
title: Använda orderplanering för att skapa och reservera leverans
description: I genom gången för att lära dig hur du använder orderplanering för att skapa en produktionsorder som krävs för leverans i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Genomgång: Använda orderplanering för att skapa och reservera leverans

I den här artikeln tar vi dig genom stegen för att använda Contoso Coffees demodata för att planera.

## <a name="scenario"></a>Scenario

Du arbetar med produktionsplaneraren på Contoso Coffee. Du har skapat en produktions order för 100 enheter av artikeln **SP-SCM1009, Airpot** och du vill planera del enheter för ordern. Du använder orderplanering när du vill skapa en produktionsorder som krävs för leveransen. Eftersom du skapar produktionsordern för att uppfylla kraven från en specifik order bestämmer du dig för att reservera utflödet av produktionsordern.  

## <a name="steps"></a>Steg

1. Skapa den nya släppta produktionsordern för 100 enheter av artikeln **SP-SCM1009, Airpot**.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utsläppta produktionsorder** och väljer sedan relaterad länk.  

    2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

        |Fält  |Värde  |
        |---------|---------|
        |**Ursprungstyp** |Artikel|
        |**Ursprungsnr** |SP-SCM1009|
        |**Antal** |100|
    3. Välj åtgärden **Uppdatera produktionsorder**.  

    Notera nummer för utsläppt produktionsorder.

2. Öppna sidan **orderplanering** och beräkna en ny plan.

    1. Välj åtgärden **Planerad**.  

    2. På sidan **Orderplanering** väljer du åtgärden **Skapa inköpsförslag**.  

    3. Bläddra ned till den efterfrågerad som motsvarar den släppta produktionsorder som du skapade tidigare.  

    4. Expandera raderna för att se detaljerna för efterfrågeraden. Bekräfta att det är ett förslag för en produktionsorder på 100 enheter av artikel 1001.  

3. Skapa en ny produktions order för 100 enheter av artikeln **SP-BOM2000, Tankmont.** och reservera produktionen för den här produktionsordern på uppdrag av den relaterade överordnade ordern.  

    1. Markera kryss rutan i fältet **reservera** på efterfrågeraden för 100 enheter av artikeln SP-BOM2000.

    2. Välj åtgärden **Skapa order**.  

    3. Ställ in fältet **skapa order för** den *aktiva raden*.  

    4. Ställ in fältet **Skapa produktionsorder** på *fast planerade*.

    5. Välj **OK** för att skapa produktionsordern.

    6. På sidan **orderplanering** bekräftar du att efterfrågeraden för 100-enheterna för artikel 1001 har tagits bort.

Det är det för orderplanering i [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="see-also"></a>Se även

[Introduktion till demonstrationsdata för Contoso Coffee](../contoso-coffee-intro.md)  
[Om produktionsorder](../../production-about-production-orders.md)  
