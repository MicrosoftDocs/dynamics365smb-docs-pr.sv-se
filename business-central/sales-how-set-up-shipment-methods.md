---
title: Så här definierar du leveransmetoder
description: Du kan lägga upp en kod för var och en av dina leveransmetoder , samt ange information om dem.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.search.form: 11, 130
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7f83c8e3e001fe1b92e975d165d40a353ece032a
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134931"
---
# <a name="set-up-shipment-methods"></a>Så här definierar du leveransmetoder

Utleveransmetoderna är ofta beroende av vilka artiklar, kunder eller leverantörer som avses. Om kunden t. ex. bor på en ö kan han eller hon välja att få artiklarna levererade per flyg eller båt. Vissa kunder kan kräva leverans nästa dag. En del kanske vill plocka upp ordern. På kund- och leverantörskorten kan du ange vilken typ av leverans som önskas.

Du upprättar en beskrivning och en kod för varje leveransvillkor på sidan **Leveransmetoder**. Du kan t. ex. upprätta koden FOB och i fältet **Beskrivning** skriver du Fritt ombord. Du kan skriva in koden i fältet **Leveransmetodkod** någon annanstans i systemet, t. ex. på ett kundkort. När du sedan skapar nya order, fakturor, kreditnotor, etc. fyller systemet i den beskrivning, som representeras av koden. Du kan ändra den i dokumentet om det behövs.

## <a name="to-set-up-a-shipment-method"></a>Så här definierar du utleveransvillkor

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **leveransmetoder** och väljer sedan relaterad länk.
2. På sidan **Leveransmetoder** väljer du åtgärden **Ny**.
3. På den nya raden anger du en kod och en beskrivning för leveransmetoden.

> [!TIP]
> Om du använder Incoterms ställer du in utleveransmetoder för att representera relevanta Incoterms-regler.  

## <a name="see-also"></a>Se även

[Så här konfigurerar du speditörer](sales-how-to-set-up-shipping-agents.md)  
[Spåra paket](sales-how-track-packages.md)  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterms på iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]