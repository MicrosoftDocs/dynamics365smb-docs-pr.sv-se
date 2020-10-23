---
title: Så här reserverar du artiklar | Microsoft Docs
description: Du kan reservera artiklar för försäljningsorder, inköpsorder och produktionsorder. Du kan reservera artiklar i lager eller ankommande på öppna dokumentrader.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cd2ff853ba4e98115988b318663714ef4a842719
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919420"
---
# <a name="reserve-items"></a>Reservera artiklar
Reservera artiklar för försäljningsorder, inköpsorder, serviceorder, monteringsorder eller produktionsorder. Du kan reservera artiklar i lager eller ankommande på öppna dokument eller journalrader. Du utför arbetet på sidan **Reservation**.

Varje rad på sidan **Reservation** som du öppnar för att reservera artiklar visar information om en viss typ av rad (försäljning, inköp, journal) eller lagerpost. Raderna beskriver hur många artiklar som är disponibla för reservation för varje radtyp eller post.

## <a name="to-reserve-items-for-sales"></a>Så här reserverar du artiklar för försäljning
Nedan beskrivs hur du reserverar artiklar från en försäljningsorder. Momentet är liknande för inköp, service och monteringsorder.  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  På en föräljningsorder, på snabbfliken **Rader** väljer du åtgärden **Reservera**. Sidan **Reservation** visas.  
3. Välj den rad som du vill reservera artiklarna från.  
4. Välj något av följande åtgärder:  

    |**Funktion**|**Beskrivning**|
    |------------------|---------------------|  
    |**Reservera auto.**|Om du vill reservera artiklar automatiskt på sidan **Reservation**.|  
    |**Reservera från aktuell rad**|För reservering av artiklar från den rad du har markerat i dokumentet.|  
    |**Avbeställ reservation från aktuell rad**|För att avbeställa reservation av artiklar från den rad du har markerat i dokumentet.|

> [!NOTE]  
>  Om artikelspårningsrader finns för försäljningsordern används en särskild procedur. Mer information finns i avsnittet [Att reservera ett specifikt parti- eller serienummer](inventory-how-to-reserve-items.md#to-reserve-a-specific-serial-or-lot-number).  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Så här reserverar du artiklar för produktionsorderrader  
Om du vill kan du reservera artiklar för produktionsorder. Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.

I det följande procedur används en fast planerad produktionsorder.   
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.  
2. Öppna den fast planerade produktionsorder som du vill reservera överordnade artiklar för.  
3. Markera relevant produktionsorderrad.  
4. På snabbfliken **rader** i fältet **Reservera.**
5. På sidan **Reservation** väljer du raden **Försäljningsrad, Order** och sedan åtgärden **Reservera från aktuell rad**.  

Det antal som du angett på raden för den fast planerade produktionsorden har nu reserverats.

## <a name="to-reserve-items-for-production-order-components"></a>Så här reserverar du artiklar för produktionsorderkomponenter  
Om du vill kan du reservera artiklar för produktionsorder. Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.

I det följande procedur används en fast planerad produktionsorder.    
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.  
2. Öppna den fast planerade produktionsorder som du vill reservera komponentartiklar för.  
3. Markera relevant produktionsorderrad.  
4. Välj **Rad**och sedan **Koppla trans.** på snabbfliken **Komponenter**.  
5. Välj relevant komponentrad.  
6. På snabbfliken **rader** i fältet **Reservera.**  
7. På sidan **Reservation** väljer du raden **Reservera från aktuell rad**.  

Det antal som du angett på raden för den fast planerade produktionskomponentraden har nu reserverats.

## <a name="to-change-a-reservation"></a>Så här ändrar du en reservation  
Någon gång kan du behöva ändra en artikelreservation.   
1. Från dokumentraden som du har reserverats från snabbfliken **rader** väljer du åtgärden **reservera**.  
2. På sidan **Reservation** väljer du åtgärden **Reservationstransaktioner**.
3. Sidan **Reservationstransaktioner** uppdaterar fältet **antal** på den rad som du vill ändra.
4. Bekräfta meddelandet som visas, genom att välja **OK**-knappen.

## <a name="to-cancel-a-reservation"></a>Så här avbeställer du en reservation  
Någon gång kan du behöva avbeställa en artikelreservation.   
1. Från dokumentraden som du vill avbryta en reservervation från på snabbfliken **rader** väljer du åtgärden **reservera**.  
2. På sidan **Reservation** väljer du åtgärden **Reservationstransaktioner**.  
3.  På sidan **Reservation** väljer du åtgärden **Avbeställ reservation**.  
4.  Bekräfta meddelandet som visas, genom att välja **OK**-knappen.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Om du vill reservera ett visst serie- eller partinummer  
Från utgående dokument för spårade artiklar t.ex. försäljningsorder eller produktionskomponentlistor kan du reservera specifika serie- eller partinummer. Detta kan vara användbart till exempel om du behöver produktionskomponenter från ett visst parti för att kontrollera överensstämmelse med tidigare produktionsbatcher eller därför att en kund har begärt ett specifikt serienummer. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).

Detta kallas för en specifik reservation, eftersom du reserverar från antalet av artikeln X som tillhör parti X. Om du enbart reserverar från antal av artikeln X, är det en helt vanlig, icke-specifik reservation. Mer information finns i  [Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md).

Följande procedur är baserad på en försäljningsorder.    
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Skapa försäljningsorderrader för en artikelspårad artikel.  
3. Fortsätt med att tilldela serie- och partinummer på försäljningsorderraden. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).
4. På försäljningsorderraden väljer du åtgärden **Reservera**.  
5. Välj knappen **Ja** för att reservera specifika serie- eller partinummer.  
6. På sidan **Artikelspårningslista**, välj serie- och partinummerkombinationen som du precis har tilldelats.  
7. Välj knappen **OK** för att öppna sidan **Reservation** där endast lager med det angivna artikelspårningsnumret visas. Om det finns icke-specifika reservationer för något av artikelspårningsnumren som har angetts på den här raden, informeras du om den kvantitet som redan har reserverats.  
8. Välj antingen **Reservera auto** eller åtgärden **Reservera från aktuell rad** för att skapa reservationen med de specifika artikelspårningsnumren.

## <a name="see-also"></a>Se även
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
