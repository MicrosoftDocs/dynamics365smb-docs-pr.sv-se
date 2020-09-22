---
title: Översikt över proceduren för att konfigurera försäljningsprocesser | Microsoft Docs
description: Innehåller information om hur du definierar regler och värden för att definiera dina försäljningspolicyer och -processer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 65064d8c8fb0082c49f230398f22ce1406993f46
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788831"
---
# <a name="setting-up-sales"></a>Konfigurera försäljning
Innan du kan hantera försäljningsprocesser måste du konfigurera reglerna och värdena som definierar företagets försäljningspolicies.

Först måste du definiera allmänna inställningar, till exempel vilka försäljningsdokument som krävs och hur deras värden bokförs. Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.

En separat serie uppgifter relaterade till att registrera nya kunder är att registrera alla specialpriser eller rabattavtal som du har med varje kund.

Finansrelaterade försäljningar, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans. Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).

| Om du vill | Gå till |
| --- | --- |
| Skapa ett kundkort för varje kund som du säljer till. |[Registrera nya kunder](sales-how-register-new-customers.md) |
| Låt kunder betala via PayPal, genom att välja PayPal-logotypen på försäljningsdokument. |[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md) |
| Ange olika rabatter och specialpriser som du beviljar kunden beroende på artikel, antal och/eller datum. |[Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md) |
| Skapa säljare så att du kan tilldela dem till kundkontakter eller mät säljares prestanda som grund för att beräkna deras försäljningprovision eller bonus. |[Skapa säljare](sales-how-setup-salespeople.md) |
| Ange hur försäljningsdokument ska skickas som standard för enskilda kunder eller för alla kunder när du väljer åtgärden **Bokför och skicka**. |[Skapa dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md) |
| Konfigurera din e-post så att den innehåller en sammanfattning av informationen på försäljningsdokumentet som har skickats. |[Skicka dokument som e-post](ui-how-send-documents-email.md). |
|Du kan använda en EU-webbtjänst för att kontrollera kundens momsregistreringsnummer.|[Kontrollera momsregistreringsnummer](finance-setup-vat.md)|
|Definiera de olika Incoterms som du erbjuder till kunder eller som leverantören erbjuder dig.|[Så här definierar du leveransmetoder](sales-how-set-up-shipment-methods.md)|
|Ange information om de olika transportleverantörerna som du använder, bland annat en länk till deras godsupplysningstjänst.|[Så här konfigurerar du speditörer](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
