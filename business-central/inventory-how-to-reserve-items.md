---
title: Så här reserverar du artiklar
description: 'Lär dig hur du kan reservera artiklar för försäljningsorder, inköpsorder och produktionsorder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 02/22/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Reservera artiklar

Reservera artiklar för försäljningsorder, inköpsorder, serviceorder, monteringsorder, överföringsorder eller produktionsorder. Du kan reservera artiklar i lager eller inkommande på öppna dokument eller journalrader. Det gör du på sidan **reservation**.

Varje rad du öppnar för att reservera artiklar på sidan **Reservation** visar information om en viss typ av rad (försäljning, inköp, journal) eller lagerpost. Raderna beskriver hur många artiklar som är disponibla för reservation för varje radtyp eller post.

> [!TIP]
> Baserat på de kvantiteter du har reserverat i lager visar [!INCLUDE [prod_short](includes/prod_short.md)] en status för dokumenten, så att du snabbt kan få reda på nästa steg. Till exempel för att ange att du kan leverera en försäljningsorder eller börja arbeta med en projekt-, monterings- eller produktionsorder. Statusen bidrar också till att minska risken för oavsiktliga delleveranser eller förseningar på grund av att lager saknas för produktions- och monteringsorder.
>
> Fältet **Reserverat från lager** kan hjälpa dig att förstå om du kan leverera eller plocka för en viss order eller orderrad. För rader finns fältet Reserverat från lager i faktaboxar. Om du vill komma åt informationen för hela ordern finns fältet på sidan **Statistik**.

## Reservera artiklar för försäljning

Nedan beskrivs hur du reserverar artiklar från en försäljningsorder. Momentet är liknande för inköp, service, överföring och monteringsorder.
  
1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Välj försäljningsordern.
3. På snabbfliken **rader** i fältet **Reservera.** Sidan **Reservation** visas.  
4. Välj den rad som du vill reservera artiklarna från.  
5. Välj något av följande åtgärder:  

    |**Funktion**|**Beskrivning**|
    |------------------|---------------------|  
    |**Reservera auto.**|Om du vill reservera artiklar automatiskt på sidan **Reservation**.|  
    |**Reservera från aktuell rad**|För reservering av artiklar från den rad du har markerat i dokumentet.|  
    |**Avbeställ reservation från aktuell rad**|För att avbeställa reservation av artiklar från den rad du har markerat i dokumentet.|

> [!NOTE]  
> Om artikelspårningsrader finns för försäljningsordern används en särskild procedur. Mer information finns i avsnittet [Att reservera ett specifikt parti- eller serienummer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## Reservera artiklar för produktionsorderrader

Om du vill kan du reservera artiklar för produktionsorder. Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.

I det följande procedur används en fast planerad produktionsorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.  
2. Öppna den fast planerade produktionsorder som du vill reservera överordnade artiklar för.  
3. Markera relevant produktionsorderrad.  
4. På snabbfliken **rader** i fältet **Reservera.**
5. På sidan **Reservation** väljer du raden **Försäljningsrad, Order** och sedan åtgärden **Reservera från aktuell rad**.  

Det antal som du angett på raden för den fast planerade produktionsorden har nu reserverats.

## Reservera artiklar för produktionsorderkomponenter

Om du vill kan du reservera artiklar för produktionsorder. Tänk på att produktionsorderrader, den överordnade artikeln, inte är samma sak som produktionsorderkomponenter.

I det följande procedur används en fast planerad produktionsorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.  
2. Öppna den fast planerade produktionsorder som du vill reservera komponentartiklar för.  
3. Markera relevant produktionsorderrad.  
4. Välj **Rad**och sedan **Koppla trans.** på snabbfliken **Komponenter**.  
5. Välj relevant komponentrad.  
6. På snabbfliken **rader** i fältet **Reservera.**  
7. På sidan **Reservation** väljer du raden **Reservera från aktuell rad**.  

Det antal som du angett på raden för den fast planerade produktionskomponentraden har nu reserverats.

## Reservera artiklar i bulk

Använd sidan **Reservationsförslag** för att reservera och fördela inkommande varor i bulk. Massreservationer kan till exempel hjälpa dig att se till att kvantiteter är tillgängliga för försäljnings- och produktionsorder. Du kan ha flera journaler för olika syften. Du kan till exempel fördela produktionsorder veckovis, men reservera dagligen för försäljning.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Reservationförslag** och väljer sedan relaterad länk.  
2. Välj åtgärden **Hämta efterfrågan** och ange sedan vilken typ av behov du vill reservera från tillgängligt lager.
3. Fyll i filter efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
4. Valfritt: Om du vill fördela artiklarna direkt väljer du åtgärden **Fördela** .
5. På sidan **Fördelningsprincip** väljer du en policy för respektive steg.

   |Fördelningspolicy  |Description  |
   |---------|---------|
   |Grundläggande     | Allokerar lager till en efterfrågan om det inte finns några konflikter och efterfrågan kan täckas helt. Du har till exempel försäljningsorder A med antalet 10 och ett projekt med antalet 7. Om du har 20 i lager får båda kraven full kvantitet. Om ditt lager är 12 fördelas inget lager. Du måste fördela kvantiteten manuellt.        |
   |Lika    | Distribuerar tillgängligt lager till efterfrågan lika. Du har till exempel en försäljningsorder med antalet 10 och ett projekt med antalet 7. Om din lagernivå är 20 kommer båda kraven att få full kvantitet. Om ditt lager är 12 kommer båda kraven att få 6.        |
   |Efter kundprioritet|Distribution baserad på fältet **Prioritet** på sidan **Kundkort**. I händelse av låga lagerkvantiteter tillhandahåller Business Central kunder med högre prioritet först.|

6. Om du vill reservera alla rader där **Acceptera** är aktiverat väljer du åtgärden **Reservera**.
    
## Ändra reservation

Du kan ändra en artikelreservation.

1. Från dokumentraden som du gjorde reservationen från snabbfliken **rader** väljer du åtgärden **reservera**.  
2. På sidan **Reservation** väljer du åtgärden **Reservationstransaktioner**.
3. Sidan **Reservationstransaktioner** uppdaterar fältet **antal** på den rad som du vill ändra.
4. Bekräfta meddelandet som visas, genom att välja **OK**-knappen.

## Avbeställ en reservation

Du kan avbryta en artikelreservation.

1. Från dokumentraden som du vill avbryta en reservervation från på snabbfliken **rader** väljer du åtgärden **reservera**.  
2. På sidan **Reservation** väljer du åtgärden **Reservationstransaktioner**.  
3. På sidan **Reservation** väljer du åtgärden **Avbeställ reservation**.  
4. Bekräfta meddelandet som visas, genom att välja **Ja**-knappen.  

## Reservera ett visst serie- eller partinummer

Från utgående dokument för spårade artiklar t. ex. försäljningsorder eller produktionskomponentlistor kan du reservera specifika serie- eller partinummer. Det kan till exempel vara praktiskt att reservera specifika serie- eller partinummer i följande situationer:

* Om du behöver produktionskomponenter från ett visst parti för att säkerställa överensstämmelse med tidigare produktionsbatchar.
* Eftersom en kund har begärt ett visst serienummer. 

Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).

Detta kallas för en specifik reservation, eftersom du reserverar från antalet av artikeln X som tillhör parti X. Om du enbart reserverar från antal av artikeln X, är det en helt vanlig, icke-specifik reservation. Läs mer i [Designdetaljer – Artikelspårning och reservationer](design-details-item-tracking-and-reservations.md).

Följande procedur är baserad på en försäljningsorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Skapa försäljningsorderrader för en artikelspårad artikel.  
3. Fortsätt med att tilldela serie- och partinummer på försäljningsorderraden. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).
4. På försäljningsorderraden väljer du åtgärden **Reservera**.  
5. Välj knappen **Ja** för att reservera specifika serie- eller partinummer.  
6. På sidan **Artikelspårningslista**, välj serie- och partinummerkombinationen som du har tilldelats.  
7. Välj knappen **OK** för att öppna sidan **Reservation** där endast lager med det angivna artikelspårningsnumret visas. Om det finns icke-specifika reservationer för något av artikelspårningsnumren som har angetts på den här raden, informeras du om den kvantitet som redan har reserverats.  
8. Välj antingen **Reservera auto** eller åtgärden **Reservera från aktuell rad** för att skapa reservationen med de specifika artikelspårningsnumren.

## Se även

[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
