---
title: Så här skapar du produktionsorder från försäljningsorder
description: Lär dig de olika sätten att skapa produktionsorder för producerade artiklar direkt från försäljningsorder.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000883, 99000884
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 3080556ad69882c533bec3768787784bfdac5c4f
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145530"
---
# <a name="create-production-orders-from-sales-orders"></a>Så här skapar du produktionsorder från försäljningsorder
Du kan skapa produktionsorder för producerade artiklar direkt från försäljningsorder.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Så här skapar du produktionsorder från försäljningsorder  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2.  Markera den försäljningsorder som du vill skapa en produktionsorder för.  
3.  Välj åtgärden **Planerad**. På sidan **Förs.orderplanering** kan du visa dispositionen för artikeln på i ordern.  
4.  Välj åtgärden **Skapa prod.order**.  
5.  Välj status och ordertyp.  
6.  Tryck på knappen **Ja** för att skapa en eller flera produktionsorder för raderna som har **Prod.order** i fältet **Återanskaffningssystem**.


> [!NOTE]  
> Behovsrader i den skapade produktionsordern, som har **Prod.order** i sitt **Återanskaffningssystem**-fält, motsvarar underliggande produktionsorder. När du har genererat dessa produktionsorder får du inte glömma att att identifiera ouppfyllda komponentbehov för dem med sidan **Orderplanering** eller funktionen **Omplanering** från skapade order. 

## <a name="order-type"></a>Ordertyp  
Du kan välja mellan två olika sätt att skapa produktionsorder enligt vad som beskrivs i följande tabell.

|Alternativ|Beskrivning|
|------|-----------|
|Artikelorder|En produktionsorder skapas för varje nödvändig produktionsorder som representeras av en rad i fönstret **Försäljningsorderplanering**.|
|Projektorder|En produktionsorder skapas för varje nödvändig produktionsorder som representeras av en rad i fönstret **Försäljningsorderplanering**. |

När du använder projektorder innehåller fältet **Ursprungstyp** för produktionsordern **Försäljningshuvud**, och ordern innehåller flera rader (en för varje försäljningsradartikel som måste skapas).  


## <a name="see-also"></a>Se även  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
