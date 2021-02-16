---
title: Tillägg för skicka kundremissa | Microsoft Docs
description: Beskriver tillägget för skicka kundremissa som möjliggör e-post och skicka om kundremissa från betalningsjournalen och leverantörsreskontratransaktionerna.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3ae8d131b714b0d7ffb60727d1a991cd6e4ab692
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757073"
---
# <a name="send-remittance-advice"></a>Skicka kundremissa

När kundremissa används för att meddela leverantörerna om de betalningar som görs kan du nu skicka kundremissa i bulk från betalningsjournalen och skicka om när du har utfört betalningar från leverantörsreskontratransaktioner genom att använda dokumentutskicksprofiler.

> [!NOTE]
> Denna funktion stöds endast i Business Central online och lokalt i följande länder: Storbritannien, USA, Kanada, Australien, Nya Zeeland och Sydafrika.  

Du kan skicka kundremissa på två olika sätt:

* Gå till sidan **Utbetalningsjournal** och välj **Relaterat**, **Betalningar**, **Skicka kundremissa** för att skicka kundremissa via e-post för en eller flera utbetalningsjournaltyper
* På sidan **leverantörsreskontratransaktioner** välj **åtgärder**, **funktioner**, **skicka kundremissa** via e-post efter bokföring av leverantörsbetalningar, för en av flera leverantörsreskontratransaktioner

## <a name="see-also"></a>Se även

[Betalningsförslag för lev.](payables-how-suggest-vendor-payments.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
