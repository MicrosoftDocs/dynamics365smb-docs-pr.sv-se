---
title: Bokföringsdatum för värdetransaktioner
description: Lär dig hur batch-jobbet Justera Kostnad – Artikeltransaktioner används för att identifiera och tilldela ett bokföringsdatum till de värdetransaktioner som batchjobbet håller på att skapa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/27/2021
ms.author: edupont
ms.openlocfilehash: 2a3d35672905094e714f85ac4758cbf39ec88cb6
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688320"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen  

Den här artikeln innehåller riktlinjer för kostnadsberäkningsfunktioner för lager [!INCLUDE[prod_short](includes/prod_short.md)]. Den specifika artikeln vägleder dig i hur batchjobbet **Justera kostnad – Artikeltransaktioner** identifierar och tilldelar ett bokföringsdatum till de värdeposter som batchjobbet håller på att skapa.  

Först granskas processens koncept, hur batch-jobbet identifierar och tilldelar bokföringsdatum till värdetransaktionen som ska skapas. Därefter delas vissa situationer som vi i supportteamet stöter på då, och slutligen kommer en sammanfattning av de begrepp som används.  

## <a name="the-concept"></a>Konceptet  

Batchjobbet **Justera kost.-artikeltrans** tilldelar ett bokföringsdatum för den värdetransaktion den håller på att skapa genom följande steg:  

1.  Bokföringsdatum för den transaktion som skapas är från början samma datum som för den transaktion den justerar.  

2.  Bokföringsdatum verifieras mot lagerperioder och/eller redovisningsinställningar.  

3.  Fördelningen av bokföringsdatum: Om det ursprungliga bokföringsdatumet inte ligger inom tillåtet intervall, tilldelar batchjobbet ett tillåtet bokföringsdatum från antingen Redovisningsinställningar eller Lagerperiod. Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att tilldelas justeringsvärdetransaktionen.  

 Vi ska nu granska denna process i praktiken. Anta att vi har en försäljningspost för en artikeltransaktion. Artikeln skeppades iväg den 5 september 2020 och fakturerades dagen efter.  


**Artikeltransaktion**  
Datumformat: ÅÅÅÅ-MM-DD

|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  | Dokumentnummer |Lagerställekod  |Antal  |Kost.belopp (aktuellt)  |Fakturerat antal  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Försäljning       |102033     |  Blå       | -1    |    -11     |-1     |    0     |

Nedan representerar den första värdetransaktionen (379) själva leveransen och bär samma bokföringsdatum som den överordnade artikeltransaktionen.  
  
Den andra värdetransaktionen (381) motsvarar fakturan.  

Den tredje värdetransaktionen (391) är en justering av värdetransaktionen för fakturering (381).  
  

|Löpnr  |Artikelnr  |Bokföringsdatum  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Artikeltrans.löpnr  |Lagerställekod  |Antal i artikeltransaktioner  |Fakturerat antal  |Kost.belopp (aktuellt)  |Kost.belopp (förväntat)  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Försäljning     | Direkt kostnad   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nej   |0    |FÖRS          |
|381     |  A       |    2020-09-06     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nej  |0      |       FÖRS   |
|391     |  A       |    2020-09-10     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGJUST   |

Bokföringsdatum för justeringstransaktion anges från början till samma bokföringsdatum som för den transaktion den justerar.

 Steg 1: Justeringsvärdetransaktionen som ska skapas tilldelas samma bokföringsdatum som den transaktion den justerar, vilket illustreras ovan genom värdetransaktion 391.  
  
 Steg 2: Validering av ursprungligen tilldelat bokföringsdatum.  

Batchjobbet **Justera kost.-artikeltrans** avgör om justeringsvärdetransaktionens inledande bokföringsdatum ligger inom tillåtet spann för bokföringsdatum baserat på lagerperioder och/eller redovisningsinställningar.  

Vi ska nu granska ovannämnda försäljning genom att lägga till inställningen av tillåtna datumintervall för bokföring.  
  
**Lagerperioder**

|Slutdatum  |Name  |Avslutad  |
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

Första tillåtna bokföringsdatum är den första dagen i den första öppna perioden. 1 september 2020.  

**Redovisningsinställningar**

|Fält|Värde  |
|---------|---------|
|Tillåt bokföring fr.o.m.:  |  2020-09-10      |
|Tillåt bokföring t.o.m.:    |  2020-09-30      |
|Tidsregistrering:       |         |
|Lokalt adressformat:|   Postnr      |  

 Första tillåtna bokföringsdatum är det datum som anges i fältet Tillåt bokföring från: 1 september 2020.  
 Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att bestämma det tillåtna datumspannet för bokföring.  

 Steg 3: Fördelning av ett tillåtet bokföringsdatum.  

 Det ursprungliga tilldelade bokföringsdatumet var den 6 september, vilket visas i steg 1. I det andra steget identifierar emellertid batchjobbet Justera kostn. – Artikeltrans att det tidigast tillåtna bokföringsdatumet är den 10 september och tilldelar därmed den 10 september till justeringsvärdetransaktionen nedan.  

   
|Löpnr  |Artikelnr  |Bokföringsdatum  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Artikeltrans.löpnr  |Lagerställekod  |Antal i artikeltransaktioner  |Fakturerat antal  |Kost.belopp (aktuellt)  |Kost.belopp (förväntat)  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Försäljning     | Direkt kostnad   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nej   |0    |FÖRS          |
|381     |  A       |    2020-09-06     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nej  |0      |       FÖRS   |
|391     |  A       |    **2020-09-10**     |    Försäljning     | Direkt kostnad   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGJUST   |

 Vi har nu gått igenom hur man tilldelar bokföringsdatum för värdetransaktioner som skapats genom batchjobbet Justera kost. – artikeltrans.  

 Vi fortsätter nu med att granska några scenarier som vi i supportteamet då och då stöter på i samband med tilldelade boföringsdatum i batchjobbet Justera kost. – artikeltrans och relaterade inställningar.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenario I: "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum..."  

 Dett är ett scenario där en användare får nämnda felmeddelande när batch-jobbet Justera kost. – artikeltrans körs.  

 I föregående avsnitt, som beskrev begreppet att tilldela bokföringsdatum, var syftet med batch-jobbet Justera kost. – artikeltrans att skapa en Värdetransaktion med bokföringsdatum 10 september.  

![Felmeddelande om bokföringsdatum.](media/helene/TechArticleAdjustcost6.png "Felmeddelande om bokföringsdatum")

 Vi följer upp användarinställningarna:  

**Användarinställningar**  

Sortering: användar-ID  

|Användar-ID  |Tillåt bokföring fr.o.m.  | Tillåt bokföring t.o.m.  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

 Användaren i detta exempel har ett tillåtet datumintervall för bokföring från den 11 september till den 30 september, och får därmed inte bokföra justeringsvärdetransaktionen med bokföringsdatum 10 september.  

### <a name="overview-of-involved-posting-date-setup"></a>Översikt över berörda inställningar för bokföringsdatum:

**Lagerperioder**  

|Slutdatum  |Name  |Avslutad  |
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

**Redovisningsinställningar**  

|Fält|Värde|
|---------|---------|
|Tillåt bokföring fr.o.m.:  |  2020-09-10      |
|Tillåt bokföring t.o.m.:    |  2020-09-30      |
|Tidsregistrering:       |         |
|Lokalt adressformat:|   Postnr      |  

**Användarinställningar**    

|Användar-ID  |Tillåt bokföring fr.o.m.  | Tillåt bokföring t.o.m.  |
|---------|---------|--------|
|<name> |  2020-09-11      |2020-09-30      |

 Tilldela användaren ett bredare (eller samma) tillåtna intervall för bokföringsdatum som i lagerperioden eller redovisningskonfigurationen (omnämnd konflikt kommer att undvikas). Justeringsvärdestransaktionen med bokföringsdatum 10 september kommer att bokföras med denna inställning.

En äldre kunskapsbasartikel [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) beskriver ytterligare scenarier relaterade till omnämnda felmeddelande.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenario II: Bokföringsdatum på justeringsvärdetransaktionen jämfört med bokföringsdatum för transaktionen som orsakar justeringen, till exempel omvärdering eller artikelomkostnad.  

### <a name="revaluation-scenario"></a>Omvärderingsscenario:  

 Förutsättningar:  

 Lagerinställningar:  
me
-   Automatisk kostnadsbokföring = Ja  

-   Automatisk kostnadsjustering = Alltid  

-   Genomsn. kost.ber.typ = artikel  

-   Genomsn, kostnadsperiod = Dag  

 Redovisningsinställningar:  

-   Tillåt bokföring från = 1 januari 2021  

-   Tillåt bokföring t.o.m. = tom  

 Användarinställningar:  

-   Tillåt bokföring från = 1 december 2020  

-   Tillåt bokföring t.o.m. = tom  

### <a name="to-test-the-scenario"></a>För att testa scenariot  

1.  Skapa artikel TEST:  

     Basenhet = ST  

     Kostnad = Genomsnitt  

     Markera valfria bokföringsmallar.  

2.  Öppna artikeljournalen, skapa och bokför en rad så här:  

     Bokföringsdatum = 15 december 2020  

     Artikel = TEST  

     Trans.typ = Köp  

     Antal = 100  

     A-pris = 10  

3.  Öppna artikeljournalen, skapa och bokför en rad så här:  

     Datum = 20 december 2020  

     Artikel = TEST  

     Trans.typ = Negativ justering  

     Antal = 2  

4.  Öppna artikeljournalen, skapa och bokför en rad så här:  

     Datum = 15 januari, 2021  

     Artikel = TEST  

     Trans.typ = Negativ justering  

     Antal = 3  

5.  Öppna omvärderingsjournalen, skapa och bokför en rad så här:  

     Artikel = TEST  

     Kopplas till löpnr = välj den inköpstransaktion som bokförts i steg 2. Bokföringsdatum för omvärderingen ska vara detsamma som den transaktionen som den justerar.  

     Styckkostnad (omvärderad) = 40  

Följande **artikeltransaktioner** och **värdetransaktioner** har bokförts:  

**Artikeltransaktion - inköp**  
Datumformat: ÅÅÅÅ-MM-DD  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Inköp         |T00001         |100         |4000         |95        |

**Värdetransaktioner**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Löpnummerantal för artikelnummer  |Kost.belopp (aktuellt)  |Kostnad bokförd i redov.  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Inköp         |Direkt kostnad         |T00001         |100         |1 000,00          |1 000,00    |Nej         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Inköp         |Omvärdering         |T04002         |0         |3 000         |3 000         |Nej         |0         |REVALINL         |

**Artikeltransaktion - negativ justering, steg 3**  

|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Negativ justering  |T00002         |-2         |-80         | 0        |

**Värdetransaktioner**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Löpnummerantal för artikelnummer  |Kost.belopp (aktuellt)  |Kostnad bokförd i redov.  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Negativ justering         |Direkt kostnad         |T00002         |-2         |-20          |-20    |Nej         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Negativ justering         |Direkt kostnad         |T04002         |0         |-60         |-60         |Ja         |377         |INVTADAMT         |

**Artikeltransaktion - negativ justering, steg 4**  

|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Negativ justering  |T00003         |-3         |-120         | 0        |

**Värdetransaktioner**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Löpnummerantal för artikelnummer  |Kost.belopp (aktuellt)  |Kostnad bokförd i redov.  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Negativ justering         |Direkt kostnad         |T00003         |-3         |-30          |-30    |Nej         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Negativ justering         |Direkt kostnad         |T04003         |0         |-90         |-90         |Ja         |378         |INVTADAMT         |

Batchjobbet Justera kost. – artikeltrans har identifierat en ändring i kostnad och justerat de negativa justeringarna.  

**Granskning av bokföringsdatum på skapade justeringsvärdetransaktioner:** Tidigast tillåtna bokföringsdatum som batchjobbet Justera kost. – artikeltrans. måste beakta är den 1 januari 2021, vilket anges i redovisningsinställningarna.  

**Negativ justering i steg 3:** tilldelat bokföringsdatum är den 1 januari 1, vilket anges i redovisningsinställningarna. Bokföringsdatum för den värdetransaktion som ska omfattas av justering är den 20 december 2020. Enligt redovisningsinställningarna ligger datumet inte inom tillåtet datumintervall för bokföring. Därför tilldelas det bokföringsdatum som anges i fältet Tillåt bokföring fr.o.m i Redovisningsinställningar till justeringsvärdetransaktionen.  

**Negativ justering i steg 4:** tilldelat bokföringsdatum är den 15 januari. Värdetransaktionen som omfattas av justering har bokföringsdatum 15 januari, vilket ligger inom intervallet för tillåten bokföring enligt redovisningsinställningarna.  

Justeringen för den negativa justeringen i steg 3 förorsakar diskussion. Ett bättre bokföringsdatum för justeringsvärdetransaktionen hade varit den 20 december eller åtminstone i december, detta eftersom den omvärderingen som förorsakar ändringen i KSV bokfördes i december.  

För att uppnå en decemberjustering av den negativa justeringen i steg 3 måste Redovisningsinställningar, fältet Tillåt bokföring fr.o.m, ange ett datum i december.  

**Sammanfattning:**  

Med erfarenheterna från detta scenario i ryggen och i beaktande av de lämpligaste inställningarna för tillåtet datumintervall för bokföring för ett företag, kanske du bör överväga följande information: Så länge du låter ändringar i lagervärde bokföras inom en period (i detta fall december) bör de inställningar som företaget använder för tillåtna bokföringsintervall justeras i enlighet med detta beslut. Fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna, som anger att den 1 december skulle låta omvärderingen utförd i december vidarebefordras till att påverka utgående transaktioner under samma period.  

Användargrupper är inte behöriga att bokföra i december utan i januari, vilket troligen var avsett att begränsas av Redovisningsinställningarna i detta scenario, bör i stället tas upp via användarinställningarna.  

### <a name="item-charge-scenario"></a>Artikelomkostnadsscenario:  

 Förutsättningar:  

 Lagerinställningar:  

-   Automatisk kostnadsbokföring = Ja  

-   Automatisk kostnadsjustering = Alltid  

-   Genomsn. kost.ber.typ = artikel  

-   Genomsn, kostnadsperiod = Dag  

 Redovisningsinställningar:  

-   Tillåt bokföring från = 1 december 2020.  

-   Tillåt bokföring t.o.m. = tom  

 Användarinställningar:  

-   Tillåt bokföring från = 1 december 2020.  

-   Tillåt bokföring t.o.m. = tom  


### <a name="to-test-the-scenario"></a>För att testa scenariot  

1.  Skapa artikelomkostnad:  

     Basenhet = ST  

     Kostnad = Genomsnitt  

     Markera valfria bokföringsmallar.  

2.  Skapa en ny inköpsorder  

     Inköpsleverantörsnr: 10000  

     Bokföringsdatum = 15 december 2020

     Leverantörens fakturanr: 1234  

     På inköpsorderraden:  

     Artikel = DEBITERING  

     Antal = 1  

     Inköpspris (BVA) = 100  

     Bokför Inleverera och Fakturera.  

3.  Skapa en ny försäljningsorder:  

     Förs.kundnr: 10000  

     Bokföringsdatum = 16 december 2020  

     På försäljningsorderraden:  

     Artikel = DEBITERING  

     Antal = 1  

     A-pris = 135  

     Bokför leverans och faktura.  

4.  Redovisningsinställningar:  

     Tillåt bokföring från = 1 januari 2021  

     Tillåt bokföring t.o.m. = tom  

5.  Skapa en ny inköpsorder:  

     Inköpsleverantörsnr: 10000  

     Bokföringsdatum = 2 januari 2021  

     Leverantörens fakturanr: 2345  

     På inköpsorderraden:  

     Artikelomkostnad = JB-FRAKT  

     Antal = 1  

     Inköpspris (BVA) = 3  

     Tilldela artikelomkostnader till inleverans från steg 2.  

     Bokför inleverans och faktura.  


**Status för artikeltransaktion för inköp steg 2**:  
  
|Löpnummer  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |TILLÄGG         |2020-12-15         |Inköp         |107030         |1         |105         |0        |

**Värdetransaktioner**  

|Löpnummer |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  | Art.omkostn.nr    |  Antal i artikeltransaktioner   |Kost.belopp (aktuellt)     |Kostnad bokförd i redov. |Justering |Kopplas till löpnr |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |TILLÄGG|   2020-12-15    |324         |Inköp         |Direkt kostnad         |108029         |         |1          |100    |100         |NR         |0         |
|399      |TILLÄGG   |2021-01-02    |324         |Inköp         |Direkt kostnad         |108009         |JBFRAKT         |0         |3         |3         |NR         |0         |


**Status för artikeltransaktion för försäljning**:  
  
|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |TILLÄGG         |2020-12-16         |Försäljning         |102035         |-1         |-105         |0        |

**Värdetransaktioner**  

|Löpnummer |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  | Art.omkostn.nr    |  Antal i artikeltransaktioner   |Kost.belopp (aktuellt)     |Kostnad bokförd i redov. |Justering |Kopplas till löpnr |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |TILLÄGG|   2020-12-16    |325         |Försäljning         |Direkt kostnad         |109024         |         |-1          |-100    |-100         |NR         |0         |
|400      |TILLÄGG   |2021-01-01    |325         |Försäljning         |Direkt kostnad         |109024         |         |0         |-3         |-3         |Ja         |398         |


6.  Arbetsdagen 3 januari anländer en inköpsfaktura med ytterligare artikelomkostnader till inköpet i steg 2. Fakturan har den dokumentdatumet den 30 december och bokförs därför med bokföringsdatum 30 december 2020.  

     Skapa en ny inköpsorder:  

     Inköpsleverantörsnr: 10000  

     Bokföringsdatum = 30 december 2020  

     Leverantörens fakturanr: 3456  

     På inköpsorderraden:  

     Artikelomkostnad = JB-FRAKT  

     Antal = 1  

     Inköpspris (BVA) = 2  

     Tilldela artikelomkostnader till inleverans från steg 2.  

     Bokför inleverans och faktura.  


**Status för artikeltransaktion för inköp**:  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |TILLÄGG         |2020-12-15         |Inköp         |107030         |1         |105         |0        |

**Värdetransaktioner**  

|Löpnr |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  | Art.omkostn.nr    |  Antal i artikeltransaktioner   |Kost.belopp (aktuellt)     |Kostnad bokförd i redov. |Justering |Kopplas till löpnr |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |TILLÄGG   |2020-12-15    |324         |Inköp         |Direkt kostnad         |108029         |            |1         |100    |100         |Nej         |0         |
|399      |TILLÄGG   |2021-01-02    |324         |Inköp         |Direkt kostnad         |108030         |JBFRAKT   |0         |3         |3         |Nej         |0         |
|401      |TILLÄGG   |**2020-12-30**    |324         |Inköp         |Direkt kostnad         |108031         |JBFRAKT   |0         |2         |2         |Nej         |0         |

**Status för artikeltransaktion för försäljning**:  
  
|Löpnummer  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |TILLÄGG         |2020-12-16         |Försäljning         |102035         |-1         |-105         |0        |

**Värdetransaktioner**  

|Löpnr |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  | Art.omkostn.nr    |  Antal i artikeltransaktioner   |Kost.belopp (aktuellt)     |Kostnad bokförd i redov. |Justering |Kopplas till löpnr |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |TILLÄGG   |2020-12-16        |325         |Försäljning         |Direkt kostnad         |103024         |            |-1         |-100       |-100         |Nej         |0         |
|400      |TILLÄGG   |2021-01-01        |325         |Försäljning         |Direkt kostnad         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |TILLÄGG   |**2021-01-01**    |325         |Försäljning         |Direkt kostnad         |103024         |            |0          |-2         |-2         |Ja         |398         |

Rapporten Lagervärdering skrivs ut per den 31 december 2020

![Innehåll i rapporten Lagervärdering.](media/helene/TechArticleAdjustcost13.png "Innehåll i rapporten Lagervärdering")

 **Summering av scenario:**  

 Beskrivet scenario erhåller i slutändan en lagervärderingsrapport som visar antalet = 0 när värdet = 2. Artikelomkostnaden som bokfördes i steg 11 är en del av värdet Lagerökning för december, medan lagerminskningen för samma period inte påverkas.  

 Att låta redovisningsinställningarna ange Tillåt bokföring fr.o.m den 1 januari var användbart för den första artikelomkostnaden. Kostnaderna för ökat och minskat lager registrerades under samma period. För den andra artikelomkostnaden gör emellertid redovisningsinställningarna att ändringen i KSV bokförs under nästkommande period.  

 **Sammanfattning:**  

 Det är svårt att låta rapporten Lagerutvärdering visa kvantiteten = 0 när värdet är <> 0. I detta fall är det också svårare att uttrycka de optimala inställningarna då inköpsfakturorna anländer samma dag men adresserar olika perioder eller till och med räkenskapsår. Att flytta fram till ett nytt räkenskapsår kräver vanligtvis lite planering, och som ett led i insikten för transaktionsprocessen Justera kost. – artikeltrans måste KSV-detektering beaktas.  

 I detta scenario kunde ett alternativ vara att låta Redovisningsinställningarna, fältet Tillåt bokföring fr.o.m att ange ett datum i december några dagar längre fram, samt att flytta fram bokföringen av den första artikelomkostnaden, detta i syfte att låta alla kostnader för föregående period/räkenskapsår först registreras för den period som de tillhör, köra batch-jobbet Justera kostn. – artikeltrans. och därefter flytta tillåtet bokföringsdatum till den nya perioden\/det nya räkenskapsåret. Därefter kan den artikelomkostnaden med bokföringsdatum 2 januari bokföras.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historik för batch-jobbet Justera kost. – artikeltrans  

 Nedan visas en sammanfattning av begreppet Bokföra datum för justeringsvärdetransaktioner utförda av batch-jobbet Justera kost. – artikeltrans.  

### <a name="about-the-request-form-posting-date"></a>Om bokföringsdatum för formulär för begäran:  

 I batch-jobbet Justera kost. – artikeltrans finns inte längre något bokföringsdatum som måste anges av användaren. Batch-jobbet körs igenom alla nödvändiga förändringar och skapar värdetransaktioner med samma bokföringsdatum som den värdetransaktion jobbet korrigerar. Om bokföringsdatumet inte ligger inom tillåtet intervall används bokföringsdatumet i fältet Tillåt bokföring fr.o.m. i Redovisningsinställningarna ELLER, om lagerperioder används, så används det senare datumet av de båda. Se begreppsbeskrivningen ovan.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historik för Bokför lagerkostnad i redov.  

 Batch-jobbet Bokför lagerkostnad i redovisning är nära knutet till batch-jobbet Justera kost.-artikeltrans, varför historiken för batch-jobbet även summeras och delas här.  
 
![Faktisk kostnad jämfört med förväntad kostnad.](media/helene/TechArticleAdjustcost14.png "Faktisk kostnad jämfört med förväntad kostnad")

### <a name="about-the-posting-date"></a>Om bokföringsdatum  

 I batch-jobbet Bokför lagerkostnad i redov. finns inte längre något bokföringsdatum som måste anges i begäranformuläret. Bokföringstransaktionen skapas med samma bokföringsdatum som den relaterade värdetransaktionen. Datumintervall för tillåten bokföring måste tillåta bokföringsdatumet för redovisningstransaktionen som skapats för att avsluta batch-jobbet. I annat fall måste datumintervallet för tillåten bokföring tillfälligt öppnas igen genom att ändra eller ta bort datumen i fältet Tillåt bokföring fr.o.m och Till i Redovisningsinställningarna. För att undvika avstämningsproblem krävs att okföringsdatum för redovisningstransaktionen motsvarar bokföringsdatumet för värdetransaktionen.  

 Batch-jobbet söker igenom tabellen 5811 – Bokför värdetransaktion i redovisning i syfte att identifiera värdetransaktionerna i omfånget för bokföring i redovisningen. Tabellen töms efter slutförd körning.

## <a name="see-also"></a>Se även  

[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
