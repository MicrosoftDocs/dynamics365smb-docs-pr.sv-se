---
title: Datum för beräkning av försäljning | Microsoft Docs
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
ms.openlocfilehash: 26782d211d205bb5414c5bd423ccf240f70f197e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748474"
---
# <a name="date-calculation-for-sales"></a>Datumberäkning för försäljning
I [!INCLUDE[prod_short](includes/prod_short.md)] beräknas automatiskt tidigast möjliga leveransdatum för en artikel på en försäljningsorderrad.

Om kunden har begärt ett särskilt leveransdatum beräknas det datum då artiklarna måste vara tillgängliga för plockning så att varorna faktiskt ska kunna levereras på angiven dag.

Om inget bestämt leveransdatum begärts beräknas det datum då artiklarna kan levereras, med utgångspunkt från det datum då artiklarna är tillgängliga för plockning.

## <a name="calculating-a-requested-delivery-date"></a>Beräkna ett begärt leveransdatum
Om du anger ett begärt leveransdatum på försäljningsorderraden blir detta datum utgångspunkt för följande beräkningar.

- begärt leveransdatum – leveranstid = planerat utleveransdatum
- planerat utleveransdatum – utgående lagerhanteringstid = utleveransdatum

Om artiklarna kan plockas på utleveransdatumet kan försäljningsprocessen fortsätta. Annars visas en varning om slut på lager.

> [!Note]
> Om din process grundar sig på beräkning bakåt, till exempel om du använder det begärda leveransdatumet för att hämta planerat leveransdatum, rekommenderar vi att du använder datumformler med fast varaktighet, till exempel "5D", i fem dagar eller "1V" i en vecka. Datumformler utan fast varaktighet, till exempel "FV" för aktuell vecka eller CM för aktuell månad, kan resultera i felaktiga datumberäkningar. Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Beräkna tidigaste möjliga leveransdatum
Om du inte har angett ett begärt leveransdatum på försäljningsorderraden, eller om det begärda leveransdatumet inte kan godtas, beräknas det tidigaste datum då artiklarna är tillgängliga. Detta datum anges automatiskt i fältet Leveransdatum på raden. Det datum då du planerar att utleverera artiklarna liksom det datum då varorna kan levereras till kunden beräknas med hjälp av följande formler.

- planerat utleveransdatum + utgående lagerhanteringstid = planerat utleveransdatum
- planerat utleveransdatum +- leveranstid = planerat leveransdatum


## <a name="see-also"></a>Se även  
 [Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)   
 [Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]