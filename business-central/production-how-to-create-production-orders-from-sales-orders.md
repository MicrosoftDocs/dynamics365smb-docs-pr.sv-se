---
title: Så här skapar du produktionsorder från försäljningsorder
description: Du kan skapa produktionsorder från försäljningsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115242"
---
# <a name="create-production-orders-from-sales-orders"></a>Så här skapar du produktionsorder från försäljningsorder
Du kan skapa produktionsorder för producerade artiklar direkt från försäljningsorder.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Så här skapar du produktionsorder från försäljningsorder  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
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
