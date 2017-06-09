---
title: "Så här justerar du kostnader manuellt | Microsoft Docs"
description: "Så här justerar du artikelkostnader"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Så här justerar du artikelkostnader manuellt
Kostnaden för en artikel (lagervärde) som du köper och senare säljer kan ändras under dess livstid, eftersom till exempel en fraktkostnad läggs till dess inköpkostnad när du har sålt artikeln. Kostnadsjustering är speciellt relevant i situationer där du säljer varor, innan du fakturerar inköpet av dessa varor. För att alltid ha rätt lagervärde måste artikelkostnader därför regelbundet justeras. Detta säkerställer att försäljnings- och vinststatistiken är aktuell och ekonomiska KPI-er är korrekta.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] justera artikelkostnaderna automatiskt varje gång en lagertransaktion uppstår till exempel när bokföring av en faktura för en artikel.

Du kan också använda en funktion för att justera kostnaderna för en eller flera artiklar. Detta är användbart när du vet att artikelkostnader har ändrats av andra orsaker än artikeltransaktioner.

**Obs**! Artikelkostnader justeras endast av FIFO-principen. Det betyder att en artikels styckkostnad är det faktiska värdet av alla inleveranser av artikeln och att lagret värderas med antagandet om att de första artiklarna som finns i lager säljs först.

Funktionen Kostnadsjustering bearbetar endast värdetransaktioner som inte ännu har justerats. Om en funktion påträffas där ankommande kostnader behöver flyttas fram till kopplade avgående kostnader, görs detta genom att nya justeringsvärdetransaktioner skapas som baseras på informationen i de ursprungliga värdetransaktionerna, men som innehåller justeringsbeloppet. Funktionen Kostnadsjustering använder bokföringsdatumet för den ursprungliga värdetransaktionen om inte det datumet infaller i en avslutad lagerperiod. Om så är fallet används startdatumet för nästa öppna lagerperiod. Om lagerperioder inte används definieras datumet i fältet **Tillåt bokföring fr.o.m.** i fönstret **Redovisningsinställningar** när justeringstransaktionerna bokförs.

Ändringar av lagervärdet från handel kopplas automatiskt till din finansiella anläggningstillgångar när du bokför artikeltransaktioner. Mer information finns i [Avancerat: Lageravstämning](advanced-inventory-reconciliation.md).

## <a name="to-adjust-item-costs-manually"></a>Så här justerar du artikelkostnader manuellt
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Justera kost. - artikeltrans** och väljer sedan relaterad länk.
2. I fönstret **Justera kost. - artikeltrans** kan du ange vilka artiklar som du vill justera kostnader för.
3. Välj **OK**.

## <a name="see-also"></a>Se även
[Avancerad: Lageravstämning](advanced-inventory-reconciliation.md)  
[Lager](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

