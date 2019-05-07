---
title: Så här skapar du monteringsorder för avrop | Microsoft Docs
description: Skapa försäljningsavropsorder för anpassade monteringsartiklar före periodens skapande av faktiska försäljningsorder enligt avropsorderavtalet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 06e760f10ae1b427ebc3fb9540740f126caf2d3c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934681"
---
# <a name="create-blanket-assembly-orders"></a>Skapa monteringsorder för avrop
Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

 Som med alla typer av artiklar kan du också skapa avropsförsäljningsorder för anpassade monteringsartiklar före periodens skapande av faktiska försäljningsorder enligt avropsorderavtalet. Den här processen involverar flera extra steg i jämförelse med att skapa en vanlig avropsförsäljningsorder. Den använder en variation av en kopplad monteringsorder, dvs. en monteringsorder för avrop.

> [!NOTE]  
>  Som för alla avropsorder är antalet i monteringsavropsorder endast prognoser och kan inte användas förrän de konverterats till faktiska monteringsorder. Därför är orderfunktioner som dispositionsberäkning, reservation och artikelspårning inte aktiva för monteringsorder för avrop.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Så här skapar du en monteringsorder för avrop för montering\-mot\-kundorder  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Förs.avropsorder** och välj sedan relaterad länk.  
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
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
