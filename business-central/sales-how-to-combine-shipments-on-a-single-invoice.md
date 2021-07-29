---
title: Så här kombinerar du leveranser på en enda faktura | Microsoft Docs
description: Om du vill fakturera mer än en leverans åt gången kan du använda funktionen för kombinerade leveranser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1465ce4baadec43d28731dab50870af3c10bd77e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442731"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Kombinera leveranser på en enda faktura
Om du vill fakturera mer än en leverans åt gången kan du använda funktionen för kombinerade leveranser.  

Innan du kan skapa en kombinerad leverans måste mer än en leverans till samma kund och i samma valuta ha bokförts. Med andra ord måste du ha skapat minst två försäljningsorder och bokfört dem som levererade, men inte fakturerade. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Så här kombinerar du utleveranser manuellt på en enda faktura  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).
3. I fältet **Förs.kundnr.** Ange den kund som ska få fakturan för de levererade artiklarna, i fältet.  
4. På snabbfliken **Rader** klickar du på åtgärden **Hämta utleveransrader**.  
5. Markera den leveransrad som ska inkluderas på fakturan:  

    - Markera alla rader och klicka på **OK** om du vill infoga alla rader.  
    - Markera raderna i fråga och klicka på **OK** om du vill infoga särskilda rader. Du kan använda CTRL-tangenten om du vill markera flera rader som inte är i följd.  

    Om du har markerat fel leveransrad eller om du vill börja om kan du ta bort raderna på fakturan och köra funktionen **Hämta leveransrader** på nytt.  
7. Om du vill bokföra fakturan väljer du åtgärden **Bokför**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Så här kombinerar du utleveranser automatiskt på en enda faktura  
[!INCLUDE[prod_short](includes/prod_short.md)] väljer endast de försäljningsorder där **Kombinera leveranser** har valts. 

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kombinera leveranser** och väljer sedan relaterad länk. Sidan för begäran om batch-jobb öppnas.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Markera kryssrutan **Bokför fakturor**.  
4. Välj **OK**.  

> [!NOTE]  
>  Fakturorna måste bokföras manuellt om du inte har markerat kryssrutan **Bokför fakturor** för batch-jobbet.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Så här tar du bort öppna försäljningsorder efter kombinerad utleveransbokföring 
När utleveranser kombineras på en faktura och bokförs, skapas en bokförd försäljningsfaktura för de fakturerade raderna. Innehållet i fältet **Fakturerat antal** på den ursprungliga avropsordern eller försäljningsordern uppdateras utifrån det fakturerade antalet.  

När du fakturerar leveranser på det här sättet finns de order som leveranserna bokfördes från kvar, även om de har levererats och fakturerats i sin helhet.   

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ta bort fakturerade försäljningsorder** och väljer sedan länken.  
2. Fälten **Serienr** . vilka försäljningsorder som ska tas bort.  
3. Välj **OK**.  

Du kan också ta bort enskilda försäljningsorder manuellt.  

Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel försäljningsavropsorder.

## <a name="see-also"></a>Se även  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]