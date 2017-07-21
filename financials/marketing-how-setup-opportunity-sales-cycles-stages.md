---
title: "Så här skapar du cykler för affärsmöjligheter och cykeletapper | Microsoft Docs"
description: "Beskriver hur du definierar säljetapper från första kontakten till avslut om du vill skapa en försäljningscykel och tilldela affärsmöjligheter i Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 29f9caa8f01fe8e4cfd0f65cc290d82a49fb36bb
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Så här skapar du cykler för affärsmöjligheter och cykeletapper
Innan du börjar använda affärsmöjligheter måste du skapa försäljningscykler och försäljningscykeletapper. En försäljningscykel består av en serie etapper från den första kontakten till en genomförd försäljning. Varje etapp kan ha vissa krav som måste uppfyllas, till exempel att kräva en förs.offert innan en affärsmöjlighet kan gå till nästa etapp. Du kan också ange om en etapp kan hoppas över. Du kan skapa ett valfritt antal försäljningscykler och så många etapper som behövs inom en försäljningscykel.

Att använda affärsmöjlighetscykeler omfattar att skapa försäljningscykel och definiera de olika etapperna i cykeln och sedan tilldela cykeln till affärsmöjligheter. Tilldela relevant affärsmöjlighet eller uppgifter till kan också vara ställer in en försäljningscykel.

Det här avsnittet beskriver även hur du ställer in uppgifter och aktiviteter och tilldela uppgifter till aktiviteter. Mer information finns i avsnittet ”Skapa aktiviteter med uppgifter”.

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Så här skapar du cykelkoder för affärsmöjligheter:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningscykler**, och välj sedan relaterad länk. Fönstret **Försäljningscykler** öppnas och visar alla befintliga försäljningscyklar.
2. Välj åtgärden **Ny** och fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Upprepa stegen för varje säljcykel du vill skapa. När du har skapat cykler för affärsmöjligheter vill du kanske skapa de olika etapperna i varje cykel.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Om du vill definiera etapper för försäljningscykel för affärsmöjligheter
1. I fönstret **Försäljningscykler** markerar du den försäljningscykel för affärsmöjligheter som du vill ställa in etapper för och väljer sedan åtgärden **Etapper**. Fönstret **Försäljningscykeletapper** öppnas.
2. Välj åtgärden **Ny** för att skapa en ny etapp i försäljningscykeln.

Upprepa stegen för varje etapp du vill skapa i försäljningscykeln.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Så här tilldelar du cykler till affärsmöjligheten.
När du har lagt till försäljningscykeln till affärsmöjligheten, kan du börja lägga till affärsmöjligheter och sedan tilldela etappen för försäljningscykeln till affärsmöjligheten genom att ange fältet **försäljningscykelkod**. Mer information finnsi [Så här skapar du Försäljningsmöjligheter](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Så här skapar du aktiviteter med uppgifter
Du kan kombinera flera uppgifter, till exempel uppgifter som var och en representerar ett steg i aktiviteter. Alla steg i en aktivitet är knutna till varandra med hjälp av en datumformel. Du kan tilldela aktiviteter till affärsmöjligheter, säljare eller kontakter.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningscykler**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i fälten efter behov.
3. På snabbfliken **rader** fyller du i fälten för att definiera en eller flera uppgifter i aktiviteten.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Tilldela uppgifter eller aktiviteter till affärsmöjligheter
När du har lagt upp en aktivitet kan du tilldela aktiviteten som uppgiften tillhör och därmed tilldela affärsmöjligheter.

> [!NOTE]  
>   Den här proceduren beskriver hur du tilldelar aktiviteter för aktiviteten till affärsmöjligheter. Momentet är liknande när du tilldelar aktiviteter till kontakter och säljare.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningscykler**, och välj sedan relaterad länk.
2. Välj en affärsmöjlighet och välj sedan åtgärden **Uppgifter**.
3. I fönstret **Uppgiftslista**, välj åtgärden **Skapa uppgift**.
4.  I fönstret **Skapa uppgift** fyller du i fälten efter behov.

    Du ser i fältet **affärsmöjlighet** att det tilldelas automatiskt till den aktuella affärsmöjligheten.
5. Välj **OK**.
6. I fönstret **Uppgiftslista** väljer du en ny uppgift och väljer sedan åtgärden **Tilldela aktiviteter**.
7. I fönstret **Tilldela aktiviteter** fyller du i fälten efter behov och väljer sedan knappen **OK**.

## <a name="see-also"></a>Se även
[Behandlar försäljningsmöjligheter](marketing-processing-sales-opportunities.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

