---
title: "Så här kör du batch-jobb | Microsoft Docs"
description: "Lär dig hur batchjobb fungerar i Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1f4678ce0cfb18a746374226bb33020f70bf874d
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-run-batch-jobs"></a>Så här kör du batch-jobb
Ett batch-jobb i är en rutin som bearbetar data i omgångar, till exempel batch-jobbet **Justera valutakurser**. Det finns batch-jobb som utför regelbundna redovisningsaktiviteter, som till exempel att stänga resultaträkningen i slutet av ett räkenskapsår. Många batch-jobb utför beräkningsarbetet, t.ex beräkning av dröjsmålsränta, valutakursjustering och beräkning av styckkostnaden.

Ett batch-jobb påminner om en rapport, förutom att batch-jobbet använder resultatet från åtgärden för att uppdatera informationen direkt, i stället för att skriva ut resultatet.

## <a name="to-run-a-batch-job"></a>Så här kör du ett batch-jobb:
1. Om du vill öppna förfråganfönstret för det relevanta batch-jobbet, väljer du ikonen **Sök efter sida eller rapport** ![Sök efter sida eller rapport](media/ui-search/search_small.png "ikonen Sök efter sida eller rapport") anger namnet på batch-jobbet och väljer sedan relaterad länk.
2. Om snabbfliken **Alternativ** finns för batch-jobbet fyller du i fälten för att bestämma vad batch-jobbet ska utföra.
3. Fönstret kanske innehåller en eller flera snabbflikar med filter, som du kan använda för att begränsa vilka data som ingår i batch-jobbet. Du kan ange kriterier i de föreslagna filtren eller lägga till fler filter.
4. Klicka på **OK** för att starta batchjobbet.

## <a name="see-also"></a>Se även
[Ange villkor i filter](ui-enter-criteria-filters.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

