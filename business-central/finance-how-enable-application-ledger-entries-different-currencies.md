---
title: Tillämpa transaktioner i olika valutor
description: Du kan koppla transaktioner i olika valutor om du t. ex.. säljer i en valuta och får betalningen i en annan valuta.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.search.form: 148, 460
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9b2d1f66ff5b43832fada681320a99ef2b7c06bf
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971125"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Aktivera koppling av kundreskontratransaktioner till olika valutor

Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du koppla betalningen till inköpet.

Om du säljer i en valuta och får betalt i en annan kan du koppla betalningen till försäljningsfakturan.

Efterföljande proceduren beskriver hur du ställer in detta för leverantörsreskontratransaktioner på sidan **Inköpsinställningar**. Denna inställning liknar den för kundreskontratransaktioner på sidan **Försäljningsinställningar**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Så här aktiverar du koppling av leverantörsreskontratransaktioner i olika valutor

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inköpsinställningar** och väljer sedan relaterad länk.
2. I fältet **Koppling mellan valutor** markerar du ett av följande alternativ.

| Alternativ | Beskrivning |
| --- | --- |
| Ingen |Koppling mellan valutor är inte tillåten. |
| EMU |Koppling mellan EMU-valutor är tillåten. |
| Alla |Koppling mellan alla valutor är tillåten. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Så här skapar du redovisningskonton för avrundningsdifferenser vid valutakoppling

Om du kopplar transaktioner till olika valutor måste du ange de redovisningskonton som du vill bokföra avrundningsdifferenserna på.  

> [!NOTE]  
> Du måste skapa redovisningskonton innan du slutför uppgiften. Mer information finns i [Förstå redovisning och kontoplan](finance-general-ledger.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kundbokföringsmallar** och väljer sedan relaterad länk.  
2. Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.  
3. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörsbokföringsmallar** och väljer sedan relaterad länk.  
4. Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.  

## <a name="see-also"></a>Se även

[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]