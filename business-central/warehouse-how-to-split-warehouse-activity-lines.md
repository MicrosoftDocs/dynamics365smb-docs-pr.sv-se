---
title: 'Så här: Dela Dist.lageraktivitetsrader | Microsoft Docs'
description: I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerställen för plockning och införsel av artiklar. det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på den föreslagna lagerstället för införsel av det aktuella antalet. I så fall måste du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08cebf3fb140fd76396add89bf8d7418aa4f115a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784148"
---
# <a name="split-warehouse-activity-lines"></a>Dela rader för dist.lageraktivitet
I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerställen för plockning och införsel av artiklar. det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på den föreslagna lagerstället för införsel av det aktuella antalet. I så fall måste du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats.  

Följande procedur gäller alla distributionslagerdokument, till exempel Dist.lager artikelinförsel, transport och plockningsrader, eller lager, artikelinförsel, transport och plockningsrader.  

## <a name="to-split-warehouse-activity-lines"></a>Att dela Dist.lageraktivitet rader  
1.  Öppna en lageraktivitetsrad där du försöker manipulera ett otillräckligt antal.  
2.  I **Ant. att hantera** fältet, ange det antal som kan hantera.  
3.  På snabbfliken **Rader** väljer du åtgärden **Åtgärder** och väljer sedan åtgärden **Funktioner** och sedan åtgärden **Dela rad**. Det visas en ny rad, som är en kopia av den ursprungliga raden, med den skillnaden att fältet **Ant. att hantera** innehåller det antal som du tog bort från den ursprungliga raden.  
4.  Tilldela den nya raden en lämplig lagerplats och zon, om du använder dirigerad artikelinförsel och plockning, eller fortsätt att dela upp raden efter behov tills du har önskat antal lagerställen för hela kvantiteten.  

> [!NOTE]  
>  Om lagerstället är inställt på dirigerad artikelinförsel och plockning, och du delar raderna, måste du vara förtrogen med distributionslagret och kunna välja en lagerplats som passar artikelns lagringskrav och uppfyller de allmänna kraven i distributionslagerdokumentet. Du skulle till exempel inte dela en rad i ett plockningsdokument och placera några artiklar i volymlagret.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]