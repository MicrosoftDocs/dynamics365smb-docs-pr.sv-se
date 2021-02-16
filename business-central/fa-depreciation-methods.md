---
title: Avskrivningsmetoder | Microsoft Docs
description: Lär dig mer om de olika metoderna för avskrivning eller nedskrivning av anläggningstillgångar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6f349d7a77078536b7a61e14b5dcd4169ba0f9b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749499"
---
# <a name="depreciation-methods"></a>Avskrivningsmetoder
Det finns åtta avskrivningsmetoder att tillgå:  

* Linjär  
* Degressiv 1  
* Degressiv 2  
* DEG1/LIN  
* DEG2/LIN  
* Användardefinierad  
* Manuell  

  > [!NOTE]  
  >   Du kan använda den här metoden för tillgångar som du inte längre kan skriva av, exempelvis mark. Du måste föra in avskrivningen i redovisningsjournalen för anläggningstillgångar. Batch-jobbet **Beräkna avskrivning** utesluter anläggningstillgångar där denna avskrivningsmetod används.  
* Halvårspraxis  

  > [!NOTE]  
  >    När du använder den här metoden avskrivs en anläggningstillgång med samma belopp varje år.  

## <a name="straight-line-depreciation"></a>Linjär avskrivning
När du använder den linjära metoden måste du ange ett av följande alternativ i avskrivningsregeln för anläggningstillgångar:  

* avskrivningsperiod (år eller månader) eller ett slutdatum för avskrivningen  
* en fast årlig procentsats  
* ett fast årligt belopp  
* avskrivningsperiod  

### <a name="depreciation-period"></a>Avskrivningsperiod
Om du anger en avskrivningsperiod (antal avskrivningsår, antal avskrivningsmånader eller slutdatum för avskrivningen) används den här formeln vid beräkning av avskrivningsbeloppet:  

*Avskrivningsbelopp = ((Bokföringsvärde – Återanskaffningsvärde) × Antal avskrivningsdagar) / Återstående avskrivningsdagar*  

De återstående avskrivningsdagarna beräknas som antalet avskrivningsdagar minus antalet dagar mellan avskrivningens startdatum och den senaste anläggningstillgångstransaktionens datum.  

Bokföringsvärdet kan minskas genom bokförd uppskrivning, nedskrivning, val 1- eller val 2-belopp, om fältet **Ta med i avskrivningsberäkning** är inaktiverat och om fältet **Ingår i bokföringsvärde** är aktiverat på sidan **Anl. inställning bokföring**. Genom den här beräkningen garanteras att anläggningstillgången helt är avskriven på slutdatum för avskrivningen.  

### <a name="fixed-yearly-percentage"></a>Fast årlig procentsats
Om du anger en fast årlig procentsats används följande formel vid beräkning av avskrivningsbeloppet:  

Avskrivningsbelopp = (Linjär % × Avskrivningsbas × Antal avskr.dagar) / (100 × 360)  

### <a name="fixed-yearly-amount"></a>Fast årligt belopp
Om du anger ett fast årligt belopp används följande formel vid beräkning av avskrivningsbeloppet:  

Avskrivningsbelopp = (Fast avskrivningsbelopp × Antal avskrivningsdagar) / 360  

### <a name="example---straight-line-depreciation"></a>Exempel – linjär avskrivningsmetod
Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Den beräknade livslängden är åtta år. Batch-jobbet **Beräkna avskrivning** körs två gånger per år.  

För detta exempel ser anläggningstillgångstransaktionen ut så här:  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-01-01 |Anskaffningskostnad |* |100,000.00 |100,000.00 |
| 10-06-30 |Avskrivning |180 |-6 250,00 |93,750.00 |
| 10-12-31 |Avskrivning |180 |-6 250,00 |87,500.00 |
| 11-06-30 |Avskrivning |180 |-6 250,00 |81,250.00 |
| 11-12-31 |Avskrivning |180 |-6 250,00 |75,000.00 |
| 17-06-30 |Avskrivning |180 |-6 250,00 |6,250.00 |
| 17-12-31 |Avskrivning |180 |-6 250,00 |0 |

* Avskrivning startdatum  

## <a name="declining-balance-1-depreciation"></a>Degressiv 1, avskrivning
Det här är en accelererande avskrivningsmetod som fördelar den största delen av kostnaden för en tillgång på de första åren av tillgångens livslängd. Om du använder den här metoden måste du ange en fast årlig procentsats.  

Följande formel beräknar avskrivningsbelopp:  

*Avskrivningsbelopp = (Degressiv % × Antal avskr.dagar × Avskrivningsbas) / (100 × 360)*  

Avskrivningsbasen beräknas som bokföringsvärdet för den lägsta bokförda avskrivningen sedan startdatumet för det aktuella räkenskapsåret.  

Det bokförda avskrivningsbeloppet kan innehålla transaktioner av olika bokföringstyper (nedskrivning, val 1 och val 2) som har bokförts efter startdatumet för det aktuella räkenskapsåret. De här bokföringstyperna inkluderas i det bokförda avskrivningsbeloppet om fälten **Avskrivningstyp** och **Ingår i bokföringsvärde** är markerade på sidan **Anl. inställning bokföring**.  

### <a name="example---declining-balance-1-depreciation"></a>Exempel – Degressiv 1, avskrivning
Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Värdet i fältet **Degressiv %** är 25. Batch-jobbet **Beräkna avskrivning** körs två gånger per år.  

Följande tabell visar hur anläggningstillgångstransaktionerna ser ut.  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-01-01 |Anskaffningskostnader |* |100,000.00 |100,000.00 |
| 10-06-30 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 10-12-31 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 11-06-30 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 11-12-31 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 12-06-30 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 12-12-31 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 13-06-30 |Avskrivning |180 |-5 273,44 |36,914.06 |
| 13-12-31 |Avskrivning |180 |-5 273,44 |31,640.62 |
| 14-06-30 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 14-12-31 |Avskrivning |180 |-3 955,08 |23,730.46 |

* Avskrivning startdatum  

    Beräkningsmetod:  

    *Första året: 25 % av 100 000 = 25 000 = 12 500 + 12 500*

    *Andra året: 25 % av 75 000 = 18 750 = 9 375 + 9 375*

    *Tredje året: 25 % av 56 250 = 14 062,50 = 7 031,25 + 7 031,25*

    Beräkningen fortsätter tills bokföringsvärdet är lika med det avrundade slutavskrivningsbelopp eller det återanskaffningsvärde som du har angett.   

## <a name="declining-balance-2-depreciation"></a>Degressiv 2, avskrivning
Med metoderna Degressiv 1 och Degressiv 2 beräknas samma totala avskrivningsbelopp för varje år. Om du däremot vill köra batch-jobbet **Beräkna avskrivning** mer än en gång om året resulterar metoden Degressiv 1 i lika stora avskrivningsbelopp för varje avskrivningsperiod. Metoden Degressiv 2 resulterar däremot i avskrivningsbelopp som minskar för varje period.  

### <a name="example---declining-balance-2-depreciation"></a>Exempel – Degressiv 2, avskrivning
Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Värdet i fältet **Degressiv %** är 25. Batch-jobbet **Beräkna avskrivning** körs två gånger per år. Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-01-01 |Anskaffningskostnader |* |100,000.00 |100,000.00 |
| 10-06-30 |Avskrivning |180 |–13 397,46 |86,602.54 |
| 10-12-31 |Avskrivning |180 |–11 602,54 |75,000.00 |
| 11-06-30 |Avskrivning |180 |–10 048,09 |64,951.91 |
| 11-12-31 |Avskrivning |180 |–8 701,91 |56,250.00 |

* Avskrivning startdatum  

Beräkningsmetod:  

* BV = Bokföringsvärde  
* ND = Antal avskrivningsdagar  
* DBP = Degressiv procent  
* P = DBP/100  
* D = ND/360  

Beräkningsformeln för avskrivningsbelopp är:  

*DA = BV x (1 – (1 –P)<sup>D<sup>*  

Avskrivningsvärdena är:  

| Datum | Beräkning |
| --- | --- |
| 10-06-30 |DA = 100 000,00 x (1 – (1 – 0,25)<sup> 0,5<sup>) = 13 397,46 |
| 10-12-31 |DA = 86 602,54 x (1 – (1 – 0,25)<sup> 0,5<sup>) = 11 602,54 |
| 11-06-30 |DA = 75 000,00 x (1 – (1 – 0,25)<sup> 0,5<sup>) = 10 048,09 |
| 11-12-31 |DA = 64 951,91 x (1 – (1 – 0,25)<sup> 0,5<sup>) = 8 701,91 |

## <a name="db1sl-depreciation"></a>DB1/SL Avskrivning
DEG1/LIN är en förkortning av Degressiv 1 och Linjär. Beräkningen fortsätter tills bokföringsvärdet är lika med det avrundade slutavskrivningsbelopp eller det återanskaffningsvärde som du har angett.  

**Beräkna avskrivning** beräknar både ett linjärt belopp och ett degressivt belopp, men endast det större av beloppen förs över till journalen.  

Du kan använda olika procentsatser för att beräkna degressiv.  

Om du använder den här metoden måste du ange den beräknade livslängden och en degressiv procentsats på sidan **Anl. avskrivningsregel**.  

### <a name="example---db1-sl-depreciation"></a>Exempel – DB1-SL-avskrivning
Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Värdet i fältet **Degressiv %** på sidan **Anl.avskrivningsregel** är 25 och värdet i fältet **Antal avskrivningsår** är 8. Batch-jobbet **Beräkna avskrivning** körs två gånger per år.  

Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-01-01 |Anskaffningskostnader |* |100,000.00 |100,000.00 |
| 10-06-30 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 10-12-31 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 11-06-30 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 11-12-31 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 12-06-30 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 12-12-31 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 13-06-30 |Avskrivning |180 |-5 273,44 |36,914.06 |
| 13-12-31 |Avskrivning |180 |-5 273,44 |31,640.62 |
| 14-06-30 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 14-12-31 |Avskrivning |180 |-3 955,08 |23,730.46 |
| 15-06-30 |Avskrivning |180 |-3 955,08 |19 775,38 LIN |
| 15-12-31 |Avskrivning |180 |-3 955,08 |15 820,30 LIN |
| 16-06-30 |Avskrivning |180 |-3 955,08 |11 865,22 LIN |
| 16-12-31 |Avskrivning |180 |-3 955,07 |7 910,15 LIN |
| 17-06-30 |Avskrivning |180 |-3 955,08 |3 955,07 LIN |
| 17-12-31 |Avskrivning |180 |-3 955,07 |0,00 LIN |

* Avskrivning startdatum  

"SL" efter bokföringsvärdet betyder att den linjära metoden har använts.  

Beräkningsmetod:  

Första året:  

*Degressivt belopp: 25 % av 100 000 = 25 000 = 12 500 + 12 500*  

*Linjärt belopp = 100 000 / 8 = 12 500 = 6 250 + 6 250*  

Det degressiva beloppet används eftersom det är det större beloppet.  

Sjätte året (2015):  

*Degressivt belopp: 25 % av 23 730,46 = 4 943,85 = 2 471,92 + 2 471,92*  

*Linjärt värde = 23 730,46/3 = 7 910,15 = 3 995,07 + 3 995,08*  

Det linjära beloppet används eftersom det är det större beloppet.  

## <a name="user-defined-depreciation"></a>Användardefinierad avskrivning
I det här programmet finns en funktion som gör att du kan skapa användardefinierade avskrivningsmetoder.  

Med en användardefinierad metod använder du sidan **Avskrivningstabeller** där du måste ange en avskrivningsprocent för varje period (månad, kvartal, år eller bokföringsperiod).  

Beräkningsformeln för avskrivningsbelopp är:  

Avskrivningsbelopp = (Avskrivning % × Antal avskr.dagar × Avskrivningsbas) / (100 × 360)  

### <a name="depreciation-based-on-number-of-units"></a>Avskrivning baserad på antal enheter
Den här användardefinierade metoden kan även användas för avskrivning baserad på enheter, till exempel när det gäller produktionsmaskiner med en fastställd livslängdskapacitet. På sidan **Avskrivningstabeller** kan du ange det antal enheter som kan produceras under varje period (månad, kvartal, år eller bokföringsperiod).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Så här skapar du användardefinierade avskrivningsmetoder
På sidan **Avskrivning tabellkort** kan du skapa användardefinierad avskrivningsmetod. Du kan till exempel lägga upp avskrivning baserad på antalet enheter.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Avskrivningstabeller** och välj sedan tillhörande länk.  
2. På sidan **Avskrivning tabellista** väljer du åtgärden **Ny**.  
3. På sidan **Avskrivning tabellkort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="example---user-defined-depreciation"></a>Exempel – Användardefinierad avskrivning
Du kan använda en avskrivningsmetod som gör det möjligt att av skatteskäl skriva av tillgångar snabbare.  

Du ska av skatteskäl använda följande avskrivningsgrad för en anläggningstillgång med en livslängd på tre år:  

* År 1: 25%  
* År 2: 38%  
* År 3: 37%  

Anskaffningskostnaden är 100 000 BVA och livslängden är fem år. Avskrivningen beräknas en gång om året.  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-01-01 |Anskaffningskostnad |* |100,000.00 |100,000.00 |
| 10-12-31 |Avskrivning |360 |-25 000,00 |75,000.00 |
| 11-12-31 |Avskrivning |360 |-38 000,00 |37,000.00 |
| 12-12-31 |Avskrivning |360 |-37 000,00 |0 |
| 13-12-31 |Avskrivning |Ingen |Ingen |0 |
| 14-12-31 |Avskrivning |Ingen |Ingen |0 |

* Avskrivning startdatum  

Om du använder en användardefinierad metod, måste fälten **Startdatum använd.def. avskrv.** och **Avskrivning startdatum** fyllas i på sidan **Anl. avskrivningsregler**. Fältet **Startdatum använd.def. avskrv.** och innehåller i fältet **Period** på sidan **Avskrivningstabeller** används för att bestämma vilket tidsintervall som ska användas för beräkning av avskrivning. Detta garanterar att programmet ska påbörjas genom att använda den angivna procentsatsen på samma dag för alla tillgångar. Fältet **Avskrivning startdatum** används för att beräkna antalet avskrivningsdagar.  

I föregående exempel innehöll både **Startdatum använd.def. avskrv.** och **Avskrivning startdatum** 01-01-01. Om däremot **Startdatum använd.def. avskrv.** innehåller 10-01-01 och **Avskrivning startdatum** innehåller 11-01-04 blir resultatet:  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-01-01 |Anskaffningskostnad |* |100,000.00 |100,000.00 |
| 10-12-31 |Avskrivning |270 |-18 750,00 |81,250.00 |
| 11-12-31 |Avskrivning |360 |-38 000,00 |42,250.00 |
| 12-12-31 |Avskrivning |360 |-37 000,00 |6,250.00 |
| 13-12-31 |Avskrivning |90 |-6 250,00 |0 |
| 14-12-31 |Avskrivning |Ingen |Ingen |0 |

* Avskrivning startdatum  

## <a name="half-year-convention-depreciation"></a>Avskrivning med halvårspraxis
Metoden Halvårspraxis kan endast användas om du har markerat fältet **Använd halvårsgammal** på sidan **Avskrivningsregel för anl.tillg.**.  

Den här avskrivningsregeln kan användas tillsammans med följande avskrivningsmetoder i programmet:  

* Linjär  
* Degressiv 1  
* DEG1/LIN  

När du använder Halvårspraxis kommer en avskrivning på sex månader att tillämpas det första räkenskapsåret, oavsett innehållet i fältet **Avskrivning startdatum**.  

> [!NOTE]  
>   Den beräknade livslängd för en anläggningstillgång som återstår efter det första räkenskapsåret kommer alltid att innehålla ett halvår med hjälp av metoden Halvårspraxis. För att metoden Halvårspraxis ska användas på rätt sätt måste fältet **Avskrivning slutdatum** på sidan **Avskrivningsregel för anl.tillg.** alltid innehålla ett datum som infaller exakt sex månader före slutdatumet för det räkenskapsår då anläggningstillgången helt har avskrivits.  

### <a name="example---half-year-convention-depreciation"></a>Exempel: Avskrivning med metoden Halvårspraxis
Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. **Avskrivningens startdatum** är 10-03-01. Den beräknade livslängden är fem år så **avskrivningens slutdatum** blir 15-06-30. Batch-jobbet **Beräkna avskrivning** körs en gång om året. Detta exempel bygger på att räkenskapsåret sammanfaller med kalenderåret.  

Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-03-01 |Anskaffningskostnad |* |100,000.00 |100,000.00 |
| 10-12-31 |Avskrivning |270 |-10 000,00 |90,000.00 |
| 11-12-31 |Avskrivning |360 |-20 000,00 |70,000.00 |
| 12-12-31 |Avskrivning |360 |-20 000,00 |50,000.00 |
| 13-12-31 |Avskrivning |360 |-20 000,00 |30,000.00 |
| 14-12-31 |Avskrivning |360 |-20 000,00 |10,000.00 |
| 15-12-31 |Avskrivning |180 |-10 000,00 |0.00 |

* Avskrivning startdatum  

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Exempel: DEG1/LIN-avskrivning med metoden Halvårspraxis
Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. **Avskrivningens startdatum** är 10-11-01. Den beräknade livslängden är fem år så **avskrivningens slutdatum** blir 15-06-30. På sidan **Anl. avskrivningsregler** är värdet 40 i fältet **Degressiv %**. Batch-jobbet **Beräkna avskrivning** körs en gång om året. Detta exempel bygger på att räkenskapsåret sammanfaller med kalenderåret.  

Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl. bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 10-11-01 |Anskaffningskostnad |* |100,000.00 |100,000.00 |
| 10-12-31 |Avskrivning |60 |-20 000,00 |80,000.00 |
| 11-12-31 |Avskrivning |360 |-32 000,00 |48,000.00 |
| 12-12-31 |Avskrivning |360 |-19 200,00 |28,800.00 |
| 13-12-31 |Avskrivning |360 |-11 520,00 |17,280.00 |
| 14-12-31 |Avskrivning |360 |-11 520,00 |5 760,00 LIN |
| 15-12-31 |Avskrivning |180 |-5 760,00 |0,00 LIN |

* Avskrivning startdatum  

"SL" efter bokföringsvärdet betyder att den linjära metoden har använts.  

Beräkningsmetod:  

Första året:  

*Degressivt belopp = Helårsbelopp = 40 % av 100 000 = 40 000. Halvår: 40 000 / 2 = 20 000*  

*Linjärt belopp = Helårsbelopp = 100 000 / 5=20 000. Halvår: 20 000 / 2 = 10 000*  

Det degressiva beloppet används eftersom det är det större beloppet.  

Femte året (2004):  

*Degressivt belopp = 40 % av 17 280,00 = 6 912,00*  

*Linjärt belopp = 28 800 / 1,5 = 11 520,00*  

Det linjära beloppet används eftersom det är det större beloppet.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Kopiera transaktioner till fler avskrivningsregler
Om du har tre avskrivningsregler, B1, B2 och B3, och vill kopiera transaktioner från B1 till B2 och B3 kan du markera fältet **Ingår i dubblettlista** på avskrivningsregelkorten för B2 och B3. Detta är praktiskt om avskrivningsregel B1 är integrerad med redovisningen samt använder redovisningsjournalen för anläggningstillgångar och om avskrivningsreglerna B2 och B3 inte är integrerade med redovisningen och använder journalen för anläggningstillgångar.  

När du registrerar en transaktion i B1 i redovisningsjournalen för anläggningstillgångar och markerar fältet **Använd dubblettlista** kopieras transaktionen till regel B2 och B3 i journalen för anläggningstillgångar när transaktionen har bokförts.  

> [!NOTE]  
>   Du kan inte kopiera till samma journal som du kopierar från. Om du bokför transaktioner i redovisningsjournalen för anläggningstillgångar kan du kopiera dem till journalen för anläggningstillgångar eller till redovisningsjournalen för anläggningstillgångar med hjälp av en annan journal.  

> [!NOTE]  
>   Det är inte möjligt att använda samma nummerserie i Anl. redovisningsjournal och Anl.journal. När du bokför transaktioner i redovisningsjournalen för anläggningstillgångar måste du lämna fältet **Dokumentnr** tomt. Om du anger ett nummer i fältet dupliceras det numret i anläggningstillgångsjournalen. Du måste ändra verifikationsnummer manuellt innan du kan bokföra raderna.  

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
