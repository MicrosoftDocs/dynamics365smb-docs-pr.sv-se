---
title: Sälj artiklar för montering mot kundorder och lagerartiklar ihop | Microsoft Docs
description: Om en monteringsartikel är inställd på montering mot lagerförutsätter standardprocessen för försäljningsorder att artikeln redan monterats och kan plockas från lagret, om den är tillgänglig. Men om en del (eller hela) antalet inte är tillgängligt har du möjlighet att skapa en monteringsorder för återstående antal direkt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 123d4613d042d9c3f7f863e7cd98b45c84a368ad
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772935"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Artiklar för montering mot kundorder och lagerartiklar ihop
Om fältet **Monteringsmetod** på en monteringsartikels artikelkort innehåller **Montering mot lager** förutsätter standardprocessen för försäljningsorder att artikeln redan monterats och kan plockas från lagret, om den är tillgänglig. Därför skapas inte monteringsorder automatiskt och länkas till försäljningsorderraden. Men om en del av (eller hela) antalet inte är tillgängligt har du en möjlighet att skapa en monteringsorder för återstående antal genom att fylla i fältet **Antal att montera mot kundorder** på försäljningsorderraden. På det här viset kan du montera artikeln mot kundorder även om det har lagts upp för montering mot lager som standard.  

Liknande flexibilitet finns när du säljer artiklar för montering mot order och en del av antalet finns i lagret. Du vill då dra av dessa från monteringsordern. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
>  Vissa regler gäller för fältet **Levereras antal** på försäljningsorderrader som innehåller en kombination av antal i montering mot kundorder och antal i lager. Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

> [!NOTE]  
>  I följande procedur ingår inte de standardsteg för försäljningsorder som du bör följa innan du skapar en monteringsorder för antal som inte är tillgängliga.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Så här säljer du artiklar för montering mot kundorder och lagerartiklar ihop  
1.  Ange ett antal i fältet **Antal** som överstiger lagret på en försäljningsorderrad för en artikel som ska monteras mot lager. Sidan **Kontrollera disponibelt** visas. Mer information finns i [Visa tillgängliga objekt](inventory-how-availability-overview.md).
2.  Observera fältet **Totalt antal** (med ett negativt värde), som du ska skriva in i nästa steg.  
3.  I fältet **Antal att montera mot kundorder** anger du värdet från föregående steg.  
4.  Utför någon ändring i monteringskomponenterna. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Släpp försäljningsordern, förbered den för plockning av lagerartiklarna och för montering av de artiklar som inte är tillgängliga. Mer information om dessa standardsteg för montering finns i [Montera artiklar](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Fältet **Lagerställeskod** på försäljningsordern kan fyllas i i förväg enligt fältet **Lagerpl.kod för mont. mot lev.** eller fältet **Från monteringsplats – kod** på lagerställekortet. I så fall här kan fältet **Lagerställeskod** på försäljningsorderraden vara felaktigt i den här kombinationen av antal av montering mot kundorder och antal av montering mot lager. Det kan vara bra att undersöka fältet **Lagerställeskod** och se till att placeringen fungerar för alla antal. Alternativt kan du ange de två olika antalen på separata försäljningsorderrader.  

## <a name="see-also"></a>Se även  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]