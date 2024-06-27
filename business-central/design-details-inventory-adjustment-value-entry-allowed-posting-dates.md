---
title: Felmeddelanden "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum"
description: Lös felet bakom meddelandet "bokföringsdatumet är inte inom det tillåtna intervallet av bokföringsdatum" när du kör batch-jobbet Justera kostn. – artikeltrans.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# Felmeddelande "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum..."

När du använder batch-jobbet **Justera kost. – artikeltrans.** kan du köra följande felmeddelande:

**Bokföringsdatumet är inte inom det tillåtna intervallet för bokföringsdatum**

Det här meddelandet anger att du inte får bokföra transaktioner för det datum du angav. Du kan komma runt det här problemet genom att ändra användarinställningarna.

## Ändra användarinställningar  

|Användar-ID  |Tillåt bokföring från  | Tillåt bokföring till  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

I det här fallet får du bokföra i datumintervallet från 11 september till 30 september. Du får dock inte bokföra justeringsvärdetransaktionen med bokföringsdatumet den 10 september.  

### Översikt över inställningar för bokföringsdatum

#### Lagerperioder

|Slutdatum  |Name  |Avslutat  |
|---------|---------|---------|
|2020-01-31     |2020 januari      |  Ja    |
|2020-02-28     |Februari 2020     |  Ja    |
|2020-03-31     |Mars 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |   Ja   |
|2020-08-31     |Augusti 2020     |   Ja   |
|2020-09-30     |September 2020.  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 202   |         |  

#### Redovisningsinställningar

|Fält|Värde|
|---------|---------|
|Tillåt bokföring fr.o.m.:  |  2020-09-10      |
|Tillåt bokföring t.o.m.:    |  2020-09-30      |
|Tidsregistrering:       |         |
|Lokalt adressformat:|   Postnr      |  

#### Användarinställningar

|Användar-ID  |Tillåt bokföring fr.o.m.  | Tillåt bokföring till  |
|---------|---------|--------|
|ANVÄNDARNAMN |  2020-09-10      |2020-09-30      |

Tilldela ett bredare datumintervall där du tillåter inlägg på sidan **lagerperiod** eller **redovisningskonfigurationen** för att undvika konflikten som orsakar felmeddelandet. Med det bredare intervallet kan du till exempel bokföra justeringsvärdetransaktionen med bokföringsdatumet den 10 september.
  
## Se även  

[Designdetaljer: Bokföringsdatumet för justeringsvärdetransaktionen](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
