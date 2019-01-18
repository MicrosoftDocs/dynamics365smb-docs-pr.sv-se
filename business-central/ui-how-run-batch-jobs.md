---
title: "Skapa och köra ett batch-jobb | Microsoft Docs"
description: "Du kör batch-jobben för att bearbeta data och uppdatera information, till exempel, att göra regelbundna redovisningsaktiviteter eller för att utföra beräkningar."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 7357ae501c4b53ae66869bbbc1ce415a3996f542
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="run-batch-jobs"></a>Kör batchjobb
Ett batch-jobb i är en rutin som bearbetar data i omgångar, till exempel batch-jobbet **Justera valutakurser**. Det finns batch-jobb som utför regelbundna redovisningsaktiviteter, som till exempel att stänga resultaträkningen i slutet av ett räkenskapsår. Många batch-jobb utför beräkningsarbetet, t.ex beräkning av dröjsmålsränta, valutakursjustering och beräkning av styckkostnaden.

Ett batch-jobb påminner om en rapport, förutom att batch-jobbet använder resultatet från åtgärden för att uppdatera informationen direkt, i stället för att skriva ut resultatet.

## <a name="to-run-a-batch-job"></a>Så här kör du ett batch-jobb:
1. Öppna definitionssidan för önskat batch-jobb, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange namnet på batch-jobbet och välj sedan relaterad länk.
2. Om snabbfliken **Alternativ** finns för batch-jobbet fyller du i fälten för att bestämma vad batch-jobbet ska utföra.
3. Sidan kanske innehåller en eller flera snabbflikar med filter, som du kan använda för att begränsa vilka data som ingår i batch-jobbet. Du kan ange villkor i de föreslagna filtren eller lägga till fler filter.
4. Klicka på **OK** för att starta batchjobbet.

## <a name="see-also"></a>Se även
[Söka, filtrera och sortera data](ui-enter-criteria-filters.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

