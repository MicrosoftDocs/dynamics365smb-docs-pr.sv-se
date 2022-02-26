---
title: Datumberäkning för försäljning
description: Programmet beräknar automatiskt det datum då du måste beställa en artikel som du vill ha i lager på ett visst datum och tillgänglig för plockning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 221580cebab85be781cd56d461e9d75bb321c15b
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6320212"
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