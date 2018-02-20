---
title: "Så här lägger du ut legotillverkning för produktion | Microsoft Docs"
description: "När inköpsordern har skapats från legotillverkningsförslaget kan den bokföras."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2796da1b41569c8c950dc844fc31eaf4f0179efa
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="subcontract-manufacturing"></a>Lägga ut legotillverkning för produktion
Legotillverkningsvalda operationer till leverantör är vanligt i många tillverkningsföretag. Legotillverkning kan vara sällan förekommande eller en integrerad del i alla produktionsprocesser.

I programmet finns flera verktyg som kan användas för att hantera legotillverkning:  

- Produktionsgrupper med tilldelad leverantör: Med den här funktionen kan du upprätta en produktionsgrupp som är associerad med en leverantör (underleverantör). Detta kallas för en produktionsgrupp för legotillverkning. Du kan ange en produktionsgrupp för legotillverkning i en verksamhetsföljd, vilket gör att du på ett enkelt sätt kan bearbeta legoaktiviteten. Dessutom kan kostnaden för operationen anges på verksamhetsföljdsnivå eller produktionsgruppsnivå.  
- Produktionsgrupper kostnadsbaserade på enheter eller tid: Med den här funktionen kan du ange om kostnaderna som är associerade med produktionsgruppen baseras på produktionstiden eller en fast kostnad per enhet. Även om underleverantörer oftast använder en fast kostnad per enhet för att debitera kostnaden för tjänsten, kan båda alternativ hanteras i programmet (produktionstid och fast kostnad per enhet).  
- Legotillverkningsförslag: Med den här funktionen kan du söka efter de produktionsorder som innehåller material som är klart att skickas till en underleverantör, och automatiskt skapa inköpsorder för legotillverkningsoperationer från verksamhetsföljder för produktionsorder. Inköpsorderkostnader bokförs automatiskt i produktionsordern under bokföringen av inköpsordern. Endast produktionsorder med statusen Släppt kan kommas åt och användas från ett legotillverkningsförslag.  

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

## <a name="subcontracting-worksheet"></a>Legotillverkningsförslag  
När du har beräknat legotillverkningsförslaget skapas relevant dokument, i det här fallet en inköpsorder.  

# <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Beräkna legotillverkningsförslag och skapa inköpsorder för underkontrakt
Fönstret **Legotillverkningsförslag** fungerar som **Planeringsförslag** genom att beräkna den nödvändiga leveransen, i inköpsordern för det här fallet, som du granskar i förslaget och skapa den med funktionen **Verkställ åtgärdsmeddelande**.  

> [!NOTE]  
>  Endast produktionsorder med statusen **Släppt** kan kommas åt och användas från ett legotillverkningsförslag.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Beräkna legotillverkningsförslag  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Legotillverkningsförslag**, och välj sedan relaterad länk.  
2.  Om du vill beräkna förslaget väljer du åtgärden **Beräkna förslag**.  
3.  I fönstret **Beräkna utlego** ställer du in filter för de operationerna eller produktionsgrupperna där de utförs för att beräkna endast relevanta produktionsorder.  
4.  Välj **OK**.  

    Granska raderna i fönstret **legotillverkningsförslag**. Informationen i det här förslaget kommer från produktionsordern och verksamhetsföljdsraderna för produktionsordern, och skickas vidare till inköpsordern när den skapas. Du kan ta bort en rad i legotillverkningsförslaget utan att påverka den ursprungliga informationen, precis som med andra förslag. Informationen visas på nytt nästa gång du kör funktionen **Beräkna utlego**.  

### <a name="to-create-the-subcontract-purchase-order"></a>Så här skapar du en inköpsorder för underkontrakt  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Legotillverkningsförslag**, och välj sedan relaterad länk.  
2.  Välj **Verkställ åtgärdsmeddelande** i gruppen **Process** på fliken **Åtgärder**.  
3.  Markera fältet **Skriv ut inköpsorder** om du vill skriva inköpsordern när den skapas.  
4.  Välj knappen **OK**.  

Endast en inköpsorder skapas om alla legotillverkningsoperationer ska skickas till samma leverantör.  

Den förslagsrad som användes för att skapa en inköpsorder tas bort från förslaget. När en inköpsorder har skapats kommer den inte att visas i förslaget igen.  

## <a name="posting-subcontract-purchase-orders"></a>Bokföra inköpsorder för underkontrakt  
När du har skapat inköpsorder för underkontrakt kan du bokföra dessa. När ordern tas emot bokförs en kapacitetstransaktion i produktionsordern och när ordern faktureras bokförs den direkta kostnaden för inköpsordern i produktionsordern.  

När inköpsordern bokförs som inlevererad bokförs en utflödesjournalrad automatiskt för produktionsordern. Detta gäller endast om legotillverkningsoperationen, är den sista operationen i verksamhetsföljden för produktionsordern.  

> [!CAUTION]  
>  Bokföra utflöde automatiskt för en pågående produktionsorder när underleverantörsartiklar tas emot kanske inte är önskvärt. Anledningar för det kan vara att det förväntade utflödeantalet som bokförs kan skilja sig från det faktiska antalet och att bokföringsdatumet för det automatiska utflödet är missvisande.  
>   
>  För att undvika att förväntade utdata för en produktionsorder bokförs när legotillverkningsinköp tas emot, kontrollera att legotillverkningsoperationen inte är den sista. Alternativt infogar du en ny sista åtgärd för det sista utflödesantalet.

## <a name="to-post-a-subcontract-purchase-order"></a>Så här bokför du en inköpsorder för underkontrakt:  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsorder** och välj sedan relaterad länk.  
2.  Öppna den inköpsorder som skapades från legotillverkningsförslaget.  

    På inköpsorderraderna ser du samma information som i förslaget. Fälten **Prod. Ordernr**, **Prod. Radnr**, **Operationsnr**, och **Prod.gruppsnr** fylls i automatiskt med information från den ursprungliga produktionsordern.  

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
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

