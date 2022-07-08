---
title: Avskrivningsmetoder för anläggningstillgångar
description: Lär dig mer om de olika inbyggda metoderna för att skriva av eller skriva ned anläggningstillgångar i standardversionen av Business Central som inkluderar åtta metoder.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: 5629, 5633
ms.date: 07/05/2021
ms.author: edupont
ms.openlocfilehash: ec81b14510d89729f7c51f95a3907db38e3876ea
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075947"
---
# <a name="depreciation-methods-for-fixed-assets"></a>Avskrivningsmetoder för anläggningstillgångar

Det finns åtta avskrivningsmetoder tillgängliga i standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Linjär  
* Degressiv 1  
* Degressiv 2  
* DEG1/LIN  
* DEG2/LIN  
* Användardefinierad  

  > [!NOTE]  
  > Ange din egen avskrivningsmetod genom att definiera avskrivningstabeller. Information om hur du tillämpar en användardefinierad avskrivningsmetod finns i [Konfigurera användardefinierad avskrivningsmetod](fa-how-setup-user-defined-depreciation-method.md).
* Manuell  

  > [!NOTE]  
  > Du kan använda den här metoden för tillgångar som du inte längre kan skriva av, exempelvis mark. Du måste föra in avskrivningen i redovisningsjournalen för anläggningstillgångar. Batch-jobbet **Beräkna avskrivning** utesluter anläggningstillgångar där denna avskrivningsmetod används.  
* Halvårspraxis  

  > [!NOTE]  
  > När du använder den här metoden avskrivs en anläggningstillgång med samma belopp varje år.  

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

*Avskrivningsbelopp = (Linjär % × Avskrivningsbas × Antal avskr.dagar) / (100 × 360)*  

### <a name="fixed-yearly-amount"></a>Fast årligt belopp

Om du anger ett fast årligt belopp används följande formel vid beräkning av avskrivningsbeloppet:  

*Avskrivningsbelopp = (Fast avskrivningsbelopp × Antal avskrivningsdagar) / 360*  

### <a name="example---straight-line-depreciation"></a>Exempel – linjär avskrivningsmetod

Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Den beräknade livslängden är åtta år. Batch-jobbet **Beräkna avskrivning** körs två gånger per år.  

För detta exempel ser anläggningstillgångstransaktionen ut så här:  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-01-01 |Anskaffningskostnad |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-06-30 |Avskrivning |180 |-6 250,00 |93,750.00 |
| 20-12-31 |Avskrivning |180 |-6 250,00 |87,500.00 |
| 21-06-30 |Avskrivning |180 |-6 250,00 |81,250.00 |
| 21-12-31 |Avskrivning |180 |-6 250,00 |75,000.00 |
| 27-06-30 |Avskrivning |180 |-6 250,00 |6,250.00 |
| 27-12-31 |Avskrivning |180 |-6 250,00 |0 |

## <a name="declining-balance-1-depreciation"></a>Degressiv 1, avskrivning

Det här är en accelererande avskrivningsmetod som fördelar den största delen av kostnaden för en tillgång på de första åren av tillgångens livslängd. Om du använder den här metoden måste du ange en fast årlig procentsats.  

Följande formel beräknar avskrivningsbelopp:  

*Avskrivningsbelopp = (Degressiv % × Antal avskr.dagar × Avskrivningsbas) / (100 × 360)*  

Avskrivningsbasen beräknas som bokföringsvärdet för den lägsta bokförda avskrivningen sedan startdatumet för det aktuella räkenskapsåret.  

Det bokförda avskrivningsbeloppet kan innehålla transaktioner av olika bokföringstyper (nedskrivning, val 1 och val 2) som har bokförts efter startdatumet för det aktuella räkenskapsåret. De här bokföringstyperna inkluderas i det bokförda avskrivningsbeloppet om fälten **Avskrivningstyp** och **Ingår i bokföringsvärde** är markerade på sidan **Anl. inställning bokföring**.  

### <a name="example---declining-balance-1-depreciation"></a>Exempel – Degressiv 1, avskrivning

Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Värdet i fältet **Degressiv %** är 25. Batch-jobbet **Beräkna avskrivning** körs två gånger per år.  

Följande tabell visar hur anläggningstillgångstransaktionerna ser ut.  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-01-01 |Anskaffningskostnader |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-06-30 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 20-12-31 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 21-06-30 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 21-12-31 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 22-06-30 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 22-12-31 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 23-06-30 |Avskrivning |180 |-5 273,44 |36,914.06 |
| 23-12-31 |Avskrivning |180 |-5 273,44 |31,640.62 |
| 24-06-30 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 24-12-31 |Avskrivning |180 |-3 955,08 |23,730.46 |

Beräkningsmetod:  

* År 1: *25 % av 100 000 = 25 000 = 12 500 + 12 500*

* År 2: *25 % av 75 000 = 18 750 = 9 375 + 9 375*

* År 3: *25 % av 56 250 = 14 062,50 = 7 031,25 + 7 031,25*

Beräkningen fortsätter tills bokföringsvärdet är lika med det avrundade slutavskrivningsbelopp eller det återanskaffningsvärde som du har angett.  

## <a name="declining-balance-2-depreciation"></a>Degressiv 2, avskrivning

Med metoderna Degressiv 1 och Degressiv 2 beräknas samma totala avskrivningsbelopp för varje år. Om du däremot vill köra batch-jobbet **Beräkna avskrivning** mer än en gång om året resulterar metoden Degressiv 1 i lika stora avskrivningsbelopp för varje avskrivningsperiod. Metoden Degressiv 2 resulterar däremot i avskrivningsbelopp som minskar för varje period.  

### <a name="example---declining-balance-2-depreciation"></a>Exempel – Degressiv 2, avskrivning

Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Värdet i fältet **Degressiv %** är 25. Batch-jobbet **Beräkna avskrivning** körs två gånger per år. Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-01-01 |Anskaffningskostnader |(startdatum för avskrivning)|100,000.00 |100,000.00 |
| 20-06-30 |Avskrivning |180 |–13 397,46 |86,602.54 |
| 20-12-31 |Avskrivning |180 |–11 602,54 |75,000.00 |
| 21-06-30 |Avskrivning |180 |–10 048,09 |64,951.91 |
| 21-12-31 |Avskrivning |180 |–8 701,91 |56,250.00 |

Beräkningsmetod:  

* *BV* = Bokföringsvärde  
* *ND* = Antal avskrivningsdagar  
* *DBP* = Degressivt belopp  
* *P* = *DBP*/100  
* *D* = *ND*/360  

Beräkningsformeln för avskrivningsbelopp är:  

*DA* = *BV* x (1 – (1 –P)<sup>D</sup>)

Avskrivningsvärdena är:  

| Datum | Beräkning |
| --- | --- |
| 20-06-30 |DA = 100 000,00 x (1 – (1 – 0,25)<sup> 0,5</sup>) = 13 397,46 |
| 20-12-31 |DA = 86 602,54 x (1 – (1 – 0,25)<sup> 0,5</sup>) = 11 602,54 |
| 21-06-30 |DA = 75 000,00 x (1 – (1 – 0,25)<sup> 0,5</sup>) = 10 048,09 |
| 21-12-31 |DA = 64 951,91 x (1 – (1 – 0,25)<sup>0,5</sup>) = 8 701,91 |

## <a name="db1sl-depreciation"></a>DB1/SL Avskrivning

DEG1/LIN är en förkortning av Degressiv 1 och Linjär. Beräkningen fortsätter tills bokföringsvärdet är lika med det avrundade slutavskrivningsbelopp eller det återanskaffningsvärde som du har angett.  

**Beräkna avskrivning** beräknar både ett linjärt belopp och ett degressivt belopp, men endast det större av beloppen förs över till journalen.  

Du kan använda olika procentsatser för att beräkna degressiv.  

Om du använder den här metoden måste du ange den beräknade livslängden och en degressiv procentsats på sidan **Anl. avskrivningsregel**.  

### <a name="example---db1-sl-depreciation"></a>Exempel – DB1-SL-avskrivning

Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. Värdet i fältet **Degressiv %** på sidan **Anl.avskrivningsregel** är 25 och värdet i fältet **Antal avskrivningsår** är 8. Batch-jobbet **Beräkna avskrivning** körs två gånger per år.  

Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-01-01 |Anskaffningskostnader |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-06-30 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 20-12-31 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 21-06-30 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 21-12-31 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 22-06-30 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 22-12-31 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 23-06-30 |Avskrivning |180 |-5 273,44 |36,914.06 |
| 23-12-31 |Avskrivning |180 |-5 273,44 |31,640.62 |
| 24-06-30 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 24-12-31 |Avskrivning |180 |-3 955,08 |23,730.46 |
| 25-30-06 |Avskrivning |180 |-3 955,08 |19 775,38 LIN |
| 25-12-31 |Avskrivning |180 |-3 955,08 |15 820,30 LIN |
| 26-06-30 |Avskrivning |180 |-3 955,08 |11 865,22 LIN |
| 26-12-31 |Avskrivning |180 |-3 955,07 |7 910,15 LIN |
| 27-06-30 |Avskrivning |180 |-3 955,08 |3 955,07 LIN |
| 27-12-31 |Avskrivning |180 |-3 955,07 |0,00 LIN |

`SL` efter bokföringsvärdet betyder att den linjära metoden har använts.  

Beräkningsmetod:  

* År 1 (2020):  

    *Degressivt belopp: 25 % av 100 000 = 25 000 = 12 500 + 12 500*  

    *Linjärt belopp = 100 000 / 8 = 12 500 = 6 250 + 6 250*  

    Det degressiva beloppet används eftersom det är det större beloppet.  

* År 5 (2025):  

    *Degressivt belopp: 25 % av 23 730,46 = 4 943,85 = 2 471,92 + 2 471,92*  

    *Linjärt värde = 23 730,46/3 = 7 910,15 = 3 995,07 + 3 995,08*  

    Det linjära beloppet används eftersom det är det större beloppet.  

## <a name="half-year-convention-depreciation"></a>Avskrivning med halvårspraxis

Metoden Halvårspraxis kan endast användas om du har markerat fältet **Använd halvårsgammal** på sidan **Avskrivningsregel för anl.tillg.**.  

Den här avskrivningsregeln kan användas tillsammans med följande avskrivningsmetoder i programmet:  

* Linjär  
* Degressiv 1  
* DEG1/LIN  

När du använder Halvårspraxis kommer en avskrivning på sex månader att tillämpas det första räkenskapsåret, oavsett innehållet i fältet **Avskrivning startdatum**.  

> [!NOTE]  
> Den beräknade livslängd för en anläggningstillgång som återstår efter det första räkenskapsåret kommer alltid att innehålla ett halvår med hjälp av metoden Halvårspraxis. För att metoden Halvårspraxis ska användas på rätt sätt måste fältet **Avskrivning slutdatum** på sidan **Avskrivningsregel för anl.tillg.** alltid innehålla ett datum som infaller exakt sex månader före slutdatumet för det räkenskapsår då anläggningstillgången helt har avskrivits.  

### <a name="example---half-year-convention-depreciation"></a>Exempel: Avskrivning med metoden Halvårspraxis

Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. **Avskrivningens startdatum** är 20-03-01. Den beräknade livslängden är fem år så **avskrivningens slutdatum** blir 25-06-30. Batch-jobbet **Beräkna avskrivning** körs en gång om året. Detta exempel bygger på att räkenskapsåret sammanfaller med kalenderåret.  

Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-03-01 |Anskaffningskostnad |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-12-31 |Avskrivning |270 |-10 000,00 |90,000.00 |
| 21-12-31 |Avskrivning |360 |-20 000,00 |70,000.00 |
| 22-12-31 |Avskrivning |360 |-20 000,00 |50,000.00 |
| 23-12-31 |Avskrivning |360 |-20 000,00 |30,000.00 |
| 24-12-31 |Avskrivning |360 |-20 000,00 |10,000.00 |
| 25-12-31 |Avskrivning |180 |-10 000,00 |0.00 |

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Exempel: DEG1/LIN-avskrivning med metoden Halvårspraxis

Anskaffningskostnaden för en anläggningstillgång är 100 000 BVA. **Avskrivningens startdatum** är 20-11-01. Den beräknade livslängden är fem år, varför **Slutdatum för avskrivning** blir 25-06-30. På sidan **Anl. avskrivningsregler** är värdet 40 i fältet **Degressiv %**. Batch-jobbet **Beräkna avskrivning** körs en gång om året. Detta exempel bygger på att räkenskapsåret sammanfaller med kalenderåret.  

Så här ser anläggningstillgångstransaktionerna ut:  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 11-01-20 |Anskaffningskostnad |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-12-31 |Avskrivning |60 |-20 000,00 |80,000.00 |
| 21-12-31 |Avskrivning |360 |-32 000,00 |48,000.00 |
| 22-12-31 |Avskrivning |360 |-19 200,00 |28,800.00 |
| 23-12-31 |Avskrivning |360 |-11 520,00 |17,280.00 |
| 24-12-31 |Avskrivning |360 |-11 520,00 |5 760,00 LIN |
| 25-12-31 |Avskrivning |180 |-5 760,00 |0,00 LIN |

`SL` efter bokföringsvärdet betyder att den linjära metoden har använts.  

Beräkningsmetod:  

* År 1:  

    *Degressivt belopp = Helårsbelopp = 40 % av 100 000 = 40 000.* Därför, för ett halvår: 40 000 / 2 = 20 000  

    *Linjärt belopp = Helårsbelopp = 100 000/5 = 20 000.* Därför, för ett halvår: 20 000 / 2 = 10 000  

    Det degressiva beloppet används eftersom det är det större beloppet.  

* År 5 (2024):  

    *Degressivt belopp = 40 % av 17 280,00 = 6 912,00*  

    *Linjärt belopp = 28 800 / 1,5 = 11 520,00*  

    Det linjära beloppet används eftersom det är det större beloppet.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Kopiera transaktioner till fler avskrivningsregler

Om du har tre avskrivningsregler, B1, B2 och B3, och vill kopiera transaktioner från B1 till B2 och B3 kan du markera fältet **Ingår i dubblettlista** på avskrivningsregelkorten för B2 och B3. Detta är praktiskt om avskrivningsregel B1 är integrerad med redovisningen samt använder redovisningsjournalen för anläggningstillgångar och om avskrivningsreglerna B2 och B3 inte är integrerade med redovisningen och använder journalen för anläggningstillgångar.  

När du registrerar en transaktion i B1 i redovisningsjournalen för anläggningstillgångar och markerar fältet **Använd dubblettlista** kopieras transaktionen till regel B2 och B3 i journalen för anläggningstillgångar när transaktionen har bokförts.  

> [!NOTE]  
> Du kan inte kopiera till samma journal som du kopierar från. Om du bokför transaktioner i redovisningsjournalen för anläggningstillgångar kan du kopiera dem till journalen för anläggningstillgångar eller till redovisningsjournalen för anläggningstillgångar med hjälp av en annan journal.  

> [!NOTE]  
> Det är inte möjligt att använda samma nummerserie i Anl. redovisningsjournal och Anl.journal. När du bokför transaktioner i redovisningsjournalen för anläggningstillgångar måste du lämna fältet **Dokumentnr** tomt. Om du anger ett nummer i fältet dupliceras det numret i anläggningstillgångsjournalen. Du måste ändra verifikationsnummer manuellt innan du kan bokföra raderna.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/configure-depreciation-books/)

## <a name="see-also"></a>Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
