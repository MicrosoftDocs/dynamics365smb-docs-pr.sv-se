---
title: Bokförings datumet på justeringsvärde transaktionen jämfört med källtransaktionen
description: 'Läs mer om scenariot "bokföringsdatum på justeringsvärde transaktion jämfört med bokföringsdatum vid transaktion som orsakar justeringen, som omvärdering eller artikel omkostnad" när du kör batch-jobbet Justera kostn. – artikeltrans. identifierar.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a>Bokförings datumet på justeringsvärde transaktionen jämfört med källtransaktionen

I den här artikeln jämförs bokföringsdatum på posten för justeringsvärde med bokföringsdatumet på posten som orsakar att batchjobbet Justera kostn. – artikeltrans. körs, särskilt ett omvärderingsscenario och ett artikelavgiftsscenario.

Med batch-jobbet **Justera kost. – artikeltrans.** behandlas dina data beroende på ditt scenario och konfigurering av [!INCLUDE[prod_short](includes/prod_short.md)]. I det här avsnittet beskrivs två olika processer, och för var och en visar den typ av effekt som batch-jobbet Justera kost. – artikeltrans. innehåller på informationen.

## <a name="revaluation-scenario"></a>Omvärderingsscenario

### <a name="prerequisites"></a>Förutsättningar

Ange följande värden:

**Lagerinställningar**:  

- Automatisk kostnadsbokföring = Ja  

- Automatisk kostnadsjustering = Alltid  

- Genomsn. kost.ber.typ = artikel  

- Genomsn, kostnadsperiod = Dag  

**Redovisningsinställningar**:  

- Tillåt bokföring från = 1 januari 2021  

- Tillåt bokföring t.o.m. = tom  

**Användarinställningar**:  

- Tillåt bokföring från = 1 december 2020  

- Tillåt bokföring t.o.m. = tom  

### <a name="to-test-the-scenario"></a>För att testa scenariot

Testa det här scenariot genom att utföra följande steg.

1. Skapa ett **objekt** med namnet TEST med följande värden:  

     - Basenhet = ST  

     - Kostnad = Genomsnitt  

     - Markera valfria bokföringsmallar.  

2. Öppna **artikeljournalen**, skapa en ny post och bokför en rad så här:  

     - Bokföringsdatum = 15 december 2020  

     - Artikel = TEST  

     - Trans.typ = Köp  

     - Antal = 100  

     - A-pris = 10  

3. Öppna **artikeljournalen**, skapa en ny post och bokför en rad så här:  

     - Datum = 20 december 2020  

     - Artikel = TEST  

     - Trans.typ = Negativ justering  

     - Antal = 2  

4. Öppna **artikeljournalen**, skapa en ny post och bokför en rad så här:  

     - Datum = 15 januari, 2021  

     - Artikel = TEST  

     - Trans.typ = Negativ justering  

     - Antal = 3  

5. Öppna **Omvärderingsjournaler för artikel**, skapa en ny post och bokför en rad så här:  

     - Artikel = TEST  

     - Kopplas till löpnr = välj den inköpstransaktion som bokförts i steg 2. Bokföringsdatum för omvärderingen ska vara detsamma som den transaktionen som den justerar.  

     - Styckkostnad (omvärderad) = 40  

Följande **artikeltransaktioner** och **värdetransaktioner** har bokförts:  

**Artikeltransaktion – inköp**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Inköp         |T00001         |100         |4000         |95        |

**Värdetransaktioner**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Löpnummerantal för artikelnummer  |Kost.belopp (aktuellt)  |Kostnad bokförd i redov.  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Inköp         |Direkt kostnad         |T00001         |100         |1 000,00          |1 000,00    |Nej         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Inköp         |Omvärdering         |T04002         |0         |3 000         |3 000         |Nej         |0         |REVALINL         |

**Artikeltransaktion – negativ justering, steg 3**  

|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Negativ justering  |T00002         |-2         |-80         | 0        |

**Värdetransaktioner**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Löpnummerantal för artikelnummer  |Kost.belopp (aktuellt)  |Kostnad bokförd i redov.  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Negativ justering         |Direkt kostnad         |T00002         |-2         |-20          |-20    |Nej         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Negativ justering         |Direkt kostnad         |T04002         |0         |-60         |-60         |Ja         |377         |INVTADAMT         |

**Artikeltransaktion – negativ justering, steg 4**  

|Löpnr  |Artikelnr  |Bokföringsdatum  |Transaktionstyp  |Dokumentnummer  |Antal  |Kost.belopp (aktuellt)  |Återstående antal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Negativ justering  |T00003         |-3         |-120         | 0        |

**Värdetransaktioner**  

|Löpnummer  |Artikelnr  |Bokföringsdatum  |Artikeltrans.löpnr  |Artikeltransaktionstyp  |Transaktionstyp  |Dokumentnummer  |Löpnummerantal för artikelnummer  |Kost.belopp (aktuellt)  |Kostnad bokförd i redov.  |Justering  |Kopplas till löpnr  |Ursprungskod  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Negativ justering         |Direkt kostnad         |T00003         |-3         |-30          |-30    |Nej         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Negativ justering         |Direkt kostnad         |T04003         |0         |-90         |-90         |Ja         |378         |INVTADAMT         |

Batchjobbet **Justera kost. – artikeltrans** har identifierat en ändring i kostnad och justerat de negativa justeringarna.  

**Granskning av bokföringsdatum på skapade justeringsvärdetransaktioner:** Tidigast tillåtna bokföringsdatum som batchjobbet Justera kost. – artikeltrans. måste beakta är den 1 januari 2021, vilket anges i redovisningsinställningarna.  

**Negativ justering i steg 3:** tilldelat bokföringsdatum är den 1 januari 1, vilket anges i redovisningsinställningarna. Bokföringsdatum för den värdetransaktion som ska omfattas av justering är den 20 december 2020. Enligt redovisningsinställningarna ligger datumet inte inom tillåtet datumintervall för bokföring. Därför tilldelas det bokföringsdatum som anges i fältet Tillåt bokföring fr.o.m i Redovisningsinställningar till justeringsvärdetransaktionen.  

**Negativ justering i steg 4:** tilldelat bokföringsdatum är den 15 januari. Värdetransaktionen som omfattas av justering har bokföringsdatum 15 januari, vilket ligger inom intervallet för tillåten bokföring enligt redovisningsinställningarna.  

Justeringen för den negativa justeringen i steg 3 förorsakar diskussion. Ett bättre bokföringsdatum för justeringsvärdetransaktionen hade varit den 20 december eller åtminstone i december, detta eftersom den omvärderingen som förorsakar ändringen i KSV bokfördes i december.  

För att uppnå en decemberjustering av den negativa justeringen i steg 3 måste Redovisningsinställningar, fältet Tillåt bokföring fr.o.m, ange ett datum i december.  

### <a name="conclusion"></a>Slutsats

Med den erfarenhet som vunnits i det här scenariot kanske du vill tänka på följande när du bedömer de lämpligaste inställningarna för ett tillåtet bokföringsdatumintervall för ett företag. Så länge du tillåter att lagervärdet bokförs under en period, till exempel december i det här fallet, bör inställningarna som företaget använder för tillåtna bokföringsdatumintervall justeras enligt det här beslutet. Fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna, som anger att den 1 december skulle låta omvärderingen utförd i december vidarebefordras till att påverka utgående transaktioner under samma period.  

Användargrupper är inte behöriga att bokföra i december utan i januari, vilket troligen var avsett att begränsas av Redovisningsinställningarna i detta scenario, bör i stället tas upp via användarinställningarna.  

## <a name="item-charge-scenario"></a>Artikelomkostnadsscenario

### <a name="prerequisites-1"></a>Förutsättningar

Ange följande värden:

**Lagerinställningar**:  

- Automatisk kostnadsbokföring = Ja  

- Automatisk kostnadsjustering = Alltid  

- Genomsn. kost.ber.typ = artikel  

- Genomsn, kostnadsperiod = Dag  

**Redovisningsinställningar**:  

- Tillåt bokföring från = 1 december 2020.  

- Tillåt bokföring t.o.m. = tom  

**Användarinställningar**:  

- Tillåt bokföring från = 1 december 2020.  

- Tillåt bokföring t.o.m. = tom  

### <a name="to-test-the-scenario-1"></a>För att testa scenariot

Testa det här scenariot genom att utföra följande steg:

1.  Skapa ett **objekt** Ladda med följande värden:  

     - Basenhet = ST  

     - Kostnad = Genomsnitt  

     - Markera valfria bokföringsmallar.  

2.  Skapa en ny **inköpsorder** med följande värden:  

     - Inköpsleverantörsnr: 10000  

     - Bokföringsdatum = 15 december 2020

     - Leverantörens fakturanr: 1234  

     Välj följande värden på inköpsorderraden:  

     - Artikel = DEBITERING  

     - Antal = 1  

     - Inköpspris (BVA) = 100  

     Slutför steget genom att bokföra dokumentet som Inlevererat och fakturerat.  

3.  Skapa en ny **försäljningsorder** med följande värden:  

     - Förs.kundnr: 10000  

     - Bokföringsdatum = 16 december 2020  

     På försäljningsorderraden:  

     - Artikel = DEBITERING  

     - Antal = 1  

     - A-pris = 135  

     Slutför steget genom att bokföra dokumentet som Inlevererat och fakturerat.  

4.  Ange värden för sidan **redovisningsinställningar**:  

     - Tillåt bokföring från = 1 januari 2021  

    -  Tillåt bokföring t.o.m. = tom  

5.  Skapa en ny **inköpsorder** med följande värden:  

     - Inköpsleverantörsnr: 10000  

     - Bokföringsdatum = 2 januari 2021  

     - Leverantörens fakturanr: 2345  

     På inköpsorderraden:  

     - Artikelomkostnad = JB-FRAKT  

     - Antal = 1  

     - Inköpspris (BVA) = 3  

     - Tilldela artikelomkostnader till inleverans från steg 2.  

     Slutför steget genom att bokföra dokumentet som Inlevererat och fakturerat.  


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

     Skapa en ny **inköpsorder** med följande värden:  

     - Inköpsleverantörsnr: 10000  

     - Bokföringsdatum = 30 december 2020  

     - Leverantörens fakturanr: 3456  

     Välj följande värden på inköpsorderraden:  

     - Artikelomkostnad = JB-FRAKT  

     - Antal = 1  

     - Inköpspris (BVA) = 2  

     Tilldela artikelomkostnader till inleverans från steg 2  

     Slutför steget genom att bokföra dokumentet som Inlevererat och fakturerat.  


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

Beskrivet scenario erhåller i slutändan en lagervärderingsrapport som visar antalet = 0 när värdet = 2. Artikelomkostnaden som bokfördes i steg 6 är en del av värdet Lagerökning för december, medan lagerminskningen för samma period inte påverkas.  

Att låta redovisningsinställningarna ange Tillåt bokföring fr.o.m den 1 januari var användbart för den första artikelomkostnaden. Kostnaderna för ökat och minskat lager registrerades under samma period. För den andra artikelomkostnaden gör emellertid redovisningsinställningarna att ändringen i KSV bokförs under nästkommande period.  

**Sammanfattning:**  

Det är svårt att låta rapporten Lagerutvärdering visa kvantiteten = 0 när värdet är <> 0. I detta fall är det också svårare att uttrycka de optimala inställningarna då inköpsfakturorna anländer samma dag men adresserar olika perioder eller till och med räkenskapsår. Att flytta fram till ett nytt räkenskapsår kräver vanligtvis lite planering, och som ett led i insikten för transaktionsprocessen Justera kost. – artikeltrans måste KSV-detektering beaktas.  

I detta scenario kunde ett alternativ vara att låta Redovisningsinställningarna, fältet Tillåt bokföring fr.o.m att ange ett datum i december några dagar längre fram, samt att flytta fram bokföringen av den första artikelomkostnaden, detta i syfte att låta alla kostnader för föregående period/räkenskapsår först registreras för den period som de tillhör, köra batch-jobbet Justera kostn. – artikeltrans. och därefter flytta tillåtet bokföringsdatum till den nya perioden\/det nya räkenskapsåret. Därefter kan den artikelomkostnaden med bokföringsdatum 2 januari bokföras.  

## <a name="see-also"></a>Se även

[Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
