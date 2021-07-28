---
title: Skapa och köra ett batch-jobb | Microsoft Docs
description: Du kör batch-jobben för att bearbeta data och uppdatera information, till exempel, att göra regelbundna redovisningsaktiviteter eller för att utföra beräkningar.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 42cb5f19dde06211136b0b3b276fed2ba267ec62
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435275"
---
# <a name="run-batch-jobs-and-xmlports"></a>Kör batch-jobb och XML-portar
Ett batch-jobb i är en rutin som bearbetar data i omgångar, till exempel batch-jobbet **Justera valutakurser**. Det finns batch-jobb som utför regelbundna redovisningsaktiviteter, som till exempel att stänga resultaträkningen i slutet av ett räkenskapsår. Många batch-jobb utför beräkningsarbetet, t.ex beräkning av dröjsmålsränta, valutakursjustering och beräkning av styckkostnaden.

Ett batch-jobb påminner om en rapport, förutom att batch-jobbet använder resultatet från åtgärden för att uppdatera informationen direkt, i stället för att skriva ut resultatet.

Du kan schemalägga när ett batchjobb körs. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Så här kör du ett batch-jobb:
1. Om du vill öppna sidan för begäran för det relevanta batch-jobbet väljer du ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du namnet på batch-jobbet och väljer sedan relaterad länk.
2. Om snabbfliken **Alternativ** finns för batch-jobbet fyller du i fälten för att bestämma vad batch-jobbet ska utföra.
3. Sidan kanske innehåller en eller flera snabbflikar med filter, som du kan använda för att begränsa vilka data som ingår i batch-jobbet. Du kan ange villkor i de föreslagna filtren eller lägga till fler filter.
4. Klicka på **OK** för att starta batchjobbet.

## <a name="see-also"></a>Se även
[Sortera, söka och filtrera listor](ui-enter-criteria-filters.md)  
[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]