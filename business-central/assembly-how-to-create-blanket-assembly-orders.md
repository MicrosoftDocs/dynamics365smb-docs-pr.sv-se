---
title: Skapa monteringsorder för avrop
description: Skapa försäljningsavropsorder för anpassade monteringsartiklar före periodens skapande av faktiska försäljningsorder enligt avropsorderavtalet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-blanket-assembly-orders"></a>Skapa monteringsorder för avrop

Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

 Som med alla typer av artiklar kan du också skapa avropsförsäljningsorder för anpassade monteringsartiklar före periodens skapande av faktiska försäljningsorder enligt avropsorderavtalet. Den här processen involverar flera extra steg i jämförelse med att skapa en vanlig avropsförsäljningsorder. Den använder en variation av en kopplad monteringsorder, dvs. en monteringsorder för avrop.

> [!NOTE]  
>  Som för alla avropsorder är antalet i monteringsavropsorder endast prognoser och kan inte användas förrän de konverterats till faktiska monteringsorder. Därför är orderfunktioner som dispositionsberäkning, reservation och artikelspårning inte aktiva för monteringsorder för avrop.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Så här skapar du en monteringsorder för avrop för montering\-mot\-kundorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsavropsorder** och väljer sedan relaterad länk.  
2. Skapa en ny avropsorder med en rad för en monteringsartikel. Mer information finns i [Skapa försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md).  
3. I fältet **Antal att montera mot kundorder** på monteringsorderraden anger du det totala antalet.

    > [!NOTE]  
    >  Du bör inte skapa avropsorderavtal för delvisa antal. Därför måste du ange samma antal som du angett i fältet **Antal** på avropsorderraden.  

4. Välj åtgärden **Montering mot kundorder** och välj sedan åtgärden **Montering mot kundorderrader**. Alternativt kan du välja fältet **Antal att montera mot kundorder** på raden.  
5. På sidan **Montering mot kundorderrader** granskar eller ändrar du monteringsorderrader enligt avropsorderavtalet som du har gjort med kunden. Om du vill ha mer information kan du välja åtgärden **Visa dokument** för att öppna hela avropsförsäljningsordern. Du kan inte ändra innehållet i de flesta fält, och du kan inte bokföra.  
6. När du har justerat monteringsorderraderna enligt avropsorderavtalet stänger du sidan **Montering mot kundorderrader** så att du kommer tillbaka till sidan **Förs.avropsorder**.  
7. När kunden efterfrågar en försäljningsorder baserat på den överenskomna avropsordern, skapar du en försäljningsorder för den överenskomna monteringsartikeln eller artiklarna. Mer information finns i [Skapa försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md).

Den länkade avropsmonteringsofferten och eventuella anpassningar är kopplade till den nya försäljningsordern så att artikelmontering eller -försäljning kan förberedas.  

## <a name="see-also"></a>Se även

[Skapa försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
