---
title: "Så här kan du planera projektorder | Microsoft Docs"
description: "Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna på sidan **Förs.orderplanering** används. När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av sidan **Orderplanering**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4cb63a7dc26e13c7947ba2ae071c3dff87c53e9d
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="plan-project-orders"></a>Planera projektorder
Den här planeringsåtgärden påbörjas från en försäljningsorder, och inställningarna på sidan **Förs.orderplanering** används. När du har skapat en projektproduktionsorder kan du planera den ytterligare med hjälp av sidan **Orderplanering**.  

## <a name="to-create-a-project-production-order"></a>Så här skapar du en projektproduktionsorder  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Markera den försäljningsorder som motsvarar produktionsprojektet och välj sedan åtgärden **planering**.  
4.  På sidan **Förs.orderplanering** väljer du åtgärden **Skapa prod.order**.  
5.  På sidan **Skapa order från försäljning** markerar du **Ordertyp** i **Prod.order per order**.  
6.  Välj **Ja**.  
7.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Produktionsorder** och välj sedan relaterad länk.
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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

