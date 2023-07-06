---
title: Uppdatera valutakurser (innehåller video)
description: Om du spårar belopp i olika valutor kan du låta Business Central hjälpa dig att justera valutakurser för bokförda transaktioner med en extern tjänst.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates"></a><a name="update-currency-exchange-rates"></a><a name="update-currency-exchange-rates"></a>Uppdatera valutakurser

Du kan definiera olika valutor i [!INCLUDE [prod_short](includes/prod_short.md)], till exempel om du gör affärer i andra valutor än den lokala valutan. För att hjälpa dig att hålla reda på förändringar i valutakurserna kan du sedan hantera valutorna manuellt, eller också ställa in en tjänst för valutakurs.

## <a name="currencies"></a><a name="currencies"></a><a name="currencies"></a>Valutor

> [!TIP]  
> Om du söker efter realtidsinformation om valutakurser i utländsk valuta (FX) eller historiska kurser i [!INCLUDE[prod_short](includes/prod_short.md)], hittar du den som "valuta". Förutom denna artikel, se även [Konfigurera en Alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Du anger valutakoder i listan **Valutor**, inklusive extra information och inställningar som behövs för respektive valutakod. Mer information finns i [Valutor](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a>Exempel på en transaktion med ingående valuta

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a><a name="exchange-rates"></a><a name="exchange-rates"></a>Valutakurser

Valutakurserna är det verktyg som används för att beräkna värdet i den lokala valutan (BVA) för respektive valutatransaktion. Sidan **Valutakurser** innehåller följande fält:

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

## <a name="adjusting-exchange-rates"></a><a name="adjusting-exchange-rates"></a><a name="adjusting-exchange-rates"></a>Justera valutakurser

Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats.

Batch-jobbet **Justera valutakurser** används för att manuellt justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner.  

> [!TIP]
> Du kan använda en tjänst för att uppdatera bytesfrekvenser i systemet automatiskt. Mer information finns i [Så här konfigurerar du en valutakurstjänst](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Detta justerar emellertid inte bytesfrekvensen för redan publicerade transaktioner. Om du vill uppdatera bytesfrekvenser för publicerade poster använder du batchjobbet **Justera bytesfrekvenser**.

Du kan förhandsgranska den effekt som en justering har för att bokföra innan du bokför genom att klicka på **Förhandsgranska** på sidan **Justera valutakurser**. Du kan också välja om redovisnings bokföringen ska vara detaljerad (per transaktion) eller summerad (per valuta) genom att välja **summera transaktioner**. Du kan också ange hur dimensioner ska hanteras för orealiserade vinster och förluster genom att välja ett av följande alternativ i fältet **överföringsdimensionsvärden**:  

- **Källtransaktionen**: redovisningstransaktioner för orealiserade vinster och förluster kommer att ha dimensions värden överförda från den justerade transaktionen.
- **Per redovisningskonto**: redovisningstransaktioner för orealiserade vinster och förluster kommer att ha dimensionsvärden som överförs från redovisningskontot för orealiserade vinster och förluster i dimensionsinställningar.
- **Ingen överföring**: redovisningstransaktioner för orealiserade vinster och förluster saknar dimensionsvärden.

### <a name="effect-on-customers-and-vendors"></a><a name="effect-on-customers-and-vendors"></a><a name="effect-on-customers-and-vendors"></a>Påverkan på kunder och leverantörer

För kund- och leverantörskonton justeras valutan med hjälp av valutakursen från det bokföringsdatum som angetts i batchjobbet. I batch-jobbet beräknas skillnaderna för enskilda valutasaldon och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster väntade** eller **Kursförluster befarade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt till redovisningens försäljnings-/inköpskonto.

Batch-jobbet behandlar alla öppna kundredovisningstransaktioner och leverantörstransaktioner. Om det finns valutakursdifferens i någon transaktion skapas i batch-jobbet en ny detaljerad kund- eller leverantörstransaktion som återger det justerade beloppet på kund- eller leverantörstransaktionen.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a><a name="dimensions-on-customer-and-vendor-ledger-entries"></a><a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioner på kund-/leverantörstransaktioner

Justeringstransaktionerna tilldelas dimensioner från kund-/leverantörsreskontratransaktionerna, och justeringarna bokförs per kombination av dimensionsvärden.

### <a name="effect-on-bank-accounts"></a><a name="effect-on-bank-accounts"></a><a name="effect-on-bank-accounts"></a>Påverkan på bankkonton

För bankkonton justerar batchjobbet valutan efter valutakursen på det bokföringsdatum som angetts i batchjobbet. I batch-jobbet beräknas skillnaderna för varje bankkonto med valutakod och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster konstaterade** eller **Kursförluster konstaterade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt på de redovisningsbankkonton som angetts i bankkontobokföringsmallarna. Batch-jobbet beräknar en transaktion per valuta per bokföringsmall.

#### <a name="dimensions-on-bank-account-entries"></a><a name="dimensions-on-bank-account-entries"></a><a name="dimensions-on-bank-account-entries"></a>Dimensioner för bankkontotransaktioner

Justeringstransaktionerna för bankkontots redovisningskonto och för vinst-/förlustkontot tilldelas bankkontots standarddimensioner.

### <a name="effect-on-gl-accounts"></a><a name="effect-on-gl-accounts"></a><a name="effect-on-gl-accounts"></a>Påverkan på redovisningskonton
Om du bokför i alternativ rapporteringsvaluta kan du låta nya redovisningstransaktioner för valutajusteringar mellan BVA och den alternativa rapporteringsvalutan skapas i batch-jobbet. I batch-jobbet beräknas differenser för varje redovisningstransaktion och redovisningstransaktionen justeras enligt innehållet i fältet **Valutakursjustering** för varje redovisningskonto.

##### <a name="dimensions-on-gl-account-entries"></a><a name="dimensions-on-gl-account-entries"></a><a name="dimensions-on-gl-account-entries"></a>Dimensioner för redovisningskontotransaktioner
Justeringstransaktionerna tilldelas dimensioner från de redovisningskonton de bokförs på.

> [!Important]
> Innan du kan använda batchjobbet måste du ange de valutakurser som ska användas vid justering av de utländska valutasaldona. Du gör det med sidan **valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a><a name="to-set-up-a-currency-exchange-rate-service"></a><a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser. 

> [!NOTE]
> De flesta valutakurstjänster tillhandahåller data som är kompatibla med importförfarandet i [!INCLUDE[prod_short](includes/prod_short.md)]. Ibland har datan emellertid formaterats annorlunda, och du måste då anpassa importen. Du kan använda ramverket för dataintegrering för att göra detta genom att lägga till din egen codeunit. Du behöver troligen lite hjälp från en utvecklare för att göra detta. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktivera **Aktiverad** för att aktivera tjänsten.

> [!NOTE]
> Följande video visar ett exempel på hur du ansluter till en valutakursservice med hjälp av Europeiska centralbanken som exempel. I det segment som beskriver hur man konfigurerar fältmappningar returnerar inställningen i kolumnen **Källa** för **den överordnade noden för valutakod** endast den valuta som hittas först. Inställningen bör vara `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a><a name="to-update-currency-exchange-rates-through-a-service"></a><a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Valutor** och väljer sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** på sidan **valutor** uppdateras med den senaste valutakursen.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Valutor i Business Central](finance-currencies.md)  
[Konfigurera valutor](finance-set-up-currencies.md)  
[Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
