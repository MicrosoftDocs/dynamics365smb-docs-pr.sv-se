---
title: Beräkning av leveransdatum för försäljning
description: Programmet beräknar automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum och tillgänglig för plockning.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Beräkning av leveransdatum för försäljning

I [!INCLUDE[prod_short](includes/prod_short.md)] beräknas automatiskt tidigast möjliga leveransdatum för en artikel på en försäljningsorderrad.

* Om kunden har begärt ett särskilt leveransdatum beräknas det datum då artiklarna måste vara tillgängliga för plockning så att varorna faktiskt ska kunna levereras på angiven dag.
* Om kunden inte begär ett särskilt leveransdatum beräknas det datum då artiklarna kan levereras. Beräkningen börjar från det datum då artiklarna är tillgängliga för plockning.

## Beräkna ett begärt leveransdatum

Om du anger ett begärt leveransdatum på försäljningsorderraden blir detta datum utgångspunkt för följande beräkningar.

- *begärt leveransdatum – leveranstid = planerat utleveransdatum*
- *planerat utleveransdatum – utgående lagerhanteringstid = utleveransdatum*

Om artiklarna kan plockas på utleveransdatumet kan försäljningsprocessen fortsätta. Annars visas en varning om slut på lager.

> [!NOTE]
> Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda leveransdatumet för att hämta planerat leveransdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D" för fem dagar eller "1V" för en vecka. Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar. Mer information om datumformler finns i [Arbeta med datum och tider för kalender](ui-enter-date-ranges.md).

## Beräkna tidigaste möjliga leveransdatum

Om du inte har angett ett begärt leveransdatum på försäljningsorderraden, eller om det begärda leveransdatumet inte kan godtas, beräknas det tidigaste datum då artiklarna är tillgängliga. Detta datum anges automatiskt i fältet **Leveransdatum** på raden. Det datum då du planerar att utleverera artiklarna liksom det datum då varorna kan levereras till kunden beräknas med hjälp av följande formler.

- *utleveransdatum + utgående lagerhanteringstid = planerat utleveransdatum*
- *planerat utleveransdatum + leveranstid = planerat leveransdatum*

## Se även

[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)  
[Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
