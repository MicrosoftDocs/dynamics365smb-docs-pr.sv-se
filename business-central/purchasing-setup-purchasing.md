---
title: Översikt över uppgifter för att ställa in inköp
description: Beskriver uppgifterna för att definiera företagets inköppolicyer och registrerar inköpsprocesserna.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.search.form: 175, 176, 177, 178, 456, 460, 5727, 5729
ms.date: 07/04/2022
ms.author: edupont
ms.openlocfilehash: 008c0d35c8bfefdf002e08b967ddc1a9336b04a5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530385"
---
# <a name="setting-up-purchasing"></a>Ställa in inköp

Innan du kan hantera inköpsprocesser måste du konfigurera reglerna och värdena som definierar företagets inköpspolicyer.

Du måste ställa in de allmänna inställningarna, till exempel vilka inköpsdokument som är obligatoriska och hur deras värden ska bokföras. Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.

En separat serie uppgifter relaterade till att registrera nya leverantörer är att registrera alla specialpriser eller rabattavtal som du har med varje leverantör.

Finansrelaterade inköp, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans. Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md). På samma sätt kan lagerrelaterade inköpsinställningar, till exempel enheter och artikelspårningskoder, finnas i [avsnittet lagerinställningar](inventory-setup-inventory.md).

| Till | Gå till |
| --- | --- |
| Skapa ett leverantörskort för varje leverantör som du har köpt av. |[Registrera nya leverantörer](purchasing-how-register-new-vendors.md) |
| Prioritera leverantörer |[Prioritera leverantörer](purchasing-how-prioritize-vendors.md) |
| Ange bank konto information – inklusive IBAN och SWIFT-koder – på leverantörens kort. | [Skapa bankkonton för leverantörer](purchasing-how-set-up-vendors-bank-accounts.md) |
| Skapa inköpare, tilldela leverantörer och koder för att spåra statistik. |[Konfigurera inköpare](purchasing-how-setup-purchasers.md) |
| Ange de olika rabatterna och specialpriserna som leverantörerna beviljar dig beroende på artikel, kvantitet och/eller datum. |[Registrera inköpspris, rabatt och betalningsavtal](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definiera vad du betalar för de artiklar och tjänster som köpts av ditt företag.  | [Ställa in priser och rabatter](across-prices-and-discounts.md) |
| Skapa standardrader som ska infogas på återkommande inköpsdokument. | [Ställ in återkommande inköpsrader](purchasing-how-work-recurring-purchase-lines.md) |
| Skapa sekvenser av uppgifter för att ansluta processer som utförs av olika användare, till exempel begära och godkänna inköpsorder. | [Konfigurera arbetsflöden för godkännande av inköp](across-set-up-workflows.md) |
| Hantera affärsinteraktion med leverantörerna, importera mottagna fakturadokument och registrera nya leverantörer med hjälp av e-postklienten för Outlook. | [Konfigurera Business Central-tillägget för Outlook](admin-outlook.md) |
| Granska utgiftskvitton, konvertera papper och elektroniska dokument till journalrader och digitala pappersfakturor från leverantörer. | [Ställa in inkommande dokument](across-how-setup-income-documents.md) |
| Ange standardrapporter som ska användas för olika dokumenttyper. |[Rapportval i Business Central](across-report-selections.md)|

> [!TIP]
> Beroende på ditt geografiska läge kan vissa sidor innehålla fält som inte beskrivs i artiklarna som anges här, detta eftersom de gäller lokala funktioner eller anpassningar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="external-document-number"></a>Externt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/trade-get-started-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Inköp](purchasing-manage-purchasing.md)  
[Översikt över installation](setup.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
