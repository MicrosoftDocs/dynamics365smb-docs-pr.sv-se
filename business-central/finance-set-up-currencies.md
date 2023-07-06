---
title: Konfigurera valutor
description: Du måste konfigurera respektive valuta om du köper eller säljer i andra valutor än den lokala valutan (BVA) eller registrerar redovisningstransaktioner i olika valutor.
author: edupont04
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="set-up-currencies"></a><a name="set-up-currencies"></a><a name="set-up-currencies"></a>Konfigurera valutor

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Använd en extern tjänst för att hämta de senaste valutakurserna till listan **Valutor**. Mer information finns i [Så här konfigurerar du en valutakurstjänst](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="currencies"></a><a name="currencies"></a><a name="curr"></a>Valutor

I följande tabell beskrivs fälten i listan **Valutor**.

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Kod**|Identifierare för valutan.|
|**Beskrivning**|En fritextbeskrivning av valutan.|
|**ISO-kod**|Den internationella bokstavskoden till den valuta som anges i ISO 4217.|
|**Numerisk ISO-kod**|Den internationella numeriska referensen till den valuta som anges i ISO 4217.|
|**Valutakursdatum**|Det senaste faktiska valutakursdatumet.|
|**EMU-valuta**|Anger om valutan är en EMU-valuta (ekonomisk och monetär union), till exempel EUR.|
|**Kursvinst konstaterad redov.**|Kontot där den faktiska vinsten kommer att bokföras när du får betalningar för fordringar eller registrerar den faktiska valutakursen på betalningar till leverantörsreskontra. Exempel på en transaktion för en fordringsvaluta finns i exemplet under den här tabellen. |
|**Kursförlust konstaterad redov.**|Kontot där den faktiska förlusten kommer att bokföras när du får betalningar för fordringar eller registrerar den faktiska valutakursen på betalningar till leverantörsreskontra. Exempel på en transaktion för en fordringsvaluta finns i exemplet under den här tabellen. |
|**Kursvinst okonstaterad redov.**|Det konto där den teoretiska vinsten kommer att bokföras när du utför en valutajustering.|
|**Kursförlust okonstaterad redov.**|Det konto där den teoretiska förlusten kommer att bokföras när du utför en valutajustering.|
|**Precision av beloppavrundning**|Vissa valutor har andra format för fakturabelopp än vad som har definierats på sidan **Redovisningsinställning**. Om du ändrar precisionen av beloppavrundning för en valuta avrundas alla fakturabelopp i den valutan med den uppdaterade precisionen.|
|**Beloppdecimaler**|Vissa valutor har andra format för fakturabelopp än vad som har definierats på sidan **Redovisningsinställning**. Om du ändrar plats för beloppdecimaler för en valuta avrundas alla fakturabelopp i den valutan med de uppdaterade decimalerna|
|**Avrundningstyp faktura**|Anger vilken metod som ska användas om beloppen ska avrundas. Alternativen är **Närmsta**, **Uppåt** och **Nedåt**.|
|**Precision av avrundning av enhetsbelopp**|Vissa valutor har andra format för enhetsbelopp än vad som har definierats på sidan **Redovisningsinställning**. Om du ändrar precisionen av avrundning av enhetsbelopp för en valuta avrundas alla enhetsbelopp i den valutan med den uppdaterade precisionen.|
|**Decimalplatser för enhetsbelopp**|Vissa valutor har andra format för enhetsbelopp än vad som har definierats på sidan **Redovisningsinställning**. Om du ändrar plats för decimaler i enhetsbelopp för en valuta avrundas alla enhetsbelopp i den valutan med de uppdaterade decimalerna.|
|**Precision av programavrundning**|Anger storleken på det intervall som tillåts som avrundningsskillnad när du kopplar transaktioner i olika valutor till varandra.|
|**Avrundning konversation BVA. Debetkonto**|Anger konverteringsinformation som även måste innehålla ett debetkonto om du vill infoga korrigeringsrader för avrundningsdifferenser i redovisningsjournalerna med hjälp av åtgärden **Infoga rader för konv. BVA avr.**.|
|**Avrundning konversation BVA. Kreditkonto**|Anger konverteringsinformation som även måste innehålla ett kreditkonto om du vill infoga korrigeringsrader för avrundningsdifferenser i redovisningsjournalerna med hjälp av åtgärden **Infoga rader för konv. BVA avr.**.|
|**Senaste justeringsdatum**|Datumet för den senaste valutajusteringen.|
|**Senaste uppdateringsdatum**|Datumet för ändringen av valutainställningen.|
|**Betalningstolerans %**|Den angivna maximala betalningstoleransen i procent för valutan. Mer information finns i [Betalningstolerans och kassarabattstolerans](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Max.belopp betalningstolerans**|Det angivna maximala betalningstoleransbeloppet för valutan. Mer information finns i [Betalningstolerans och kassarabattstolerans](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Valutafaktor**|Specificerar sambandet mellan valutan och den lokala valutan med den aktuella växelkursen.|
|**Kursvinst konstaterad redov.**|Anger vilket redovisningskonto som används för att bokföra valutakursvinster vid valutakursjusteringar mellan den lokala valutan (BVA) och den alternativa rapporteringsvalutan. Kursvinsterna beräknas när batch-jobbet Justera valutakurser körs för att justera redovisningskonton. Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|
|**Kursförlust konstaterad redov.**|Anger vilket redovisningskonto som används för att bokföra valutakursförluster vid valutakursjusteringar mellan den lokala valutan (BVA) och den alternativa rapporteringsvalutan. Kursvinsterna beräknas när batch-jobbet Justera valutakurser körs för att justera redovisningskonton. Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|
|**Restvinster**|Anger det redovisningskonto som används för att bokföra kvarvarande vinstbelopp (avrundningsdifferenser) när en alternativ rapporteringsvaluta används i modulen Redovisning. Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|
|**Restförluster**|Anger det redovisningskonto som används för att bokföra kvarvarande förlustbelopp (avrundningsdifferenser) när en alternativ rapporteringsvaluta används i modulen Redovisning. Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|
|**Max. tillåten momsdifferens**|Det högsta belopp som tillåts för momsskillnader i den här valutan. Mer information finns i [Korrigera momsbelopp manuellt i försäljnings- och inköpsdokument](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|
|**Momsavrundningstyp**|Anger avrundningsmetoden för att korrigera momsbelopp manuellt i försäljnings- och inköpsdokument. Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|

### <a name="available-currency-functions"></a><a name="available-currency-functions"></a><a name="available-currency-functions"></a>Tillgängliga valutafunktioner

I följande tabell anges viktiga åtgärder på sidan **Valutor**.  

|Meny|Åtgärd|Beskrivning|
|-------------|--------------|------------------------------|
|**Bearbeta**|**Föreslå konton**|Använd konton från övriga valutor. De konton som används oftast kommer att infogas.|
||**Ändra betalningstolerans**|Ändra den maximala betalningstoleransen och betalningstoleransens procenttal och filtrera efter valuta. Mer information finns i [Betalningstolerans och kassarabattstolerans](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Valutakurser**|Visa uppdaterade valutakurser för valutorna du använder.|
||**Justera valutakurser**|Justera redovisnings-, kund-, leverantörs- och bankkontotransaktioner för att återspegla ett mer aktuellt saldo om valutakursen har ändrats sedan transaktionerna bokfördes.|
||**Valutakursjusteringsregister**|Visa resultatet av körningen av batch-jobbet **Justera valutakurser**. En rad skapas för varje valuta eller varje kombination av valuta och bokföringsmall som tas med i justeringen.|
|**Valutakurstjänster**|**Valutakurstjänster**|Visa eller redigera inställningarna av tjänster som ställts in för att hämta uppdaterade valutakurser när du väljer åtgärden **Uppdatera valutakurser**.|
||**Uppdatera valutakurser**|Hämta de senaste valutakurserna från en tjänsteleverantör.|
|**Rapporter**|**Utländskt valutasaldo**|Visa saldon för alla kunder och leverantörer i både utländska valutor och i lokal valuta (BVA). Rapporten innehåller två saldon i BVA. Ett är det utländska valutasaldot konverterat till BVA med hjälp av valutakursen vid tidpunkten för transaktionen. Det andra är det utländska valutasaldot konverterat till BVA med hjälp av valutakursen på arbetsdagen.|

## <a name="lcy-and-other-currencies"></a><a name="lcy-and-other-currencies"></a><a name="lcy-and-other-currencies"></a>BVA och andra valutor

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a><a name="rounding-currencies"></a><a name="rounding-currencies"></a>Avrunda valutor

När du hanterar valutor som inte använder decimaler och om du vill undvika onödiga decimaler i utländsk valuta kan du använda två olika avrundningsfunktioner:

- A-pris avrundning  

- Belopp avrundning  

Dessa funktioner kan användas oberoende av varandra eller i kombination. Dessa funktioner kan dessutom användas i samband med fakturaavrundning.

I motsats till fakturaavrundningsfunktionerna, påverkar funktionen A-pris avrundning och Belopp avrundning bara belopp i utländsk valuta - inte motsvarande belopp i BVA. Dessa två funktioner leder inte till några bokföringar på redovisningskontona. Därför behöver inga redovisningskonton anges i bokföringsmallar eller på andra ställen.

### <a name="unit-amount-rounding"></a><a name="unit-amount-rounding"></a><a name="unit-amount-rounding"></a>Enhetspris-avrundning

Funktionen Enhetspris-avrundning styr hur försäljningspriser för artiklar och resurser i utländsk valuta rundas av på försäljnings- och inköpsrader. Du måste ange reglerna för respektive valuta separat, i fältet **Enhetspris-avrundning** i listan **Valutor**.

Funktionen Enhetspris-avrundning används automatiskt varje gång du registrerar ett artikel- eller resursnummer på en försäljningsrad. Om fakturan gäller en kund med en valutakod, konverteras artikel- eller resurspriset till kundens valuta. Priset avrundas enligt Enhetspris-avrundning för valutan.

### <a name="amount-rounding"></a><a name="amount-rounding"></a><a name="amount-rounding"></a>Beloppavrundning

Funktionen Beloppsavrundning styr hur belopp i utländsk valuta rundas av på redovisningsjournalrader, försäljningsrader och inköpsrader. Du måste ange reglerna för respektive valuta separat, i fältet **Beloppsavrundning** i listan **Valutor**.

Belopp i utländsk valuta avrundas när du fyller i och bokför redovisningsjournalrader, försäljningsrader och inköpsrader.

## <a name="exchange-rates"></a><a name="exchange-rates"></a><a name="exchange-rates"></a>Valutakurser

Du kan registrera valutakurser för varje utländsk valuta och ange vilka datum som valutakurserna gäller från. Du kan t.ex. ange dagliga, månatliga eller kvartalsvisa valutakurser för respektive utländsk valuta.

Du kan lagra historiska valutakurser på sidan **Valutakurser** som referens. När du behöver uppdatera valutakurserna kan du använda knappen **Uppdatera valutakurser** för att visa de senaste valutakurserna från en extern tjänsteleverantör.

## <a name="general-ledger-accounts"></a><a name="general-ledger-accounts"></a><a name="general-ledger-accounts"></a>Redovisningskonton

Du kan inte koppla valutakoder till redovisningskonton eftersom belopp på redovisningskonton anges i BVA. Om du har ett banklån i USD och gör insättningar på ett bankkonto i SEK, kan du hålla ordning på dessa konton genom att skapa bankkonton i både USD och SEK. Med bokföringsmallar kan du koppla kontona till relevanta redovisningskonton. I redovisningen visas värdet på beloppen i BVA.

Du kan registrera en valutakod på en redovisningsjournalrad och bokföra raden på ett redovisningskonto. Relevant valutakurs används för att konvertera beloppet till BVA innan det bokförs på redovisningskontot.  

## <a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a>Exempel på en transaktion med ingående valuta

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/currencies-exchange-rates-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Uppdatera valutakurser](finance-how-update-currencies.md)  
[Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
