---
title: Datum för beräkning av inköp | Microsoft Docs
description: Programmet beräknar automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum. Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22153df1e56d274256b53d426e2dff30cad3e4bc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758598"
---
# <a name="date-calculation-for-purchases"></a>Datumberäkning för inköp

I [!INCLUDE[prod_short](includes/prod_short.md)] beräknas automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum. Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.  

Om du anger ett begärt inleveransdatum i en inköpsorderhuvud, är det beräknade orderdatumet det datum då ordern måste placeras för inleverans av artiklarna på datumet som du valde. Då beräknas datumet då artiklarna är tillgängliga för plockning och visas i fältet **Förväntat inleveransdatum**.  

Om inget begärt inleveransdatum anges används orderdatumet på raden som utgångspunkt när programmet beräknar det datum då du kan förvänta dig att ta emot artiklarna och det datum då artiklarna kommer att vara tillgängliga för plockning.  

## <a name="calculating-with-a-requested-receipt-date"></a>Beräkna med ett begärt inleveransdatum

Om ett begärt inleveransdatum angetts på inköpsorderraden används detta datum som utgångspunkt i följande beräkningar:  

- begärt inleveransdatum – ledtidsberäkning = orderdatum  
- begärt inleveransdatum + inkommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum  

Om du angett ett begärt inleveransdatum i inköpsorderhuvudet kopieras detta datum till motsvarande fält på alla raderna. Du kan ändra datumet på raderna eller ta bort datumet på raden.  

> [!NOTE]
> Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda inleveransdatumet för att hämta planerat orderdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D", i fem dagar eller "1V" i en vecka. Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar. Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Beräkna utan ett begärt leveransdatum

Om du skriver in en inköpsorderrad utan ett begärt leveransdatum fylls fältet **Orderdatum** i automatiskt med datumet i fältet **Orderdatum** i inköpshuvudet. Detta datum är antingen det datum du angett eller arbetsdatumet. Därefter utförs följande datumberäkningar för inköpsorderraden, med utgångspunkt från orderdatumet:  

- orderdatum + ledtidsberäkning = planerat inleveransdatum.  
- planerat inleveransdatum + inkommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum  

Om du ändrar orderdatumet på raden, t.ex. om artiklarna inte är tillgängliga hos leverantören förrän vid ett senare datum, beräknas de aktuella datumen automatiskt om på raden.  

Om du ändrar orderdatumet i huvudet kopieras detta datum till fältet **Orderdatum** på samtliga rader, varefter alla relaterade datumfält beräknas om.  

## <a name="default-values-for-lead-time-calculation"></a>Standardvärden för ledtidsberäkning

[!INCLUDE[prod_short](includes/prod_short.md)] använder värdet från fältet **Ledtidsberäknin** på inköpsorderraden för att beräkna ordern och förväntade inleveransdatum.  

Du kan ange värdet på raden manuellt eller låta programmet använda värden som har definierats på leverantörskortet, artikekortet, lagerställets enhetkort eller i artikelleverantörens katalog.
Ledtidsvärdet på leverantörskortet används dock endast om ingen ledtid har angetts på artikelkortet, lagerställets enhetkort eller i artikelleverantörens katalog för artikeln. Detta är också den eskalerade prioritetsordningen för dessa värden. Om alla anges har ledtiden från leverantörskortet lägst prioritet och ledtiden från artikelleverantörens katalog högst prioritet.  

## <a name="see-also"></a>Se även

[Datumberäkning för försäljning](sales-date-calculation-for-sales.md)   
[Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]