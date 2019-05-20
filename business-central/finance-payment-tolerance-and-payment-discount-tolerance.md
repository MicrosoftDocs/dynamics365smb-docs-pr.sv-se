---
title: Betalningstolerans och kassarabattstolerans | Microsoft Docs
description: Du kan skapa betalningstolerans för att avsluta en faktura, när betalningen inte täcker hela beloppet på fakturan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: def9338cea3a1998aafac671e304c55f83fdece7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242474"
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Arbeta med betalningstoleranser och kassarabattstoleranser
Du kan skapa betalningstolerans för att avsluta en faktura, när betalningen inte täcker hela beloppet på fakturan. Du kan ställa in betalningstolerans (rabatt) när du ska bevilja en kassarabatt efter att kassarabattsdatumet har passerat.  

Du kan använda betalningstolerans så att alla utestående belopp anger ett maximum som medger betalningstolerans. Om betalningstoleransen uppfylls analyseras betalningsbeloppet. Om beloppet är en underbetalning stängs det utestående beloppet helt av underbetalningen. En detaljerad redovisningstransaktion har bokförts på betalningstransaktionen så att det inte finns något belopp kvar på fakturaposten. Om beloppet är en överbetalning bokförs en ny detaljerad reskontratransaktion på betalningstransaktionen så att det inte finns något belopp kvar på betalningstransaktionen.

Du kan använda kassarabattstolerans så att om du godkänner en kassarabatt efter kassarabattsdatumet, bokförs den alltid på kontot för kassarabatt eller kontot för betalningstolerans.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Använda betalningstolerans på flera dokument  
Ett enskilt dokument har samma betalningstolerans oavsett om det används som det är eller tillsammans med andra dokument. Godkännande av en sen kassarabatt, när du kopplar betalningstolerans till flera dokument sker automatiskt för varje dokument där följande regel gäller:  

*kassarabattsdatum < betalningsdatum för fokustransaktionen <= betalningstoleransdatum*  

Denna regel gäller även när du vill bestämma om du vill visa varningar när du kopplar betalningstolerans till flera dokument. Varningen för kassarabattstoleransen visas för varje transaktion som uppfyller villkoren. Mer information finns i avsnittet [exempel 2 – toleransberäkningar för flera dokument](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Du kan välja att visa ett varningsmeddelande som baseras på olika toleranssituationer.  

- Den första varningstexten gäller betalningsrabattoleransen. Du får information om att du kan godkänna en sen kassarabatt. Du kan sedan välja att godkänna toleransen för rabattdatumet.  
- Den andra varningstexten gäller betalningstoleransen. Du informeras om att alla transaktioner kan stängas eftersom skillnaden ligger inom den totala betalningstoleransen för transaktionerna. Du kan sedan välja att godkänna toleransen för betalningsbeloppet.

Mer information finns i [aktivera eller inaktivera betalningstoleransvarningar](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).     

## <a name="to-set-up-tolerances"></a>Så här lägger du upp toleranser  
Du kan använda toleranser för dagar och belopp så att du kan avsluta en faktura även om betalningen inte täcker hela fakturabeloppet, oavsett om det beror på att förfallodatumet för kassarabatten har passerats, att varorna har dragits av eller att ett mindre fel har begåtts. Det gäller även återbetalningar och kreditnotor.  

Du lägger upp toleransen genom att lägga upp olika toleranskonton, ange bokföringsmetoder för både kassarabattstolerans och betalningstolerans samt köra batch-jobbet **Ändra betalningstolerans**.  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokföringsinställningar** och välj sedan relaterad länk.  
2. Öppna sidan **Bokföringsinställningar**. Lägg upp ett debet- och ett kreditkonto för försäljningsbetalningstolerans och ett debet- och ett kreditkonto för inköpsbetalningstolerans.  
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kundbokföringsmallar** och välj sedan relaterad länk.    
4. Öppna sidan **Kundbokföringsmallar**. Lägg upp ett debetkonto och ett kreditkonto för betalningstolerans. Mer information finns i [Ställa in bokföringsmallar](finance-posting-groups.md).  
5. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokföringsinställningar för leverantör** och välj sedan relaterad länk.  
6. Öppna sidan **Leverantörsbokföringsmallar**. Lägg upp ett debetkonto och ett kreditkonto för betalningstolerans.  
7. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsinställningar** och välj sedan relaterad länk.  
8. Öppna sidan **Redovisningsinställningar**.  
9. På snabbfliken **Program**, fyll i fälten **Kassarabattolerans bokf.**, **Kassarabattfrist** och **Betalningstolerans bokföring**.   
10. Välj åtgärden **Ändra betalningstolerans**.
11. P sidan **Ändra betalningstolerans** genom att fylla i fälten **Betalningstolerans %** och **Max.belopp betalningstolerans** samt välja **OK**.

> [!IMPORTANT]  
>  Du har nu lagt upp toleransen för basvalutan. Om du vill att [!INCLUDE[d365fin](includes/d365fin_md.md)] ska hantera tolerans för betalningar, kreditnotor och återbetalningar i en utländsk valuta ska hanteras måste du köra batch-jobbet **Ändra betalningstolerans** med ett värde i fältet **Valutakod**.  

> [!NOTE]  
>  Om du vill visa ett varningsmeddelande när du bokför en kopplad transaktion inom toleransen måste du aktivera betalningstoleransvarningen. Mer information finns i [aktivera eller inaktivera betalningstoleransvarningar](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
>  Du inaktiverar toleransen för en kund eller leverantör genom att spärra toleransen på motsvarande kund- eller leverantörskort. Mer information finns i [Spärra betalningstolerans för kunder](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
>  När du lägger upp toleransen kontrollerar [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt om det finns några öppna transaktioner och beräknas toleransen för dessa transaktioner också.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Så här aktiverar eller inaktiverar du betalningstoleransvarningen:
Betalningstoleransvarningen visas när du bokför en kopplad transaktion med ett saldo som ligger inom den tillåtna toleransen. Du kan då välja hur du vill bokföra och dokumentera saldot.    
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** på snabbfliken **Koppling** i fönstret **Betal.tolerans varning** för att aktivera varningen. Inaktivera varningen genom att avmarkera kryssrutan.  

> [!NOTE]  
>  Standardalternativet för sidan **Betal.tolerans varning** är **Lämna saldo som återstående belopp**. Standardalternativet för sidan **Kassarabattolerans varning** är **Acceptera inte sen kassarabatt**.

## <a name="to-block-payment-tolerance-for-customers"></a>Så här spärrar du betalningstolerans för kunder  
Betalningstoleransens standardinställning är tillåten. Du inaktiverar toleransen för en kund eller leverantör genom att spärra toleransen på motsvarande kund- eller leverantörskort. Nedan beskrivs hur du gör för en kund. Momenten är liknande för en leverantör.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kund** eller **Leverantör** och välj sedan relaterad länk.  
2. Välj kryssrutan **Spärra betalningstolerans** på Snabbfliken **Betalningar**.  

> [!NOTE]  
>  Om det finns öppna transaktioner för kunden eller leverantören tillfrågas du om du vill ta bort betalningstoleransen från transaktioner som är öppna för tillfället.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Exempel 1 - toleransberäkningar för enstaka dokument
Följande är några exempelscenarier som visar förväntade toleransberäkningar och bokföringar i olika situationer.  

Sidan **redovisning** innehåller följande inställningar:
- Kassarabattfrist:    5D  
- Max betalningstolerans: 5  

Scenarier med alternativ A och B motsvarar dessa följande:  

- **A** I det här fallet har varningen för betalningstolerans (rabatt) kopplats från, eller så har användaren kopplat på varningen och valt att tillåta sen kassarabatt (Bokför saldo som betalningstolerans).  
- **B** I det här fallet har användaren kopplat på varningen och valt att inte tillåta sen kassarabatt (Lämna saldo som återstående belopp).  

|—|Fakturering|Kassarabatt|Max bet. tol.|Kassarabattsdatum|Betal.tol.rabatt Datum|Betalningsdatum|Bet.|Toleranstyp|Alla poster stängda|Betal.tol.rabatt GL/CL|Bet. tol. Redovisning|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1 000|20|5|03-01-15|03-01-20|<=03-01-15|985|Bet.tol.|Ja|0|-5|  
|2|**1,000**|**20**|**5**|**03-01-15**|**03-01-20**|**<=03-01-15**|**980**|**Ingen**|**Ja**|**0**|**0**|  
|3|1 000|20|5|03-01-15|c|<=03-01-15|975|Bet.tol.|Ja|0|5|  
|4A|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|1005|Betal.tol.rabatt|Nej, 25 på Bet.|20/-20|0|  
|5A|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|1000|Betal.tol.rabatt|Nej, 20 på Bet.|20/-20|0|  
|6A|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|995|Betal.tol.rabatt|Nej, 15 på Bet.|20/-20|0|  
|4B|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|1005|Bet.tol.|Ja|0|-5|  
|**5B**|**1,000**|**20**|**5**|**03-01-15**|**03-01-20**|**03-01-16 03-01-20**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|6B|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|995|Bet.tol.|Ja|0|5|  
|7|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|985|Betal.tol.rabatt och Bet. tol.|Ja|20/-20|-5|  
|8|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|980|Betal.tol.rabatt|Ja|20/-20|0|  
|9|1 000|20|5|03-01-15|03-01-20|03-01-16 03-01-20|975|Betal.tol.rabatt och Bet. tol.|Ja|20/-20|5|  
|10|1 000|20|5|03-01-15|03-01-20|>03-01-20|1005|Bet.tol.|Ja|0|-5|  
|**11**|**1,000**|**20**|**5**|**03-01-15**|**03-01-20**|**>03-01-20**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|12|1 000|20|5|03-01-15|03-01-20|>03-01-20|995|Bet.tol.|Ja|0|5|  
|13|1 000|20|5|03-01-15|03-01-20|>03-01-20|985|Ingen|Nej, 15 på fakturan|0|0|  
|14|1 000|20|5|03-01-15|03-01-20|>03-01-20|980|Ingen|Nej, 20 på fakturan|0|0|  
|15|1 000|20|5|03-01-15|03-01-20|>03-01-20|975|Ingen|Nej, 25 på fakturan|0|0|  

### <a name="payment-range-diagrams"></a>Betalningsintervalldiagram  
I relation till scenariot ovan kan betalningsintervallen illustreras på följande sätt:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Betalningsdatum <=03-01-15 (scenarier 1–3)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för enkel betalning 1](media/singlePmtTolRules(Pre1503).gif "Toleransregler för enkel betalning 1")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Betalningsdatumet infaller mellan 03-01-16 och 03-01-20 (scenario 4-9)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för enkel betalning 2](media/singlePmtTolRules(GracePeriod).gif "Toleransregler för enkel betalning 2")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Betalningsdatum infaller efter 03-01-20 (scenario 10-15)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för enkel betalning 3](media/singlePmtTolRules(Post0120).gif "Toleransregler för enkel betalning 3")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Exempel 2 -  toleransberäkningar för flera dokument
Följande är några exempelscenarier som visar förväntade toleransberäkningar och bokföringar i olika situationer. Exemplen gäller bara de scenarier som resulterar i att alla poster i programmet stängs.  

Sidan **redovisning** innehåller följande inställningar:
- Kassarabattfrist    5D  
- Max betalningstolerans; 5  

Scenarier med alternativ A, B, C, eller D motsvarar dessa följande:  

- **A**  I det här fallet har varningen för betalningstolerans (rabatt) kopplats från, eller så har användaren kopplat på varningen och valt att tillåta sen kassarabatt (Bokför som tolerans) i en faktura.  
- **B** I det här fallet har användaren kopplat på varningen och valt att inte tillåta sen kassarabatt i en faktura.  
- **C** - I det här fallet har användaren kopplat på varningen och valt att tillåta sen kassarabatt på den första fakturan men inte på den andra.  
- **D** - I det här fallet har användaren kopplat på varningen och valt att inte tillåta sen kassarabatt på den första fakturan men däremot på den andra.  

|—|Fakturering|Kassarabatt|Max bet. tol.|Kassarabattsdatum|Betal.tol.rabatt Datum|Betalningsdatum|Bet|Toleranstyp|Alla poster stängda|Betal.tol.rabatt GL/CL|Bet. tol. Redovisning|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|<=03-01-15|1920|Bet.tol.|Ja|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**<=03-01-15**|**1910**|**Ingen**|**Ja**|**0**<br /><br /> **0**|0 <br />0|  
|3|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|<=03-01-15|1900|Bet.tol.|Ja|0<br /><br /> 0|5 <br />5|  
|4B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1980|Bet.tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**03-01-16 03-01-17**|**1970**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1960|Bet.tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1920|Betal.tol.rabatt och Bet. tol.|Ja|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1910|Betal.tol.rabatt|Ja|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-16 03-01-17|1900|Betal.tol.rabatt och Bet. tol.|Ja|60/60|5 <br />5|  
|10B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|2010|Bet.tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**03-01-18 03-01-20**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1990|Bet.tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1980|Betal.tol.rabatt och Bet. tol.|Ja|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1970|Betal.tol.rabatt|Ja|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1960|Betal.tol.rabatt och Bet. tol.|Ja|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1950|Betal.tol.rabatt och Bet. tol.|Ja|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1940|Betal.tol.rabatt|Ja|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1930|Betal.tol.rabatt och Bet. tol.|Ja|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1920|Betal.tol.rabatt och Bet. tol.|Ja|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1910|Betal.tol.rabatt|Ja|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-18 03-01-20|1900|Betal.tol.rabatt och Bet. tol.|Ja|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|2010|Bet.tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**03-01-21 03-01-22**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1990|Bet.tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1980|Betal.tol.rabatt och Bet. tol.|Ja|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1970|Betal.tol.rabatt|Ja|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|03-01-21 03-01-22|1960|Betal.tol.rabatt och Bet. tol.|Ja|0/0<br /><br /> 30/30|5 <br />5|  
|28|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|>03-01-22|2010|Bet.tol.|Ja|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**03-01-15** <br />**03-01-17**|**03-01-20** <br />**03-01-22**|**>03-01-22**|**2000**|**Ingen**|**Ja**|**0**|**0**|  
|30|1 000 <br />1 000|60 <br />30|5 <br />5|03-01-15 <br />03-01-17|03-01-20 <br />03-01-22|>03-01-22|1990|Bet.tol.|Ja|0|5|  

### <a name="payment-range-diagrams"></a>Betalningsintervalldiagram  
I relation till scenariot ovan kan betalningsintervallen illustreras på följande sätt:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Betalningsdatum <=03-01-15 (scenarier 1–3)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för flera betalningar 1](media/multiplePmtTolRules(Pre1503).gif "Toleransregler för flera betalningar 1")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Betalningsdatumet infaller mellan 03-01-16 och 03-01-17 (scenario 4-9)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för flera betalningar 2](media/multiplePmtTolRules(GracePeriodInv1).gif "Toleransregler för flera betalningar 2")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Betalningsdatumet infaller mellan 03-01-18 och 03-01-20 (scenario 10-21)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för flera betalningar 3](media/multiplePmtTolRules(GracePeriodInv1-2).gif "Toleransregler för flera betalningar 3")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Betalningsdatumet infaller mellan 03-01-21 och 03-01-22 (scenario 22-27)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för flera betalningar 4](media/multiplePmtTolRules(GracePeriodInv2).gif "Toleransregler för flera betalningar 4")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Betalningsdatum infaller efter 03-01-22 (scenario 28-30)  
Återstående belopp per  

normala kopplingsregler  

![Toleransregler för flera betalningar 5](media/multiplePmtTolRules(Post0122).gif "Toleransregler för flera betalningar 5")  

(1) Om betalningen återfinns inom dessa intervall kan alla kopplingsposter avslutas med eller utan tolerans.  

(2) Om betalningen faller återfinns dessa intervall kan inte alla kopplingsposter avslutas ens med tolerans.

## <a name="see-also"></a>Se även  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
