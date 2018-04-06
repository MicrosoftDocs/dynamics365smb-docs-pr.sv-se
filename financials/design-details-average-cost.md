---
title: Designdetaljer - Genomsnittskostnad | Microsoft Docs
description: "Genomsnittskostnaden för en artikel beräknas med ett återkommande viktat genomsnitt baserat på den genomsnittskostnadsperiod som ställs in i Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9e04bd1dbbae80cd209b28c14764fbf7dc7f0934
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-average-cost"></a>Designdetaljer: Genomsnittskostnad
Genomsnittskostnaden beräknas för en artikel med ett återkommande viktat genomsnitt baserat på den genomsnittskostnadsperiod som ställs in i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Värderingsdatum anges automatiskt.  

## <a name="setting-up-average-cost-calculation"></a>Ställa in beräkning av genomsnittskostnad  
 Följande tabell beskriver de två fälten i fönstret **Lagerinställningar** som måste fyllas för att aktivera beräkning av genomsnittskostnader.  

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Period för genomsnittskostnad**|Anger vilken period genomsnittskostnaden beräknas i. Följande alternativ finns:<br /><br /> -   **Dag**<br />-   **Vecka**<br />-   **Månad**<br />-   **Bokföringsperiod**<br /><br /> Genomsnittskostnaden beräknas för aktuell period för alla lagerminskningar som bokfördes inom den angivna genomsnittskostnadsperioden.|  
|**Genoms. kost.ber.typ**|Anger hur genomsnittskostnaden beräknas. Följande alternativ finns:<br /><br /> -   **Artikel**<br />-   **Artikel, Variant och Lagerställe**<br />     Med det här alternativet beräknas genomsnittskostnaden för varje artikel, för varje lagerställe och för varje variant av artikeln. Det innebär att genomsnittskostnaden för den här artikeln styrs av var den lagras och vilken variant av artikeln du har valt, som färg.|  

> [!NOTE]  
>  Du kan endast använda en genomsnittskostnadsperiod och beräkningstyp för genomsnittskostnad under ett räkenskapsår.  
>   
>  **Bokföringsperioder** visar genomsnittskostnadsperioden och vilken beräkningstyp för genomsnittskostnad som används under perioden, för varje bokföringsperiod.  

## <a name="calculating-average-cost"></a>Beräkna genomsnittskostnad  
 När du bokför en transaktion för en artikel som använder metoden Genomsnittskostnad skapas en transaktion i tabellen **Ingångspunkt för genomsn.kostn.justering**. Den här transaktionen innehåller transaktionens artikelnummer, variantkod och lagerplatskod. Transaktionen innehåller fältet **Värderingsdatum** som anger det senaste datumet i genomsnittskostnadsperioden som transaktionen bokfördes i.  

> [!NOTE]  
>  Detta fält ska inte förväxlas med fältet i tabellen **Värderingsdatum** i tabellen **Värdetransaktion** som innehåller datumet då värdet börjar gälla och används för att fastställa genomsnittskostnadsperioden som värdetransaktionen tillhör.  

 Genomsnittskostnaden för en transaktion beräknas när artikelns kostnad justeras. Mer information finns i [Designdetaljer: kostnadsjustering](design-details-cost-adjustment.md). En kostnadsjustering använder transaktionerna i tabellen **Ingångspunkt för genomsn.kostn.justering** för att identifiera vilka artiklar (eller artiklar, lagerställen och varianter) som genomsnittskostnader ska beräknas för. För varje transaktion med kostnad som ännu inte har justerats, använder kostnadsjustering följande för att fastställa genomsnittskostnaden:  

-   Kostnaden för artikeln i början av genomsnittskostnadsperioden fastställs.  
-   Summan av ankommande kostnader som bokfördes i genomsnittskostnadsperioden adderas. De innehåller inköp, försäljningsreturer, positiva justeringar och produktions- och monteringsutflöden.  
-   Summan av kostnaderna för de avgående transaktionerna som kopplades till inleveranserna i genomsnittskostnadsperioden subtraheras. De innehåller vanligtvis inköpsreturer och negativa utflöden.  
-   Delar med den totala lagerkvantiteten för slutet av genomsnittskostnadsperioden, exklusive lagerminskningar som håller på att värderas.  

 Denna beräknade genomsnittskostnad kopplas sedan till lagerminskningarna för artikeln (eller artikeln, lagerstället och varianten) med bokföringsdatum i perioden för genomsnittskostnad. Om en lagerökning finns som är fast kopplad till lagerminskningar i genomsnittskostnadsperioden, speditioneras den beräknade genomsnittskostnaden från ökningen till minskningen.  

### <a name="example-average-cost-period--day"></a>Exempel: Period för genomsnittskostnad = Dag  
 Följande exempel visar hur resultatet blir när genomsnittskostnaden beräknas baserat på genomsnittskostnadsperioden en dag. Fältet **Genoms. kost.ber.typ** i fönstret **Lagerinställning** är inställd på **Artikel**.  

 Följande tabell visar artikeltransaktionerna för exempelgenomsnittskostnadsartikeln, ARTIKEL1, innan batch-jobbet **Justera kostnad - Artikeltransaktioner** är färdigt.  

|**Bokföringsdatum**|**Artikeltransaktionstyp**|**Antal**|**Kost.belopp (aktuellt)**|**Löpnr**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Inköp|1|20.00|1|  
|01-01-20|Inköp|1|40.00|2|  
|01-01-20|Försäljning|-1|-20.00|3|  
|02-01-20|Försäljning|-1|-40.00|4|  
|02-02-20|Inköp|1|100,00|5|  
|02-03-20|Försäljning|-1|-100.00|6|  

> [!NOTE]  
>  Eftersom kostnadsjustering inte ännu har skett, motsvarar värdena i fältet **Kostnadsbelopp (Aktuellt)** för lagerminskningarna de lagerökningar som de är kopplade till.  

 Följande tabell visar de transaktioner i tabellen **Ingångspunkt för genomsn.kostn.justering** som gäller för värdetransaktionenerna som härrör från artikeltransaktionerna i föregående tabell.  

|**Artikelnr**|**Variantkod**|**Platskod**|**Värderingsdatum**|**Kostnaden är justerad**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|ARTIKEL1||BLÅ|01-01-20|Nej|  
|ARTIKEL1||BLÅ|02-01-20|Nej|  
|ARTIKEL1||BLÅ|02-02-20|Nej|  
|ARTIKEL1||BLÅ|02-03-20|Nej|  

 Följande tabell visar samma artikeltransaktioner efter att batch-jobbet **Justera kostnader - Artikeltransaktioner** är färdigt. Genomsnittskostnaden per dag beräknas och den används till lagerminskningarna.  

|**Bokföringsdatum**|**Artikeltransaktionstyp**|**Antal**|**Kost.belopp (aktuellt)**|**Löpnr**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Inköp|1|20.00|1|  
|01-01-20|Inköp|1|40.00|2|  
|01-01-20|Försäljning|-1|-30.00|3|  
|02-01-20|Försäljning|-1|-30.00|4|  
|02-02-20|Inköp|1|100,00|5|  
|02-03-20|Försäljning|-1|-100.00|6|  

### <a name="example-average-cost-period--month"></a>Exempel: Period för genomsnittskostnad = Månad  
 Följande exempel visar hur resultatet blir när genomsnittskostnaden beräknas baserat på genomsnittskostnadsperioden en månad. Fältet **Genoms. kost.ber.typ** i fönstret **Lagerinställning** är inställd på **Artikel**.  

 Om genomsnittskostnadsperioden är en månad skapas endast en transaktion för varje kombination av artikelnummer, variantkod, lagerställekod och värderingsdatum.  

 Följande tabell visar artikeltransaktionerna för exempelgenomsnittskostnadsartikeln, ARTIKEL1, innan batch-jobbet **Justera kostnad - Artikeltransaktioner** är färdigt.  

|**Bokföringsdatum**|**Artikeltransaktionstyp**|**Antal**|**Kost.belopp (aktuellt)**|**Löpnr**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Inköp|1|20.00|1|  
|01-01-20|Inköp|1|40.00|2|  
|01-01-20|Försäljning|-1|-20.00|3|  
|02-01-20|Försäljning|-1|-40.00|4|  
|02-02-20|Inköp|1|100,00|5|  
|02-03-20|Försäljning|-1|-100.00|6|  

> [!NOTE]  
>  Eftersom kostnadsjustering inte ännu har skett, motsvarar värdena i fältet **Kostnadsbelopp (Aktuellt)** för lagerminskningarna de lagerökningar som de är kopplade till.  

 Följande tabell visar de transaktioner i tabellen **Ingångspunkt för genomsn.kostn.justering** som gäller för värdetransaktionenerna som härrör från artikeltransaktionerna i föregående tabell.  

|**Artikelnr**|**Variantkod**|**Platskod**|**Värderingsdatum**|**Kostnaden är justerad**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|ARTIKEL1||BLÅ|01-31-20|Nej|  
|ARTIKEL1||BLÅ|02-28-20|Nej|  

> [!NOTE]  
>  Värderingsdatum anges till den sista dagen i genomsnittskostnadsperioden, som i det här fallet är den sista dagen i månaden.  

 Följande tabell visar samma artikeltransaktioner efter att batch-jobbet **Justera kostnader - Artikeltransaktioner** är färdigt. Genomsnittskostnaden per månad beräknas och den används till lagerminskningarna.  

|**Bokföringsdatum**|**Artikeltransaktionstyp**|**Antal**|**Kost.belopp (aktuellt)**|**Löpnr**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Inköp|1|20.00|1|  
|01-01-20|Inköp|1|40.00|2|  
|01-01-20|Försäljning|-1|-30.00|3|  
|02-01-20|Försäljning|-1|-65.00|4|  
|02-02-20|Inköp|1|100,00|5|  
|02-03-20|Försäljning|-1|-65.00|6|  

 Genomsnittskostnaden för transaktion nummer 3 beräknas i genomsnittskostnadsperioden för januari och genomsnittskostnaden för transaktionerna 4 och 6 beräknas i genomsnittskostnadsperioden för februari.  

 För att få fram genomsnittskostnaden för februari läggs genomsnittskostnaden för stycket som tas emot i lagret (100,00) till genomsnittskostnaden i början av perioden (30,00). Summan av de två (130,00) divideras sedan med det totala antalet i lagret (2). Det ger genomsnittskostnaden för artikeln i perioden februari (65,00). Genomsnittskostnaden tilldelas till lagerminskningarna i perioden (transaktionerna 4 och 6).  

## <a name="setting-the-valuation-date"></a>Ange värderingsdatum  
 Fältet **Värderingsdatum** i tabellen **Värdetransaktion** används för att bestämma i vilken genomsnittskostnadsperiod en lagerminskningspost tillhör. Det gäller även för PIA-lagret (produkter i arbete).  

 Följande tabell visar de villkor som används för att ange värderingsdatum.  

|Scenario|Bokföringsdatum|Antal|Omvärdering|Värderingsdatum|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positiv|Nej|Bokföringsdatum på artikeltransaktionen|  
|2|Senare än det senaste värderingsdatumet för kopplade värdetransaktioner|Negativt|Nej|Bokföringsdatum på artikeltransaktionen|  
|3|Tidigare än det senaste värderingsdatumet för kopplade värdetransaktioner|Positiv|Nej|Det senaste värderingsdatumet för de kopplade värdetransaktionerna|  
|4||Negativt|Ja|Bokföringsdatum för omvärderingsvärdetransaktionen.|  

### <a name="example"></a>Exempel  
 I följande tabell med värdetransaktioner visas de olika scenarierna.  

|Scenario|Bokföringsdatum|Artikeltransaktionstyp|Värderingsdatum|Antal|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01-01-20|Inköp|01-01-20|2|20.00|1|1|  
|2|01-15-20|(Artikelomkostnad)|01-01-20|2|8,00|1|2|  
|3|02-01-20|Försäljning|02-01-20|-1|-14.00|2|3|  
|4|03-01-20|(Omvärdering)|03-01-20|1|-.4.00|1|4|  
|5|02-01-20|Försäljning|03-01-20|-1|-10.00|3|5|  

> [!NOTE]  
>  I löpnummer 5 i den föregående tabellen har användaren angett en försäljningsorder med ett bokföringsdatum (02-01-20) som kommer före det senaste värderingsdatumet för kopplade värdetransaktioner (03-01-20). Om det motsvarande värdet i fältet **Kostnadsbelopp (Aktuell)** för datumet (02-01-20) användes för transaktionen, skulle det vara 14,00. Det skapar en situation där antalet i lagret är noll, men lagervärdet är – 4,00.  
>   
>  För att undvika en sådan obalans mellan antal-värde anges ett värderingsdatum som motsvarar det senaste värderingsdatumet för de kopplade värdetransaktionerna (03-01-20). Värdet i fältet **Kostnadsbelopp (Aktuell)** förblir 10,00 (efter omvärderingen), vilket betyder att antalet i lager är noll, och lagervärdet också är noll.  

> [!CAUTION]  
>  Eftersom rapporten **Lagervärdering** baseras på bokföringsdatumet, kommer rapporten att visa alla antal och värden som inte överensstämmer i scenarier som i exemplet ovan. Mer information finns i [Designdetaljer: Lagervärdering](design-details-inventory-valuation.md)  

 Om antalet i lager är mindre än noll när du har bokfört lagerminskningen, anges värderingsdatumet först som bokföringsdatumet för lagerminskningen. Datumet kan ändras senare enligt reglerna som beskrivs i anmärkningen i det tidigare avsnitt, när lagerökningen kopplas.  

## <a name="recalculating-average-cost"></a>Beräkna om genomsnittskostnad  
 Värdering av lagerminskningar som ett vägt medeltal skulle vara okomplicerat om inköp alltid fakturerades innan försäljningar faktureras, bokföringar aldrig bakåtdaterades och du aldrig gjorde misstag. Däremot skiljer sig verkligheten något sig från idealet.  

 Som illustreras i exemplen i det här avsnittet definieras värderingsdatumet som datumet från vilket värdetransaktionen inkluderas i beräkningen av genomsnittskostnaden. Detta ger dig flexibilitet att göra följande för artiklar som använder värderingsprincipen Genomsnitt:  

-   Fakturera försäljningen av en artikel innan köpet av artikeln har fakturerats.  
-   Bakåtdatera en bokföring.  
-   Återställ en felaktig bokföring.  

> [!NOTE]  
>  En annan anledning för den flexibiliteten är fast koppling. Läs mer om fast koppling i [Designdetaljer: artikelkoppling](design-details-item-application.md).  

 På grund av den flexibiliteten kanske du måste beräkna om genomsnittskostnaden när den relaterade bokföringen har uppstått. Till exempel, om du bokför en lagerökning eller en minskning med ett värderingsdatum som kommer före en eller flera lagerminskningar. Omberäkningen av genomsnittskostnaden sker automatiskt när du kör batchjobbet **Justera kostnad - Artikeltransaktioner** manuellt eller automatiskt.  

 Det är möjligt att ändra lagervärderingsbasen inom en bokföringsperiod genom att ändra fältet **Period för genomsnittskostnad** och fältet **Genoms. kost.ber.typ**. Du bör göra det med omsorg och i samförstånd med en revisor.  

### <a name="example"></a>Exempel  
 Följande exempel visar hur genomsnittskostnaden omberäknas när en sen bokföring introduceras på ett datum som kommer före en eller flera lagerminskningar. Exemplet baseras på genomsnittskostnadsperioden **Dag**.  

 Följande tabell visar de värdetransaktioner som finns för artikeln innan bokföringen har tillkommit.  

|Värderingsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|02-15-20|-1|-15.00|3|  
|02-16-20|-1|-15.00|4|  

 Användaren bokför en lagerökning (löpnummer 5) med ett värderingsdatum (01-03-20) som kommer före en eller flera lagerminskningar. För att balansera lagret måste genomsnittskostnaden omberäknas och justeras till 17,00.  

 Följande tabell visar de värdetransaktioner som finns för artikeln när löpnummer 5 har tillkommit.  

|Värderingsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|01-03-20|1|21.00|5|  
|02-15-20|-1|-17.00|3|  
|02-16-20|-1|-17.00|4|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)   
 [Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)   
 [Designdetaljer: Artikelkoppling](design-details-item-application.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

