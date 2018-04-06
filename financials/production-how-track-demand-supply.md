---
title: "Hur du spårar relationer mellan tillgång och efterfrågan | Microsoft Docs"
description: "Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8c53878418592daf9179d6864da4447ca8ad1262
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="track-relations-between-demand-and-supply"></a>Spåra relationer mellan tillgång och efterfrågan
Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.

Planeringsförslaget omfattar också stödinformation för planeringen, till exempel enheter som inte finns på order som hjälper planeraren att ta fram en optimal leveransplan. Mer information finns i avsnittet Planeringselement, inte spårat.

## <a name="to-track-linked-items"></a>Så här spårar du länkade artiklar
Orderspårningen visar hur försäljningsorder, produktionsorder och inköpsorder är relaterade till produktionsordern genom planerings- och reservationssystem.

Nedan beskrivs hur du spårar länkade artiklar på en fast planerad produktionsorder. Momentet är liknande för alla andra ordertyper och från planeringsförslagsraderna.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.
2. Öppna relevant fast planerad produktionsorder i listan.
3. På snabbfliken **Rader** väljer du åtgärden **Funktioner** och sedan åtgärden **Orderspårning**.

På raderna i fönstret **Orderspårning** visas de dokument som är relaterade till den aktuella produktionsorderraden.

## <a name="untracked-planning-elements"></a>Ej spårade planeringselement
Fönstret **Ej spårade planeringselement** öppnas när du väljer fönstret **ej spårat antal** i fönstret **orderplanering**. Den har två syften:

1. Den innehåller information om ej spårade kvantiteter, som visas när användaren vill se ej spårade kvantiteter från fönstret Orderspårning .
2. Den innehåller varningsmeddelanden som visas när användaren klickar på en **varningsikon** i fönstret **planeringsförslag**.

Fönstret innehåller poster som redogör för en överskottskvantitet i orderspårningsnätverket. Dessa poster skapas under planeringen och förklarar var den ej spårade överskottskvantiteten på orderspårningsraderna kommer ifrån. Överskottet som inte har spårats kan komma från:

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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

