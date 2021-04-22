---
title: Så här kan du planera projektorder | Microsoft Docs
description: Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna på sidan **Förs.orderplanering** används. När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av sidan **Orderplanering**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 28568cd8ab7751e15bf24acd3c727828bba9f76c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787958"
---
# <a name="plan-project-orders"></a>Planera projektorder
Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna på sidan **Förs.orderplanering** används. När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av sidan **Orderplanering**.  

## <a name="to-create-a-project-production-order"></a>Så här skapar du en projektproduktionsorder  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Markera den försäljningsorder som motsvarar produktionsprojektet och välj sedan åtgärden **planering**.  
4.  På sidan **Förs.orderplanering** väljer du åtgärden **Skapa prod.order**.  
5.  På sidan **Skapa order från försäljning** markerar du **Ordertyp** i **Prod.order per order**.  
6.  Välj **Ja**.  
7.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **produktionsorder** och välj sedan relaterad länk.
8. Öppna den produktionsorder som du skapade nyss.  

    Observera att fältet **Ursprungstyp** för produktionsordern visas **Försäljningshuvud**, och ordern innehåller flera rader (en för varje försäljningsradartikel som måste skapas).  
9. Välj åtgärden **Planerad**.
10. På sidan **Orderplanering** väljer du åtgärden **uppdatera** för att beräkna det nya behovet.  

Orderhuvudraden för projektordern visas, och alla rader med ouppfyllda behov expanderas under den. Även om produktionsordern innehåller rader för flera producerade artiklar så visas det totala behovet för alla produktionsorderrader under en orderhuvudrad på sidan **Orderplanering**, och det ursprungliga kundnamnet visas. Du kan nu fortsätta med att planera för behovet enligt beskrivningen i [Planera ny behovsorder efter order](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Behovsrader i projektproduktionsordern, som har **Prod. Order** i sitt **Återanskaffningssystem** -fält, motsvarar underliggande produktionsorder. När du har genererats dessa produktionsorder, måste du återigen beräkna en plan på sidan **Orderplanering** för att identifiera några ouppfyllda komponentbehov för dem. I så fall visas de som behovsrader under en typisk rad i ett produktionsorderhuvud, dvs. att projektrelationen inte längre visas på sidan. Men om du använder orderspårningsfunktionen kan du se bakåt och framåt i alla leveransorder som skapas under den ursprungliga försäljningsordern.  

## <a name="see-also"></a>Se även
[Planerad](production-planning.md)   
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]