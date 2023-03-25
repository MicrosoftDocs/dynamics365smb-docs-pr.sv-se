---
title: Skapa cykler för affärsmöjligheter och cykeletapper
description: Beskriver hur du definierar säljetapper från första kontakt till avslut om du vill skapa en försäljningscykel och tilldela affärsmöjligheter i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5122, 5121, 5120, 5175, 5119, 5098, 5096'
ms.date: 05/27/2022
ms.author: jswymer
---
# Skapa cykler för affärsmöjligheter och cykeletapper

Innan du börjar använda affärsmöjligheter måste du skapa försäljningscykler och försäljningscykeletapper. En försäljningscykel består av en serie etapper från den första kontakten till en genomförd försäljning. För varje steg definierar du vissa krav som måste uppfyllas, till exempel att kräva en förs.offert innan en affärsmöjlighet kan gå till nästa etapp. Du kan också ange om en etapp kan hoppas över. Du kan skapa ett valfritt antal försäljningscyklar. Du kan upprätta så många försäljningscykeletapper som behövs inom en försäljningscykel.

Att använda affärsmöjlighetscykeler omfattar att skapa försäljningscykel och definiera de olika etapperna i cykeln och sedan tilldela cykeln till affärsmöjligheter. Tilldela relevant affärsmöjlighet eller uppgifter till kan också vara ställer in en försäljningscykel.

Det här avsnittet beskriver även hur du ställer in uppgifter och aktiviteter och tilldela uppgifter till aktiviteter. Mer information finns i [Skapa aktiviteter med uppgifter](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## Så här skapar du cykelkoder för affärsmöjligheter:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningscykler** och väljer sedan relaterad länk. Sidan **Försäljningscykler** öppnas och visar alla befintliga försäljningscyklar.
2. Välj åtgärden **Ny** och fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Upprepa stegen för varje säljcykel du vill skapa. När du har skapat cykler för affärsmöjligheter vill du kanske skapa de olika etapperna i varje cykel.

## Om du vill definiera etapper för försäljningscykel för affärsmöjligheter

1. På sidan **Försäljningscykler** markerar du den försäljningscykel för affärsmöjligheter som du vill ställa in etapper för och väljer sedan åtgärden **Etapper**. Sidan **Försäljningscykeletapper** öppnas.
2. Välj åtgärden **Ny** för att skapa en ny etapp i försäljningscykeln.

Upprepa stegen för varje etapp du vill skapa i försäljningscykeln.

## Så här tilldelar du cykler till affärsmöjligheten.

När du har lagt till försäljningscykeln till affärsmöjligheten, kan du börja lägga till affärsmöjligheter och sedan tilldela etappen för försäljningscykeln till affärsmöjligheten genom att ange fältet **försäljningscykelkod**. Mer information finns i [Så här skapar du försäljningsmöjligheter](marketing-how-create-opportunities.md).

## Så här skapar du aktiviteter med uppgifter

Du kan kombinera flera uppgifter, till exempel uppgifter som var och en representerar ett steg i aktiviteter. Alla steg i en aktivitet är knutna till varandra med hjälp av en datumformel. Du kan tilldela aktiviteter till affärsmöjligheter, säljare eller kontakter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Aktiviteter** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i fälten efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. På snabbfliken **rader** fyller du i fälten för att definiera en eller flera uppgifter i aktiviteten.

## Tilldela uppgifter eller aktiviteter till affärsmöjligheter

När du har lagt upp en aktivitet kan du tilldela aktiviteten som uppgiften tillhör och därmed tilldela affärsmöjligheter.

> [!NOTE]
> Du kan inte skapa aktiviteter av typen *möte* i [!INCLUDE [prod_short](includes/prod_short.md)] online. Funktionen kräver åtkomst till en lokal distribution.

Följande proceduren beskriver hur du tilldelar aktiviteter för aktiviteten till affärsmöjligheter. Momentet är liknande när du tilldelar aktiviteter till kontakter och säljare.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Affärsmöjligheter** och väljer sedan relaterad länk.
2. Välj en affärsmöjlighet och välj sedan åtgärden **Uppgifter**.
3. På sidan **Uppgiftslista**, välj åtgärden **Skapa uppgift**.
4. På sidan **Skapa uppgift** fyller du i fälten efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Som du kan se i fältet **affärsmöjlighet** att det tilldelas automatiskt till den aktuella affärsmöjligheten.
5. Välj **OK**.
6. På sidan **Uppgiftslista** väljer du en ny uppgift och väljer sedan åtgärden **Tilldela aktiviteter**.
7. På sidan **Tilldela aktiviteter** fyller du i fälten efter behov och väljer sedan knappen **OK**.

## Se även

[Behandlar försäljningsmöjligheter](marketing-processing-sales-opportunities.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]