---
title: "Så här reserverar du artiklar | Microsoft Docs"
description: "Du kan reservera artiklar för försäljningsorder, inköpsorder och produktionsorder. Du kan reservera artiklar i lager eller ankommande på öppna dokumentrader."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b03209b5681c264f7d788d3d731d32b60f1709b6
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reserve-items"></a>Så här reserverar du artiklar
Reservera artiklar för försäljningsorder, inköpsorder, serviceorder, monteringsorder eller produktionsorder. Du kan reservera artiklar i lager eller ankommande på öppna dokument eller journalrader. Du utför arbetet i fönstret **Reservation**.

Varje rad i fönstret **Reservation** som du öppnar för att reservera artiklar visar information om en viss typ av rad (försäljning, inköp, journal) eller lagerpost. Raderna beskriver hur många artiklar som är disponibla för reservation för varje radtyp eller post.

## <a name="to-reserve-items-for-sales"></a>Så här reserverar du artiklar för försäljning
Nedan beskrivs hur du reserverar artiklar från en försäljningsorder. Momentet är liknande för inköp, service och monteringsorder.  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  På en föräljningsorder, på snabbfliken **Rader** väljer du åtgärden **Reservera**. Fönstret **Reservation** öppnas.  
3. Välj den rad som du vill reservera artiklarna från.  
4. Välj något av följande åtgärder:  

    |**Funktion**|**Beskrivning**|
    |------------------|---------------------|  
    |**Reservera auto.**|Om du vill reservera artiklar automatiskt i fönstret **Reservation**.|  
    |**Reservera från aktuell rad**|För reservering av artiklar från den rad du har markerat i dokumentet.|  
    |**Avbeställ reservation från aktuell rad**|För att avbeställa reservation av artiklar från den rad du har markerat i dokumentet.|

> [!NOTE]  
>  Om artikelspårningsrader finns för försäljningsordern används en särskild procedur. Mer information finns i avsnittet "Att reservera ett specifikt parti- eller serienummer".  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Så här reserverar du artiklar för produktionsorderrader  
Om du vill kan du reservera artiklar för produktionsorder. Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.

I det följande procedur används en fast planerad produktionsorder.   
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.  
2. Öppna den fast planerade produktionsorder som du vill reservera överordnade artiklar för.  
3. Markera relevant produktionsorderrad.  
4. På snabbfliken **rader** i fältet **Reservera.**
5. I fönstret **Reservation** väljer du raden **Försäljningsrad, Order** och sedan åtgärden **Reservera från aktuell rad**.  

Det antal som du angett på raden för den fast planerade produktionsorden har nu reserverats.

## <a name="to-reserve-items-for-production-order-components"></a>Så här reserverar du artiklar för produktionsorderkomponenter  
Om du vill kan du reservera artiklar för produktionsorder. Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.

I det följande procedur används en fast planerad produktionsorder.    
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Fast planerad prod.order** och välj sedan relaterad länk.  
2. Öppna den fast planerade produktionsorder som du vill reservera komponentartiklar för.  
3. Markera relevant produktionsorderrad.  
4. Välj **Rad**och sedan **Koppla trans.** på snabbfliken **Komponenter**.  
5. Välj relevant komponentrad.  
6. På snabbfliken **rader** i fältet **Reservera.**  
7. I fönstret **Reservation** väljer du raden **Reservera från aktuell rad**.  

Det antal som du angett på raden för den fast planerade produktionskomponentraden har nu reserverats.

## <a name="to-change-a-reservation"></a>Så här ändrar du en reservation  
Någon gång kan du behöva ändra en artikelreservation.   
1. Från dokumentraden som du har reserverats från snabbfliken **rader** väljer du åtgärden **reservera**.  
2. I fönstret **Reservation** väljer du åtgärden **Reservationstransaktioner**.
3. Fönstret **Reservationstransaktioner** uppdaterar fältet **antal** på den rad som du vill ändra.
4. Bekräfta meddelandet som visas, genom att välja **OK**-knappen.

## <a name="to-cancel-a-reservation"></a>Så här avbeställer du en reservation  
Någon gång kan du behöva avbeställa en artikelreservation.   
1. Från dokumentraden som du vill avbryta en reservervation från på snabbfliken **rader** väljer du åtgärden **reservera**.  
2. I fönstret **Reservation** väljer du åtgärden **Reservationstransaktioner**.  
3.  I fönstret **Reservationstransaktioner** väljer du åtgärden **Avbryt reservation**.  
4.  Bekräfta meddelandet som visas, genom att välja **OK**-knappen.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Om du vill reservera ett visst serie- eller partinummer  
Från utgående dokument för spårade artiklar t.ex. försäljningsorder eller produktionskomponentlistor kan du reservera specifika serie- eller partinummer. Detta kan vara användbart till exempel om du behöver produktionskomponenter från ett visst parti för att kontrollera överensstämmelse med tidigare produktionsbatcher eller därför att en kund har begärt ett specifikt serienummer. Mer information finns i [Så här arbetar du med serienummer och partinummer](inventory-how-work-item-tracking.md).

Detta kallas för en specifik reservation, eftersom du reserverar från antalet av artikeln X som tillhör parti X. Om du enbart reserverar från antal av artikeln X, är det en helt vanlig, icke-specifik reservation. Mer information finns i  [Designdetaljer: Artikelspårning och reservationer](design-details-item-tracking-and-reservations.md).

Följande procedur är baserad på en försäljningsorder.    
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Skapa försäljningsorderrader för en artikelspårad artikel.  
3. Fortsätt med att tilldela serie- och partinummer på försäljningsorderraden. Mer information finns i [Så här arbetar du med serienummer och partinummer](inventory-how-work-item-tracking.md).
4. På försäljningsorderraden väljer du åtgärden **Reservera**.  
5. Välj knappen **Ja** för att reservera specifika serie- eller partinummer.  
6. I fönstret **Artikelspårningslista**, välj serie- och partinummerkombinationen som du precis har tilldelats.  
7. Välj knappen **OK** för att öppna fönstret **Reservation** där endast lager med det angivna artikelspårningsnumret visas. Om det finns icke-specifika reservationer för något av artikelspårningsnumren som har angetts på den här raden, informeras du om den kvantitet som redan har reserverats.  
8. Välj antingen **Reservera auto** eller åtgärden **Reservera från aktuell rad** för att skapa reservationen med de specifika artikelspårningsnumren.

## <a name="see-also"></a>Se även
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Artikelspårning och reservationer](design-details-item-tracking-and-reservations.md)  
[Så här arbetar du med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

