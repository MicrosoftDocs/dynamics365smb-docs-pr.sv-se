---
title: Spåra relationer mellan tillgång och efterfrågan
description: 'I det här avsnittet beskrivs olika sätt att följa upp samband mellan efter frågan och till gång, t.ex. spårning av länkade objekt och hantering av schemaelement som inte har spårats.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5830, 9101, 99000822, 99000855'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="track-relations-between-demand-and-supply"></a>Spåra relationer mellan tillgång och efterfrågan

Du kan spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden från alla försörjnings- eller behovsdokument i det så kallade ordernätverker.

Planeringsförslaget omfattar också stödinformation för planeringen, till exempel enheter som inte finns på order som hjälper planeraren att ta fram en optimal leveransplan. Mer information finns i [Planeringselement, inte spårat](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Så här spårar du länkade artiklar
Orderspårningen visar hur försäljningsorder, produktionsorder och inköpsorder är relaterade till produktionsordern genom planerings- och reservationssystem.

Nedan beskrivs hur du spårar länkade artiklar på en fast planerad produktionsorder. Momentet är liknande för alla andra ordertyper och från planeringsförslagsraderna.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.
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
