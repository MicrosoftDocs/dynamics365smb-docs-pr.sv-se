---
title: "Bokföringsdatum för värdetransaktioner"
description: "Lär dig hur batch-jobbet Justera Kostnad - Artikeltransaktioner används för att identifiera och tilldela ett bokföringsdatum till de värdetransaktioner som batchjobbet håller på att skapa."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c95432ec1cf24aaaedf0fad5a2746ace9705e2e3
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen
Den här artikeln innehåller riktlinjer för kostnadsberäkningsfunktioner för lager [!INCLUDE[d365fin](includes/d365fin_md.md)]. Den specifika artikeln vägleder dig i hur batchjobbet **Justera kostnad - Artikeltransaktioner** identifierar och tilldelar ett bokföringsdatum till de värdeposter som batchjobbet håller på att skapa.  

Först granskas processens koncept, hur batch-jobbet identifierar och tilldelar bokföringsdatum till värdetransaktionen som ska skapas. Därefter delas vissa situationer som vi i supportteamet stöter på då, och slutligen kommer en sammanfattning av de begrepp som använd
s i version 3.0.  

## <a name="the-concept"></a>Konceptet  
Från och med version 5.0 tilldelar batchjobbet **Justera kost.-artikeltrans** ett bokföringsdatum för den värdetransaktion den håller på att skapa genom följande steg:  

1.  Bokföringsdatum för den transaktion som skapas är från början samma datum som för den transaktion den justerar.  

2.  Bokföringsdatum verifieras mot lagerperioder och/eller redovisningsinställningar.  

3.  Fördelningen av bokföringsdatum: Om det ursprungliga bokföringsdatumet inte ligger inom tillåtet intervall, tilldelar batchjobbet ett tillåtet bokföringsdatum från antingen Redovisningsinställningar eller Lagerperiod. Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att tilldelas justeringsvärdetransaktionen.  

 Vi ska nu granska denna process i praktiken. Anta att vi har en försäljningspost för en artikeltransaktion. Artikeln skeppades iväg den 5 september 2013 och fakturerades dagen efter.  

![Artikeltransaktion: Datumformat: ÅÅÅÅ MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")  

Nedan representerar den första värdetransaktionen (379) själva leveransen och bär samma bokföringsdatum som den överordnade artikeltransaktionen.  

Den andra värdetransaktionen (381) motsvarar fakturan.  

 Den tredje värdetransaktionen (391) är en justering av värdetransaktionen för fakturering (381)  

 ![Artikeltransaktion: Datumformat: ÅÅÅÅ MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")  

 Steg 1: Justeringsvärdetransaktionen som ska skapas tilldelas samma bokföringsdatum som den transaktion den justerar, vilket illustreras ovan genom värdetransaktion 391.  

 Steg 2: Validering av ursprungligen tilldelat bokföringsdatum.  

Batchjobbet **Justera kost.-artikeltrans** avgör om justeringsvärdetransaktionens inledande bokföringsdatum ligger inom tillåtet spann för bokföringsdatum baserat på lagerperioder och/eller redovisningsinställningar.  

 Vi ska nu granska ovannämnda försäljning genom att lägga till inställningen av tillåtna datumintervall för bokföring.  

 Lagerperioder:  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")

 Första tillåtna bokföringsdatum är den första dagen i den första öppna perioden. 1 september 2013.  

 Redovisningsinställningar:  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")

 Första tillåtna bokföringsdatum är det datum som anges i fältet Tillåt bokföring från: 10 September 2013.  

 Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att bestämma det tillåtna datumspannet för bokföring.  

 Steg 3: Fördelning av ett tillåtet bokföringsdatum.  

 Det ursprungliga tilldelade bokföringsdatumet var den 6 september, vilket visas i steg 1. I det andra steget identifierar emellertid batchjobbet Justera kostn. – Artikeltrans att det tidigast tillåtna bokföringsdatumet är den 10 september och tilldelar därmed den 10 september till justeringsvärdetransaktionen nedan.  

 ![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")

 Vi har nu gått igenom hur man tilldelar bokföringsdatum för värdetransaktioner som skapats genom batchjobbet Justera kost. - artikeltrans.  

 Vi fortsätter nu med att granska några scenarier som vi i supportteamet då och då stöter på i samband med tilldelade boföringsdatum i batchjobbet Justera kost. - artikeltrans och relaterade inställningar.  

## <a name="scenarios"></a>Scenarierna  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenario I: "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum..."  
 Dett är ett scenario där en användare får nämnda felmeddelande när batch-jobbet Justera kost. - artikeltrans körs.  

 I föregående avsnitt, som beskrev begreppet att tilldela bokföringsdatum, var syftet med batch-jobbet Justera kost. - artikeltrans att skapa en Värdetransaktion med bokföringsdatum 10 september.  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")

 Vi följer upp användarinställningarna:  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")

 Användaren i detta exempel har ett tillåtet datumintervall för bokföring från den 11 september till den 30 september, och får därmed inte bokföra justeringsvärdetransaktionen med bokföringsdatum 10 september.  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")

 Kunskapsbasartikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) beskriver ytterligare scenarion relaterade till nämnda felmeddelande.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenario II: Bokföringsdatum på justeringsvärdetransaktionen jämfört med bokföringsdatum för transaktionen som orsakar justeringen, till exempel omvärdering eller artikelomkostnad.  

### <a name="revaluation-scenario"></a>Omvärderingsscenario:  
 Förutsättningar:  

 Lagerinställningar:  

-   Automatisk kostnadsbokföring = Ja  

-   Automatisk kostnadsjustering = Alltid  

-   Genoms. kost.ber.typ = artikel  

-   Period för genomsnittskostnad = Dag  

 Redovisningsinställningar:  

-   Tillåt bokföring från = 1 januari 2014  

-   Tillåt bokföring t.o.m. = tom  

 Användarinställningar:  

-   Tillåt bokföring från = 1 januari 2013.  

-   Tillåt bokföring t.o.m. = tom  

##### <a name="to-test-the-scenario"></a>För att testa scenariot  

1.  Skapa artikel TEST:  

     Basenhet = ST  

     Kostnad = Genomsnitt  

     Markera valfria bokföringsmallar.  

2.  Öppna artikeljournalen, skapa och bokför en rad så här:  

     Bokföringsdatum = 15 December 2013  

     Artikel = TEST  

     Trans.typ = Köp  

     Antal = 100  

     A-pris = 10  

3.  Öppna artikeljournalen, skapa och bokför en rad så här:  

     Datum = 20 december 2013  

     Artikel = TEST  

     Trans.typ = Negativ justering  

     Antal = 2  

4.  Öppna artikeljournalen, skapa och bokför en rad så här:  

     Datum = 15 januari 2014  

     Artikel = TEST  

     Trans.typ = Negativ justering  

     Antal = 3  

5.  Öppna omvärderingsjournalen, skapa och bokför en rad så här:  

     Artikel = TEST  

     Kopplas till löpnr = välj den inköpstransaktion som bokförts i steg 2. Bokföringsdatum för omvärderingen ska vara detsamma som den transaktionen som den justerar.  

     Styckkostnad (omvärderad) = 40  

 Följande artikeltransaktioner och värdetransaktioner har bokförts:  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")

 ![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")

 Batchjobbet Justera kost. - artikeltrans har identifierat en ändring i kostnad och justerat de negativa justeringarna.  

 **Granskning av bokföringsdatum på skapade justeringsvärdetransaktioner:** Tidigast tillåtna bokföringsdatum som batchjobbet Justera kost. - artikeltrans måste beakta är den 1 januari 2014, vilket anges i redovisningsinställningarna.  

 **Negativ justering i steg 3:** tilldelat bokföringsdatum är den 1 januari 1, vilket anges i redovisningsinställningarna. Bokföringsdatum för den värdetransaktion som ska omfattas av justering är den 20 december 2013. Enligt redovisningsinställningarna ligger datumet inte inom tillåtet datumintervall för bokföring. Därför tilldelas det bokföringsdatum som anges i fältet Tillåt bokföring fr.o.m i Redovisningsinställningar till justeringsvärdetransaktionen.  

 **Negativ justering i steg 4:** tilldelat bokföringsdatum är den 15 januari. Värdetransaktionen som omfattas av justering har bokföringsdatum 15 januari, vilket ligger inom intervallet för tillåten bokföring enligt redovisningsinställningarna.  

 Justeringen för den negativa justeringen i steg 3 förorsakar diskussion. Ett bättre bokföringsdatum för justeringsvärdetransaktionen hade varit den 20 december eller åtminstone i december, detta eftersom den omvärderingen som förorsakar ändringen i KSV bokfördes i december.  

 För att uppnå en decemberjustering av den negativa justeringen i steg 3 måste Redovisningsinställningar, fältet Tillåt bokföring fr.o.m, ange ett datum i december.  

 **Sammanfattning:**  

 Med erfarenheterna från detta scenario i ryggen och i beaktande av de lämpligaste inställningarna för tillåtet datumintervall för bokföring för ett företag, kan följande komma till nytta: Så länge ändringar i lagervärde får bokföras inom en period (i detta fall december) bör de inställningar som företaget använder för tillåtna bokföringsintervall justeras i enlighet med detta beslut. Fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna, som anger att den 1 december skulle låta omvärderingen utförd i december vidarebefordras till att påverka utgående transaktioner under samma period.  

 Användargrupper är inte behöriga att bokföra i december utan i januari, vilket troligen var avsett att begränsas av Redovisningsinställningarna i detta scenario, bör i stället tas upp via användarinställningarna.  

### <a name="item-charge-scenario"></a>Artikelomkostnadsscenario:  
 Förutsättningar:  

 Lagerinställningar:  

-   Automatisk kostnadsbokföring = Ja  

-   Automatisk kostnadsjustering = Alltid  

-   Genoms. kost.ber.typ = artikel  

-   Period för genomsnittskostnad = Dag  

 Redovisningsinställningar:  

-   Tillåt bokföring från = 1 januari 2013.  

-   Tillåt bokföring t.o.m. = tom  

 Användarinställningar:  

-   Tillåt bokföring från = 1 januari 2013.  

-   Tillåt bokföring t.o.m. = tom  

##### <a name="to-test-the-scenario"></a>För att testa scenariot  

1.  Skapa artikelomkostnad:  

     Basenhet = ST  

     Kostnad = Genomsnitt  

     Markera valfria bokföringsmallar.  

2.  Skapa en ny inköpsorder  

     Inköpsleverantörsnr: 10000  

     Bokföringsdatum = 15 December 2013  

     Leverantörens fakturanr: 1234  

     På inköpsorderraden:  

     Artikel = DEBITERING  

     Antal = 1  

     Inköpspris (BVA) = 100  

     Bokför Inleverera och Fakturera.  

3.  Skapa en ny försäljningsorder:  

     Förs.kundnr: 10000  

     Bokföringsdatum = 16 december 2013  

     På försäljningsorderraden:  

     Artikel = DEBITERING  

     Antal = 1  

     A-pris = 135  

     Bokför leverans och faktura.  

4.  Redovisningsinställningar:  

     Tillåt bokföring från = 1 januari 2014  

     Tillåt bokföring t.o.m. = tom  

5.  Skapa en ny inköpsorder:  

     Inköpsleverantörsnr: 10000  

     Bokföringsdatum = 2 januari 2014  

     Leverantörens fakturanr: 2345  

     På inköpsorderraden:  

     Artikelomkostnad = JB-FRAKT  

     Antal = 1  

     Inköpspris (BVA) = 3  

     Tilldela artikelomkostnader till inleverans från steg 2.  

     Bokför inleverans och faktura.  

     ![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")

6.  Arbetsdagen 3 januari anländer en inköpsfaktura med ytterligare artikelomkostnader till inköpet i steg 2. Fakturan har den dokumentdatumet den 30 december och bokförs därför med bokföringsdatum 30 december 2013.  

     Skapa en ny inköpsorder:  

     Inköpsleverantörsnr: 10000  

     Bokföringsdatum = 30 december 2013  

     Leverantörens fakturanr: 3456  

     På inköpsorderraden:  

     Artikelomkostnad = JB-FRAKT  

     Antal = 1  

     Inköpspris (BVA) = 2  

     Tilldela artikelomkostnader till inleverans från steg 2.  

     Bokför inleverans och faktura.  

   ![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")

 Rapporten Lagervärdering skrivs ut per den 31 december 2013  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")

 **Summering av scenario:**  

 Beskrivet scenario erhåller i slutändan en lagervärderingsrapport som visar antalet = 0 när värdet = 2. Artikelomkostnaden som bokfördes i steg 11 är en del av värdet Lagerökning för december, medan lagerminskningen för samma period inte påverkas.  

 Att låta redovisningsinställningarna ange Tillåt bokföring fr.o.m den 1 januari var användbart för den första artikelomkostnaden. Kostnaderna för ökat och minskat lager registrerades under samma period. För den andra artikelomkostnaden gör emellertid redovisningsinställningarna att ändringen i KSV bokförs under nästkommande period.  

 **Sammanfattning:**  

 Det är svårt att låta rapporten Lagerutvärdering visa kvantiteten = 0 när värdet är <> 0. I detta fall är det också svårare att uttrycka de optimala inställningarna då inköpsfakturorna anländer samma dag men adresserar olika perioder eller till och med räkenskapsår. Att flytta fram till ett nytt räkenskapsår kräver vanligtvis lite planering, och som ett led i insikten för transaktionsprocessen Justera kost. - artikeltrans måste KSV-detektering beaktas.  

 I detta scenario kunde ett alternativ vara att låta Redovisningsinställningarna, fältet Tillåt bokföring fr.o.m att ange ett datum i december några dagar längre fram, samt att flytta fram bokföringen av den första artikelomkostnaden, detta i syfte att låta alla kostnader för föregående period/räkenskapsår först registreras för den period som de tillhör, köra batch-jobbet Justera kostn. - artikeltrans. och därefter flytta tillåtet bokföringsdatum till den nya perioden\/det nya räkenskapsåret. Därefter kan den artikelomkostnaden med bokföringsdatum 2 januari bokföras.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historik för batch-jobbet Justera kost. - artikeltrans  
 Nedan visas en sammanfattning av begreppet Bokföra datum för justeringsvärdetransaktioner utförda av batch-jobbet Justera kost. - artikeltrans. sedan version 3.0.  

### <a name="from-version-30370a"></a>Från version 3.0..3.70.A  
 I begäranformuläret i batch-jobbet Justera kost. - artikeltrans är finns ett bokföringsdatum som ska anges av användaren. Batch-jobbet körs genom alla nödvändiga förändringar och skapar värdetransaktioner med det bokföringsdatum som har angetts i formuläret. Föreslaget bokföringsdatum som ska användas är dagens datum.  

### <a name="version-370b40"></a>Version 3.70.B..4.0  
 I begäranformuläret i batch-jobbet Justera kost. - artikeltrans finns ett bokföringsdatum för stängd periodtransaktion som ska anges av användaren. Batch-jobbet körs genom alla nödvändiga ändringar och skapar värdetransaktioner med bokföringsdatumet för den överordnade artikeltransaktionen (leveransdatumet för den försäljning som justeringen adresserar). Om bokföringsdatumet för den överordnade artikeltransaktionen inte faller inom det tillåtna bokföringsintervallet, kommer det bokföringsdatum som angetts som bokföringsdatum för stängd periodtransaktion att tilldelas justeringsvärdetransaktionen. Ett datum anses ligga i en stängd period då det infaller före datumet i fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna.  

### <a name="from-version-50"></a>Från version 5.0:  
 I batch-jobbet Justera kost. - artikeltrans finns inte längre något bokföringsdatum som måste anges av användaren. Batch-jobbet körs igenom alla nödvändiga förändringar och skapar värdetransaktioner med samma bokföringsdatum som den värdetransaktion jobbet korrigerar. Om bokföringsdatumet inte ligger inom tillåtet intervall används bokföringsdatumet i fältet Tillåt bokföring fr.o.m. i Redovisningsinställningarna ELLER, om lagerperioder används, så används det senare datumet av de båda. Se begreppsbeskrivningen ovan.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historik för Bokför lagerkostnad i redov.  
 Batch-jobbet Bokför lagerkostnad i redovisning är nära knutet till batch-jobbet Justera kost.-artikeltrans, varför historiken för batch-jobbet även summeras och delas här.  

### <a name="from-version-30370a"></a>Från version 3.0..3.70.A  
 I begäranformuläret i Bokför lagerkostnad i redov. finns ett bokföringsdatum som ska anges av användaren. Batch-jobbet körs genom alla värdetransaktioner i filtret (om sådana finns) och skapar redovisningstransaktioner med det bokföringsdatum som har angetts i formuläret.  

### <a name="version-370b40"></a>Version 3.70.B..4.0  
 I begäranformuläret i Bokför lagerkostnad i redov. är finns fältet Bokföringsdatum för stängd periodtransaktion tillgängligt. Programmet använder det datum som du anger i detta fält som bokföringsdatum för de redovisningstransaktioner som skapas för värdetransaktioner vars bokföringsdatum finns i avslutade bokföringsperioder. I annat fall kommer redovisningstransaktionerna att ha samma bokföringsdatum som de ursprungliga värdetransaktionerna. Ett datum anses ligga i en stängd period då det infaller före datumet i fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna. Om du bokför G\/L per bokföringsmall kommer redovisningstransaktionerna att få det bokföringsdatum som har angetts i fältet Bokföringsdatum i formuläret.  

 I version 3 och 4 söker batch-jobbet igenom alla värdetransaktioner i syfte att undersöka om det finns några värdetransaktioner där kost.belopp (faktiskt) skiljer sig från den kostnad som bokförts i redov. Om det finns skillnader kommer skillnaden att bokföras i en redovisningstransaktion. Om förväntad kostnadsbokföring används kommer motsvarande fält att bearbetas på samma sätt.  

![Justera kostn. &#45;artikeltransaktionsdata](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")

### <a name="from-version-50"></a>Från version 5.0:  
 I batch-jobbet Bokför lagerkostnad i redov. finns inte längre något bokföringsdatum som måste anges i begäranformuläret. Bokföringstransaktionen skapas med samma bokföringsdatum som den relaterade värdetransaktionen. Datumintervall för tillåten bokföring måste tillåta bokföringsdatumet för redovisningstransaktionen som skapats för att avsluta batch-jobbet. I annat fall måste datumintervallet för tillåten bokföring tillfälligt öppnas igen genom att ändra eller ta bort datumen i fältet Tillåt bokföring fr.o.m och Till i Redovisningsinställningarna. För att undvika avstämningsproblem krävs att okföringsdatum för redovisningstransaktionen motsvarar bokföringsdatumet för värdetransaktionen.  

 Batch-jobbet söker igenom tabellen 5811 - Bokför värdetransaktion i redovisning i syfte att identifiera värdetransaktionerna i omfånget för bokföring i redovisningen. Tabellen töms efter slutförd körning.  

 All feedback kring hur denna process och dokumentationen kan utvecklas ytterligare är varmt välkommen.  

 Helene Holmin  

 Dynamics NAV-utvecklingsingenjör  

## <a name="see-also"></a>Se även  
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  

