---
title: Ställ in alternativa valutor
description: 'Din redovisning ställs in för att använda den lokala valutan (BVA) och en annan valuta ställs in som en alternativ valuta, med en tilldelad aktuell valutakurs.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Konfigurera en alternativ rapporteringsvaluta

Eftersom företag verkar i allt fler länder/regioner blir det alltmer viktigt att de kan granska och rapportera ekonomiska data i fler än en valuta.

> [!NOTE]  
> Om du söker efter realtidsinformation om valutakurser i utländsk valuta (FX) eller historiska kurser, hittar du den som "valuta" i [!INCLUDE[prod_short](includes/prod_short.md)]. Förutom denna artikel, se även [Uppdatera valutakurser](finance-how-update-currencies.md).

Din redovisning ställs in för att använda den lokala valutan (BVA) men du kan ställa in en annan valuta med en tilldelad aktuell valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta (ACY) kommer [!INCLUDE[prod_short](includes/prod_short.md)] att registrera belopp automatiskt i både BVA och AVAL och andra transaktioner, t.ex. momstransaktioner.

> [!Warning]
> Du bör inte använda AVAL-funktionen som grund för omräkning av finansiella rapporter om du inte förstår dess begränsningar. Det kan inte utföra omräkningar av ekonomirapporter för utländska dotterbolag som en del i en företagskonsolidering. AVAL kan endast användas för att förbereda rapporter i en annan valuta på ett sådant sätt som om den valutan var företagets BVA.
>
> Du har till exempel en stor mängd kundreskontra i brittiska pund (GBP) och du har ställt in den AVAL som GBP. I det här scenariot kommer belopp i de kundreskontra som använder GBP inte att justeras för valutakurs vinster/-förluster i AVAL, utan endast belopp i kundreskontra som tillhör andra valutor. Det innebär att om du använder ACY för att rapportera de ekonomiska rapporterna, kan det leda till att utestående saldon för kundreskontra blir undertryckta eller överskattade.

## Visa rapporter och belopp i AVAL

Med hjälp av AVAL kan rapporteringsprocessen för ett företag förenklas i följande fall:

- Företag i länder/regioner utanför EU som har en stor andel transaktioner med länder/regioner inom EU. I det här fallet kan landet utanför EU också vilja rapportera i euro för att göra sina ekonomirapporter mer användbara för sina EU-handelspartner.
- Företag som också vill visa rapporter i en mer internationell handelsvaluta än sin egen lokala valuta.

Flera finansiella rapporter som är baserade på redovisningstransaktioner. Om du vill visa rapportdata i AVAL markerar du kryssrutan **Visa belopp i alt. rapporteringsvaluta** på snabbfliken **Alternativ** för den relevanta redovisningsrapporten.

## Justera valutakurser

Eftersom valutakurser ständigt fluktuerar måste alternativa AVAL i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats. Batch-jobbet **Justera valutakurser** används för att justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera AVAL-belopp för redovisningstransaktioner. Mer information finns i [uppdatera valutakurser](finance-how-update-currencies.md).

## Konfigurerar en AVAL

Följ dessa steg för att konfigurera AVAL:

- Ange redovisningskonton för bokföring av valutakursjusteringar.  
- Ange kursjusteringsmetod för alla redovisningskonton.  
- Ange kursjusteringsmetod för momstransaktioner.  
- Aktivera AVAL.  

### Så här anger du redovisningskonton för bokföring av valutakursjusteringar  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Valutor** och väljer sedan relaterad länk.  
2. På sidan **Valutor** fyller du i följande fält för AVAL.  

|Fält|Description|  
|---------------------------------|---------------------------------------|  
|**Kursvinst konstaterad redov.**|Det redovisningskonto som valutakursvinster ska bokföras på vid valutakursjusteringar mellan BVA och AVAL.|  
|**Kursförlust konstaterad redov.**|Det redovisningskonto som valutakursförluster ska bokföras på vid valutakursjusteringar mellan BVA och AVAL.|  
|**Restvinster**|Det redovisningskonto där restbelopp som är vinster kommer att bokföras, om du bokför i redovisningsmodulen i både BVA och i en AVAL.|  
|**Restförluster**|Det redovisningskonto där restbelopp som är förluster kommer att bokföras, om du bokför i redovisningsmodulen i både BVA och i en AVAL.|

> [!NOTE]  
> Restbelopp kan uppstå när debet- och kreditbelopp som har konverterats i [!INCLUDE[prod_short](includes/prod_short.md)] från BVA till en AVAL.  

För varje redovisningskonto måste du ange hur redovisningsbelopp för det kontot ska justeras för valutakursfluktuationer mellan BVA och AVAL.  

### Ange kursjusteringsmetod för alla redovisningskonton

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. På sidan **Kontoplan** väljer du relevant konto och sedan åtgärden **Redigera**.  
3. På sidan **Redovisningskontokort** väljer du relevant metod i fältet **Valutakursjustering**.  

    Om du bokför i en AVAL, anger du i fältet **Valutakursjustering** hur detta redovisningskonto kommer att justeras för valutakursfluktuationer mellan BVA och AVAL. Alternativen beskrivs i tabellen nedan.  

    |Fält|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ingen justering**|Ingen valutakursjustering kommer att ske till redovisningskontot. Den här inställningen är standardalternativet.<br /><br /> **OBS!** Välj det här alternativet om valutakursen mellan BVA och AVAL alltid är fast.|  
    |**Justera belopp**|BVA-beloppet justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  
    |**Justera belopp i alternativ valuta**|AVAL justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Alt. valuta belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  

    Kursvinster och -förluster bokförs när du kör batch-jobbet **Justera valutakurser**. I det batch-jobbet identifieras den justerade valutakursen på sidan **Valutakurser** och sedan jämförs beloppen i fälten **Belopp** och **Alt. valuta belopp** i redovisningstransaktionen för att fastställa om det finns en kursvinst eller kursförlust. När batch-jobbet körs används det alternativ som du har markerat i fältet **Valutakursjustering** för att bestämma hur kursvinster eller -förluster ska beräknas och bokföras för redovisningskonton.  

4.  Stäng sidan **Redovisningskontokort**.  

### Så här anger du kursjusteringsmetod för momstransaktioner

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** väljer du relevant metod i fältet **Moms valutakursjustering**.  
3. Om du bokför i en AVAL kan du i fältet **Moms valutakursjustering** ange hur de konton som ställts in för momsbokföring på sidan **Moms bokföringsinställning** ska justeras för kursfluktuationer mellan BVA och AVAL.  

    När du kör batch-jobbet **Justera valutakurser** identifieras justeringskursen på sidan **Valutakurs** och sedan beloppen i fälten **Belopp** och **Alt. valuta belopp** i momstransaktionen för att fastställa om det finns en kursvinst eller kursförlust. Det här batch-jobbet använder det alternativ du väljer i det här fältet för att avgöra hur valutakursvinster eller -förluster för momskonton ska bokföras.  

    Du kan välja mellan samma tre alternativ som med redovisningstransaktioner, men i det här fallet är de transaktioner som justeras momstransaktionerna. Alternativen beskrivs i tabellen nedan.

    |Fält|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ingen justering**|Ingen valutakursjustering kommer att ske till redovisningskontot. Den här inställningen är standardalternativet.|  
    |**Justera belopp**|BVA-beloppet justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  
    |**Justera belopp i alternativ valuta**|AVAL justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Alt. valuta belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  

### Så här aktiverar du AVAL  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** väljer du fältet **Alternativ rapporteringsvaluta** och välj den alternativa valuta du vill rapportera i.  
3. När du lämnar fältet visar [!INCLUDE[prod_short](includes/prod_short.md)] ett bekräftelsemeddelande som beskriver effekterna när du aktiverar AVAL.  
4. Välj **ja** för att bekräfta att du vill aktivera valutan.  
5. Batch-jobbet **Justera alt. rapporteringsvaluta** öppnas.

    Detta batch-jobb omvandlar BVA-belopp för befintliga transaktioner till AVAL. I batch-jobbet används en standardkurs som har kopierats från den valutakurs som är giltig på arbetsdatumet på sidan **Valutakurser**. Restbelopp som uppstår vid omräkning av BVA till AVAL bokförs på de konton för restvinster och restförluster som har angetts på sidan **Valutor**. Bokföringsdatumet och verifikationsnumret för dessa verifikationer är samma som för den ursprungliga redovisningstransaktionen. När du har bokfört alla resttransaktioner bokförs en avrundningstransaktion vid avslutsdatumet för varje avslutat år på kontot för balanserad vinst eller förlust. Denna bokför görs för att den utgående balansen på intäktskontona för varje avslutat år är 0 för både BVA och AVAL.
6. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Klicka på **OK** för att köra batchjobbet.  

När du har kört batch-jobbet finns beloppen för följande befintliga transaktioner i både BVA och AVAL:  

- Redovisningstransaktioner  
- Artikelkopplingstransaktioner  
- Momstransaktioner  
- Projekttransaktioner  
- Värdetransaktioner  
- Produktionsorderrader  
- Produktionsordertransaktioner  

Dessutom kommer alla framtida transaktioner av samma typ att ha registrerade belopp i både BVA och AVAL.  

> [!NOTE]  
> Fältet **Alt. rapporteringsvaluta** kommer bara att vara aktivt när du har valt **OK** i batch-jobbet **Just. alt. rapporteringsvaluta**.  

## Se även

[Uppdatera valutakurser](finance-how-update-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
