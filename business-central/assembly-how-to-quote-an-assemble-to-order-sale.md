---
title: Skapa en försäljning för montering mot kundorder
description: Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 79d7e9ac5e3a71002af168ee02feef1a76671fce
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528418"
---
# <a name="quote-an-assemble-to-order-sale"></a>Skapa en försäljning för montering mot kundorder

Du kan använda monteringshantering för att anpassa en monteringsartikel till ett kundkrav under försäljningsprocessen. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

När du säljer någon annan typ av artikel kan du också skapa en försäljningsoffert för en anpassad monteringsartikel innan du omvandlar den till en försäljningsorder. Den här processen involverar flera extra steg i jämförelse med att skapa en vanlig försäljningsoffert. Den använder en variation av en kopplad monteringsorder, dvs. en monteringsoffert.

> [!NOTE]  
>  Precis som på alla typer av offerter används inte antalet på monteringsoffertar för tillgänglighet, planering eller reservationer.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Så här skapar du en försäljningsoffert för en artikel för montering mot kundorder

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsoffert** och väljer sedan relaterad länk.  
2.  Skapa en försäljningsoffertrad med en rad för en monteringsartikel. Mer information finns i [Gör försäljningsoffert](sales-how-make-offers.md).  
3.  I fältet **Antal att montera mot kundorder** anger du hela antalet.

    > [!NOTE]  
    >  Du bör inte erbjuda ett delantal i offerten. Därför måste du ange samma antal som du angett i fältet **Antal** på försäljningsoffertraden.  

4.  På snabbfliken **Rader** väljer du **Rad**, **Montering mot kundorder** och sedan **Montering mot kundorderrader**. Alternativt kan du välja fältet **Antal att montera mot kundorder** på raden.  
5.  På sidan **Montering mot kundorderrader** granskar eller ändrar du monteringsorderrader enligt den offert som kunden begär. Om du vill ha mer information kan du välja åtgärden **Visa dokument** för att öppna hela avropsordern för offerten. Du kan inte ändra innehållet i de flesta fält, och du kan inte bokföra.  
6.  När du har justerat monteringsorderraderna enligt offerten stänger du sidan **Montering mot kundorderrader** så att du kommer tillbaka till sidan **Försäljningsoffert**.  
7.  Om kunden accepterar offerten skapar du en försäljningsorder för den offererade monteringsartikeln. Mer information finns i [Gör försäljningsoffert](sales-how-make-offers.md). Den länkade monteringsofferten och eventuella anpassningar är kopplad till den nya försäljningsordern så att artikelmontering eller -försäljning kan förberedas.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
