---
title: Sälja lagerartiklar i flöden för montering mot kundorder
description: Artiklar där montering mot kundorder monteras för försäljningsorder via en monteringsorder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows" />Så här säljer du lagerartiklar i flöde för montering mot kundorder

Om fältet **Monteringsmetod** på en monteringsartikels artikelkort innehåller **Montering mot kundorder** förutsätter processen för försäljningsorder att artikeln inte finns på lager och måste monteras för försäljningsordern. När du anger en artikel på en rad på försäljningsordern skapar [!INCLUDE [prod_short](includes/prod_short.md)] en monteringsorder som länkas till försäljningsordern. Om du vill veta mer om att sälja artiklar för montering mot kundorder går du till [Sälja artiklar monterade på order](assembly-how-to-sell-items-assembled-to-order.md). Men om en del av försäljningsorderantalet redan är tillgängligt i lagret kan du minska monteringsordersantalet genom att ändra i fältet **Antal att montera mot kundorder** på försäljningsorderraden.  

Det är ganska ovanligt att företag säljer lagerartiklar som artiklar för montering mot kundorder. Artiklar där montering mot kundorder är normalt inte standard. De har anpassats så att de uppfyller specifika kundkrav. Du kan dock ha antal artiklar för artiklar för montering mot kundorder på grund av returer eller orderannulleringar. Dessa kvantiteter bör plockas och säljas innan nya monteras.  

> [!NOTE]  
> För att kontrollera om artiklar för montering mot kundorder redan är tillgängliga för monteringsbeställningar, använd faktaboxen **Försäljningsraddetaljer** på försäljningsordern.  

Du kan göra liknande saker när du säljer monteringsartiklar från lagret och en del av eller hela antalet är inte tillgängligt. Du kan ange den saknade kvantiteten via en monteringsorder. Mer information om att sälja lager- och monteringsartiklar finns i [Artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Vissa regler gäller för fältet **Ant. att utleverera** på försäljningsorderrader som innehåller en kombination av antal i montering mot kundorder och antal i lager. Om du vill veta mer om reglerna går du till [kombinationsscenarier](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

I den här proceduren ersätter du antalet för montering mot kundorder med lagerantal på en försäljningsorderrad. Följande steg ger en översikt:

1. Bestäm tillgänglighet.
2. Minskning av kvantiteten från den kopplade monteringsordern.
3. Reservera lagerkvantiteten för att kontrollera att den har plockats och levererats för ordern.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows" />Så här säljer du lagerartiklar i flöde för montering mot kundorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Skapa en försäljningsorder. Mer information om hur du använder försäljningsorder finns i [Sälj produkter](sales-how-sell-products.md).  
3. Ange antal på en försäljningsorderrad för en artikel för montering mot kundorder i fältet **Antal**.  
4. I faktaboxen **Försäljningsraddetaljer**, avgöra om en del av hela kvantiteten är tillgänglig.  
5. I fältet **Antal att montera mot kundorder** drar du av det disponibla antalet så att endast det ej tillgängliga antalet monteras mot ordern. I fältet **Reserverat antal** minskas därefter antalet för att visa att länken på orderbasis, eller reservationen, bara gäller det antal som måste monteras.  
6. På snabbfliken **Rader** klickar du på **Funktioner** och väljer sedan åtgärden **Reservera**.  
7. På sidan **Reservation** väljer du den/de artikeltransaktionsrad/-er som har det disponibla antalet, välj åtgärden **Reservera från aktuell rad** och välj sedan knappen **OK**.  

    På sidan **Försäljningsorder** visar fältet **Reserverat antal** nu att hela orderradens antal har reserverats. Fältet **Antal att montera mot kundorder** återspeglar fortfarande det antal som ska monteras.  

8. Släpp försäljningsordern för att göra artiklarna tillgängliga för plockning och för montering av de artiklar som inte är tillgängliga. För att lära dig mer om montering av artiklar, gå till [Montera artiklar](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Fältet **Lagerställeskod** på försäljningsordern kan innehålla värdet från fältet **Lagerpl.kod för mont. mot lev.** eller fältet **Från monteringsplats – kod** på lagerställekortet. I så fall här kan fältet **Lagerställeskod** på försäljningsorderraden vara felaktigt i den här kombinationen av antal av montering mot kundorder och antal av montering mot lager. Det kan vara bra att titta i fältet **Lagerställeskod** och se till att det fungerar för alla antal. Alternativt kan du ange de två olika antalen på separata försäljningsorderrader.  

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Monteringshantering](assembly-assemble-items.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
