---
title: Så här skapar du leveransmetoder | Microsoft Docs
description: Du kan lägga upp en kod för var och en av dina leveransmetoder och ange information om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f1916724c995f875d15b931e919d07d2253dcdb1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748300"
---
# <a name="set-up-shipment-methods"></a>Så här definierar du leveransmetoder
Leveransmetoder, även kallade incoterms är ofta beroende av vilka artiklar, kunder eller leverantörer som avses. Om kunden t.ex. bor på en ö kan han eller hon välja att få artiklarna levererade per flyg eller båt. Vissa kunder kan kräva leverans nästa dag. En del kanske vill plocka upp ordern. På kund- och leverantörskorten kan du ange vilken typ av leverans som önskas.

Du upprättar en beskrivning och en kod för varje leveransvillkor på sidan **Leveransmetoder**. Du kan t.ex. upprätta koden FOB och i fältet **Beskrivning** skriver du Fritt ombord. Du kan skriva in koden i fältet **Leveransmetodkod** någon annanstans i systemet, t.ex. på ett kundkort. När du sedan skapar nya order, fakturor, kreditnotor, etc. fyller systemet i den beskrivning, som representeras av koden. Du kan ändra den i dokumentet om det behövs.

## <a name="to-set-up-a-shipment-code"></a>Så här skapar du en leveranskod
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **leveransmetoder** och välj sedan relaterad länk.
2. På sidan **Leveransmetoder** väljer du åtgärden **Ny**.
3. På den nya raden anger du en kod och en beskrivning för leveransmetoden.

## <a name="see-also"></a>Se även
[Incoterms](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Så här konfigurerar du speditörer](sales-how-to-set-up-shipping-agents.md)  
[Spåra paket](sales-how-track-packages.md)    
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]