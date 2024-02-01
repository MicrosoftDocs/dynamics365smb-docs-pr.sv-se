---
title: Designdetaljer – Omvärdering
description: Du kan omvärdera lagret utifrån den värderingsbas som bäst återspeglar lagervärdet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Designdetaljer: Omvärdering

Du kan omvärdera lagret utifrån den värderingsbas som bäst återspeglar lagervärdet. Du kan också bakåtdatera en omvärdering för att korrekt uppdatera kostnaden för sålda varor (KSV) för artiklar du redan har sålt. Artiklar som använder värderingsprincipen Standard och inte har fakturerats helt, kan också omvärderas.  

I [!INCLUDE[prod_short](includes/prod_short.md)] stöds följande flexibilitet för omvärdering:  

- Det antal som kan omvärderas kan beräknas för vissa datum, även bakåt i tid.  
- För artiklar som använder värderingsprincipen Standard tas förväntade kostnadstransaktioner med i omvärderingen.  
- Lagerminskningar som påverkas av omvärdering har identifierats.  

## Beräkna antal som kan omvärderas

Det antal som kan omvärderas är det återstående lager som är tillgängligt på ett givet datum. Antalet är summan av fullständigt fakturerade artikeltransaktioner som du bokför på eller före omvärderingsdatumet.  

> [!NOTE]  
>  Artiklar som använder värderingsprincipen Standard hanteras på annat sätt när du beräknar det omvärderingsbara antalet per artikel, lagerställe och variant. Antal och värden i artikeltransaktioner som inte har fakturerats helt ingår i det antal som kan omvärderas.  

När en omvärdering har bokförts kan du bokföra en lagerökning eller en minskning med ett bokföringsdatum som kommer före omvärderingsbokföringsdatumet. Emellertid påverkas inte antalet av omvärderingen. För att balansera lagret beaktas endast det ursprungliga antal som kan omvärderas.  

Eftersom du lan omvärdera vilket datum som helst, måste du ha regler för när du anser att en artikel är en del av lagret. Till exempel, när artikeln finns i lager och när artikeln är produkter i arbete (PIA).  

### Exempel  

Följande exempel visar när en PIA-artikel övergår till att bli en del av lagret. Följande exempel baseras på produktionen av en kedja med 150 länkar.  

![PIA – omvärdering av lager.](media/design_details_inventory_costing_10_revaluation_wip.png "PIA – omvärdering av lager")  

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

**3V**: Användare kör batch-jobbet **Justera kost. – artikeltran.** som bokför kedjan som fakturerad för att ange att all materialförbrukning har förbrukats helt. Från en ekonomisk synvinkel är länkarna inte längre en del av PIA-lagret när utflödet faktureras och justeras fullständigt. Följande tabell visar de resulterande värdetransaktionerna.  

|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Inköpskostnad|01-01-20|150.00|2|2|  
|02-01-20|Inköpskostnad|02-01-20|-150.00|2|2|  
|02-15-20|Direkt kostnad|02-15-20|150.00|3|3|  

## Förväntade kostnader i omvärdering

De antal du kan omvärdera är summan av antalet för fullständigt fakturerade artikeltransaktioner som du bokfört på eller före omvärderingsdatumet. När vissa artiklar har inlevererats eller levererats men inte fakturerats kan du inte beräkna deras lagervärde. Artiklar som använder värderingsprincipen Standard begränsas inte på detta sätt.  

> [!NOTE]  
>  En annan typ av förväntad kostnad som kan omvärderas är PIA-lagret, enligt vissa regler. Mer information finns i [Omvärdera PIA-lager](design-details-revaluation.md#wip-inventory-revaluation).  

När du beräknar det omvärderingsbara antalet för artiklar som använder värderingsprincipen Standard, i beräkningen ingår reskontraposter som inte är fullständigt fakturerade. Dessa transaktioner omvärderas sedan när du bokför omvärderingen. När du fakturerar den omvärderade transaktionen skapar du följande värdetransaktioner:  

- Den vanliga fakturerade värdetransaktionen med transaktionstypen **Direkt kostnad**. Kostnadsbeloppet för den här transaktionen är den direkta kostnaden från källraden.  
- En värdetransaktion med transaktionstypen **Varians**. Den här transaktionen registrerar skillnaden mellan det fakturerade kostnaden och den omvärderade standardkostnaden.  
- En värdetransaktion med transaktionstypen **Omvärdering**. Den här transaktionen registrerar återföringen av omvärdering av den förväntade kostnaden.

### Exempel  

Följande exempel bygger på produktionen av kedjan i föregående exempel. I det här exemplet visas hur de tre typerna av transaktioner skapas, baserat på följande scenario:  

1.  Du bokför de inköpta länkarna som inlevererade med en styckkostnad på BVA 2,00.  
2.  Du bokför en omvärdering av länkarna med en ny styckkostnad på BVA 3,00 som uppdaterar standardkostnaden till BVA 3,00.  
3.  Du bokför det ursprungliga inköpet av kedjelänkarna som fakturerat, vilket skapar följande värdetransaktioner:  

    1.  En fakturerad värdetransaktion med transaktionstypen **Direkt kostnad**.  
    2.  En värdetransaktion med transaktionstypen **Omvärdering** för att registrera återföringen av omvärderingen av förväntade kostnader.  
    3.  En värdetransaktion med transaktionstypen Varians som registrerar skillnaden mellan den fakturerade kostnaden och den omvärderade standardkostnaden.  

I tabellen visas resultaten.  

|Steg|Bokföringsdatum|Transaktionstyp|Värderingsdatum|Kost.belopp (förväntat)|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Inköpskostnad|01-15-20|300.00|0,00|1|1|  
|2.|01-20-20|Omvärdering|01-20-20|150.00|0,00|1|2|  
|3.a.|01-15-20|Inköpskostnad|01-15-20|-300.00|0,00|1|3|  
|3.b.|01-15-20|Omvärdering|01-20-20|-150.00|0,00|1|4|  
|3.c.|01-15-20|Varians|01-15-20|0.00|450.00|1|5|  

## Fastställa huruvida omvärderingen påverkar en lagerminskning  

Använd datumet för bokföringen eller omvärderingen för att bestämma om en lagerminskning påverkas av en omvärdering eller inte.  

Följande tabell visar de villkor som används för en artikel som inte använder värderingsprincipen Genomsnitt.  

|Scenario|Löpnr|Tidsplan|Påverkat av omvärdering|  
|--------------|---------------|------------|-----------------------------|  
|A|Tidigare än omvärderingstransaktionsnummer|Tidigare än omvärderingbokföringsdatum|Nej|  
|B|Tidigare än omvärderingstransaktionsnr.|Lika med omvärderingbokföringsdatumet|Nej|  
|L|Tidigare än omvärderingstransaktionsnr.|Senare än omvärderingbokföringsdatum|Ja|  
|D|Senare än omvärderingstransaktionsnr.|Tidigare än omvärderingbokföringsdatum|Ja|  
|Ö|Senare än omvärderingstransaktionsnr.|Lika med omvärderingbokföringsdatumet|Ja|  
|K|Senare än omvärderingstransaktionsnr.|Senare än omvärderingbokföringsdatum|Ja|  

### Exempel  

Följande exempel, som visar omvärdering av en artikel som använder FIFO-värderingsprincipen: Exemplet baseras på följande scenario:  

1.  Den 01-01-20 bokför du ett inköp på 6 enheter.  
2.  Den 02-01-20 bokför du en försäljning på 1 enhet.  
3.  Den 03-01-20 bokför du en försäljning på 1 enhet.  
4.  Den 04-01-20 bokför du en försäljning på 1 enhet.  
5.  Den 03-01-20 beräknar du lagervärdet för artikeln och bokför en omvärdering av artikelns styckkostnad från BVA 10,00 till BVA 8,00.  
6.  Den 02-01-20 bokför du en försäljning på 1 enhet.  
7.  Den 03-01-20 bokför du en försäljning på 1 enhet.  
8.  Den 04-01-20 bokför du en försäljning på 1 enhet.  
9. Du kör batch-jobbet **Justera kost. – artikeltrans**.  

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
||04-01-20|Försäljning|04-01-20|-1|2.00|7|12|  

## PIA – omvärdering av lager  

Omvärdering av PIA-lager innebär att du omvärderar komponenter som är registrerade som PIA-lager.  

Det är viktigt att ha konventioner som styr när en artikel är PIA-lager från en finansiell synpunkt. I [!INCLUDE[prod_short](includes/prod_short.md)] finns följande regler:  

- En inhandlad komponent blir en del av råmateriallagret från tidpunkten när du bokför ett inköp som fakturerat.  
- En inköpt/detaljmonterad komponent ingår i PIA-lagret när du bokför dess förbrukning med en produktionsorder.  
- En inköpt/detaljmonterad komponent ingår i PIA-lagret tills du fakturerar en produktionsorder (tillverkad artikel).  

Sättet som värderingsdatumet för värdetransaktionen av förbrukning har angetts följer samma regler som för icke-PIA-lager. För mer information, gå till [Fastställa huruvida omvärderingen påverkar en lagerminskning](#determine-whether-revaluation-affects-an-inventory-decrease).  

Du kan omvärdera PIA-lagret på följande villkor:

- Omvärderingsdatumet infaller före bokföringsdatumen för motsvarande artikeltransaktioner av typen förbrukning.
- Du har inte fakturerat produktionsordern.  

> [!CAUTION]  
> Rapporten **Lagervärdering – PIA** visar värdet för bokförda produktionsordertransaktioner och kan vara lite förvirrande för PIA-artiklar som har omvärderats.  

## Omvärdera artiklar med värderingsprincipen Genomsnitt

Du kan endast omvärdera artiklar som använder värderingsprincipen Genomsnitt om **Beräkna per** är *Artikel*.

Du kan endast göra omvärdering i slutet av perioden som valdes i fältet **Period för genomsnittskostnad** på sidan **Lagerinställning**.

Omvärdering påverkar inte negativa transaktioner i den aktuella månaden, varför de helt tillämpade inkommande transaktionerna inte inkluderas.

### Exempel

Det här exemplet visar vad som händer när du beräknar lagervärdet på sidan **Omvärderingsjournaler för artikel**. På sidan **Lagerinställning** väljs **Artikel** i fältet **Genoms. kost.ber.typ** och **Månad** väljs i fältet **Period för genomsnittskostnad**.

Följande tabell visas de artikeltransaktioner för exempel genomsnittskostnadsartikeln, ITEM1.

|Bokföringsdatum|Artikeltransaktionstyp|Kvantitet|Kost.belopp (faktiskt)|Löpnr|
|----|----|----|----|----|
25-04-23|Inköp|5|5.00|1
26-04-23|Inköp|3|3.00|2
27-04-23|Försäljning|-5|-5,00|3
28-04-23|Försäljning|-1|-1,00|4
13-05-23|Inköp|2|20.00|5
17-06-23|Försäljning|-6|-22,00|6

I tabellen nedan visas resultatet av körningen av rapporten **beräkna lagervärde** med olika datum.

|Bokföringsdatum|Kvantitet|Kommentar|
|---|---|-------------|
30-04-23|2|Inkluderar endast den återstående kvantiteten från transaktion 2. Transaktion 1 tillämpas helt före bokföringsdatumet och transaktion 5 är efter bokföringsdatumet.
31-05-23|4|Inkluderar de återstående kvantiteterna från transaktioner 2 och 13.
30-06-23|0|Ingen resterande kvantitet vid bokföringsdatum.

Resultatet av följande transaktioner blir 0 oavsett bokföringsdatum.

|Bokföringsdatum|Artikeltransaktionstyp|Kvantitet|Kost.belopp (faktiskt)|Löpnr|
|----|----|----|----|----|
13-05-23|Inköp|5|5.00|1
26-04-23|Försäljning|-5|5.00|2

## Se även  

[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)   
[Designdetaljer: Lagervärdering](design-details-inventory-valuation.md)
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
