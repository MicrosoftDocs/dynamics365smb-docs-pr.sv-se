---
title: Bokföringsdatum för värdetransaktioner
description: Lär dig hur batch-jobbet Justera Kostnad – Artikeltransaktioner används för att identifiera och tilldela ett bokföringsdatum till de värdetransaktioner som batchjobbet håller på att skapa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
---
# Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen

Den här artikeln ger vägledning för användare av lagerkostnadsfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)] och särskilt för hur batchjobbet **Justera kostn. – artikeltrans.** identifierar och tilldelar ett bokföringsdatum till de värdeposter som batchjobbet ska skapa.

## Hur bokföringsdatum tilldelas

Batchjobbet **Justera kost.-artikeltrans** tilldelar ett bokföringsdatum för den värdetransaktion den håller på att skapa genom följande steg:  

1. Bokföringsdatum för den transaktion som skapas är från början samma datum som för den transaktion den justerar.  

2. Bokföringsdatum verifieras mot lagerperioder och/eller redovisningsinställningar.  

3. Fördelningen av bokföringsdatum: Om det ursprungliga bokföringsdatumet inte ligger inom tillåtet intervall, tilldelar batchjobbet ett tillåtet bokföringsdatum från antingen Redovisningsinställningar eller Lagerperiod. Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att tilldelas justeringsvärdetransaktionen.  

Vi ska nu granska denna process i praktiken. Anta att vi har en försäljningspost för en artikeltransaktion. Artikeln skeppades iväg den 5 september 2020 och fakturerades dagen efter.  

#### Artikeltransaktion

|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  | Dokumentnummer |Lagerställekod  |Antal  |Kost.belopp (aktuellt)  |Fakturerat antal  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Försäljning       |102033     |  Blå       | -1    |    -11     |-1     |    0     |

Nedan visas de relaterade värdetransaktionerna:

- **Löpnr. 379** representerar den första värdetransaktionen (379) själva leveransen och bär samma bokföringsdatum som den överordnade artikeltransaktionen.  
- **Löpnr 381** motsvarar fakturan.  
- **Löpnr. 391** är en justering av värdetransaktionen för fakturering (Löpnr. 381 ovan).  

|Löpnr  |Artikelnr  |Bokföringsdatum  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Artikeltrans.löpnr  |Lagerställekod  |Antal i artikeltransaktioner  |Fakturerat antal  |Kost.belopp (aktuellt)  |Kost.belopp (förväntat)  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Försäljning     | Direkt kostnad   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nej   |0    |FÖRS          |
|381     |  A       |    2020-09-06     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nej  |0      |       FÖRS   |
|391     |  A       |    2020-09-10     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGJUST   |

Om du vill tilldela bokföringsdatumet för **Löpnr. 391** följande steg tillämpade:

1. **Justeringsvärdetransaktionen** som ska skapas (**Löpnr. 391**) tilldelas samma **Bokföringsdatum** som den transaktion den justerar.

2. Batchjobbet **Justera kost.-artikeltrans** avgör om justeringsvärdetransaktionens inledande bokföringsdatum ligger inom tillåtet spann för bokföringsdatum baserat på lagerperioder och/eller redovisningsinställningar.  

Vi ska nu granska ovannämnda försäljning genom att lägga till inställningen av tillåtna datumintervall för bokföring.  
  
#### Lagerperioder

|Slutdatum  |Name  |Avslutad  |
|---------|---------|---------|
|2020-01-31     |2020 januari      |  Ja    |
|2020-02-28     |Februari 2020     |  Ja    |
|2020-03-31     |Mars 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |  Ja    |
|2020-08-31     |Augusti 2020     |  Ja    |
|2020-09-30     |September 2020.  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 202   |         |

Första tillåtna bokföringsdatum är den första dagen i den första öppna perioden som är 1 september 2020.  

#### Redovisningsinställningar

|Fält|Värde  |
|---------|---------|
|Tillåt bokföring fr.o.m.:  |  2020-09-10      |
|Tillåt bokföring t.o.m.:    |  2020-09-30      |
|Tidsregistrering:       |         |
|Lokalt adressformat:|   Postnr      |  

Första tillåtna bokföringsdatum är det datum som anges i fältet **Tillåt bokföring från**: 10 september 2020. Om såväl lagerperioder som tillåtna bokföringsdatum i **Redovisningsinställningar** har angetts, kommer det senare av de två att bestämma det tillåtna datumspannet för bokföring.  

**Fördelning av ett tillåtet bokföringsdatum**  

Det ursprungliga tilldelade bokföringsdatumet var den 6 september, vilket visas i steg 1. I det andra steget identifierar emellertid batchjobbet Justera kostn. – Artikeltrans att det tidigast tillåtna bokföringsdatumet är den 10 september och tilldelar därmed den 10 september till justeringsvärdetransaktionen (**Löpnr. 391**).  


|Löpnr  |Artikelnr  |Bokföringsdatum  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Artikeltrans.löpnr  |Lagerställekod  |Antal i artikeltransaktioner  |Fakturerat antal  |Kost.belopp (aktuellt)  |Kost.belopp (förväntat)  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Försäljning     | Direkt kostnad   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nej   |0    |FÖRS          |
|381     |  A       |    2020-09-06     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nej  |0      |       FÖRS   |
|391     |  A       |    **2020-09-10**     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGJUST   |

## Vanliga problem med batch-jobbet Justera kost. – artikeltrans.

Supportteamet räknar regelbundet med jämna mellanrum så att de kan motivera sina egna artiklar om problemlösning.

### Felmeddelande "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum..."

Om det här felet uppstår måste du justera de datum som användaren får bokföra transaktioner med. Mer information finns i [felmeddelandet "bokföringsdatum är inte inom det tillåtna intervallet för bokföringsdatum"](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### Bokföringsdatum på justeringsvärdetransaktionen jämfört med bokföringsdatum för transaktionen som orsakar justeringen, till exempel omvärdering eller artikelomkostnad

För mer information, se [Bokförings datumet på justeringsvärde transaktionen jämfört med källtransaktionen](design-details-inventory-adjustment-value-entry-source-entry.md).

## Se även  

[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
