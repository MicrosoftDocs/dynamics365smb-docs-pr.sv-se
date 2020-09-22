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
ms.date: 07/16/2020
ms.author: edupont
ms.openlocfilehash: 092b76b7b25958b0df7155c335d7567c2b92fbf9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783180"
---
# <a name="date-calculation-for-purchases"></a>Datumberäkning för inköp

I [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknas automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum. Det är detta datum då du kan förvänta dig att artiklar som beställts ett visst datum ska vara tillgängliga för plockning.  

Om du anger ett begärt inleveransdatum i en inköpsorderhuvud, är det beräknade orderdatumet det datum då ordern måste placeras för inleverans av artiklarna på datumet som du valde. Då beräknas datumet då artiklarna är tillgängliga för plockning och visas i fältet **Förväntat inleveransdatum**.  

Om inget begärt inleveransdatum anges används orderdatumet på raden som utgångspunkt när programmet beräknar det datum då du kan förvänta dig att ta emot artiklarna och det datum då artiklarna kommer att vara tillgängliga för plockning.  

## <a name="calculating-with-a-requested-receipt-date"></a>Beräkna med ett begärt inleveransdatum

Om ett begärt inleveransdatum angetts på inköpsorderraden används detta datum som utgångspunkt i följande beräkningar:  

- begärt inleveransdatum – ledtidsberäkning = orderdatum  
- begärt inleveransdatum + ankommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum  

Om du angett ett begärt inleveransdatum i inköpsorderhuvudet kopieras detta datum till motsvarande fält på alla raderna. Du kan ändra datumet på raderna eller ta bort datumet på raden.  

> [!NOTE]
> Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda inleveransdatumet för att hämta planerat orderdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D", i fem dagar eller "1V" i en vecka. Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar. Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Beräkna utan ett begärt leveransdatum

Om du skriver in en inköpsorderrad utan ett begärt leveransdatum fylls fältet **Orderdatum** i automatiskt med datumet i fältet **Orderdatum** i inköpshuvudet. Detta datum är antingen det datum du angett eller arbetsdatumet. Därefter utförs följande datumberäkningar för inköpsorderraden, med utgångspunkt från orderdatumet:  

- orderdatum + ledtidsberäkning = planerat inleveransdatum.  
- planerat inleveransdatum + ankommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum  

Om du ändrar orderdatumet på raden, t.ex. om artiklarna inte är tillgängliga hos leverantören förrän vid ett senare datum, beräknas de aktuella datumen automatiskt om på raden.  

Om du ändrar orderdatumet i huvudet kopieras detta datum till fältet **Orderdatum** på samtliga rader, varefter alla relaterade datumfält beräknas om.  

## <a name="default-values-for-lead-time-calculation"></a>Standardvärden för ledtidsberäkning

[!INCLUDE[d365fin](includes/d365fin_md.md)] använder värdet från fältet **Ledtidsberäknin** på inköpsorderraden för att beräkna ordern och förväntade inleveransdatum.  

Du kan ange värdet på raden manuellt eller låta programmet använda värden som har definierats på leverantörskortet, artikekortet, lagerställets enhetkort eller i artikelleverantörens katalog.
Ledtidsvärdet på leverantörskortet används dock endast om ingen ledtid har angetts på artikelkortet, lagerställets enhetkort eller i artikelleverantörens katalog för artikeln. Detta är också den eskalerade prioritetsordningen för dessa värden. Om alla anges har ledtiden från leverantörskortet lägst prioritet och ledtiden från artikelleverantörens katalog högst prioritet.  

## <a name="see-also"></a>Se även

[Datumberäkning för försäljning](sales-date-calculation-for-sales.md)   
[Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
