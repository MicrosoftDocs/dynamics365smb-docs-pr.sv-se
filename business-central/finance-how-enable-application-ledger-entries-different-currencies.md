---
title: Tillämpa transaktioner i olika valutor
description: Du kan koppla transaktioner i olika valutor om du t. ex.. säljer i en valuta och får betalningen i en annan valuta.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.search.form: 148, 460, 25
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ec081740ff45dc018d975f6d84deae4aae907cb
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078706"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Aktivera koppling av kundreskontratransaktioner till olika valutor

Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du koppla betalningen till inköpet.

Om du säljer i en valuta och får betalt i en annan kan du koppla betalningen till försäljningsfakturan.

Efterföljande proceduren beskriver hur du ställer in detta för leverantörsreskontratransaktioner på sidan **Inköpsinställningar**. Denna inställning liknar den för kundreskontratransaktioner på sidan **Försäljningsinställningar**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Så här aktiverar du koppling av leverantörsreskontratransaktioner i olika valutor

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inköpsinställningar** och väljer sedan relaterad länk.
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

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kundbokföringsmallar** och väljer sedan relaterad länk.  
2. Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.  
3. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörsbokföringsmallar** och väljer sedan relaterad länk.  
4. Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/process-foreign-currency-payments-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]