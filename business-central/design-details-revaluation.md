---
title: Designdetaljer - Omvärdering | Microsoft Docs
description: Du kan omvärdera lagret utifrån den värderingsbas som bäst återspeglar lagervärdet. Du kan också bakåtdatera en omvärdering, så att kostnaden för sålda varor (KSV) uppdateras korrekt för artiklar som redan har sålts. Artiklar som använder värderingsprincipen Standard, som inte har fakturerats helt, kan också omvärderas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d0e779587a409232a6ab618ec80f5ad1ae17e31f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184778"
---
# <a name="design-details-revaluation"></a>Designdetaljer: Omvärdering
Du kan omvärdera lagret utifrån den värderingsbas som bäst återspeglar lagervärdet. Du kan också bakåtdatera en omvärdering, så att kostnaden för sålda varor (KSV) uppdateras korrekt för artiklar som redan har sålts. Artiklar som använder värderingsprincipen Standard, som inte har fakturerats helt, kan också omvärderas.  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] stöds följande flexibilitet för omvärdering:  

-   Det antal som kan omvärderas kan beräknas för vissa datum, även bakåt i tid.  
-   För artiklar som använder värderingsprincipen Standard tas förväntade kostnadstransaktioner med i omvärderingen.  
-   Lagerminskningar som påverkas av omvärdering har identifierats.  

## <a name="calculating-the-revaluable-quantity"></a>Beräknar antal som kan omvärderas  
 Det antal som kan omvärderas är det återstående antal på lagret som är tillgängligt för omvärdering på ett givet datum. Det beräknas som totalsumma av antalet fullständigt fakturerade artikeltransaktioner som har ett bokföringsdatum som är lika med eller tidigare än omvärderingbokföringsdatumet.  

> [!NOTE]  
>  Artiklar som använder värderingsprincipen Standard hanteras på annat sätt när du beräknar det omvärderingsbara antalet per artikel, lagerställe och variant. Antal och värden i artikeltransaktioner som inte har fakturerats helt ingår i det antal som kan omvärderas.  

När en omvärdering har bokförts kan du bokföra en lagerökning eller en minskning med ett bokföringsdatum som kommer före omvärderingsbokföringsdatumet. Emellertid påverkas inte antalet av omvärderingen. För att balansera lagret beaktas endast det ursprungliga antal som kan omvärderas.  

Eftersom omvärderingen kan göras vilket datum som helst, måste du ha regler för när en artikel anses vara en del av lagret från en ekonomisk synvinkel. Till exempel, när artikeln finns i lager och när artikeln är produkter i arbete (PIA).  

### <a name="example"></a>Exempel  
Följande exempel visar när en PIA-artikel övergår till att bli en del av lagret. Följande exempel baseras på produktionen av en kedja med 150 länkar.  

![PIA - omvärdering av lager](media/design_details_inventory_costing_10_revaluation_wip.png "PIA - omvärdering av lager")  

**1Q**: Användaren bokför de inköpta länkarna som inlevererade. Följande tabell visar den resulterande artikeltransaktionen.  

|Bokföringsdatum|Artikel|Transaktionstyp|Antal|Löpnr|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|LÄNK|Inköp|150|1|  

> [!NOTE]  
>  Nu finns en artikel som använder värderingsprincipen Standar, tillgänglig för omvärdering.  

**1V**: Användaren bokför de inköpta länkarna som fakturerade och länkarna blir en del av lagret, från en ekonomisk synvinkel. Följande tabell visar de resulterande värdetransaktionerna.  

|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Inköpskostnad|01-01-20|150.00|1|1|  

 **2Q + 2V**: Användaren bokför de inköpta länkarna som förbrukade för produktionen av järnkedjan. Från en ekonomisk synvinkel blir länkarna en del av PIA-lagret.  Följande tabell visar den resulterande artikeltransaktionen.  

|Bokföringsdatum|Artikel|Transaktionstyp|Antal|Löpnr|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|LÄNK|Förbrukning|-150|1|  

Följande tabell visar den resulterande värdetransaktionen.  

|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|Inköpskostnad|02-01-20|-150.00|2|2|  

Värderingsdatum anges till datumet för förbrukningsbokföringen (02-01-20), som en vanlig lagerminskning.  

**3Q**: Användaren bokför kedjan som utflöde och avslutar produktionsordern. Följande tabell visar den resulterande artikeltransaktionen.  

|Bokföringsdatum|Artikel|Transaktionstyp|Antal|Löpnr|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|KEDJA|Utflöde|1|3|  

**3V**: Användare kör batch-jobbet **Justera kost. - artikeltran.** som bokför kedjan som fakturerad för att ange att all materialförbrukning har förbrukats helt. Från en ekonomisk synvinkel är länkarna inte längre en del av PIA-lagret när utflödet faktureras och justeras fullständigt. Följande tabell visar de resulterande värdetransaktionerna.  

|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Inköpskostnad|01-01-20|150.00|2|2|  
|02-01-20|Inköpskostnad|02-01-20|-150.00|2|2|  
|02-15-20|Inköpskostnad|02-15-20|150.00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Förväntade kostnader i omvärdering  
Det antal som kan omvärderas XE "antal som kan omvärderas" XE "Antal;kan omvärderas" beräknas som summan av antalet XE "antal" för fullständigt fakturerade XE "faktura" artikeltransaktioner XE "artikeltransaktion" med bokföringsdatum samtidigt som eller tidigare än datumet för omvärderingen XE "omvärdering". Det betyder att när vissa artiklar har inlevererats/levererats men inte fakturerats kan deras lagervärde inte beräknas XE "Lagervärde". Artiklar som använder värderingsprincipen Standard begränsas inte i detta avseende. XE ”värde”  

> [!NOTE]  
>  En annan typ av förväntad kostnad som kan omvärderas är PIA-lagret, enligt vissa regler. Mer information finns i avsnittet “PIA Lager - omvärdering” i den här artikeln.  

När du beräknar det omvärderingsbara antalet för artiklar som använder värderingsprincipen Standard, tas artikeltransaktioner med som inte har fakturerats helt och ingår i beräkningen. Dessa transaktioner omvärderas sedan när du bokför omvärderingen. När du fakturerar den omvärderade transaktionen skapas följande värdetransaktioner:  

-   Den vanliga fakturerade värdetransaktionen med transaktionstypen **Direkt kostnad**. Kostnadsbeloppet för den här transaktionen är den direkta kostnaden från källraden.  
-   En värdetransaktion med transaktionstypen **Varians**. Den här transaktionen registrerar skillnaden mellan det fakturerade kostnaden och den omvärderade standardkostnaden.  
-   En värdetransaktion med transaktionstypen **Omvärdering**. Den här transaktionen registrerar återföringen av omvärdering av den förväntade kostnaden.  

### <a name="example"></a>Exempel  
Följande exempel, baserat på produktionen av kedjan i föregående exempel, visar hur de tre typerna av transaktioner skapas. Det baseras på följande scenario:  

1.  Användaren bokför de inköpta länkarna som inlevererade med en styckkostnad på BVA 2,00.  
2.  Användaren bokför sedan en omvärdering av länkarna med en ny styckkostnad på BVA 3,00 som uppdaterar standardkostnaden till BVA 3,00.  
3.  Användaren bokför det ursprungliga inköpet av länkarna som fakturerat, vilket skapar följande:  

    1.  En fakturerad värdetransaktion med transaktionstypen **Direkt kostnad**.  
    2.  En värdetransaktion med transaktionstypen **Omvärdering** för att registrera återföringen av omvärderingen av förväntade kostnader.  
    3.  En värdetransaktion med transaktionstypen Varians som registrerar skillnaden mellan den fakturerade kostnaden och den omvärderade standardkostnaden.  
Följande tabell visar de resulterande värdetransaktionerna.  

|Steg|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Kost.belopp (förväntat)|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Inköpskostnad|01-15-20|300.00|0,00|1|1|  
|2.|01-20-20|Omvärdering|01-20-20|150.00|0,00|1|2|  
|3.a.|01-15-20|Inköpskostnad|01-15-20|-300.00|0,00|1|3|  
|3.b.|01-15-20|Omvärdering|01-20-20|-150.00|0,00|1|4|  
|3.c.|01-15-20|Varians|01-15-20|0,00|450.00|1|5|  

## <a name="determining-if-an-inventory-decrease-is-affected-by-revaluation"></a>Fastställa om en lagerminskning påverkas av omvärderingen  
Datumet för bokföringen eller omvärderingen används för att bestämma om en lagerminskning påverkas av en omvärdering.  

Följande tabell visar de villkor som används för en artikel som inte använder värderingsprincipen Genomsnitt.  

|Scenario|Löpnr|Tidsplan|Påverkat av omvärdering|  
|--------------|---------------|------------|-----------------------------|  
|A|Tidigare än omvärderingstransaktionsnummer|Tidigare än omvärderingbokföringsdatum|Nej|  
|B|Tidigare än omvärderingstransaktionsnr.|Lika med omvärderingbokföringsdatumet|Nej|  
|L|Tidigare än omvärderingstransaktionsnr.|Senare än omvärderingbokföringsdatum|Ja|  
|D|Senare än omvärderingstransaktionsnr.|Tidigare än omvärderingbokföringsdatum|Ja|  
|Ö|Senare än omvärderingstransaktionsnr.|Lika med omvärderingbokföringsdatumet|Ja|  
|K|Senare än omvärderingstransaktionsnr.|Senare än omvärderingbokföringsdatum|Ja|  

### <a name="example"></a>Exempel  
Följande exempel, som visar omvärdering av en artikel som använder FIFO-värderingsprincipen, baseras på följande scenariot:  

1.  Den 01-01-20 bokför användaren ett inköp på 6 enheter.  
2.  Den 02-01-20 bokför användaren en försäljning på 1 enhet.  
3.  Den 03-01-20 bokför användaren en försäljning på 1 enhet.  
4.  Den 04-01-20 bokför användaren en försäljning på 1 enhet.  
5.  Den 03-01-20 beräknar användaren lagervärdet för artikeln och bokför en omvärdering av artikelns styckkostnad från BVA 10,00 till BVA 8,00.  
6.  Den 02-01-20 bokför användaren en försäljning på 1 enhet.  
7.  Den 03-01-20 bokför användaren en försäljning på 1 enhet.  
8.  Den 04-01-20 bokför användaren en försäljning på 1 enhet.  
9. Användaren kör batch-jobbet  **Justera kost. - artikeltrans.**  

Följande tabell visar de resulterande värdetransaktionerna.  

|Scenario|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Antal|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Inköp|01-01-20|6|60,00|1|1|  
||03-01-20|Omvärdering|03-01-20|4|-8.00|1|5|  
|A|02-01-20|Försäljning|02-01-20|-1|-10.00|2|2|  
|B|03-01-20|Försäljning|03-01-20|-1|-10.00|3|3|  
|L|04-01-20|Försäljning|04-01-20|-1|-10.00|4|4|  
||04-01-20|Försäljning|04-01-20|-1|2,00|4|9|  
|D|02-01-20|Försäljning|03-01-20|-1|-10.00|5|6|  
||02-01-20|Försäljning|03-01-20|-1|2,00|5|10|  
|Ö|03-01-20|Försäljning|03-01-20|-1|-10.00|6|7|  
||03-01-20|Försäljning|03-01-20|-1|2,00|6|11|  
|K|04-01-20|Försäljning|04-01-20|-1|-10.00|7|8|  
||04-01-20|Försäljning|04-01-20|-1|2,00|7|12|  

## <a name="wip-inventory-revaluation"></a>PIA - Omvärdering av lager  
Omvärdering av PIA-lagret betyder omvärdering av komponenter som är registrerade som en del av PIA-lagret vid tidpunkten för omvärdering.  

Med det i åtanke är det viktigt att skapa regler för när en artikel anses vara en del av PIA-lagret från en ekonomisk synvinkel. I [!INCLUDE[d365fin](includes/d365fin_md.md)] finns följande regler:  

-   En inhandlad komponent blir en del av råmateriallagret från tidpunkten då ett inköp bokförs som fakturerat.  
-   Den inköpta/detaljmonterade komponenten ingår i PIA-lagret från tidpunkten då dess förbrukning bokförs i samband med en produktionsorder.  
-   En inköpt/detaljmonterad komponent ingår i PIA-lagret tills en produktionsorder (tillverkad artikel) faktureras.  

Sättet som värderingsdatumet för värdetransaktionen av förbrukning har angetts följer samma regler som för icke-PIA-lager. Mer information finns i avsnittet "Fastställa om en lagerminskning påverkas av omvärderingen" i det här avsnittet.  

PIA-lagret kan omvärderas förutsatt att omvärderingdatumet inte är tidigare än bokföringsdatumet för motsvarande artikeltransaktioner av typen Förbrukning, och förutsatt att motsvarande produktionsorder inte har fakturerats ännu.  

> [!CAUTION]  
>  Rapporten **Lagervärdering - PIA** visar värdet för bokförda produktionsordertransaktioner och kan därför vara lite förvirrande för PIA-artiklar som har omvärderats.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)   
 [Designdetaljer: Lagervärdering](design-details-inventory-valuation.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
