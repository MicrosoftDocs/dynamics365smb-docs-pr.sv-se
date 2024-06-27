---
title: Beräkna orderlöftesdatum
description: Orderlöftesfunktionen är ett verktyg för att beräkna det första möjliga datum då en artikel är disponibel för leverans.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Beräkna orderlöftesdatum

Ett företag måste kunna informera sina kunder om orderleveransdatum. Sidan **Orderlöftesrader** ger dig möjlighet att göra detta från en försäljningsorder.  

[!INCLUDE[prod_short](includes/prod_short.md)] beräknar leverans- och leveransdatum baserat på en varas kända och förväntade tillgänglighetsdatum, som du kan lova kunderna.  

Om du anger ett begärt leveransdatum på försäljningsorderraden används detta datum som utgångspunkt för följande beräkningar.  

- begärt leveransdatum – leveranstid = planerat utleveransdatum  
- planerat utleveransdatum – utgående lagerhanteringstid = utleveransdatum  

Om artiklarna kan plockas på utleveransdatumet kan försäljningsprocessen fortsätta. Om artiklarna inte kan plockas på utleveransdatumet visas en varning om att varan inte finns i lager.  

Om du inte har angett ett begärt leveransdatum på försäljningsorderraden, eller om det begärda leveransdatumet inte kan godtas, beräknas det tidigaste datum då artiklarna är tillgängliga. Detta datum anges automatiskt i fältet **Leveransdatum** på raden. Det datum då du planerar att utleverera artiklarna liksom det datum då varorna kan levereras till kunden beräknas med hjälp av följande beräkningar.  

- planerat utleveransdatum + utgående lagerhanteringstid = planerat utleveransdatum  
- planerat utleveransdatum +- leveranstid = planerat leveransdatum  

## Om orderlöfte

Med funktionen Orderlöfte kan du lova att en order ska levereras på ett visst datum. Det datum då en artikel är disponibel eller kapabel att lova beräknas och orderrader skapas för de datum som du accepterar. Funktionen är ett verktyg för att beräkna det första möjliga datum då en artikel är disponibel för leverans. Funktionen skapar också inköpsrader, om artiklar måste först vara inköpta eller producerade för de datum som du accepterar.

[!INCLUDE[prod_short](includes/prod_short.md)] använder två grundläggande begrepp:  

- Disponibelt att lova (ATP)  
- Kapabel att lova (CTP)  

### Disponibelt att lova

Disponibelt att lova (ATP) beräknar datum baserat på reservationssystemet. Det utför en tillgänglighetskontroll av det icke reserverade antalet i lager om planerad produktion, inköp, överföringar och returer. Baserat på de här uppgifterna beräknas kundbeställningens leveransdatum i [!INCLUDE[prod_short](includes/prod_short.md)] eftersom artiklarna är disponibla, antingen i lagret eller i planerade inleveranser.  

### Kapabel att lova

Kapabel att lova (CTP) utgår från ett ”vad händer om”-scenario som endast gäller artikelantal som inte finns i lager eller i planerade ordrar. Med hjälp av det här scenariot beräknas i [!INCLUDE[prod_short](includes/prod_short.md)] det tidigaste datum då artikeln kan vara tillgänglig, om det ska produceras, köpas in eller överföras.

#### Exempel

Om det finns en order för 10 enheter och 6 enheter finns i lager eller i planerade ordrar, så kommer Kapabel att lova-beräkningen att ske utifrån 4 delar.

### Beräkningar

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

## Så här skapar du orderlöfte

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Orderlöfteinställning** och välj sedan relaterad länk.  
2. Ange ett nummer och en tidsenhetskod i fältet **Offset (tid)**. Välj en av följande koder.  

    |Kod|Beskrivning|  
    |----------|-----------------|  
    |**d**|Kalenderdag|  
    |**a**|Vecka|  
    |**m**|Månad|  
    |**q**|Kvartal|  
    |**y**|År|  

    "3v" anger till exempel att offset-tiden är tre veckor. Använd "c" som ett prefix för alla de här koderna när du ska ange aktuell period. Om du t. ex. vill att offset-tiden ska vara den aktuella månaden skriver du **cm**.  
3. Ange en nummerserie i fältet **Orderlöfte nr-serie** genom att markera en rad från listan på sidan **Nr-serier**.  
4. Ange en orderlöftesmall i fältet **Orderlöftesmall** genom att välja en rad från listan på sidan **Inköpskalkylarksmallista**.  
5. Ange ett inköpskalkylark i fältet **Orderlöfteskalkylark** genom att markera en rad från listan på sidan **Inköpskalkylarksnamn**.

### Ankommande och avgående lagerhanteringstider i order löftet

Om du vill inkludera lagerhanteringstid i beräkningen för beställning som lovar på inköpsraden, på sida **Lagerinställningar** kan du ange en standardhanteringstid att använda på försäljnings- och inköpsdokument. Du kan också ange särskilda tider för var och en av dina lager ställen på sidan **lagerställekort**. 

#### Så här anger du standard- och avgående lagerhanteringstid för försäljnings- och inköpsdokument

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerinställning** och väljer sedan relaterad länk.  
2. På snabbfliken **Allmänt** i fältet **inkommande lagerhanteringstid** och **utgående lagerhanteringstid**, ange det antal dagar som du vill inkludera i beräkningen med löfte om beställning.  

#### Att ange inkommande och utgående lagerhanteringstider på platser

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Plats** och väljer sedan relaterad länk.  
2.  Öppna önskat lagerställekort.  
3.  På snabbfliken **Distributionslager** i fältet **inkommande lagerhanteringstid** och **utgående lagerhanteringstid**, ange det antal dagar som du vill inkludera i beräkningen med löfte om beställning.  

> [!NOTE]  
>  När du skapar en inköps order, väljer du **Plats** i fältet **Leverans** på snabbfliken **Leverans och betalning** och välj sedan en plats i fältet **Platskod** kommer fälten **utgående lagerhanteringstid** och **inkommande Lagerhanteringstid** att använda den hanteringstid som har angetts för lagerstället. För försäljningsorder är samma sant om du väljer en plats i fältet **platskod**. Om ingen hanterings tid har angetts för platsen är fälten **utgående lagerhanteringstid** och **inkommande lagerhanteringstid** tomma. Om du lämnar fältet **Platskod** tomt på försäljnings- och inköpshandlingar använder beräkningen den hanteringstid som anges på sidan **Lagerinställningar**.

## Så här gör du en artikel kritisk

Innan ett objekt kan tas med i orderlöftesberäkningen, måste den markeras som kritisk. Den här inställningen ser till att icke-kritiska objekt inte orsakar orderlöftesberäkningar.   
1.  Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2.  Öppna relevant artikelkort.  
3.  Välj **Kritiskt** på snabbfliken **Planering**.  

## Så här beräknar du ett orderlöftesdatum

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2.  Öppna relevant försäljningsorder och markera de försäljningsorderrader som ska beräknas.  
3.  Välj åtgärden **Orderlöfte** och klicka på åtgärden **Orderlöftesrader**.  
4.  Välj en ny rad och välj sedan ett av följande alternativ.  

    - Markera **Disponibelt att lova** om du vill beräkna det tidigaste datum då artikeln är disponibel avseende lager, planenlig inleverans och bruttobehov.  
    - Markera **Kapabel att lova** om du vet att artikeln för närvarande är slut på lagret och vill beräkna det tidigaste datum då artikeln kan vara disponibel genom att skicka ut nya påfyllningsrekvisitioner.  
5.  Välj **Acceptera** om du accepterar det tidigaste leveransdatum som är tillgängligt.  

## Se även

[Försäljning](sales-manage-sales.md)  
[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
