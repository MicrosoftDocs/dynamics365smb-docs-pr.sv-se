---
title: "Så här kombinerar du leveranser på en enda faktura | Microsoft Docs"
description: "Om du vill fakturera mer än en leverans åt gången kan du använda funktionen för kombinerade leveranser."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a>Kombinera leveranser på en enda faktura
Om du vill fakturera mer än en leverans åt gången kan du använda funktionen för kombinerade leveranser.  

 Innan du kan skapa en kombinerad leverans måste mer än en leverans till samma kund och i samma valuta ha bokförts. Med andra ord måste du ha fyllt i minst två försäljningsorder och bokfört dem som levererade, men inte fakturerade. Om du vill kombinera utleveranser måste du markera kryssrutan **Samlingsfakturering** på snabbfliken **Leverans** på **Kund**-kortet.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Så här kombinerar du utleveranser manuellt på en enda faktura  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsfakturor** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).
3. I fältet **Förs.kundnr.** Ange den kund som ska få fakturan för de levererade artiklarna, i fältet.  
4. På snabbfliken **Rader** klickar du på åtgärden **Hämta utleveransrader**.  
5. Markera den leveransrad som ska inkluderas på fakturan:  

    - Markera alla rader och klicka på **OK** om du vill infoga alla rader.  
    - Markera raderna i fråga och klicka på **OK** om du vill infoga särskilda rader. Du kan använda CTRL-tangenten om du vill markera flera rader som inte är i följd.  

    Om du har markerat fel leveransrad eller om du vill börja om kan du ta bort raderna på fakturan och köra funktionen **Hämta leveransrader** på nytt.  
7. Om du vill bokföra fakturan väljer du åtgärden **Bokför**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Så här kombinerar du utleveranser automatiskt på en enda faktura  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Samlingsfakturering** och välj sedan relaterad länk. Beställningsfönstret för batch-jobbet  öppnas.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Markera kryssrutan **Bokför fakturor**.  
4.  Välj knappen **OK**.  

> [!NOTE]  
>  Fakturorna måste bokföras manuellt om du inte har markerat kryssrutan **Bokför fakturor** för batch-jobbet.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Så här tar du bort öppna försäljningsorder efter kombinerad utleveransbokföring 
När utleveranser kombineras på en faktura och bokförs, skapas en bokförd försäljningsfaktura för de fakturerade raderna. Innehållet i fältet **Fakturerat antal** på den ursprungliga avropsordern eller försäljningsordern uppdateras utifrån det fakturerade antalet.  

När du fakturerar leveranser på det här sättet finns de order som leveranserna bokfördes från kvar, även om de har levererats och fakturerats i sin helhet.   

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Ta bort fakturerade förs.order** och välj sedan länken.  
2. Fälten **Serienr** . vilka försäljningsorder som ska tas bort.  
3. Välj **OK**.  

Du kan också ta bort enskilda försäljningsorder manuellt.  

Upprepa steg 1 till 3 för alla andra berörda dokument, till exempel försäljningsavropsorder.

## <a name="see-also"></a>Se även  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

