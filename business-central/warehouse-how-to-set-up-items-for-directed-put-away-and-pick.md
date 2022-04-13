---
title: Konfigurera Dirigerad art.inf. och plock.
description: Ställ in lagerställen för dirigerad artikelinförsel och plockning, finns det en ny funktion som du kan använda för att hantera dist.lagret på det mest effektiva sättet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: a33e68984a20a815b0ac774695937d5aae36a093
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519472"
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Registrera artiklar och platser för dirigerad artikelinförsel och plockning
När du skapar ett dist.lagerställe för dirigerad artikelinförsel och plockning, finns det en ny funktion som du kan använda för att hantera dist.lagret på det mest effektiva sättet. För att använda funktionen till fullo anger du extra information om artiklarna, vilket i sin tur innebär att beräkningar kan göras som talar om för dig hur du på bästa och effektivaste sätt utför dist.lageraktiviteter. Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Så här skapar du artiklar för dirigerad artikelinförsel och plockning  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2.  Öppna kortet för artikeln som du vill skapa dirigerad artikelinförsel och plockning för.
3. Definiera hur artikeln ska hanteras i dist.lagret genom att fylla i fälten på snabbfliken **Dist.lager** på artikelkortet.  
4.  Välj åtgärden **Enheter**.
5. På sidan **Artikelenheter** fyller du i de olika fälten för att definiera de olika enheter som artikeln kan överföras i, inklusive enhetens höjd, bredd, längd, kubik och vikt i formuläret.
6. Välj åtgärden **Lagerställesinnehåll**.
7. På sidan **Lagerställesinnehåll** definierar du det lagerställe och den lagerplats som artikeln ska associeras med. Fältet **Standard** används inte när lagerstället lagts upp för att använda dirigerad artikelinförsel och plockning.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>Så här aktiverar du funktionen för dirigerad artikelinförsel och plockning  
Med hjälp av dirigerad artikelinförsel och plockning får du tillgång till avancerade funktioner för distributionslagerkonfiguration som väsentligt kan öka effektiviteten och datatillförlitligheten. Om du vill använda den här funktionen måste du först ange ett antal parametrar för ditt lagerställe.  

Om du vill använda funktionen för dirigerad artikelinförsel och plockning måste du aktivera den på lagerställekortet.    
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2.  Markera det lagerställe där du vill använda dirigerad artikelinförsel och plockning, högerklicka och välj åtgärden **Redigera**.  
3.  Markera kryssrutan **Dirigerad artikelinförsel och plockning** på snabbfliken **Dist.lager**.  

Du behöver inte fylla i några andra fält på lagerställekortet förrän senare i inställningsprocessen.  

> [!NOTE]  
>  Du kan inte ställa in lager att använda lagerställen när lagerstället har öppna artikeltransaktioner.  

Nästa steg är att definiera vilken typ av lagerställen som du vill använda. Mer information finns i [Skapa lagerställen](warehouse-how-to-set-up-bin-types.md). Med hjälp av lagerplatstyper kan man styra hur en viss lagerplats används när artiklar flyttas i distributionslagret. Du kan fördela en lagerplatstyp till både en zon och en lagerplats.  

Du kan även definiera klasskoder för distributionslagret om distributionslagret innehåller artiklar som kräver olika lagringsförhållanden. Distributionsklasskoder används när lagerställen föreslås för artiklar. Du kan fördela lagerklasskoder till produktgrupper, som sedan tilldelas artiklar och lagerställeenheter, eller till zoner och lagerställen, som kan hysa lagringsvillkoren som krävs enligt lagerklasskoderna.  

Nu kan du skapa zoner om du vill använda zoner i distributionslagret. Genom att använda zoner minskar du antalet fält som måste fyllas i när du lägger upp lagerställen, eftersom lagerställen som skapas i zoner ärver flera av zonens egenskaper. Zoner kan även göra det lättare för ny- eller korttidsanställda att orientera sig i distributionslagret. Observera att flödet styrs av lagerställen, därför är det möjligt att arbeta med lagerställen och endast en zon.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>Så här skapar du en zon i distributionslagret  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2.  Välj lagerstället där du vill ställa in zonen och öppna lagerställekortet och välj sedan åtgärden **Zoner**.  
3.  Fyll i fälten på snabbfliken **Zoner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du ändrar en zonkod har alla lagerställen du skapar därefter i zonen samma egenskaper men de lagerställen inte kommer att ändras.  

> [!NOTE]  
>  Om du vill arbeta utan zoner, måste du fortfarande skapa en zonkod som är odefinierad förutom i kod.  

Nästa steg när du lägger upp dist.lagret är att definiera lagerställen. Mer information finns i [Så här lägger du upp lagerställen för att använda lagerställen](warehouse-how-to-set-up-locations-to-use-bins.md).  

Dessutom måste du skapa artikelinförselmallar och inventeringsperioder. Mer information finns i [Skapa artikelinförselsmallar](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]