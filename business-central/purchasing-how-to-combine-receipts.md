---
title: Så här kombinerar du inleveranser | Microsoft Docs
description: Om du vill fakturera mer än en inleverans i taget kan du använda funktionen Kombinera inleveranser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5e1b04cc998319cc835b5dcc1547723c48be6763
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252890"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Kombinera inleveranser på en enda faktura
Om du vill fakturera mer än en inleverans i taget kan du använda funktionen **Kombinera inleveranser**.  

Innan du kan skapa en kombinerad inleverans måste du bokföra mer än en inköpsinleverans från samma leverantör i samma valuta. Med andra ord måste du ha fyllt i två eller flera inköpsorder och bokfört dem som inlevererade (men inte fakturerade).  

När inleveranser kombineras på en faktura och bokförs, skapas en bokförd inköpsfaktura för de fakturerade raderna. Fältet **Fakturerat antal** på den ursprungliga inköpsordern eller inköpsavropsordern uppdateras utifrån det fakturerade antalet. Emellertid tas det ursprungliga inköpsdokumentet inte bort, även om det är helt inlevererat och fakturerat, och därför måste du ta bort inköpsdokumentet.  

## <a name="to-combine-receipts"></a>Så här kombinerar du inleveranser:  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Inköpsfakturor** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).  
3. På snabbfliken **Rader** klickar du på åtgärden **Hämta inleveransrader**.  
4. Välj flera inleveransrader som du vill inkludera på fakturan.  

    Om du har valt en ogiltig rad, eller du måste börja om från början, behöver du bara ta bort raderna från fakturan och köra funktionen **Hämta inleveransrader** på nytt.  
5. Om du vill bokföra fakturan väljer du åtgärden **Bokför**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Så här tar du bort öppna inköpsorder efter kombinerad inleveransbokföring  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort fakturerade inköpsorder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Välj knappen **OK**.  

Du kan också ta bort enskilda order manuellt.

Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel inköpsavropsorder.

## <a name="see-also"></a>Se även  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
