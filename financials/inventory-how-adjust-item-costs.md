---
title: "Så här justerar du kostnader för artiklar manuellt | Microsoft Docs"
description: "Du kan justera lagervärderingen för en artikel som använder FIFO eller genomsnittliga värderingsprinciper, till exempel när artikelkostnader ändras av andra skäl än transaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Så här justerar du artikelkostnader manuellt
Kostnaden för en artikel (lagervärde) som du köper och senare säljer kan ändras under dess livstid, eftersom till exempel en fraktkostnad läggs till dess inköpkostnad när du har sålt artikeln. Kostnadsjustering är speciellt relevant i situationer där du säljer varor, innan du fakturerar inköpet av dessa varor. För att alltid ha rätt lagervärde måste artikelkostnader därför regelbundet justeras. Detta säkerställer att försäljnings- och vinststatistiken är aktuell och ekonomiska KPI-er är korrekta.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] justera artikelkostnaderna automatiskt varje gång en lagertransaktion uppstår till exempel när bokföring av en faktura för en artikel.

Du kan också använda en funktion för att justera kostnaderna för en eller flera artiklar. Detta är användbart när du vet att artikelkostnader har ändrats av andra orsaker än artikeltransaktioner.

Artikelkostnaderna justeras av FIFO eller metoden Genomsnittskostnad beroende på ditt val i assisterad konfiguration för **Konfigurera mitt företag**. Mer information finns i [Komma igång med att göra affärer ](ui-get-ready-business.md).  

Om du använder en FIFO-kostnadsmetod är artikelns enhetskostnad det verkliga värdet på en inleverans av artikeln. Lager värders genom att anta att de första artiklarna in i lagret säljs först.

Om du använder metoden Genomsnittskostnad beräknas en artikels enhetskostnad som den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp. Lager värderas med förutsättningen att alla lagerartiklar säljs samtidigt.

Funktionen Kostnadsjustering bearbetar endast värdetransaktioner som inte ännu har justerats. Om en funktion påträffas där ankommande kostnader behöver flyttas fram till kopplade avgående kostnader, görs detta genom att nya justeringsvärdetransaktioner skapas som baseras på informationen i de ursprungliga värdetransaktionerna, men som innehåller justeringsbeloppet. Funktionen Kostnadsjustering använder bokföringsdatumet för den ursprungliga värdetransaktionen om inte det datumet infaller i en avslutad lagerperiod. Om så är fallet används startdatumet för nästa öppna lagerperiod. Om lagerperioder inte används definieras datumet i fältet **Tillåt bokföring fr.o.m.** i fönstret **Redovisningsinställningar** när justeringstransaktionerna bokförs.

Ändringar av lagervärdet från handel kopplas automatiskt till din finansiella anläggningstillgångar när du bokför artikeltransaktioner. Mer information finns i avsnittet "Lageravstämning" i [Lager](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>Så här justerar du artikelkostnader manuellt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Justera kost. - artikeltrans** och välj sedan relaterad länk.
2. I fönstret **Justera kost. - artikeltrans** kan du ange vilka artiklar som du vill justera kostnader för.
3. Välj **OK**.

## <a name="see-also"></a>Se även
[Lagersaldo](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

