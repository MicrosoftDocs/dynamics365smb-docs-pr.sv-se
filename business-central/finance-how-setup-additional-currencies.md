---
title: Ställa in alternativa valutor | Microsoft Docs
description: Din redovisning ställs in för att använda den lokala valutan (BVA) och en annan valuta ställs in som en alternativ valuta, med en tilldelad aktuell valutakurs.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2fde5bd3cd713b0eb6a9fade1ce7916fc952934d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "936872"
---
# <a name="set-up-an-additional-reporting-currency"></a>Ställa in en alternativ rapporteringsvaluta.
Eftersom företag verkar i allt fler länder/regioner blir det alltmer viktigt att de kan granska och rapportera ekonomiska data i fler än en valuta.

Din redovisning ställs in för att använda den lokala valutan (BVA) men du kan ställa in en annan valuta med en tilldelad aktuell valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion och för andra transaktioner, t.ex. momstransaktioner.

> [!Warning]
> Funktionen Alt. rapporteringsvaluta bör inte användas som underlag vid omräkning av ekonomirapporter. Verktyget kan inte användas för att utföra omräkningar av ekonomirapporter för utländska dotterbolag som en del i en företagskonsolidering. Den alternativa rapporteringsvalutan kan endast användas för att förbereda rapporter i en annan valuta på ett sådant sätt som om den valutan var företagets lokala valuta.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Visa rapporter och belopp i den alternativa rapporteringsvalutan
Med hjälp av en alternativ rapporteringsvaluta kan rapporteringsprocessen för ett företag förenklas i följande fall:

- Företag i länder/regioner utanför EU som har en stor andel transaktioner med länder/regioner inom EU. I det här fallet kan landet utanför EU också vilja rapportera i euro för att göra sina ekonomirapporter mer användbara för sina EU-handelspartner.
- Företag som också vill visa rapporter i en mer internationell handelsvaluta än sin egen lokala valuta.

Flera finansiella rapporter som är baserade på redovisningstransaktioner. Om du vill visa rapportdata i alternativ rapporteringsvaluta markerar du helt enkelt fältet **Visa belopp i alt. rapporteringsvaluta** på snabbfliken **Alternativ** för den relevanta redovisningsrapporten.

## <a name="adjusting-exchange-rates"></a>Justera valutakurser
Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats. Batch-jobbet **Justera valutakurser** används för att justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner. Mer information finns i [uppdatera valutakurser](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency"></a>Skapa en alternativ rapporteringsvaluta
Du måste följa dessa steg för att definiera alternativ rapporteringsvaluta:

-   Ange redovisningskonton för bokföring av valutakursjusteringar.  
-   Ange kursjusteringsmetod för alla redovisningskonton.  
-   Ange kursjusteringsmetod för momstransaktioner.  
-   Aktivera den alternativa rapporteringsvalutan.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Så här anger du redovisningskonton för bokföring av valutakursjusteringar  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutor** och välj sedan relaterad länk.  
2. På sidan **Valutor** fyller du i följande fält för alternativ rapporteringsvaluta.  

|Fält|Description|  
|---------------------------------|---------------------------------------|  
|**Kursvinst konstaterad redov.**|Det redovisningskonto som valutakursvinster ska bokföras på vid valutakursjusteringar mellan BVA och den alternativa rapporteringsvalutan.|  
|**Kursförlust konstaterad redov.**|Det redovisningskonto som valutakursförluster ska bokföras på vid valutakursjusteringar mellan BVA och den alternativa rapporteringsvalutan.|  
|**Restvinster**|Det redovisningskonto där restbelopp som är vinster kommer att bokföras, om du bokför i redovisningsmodulen i både BVA och i en alternativ rapporteringsvaluta.|  
|**Restförluster**|Det redovisningskonto där restbelopp som är förluster kommer att bokföras, om du bokför i redovisningsmodulen i både BVA och i en alternativ rapporteringsvaluta.|

> [!NOTE]  
>  Restbelopp kan uppstå när debet- och kreditbelopp som har konverterats i [!INCLUDE[d365fin](includes/d365fin_md.md)] från BVA till en alternativ rapporteringsvaluta avrundas.  

För varje redovisningskonto måste du ange hur redovisningsbelopp för det kontot ska justeras för valutakursfluktuationer mellan BVA och den alternativa rapporteringsvalutan.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Ange kursjusteringsmetod för alla redovisningskonton  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontoplan** och välj sedan relaterad länk.  
2. På sidan **Kontoplan** väljer du relevant konto och sedan åtgärden **Redigera**.  
3. På sidan **Redovisningskontokort** väljer du relevant metod i fältet **Valutakursjustering**.  

    Om du bokför i en alternativ rapporteringsvaluta, anger du i fältet **Valutakursjustering** hur detta redovisningskonto kommer att justeras för valutakursfluktuationer mellan BVA och den alternativa rapporteringsvalutan. Tabellen visar de alternativ som du kan välja.  

    |Fält|Beskrivning|  
    |----------------------------------|---------------------------------------|  
    |**Ingen justering**|Ingen valutakursjustering kommer att ske till redovisningskontot. Detta är standardförslaget.<br /><br /> **OBs!** Du bör välja det här alternativet om valutakursen BVA och den alternativa rapporteringsvalutan alltid är fast.|  
    |**Justera belopp**|BVA-beloppet justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  
    |**Justera belopp alt. valuta**|Alternativ rapporteringsvaluta justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Alt. valuta belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  

    Kursvinster och -förluster bokförs när du kör batch-jobbet **Justera valutakurser**. I det batch-jobbet identifieras den justerade valutakursen på sidan **Valutakurser** och sedan jämförs beloppen i fälten **Belopp** och **Alt. valuta belopp** i redovisningstransaktionen för att fastställa om det finns en kursvinst eller kursförlust. När batch-jobbet körs används det alternativ som du har markerat i fältet **Valutakursjustering** för att bestämma hur kursvinster eller -förluster ska beräknas och bokföras för redovisningskonton.  

4.  Stäng sidan **Redovisningskontokort**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Så här anger du kursjusteringsmetod för momstransaktioner  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** väljer du relevant metod i fältet **Moms valutakursjustering**.  
3. Om du bokför i en alternativ rapporteringsvaluta kan du ange i fältet **Moms valutakursjustering** hur de konton som ställts in för momsbokföring på sidan **Moms bokföringsinställning** ska justeras för kursfluktuationer mellan BVA och den alternativa rapporteringsvalutan.  

    När du kör batch-jobbet **Justera valutakurser** identifieras justeringskursen på sidan **Valutakurs** och sedan beloppen i fälten **Belopp** och **Alt. valuta belopp** i momstransaktionen för att fastställa om det finns en kursvinst eller kursförlust. Det här batch-jobbet använder det alternativ du väljer i det här fältet för att avgöra hur valutakursvinster eller -förluster för momskonton ska bokföras.  

    Du kan välja mellan samma tre alternativ som med redovisningstransaktioner, men i det här fallet är de transaktioner som justeras momstransaktionerna. Tabellen visar de alternativ som du kan välja.

    |Fält|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ingen justering**|Ingen valutakursjustering kommer att ske till redovisningskontot. Detta är standardförslaget.|  
    |**Justera belopp**|BVA-beloppet justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  
    |**Justera belopp alt. valuta**|Alternativ rapporteringsvaluta justeras för alla kursvinster eller kursförluster. Alla kursvinster eller kursförluster bokförs på redovisningskontot i fältet **Alt. valuta belopp** och på de konton du har angett för vinster eller förluster i fälten **Kursvinst konstaterad redov** och **Kursförlust konstaterad redov** på sidan **Valutor**.|  

### <a name="to-activate-the-additional-reporting-currency"></a>Så här aktiverar du den alternativa rapporteringsvalutan.  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** väljer du fältet **Alternativ rapporteringsvaluta** och välj den alternativa valuta du vill rapportera i.  
3. När du lämnar fältet visar [!INCLUDE[d365fin](includes/d365fin_md.md)] ett bekräftelsemeddelande som beskriver effekterna när du väljer (och aktiverar) den alternativa rapporteringsvalutan.  
4. Välj **ja** för att bekräfta att du vill aktivera valutan.  
5. Batch-jobbet **Justera alt. rapporteringsvaluta** öppnas.

    Detta batch-jobb omvandlar BVA-belopp för befintliga transaktioner till alternativ rapporteringsvaluta. I batch-jobbet används en standardkurs som har kopierats från den valutakurs som är giltig på arbetsdatumet på sidan **Valutakurser**. Restbelopp som uppstår vid omräkning av BVA till alternativ rapporteringsvaluta bokförs på de konton för restvinster och restförluster som har angetts på sidan **Valutor**. Bokföringsdatumet och verifikationsnumret för dessa verifikationer är samma som för den ursprungliga redovisningstransaktionen. När alla dessa resttransaktioner är bokförda bokförs en avrundningstransaktion vid avslutsdatumet för varje avslutat år på kontot för balanserad vinst eller förlust. Detta görs för att den utgående balansen på intäktskontona för varje avslutat år är 0 för både BVA och den alternativa rapporteringsvalutan.
6. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Klicka på **OK** för att köra batchjobbet.  

När du har kört det här batch-jobbet visas beloppen för följande befintliga transaktioner både i BVA och i den alternativa rapporteringsvalutan:  

- Redovisningstransaktioner  
- Artikelkopplingstransaktioner  
- Momstransaktioner  
- Projekttransaktioner  
- Värdetransaktioner  
- Produktionsorderrader  
- Produktionsordertransaktioner  

Dessutom kommer alla framtida transaktioner av samma typ att ha registrerade belopp i både BVA och den alternativa rapporteringsvalutan.  

> [!NOTE]  
>  Fältet **Alt. rapporteringsvaluta** kommer bara att vara aktivt när du har valt **OK** i batch-jobbet **Just. alt. rapporteringsvaluta**.  

## <a name="see-also"></a>Se även
[Uppdatera valutakurser](finance-how-update-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
