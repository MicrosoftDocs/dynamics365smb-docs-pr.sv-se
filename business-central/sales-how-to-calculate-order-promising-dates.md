---
title: Så här beräknar du ett orderlöftesdatum | Microsoft Docs
description: Orderlöftesfunktionen är ett verktyg för att beräkna det första möjliga datum då en artikel är disponibel för leverans. Funktionen skapar också inköpsrader för de datum som du accepterar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 150c5c552e314d17af15968ebcbe57d8e8bc3fc1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758123"
---
# <a name="calculate-order-promising-dates"></a>Beräkna orderlöftesdatum
Ett företag måste kunna informera sina kunder om orderleveransdatum. Sidan **Orderlöftesrader** ger dig möjlighet att göra detta från en försäljningsorderrad.  

Baserat på en artikels kända och förväntade dispositionsdatum beräknas utleverans- och leveransdatum omedelbart i [!INCLUDE[prod_short](includes/prod_short.md)]. Datum kan sedan utlovas till kund.  

Om du anger ett begärt leveransdatum på försäljningsorderraden används detta datum som utgångspunkt för följande beräkningar.  

- begärt leveransdatum – leveranstid = planerat utleveransdatum  
- planerat utleveransdatum – utgående lagerhanteringstid = utleveransdatum  

Om artiklarna kan plockas på utleveransdatumet kan försäljningsprocessen fortsätta. Om artiklarna inte kan plockas på utleveransdatumet visas en varning om att varan inte finns i lager.  

Om du inte har angett ett begärt leveransdatum på försäljningsorderraden, eller om det begärda leveransdatumet inte kan godtas, beräknas det tidigaste datum då artiklarna är tillgängliga. Detta datum anges automatiskt i fältet **Leveransdatum** på raden. Det datum då du planerar att utleverera artiklarna liksom det datum då varorna kan levereras till kunden beräknas med hjälp av följande beräkningar.  

- planerat utleveransdatum + utgående lagerhanteringstid = planerat utleveransdatum  
- planerat utleveransdatum +- leveranstid = planerat leveransdatum  

## <a name="about-order-promising"></a>Om Orderlöfte
Med funktionen Orderlöfte kan du lova att en order ska levereras på ett visst datum. Det datum då en artikel är disponibel eller kapabel att lova beräknas och orderrader skapas för de datum som du accepterar. Funktionen är ett verktyg för att beräkna det första möjliga datum då en artikel är disponibel för leverans. Funktionen skapar också inköpsrader, om artiklar måste först vara inköp för de datum som du accepterar.

[!INCLUDE[prod_short](includes/prod_short.md)] använder två grundläggande begrepp:  

- Disponibelt att lova (ATP)  
- Kapabel att lova (CTP)  

### <a name="available-to-promise"></a>Disponibelt att lova  
Disponibelt att lova (ATP) beräknar datum baserat på reservationssystemet. Det utför en tillgänglighetskontroll av det icke reserverade antalet i lager med hänsyn till planerad produktion, inköp, överföringar och returer. Baserat på de här uppgifterna beräknas automatiskt kundbeställningens leveransdatum i [!INCLUDE[prod_short](includes/prod_short.md)] eftersom artiklarna är disponibla, antingen i lagret eller i planerade inleveranser.  

### <a name="capable-to-promise"></a>Kapabel att lova  
Kapabel att lova (CTP) utgår från ett ”vad händer om”-scenario som endast gäller artikelantal som inte finns i lager eller i planerade ordrar. Med hjälp av det här scenariot beräknas i [!INCLUDE[prod_short](includes/prod_short.md)] det tidigaste datum då artikeln kan vara tillgänglig, om det ska produceras, köpas in eller överföras.

#### <a name="example"></a>Exempel
Om det finns en order för 10 enheter och 6 enheter finns i lager eller i planerade ordrar, så kommer Kapabel att lova-beräkningen att ske utifrån 4 delar.

### <a name="calculations"></a>Beräkningar  
När kundens leveransdatum beräknas i [!INCLUDE[prod_short](includes/prod_short.md)] utförs två uppgifter:  

- Beräkning av tidigast möjliga leveransdatum när kunden inte har begärt ett visst leveransdatum.  
- Kontroll om det leveransdatum som kunden har begärt, eller som har utlovats till kunden, är realistiskt.  

Om kunden inte begär ett visst leveransdatum anges leveransdatum till arbetsdatum, och tillgänglighet baseras sedan på det datumet. Om artikeln finns i lager beräknar [!INCLUDE[prod_short](includes/prod_short.md)] framåt i tiden för att kunna bestämma när ordern kan levereras. Det utförs med hjälp av följande formler:  

- Utleveransdatum + Tid för utgående lagerhantering = Planerat utleveransdatum  
- Planerat utleveransdatum + Leveranstid = Planerat leveransdatum  

[!INCLUDE[prod_short](includes/prod_short.md)] verifierar sedan om beräknat leveransdatum är realistiskt. Det beräknar bakåt i tiden så att det blir möjligt att fastställa när artikeln måste vara tillgänglig på det utlovade datumet. Det utförs med hjälp av följande formler:  

- Planerat leveransdatum – Leveranstid = Planerat utleveransdatum  
- Planerat utleveransdatum – Tid för utgående lagerhantering = Utleveransdatum  

Utleveransdatum används för att göra tillgänglighetskontrollen. Om artikeln är tillgänglig på detta datum bekräftar [!INCLUDE[prod_short](includes/prod_short.md)] bekräftar att den begärda/utlovade leveransen kan ske. Det görs genom att ange det planerade leveransdatum på samma dag som det begärda/utlovade leveransdatum. Om artikeln är inaktiverad returneras ett tomt datum och orderhandläggaren kan då använda CTP-funktionen.  

Baserat på nya datum och tider beräknas alla relaterade datum enligt de formler som definierats tidigare i det här avsnittet. CTP-beräkningen tar längre tid, men den ger det exakta datumet för när kunden kan vänta sig leverans av artikeln. De datum som beräknas från CTP presenteras i **planerat leveransdatum** och **tidigaste leveransdatum** på sidan **Orderlöftesrader**.  

Orderhandläggaren slutför CTP-processen genom att acceptera datum. Det innebär att en planeringsrad och en reservationstransaktion har skapats för artikeln före beräknade datum så att ordern kan uppfyllas.  

Förutom ett externt orderlöfte som du kan utföra på sidan **Orderlöftesrader** kan du också utlova interna eller externa leveransdatum för strukturartiklar. Mer information finns i [Visa tillgängliga objekt](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Så här skapar du orderlöfte  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Orderlöfteinställning** och välj sedan relaterad länk.  
2. Ange ett nummer och en tidsenhetskod i fältet **Offset (tid)**. Välj en av följande koder.  

    |Kod|Beskrivning|  
    |----------|-----------------|  
    |**d**|Kalenderdag|  
    |**a**|Vecka|  
    |**m**|Månad|  
    |**q**|Kvartal|  
    |**y**|År|  

    "3v" anger till exempel att offset-tiden är tre veckor. Använd "c" som ett prefix för alla de här koderna när du ska ange aktuell period. Om du t.ex. vill att offset-tiden ska vara den aktuella månaden skriver du **cm**.  
3. Ange en nummerserie i fältet **Orderlöfte nr-serie** genom att markera en rad från listan på sidan **Nr-serier**.  
4. Ange en orderlöftesmall i fältet **Orderlöftesmall** genom att välja en rad från listan på sidan **Inköpskalkylarksmallista**.  
5. Ange ett inköpskalkylark i fältet **Orderlöfteskalkylark** genom att markera en rad från listan på sidan **Inköpskalkylarksnamn**.

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Så här anger du inkommande lagerhanteringstid på sidan för lagerinställningarna  
Om du vill ange en inkommande lagerhanteringstid som ska tas med i orderlöftesberäkningen på inköpsraden, kan du ange tiden som standard för lagret och för lagerstället.    
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerinställningar** och välj sedan relaterad länk.  
2. I fältet **inkommande lagerhanteringstid** på snabbfliken **Allmänt** anger du det antal dagar som ska tas med i orderlöftesberäkningen.  

> [!NOTE]  
>  Om du har fyllt i fältet **inkommande lagerhanteringstid** på **lagerställekortet** för lagerstället, används värdet i detta fält som standard för inkommande lagerhanteringstid.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Så här anger du inkommande lagerhanteringstid på lagerställekort  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Plats** och välj sedan relaterad länk.  
2.  Öppna önskat lagerställekort.  
3.  I fältet **inkommande lagerhanteringstid** på snabbfliken **Lager** anger du det antal dagar som ska tas med i orderlöftesberäkningen.  

> [!NOTE]  
>  Om du lämnar fältet **inkommande Lagerhanteringstid. Lagerhanteringstid** tomt använder beräkningen värdet på sidan **Lagerinställningar**.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Så här anger du utgående lagerhanteringstid på sidan för lagerinställningarna  
Om du vill ange en utgående lagerhanteringstid som ska tas med i orderlöftesberäkningen på försäljningsraden, kan du ange tiden som standard för lagret.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerinställningar** och välj sedan relaterad länk.  
2. I fältet **utgående lagerhanteringstid** på snabbfliken **Allmänt** anger du det antal dagar som ska tas med i orderlöftesberäkningen.  

> [!NOTE]  
>  Om du har fyllt i fältet **utgående lagerhanteringstid** på lagerställekortet för lagerstället, används värdet i detta fält som standard för utgående lagerhanteringstid.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Så här anger du utgående lagerhanteringstid på lagerställekort  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan relaterad länk.  
2.  Öppna önskat lagerställekort.  
3.  I fältet **utgående lagerhanteringstid** på snabbfliken **Lager** anger du det antal dagar som ska tas med i orderlöftesberäkningen.  

> [!NOTE]  
>  Om du lämnar fältet **utgående lagerhanteringstid** tomt använder beräkningen värdet på sidan **Lagerinställningar**.

## <a name="to-make-an-item-critical"></a>Så här gör du en artikel kritisk  
Innan ett objekt kan tas med i orderlöftesberäkningen, måste den markeras som kritisk. Den här inställningen ser till att icke-kritiska objekt inte orsakar orderlöftesberäkningar.   
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Öppna relevant artikelkort.  
3.  Välj **Kritiskt** på snabbfliken **Planering**.  

## <a name="to-calculate-an-order-promising-date"></a>Så här beräknar du ett orderlöftesdatum  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Öppna relevant försäljningsorder och markera de försäljningsorderrader som ska beräknas.  
3.  Välj åtgärden **Orderlöfte** och klicka på åtgärden **Orderlöftesrader**.  
4.  Välj en ny rad och välj sedan ett av följande alternativ.  

    - Markera **Disponibelt att lova** om du vill beräkna det tidigaste datum då artikeln är disponibel avseende lager, planenlig inleverans och bruttobehov.  
    - Markera **Kapabel att lova** om du vet att artikeln för närvarande är slut på lagret och vill beräkna det tidigaste datum då artikeln kan vara disponibel genom att skicka ut nya påfyllningsrekvisitioner.  
5.  Välj **Acceptera** om du accepterar det tidigaste leveransdatum som är tillgängligt.  

## <a name="see-also"></a>Se även  
[Försäljning](sales-manage-sales.md)  
[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]