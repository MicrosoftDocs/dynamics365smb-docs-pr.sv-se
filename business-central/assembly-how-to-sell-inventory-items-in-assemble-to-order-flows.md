---
title: "Så här säljer du lagerartiklar i flöde för montering mot kundorder | Microsoft Docs"
description: "Om artikeln är inställd för kort med montering mot kundorder förutsätter standardprocessen för försäljningsorder att artikeln inte finns på lager och måste monteras för den specifika försäljningsordern. Därför skapas en kopplad monteringsorder automatiskt när du lägger till artikeln i en försäljningsorderrad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: fe8964f46bd76d23e3f1457ad5627888ec3da012
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Sälja lagerartiklar i flöden för montering mot kundorder
Om fältet **Monteringsmetod** på en monteringsartikels artikelkort innehåller **Montering mot kundorder** förutsätter standardprocessen för försäljningsorder att artikeln inte finns på lager och måste monteras för den specifika försäljningsordern. Därför skapas en kopplad monteringsorder automatiskt när du lägger till artikeln i en försäljningsorderrad. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md). Men om en del av försäljningsorderantalet redan är tillgängligt i lagret kan du minska monteringsordersantalet genom att ändra i fältet **Antal att montera mot kundorder** på försäljningsorderraden.  

Det här är sällsynt eftersom artiklar för montering mot kundorder alltid förväntas vara anpassade. Det är föga troligt att de finns i lagret i en konfigurering som begärts av en annan kund. Men om ett företag har antal för montering mot kundorder i lager på grund av returer eller orderannulleringar ska dessa plockas och säljas innan nya monteras.  

> [!NOTE]  
>  Inga funktioner på försäljningsorder aviserar automatiskt eller hjälper till att dra av monteringsorderantal som redan är tillgängliga. Du måste i stället övervaka tillgänglighetsinformation, t.ex. som i faktaboxen **Försäljningsraddetaljer**.  

Liknande funktioner finns tillgängliga när du säljer monteringsartiklar från lagret, och en del eller hela antalet är otillgängligt och kan levereras av en monteringsorder. Mer information finns i [Så här säljer du artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Vissa regler gäller för fältet **Levereras antal** på försäljningsorderrader som innehåller en kombination av antal i montering mot kundorder och antal i lager. Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

I den här proceduren ersätter du antalet för montering mot kundorder med lagerantal på en försäljningsorderrad. I momenten ingår att undersöka tillgänglighet, dra av det aktuella antalet från kopplad monteringsorder, och sedan reservera den totala lagerkvantiteten så att den plockas och levereras för ordern.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Så här säljer du lagerartiklar i flöde för montering mot kundorder  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Skapa en försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).  
3.  Ange det efterfrågade antalet på en försäljningsorderrad för en artikel för montering mot kundorder i fältet **Antal**.  
4.  Fastställ om hela, eller något av, det efterfrågade antalet är tillgängligt i faktaboxen **Försäljningsraddetaljer**.  
5.  I fältet **Antal att montera mot kundorder** drar du av det disponibla antalet så att endast det ej tillgängliga antalet monteras mot ordern. I fältet **Reserverat antal** minskas därefter antalet för att visa att länken på orderbasis, eller reservationen, bara gäller det antal som måste monteras.  
6.  På snabbfliken **Rader** klickar du på **Funktioner** och väljer sedan åtgärden **Reservera**.  
7.  I fönstret **Reservation** väljer du den/de artikeltransaktionsrad/-er som har det disponibla antalet, välj åtgärden **Reservera från aktuell rad** och välj sedan knappen **OK**.  

    I fönstret **Försäljningsorder** visar fältet **Reserverat antal** nu att hela orderradens antal har reserverats. Fältet **Antal att montera mot kundorder** återspeglar fortfarande det underantal som måste monteras.  

8.  Släpp försäljningsordern för plockning av lagerartiklarna och för montering av de artiklar som inte är tillgängliga. Mer information finns i [Montera artiklar](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Fältet **Lagerplatskod** på försäljningsordern kan fyllas i i förväg enligt fältet **Lagerpl.kod för mont. mot lev.** eller fältet **Från monteringsplats - kod** på lagerställekortet. I så fall här kan fältet **Lagerplatskod** på försäljningsorderraden vara felaktigt i den här kombinationen av antal av montering mot kundorder och antal av montering mot lager. Det kan vara bra att titta i fältet **Lagerplatskod** och se till att placeringen fungerar för alla antal. Alternativt kan du ange de två olika antalen på separata försäljningsorderrader.  

## <a name="see-also"></a>Se även  
[Monteringshantering](assembly-assemble-items.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

