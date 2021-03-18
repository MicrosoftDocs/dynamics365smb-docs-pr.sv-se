---
title: Registrera nya kunder genom att skapa ett kundkort
description: Beskriver hur du skapar ett kundkort för att registrera information om varje ny kund eller klienten som du säljer till.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: d873c1546cebfccc6d2549b1de2b9d111589c553
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573432"
---
# <a name="register-new-customers"></a>Registrera nya kunder

Kunderna är källan till din inkomst. Du måste registrera varje kund som du säljer till som ett kundkort. Kundkort innehåller den information som behövs för att sälja produkter till kunden. Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).  

Innan du kan registrera nya kunder, måste du lägga upp olika försäljningskoder som du kan välja mellan, när du fyller i kundkort. Mer information finns i [Konfigurera försäljning](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Lägga till nya kunder

För att registrera en ny kund måste du fylla i ett kundkort. Du kan upprätta mallar för olika kundprofiler eller lägga till kunder utan mallar.  

> [!NOTE]  
> Om kundmallar finns för olika kundtyper, visas en sida när du skapar ett nytt kundkort där du kan välja en lämplig mall. Om endast en kundmall finns, då använder nya kundkort alltid den mallen.  

### <a name="to-create-a-new-customer-card"></a>SÅ här skapar du ett nytt kundkort

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.  
2. På sidan **Kunder** väljer du åtgärden **Ny**.

    Om endast en kundmall finns, då öppnas ett nytt kundkort med fält ifyllda med information från mallen.

    Om fler än en kundmall finns, öppnas en sida där du kan välja kundmall. I detta fall, följ nästa två steg.
3. Välj den mall som du vill använda för det nya kundkortet på sidan **Välj en mall för en ny kund**.
4. Välj **OK**. Ett nytt kundkort öppnas med ifyllda fält med information från mallen.  
5. Fortsätt att fylla i eller ändra fält på kundkortet vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

På snabbfliken **Försäljningspriser** ser du specialpriser eller rabatter som du beviljar för kunden om vissa villkor uppfylls, till exempel artikel, lägsta partistorlek eller slutdatum. Varje rad representerar ett speciellt pris eller radrabatt. Varje kolumn representerar ett kriterium som måste gälla för att garantera specialpriset som du anger i fältet **Enhetspris** eller radrabatten som du anger i fältet **Radrabatt %**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

Kunden är nu registrerad, och kundkortet är klart att användas i försäljningsdokument.

Om du vill använda detta kundkort som en mall när du skapar nya kundkort, så fortsätt med att spara den som en mall. Mer information finns i följande avsnitt:  

### <a name="to-save-the-customer-card-as-a-template"></a>Om du vill spara kundkortet som en mall

1. På sidan **Kundkort** väljer du åtgärden **Spara som mall**. Sidan **Kundmall** öppnas och visar kundkortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för kunden.
4. Ändra eller ange dimensionskoder som ska kopplas till nya kundkort som skapas med hjälp av mallen.  
5. Välj **OK** när du har slutfört den nya kundmallen.

Kundmallen läggs till listan över kundmallar, så att du kan använda det för att skapa nya kundkort.

## <a name="deleting-customer-cards"></a>Ta bort kundkort

Om du har bokfört en transaktion för en kund kan du inte ta bort kortet eftersom transaktionerna kan behövas för revision. Om du vill ta bort kundkort med transaktioner, kontaktar du din Microsoft-partner för att göra det via kod.  

## <a name="managing-credit-limits"></a>Hantera kreditlimits

Kreditlimits, saldobelopp och betalningsvillkor det möjligt för [!INCLUDE [prod_short](includes/prod_short.md)] att utfärda en kreditvarning och en varning om förfallet saldo när du registrerar en försäljningsorder.  Dessutom kan du använda funktionerna för betalningspåminnelsevillkor och räntevillkor för att fakturera ränta och/eller ytterligare avgifter.  

Fältet **Kreditgräns** på ett kundkort anger det maximala belopp som du tillåter kunden att överskrida betalningssaldot med innan varningar utfärdas. När du sedan anger information i journaler, offerter, order och fakturor testar [!INCLUDE [prod_short](includes/prod_short.md)] försäljningshuvudet och enskilda försäljningsrader för att se om kreditlimiten har överskridits.

Du kan bokföra även om kreditlimiten överskrids. Om fältet är tomt finns det ingen kreditlimit för kunden.  

Du kan välja att inte ha varningar som talar om för dig att kundens kreditlimit har överskridits, och du kan ange vilka typer av varningar du vill se.

### <a name="to-specify-credit-limit-warnings"></a>Så här anger du varningar om kreditlimit

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Försäljningsinställningar** och välj sedan relaterad länk.

2. På snabbfliken **Allmänt**, i fältet **Kreditvarningar**, väljer du relevant alternativ enligt beskrivet i följande tabell:

    |Alternativ| Beskrivning|
    |------|------------|
    |**Båda varningar**| Både fältet **Kreditlimit** och fältet **Förfallet saldo** på kundkortet är markerade, och en varning visas om kunden har överskridit sin kreditlimit eller om kunden har en förfallen skuld.|
    |**Kreditlimit**|Värdet i fältet **Credit Limit** på kundkortet jämförs med kundens saldo, och en varning visas om kundsaldot överskrider detta belopp.|
    |**Förfallet saldo**|Fältet **Förfallet saldo** på kundens kort markeras, och en varning visas om kunden har ett förfallet saldo.|
    |**Ingen varning**|Inga varningar visas om kundens status.|

## <a name="see-also"></a>Se även

[Definiera betalningssätt](finance-payment-methods.md)  
[Slå samman dubblettposter](sales-how-merge-duplicate-records.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]