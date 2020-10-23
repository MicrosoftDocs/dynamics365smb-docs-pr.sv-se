---
title: Definiera allmänna lagerinställningar
description: Beskriver hur du definierar den allmänna lagerinställningen så att du kan hantera distributionslagret och lagret.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 73fbf09cff59556c04b43383c507a01883bbb071
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923751"
---
# <a name="set-up-general-inventory-information"></a>Ställa in allmän lagerinformation

Du ställer in dina allmänna lagerinställningar på sidan **Lagerinställningar**.

## <a name="to-set-up-general-inventory-information"></a>Så här ställer du in allmän lagerinformation

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerinställningar** och välj sedan relaterad länk.
2. På sidan **Lagerinställningar** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Detaljerad information om kostnadsfälten, **Automatisk kostnadsbokföring**, **Förväntad kost.bokf. i redov.** och **Standarvärderingsprincip** finns i [Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md) och [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md). Mer information om kostnadsredovisning i allmänhet finns i [Hantera lagerkostnad](finance-manage-inventory-costs.md).  

Om du vill ange en ankommande lagerhanteringstid som ska tas med i orderlöftesberäkningen på inköpsraden, kan du ange tiden som standard för lagret på sidan **Lagerinställning** och för lagerstället. Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Reglaget **Automatisk kostnadsjustering** är aktiverat som standard för att säkerställa att lagervärden alltid är korrekta i redovisningen, vilket i sin tur innebär att försäljnings- och vinststatistik är aktuell. Kostnadsändringar från ankommande transaktioner, t.ex. de för inköp eller produktionsutflöde tilldelas relaterade avgående transaktioner, t.ex. försäljningar eller överföringar. Detta är användbart för nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder och mindre företag med relativt låga lagertransaktionsnivåer. När företaget växer och lagernivåerna ökar kan detta emellertid sakta ner systemets prestanda. Om du vill förhindra att prestandan vid bokföringen försämras väljer du ett tidsalternativ för att definiera hur långt tillbaka i tiden från arbetsdatumet som en ankommande transaktion kan inträffa för att eventuellt utlösa justeringar av relaterade avgående värdetransaktioner. Du kan också justera kostnader manuellt med jämna mellanrum med batch-jobbet Justera kost.-artikeltrans.

## <a name="see-also"></a>Se även
[Lagerinställning](inventory-setup-inventory.md)  
[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)    
[Hantera lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)
