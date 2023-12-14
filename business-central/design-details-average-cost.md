---
title: Designdetaljer – Genomsnittskostnad
description: Genomsnittskostnaden för en artikel beräknas med ett periodiskt viktat medelvärde.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
---
# Designdetaljer: Genomsnittskostnad

Genomsnittskostnaden för en artikel beräknas med ett periodiskt viktat medelvärde. Medelvärdet baseras på den genomsnittskostnadsperiod som har angetts i [!INCLUDE[prod_short](includes/prod_short.md)].  

Värderingsdatum anges automatiskt.  

## Ställa in beräkning av genomsnittskostnad

Följande tabell beskriver de två fälten på sidan **Lagerinställningar** som måste fyllas för att aktivera beräkning av genomsnittskostnader.  

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Period för genomsnittskostnad**|Anger vilken period genomsnittskostnaden beräknas i. Följande alternativ finns:<br /><br /> - **Dag**<br />- **Vecka**<br />- **Månad**<br />- **Bokföringsperiod**<br /><br /> Genomsnittskostnaden beräknas för aktuell period för lagerminskningar som bokfördes inom den angivna genomsnittskostnadsperioden.|  
|**Genoms. kost.ber.typ**|Anger hur genomsnittskostnaden beräknas. Följande alternativ finns:<br /><br /> - **Artikel**<br />- **Artikel, Variant och Lagerställe**<br /> Med det här alternativet beräknas genomsnittskostnaden för varje artikel, för varje lagerställe och för varje variant av artikeln. Genomsnittskostnaden för den här artikeln styrs av var den lagras och vilken variant du har valt, som färg.|  

> [!NOTE]  
> Du kan endast använda en genomsnittskostnadsperiod och beräkningstyp för genomsnittskostnad under ett räkenskapsår.  
>
> Sidan **Bokföringsperioder** visar genomsnittskostnadsperioden och vilken beräkningstyp för genomsnittskostnad som används under perioden, för varje bokföringsperiod.  

## Beräkna genomsnittskostnad

 När du bokför en transaktion för en artikel som använder metoden Genomsnittskostnad skapas en transaktion i tabellen **Ingångspunkt för genomsn.kostn.justering**. Den här transaktionen innehåller transaktionens artikelnummer, variantkod och lagerställeskod. Transaktionen innehåller fältet **Värderingsdatum** som anger det senaste datumet i genomsnittskostnadsperioden som transaktionen bokfördes i.  

> [!NOTE]  
> Detta fält ska inte förväxlas med fältet i tabellen **Värderingsdatum** i tabellen **Värdetransaktion** som innehåller datumet då värdet börjar gälla och används för att fastställa genomsnittskostnadsperioden som värdetransaktionen tillhör.  

 Genomsnittskostnaden för en transaktion beräknas när artikelns kostnad justeras. Mer information finns i [Designdetaljer: kostnadsjustering](design-details-cost-adjustment.md). En kostnadsjustering använder transaktionerna i tabellen **Ingångspunkt för genomsn.kostn.justering** för att identifiera vilka artiklar (eller artiklar, lagerställen och varianter) som genomsnittskostnader ska beräknas för. För varje transaktion med kostnad som ännu inte har justerats, använder kostnadsjustering följande för att fastställa genomsnittskostnaden:  

- Kostnaden för artikeln i början av genomsnittskostnadsperioden fastställs.  
- Summan av inkommande kostnader som bokfördes i genomsnittskostnadsperioden adderas. De innehåller inköp, försäljningsreturer, positiva justeringar och produktions- och monteringsutflöden.  
- Summan av kostnaderna för de utgående transaktionerna som kopplades till inleveranserna i genomsnittskostnadsperioden subtraheras. De innehåller vanligtvis inköpsreturer och negativa utflöden.  
- Det totala lagerantalet för slutet av genomsnittskostnadsperioden divideras. Exkluderar lagerminskningar som värderas.  

 Denna beräknade genomsnittskostnad kopplas sedan till lagerminskningarna för artikeln (eller artikeln, lagerstället och varianten) med bokföringsdatum i perioden för genomsnittskostnad. För lagerökningar som är fast kopplade till lagerminskningar i genomsnittskostnadsperioden [!INCLUDE [prod_short](includes/prod_short.md)] flyttar fram den beräknade genomsnittskostnaden från ökningen till minskningen.  

### Exempel: Period för genomsnittskostnad = Dag

Följande exempel visar hur resultatet blir när genomsnittskostnaden beräknas baserat på genomsnittskostnadsperioden en dag. Fältet **Genoms. kost.ber.typ** på sidan **Lagerinställning** är inställd på **Artikel**.  

Följande tabell visar artikeltransaktionerna för exempelgenomsnittskostnadsartikeln, ARTIKEL1, innan batch-jobbet **Justera kostnad – Artikeltransaktioner** är färdigt.  

| **Bokföringsdatum** | **Artikeltransaktionstyp** | **Antal** | **Kost.belopp (faktiskt)** | **Löpnr** |
|--|--|--|--|--|
| 01-01-23 |   Inköp | 1 | 20.00 | 1 |
| 01-01-23 |   Inköp | 1 | 40.00 | 2 |
| 01-01-23 |   Försäljning | -1 | -20.00 | 3 |
| 02-01-23 |   Försäljning | -1 | -40.00 | 4 |
| 02-02-23 |   Inköp | 1 | 100.00 | 5 |
| 02-03-23 |   Försäljning | -1 | -100.00 | 6 |

> [!NOTE]  
> Eftersom kostnadsjustering inte ännu har skett, motsvarar värdena i fältet **Kostnadsbelopp (Aktuellt)** för lagerminskningarna de lagerökningar som de är kopplade till.  

 Följande tabell visar de transaktioner i tabellen **Ingångspunkt för genomsn.kostn.justering** som resulterar från värdetransaktionerna som härrör från artikeltransaktionerna i föregående tabell.  

| **Artikelnr** | **Variantkod** | **Platskod** | **Värderingsdatum** | **Kostnaden är justerad** |
|--|--|--|--|--|
| ARTIKEL1 |  | BLÅ | 01-01-23 |   Nej |
| ARTIKEL1 |  | BLÅ | 02-01-23 |   Nej |
| ARTIKEL1 |  | BLÅ | 02-02-23 |   Nej |
| ARTIKEL1 |  | BLÅ | 02-03-23 |   Nej |

 Följande tabell visar samma artikeltransaktioner efter att batch-jobbet **Justera kostnader – Artikeltransaktioner** är färdigt. Genomsnittskostnaden per dag beräknas och den används till lagerminskningarna.  

| **Bokföringsdatum** | **Artikeltransaktionstyp** | **Antal** | **Kost.belopp (faktiskt)** | **Löpnr** |
|--|--|--|--|--|--|
| 01-01-23 |   Inköp | 1 | 20.00 | 1 |
| 01-01-23 |   Inköp | 1 | 40.00 | 2 |
| 01-01-23 |   Försäljning | -1 | -30.00 | 3 |
| 02-01-23 |   Försäljning | -1 | -30.00 | 4 |
| 02-02-23 |   Inköp | 1 | 100.00 | 5 |
| 02-03-23 |   Försäljning | -1 | -100.00 | 6 |

### Exempel: Period för genomsnittskostnad = Månad

 Detta exempel visar hur resultatet blir när genomsnittskostnaden beräknas baserat på genomsnittskostnadsperioden en månad. Fältet **Genoms. kost.ber.typ** på sidan **Lagerinställning** är inställd på **Artikel**.  

 Om genomsnittskostnadsperioden är en månad skapar [!INCLUDE [prod_short](includes/prod_short.md)] en transaktion för varje kombination av artikelnummer, variantkod, lagerställekod och värderingsdatum.  

 Följande tabell visar artikeltransaktionerna för exempelgenomsnittskostnadsartikeln, ARTIKEL1, innan batch-jobbet **Justera kostnad – Artikeltransaktioner** är färdigt.  

| **Bokföringsdatum** | **Artikeltransaktionstyp** | **Antal** | **Kost.belopp (faktiskt)** | **Löpnr** |
|--|--|--|--|--|
| 01-01-23 |   Inköp | 1 | 20.00 | 1 |
| 01-01-23 |   Inköp | 1 | 40.00 | 2 |
| 01-01-23 |   Försäljning | -1 | -20.00 | 3 |
| 02-01-23 |   Försäljning | -1 | -40.00 | 4 |
| 02-02-23 |   Inköp | 1 | 100.00 | 5 |
| 02-03-23 |   Försäljning | -1 | -100.00 | 6 |

> [!NOTE]  
> Eftersom kostnadsjustering inte ännu har skett, motsvarar värdena i fältet **Kostnadsbelopp (Aktuellt)** för lagerminskningarna de lagerökningar som de är kopplade till.  

Följande tabell visar de transaktioner i tabellen **Ingångspunkt för genomsn.kostn.justering** som resulterar från värdetransaktionerna som härrör från artikeltransaktionerna i föregående tabell.  

| **Artikelnr** | **Variantkod** | **Platskod** | **Värderingsdatum** | **Kostnaden är justerad** |
|--|--|--|--|--|
| ARTIKEL1 |  | BLÅ | 01-31-23 |   Nej |
| ARTIKEL1 |  | BLÅ | 02-28-23 |   Nej |

> [!NOTE]  
> Värderingsdatum anges till den sista dagen i genomsnittskostnadsperioden, som i det här fallet är den sista dagen i månaden.  

Följande tabell visar samma artikeltransaktioner efter att batch-jobbet **Justera kostnader – Artikeltransaktioner** är färdigt. Genomsnittskostnaden per månad beräknas och den används till lagerminskningarna.  

|**Bokföringsdatum** | **Artikeltransaktionstyp** | **Antal** | **Kost.belopp (faktiskt)** | **Löpnr** |
|--|--|--|--|--|
| 01-01-23 | Inköp | 1 | 20.00 | 1 |
| 01-01-23 | Inköp | 1 | 40.00 | 2 |
| 01-01-23 | Försäljning | -1 | -30.00 | 3 |
| 02-01-23 | Försäljning | -1 | -65.00 | 4 |
| 02-02-23 | Inköp | 1 | 100.00 | 5 |
| 02-03-23 | Försäljning | -1 | -65.00 | 6 |

Den genomsnittliga kostnaden för löpnummer 3 beräknas i genomsnittskostnadsperioden för januari. Den genomsnittliga kostnaden för transaktioner 4 och 6 beräknas i genomsnittskostnadsperioden för februari.  

För att få fram genomsnittskostnaden för februari lägger [!INCLUDE [prod_short](includes/prod_short.md)] genomsnittskostnaden för den inlevererade artikeln i lagret (100,00) till genomsnittskostnaden i början av perioden (30,00). Summan (130,00) divideras sedan med den totala kvantiteten i lagret (2). Den här beräkningen ger den resulterande genomsnittskostnaden för artikeln i perioden februari (65,00). Genomsnittskostnaden tilldelas till lagerminskningarna i perioden (transaktionerna 4 och 6).  

## Ange värderingsdatum

 Fältet **Värderingsdatum** i tabellen **Värdetransaktion** bestämmer i vilken genomsnittskostnadsperiod som en lagerminskningspost tillhör. Denna inställning gäller även för PIA-lagret (produkter i arbete).  

 Följande tabell visar de villkor som används för att ange värderingsdatum.  

| Scenario | Bokföringsdatum | Antal | Omvärdering | Värderingsdatum |
|--|--|--|--|--|
| 1 |  | Positiv | Nej | Bokföringsdatum på artikeltransaktionen |
| 2 | Senare än det senaste värderingsdatumet för kopplade värdetransaktioner | Negativt | Nej | Bokföringsdatum på artikeltransaktionen |
| 3 | Tidigare än det senaste värderingsdatumet för kopplade värdetransaktioner | Positiv | Nej | Det senaste värderingsdatumet för de kopplade värdetransaktionerna |
| 4 |  | Negativt | Ja | Bokföringsdatum för omvärderingsvärdetransaktionen. |

### Exempel

I följande tabell med värdetransaktioner visas de olika scenarierna.  

| Scenario | Bokföringsdatum | Artikeltransaktionstyp | Värderingsdatum | Antal | Kost.belopp (aktuellt) | Artikeltrans.löpnr | Löpnr |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Inköp | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 01-15-20 | (Artikelomkostnad) | 01-01-20 | 2 | 8,00 | 1 | 2 |
| 3 | 02-01-20 | Försäljning | 02-01-20 | -1 | -14.00 | 2 | 3 |
| 4 | 03-01-20 | (Omvärdering) | 03-01-20 | 1 | -.4.00 | 1 | 4 |
| 5 | 02-01-20 | Försäljning | 03-01-20 | -1 | -10.00 | 3 | 5 |

> [!NOTE]  
> I löpnummer 5 i den föregående tabellen har användaren angett en försäljningsorder med ett bokföringsdatum (02-01-20) som kommer före det senaste värderingsdatumet för kopplade värdetransaktioner (03-01-20). Om det motsvarande värdet i fältet **Kostnadsbelopp (Aktuell)** för datumet (02-01-20) användes för transaktionen, skulle det vara 14,00. Det skapar en situation där antalet i lagret är noll, men lagervärdet är – 4,00.  
>
> För att undvika en sådan obalans mellan antal-värde anges ett värderingsdatum som motsvarar det senaste värderingsdatumet för de kopplade värdetransaktionerna (03-01-20). Värdet i fältet **Kostnadsbelopp (Aktuell)** förblir 10,00 (efter omvärderingen), vilket betyder att antalet i lager är noll, och lagervärdet också är noll.  

> [!CAUTION]  
> Eftersom rapporten **Lagervärdering** baseras på bokföringsdatumet, kommer rapporten att visa alla antal och värden som inte överensstämmer i scenarier som i exemplet ovan. Mer information finns i [Designdetaljer: Lagervärdering](design-details-inventory-valuation.md)  

Om antalet i lager är mindre än noll när du har bokfört lagerminskningen, anges värderingsdatumet som bokföringsdatumet för lagerminskningen. Du kan ändra detta datum när lagerökningen tillämpas, enligt reglerna som beskrivs i anteckningen tidigare i detta avsnitt.  

## Beräkna om genomsnittskostnad

Att värdera lagerminskningar som ett viktat medelvärde kan vara okomplicerade i flera fall:

- Inköp faktureras alltid före försäljning.
- Bokföringar blir aldrig bakåtdaterade.
- Du har aldrig gjort misstag.

Verkligheten är dock annorlunda.  

Som exemplet illustrerar i det här avsnittet definieras värderingsdatumet som datumet från vilket värdetransaktionen inkluderas i beräkningen av genomsnittskostnaden. Med den här inställningen kan du göra flera saker för artiklar med värderingsprincipen genomsnitt:  

- Fakturera försäljningen av en artikel innan du fakturerar köpet.  
- Bakåtdatera en bokföring.  
- Återställ en felaktig bokföring.  

> [!NOTE]  
> En annan anledning för den flexibiliteten är fast koppling. Läs mer om fast koppling i [Designdetaljer: artikelkoppling](design-details-item-application.md).  

På grund av den flexibiliteten kanske du måste beräkna om genomsnittskostnaden efter bokföringen. Till exempel, om du bokför en lagerökning eller en minskning med ett värderingsdatum som kommer före en lagerminskning. Omberäkningen av genomsnittskostnaden sker automatiskt när du kör batchjobbet **Justera kostnad – Artikeltransaktioner** manuellt eller automatiskt.  

Du kan ändra lagervärderingsbasen inom en bokföringsperiod genom att ändra värdena i fältet **Period för genomsnittskostnad** och fältet **Genoms. kost.ber.typ**. Vi rekommenderar dock att du är försiktig och rådfrågar granskaren.  

### Exempel på omräknad genomsnittlig kostnad

I det här exemplet visas hur [!INCLUDE [prod_short](includes/prod_short.md)] beräknar om genomsnittskostnaden om när du bokför på ett datum som ligger före en lagerminskning. Exemplet baseras på genomsnittskostnadsperioden **Dag**.  

Följande tabell visar de värdetransaktioner som finns för artikeln innan bokföringen har tillkommit.  

| Värderingsdatum | Antal | Kost.belopp (aktuellt) | Löpnr |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15.00 | 3 |
| 02-16-20 | -1 | -15.00 | 4 |

Användaren bokför en lagerökning (löpnummer 5) med ett värderingsdatum (01-03-20) som kommer före en lagerminskning. För att balansera lagret måste genomsnittskostnaden omberäknas och justeras till 17,00.  

Följande tabell visar de värdetransaktioner som finns för artikeln när löpnummer 5 har tillkommit.  

| Värderingsdatum | Antal | Kost.belopp (aktuellt) | Löpnr |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17.00 | 3 |
| 02-16-20 | -1 | -17.00 | 4 |

## Se även

[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ord lista över termer i Dynamics 365 affärsprocesser](/dynamics365/guidance/business-processes/glossary)  
[Definiera översikt över produkt- och tjänstkostnader](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
