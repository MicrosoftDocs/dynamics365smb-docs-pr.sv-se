---
title: Översikt över uppgifter för konfigurering av försäljningprocesser
description: Översikt över uppgifter som krävs för att ställa in regler och värden som definierar dina försäljningsprinciper och processer, inklusive allmänna inställningar och ekonomirelaterade försäljningsinställningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.search.form: 170, 172, 300, 301, 428, 459, 1401
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 7ec2741e9ff0a5c8ccd00fb8df31cda0a5bfcec6
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752322"
---
# <a name="setting-up-sales"></a>Konfigurera försäljning
Innan du kan hantera försäljningsprocesser måste du konfigurera reglerna och värdena som definierar företagets försäljningspolicies.

Du måste definiera de allmänna inställningarna på sidan **Försäljningsinställningar**, till exempel vilka försäljningsdokument som krävs, hur deras värden ska bokföras och vilken typ av rader som ska skapas som standard. Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.

En separat serie uppgifter relaterade till att registrera nya kunder är att registrera alla specialpriser eller rabattavtal som du har med varje kund. Mer information finns i [Registrera speciella försäljningspriser och rabatter](sales-how-record-sales-price-discount-payment-agreements.md).

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
|Ange standardrapporter som ska användas för olika dokumenttyper.|[Rapportval i Business Central](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]