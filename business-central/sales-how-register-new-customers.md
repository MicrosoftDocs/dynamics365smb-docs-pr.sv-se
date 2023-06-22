---
title: Registrera nya kunder genom att skapa ett kundkort (innehåller video)
description: Beskriver hur du skapar ett kundkort för att registrera information om varje ny kund eller klienten som du säljer till.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="register-new-customers" />Registrera nya kunder

Kunderna är källan till din inkomst. Du måste registrera varje kund som du säljer till som ett kundkort. Kundkort innehåller den information som behövs för att sälja produkter till kunden. Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).  

Innan du kan registrera nya kunder, måste du lägga upp olika försäljningskoder som du kan välja mellan, när du fyller i kundkort. Läs mer i [Konfigurera försäljning](sales-setup-sales.md).


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers" />Lägga till nya kunder

Du kan lägga till nya kunder manuellt, genom att fylla i fälten på sidan för **kundkort** eller använda mallar som innehåller fördefinierad information. Du kan t.ex. skapa mallar för olika typer av kundprofiler. När du använder mallar sparar du tid när du lägger till nya kunder och ser till att informationen är korrekt varje gång. 

Om du skapar:
* Flera mallar att använda med fler än en typ av kund du kan välja lämplig mall när du lägger till en kund.
* Endast en mall kommer den att användas för alla nya kunder. 

När du har skapat en mall kan du använda åtgärden **tillämpa mall** för att tillämpa den på en eller flera valda kunden. Om du vill skapa en mall fyller du i den information som du kan använda igen på **kundkortsidan** och sparar den som en mall. Mer information finns i [För att spara sidan kundkort som en mall](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template)

> [!TIP]
> Det kan vara användbart att anpassa sidan för **kundmall** när du skapar en mall. Du kanske till exempel vill lägga till fältet **Kreditgräns** i en mall. Mer information finns i avsnittet [Anpassa din arbetsyta](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan också skapa en kund från en kontakt. Mer information finns i avsnittet [Att skapa en kund, leverantör, anställd eller bankkonto från en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card" />SÅ här skapar du ett nytt kundkort

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Åtgärden **Priser och rabatter** har alternativ för att hantera specialpriser eller rabatter för kunden när en order uppfyller vissa kriterier. Exempel på sådana kriterier kan vara när de köper en viss artikel, beställer en minsta kvantitet eller köper före ett visst datum, till exempel när en kampanj avslutas. Läs mer på [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

Kunden är nu registrerad, och kundkortet är klart att användas i försäljningsdokument.  

### <a name="to-save-the-customer-card-as-a-template" />Om du vill spara kundkortet som en mall

Du kan använda detta kundkort som en mall när du skapar nya kundkort.

1. På sidan **Kundkort** väljer du åtgärden **Spara som mall**. Sidan **Kundmall** öppnas och visar kundkortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för kunden.
4. Ändra eller ange dimensionskoder som ska kopplas till nya kundkort som skapas med hjälp av mallen.  
5. Välj **OK** när du har slutfört den nya kundmallen.

Kundmallen läggs till listan över kundmallar, så att du kan använda det för att skapa nya kundkort.

## <a name="deleting-customer-cards" />Ta bort kundkort

Om du har bokfört en transaktion för en kund kan du inte ta bort kundkortet eftersom transaktionerna kan behövas för revision. Om du vill ta bort kundkort med transaktioner, kontaktar du din Microsoft-partner för att göra det via kod.  

## <a name="managing-credit-limits" />Hantera kreditlimits

Kreditlimits, saldobelopp och betalningsvillkor det möjligt för [!INCLUDE [prod_short](includes/prod_short.md)] att utfärda en kreditvarning och en varning om förfallet saldo när du registrerar en försäljningsorder. Dessutom kan du använda funktionerna för betalningspåminnelsevillkor och räntevillkor för att fakturera ränta och/eller ytterligare avgifter.  

Fältet **Kreditgräns** på ett kundkort anger det maximala belopp som du tillåter kunden att överskrida betalningssaldot med innan varningar utfärdas. När du sedan anger information i journaler, offerter, order och fakturor testar [!INCLUDE [prod_short](includes/prod_short.md)] försäljningshuvudet och enskilda försäljningsrader för att se om kreditlimiten har överskridits.

Du kan bokföra även om kreditlimiten överskrids. Om fältet är tomt finns det ingen kreditlimit för kunden.  

Du kan välja att inte ha varningar som talar om för dig att kundens kreditgräns har överskridits, och du kan ange vilka typer av varningar du vill se.

### <a name="to-specify-credit-limit-warnings" />Så här anger du varningar om kreditlimit

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.

2. På snabbfliken **Allmänt**, i fältet **Kreditvarningar**, väljer du relevant alternativ enligt beskrivet i följande tabell:

    |Alternativ| Beskrivning|
    |------|------------|
    |**Båda varningar**| Både fältet **Kreditgräns** och fältet **Förfallet saldo** på kundkortet är markerade, och en varning visas om kunden har överskridit sin kreditgräns eller har en förfallen skuld.|
    |**Kreditlimit**|Värdet i fältet **Credit Limit** på kundkortet jämförs med kundens saldo, och en varning visas om kundsaldot överskrider detta belopp.|
    |**Förfallet saldo**|Fältet **Förfallet saldo** på kundens kort markeras, och en varning visas om kunden har ett förfallet saldo.|
    |**Ingen varning**|Inga kreditvarningar visas angående kundens status.|

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics--business-central" />Se relaterad [Microsoft utbildning](/training/modules/trade-master-data-dynamics-365-business-central/).

## <a name="see-also" />Se även

[Definiera betalningssätt](finance-payment-methods.md)  
[Slå samman dubblettposter](sales-how-merge-duplicate-records.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Aktivera delleveranser med leveranstyp](sales-how-send-partial-shipments.md)  
[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Använd Online Map för att hitta platser och vägbeskrivningar](across-online-maps.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
