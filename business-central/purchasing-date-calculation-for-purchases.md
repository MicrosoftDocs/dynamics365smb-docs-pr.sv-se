---
title: Beräkning för inköp
description: I den här artikeln beskrivs hur du beräknar datum för inköp.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# <a name="calculate-dates-for-purchases" />Beräkning för inköp

Om du vill ha varor i lager ett visst datum, [!INCLUDE[prod_short](includes/prod_short.md)] kan automatiskt räkna ut vilket datum du måste beställa dem. 

Resultatet är det datum då du kan plocka de artiklar som du har beställt.  

Om du anger ett begärt inleveransdatum på en inköpsorderrad är det beräknade orderdatumet det datum då du måste placera ordern. Datumet då föremålen kommer att vara tillgängliga för plockning visas i **Förväntat inleveransdatum**.  

Om du inte anger ett begärt inleveransdatum kommer datumet som du förväntar dig att erhålla artiklarna att baseras på orderdatumet på raden. 

Inleveransdatum är också det datum då artiklarna kommer att vara tillgängliga för plockning.  

> [!TIP]
> Som standard är många av de datum fält som nämns i den här artikeln dolda på inköpsorderrader. Om ett fält inte är tillgängligt kan du lägga till det genom att anpassa sidan. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date" />Beräkna med ett begärt inleveransdatum

Om ett begärt inleveransdatum angetts på inköpsorderraden som detta datum ligger till grund för följande beräkningar:  

- begärt inleveransdatum – ledtidsberäkning = orderdatum  
- begärt inleveransdatum + inkommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum  

Om du anger ett begärt inleveransdatum på en inköpsorderrad tilldelas det datumet till nya rader när du skapar dem. Du kan ändra eller ta bort datumet på raderna.  

> [!NOTE]
> Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda inleveransdatumet för att hämta planerat orderdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D", i fem dagar eller "1V" i en vecka. Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar. Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date" />Beräkna utan ett begärt inleveransdatum

Om du skriver in en inköpsorderrad utan ett begärt inleveransdatum fylls fältet **Orderdatum** i automatiskt med datumet i fältet **Orderdatum** i inköpshuvudet. Detta datum är antingen det datum du angett eller arbetsdatumet. Därefter utförs följande datumberäkningar för inköpsorderraden, med utgångspunkt från orderdatumet:  

- orderdatum + ledtidsberäkning = planerat inleveransdatum.  
- planerat inleveransdatum + inkommande lagerhanteringstid + säkerhetsledtid = förväntat inleveransdatum  

Om du ändrar order datumet på raden [!INCLUDE[prod_short](includes/prod_short.md)] räknas de andra datumen om.  

## <a name="default-values-for-lead-time-calculation" />Standardvärden för ledtidsberäkning

[!INCLUDE[prod_short](includes/prod_short.md)] använder datumformel från fältet **Ledtidsberäkning** på inköpsorderraden för att beräkna ordern och förväntade inleveransdatum.  

Du kan ange datum formeln på raderna manuellt. I annat fall [!INCLUDE[prod_short](includes/prod_short.md)] används formlerna som definieras på följande sidor i den här prioritetsordningen:

1. Artikelns leverantörskatalog
2. Artikelkort
3. Lagerställeenhetskort
4. Leverantörskort

## <a name="see-related-microsoft-trainingtrainingmodulesestimate-receipt-dates-dynamics-365-business-central" />Se relaterad [Microsoft utbildning](/training/modules/estimate-receipt-dates-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Datumberäkning för försäljning](sales-date-calculation-for-sales.md)  
[Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
