---
title: Konfigurera Dirigerad art.inf. och plock.
description: Dirigerad artikelinförsel och plockning ger funktioner för att driva ditt distributionslager effektivt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
---
# Registrera artiklar och platser för dirigerad artikelinförsel och plockning

När du skapar ett dist.lagerställe för dirigerad artikelinförsel och plockning, finns det en ny funktion som du kan använda för att hantera dist.lagret på det mest effektiva sättet. För att använda funktionen till fullo anger du extra information om artiklarna, vilket i sin tur innebär att beräkningar kan göras som talar om för dig hur du på bästa och effektivaste sätt utför dist.lageraktiviteter. 

## Så här skapar du artiklar för dirigerad artikelinförsel och plockning  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Öppna kortet för artikeln som du vill skapa dirigerad artikelinförsel och plockning för.
3. Definiera hur artikeln ska hanteras i dist.lagret genom att fylla i fälten på snabbfliken **Dist.lager** på artikelkortet.  
4. Välj åtgärden **Enheter**.
5. På sidan **Måttenheter för artikel** definierar du de måttenheter som artikeln kan överföras i efter artikelns höjd, bredd, längd, kubik och vikt.
6. Välj åtgärden **Lagerställesinnehåll**.
7. På sidan **Lagerställesinnehåll** definierar du det lagerställe och den lagerplats som artikeln ska associeras med. Fältet **Standard** används inte när lagerstället lagts upp för att använda dirigerad artikelinförsel och plockning.  

## För att börja använda dirigerad artikelinförsel och plockning

Med hjälp av dirigerad artikelinförsel och plockning får du tillgång till avancerade funktioner för distributionslagerkonfiguration som väsentligt kan öka effektiviteten och datatillförlitligheten. Om du vill använda den här funktionen måste du först ange ett antal parametrar för ditt lagerställe.  

Om du vill använda funktionen för dirigerad artikelinförsel och plockning måste du aktivera den på lagerställekortet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2. Markera det lagerställe där du vill använda dirigerad artikelinförsel och plockning, högerklicka och välj åtgärden **Redigera**.  
3. På snabbfliken **Lagerställe**, markera kryssrutan **Dirigerad artikelinförsel och plockning**.  

Du behöver inte fylla i några andra fält på lagerställekortet förrän senare i inställningsprocessen.  

> [!NOTE]  
> Du kan inte ställa in lager att använda lagerställen när lagerstället har öppna artikeltransaktioner.  

Nästa steg är att definiera vilken typ av lagerställen som du vill använda. Mer information finns i [Skapa lagerställen](warehouse-how-to-set-up-bin-types.md). Med hjälp av lagerplatstyper kan man styra hur en viss lagerplats används när artiklar flyttas i distributionslagret. Du kan fördela en lagerplatstyp till både en zon och en lagerplats.  

Du kan även definiera klasskoder för distributionslagret om distributionslagret innehåller artiklar som kräver specifika lagringsförhållanden. Distributionsklasskoder används när lagerställen föreslås för artiklar. Du kan fördela lagerklasskoder till produktgrupper, som sedan tilldelas artiklar och lagerställeenheter, eller till zoner och lagerställen, som kan hysa lagringsvillkoren som krävs enligt lagerklasskoderna.  

Du är nu klar att skapa zoner, om du vill. Genom att använda zoner minskar du antalet fält som måste fyllas i när du lägger upp lagerställen, eftersom lagerställen som skapas i zoner ärver flera av zonens egenskaper. Zoner kan även göra det lättare för ny- eller korttidsanställda att orientera sig i distributionslagret. Observera att flödet styrs av lagerställen, därför är det möjligt att arbeta med lagerställen och endast en zon.  

## Så här skapar du en zon i distributionslagret  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2. Välj lagerstället där du vill ställa in zonen och öppna lagerställekortet och välj sedan åtgärden **Zoner**.  
3. Fyll i fälten på snabbfliken **Zoner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du ändrar en zonkod har alla lagerställen du skapar därefter i zonen samma egenskaper men de lagerställen inte kommer att ändras.  

> [!NOTE]  
> Om du vill arbeta utan zoner, måste du fortfarande skapa en zonkod som är odefinierad förutom i kod.  

Nästa steg är att definiera lagerställen. Mer information finns i [Registrera lagerställen för att använda lagerställen](warehouse-how-to-set-up-locations-to-use-bins.md).  

Dessutom måste du skapa artikelinförselmallar och inventeringsperioder. Mer information finns i [Skapa artikelinförselsmallar](warehouse-how-to-set-up-put-away-templates.md).  

## Se även  

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]