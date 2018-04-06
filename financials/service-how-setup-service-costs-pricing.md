---
title: "Definiera prissättning och kostnader för service | Microsoft Docs"
description: "Så här: registrera prissättning och alternativa kostnader för service"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 151b63b0f68a6605ae5c935f2331803277766452
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-pricing-and-additional-costs-for-services"></a>Registrera prissättning och alternativa kostnader för tjänster
Med prissättningsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du göra inställningar i och anpassa programmet så att du tillämpar och justerar priser för serviceartiklar, reparationer och order. Dessa beslut om prissättning överförs sedan till faktureringsprocessen.  
  
Om det behövs kan du skapa prisgrupper och mappa dem till specifika tidsperioder, kunder eller valutor. Du kan lägga upp fast, minsta eller högsta pris beroende på servicekontrakten som du har med kunderna. När du har justerat priserna kan du visa och godkänna ändringarna innan du sparar dem i redovisningen.  

## <a name="to-set-up-a-service-price-group"></a>Så här skapar du en serviceprisgrupp
Du kan lägga upp grupper med serviceartiklar om du vill ha samma speciella serviceprissättning. Du tilldelar serviceprisgrupper till serviceartiklar på serviceartikelrader. Du kan även tilldela serviceprisgrupper till serviceartikelgrupper.  

1. Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Serviceprisgrupper** och välj sedan relaterad länk.  
2. Skapa en ny serviceprisgrupp.  
3. Fyll i fälten **Kod** och **Beskrivning**.  
4. Välj åtgärden **Installation**.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Fälten **Justeringstyp** och **Belopp** samarbetar för att ange om denna justering gäller ett fast belopp, eller bara gäller när det totala servicepriset överskrider eller är lägre än det belopp som anges i fältet **Belopp**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Så här skapar du serviceprisjusteringsgrupper  
Du kan ställa in prisjusteringsgrupper för att justera servicepriset för serviceartiklar. skapa en prisjusteringsgrupp som justerar priset för frakt eller reservdelar.  
  
1. Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Serviceprisgrupper** och välj sedan relaterad länk.  
2. Skapa en ny serviceprisjusteringsgrupp.  
3. Fyll i fälten **Kod** och **Beskrivning**.  
4. I fältet **Typ** anger du den transaktionstyp som du vill justera.  
  
    * Om du vill justera endast en specifik post, anger du numret på transaktionen i fältet **nr.** . Om du låter det här fältet vara tomt justerar justeringsgruppen ALLA poster av den typ som definierats i fältet **Radtyp**.  
    * Om du vill justera servicepriser som bara gäller en specifik service, fyller du i fältet **arbetstyp**. Om du låter det här fältet vara tomt ignoreras det.  
  
5. Du kan ge en kort beskrivning av serviceprisjusteringen i fältet **Beskrivning**.  
6. Om du vill justera servicepriser relaterade till bara en specifik produktbokföringsmall, fyller du i fältet **Produktbokföringsmall**.

> [!Tip]
> Du kan välja **uppgifter** för att lägga till ytterligare information om justeringsgruppen. Du kan till exempel ange vilken artikel som tillhör serviceprisjusteringsgruppen och om det är en artikel, en resurs, en resursgrupp eller en serviceavgift.  

## <a name="to-set-up-additional-costs-for-services"></a>Så här: registrera alternativa kostnader för tjänster
När du arbetar med serviceartiklar och serviceorder kanske du behöver registrera ytterligare kostnader, till exempel resekostnader för vissa service zoner eller uppstartskostnader. När du skapar en serviceorder kan du infoga kostnaderna och en rad med typen **kostnad** läggs till i ordern. Om du vill koppla kostnader till alla serviceorder kan du ställa in standardkostnaden. Till exempel om du alltid vill använda en uppstartskostnad.
  
### <a name="to-set-up-service-costs"></a>Så här skapar du servicekostnader:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Servicekostnader** och välj sedan relaterad länk. 
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Ange standardkostnaden för serviceorder
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **serviceinställningar** och välj sedan relaterad länk. 
2. I fältet **Tjänsteorder uppstartskostnad**, välj lämplig servicekostnad.

## <a name="see-also"></a>Se även
[Ställa in tjänstehantering](service-setup-service.md)  
[Servicehantering](service-service.md)  

