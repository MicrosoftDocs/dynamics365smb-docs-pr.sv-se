---
title: Uppdatera valutakurser | Microsoft Docs
description: "För att använda flera valutor i din verksamhet, kan du lägga upp en kod för varje valuta och använda en extern valutakurstjänst."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: sv-se
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a>Uppdatera valutakurser
Eftersom företag verkar i allt fler länder/regioner blir det alltmer viktigt att de kan använda och rapportera ekonomiska siffror i fler än en valuta. Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.

Din redovisning ställs in för att använda den lokala valutan (BVA) men du kan ställa in en annan valuta med en tilldelad aktuell valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion och för andra transaktioner, t.ex. momstransaktioner. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Justera valutakurser
Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats. Batch-jobbet Justera valutakurser används för att justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutor** och välj sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** på sidan **valutor** uppdateras med den senaste valutakursen.

## <a name="see-also"></a>Se även
[Ställa in en alternativ rapporteringsvaluta.](finance-how-setup-additional-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

