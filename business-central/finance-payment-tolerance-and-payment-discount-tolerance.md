---
title: Betalningstolerans och kassarabattstolerans
description: Den här artikeln förklarar hur du ställer in betalningstolerans för att stänga en faktura när betalningen inte helt täcker fakturabeloppet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '118, 314, 395'
ms.date: 04/03/2023
ms.author: edupont
---
# Arbeta med betalningstoleranser och kassarabattstoleranser

Du kan skapa betalningstolerans för att avsluta en faktura, när betalningen inte täcker hela beloppet på fakturan. Betalningstoleranser används t. ex. vanligtvis för små belopp som skulle kosta mer för att korrigeras än att bara acceptera. Du kan ställa in betalningstolerans (rabatt) när du ska bevilja en kassarabatt efter att kassarabattsdatumet har passerat.  

Du kan använda betalningstolerans så att alla utestående belopp anger ett maximum som medger betalningstolerans. Om betalningstoleransen uppfylls analyseras betalningsbeloppet. Om beloppet är en underbetalning stängs det utestående beloppet helt av underbetalningen. En detaljerad redovisningstransaktion har bokförts på betalningstransaktionen så att det inte finns något belopp kvar på fakturaposten. Om beloppet är en överbetalning bokförs en ny detaljerad reskontratransaktion på betalningstransaktionen så att det inte finns något belopp kvar på betalningstransaktionen.

Du kan använda kassarabattstolerans så att om du godkänner en kassarabatt efter kassarabattsdatumet, bokförs den alltid på kontot för kassarabatt eller kontot för betalningstolerans.

## Använda betalningstolerans på flera dokument

Ett enskilt dokument har samma betalningstolerans oavsett om det används som det är eller tillsammans med andra dokument. Godkännande av en sen kassarabatt, när du kopplar betalningstolerans till flera dokument sker automatiskt för varje dokument där följande regel gäller:  

*kassarabattsdatum < betalningsdatum för fokustransaktionen <= betalningstoleransdatum*  

Denna regel gäller även när du vill bestämma om du vill visa varningar när du kopplar betalningstolerans till flera dokument. Varningen för kassarabattstoleransen visas för varje transaktion som uppfyller villkoren. Mer information finns i avsnittet [exempel 2 – toleransberäkningar för flera dokument](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Du kan välja att visa ett varningsmeddelande som baseras på olika toleranssituationer.  

- Den första varningstexten gäller kassarabattoleransen. Du får information om att du kan godkänna en sen kassarabatt. Du kan sedan välja att godkänna toleransen för rabattdatumet.  
- Den andra varningstexten gäller betalningstoleransen. Du informeras om att alla transaktioner kan stängas eftersom skillnaden ligger inom den totala betalningstoleransen för transaktionerna. Du kan sedan välja att godkänna toleransen för betalningsbeloppet.

> [!NOTE]
> Om du aktiverar varningsmeddelandet kan du välja hur betalningar som ligger inom toleransen ska behandlas. Om du inte aktiverar meddelandet och en toleransnivå anges kommer fakturor med belopp inom toleransen automatiskt att stängas och du kan inte välja att lämna det återstående beloppet. 

Mer information finns i [aktivera eller inaktivera betalningstoleransvarningar](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## Så här lägger du upp toleranser

Tolerans på dagar och belopp gör att du kan stänga en faktura trots att betalningen inte helt täcker beloppet på fakturan. Till exempel på grund av att förfallodatumet för kassa rabatten överskrids, har varor dragits av eller på grund av ett mindre fel. Det gäller även återbetalningar och kreditnotor.  

Du lägger upp toleransen genom att lägga upp olika toleranskonton, ange bokföringsmetoder för både kassarabattstolerans och betalningstolerans samt köra batch-jobbet **Ändra betalningstolerans**.  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Bokföringsinställningar** och välj sedan relaterad länk.  
2. Öppna sidan **Bokföringsinställningar**. Lägg upp ett debet- och ett kreditkonto för försäljningsbetalningstolerans och ett debet- och ett kreditkonto för inköpsbetalningstolerans.  
3. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kundbokföringsmallar** och väljer sedan relaterad länk.    
4. Öppna sidan **Kundbokföringsmallar**. Lägg upp ett debetkonto och ett kreditkonto för betalningstolerans. Mer information finns i [Ställa in bokföringsmallar](finance-posting-groups.md).  
5. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokföringsinställningar för leverantör** och väljer sedan relaterad länk.  
6. Öppna sidan **Leverantörsbokföringsmallar**. Lägg upp ett debetkonto och ett kreditkonto för betalningstolerans.  
7. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
8. Öppna sidan **Redovisningsinställningar**.  
9. På snabbfliken **Program**, fyll i fälten **Kassarabattolerans bokf.**, **Kassarabattfrist** och **Betalningstolerans bokföring**.   
10. Välj åtgärden **Ändra betalningstolerans**.

    > [!NOTE]
    > När du väljer **Koppla till äldsta** i fältet **Avräkningsmetod** på sidan **Kundkort** kommer inte [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt att lägga upp betalningstoleranser, även när de ligger inom de tröskelvärden som anges på sidan **Redovisningsinställningar**. [!INCLUDE[prod_short](includes/prod_short.md)] förutsätter att inställningen Koppla till äldsta anger att kunden (eller leverantören) har ett konto hos dig där de regelbundet betalar saldot. Därför bör du inte ta bort de återstående beloppen genom att bokföra en betalningstolerans transaktion.

11. P sidan **Ändra betalningstolerans** genom att fylla i fälten **Betalningstolerans %** och **Max.belopp betalningstolerans** samt välja **OK**.

> [!IMPORTANT]  
> Du har nu lagt upp toleransen för basvalutan. Om du vill att [!INCLUDE[prod_short](includes/prod_short.md)] ska hantera tolerans för betalningar, kreditnotor och återbetalningar i en utländsk valuta ska hanteras måste du köra batch-jobbet **Ändra betalningstolerans** med ett värde i fältet **Valutakod**.  

> [!NOTE]  
> Om du vill visa ett varningsmeddelande när du bokför en kopplad transaktion inom toleransen måste du aktivera betalningstoleransvarningen. Mer information finns i [aktivera eller inaktivera betalningstoleransvarningar](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
> Du inaktiverar toleransen för en kund eller leverantör genom att spärra toleransen på motsvarande kund- eller leverantörskort. Mer information finns i [Spärra betalningstolerans för kunder](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
> När du lägger upp toleransen kontrollerar [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt om det finns några öppna transaktioner och beräknas toleransen för dessa transaktioner också.

> [!IMPORTANT]  
> När du aktiverar fältet **Justera för kassarabatt** på sidan **Bokföringsinställningar för moms** anses momsbeloppet vara kopplat till beloppen i **betalningstolerans** och **kassarabatter** och moms minskas för båda transaktionsbeloppen om de finns. Det går inte att konfigurera systemet att använda momsminskning för en typ av transaktion.  

## Så här aktiverar eller inaktiverar du betalningstoleransvarningen:

Betalningstoleransvarningen visas när du bokför en kopplad transaktion med ett saldo som ligger inom den tillåtna toleransen. Du kan då välja hur du vill bokföra och dokumentera saldot.    
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** på snabbfliken **Koppling** i fönstret **Betal.tolerans varning** för att aktivera varningen. Inaktivera varningen genom att stänga av växlingen.  

> [!NOTE]  
> Standardalternativet för sidan **Betal.tolerans varning** är **Lämna saldo som återstående belopp**. Standardalternativet för sidan **Kassarabattolerans varning** är **Acceptera inte sen kassarabatt**.

## Så här spärrar du betalningstolerans för kunder

Betalningstoleransens standardinställning är tillåten. Du inaktiverar toleransen för en kund eller leverantör genom att spärra toleransen på motsvarande kund- eller leverantörskort. Nedan beskrivs hur du gör för en kund. Momenten är liknande för en leverantör.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** eller **Leverantör** och väljer sedan relaterad länk.  
2. Välj kryssrutan **Spärra betalningstolerans** på Snabbfliken **Betalningar**.  

> [!NOTE]  
> Om det finns öppna transaktioner för kunden eller leverantören tillfrågas du om du vill ta bort betalningstoleransen från transaktioner som är öppna för tillfället.

## Exempel 1 – toleransberäkningar för enstaka dokument

Följande är några exempelscenarier som visar förväntade toleransberäkningar och bokföringar i olika situationer.  

Sidan **redovisning** innehåller följande inställningar:
- Kassarabattfrist:    5D  
- Max betalningstolerans: 5  

Scenarier med alternativ A och B motsvarar dessa följande:  

- **A** I det här fallet har varningen för betalningstolerans (rabatt) kopplats från, eller så har användaren kopplat på varningen och valt att tillåta sen kassarabatt (Bokför saldo som betalningstolerans).  
- **B** I det här fallet har användaren kopplat på varningen och valt att inte tillåta sen kassarabatt (Lämna saldo som återstående belopp).  

|—|Fakturering|Kassarabatt|Max. betalningstolerans|Kassarabattdatum|Datum för kassarabattstolerans|Betalningsdatum|Betalning|Toleranstyp|Alla poster stängda|Kassarabattstolerans GL/CL|Betalningstolerans GL/CL|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1 000|20|5|03-01-15|03-01-20|<=03-01-15|985|PaymentTolerance|Ja|0|-5|  
|2|**1,000**|**20**|**5**|**03-01-15**|**03-01-20**|**<=03-01-15**|**980**|**Ingen**|**Ja**|**0**|**0**|  
|3|1 000|20|5|03-01-15|a|<=03-01-15|975|PaymentTolerance|Ja|0|5|  
|4A|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|1005|PaymentDiscountTolerance|Nej, 25 på betalningen|20/-20|0|  
|5A|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|1000|PaymentDiscountTolerance|Nej, 20 på betalningen|20/-20|0|  
|6A|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|995|PaymentDiscountTolerance|Nej, 15 på betalningen|20/-20|0|  
|4B|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|1005|PaymentTolerance|Ja|0|-5|  
|**5B**|**1,000**|**20**|**5**|**03-01-15**|**03-01-20**|**03-01-16 03-01-20**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|6B|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|995|PaymentTolerance|Ja|0|5|  
|7|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|985|PaymentDiscountTolerance och PaymentTolerance|Ja|20/-20|-5|  
|8|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|980|PaymentDiscountTolerance|Ja|20/-20|0|  
|9|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|975|PaymentDiscountTolerance och PaymentTolerance|Ja|20/-20|5|  
|10|1 000|20|5|03-01-15|03-01-20|>03-01-20|1005|PaymentTolerance|Ja|0|-5|  
|**11**|**1,000**|**20**|**5**|**03-01-15**|**03-01-20**|**>03-01-20**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|12|1 000|20|5|03-01-15|03-01-20|>03-01-20|995|PaymentTolerance|Ja|0|5|  
|13|1 000|20|5|03-01-15|03-01-20|>03-01-20|985|Ingen|Nej, 15 på fakturan|0|0|  
|14|1 000|20|5|03-01-15|03-01-20|>03-01-20|980|Ingen|Nej, 20 på fakturan|0|0|  
|15|1 000|20|5|03-01-15|03-01-20|>03-01-20|975|Ingen|Nej, 25 på fakturan|0|0|  

### Betalningsintervalldiagram

I relation till scenariot ovan kan betalningsintervallen illustreras på följande sätt:  

#### (1) Betalningsdatum <=03-01-15 (scenarier 1–3)

Återstående belopp per  

normala kopplingsregler  

![Toleransregler för enkel betalning 1.](media/singlePmtTolRules_Pre1503.gif "Toleransregler för enkel betalning 1")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### (2) Betalningsdatumet infaller mellan 03-01-16 och 03-01-20 (scenario 4-9)

Återstående belopp per  

normala kopplingsregler  

![Toleransregler för enkel betalning 2.](media/singlePmtTolRules_GracePeriod.gif "Toleransregler för enkel betalning 2")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### (3) Betalningsdatum infaller efter 03-01-20 (scenario 10-15)

Återstående belopp per  

normala kopplingsregler  

![Toleransregler för enkel betalning 3.](media/singlePmtTolRules_Post0120.gif "Toleransregler för enkel betalning 3")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

## Exempel 2 – toleransberäkningar för flera dokument

Följande är några exempelscenarier som visar förväntade toleransberäkningar och bokföringar i olika situationer. Exemplen gäller bara de scenarier som resulterar i att alla poster i programmet stängs.  

Sidan **redovisning** innehåller följande inställningar:
- Kassarabattfrist    5D  
- Max betalningstolerans; 5  

Scenarier med alternativ A, B, C, eller D motsvarar dessa följande:  

- **A**  I det här fallet har varningen för betalningstolerans (rabatt) kopplats från, eller så har användaren kopplat på varningen och valt att tillåta sen kassarabatt (Bokför som tolerans) i en faktura.  
- **B** I det här fallet har användaren kopplat på varningen och valt att inte tillåta sen kassarabatt i en faktura.  
- **C** – I det här fallet har användaren kopplat på varningen och valt att tillåta sen kassarabatt på den första fakturan men inte på den andra.  
- **D** – I det här fallet har användaren kopplat på varningen och valt att inte tillåta sen kassarabatt på den första fakturan men däremot på den andra.  

|—|Fakturering|Kassarabatt|Max. betalningstolerans|Kassarabattdatum|Datum för kassarabattstolerans|Betalningsdatum|Betalning|Toleranstyp|Alla poster stängda|Kassarabattstolerans GL/CL|Betalningstolerans GL/CL|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|<=03-01-15|1920|PaymentTolerance|Ja|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**<=03-01-15**|**1910**|**Ingen**|**Ja**|**0**<br /><br /> **0**|0 <br />0|  
|3|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|<=03-01-15|1900|PaymentTolerance|Ja|0<br /><br /> 0|5 <br />5|  
|4B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1980|PaymentTolerance|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**03-01-16 03-01-17**|**1970**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1960|PaymentTolerance|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1920|PaymentDiscountTolerance och PaymentTolerance|Ja|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1910|PaymentDiscountTolerance|Ja|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1900|PaymentDiscountTolerance och PaymentTolerance|Ja|60/60|5 <br />5|  
|10B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|2010|PaymentTolerance|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**03-01-18 03-01-20**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1990|PaymentTolerance|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1980|PaymentDiscountTolerance och PaymentTolerance|Ja|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1970|PaymentDiscountTolerance|Ja|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1960|PaymentDiscountTolerance och PaymentTolerance|Ja|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1950|PaymentDiscountTolerance och PaymentTolerance|Ja|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1940|PaymentDiscountTolerance|Ja|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1930|PaymentDiscountTolerance och PaymentTolerance|Ja|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1920|PaymentDiscountTolerance och PaymentTolerance|Ja|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1910|PaymentDiscountTolerance|Ja|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1900|PaymentDiscountTolerance och PaymentTolerance|Ja|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|2010|PaymentTolerance|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**03-01-21 03-01-22**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1990|PaymentTolerance|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1980|PaymentDiscountTolerance och PaymentTolerance|Ja|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1970|PaymentDiscountTolerance|Ja|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1960|PaymentDiscountTolerance och PaymentTolerance|Ja|0/0<br /><br /> 30/30|5 <br />5|  
|28|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|>03-01-22|2010|PaymentTolerance|Ja|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**>03-01-22**|**2000**|**Ingen**|**Ja**|**0**|**0**|  
|30|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|>03-01-22|1990|PaymentTolerance|Ja|0|5|  

### Betalningsintervalldiagram

I relation till scenariot ovan kan betalningsintervallen illustreras på följande sätt:  

#### (1) Betalningsdatum <=03-01-15 (scenarier 1–3)

Återstående belopp per  

normala kopplingsregler  

:::image type="content" source="media/multiplePmtTolRules_Pre1503.gif" alt-text="Multipla regler för betalningstolerans 1a":::

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### (2) Betalningsdatumet infaller mellan 03-01-16 och 03-01-17 (scenario 4-9)

Återstående belopp per  

normala kopplingsregler  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1-2.gif" alt-text="Toleransregler för flera betalningar 2":::

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### (3) Betalningsdatumet infaller mellan 03-01-18 och 03-01-20 (scenario 10-21)

Återstående belopp per  

normala kopplingsregler  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1.gif" alt-text="Toleransregler för flera betalningar 3":::

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### (4) Betalningsdatumet infaller mellan 03-01-21 och 03-01-22 (scenario 22-27)

Återstående belopp per  

normala kopplingsregler  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv2.gif" alt-text="Toleransregler för flera betalningar 4":::

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### (5) Betalningsdatum infaller efter 03-01-22 (scenario 28-30)

Återstående belopp per  

normala kopplingsregler  

:::image type="content" source="media/multiplePmtTolRules_Post0122.gif" alt-text="Toleransregler för flera betalningar 5":::

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.

## Se relaterad [Microsoft utbildning](/training/modules/enter-payments-dynamics-365-business-central/)

## Se även

[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
