---
title: Skapa allmän information om anläggningstillgångar
description: 'Innan du kan använda anläggningstillgångar måste du skapa standardredovisningskonton, bokföringsmallar, allokeringsnycklar, journalmallar och batcher och klasskoder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-general-fixed-assets-information"></a>Konfigurera allmän information om anläggningstillgångar

Innan du kan hantera anläggningstillgångar måste du skapa standardredovisningskonton, allokeringsnycklar och journalmallar och batcher för att bokföra och gruppera om anläggningstillgångar. Definiera också en klassificeringshierarki (indelningar och underindelningar) för att strukturera dina tillgångar och definiera vid behov de platser där du lagrar tillgångar.

## <a name="to-set-up-general-behavior-for-fixed-assets-functionality"></a>För att ställa in allmänna beteenden för anläggningstillgångarnas funktion

Definiera det allmänna beteendet för funktionen för anläggningstillgångarna och dess verifikationsnummerserie på sidan **Inställningar för anläggningstillgångar**.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för anläggningstillgångar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Så här skapar du bokföringsmallar för anläggningstillgångar

använda bokföringsmallar för att definiera anläggningstillgångsgrupper. Transaktionerna för de här bokföringsmallarna bokförs på samma redovisningskonton.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anl.bokföringsmallar** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. På sidan **Anl.bokföringsmallkort** fyller du i fälten efter behov.

    > [!NOTE]  
    >   För att se till att motkonton för olika anläggningstillgångar infogas bokföringar automatiskt när du väljer åtgärden **Infoga anl. motkonto** på journalrader, följer nästa steget som baseras på bokföring av uppskrivning.
4. På snabbfliken **Motkonto** i fältet **Uppskrivning motkonto** anger du vilket redovisningskonto som du vill bokföra mottransaktioner för uppskrivning.

Mer information om hur du använder åtgärden **Infoga anl. motkonto** på journalrader för redovisningskonto för anläggningstillgångar, se [Omvärdera anläggningstillgångar](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-journal-templates"></a>Så här skapar du journalmallar för anläggningstillgångar

En mall är en fördefinierad layout för en journal. Mallen innehåller information om spårkoder, rapporter och nummerserier. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] skapar automatiskt en journalmall för anläggningstillgångar första gången du öppnar sidan **Journalmall för anläggningstillgångar** men du kan skapa ytterligare journalmallar.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anl. journalmallar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="to-set-up-fixed-asset-class-and-subclass-codes"></a>Så här skapar du indelnings- och underindelningskoder för anläggningstillgångar

I anläggningstillgångar kan du definiera en klassificeringshierarki som kan användas för att gruppera tillgångar. Hierarkin har två nivåer: indelningar och underindelningar.

### <a name="fixed-asset-class-codes"></a>Indelningskoder för anläggningstillgångar

Indelningar för anläggningstillgångar är posterna på den översta nivån i den klassificeringshierarki som du grupperar tillgångar i. Använd till exempel indelningar för att dela upp tillgångar i materiella eller immateriella tillgångar. Du måste skapa minst en indelningsklass för anläggningstillgångar i inställningarna.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl. indelningar** och väljer sedan relaterad länk.
2. Ange koder och namn för anläggningstillgångens indelningar som du vill skapa.

### <a name="fixed-asset-subclass-codes"></a>Underindelningskoder för anläggningstillgångar

Underindelningar för anläggningstillgångar är posterna på den andra nivån i den klassificeringshierarki som du grupperar tillgångar i. Varje underindelning pekar på en toppnivåindelning. Använd underindelningskoder för att gruppera anläggningstillgångar i mer specifika kategorier, som exempelvis byggnader, fordon, möbler och maskiner. Du måste skapa minst en underindelningsklass för anläggningstillgångar i inställningarna.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl. underindelningar** och väljer sedan relaterad länk.
2. Ange koder och namn för anläggningstillgångens underindelningar som du vill skapa.

## <a name="start-to-register-assets"></a>Börja registrera tillgångar

Om det är första gången som du använder anläggningstillgångarna i [!INCLUDE[prod_short](includes/prod_short.md)] måste du först ange inställningar för redovisningsmodulen. Hur du genomför detta beror på om anläggningstillgångar är integrerad med redovisningen.  

Du använder följande procedur om anläggningstillgångstransaktionerna ska bokföras i redovisningen.  

1. Slutför de grundläggande inställningarna för anläggningstillgångar.  
2. Ställ in ett anläggningstillgångskort för de befintliga tillgångarna.  
3. Skapa en avskrivningsregel för anläggningstillgångar för respektive avskrivning (till exempel skatt och bokslut). För varje avskrivningsregel definierar du villkor, till exempel integrering med redovisningen.

    Aktivera redovisningintegrering, genom att följa stegen. Försäkra dig först om att redovisningsintegrering inte är aktiverad för alla avskrivningsregler. Bokför sedan ingående transaktioner och slå sedan på redovisningsintegreringen.  
4. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **avskrivningsregler** och väljer sedan relaterad länk.  
5. Välj relevant avskrivningsregel och välj sedan åtgärden **Redigera** för att öppna sidan **Avskrivningsregelkort**.
6. Stäng av alla växlar på snabbfliken **Integration**. Om du har fler än en avskrivningsregel upprepar du detta steg för var och en.  
7. Ange följande rader för respektive anläggningstillgång i anläggningsjournalen:
   * En rad med anskaffningskostnaden.
   * En rad med den ackumulerade avskrivningen till slutet på föregående räkenskapsår.
   * En rad med den ackumulerade avskrivningen från början av det innevarande räkenskapsåret till det datum då [!INCLUDE[prod_short](includes/prod_short.md)] anges för att starta beräkningen av avskrivningen.

    Om du har andra ingående saldon kan du även ange dessa nu, t. ex. nedskrivning, uppskrivning o.s.v.  
8. När du har angett och bokfört journalraderna för respektive anläggningstillgång aktiverar du redovisningsintegreringen i avskrivningsreglerna.

Om anläggningstillgångarna inte har integrerats med redovisningen hoppar du över steg sex och åtta.

## <a name="to-set-up-fixed-asset-location-codes-optional"></a>Så här skapar du lagerställekoder för anläggningstillgångar (valfritt)

Lagerställekoder för anläggningstillgångar definierar identifierare för var en anläggningstillgång är placerad, till exempel försäljningsavdelning, reception, administration, fabrik och lager. Du kan använda dem för att registrera en anläggningstillgångs lagerställe. Den här informationen är användbar för försäkrings- och lagerändamål.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl. placeringar** och väljer sedan relaterad länk.
2. Ange koder och namn för anläggningstillgångens lagerställe som du vill skapa.

## <a name="to-set-up-fixed-asset-allocation-keys-optional"></a>Så här ställer du in fördelningsnycklar för anläggningstillgångar (valfritt)

Använd fördelningsnycklar för att allokera transaktioner till olika avdelningar eller projekt. Du kan till exempel skapa en fördelningsnyckel om du vill fördela avskrivningskostnader för bilar med 35 % på administrationsavdelningen och 65 % på försäljningsavdelningen. Mer information finns i [Fördela kostnader och intäkter](year-allocate-costs-income.md).

Fördelningsnycklar används för fördelningar av anläggningstillgångar, inte för individuella tillgångar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl.bokföringsmallar** och väljer sedan relaterad länk.  
2. På sidan **Anl.bokföringsmallar** väljer du åtgärden **Fördelningar** och sedan en bokföringstyp.
3. På sidan **Anl. fördelningar** fyller du i fälten efter behov.
4. Upprepa steg 2 och 3 för varje bokföringstyp som du vill ange fördelningsnycklar för.

## <a name="to-set-up-fixed-asset-journal-batches-optional"></a>Så här skapar du journaler för anläggningstillgångar (valfritt)

Du kan skapa flera journaler, d.v.s. enskilda journaler för varje journalmall. Personalen kan till exempel ha egna journaler som har den anställdes initialer som journalnamn. Mer information finns i [Arbeta medSkapa redovisningsjournaler](ui-work-general-journals.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl. journalmallar** och väljer sedan relaterad länk.  
2. Välj relevant försäkringsjournalmall och välj sedan åtgärden **Journaler**.
3. På sidan **Anl.journaler** fyller du i fälten efter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates-optional"></a>Så här ställer du in grupperingsmallar för anläggningstillgångar (valfritt)

Använd dedikerade grupperingsjournalen när du vill överföra, dela upp och slå ihop anläggningstillgångar. [!INCLUDE[prod_short](includes/prod_short.md)] skapar automatiskt en grupperingsjournalmall för anläggningstillgångar första gången som du öppnar sidan **Anl. grupperingsjournal** men du kan skapa ytterligare grupperingsjournalmallar för anläggningstillgångar. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl. grupperingsjournalmallar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches-optional"></a>Så här skapar du grupperingsjournaler för anläggningstillgångar (valfritt)

Du kan skapa flera journaler, d.v.s. enskilda journaler för varje grupperingsjournalmall. Personalen kan till exempel ha egna grupperingsjournaler som använder den anställdes inititaler som journalnamn. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl. grupperingsjournalmallar** och väljer sedan relaterad länk.  
2. Välj relevant försäkringsjournalmall och välj sedan åtgärden **Journaler**.
3. På sidan **Anl. grupper.journaler** fyller du i fälten efter behov.

## <a name="see-also"></a>Se även

[Ställa in anläggningstillgångar](fa-setup.md)  
[Översikt över anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
