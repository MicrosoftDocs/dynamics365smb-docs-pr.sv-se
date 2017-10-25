---
title: "Så här kombinerar du inleveranser | Microsoft Docs"
description: "Om du vill fakturera mer än en inleverans i taget kan du använda funktionen Kombinera inleveranser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9b3599a3f1a2cfc53d682a153eda8395e892305b
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-receipts-on-a-single-invoice"></a>Så här kombinerar du inleveranser på en enda faktura
Om du vill fakturera mer än en inleverans i taget kan du använda funktionen **Kombinera inleveranser**.  

Innan du kan skapa en kombinerad inleverans måste du bokföra mer än en inköpsinleverans från samma leverantör i samma valuta. Med andra ord måste du ha fyllt i två eller flera inköpsorder och bokfört dem som inlevererade (men inte fakturerade).  

När inleveranser kombineras på en faktura och bokförs, skapas en bokförd inköpsfaktura för de fakturerade raderna. Fältet **Fakturerat antal** på den ursprungliga inköpsordern eller inköpsavropsordern uppdateras utifrån det fakturerade antalet. Emellertid tas det ursprungliga inköpsdokumentet inte bort, även om det är helt inlevererat och fakturerat, och därför måste du ta bort inköpsdokumentet.  

## <a name="to-combine-receipts"></a>Så här kombinerar du inleveranser:  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsfakturor** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).  
3. På snabbfliken **Rader** klickar du på åtgärden **Hämta inleveransrader**.  
4. Välj flera inleveransrader som du vill inkludera på fakturan.  

    Om du har valt en ogiltig rad, eller du måste börja om från början, behöver du bara ta bort raderna från fakturan och köra funktionen **Hämta inleveransrader** på nytt.  
5. Om du vill bokföra fakturan väljer du åtgärden **Bokför**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Så här tar du bort öppna inköpsorder efter kombinerad inleveransbokföring  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Ta bort fakturerade inköpsorder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Välj knappen **OK**.  

Du kan också ta bort enskilda order manuellt.

Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel inköpsavropsorder.

## <a name="see-also"></a>Se även  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

