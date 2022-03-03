---
title: Uppdatera valutakurser (innehåller video)
description: Spåra belopp i olika valutor med hjälp av valutakoder och låt Business Central hjälpa dig att justera valutakurser för bokförda transaktioner med en extern tjänst.
author: SorenGP
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.search.form: 5, 118
ms.date: 02/17/2022
ms.author: edupont
ms.openlocfilehash: 04f96b269b842045c1a804f976ffddfd5348befc
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323272"
---
# <a name="update-currency-exchange-rates"></a>Uppdatera valutakurser

Eftersom företag verkar i fler länder/regioner blir det viktigt att de kan handla och rapportera ekonomisk information i fler än en valuta. Den lokala valutan (BVA) definieras på sidan **Redovisningsinställning** enligt beskrivningen i artikeln [Inställningar för finansiering](finance-setup-finance.md). När den lokala valutan (BVA) har definierats visas den som en tom valuta, så när fältet **Valuta** är tomt betyder det att valutan är BVA.  

Sedan måste du registrera valutakoder för varje valuta du använder om du köper eller säljer i andra valutor än den lokala valutan (BVA). Du kan även skapa bankkonton med hjälp av valutor. Du kan dock registrera redovisningstransaktioner i olika valutor, men redovisningstransaktionen bokförs alltid i lokal valuta (BVA).

> [!Important]
> Skapa inte den lokala valutakoden både i **Redovisningsinställning** och på sidan **Valutor**. Detta skapar förvirring mellan den tomma valutan och BVA-koden i valutatabellen, och bankkonton, kunder eller leverantörer kan av misstag skapas, en del med den tomma valutan och en del med BVA-koden.

Din redovisning ställs in för att använda den lokala valutan (BVA), men du kan ställa in den så att den använder en annan valuta med en tilldelad valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[prod_short](includes/prod_short.md)] registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion och för andra transaktioner, t. ex. momstransaktioner. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md). Den alternativa rapporteringsvalutan används oftast för att underlätta ekonomisk rapportering till ägare som finns i länder/regioner som använder andra valutor än den lokala valutan (BVA).  

> [!IMPORTANT]
> Om du vill använda en alternativ rapporteringsvaluta för ekonomisk rapportering måste du känna till begränsningarna. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).

> [!NOTE]  
> När du bokför i redovisning med hjälp av en valutakod, till exempel för att bokföra en utgift i en redovisningsjournal med en valutakod, konverteras transaktionen till BVA med hjälp av valutakursen för bokföringsdatumet. Redovisningstransaktionen kommer inte att innehålla information om vilken valuta som har använts, bara dess värde i BVA. Om du vill kunna spåra originalvalutan, till exempel för en faktura, måste du använda både försäljnings-och inköpsdokument samt bankkonton som lagrar information om valutakod för transaktionerna.

## <a name="currencies"></a>Valutor

> [!NOTE]  
> Om du söker efter realtidsinformation om valutakurser i utländsk valuta (FX) eller historiska kurser i [!INCLUDE[prod_short](includes/prod_short.md)] hittar du den som valuta. Förutom denna artikel, se [Konfigurera en Alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).

Du anger valutakoder i **valutorna**, inklusive extra information och inställningar som behövs för varje valutakod.

> [!TIP]
> Skapa valutor med den internationella ISO-koden som kod för att förenkla arbetet med valutan i framtiden.

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
|**Max. tillåten momsdifferens**|Det högsta belopp som tillåts för momsskillnader i den här valutan. Mer information finns i [Korrigera momsbelopp manuellt i försäljnings- och inköpsdokument](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|
|**Momsavrundningstyp**|Anger avrundningsmetoden för att korrigera momsbelopp manuellt i försäljnings- och inköpsdokument. Det här fältet kanske inte visas som standard. Den kan hämtas genom att anpassa sidan.|

### <a name="example-of-a-receivable-currency-transaction"></a>Exempel på en transaktion med ingående valuta

När du tar emot en faktura från ett företag i en utländsk valuta är det ganska enkelt att beräkna det lokala valutavärdet (BVA) på fakturan baserat på dagens valutakursbelopp. Fakturan levereras emellertid ofta med betalningsvillkor så att du kan försena betalningen till ett senare datum, vilket innebär en potentiellt annorlunda valutakurs. Det här problemet är i kombination med det faktum att bankens valutakurser alltid skiljer sig från de officiella valuta kurserna, vilket gör det omöjligt att förutsäga det exakta belopp i lokal valuta (BVA) som krävs för att täcka fakturan. Om fakturans förfallo datum gäller till nästa månad måste du kanske också revaluate beloppet i den lokala valutan (BVA) i slutet av månaden. Valuta justeringen är nödvändig eftersom det nya BVA-värdet som krävs för att täcka faktura beloppet kan vara ett annat, och företagets skuld till leverantören kan ha ändrats. Det nya beloppet i BVA kan vara högre eller lägre än det föregående beloppet och kommer därför att utgöra en vinst eller en förlust. Men eftersom fakturan ännu inte har betalats betraktas vinsten eller förlusten som *Orealiserad*. Senare betalas fakturan och banken har returnerat den faktiska valutakursen för betalningen. Det är inte förrän nu den *realiserade* vinsten eller förlusten beräknas. Den här orealiserade vinsten eller förlusten återförs sedan och den realiserade vinsten eller förlusten bokförs i stället.

I följande exempel inlevereras en faktura den 1 januari med valutabeloppet 1 000. När valutakursen är 1,123.

|Datum|Åtgärd|Valutabelopp|Dokumentkurs|BVA-belopp på dokument|Justeringskurs|Okonstaterat vinstbelopp|Betalningskurs|Konstaterat förlustbelopp|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fakturera**|1000|1,123|1123|||||
|1/31|**Justering**|1000||1125|1,125|2|||
|2/15|**Justeringsåterföring vid betalning**|1000||||-2|||
|2/15|**Betalning**|1000||1120|||1,120|-3|

I slutet av månaden utförs en valutajustering där den justerade valutakursen har angetts till 1,125, vilket utlöser en orealiserad vinst på 2.

Vid tidpunkten för betalningen visar den faktiska valutakurs som registrerats i banktransaktionen en valutakurs på 1,120.

Här finns en orealiserad transaktion som därför kommer att återföras tillsammans med betalningen.

Slutligen registreras betalningen och den faktiska förlusten bokförs i kontot för konstaterade förluster.

## <a name="available-currency-functions"></a>Tillgängliga valutafunktioner

I följande tabell anges viktiga åtgärder på sidan **Valutor**. En del av åtgärderna förklaras i nästa avsnitt.  

|Meny|Åtgärd|Beskrivning|
|-------------|--------------|------------------------------|
|**Bearbeta**|**Föreslå konton**|Använd konton från övriga valutor. De konton som används oftast kommer att infogas.|
||Ändra betalningstolerans|Ändra den maximala betalningstoleransen och betalningstoleransens procenttal och filtrera efter valuta. Mer information finns i [Betalningstolerans och kassarabattstolerans](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Valutakurser**|Visa uppdaterade valutakurser för valutorna du använder.|
||**Justera valutakurser**|Justera redovisnings-, kund-, leverantörs- och bankkontotransaktioner för att återspegla ett mer aktuellt saldo om valutakursen har ändrats sedan transaktionerna bokfördes.|
||**Valutakursjusteringsreg.**|Visa resultatet av körningen av batch-jobbet **Justera valutakurser**. En rad skapas för varje valuta eller varje kombination av valuta och bokföringsmall som tas med i justeringen.|
|**Valutakurstjänster**|**Valutakurstjänster**|Visa eller redigera inställningarna av tjänster som ställts in för att hämta uppdaterade valutakurser när du väljer åtgärden **Uppdatera valutakurser**.|
||**Uppdatera valutakurser**|Hämta de senaste valutakurserna från en tjänsteleverantör.|
|**Rapporter**|**Utländskt valutasaldo**|Visa saldon för alla kunder och leverantörer i både utländska valutor och i lokal valuta (BVA). Rapporten innehåller två saldon i BVA. Ett är det utländska valutasaldot konverterat till BVA med hjälp av valutakursen vid tidpunkten för transaktionen. Det andra är det utländska valutasaldot konverterat till BVA med hjälp av valutakursen på arbetsdagen.|

## <a name="exchange-rates"></a>Valutakurser

Valutakurserna är det verktyg som används för att beräkna värdet i den lokala valutan (BVA) för varje valutatransaktion. Sidan **Valutakurser** innehåller följande fält:

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Startdatum**|Det datum då valutakursen var effektuerad|  
|**Valutakod**|Valutakoden som är relaterad till den här valutakursen|  
|**Relationsvalutakod**|Om den här valutan är en del av en trepartsvalutaberäkning kan du ställa in den relaterade valutakoden här|  
|**Valutakursbelopp**|Valutakursbeloppet är den kurs som ska användas för den valutakod som är markerad på raden. Normalt 1 eller 100|  
|**Relationsvalutakursbelopp**|Det relationella valutakursbeloppet relaterar till den kurs som ska användas för den relationella valutakoden|  
|**Justeringsvalutakursbelopp**|Det justerade valutakursbeloppet är den kurs som ska användas för den valutakod som valts på raden för att använda batch-jobbet **Justera valutakurser**|  
|**Relationellt justeringsvalutakursbelopp**|Det relationella valutakursbeloppet är den kurs som ska användas för den valutakod som valts på raden för att använda batch-jobbet **Justera valutakurser**|  
|**Fast valutakursbelopp**|Anger om valutans växlingskurs ska kunna ändras på fakturor och journalrader.|  

I allmänhet används värdena för fälten **Valutakursbelopp** och **Relationellt valutakursbelopp** som standardvalutakurs på alla kund- och leverantörsreskontra som skapas framåt. Dokumentet tilldelas valutakursen enligt det aktuella arbetsdatumet.  

> [!Note]
> Den faktiska valutakursen kommer att beräknas med hjälp av följande formel:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Det justerade valutakursbeloppet eller det relationella justeringsvalutakursbeloppet kommer att användas för att uppdatera alla öppna bank-, kundreskontra- eller leverantörsreskontratransaktioner.  

> [!Note]
> Den faktiska valutakursen kommer att beräknas med hjälp av följande formel:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Justera valutakurser

Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats.

Batch-jobbet **Justera valutakurser** används för att manuellt justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner.  

> [!TIP]
> Du kan använda en tjänst för att uppdatera bytesfrekvenser i systemet automatiskt. Mer information finns i [Så här konfigurerar du en valutakurstjänst](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Detta justerar emellertid inte bytesfrekvensen för redan publicerade transaktioner. Om du vill uppdatera bytesfrekvenser för publicerade poster använder du batchjobbet **Justera bytesfrekvenser**.

### <a name="effect-on-customers-and-vendors"></a>Påverkan på kunder och leverantörer

För kund- och leverantörskonton justeras valutan med hjälp av valutakursen från det bokföringsdatum som angetts i batchjobbet. I batch-jobbet beräknas skillnaderna för enskilda valutasaldon och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster väntade** eller **Kursförluster befarade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt till redovisningens försäljnings-/inköpskonto.

Batch-jobbet behandlar alla öppna kundredovisningstransaktioner och leverantörstransaktioner. Om det finns valutakursdifferens i någon transaktion skapas i batch-jobbet en ny detaljerad kund- eller leverantörstransaktion som återger det justerade beloppet på kund- eller leverantörstransaktionen.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioner på kund-/leverantörstransaktioner

Justeringstransaktionerna tilldelas dimensioner från kund-/leverantörsreskontratransaktionerna, och justeringarna bokförs per kombination av dimensionsvärden.

### <a name="effect-on-bank-accounts"></a>Påverkan på bankkonton

För bankkonton justerar batchjobbet valutan efter valutakursen på det bokföringsdatum som angetts i batchjobbet. I batch-jobbet beräknas skillnaderna för varje bankkonto med valutakod och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster konstaterade** eller **Kursförluster konstaterade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt på de redovisningsbankkonton som angetts i bankkontobokföringsmallarna. Batch-jobbet beräknar en transaktion per valuta per bokföringsmall.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioner för bankkontotransaktioner

Justeringstransaktionerna för bankkontots redovisningskonto och för vinst-/förlustkontot tilldelas bankkontots standarddimensioner.

### <a name="effect-on-gl-accounts"></a>Påverkan på redovisningskonton
Om du bokför i alternativ rapporteringsvaluta kan du låta nya redovisningstransaktioner för valutajusteringar mellan BVA och den alternativa rapporteringsvalutan skapas i batch-jobbet. I batch-jobbet beräknas differenser för varje redovisningstransaktion och redovisningstransaktionen justeras enligt innehållet i fältet **Valutakursjustering** för varje redovisningskonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensioner för redovisningskontotransaktioner
Justeringstransaktionerna tilldelas dimensioner från de redovisningskonton de bokförs på.

> [!Important]
> Innan du kan använda batchjobbet måste du ange de valutakurser som ska användas vid justering av de utländska valutasaldona. Du gör det med sidan **valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser. 

> [!NOTE]
> De flesta valutakurstjänster tillhandahåller data som är kompatibla med importförfarandet i [!INCLUDE[prod_short](includes/prod_short.md)]. Ibland har datan emellertid formaterats annorlunda, och du måste då anpassa importen. Du kan använda ramverket för dataintegrering för att göra detta genom att lägga till din egen codeunit. Du behöver troligen lite hjälp från en utvecklare för att göra detta. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktivera **Aktiverad** för att aktivera tjänsten.

> [!NOTE]
> Följande video visar ett exempel på hur du ansluter till en valutakursservice med hjälp av Europeiska centralbanken som exempel. I det segment som beskriver hur man konfigurerar fältmappningar returnerar inställningen i kolumnen **Källa** för **den överordnade noden för valutakod** endast den valuta som hittas först. Inställningen bör vara `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Valutor** och väljer sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** på sidan **valutor** uppdateras med den senaste valutakursen.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Se även
[Ställa in en alternativ rapporteringsvaluta.](finance-how-setup-additional-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
