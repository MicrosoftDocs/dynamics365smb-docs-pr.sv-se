---
title: Hur du spårar relationer mellan tillgång och efterfrågan | Microsoft Docs
description: Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ba774a7f7ba93c132e10e19f61b7df9cf825e7a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383231"
---
# <a name="track-relations-between-demand-and-supply"></a>Spåra relationer mellan tillgång och efterfrågan
Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.

Planeringsförslaget omfattar också stödinformation för planeringen, till exempel enheter som inte finns på order som hjälper planeraren att ta fram en optimal leveransplan. Mer information finns i [Planeringselement, inte spårat](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Så här spårar du länkade artiklar
Orderspårningen visar hur försäljningsorder, produktionsorder och inköpsorder är relaterade till produktionsordern genom planerings- och reservationssystem.

Nedan beskrivs hur du spårar länkade artiklar på en fast planerad produktionsorder. Momentet är liknande för alla andra ordertyper och från planeringsförslagsraderna.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.
2. Öppna relevant fast planerad produktionsorder i listan.
3. På snabbfliken **Rader** väljer du åtgärden **Funktioner** och sedan åtgärden **Orderspårning**.

På raderna i fönstret **Orderspårning** visas de dokument som är relaterade till den aktuella produktionsorderraden.

## <a name="untracked-planning-elements"></a>Ej spårade planeringselement
Sidan **Ej spårade planeringselement** öppnas när du väljer sidan **ej spårat antal** på sidan **orderplanering**. Den har två syften:

1. Den innehåller information om ej spårade kvantiteter, som visas när användaren vill se ej spårade kvantiteter från sidan Orderspårning .
2. Den innehåller varningsmeddelanden som visas när användaren klickar på en **varningsikon** på sidan **planeringsförslag**.

Sidan innehåller poster som redogör för en överskottskvantitet i orderspårningsnätverket. Dessa poster skapas under planeringen och förklarar var den ej spårade överskottskvantiteten på orderspårningsraderna kommer ifrån. Överskottet som inte har spårats kan komma från:

- Produktionsprognos
- Avropsorder
- Säkerhetslager
- Beställningspunkt
- Beställningsgräns
- Beställningsantal
- Max. partistorlek
- Min. partistorlek
- Partistorleksmultipel
- Dämpare (% partistorlek)

## <a name="see-also"></a>Se även  
[Planerad](production-planning.md)   
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Reservation, spårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]