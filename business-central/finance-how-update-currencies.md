---
title: Uppdatera valutakurser (innehåller video)
description: Lär dig hur du använder Business Central för att justera växelkurser för belopp i olika valutor.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 11/13/2023
ms.custom: bap-template
---
# Uppdatera valutakurser

Om du handlar i olika valutor måste du hålla koll på förändringarna i valutakurserna. [!INCLUDE [prod_short](includes/prod_short.md)] hjälper dig att hantera och uppdatera växelkurserna manuellt eller automatiskt och konfigurera en valutakurstjänst.

## Valutor

> [!TIP]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] kan du hitta realtidsinformation om valutakurser (FX) eller historiska kurser under termen valuta. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Du kan ange valutakoder i listan **Valutor**, inklusive extra information och inställningar som behövs för respektive valutakod. Mer information finns i [Valutor](finance-set-up-currencies.md#curr)

### Exempel på en transaktion med ingående valuta

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Valutakurser

Valutakurserna är det verktyg som används för att beräkna värdet i den lokala valutan (BVA) för respektive valutatransaktion. Sidan **Valutakurser** innehåller följande fält:

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Fr.o.m.-datum**|Det datum då valutakursen gällde.|  
|**Valutakod**|Valutakoden som är relaterad till den här valutakursen.|  
|**Relations- valutakod**|Om den här valutan är en del av en trepartsvalutaberäkning kan du ställa in den relaterade valutakoden här.|  
|**Valutakurs- belopp**|Valutakursbeloppet är den kurs som ska användas för den valutakod som är markerad på raden. Normalt 1 eller 100.|  
|**Relations- valutakurs belopp**|Det relationella valutakursbeloppet relaterar till den kurs som ska användas för den relationella valutakoden.|  
|**Justering valutakursbelopp**|Kursen för valutakoden som valts på raden för användning av batch-jobbet **Justera valutakurser**.|  
|**Relationellt justeringsvalutakursbelopp**|Kursen för valutakoden som valts på raden för användning av batch-jobbet **Justera valutakurser**.|  
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

## Justera valutakurser

Eftersom valutakurser ständigt fluktuerar måste du justera alternativa valutavärden med jämna mellanrum. Om du inte gör detta kan belopp som du har konverterat från utländska (eller andra) valutor och bokförts i redovisningen i lokal valuta bli felaktiga. Du måste också uppdatera dagliga transaktioner som bokförts innan du anger en daglig valutakurs.

Du kan använda batch-jobbet **Justera valutakurser** för att manuellt justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Batchjobbet kan också uppdatera andra rapporteringsvalutabelopp i redovisningstransaktioner.  

> [!TIP]
> Du kan använda en tjänst för att uppdatera bytesfrekvenser i systemet automatiskt. Mer information finns i [Så här konfigurerar du en valutakurstjänst](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service). Detta justerar emellertid inte bytesfrekvensen för redan publicerade transaktioner. Om du vill uppdatera bytesfrekvenser för publicerade poster använder du batchprojektet **Justera bytesfrekvenser**.

Du kan också ange hur justeringen hanterar dimensioner för icke-realiserade vinster och förluster genom att välja ett av följande alternativ i fältet **Dimensionsbokföring**:  

* **Källtransaktionsdimensioner**: Överför dimensionsvärden för redovisningstransaktioner för orealiserade vinster och förluster från den justerade transaktionen.  
* **Inga dimensioner**: Överför inte dimensionsvärden för icke-realiserade vinster och förluster till redovisningstransaktioner. [!INCLUDE [prod_short](includes/prod_short.md)] använder fortfarande standarddimensionsinställningar, till exempel **Kod obligatorisk**, **Samma kod** eller **Ingen kod**. Om källtransaktionerna har dimensionsvärden skapas transaktioner utan dimensionsvärden i justeringen.  
* **Redovisningskontodimensioner**: Överför dimensionsvärden från källtransaktionen för redovisningskontots dimensionsinställningar för orealiserade vinster och förluster till redovisningstransaktioner.

> [!NOTE]
> Om du vill använda förhandsgranskningsfunktionen måste du aktivera funktionen **Funktionsuppdatering: Aktivera användning av ny, utökningsbar valutakursjustering, inklusive funktionen för bokföringsgranskning** på sidan **[Funktionshantering](https://businesscentral.dynamics.com/?page=2610)**.

> [!IMPORTANT]
> På grund av lokala krav i Schweiz rekommenderar vi inte att du aktiverar **Funktionsuppdatering: Aktivera användning av ny utökningsbar valutakursjustering, inklusive bokföringsgranskning** i den schweiziska landsversionen (CH).

## Förhandsgranska effekten av en justering

Du kan förhandsgranska den effekt som en valutakursjustering har på bokföring innan du bokför, detta genom att välja åtgärden **Förhandsgranska bokföring** på begärandesidan i rapporten **Justera valutakurser** (rapport 596). På begärandesidan kan du ange vad som ska ingå i förhandsversionen:

* Få en detaljerad bokföring i redovisningen efter transaktion.
* Få en sammanfattad bokföring efter valuta. Välj bara fältet **Justera efter transaktion** i rapporten **Justering av valutakurs**.

### Påverkan på kunder och leverantörer

För kund- och leverantörskonton använder batchprojektet valutakursen som var giltig på det bokföringsdatum som angetts för batchprojektet för att justera valutan. I batchprojektet beräknas skillnaderna för enskilda valutasaldon och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster väntade** eller **Kursförluster befarade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt till redovisningens försäljnings-/inköpskonto.

Batch-jobbet behandlar alla öppna kundredovisningstransaktioner och leverantörstransaktioner. Om en valutakursdifferens föreligger i någon transaktion skapas en ny detaljerad kund- eller leverantörstransaktion av batch-jobbet. Den nya transaktionen återspeglar det justerade beloppet på kund- eller leverantörsreskontratransaktionen.

#### Dimensioner på kund- och leverantörsreskontratransaktioner

[!INCLUDE [prod_short](includes/prod_short.md)] tilldelar dimensioner från kund- eller leverantörsreskontratransaktionerna till justeringstransaktionerna och bokför justeringarna för respektive kombination av dimensionsvärden.

### Påverkan på bankkonton

För bankkonton justerar batchprojektet valutan efter valutakursen på det bokföringsdatum som angetts i batchprojektet. I batchprojektet beräknas skillnaderna för varje bankkonto med valutakod och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster konstaterade** eller **Kursförluster konstaterade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt på de redovisningsbankkonton som angetts i bankkontobokföringsmallarna. Batchprojektet beräknar en transaktion per valuta per bokföringsmall.

#### Dimensioner för bankkontotransaktioner

Justeringstransaktionerna för bankkontots redovisningskonto och för vinst-/förlustkontot tilldelas bankkontots standarddimensioner.

### Påverkan på redovisningskonton

Om du bokför i en alternativ rapporteringsvaluta kan batchprojektet skapa nya redovisningstransaktioner för valutajusteringar mellan lokal valuta och den alternativa rapporteringsvalutan. Batchjobbet beräknar skillnaderna för varje huvudbokpost. Det justerar redovisningstransaktionen enligt innehållet i fältet **Valutakursjustering** för varje redovisningskonto.

#### Dimensioner för redovisningskontotransaktioner

Justeringstransaktionerna tilldelas dimensioner från de redovisningskonton de bokförs på.

> [!Important]
> Innan du kan använda batchprojektet måste du ange de valutakurser som ska användas vid justering av de utländska valutasaldona. Du gör det med sidan **valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Konfigurera en valutakurstjänst

Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser. 

> [!NOTE]
> De flesta valutakurstjänster tillhandahåller data som är kompatibla med importförfarandet i [!INCLUDE[prod_short](includes/prod_short.md)]. Ibland har data emellertid formaterats annorlunda, och du måste då anpassa importen. Du kan använda ramverket för dataintegrering för att göra detta genom att lägga till din egen codeunit. Du behöver troligen lite hjälp från en utvecklare för att göra detta. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktivera **Aktiverad** för att aktivera tjänsten.

> [!NOTE]
> Följande video visar hur du ansluter till en valutakurstjänst med hjälp av Europeiska centralbanken som exempel. I det segment som beskriver hur man konfigurerar fältmappningar returnerar inställningen i kolumnen **Källa** för den **överordnade noden för valutakod** endast den valuta som hittas först. Inställningen bör vara `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## Uppdatera du valutakurser från en tjänst

Följ stegen för att uppdatera valutakurserna via en tjänst:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Valutor** och väljer sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

## Korrigera misstag

Då och då kan du behöva korrigera ett misstag i en betalningstransaktion som är förknippad med justeringar av vinster och förluster i utländsk valuta. Du kan använda åtgärden **Återför transaktion** på sidorna **Bankkontotransaktioner**, **Kundreskontratransaktioner** och **Lev.reskontratransaktioner** för att avaktivera och återställa betalningstransaktionen.

> [!NOTE]
> När du återkallar och återför en betalning för en post som hade valutaväxlingsjusteringar kopplade till den, bokför återkallelsen omvända poster för justeringarna. Du kanske måste köra valutakursjusteringen igen för att få rätt aktuellt saldo.

## Se även

## Se även

[Valutor i Business Central](finance-currencies.md)  
[Konfigurera valutor](finance-set-up-currencies.md)  
[Konfigurera en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
