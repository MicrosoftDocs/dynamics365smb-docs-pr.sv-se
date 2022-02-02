---
title: Lägga ut legotillverkning för produktion
description: Det här avsnittet ger en utökad översikt över de utökade funktionen i Business Central inklusive produktionsgrupp och operationsföljd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 99000886
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 2b3ecc4ac84c5b3958d2ada97c104e92dced9ed2
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972729"
---
# <a name="subcontract-manufacturing"></a>Lägga ut legotillverkning för produktion

Legotillverkningsvalda operationer till leverantör är vanligt i många tillverkningsföretag. Legotillverkning kan vara sällan förekommande eller en integrerad del i alla produktionsprocesser.

[!INCLUDE[prod_short](includes/prod_short.md)] ger flera verktyg som kan användas för att hantera legotillverkning:  

- Produktionsgrupper med tilldelad leverantör: Med den här funktionen kan du upprätta en produktionsgrupp som är associerad med en leverantör (underleverantör). Detta kallas för en produktionsgrupp för legotillverkning. Du kan ange en produktionsgrupp för legotillverkning i en operationsföljd, vilket gör att du på ett enkelt sätt kan bearbeta legoaktiviteten. Dessutom kan kostnaden för operationen anges på operationsföljdsnivå eller produktionsgruppsnivå.  
- Produktionsgrupper kostnadsbaserade på enheter eller tid: Med den här funktionen kan du ange om kostnaderna som är associerade med produktionsgruppen baseras på produktionstiden eller en fast kostnad per enhet. Även om underleverantörer oftast använder en fast kostnad per enhet för att debitera kostnaden för tjänsten, kan båda alternativ hanteras i programmet (produktionstid och fast kostnad per enhet).  
- Legotillverkningskalkylark: Med den här funktionen kan du söka efter de produktionsorder som innehåller material som är klart att skickas till en underleverantör, och automatiskt skapa inköpsorder för legotillverkningsoperationer från verksamhetsföljder för produktionsorder. Inköpsorderkostnader bokförs automatiskt i produktionsordern under bokföringen av inköpsordern. Endast produktionsorder med statusen Släppt kan kommas åt och användas från ett legotillverkningsförslag.  

## <a name="subcontract-work-centers"></a>Produktionsgrupper för legotillverkning  
Produktionsgrupper för legotillverkning är inställda på samma sätt som vanliga produktionsgrupper med extra information. Dessa produktionsgrupper tilldelas till verksamhetsföljder på samma sätt som andra produktionsgrupper.  

### <a name="subcontract-work-center-fields"></a>Fält för produktionsgrupper för legotillverkning  
I fältet **Underleverantörsnr** anges produktionsgruppen som en produktionsgrupp för underkontrakt. I fältet kan du ange numret på den underleverantör som levererar till produktionsgruppen. Fältet kan användas för att hantera externa produktionsgrupper som tillverkar under kontrakt.  

Om du lägger ut arbete på legotillverkning hos en leverantör med olika taxor för varje process markerar du fältet **Specifik styckkostnad**. Då kan du lägga upp en kostnad på varje verksamhetsföljdsrad och på så sätt spara tid än om du i stället hade fått ange informationen på nytt på varje inköpsorder. Kostnaden på verksamhetsföljdsraden används i bearbetningen i stället för kostnaden i produktionsgruppens kostnadsfält. Om du aktiverar **Specifik styckkostnad** kan kostnader för leverantören beräknas utifrån verksamhetsföljdsoperationen.  

Om du lägger ut arbete på legotillverkning med en enda taxa per leverantör, lämnar du fältet **Specifik styckkostnad** tomt. Kostnaderna kommer att läggas upp när du fyller i fälten **Inköpspris**, **Indirekt kostnad %** och **Omkostnad**.  

### <a name="routings-that-use-subcontract-work-centers"></a>Operationsföljder som använder produktionsgrupper för underkontrakt  
Du kan använda produktionsgrupper för underkontrakt för operationer i verksamhetsföljder på samma sätt som vanliga produktionsorder.  

Du kan ställa in en verksamhetsföljd som använder en extern produktionsgrupp som standardverksamhetssteg. Du kan alternativt ändra verksamhetsföljden för en särskild produktionsorder så att en extern operation inkluderas. Detta kan vara bra att använda sig av i nödsituationer, till exempel när en server inte fungerar eller under en period med större arbetsbelastning när arbetet som normalt utförs internt måste läggas ut på en underleverantör.  

Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).  

## <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Beräkna legotillverkningskalkylark och skapa inköpsorder för underkontrakt  
När du har beräknat legotillverkningskalkylarket skapas relevant dokument, i det här fallet en inköpsorder.  

Sidan **Legotillverkningskalkylark** fungerar som **Planeringsförslag** genom att beräkna den nödvändiga leveransen, i inköpsordern för det här fallet, som du granskar i kalkylarket och skapa den med funktionen **Verkställ åtgärdsmeddelande**.  

> [!NOTE]  
>  Endast produktionsorder med statusen **Släppt** kan kommas åt och användas från ett legotillverkningskalkylark.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Beräkna legotillverkningskalkylark  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Legotillverkningsförslag** och väljer sedan relaterad länk.  
2.  Om du vill beräkna kalkylarket väljer du åtgärden **Beräkna kalkylark**.  
3.  På sidan **Beräkna utlego** ställer du in filter för de operationerna eller produktionsgrupperna där de utförs för att beräkna endast relevanta produktionsorder.  
4.  Välj knappen **OK**.  

    Granska raderna på sidan **legotillverkningsförslag**. Informationen i det här förslaget kommer från produktionsordern och operationsföljdsraderna för produktionsordern, och skickas vidare till inköpsordern när den skapas. Du kan ta bort en rad i legotillverkningsförslaget utan att påverka den ursprungliga informationen, precis som med andra förslag. Informationen visas på nytt nästa gång du kör funktionen **Beräkna utlego**.  

### <a name="to-create-the-subcontract-purchase-order"></a>Så här skapar du en inköpsorder för underkontrakt  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Legotillverkningsförslag** och väljer sedan relaterad länk.  
2.  Välj den **Verkställ åtgärdsmeddelande** åtgärd.  
3.  Markera fältet **Skriv ut inköpsorder** om du vill skriva inköpsordern när den skapas.  
4.  Välj knappen **OK**.  

Endast en inköpsorder skapas om alla legotillverkningsoperationer ska skickas till samma leverantör.  

Den kalkylarksrad som användes för att skapa en inköpsorder tas bort från kalkylarket. När en inköpsorder har skapats kommer den inte att visas i kalkylarket igen.  

## <a name="posting-subcontract-purchase-orders"></a>Bokföra inköpsorder för underkontrakt  
När du har skapat inköpsorder för underkontrakt kan du bokföra dessa. När ordern tas emot bokförs en kapacitetstransaktion i produktionsordern och när ordern faktureras bokförs den direkta kostnaden för inköpsordern i produktionsordern.  

## <a name="to-post-a-subcontract-purchase-order"></a>Så här bokför du en inköpsorder för underkontrakt:  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2.  Öppna den inköpsorder som skapades från legotillverkningskalkylarket.  

    På inköpsorderraderna ser du samma information som i kalkylarket. Fälten **Prod. Ordernr**, **Prod. Radnr**, **Operationsnr**, och **Prod.gruppsnr** fylls i automatiskt med information från den ursprungliga produktionsordern.  

3.  Välj åtgärden **Bokföra**.  

När inköpsordern bokförs som inlevererad bokförs en utflödesjournalrad automatiskt för produktionsordern. Detta gäller endast om legotillverkningsoperationen, är den sista operationen i verksamhetsföljden för produktionsordern.  

> [!CAUTION]  
>  Bokföra utflöde automatiskt för en pågående produktionsorder när underleverantörsartiklar tas emot kanske inte är önskvärt. Anledningar för det kan vara att det förväntade utflödeantalet som bokförs kan skilja sig från det faktiska antalet och att bokföringsdatumet för det automatiska utflödet är missvisande.  
>   
>  För att undvika att förväntade utdata för en produktionsorder bokförs när legotillverkningsinköp tas emot, kontrollera att legotillverkningsoperationen inte är den sista. Alternativt infogar du en ny sista åtgärd för det sista utflödesantalet.  

När inköpsordern faktureras bokförs inköpskostnaden för inköpsordern i produktionsordern.  

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]