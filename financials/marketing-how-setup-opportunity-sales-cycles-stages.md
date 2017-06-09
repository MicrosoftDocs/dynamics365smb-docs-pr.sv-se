---
title: "Så här skapar du cykler för affärsmöjligheter och cykeletapper | Microsoft Docs"
description: "Beskriver hur du skapar cykler för affärsmöjligheter och cykeletapper i Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Så här skapar du cykler för affärsmöjligheter och cykeletapper
Innan du börjar använda affärsmöjligheter måste du skapa försäljningscykler och försäljningscykeletapper. En försäljningscykel består av en serie etapper från den första kontakten till en genomförd försäljning. Varje etapp kan ha vissa krav som måste uppfyllas, till exempel att kräva en förs.offert innan en affärsmöjlighet kan gå till nästa etapp. Du kan också ange om en etapp kan hoppas över. Du kan skapa ett valfritt antal försäljningscykler och så många etapper som behövs inom en försäljningscykel.

Att använda affärsmöjlighetscykeler omfattar att skapa försäljningscykelkoden och definiera de olika etapperna i cykeln och sedan tilldela cykeln till affärsmöjligheter.

## <a name="to-set-up-an-opportunity-sales-cycle-code"></a>Så här skapar du cykler för affärsmöjlighetskod
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **försäljningscykler**, och välj sedan relaterad länk. Fönstret **Försäljningscykler** öppnas och visar alla befintliga försäljningscyklar.
2. Välj åtgärden **Ny** och fyll i fälten.

Upprepa stegen för varje säljcykel du vill skapa. När du har skapat cykler för affärsmöjligheter vill du kanske skapa de olika etapperna i varje cykel.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Om du vill definiera etapper för försäljningscykel för affärsmöjligheter
1. I fönstret **Försäljningscykler** markerar du den försäljningscykel för affärsmöjligheter som du vill ställa in etapper för och väljer sedan åtgärden **Etapper**. Fönstret **Försäljningscykeletapper** öppnas.
2. Välj åtgärden **Ny** för att skapa en ny etapp i försäljningscykeln.

Upprepa stegen för varje etapp du vill skapa i försäljningscykeln.

## <a name="to-assign-stage-cycle-to-an-opportunity"></a>Så här tilldelar du försäljningscykeln till affärsmöjligheten.
När du har lagt till försäljningscykeln till affärsmöjligheten, kan du börja lägga till affärsmöjligheter och sedan tilldela etappen för försäljningscykeln till affärsmöjligheten genom att ange fältet **försäljningscykelkod**. Mer information finnsi [Så här skapar du Försäljningsmöjligheter](marketing-how-create-opportunities.md).

## <a name="see-also"></a>Se även
[Behandlar försäljningsmöjligheter](marketing-processing-sales-opportunities.md)  
[Försäljning](sales-manage-sales.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

