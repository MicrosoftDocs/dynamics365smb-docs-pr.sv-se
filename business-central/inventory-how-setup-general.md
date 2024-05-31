---
title: Ställa in allmän lagerinformation
description: Beskriver hur du definierar den allmänna lagerinställningen så att du kan hantera distributionslagret och lagret.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.form: '30, 456, 461'
ms.date: 07/28/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-general-inventory-information"></a>Ställa in allmän lagerinformation

Du ställer in dina allmänna lagerinställningar på sidan **Lagerinställningar**.

## <a name="to-set-up-general-inventory-information"></a>Så här ställer du in allmän lagerinformation

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerinställning** och väljer sedan relaterad länk.
2. På sidan **Lagerinställningar** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Detaljerad information om kostnadsfälten, **Automatisk kostnadsbokföring**, **Förväntad kost.bokf. i redov.** och **Standarvärderingsprincip** finns i [Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md) och [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md). Mer information om kostnadsredovisning i allmänhet finns i [Hantera lagerkostnad](finance-manage-inventory-costs.md).  

Om du vill ange en inkommande lagerhanteringstid som ska tas med i orderlöftesberäkningen på inköpsraden, kan du ange tiden som standard för lagret på sidan **Lagerinställning** och för lagerstället. Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Fältet **Automatisk kostnadsjustering** är inställt på *Alltid* som standard i syfte att säkerställa att lagervärden alltid är korrekta i redovisningen, vilket i sin tur innebär att försäljnings- och vinststatistik är aktuell. Kostnadsändringar från inkommande transaktioner, t. ex. de för inköp eller produktionsutflöde tilldelas relaterade utgående transaktioner, t. ex. försäljningar eller överföringar. Detta är användbart för nya [!INCLUDE[prod_short](includes/prod_short.md)]-kunder och mindre företag med relativt låga lagertransaktionsnivåer.
>
> När företaget växer och lagernivåerna ökar kan detta emellertid sakta ner systemets prestanda. Om du vill förhindra att prestandan vid bokföringen försämras väljer du ett tidsalternativ för att definiera hur långt tillbaka i tiden från arbetsdatumet som en inkommande transaktion kan inträffa för att eventuellt utlösa justeringar av relaterade utgående värdetransaktioner.
>
> Du kan också justera kostnader manuellt med jämna mellanrum med batch-jobbet Justera kost.-artikeltrans. Du kan också inaktivera automatisk kostnadsbokföring eller ange fältet **Automatisk kostnadsjustering** som *Aldrig*. I båda fallen visas ett meddelande där du kan starta en assisterad konfigurationsguide som hjälper dig att schemalägga aktiviteter för jobbkön. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se även

[Lagerinställning](inventory-setup-inventory.md)  
[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Hantera lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
