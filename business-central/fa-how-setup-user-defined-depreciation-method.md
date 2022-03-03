---
title: Ställ in anl. användardefinierad avskrivningsmetod
description: I Business Central kan du använda en användardefinierad avskrivningsmetod för att definiera tillgångens avskrivningsmetod på sidan Anläggningstillgångskort.
author: jill-kotel-andersson
ms.reviewer: edupont
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: edupont
ms.openlocfilehash: 517c3cdb51762c3c0fadcf29ff1ad6dbf949f971
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144989"
---
# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Skapa anläggningstillgångar med användardefinierade avskrivningsmetoder

Du kan använda [!INCLUDE[prod_short](includes/prod_short.md)] för att skapa användardefinierade avskrivningsmetoder som beskrivs här.

Med en användardefinierad metod använder du sidan **Avskrivningstabeller** där du måste ange en avskrivningsprocent för varje period (månad, kvartal, år eller bokföringsperiod). När du sedan tilldelar en avskrivningsregel med en användardefinierad metod till en anläggningstillgång måste du ange fälten **Första användardefinierade avskrivningsdatum** och **Startdatum för avskrivning** på sidan **Avskrivningsregler för anläggningstillgångar** för den specifika anläggningstillgången.  

Beräkningsformeln för avskrivningsbelopp är:  

*Avskrivningsbelopp = (Avskrivning % × Antal avskr.dagar × Avskrivningsbas) / (100 × 360)*


> [!NOTE]  
> Medan datumet i fältet **Startdatum använd.def. avskrv.** används för att bestämma tidsintervall, det är **Avskrivningens startdatum** som används för att bestämma antalet avskrivningsdagar. Om fältet **startdatum använd.def avskrv. Datum**, är tidigare än **avskrivningens startdatum**, används procenten för den första perioden i avskrivningstabellen bara delvis när programmet beräknar den första avskrivningen. Det innebär att tillgången inte helt kommer att avskrivas i slutet av den sista perioden.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>Så här tilldelar du en avskrivningsregel till en anläggningstillgång med en användardefinierad avskrivningsmetod

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj anläggningstillgången som du vill skapa avskrivningsregeln för anläggningstillgångar för.
3. Välj åtgärden **Relaterad** och välj sedan **Anläggningstillgång** och sedan **Avskrivningsregler**. Då öppnas sidan **Anl. avskrivningsregler**.

   Som standard är en del av de fält som måste fyllas i enligt instruktionerna nedan dolda, så du måste visa dem. För att göra detta måste du anpassa sidan. Mer information finns i [Så här börjar du anpassa en sida genom den anpassningsbanderollen](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. I fältet **Avskrivningsmetod**, välj **Användardefinierad**.
5. I fältet **Avskrivningstabellkod**, välj den **Avskrivningstabell** du vill använda.
6. I fältet **Avskrivningens startdatum**, välj startdatum för avskrivningsberäkningen.
7. När du använder en användardefinierad metod anges fältet **Startdatum använd.def. avskrv.** måste anges till ett datum som är samma eller tidigare är samma eller tidigare än fältet **Avskrivningens startdatum**. Om du har valt alternativet **Periodlängd** i fältet Komprimeringsgrad i avskrivningstabellen måste datumet i fältet **Startdatum använd.def. avskrv.** vara bokföringsperiodens startdatum.
8. Fyll antingen i fältet **Antal avskrivningsår** eller **Slutdatum för avskrivning**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a>Så här skapar du användardefinierade avskrivningsmetoder

På sidan **Avskrivning tabellkort** kan du skapa användardefinierad avskrivningsmetod. Du kan till exempel lägga upp avskrivning baserad på antalet enheter.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **avskrivningstabeller** och väljer sedan relaterad länk.  
2. På sidan **Avskrivning tabellista** väljer du åtgärden **Ny**.  
3. På sidan **Avskrivningstabellkort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Använd funktionen **Skapa siffersummeringstabell** för att definiera en avskrivningstabell baserad på metoden *Siffersumma*.

Om en anläggningstillgång skrivs av över 4 år kommer, med metoden *Siffersumma*, avskrivningen per år att beräknas på följande sätt:

Siffersumma = 1 + 2 + 3 + 4 = 10 Avskrivning:

* År 1 = 4/10  
* År 2 = 3/10  
* År 3 = 2/10  
* År 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a>Avskrivning baserad på antal enheter

Den här användardefinierade metoden kan även användas för avskrivning baserad på enheter, till exempel när det gäller produktionsmaskiner med en fastställd livslängdskapacitet. På sidan **Avskrivningstabeller** kan du ange det antal enheter som kan produceras under varje period (månad, kvartal, år eller bokföringsperiod).  

### <a name="example---user-defined-depreciation"></a>Exempel – Användardefinierad avskrivning

Du kan använda en avskrivningsmetod som gör det möjligt att av skatteskäl skriva av tillgångar snabbare.  

Du ska av skatteskäl använda följande avskrivningsgrad för en anläggningstillgång med en livslängd på tre år:  

* År 1: 25 %  
* År 2: 38 %  
* År 3: 37 %  

Anskaffningskostnaden är 100 000 BVA och livslängden är fem år. Avskrivningen beräknas en gång om året.  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-01-01 |Anskaffningskostnad |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-12-31 |Avskrivning |360 |-25 000,00 |75,000.00 |
| 21-12-31 |Avskrivning |360 |-38 000,00 |37,000.00 |
| 22-12-31 |Avskrivning |360 |-37 000,00 |0 |
| 23-12-31 |Avskrivning |Ingen |Ingen |0 |
| 24-12-31 |Avskrivning |Ingen |Ingen |0 |

I föregående exempel skulle både fältet **Första användardefinierade avskrivningsdatum** och fältet **Startdatum för avskrivning** ställas in på 20/01/01 på sidan **Avskrivningsregler för anläggningstillgångar** för den specifika anläggningstillgången. Om däremot **Startdatum använd.def. avskrv.** innehåller 20-01-01 och **Avskrivning startdatum** innehåller 20-01-04 blir resultatet:  

| Datum | Anl.bokföringstyp | Dagar | Belopp | Bokföringsvärde |
| --- | --- | --- | --- | --- |
| 20-01-01 |Anskaffningskostnad |(startdatum för avskrivning) |100,000.00 |100,000.00 |
| 20-12-31 |Avskrivning |270 |-18 750,00 |81,250.00 |
| 21-12-31 |Avskrivning |360 |-38 000,00 |42,250.00 |
| 22-12-31 |Avskrivning |360 |-37 000,00 |6,250.00 |
| 23-12-31 |Avskrivning |90 |-6 250,00 |0 |
| 24-12-31 |Avskrivning |Ingen |Ingen |0 |


## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Skapa avskrivning för anläggningstillgång](fa-how-setup-depreciation.md)  
[Avskrivningsmetoder för anläggningstillgångar](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
