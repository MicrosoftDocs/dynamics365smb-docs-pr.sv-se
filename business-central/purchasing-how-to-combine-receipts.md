---
title: Så här kombinerar du inleveranser | Microsoft Docs
description: Om du vill fakturera mer än en inleverans i taget kan du använda funktionen Kombinera inleveranser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 83b2e9c488a429603158d800e9c7e7b96be3bd8b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435115"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Kombinera inleveranser på en enda faktura

Om du vill fakturera mer än en inleverans i taget kan du använda funktionen **Kombinera inleveranser**.  

Innan du kan skapa en kombinerad inleverans måste du bokföra mer än en inköpsinleverans från samma leverantör i samma valuta. Med andra ord måste du ha fyllt i två eller flera inköpsorder och bokfört dem som inlevererade (men inte fakturerade).  

När inleveranser kombineras på en faktura och bokförs, skapas en bokförd inköpsfaktura för de fakturerade raderna. Fältet **Fakturerat antal** på den ursprungliga inköpsordern eller inköpsavropsordern uppdateras utifrån det fakturerade antalet. Emellertid tas det ursprungliga inköpsdokumentet inte bort, även om det är helt inlevererat och fakturerat, och därför måste du ta bort inköpsdokumentet.  

> [!NOTE]
> Det går inte att korrigera eller annullera den resulterande inköpsfakturan senare. Om du vill ändra en inköpsfaktura som skapas på det här sättet måste du använda inköpskreditnotor. Mer information finns i [Korrigera eller annullera obetalda inköpssfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Så här kombinerar du inleveranser:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).  
3. På snabbfliken **Rader** klickar du på åtgärden **Hämta inleveransrader**.  
4. Välj flera inleveransrader som du vill inkludera på fakturan.  

    Om du har valt en ogiltig rad, eller du måste börja om från början, behöver du bara ta bort raderna från fakturan och köra funktionen **Hämta inleveransrader** på nytt.  
5. Om du vill bokföra fakturan väljer du åtgärden **Bokför**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Så här tar du bort öppna inköpsorder efter kombinerad inleveransbokföring

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ta bort fakturerade inköpsorder** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Välj knappen **OK**.  

Du kan också ta bort enskilda order manuellt.

Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel inköpsavropsorder.

## <a name="see-also"></a>Se även

[Inköp](purchasing-manage-purchasing.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]