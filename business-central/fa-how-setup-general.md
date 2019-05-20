---
title: Skapa redovisningen för anläggningstillgångar | Microsoft Docs
description: Innan du kan använda anläggningstillgångar måste du skapa standardredovisningskonton, bokföringsmallar, allokeringsnycklar, journalmallar och batcher och klasskoder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 240e3e8dc151c971dcf5875bb3e7e8bb3d5edd45
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244659"
---
# <a name="set-up-general-fixed-assets-information"></a>Skapa allmän information om anläggningstillgångar
Innan du kan hantera anläggningstillgångar, måste du skapa standardinställningredovisningskonton, fördelningsnycklar, journalmallar och journaler för bokföring och gruppering av anläggningstillgångar i klasser, som till exempel Materiella och Immateriella.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Så här anger du generella standardvärden för anläggningstillgångar
Du definierar det allmänna beteendet eller funktionen för anläggningstillgångarna och ställer in verifikationsnummerserie på sidan **Inställningar för anläggningstillgångar**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställningar för anläggningstillgångar** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Så här skapar du bokföringsmallar för anläggningstillgångar
Du kan använda bokföringsmallar om du vill definiera anläggningstillgångsgrupper. Transaktionerna för de här bokföringsmallarna bokförs på samma redovisningskonton.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. bokföringsmallar** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. På sidan **Anl. bokföringsmallkort** fyller du i fälten efter behov.

    > [!NOTE]  
    >   För att se till att motkonton för olika anläggningstillgångar infogas bokföringar automatiskt när du väljer åtgärden **Infoga anl. motkonto** på journalrader, följer nästa steget som baseras på bokföring av uppskrivning.
4. På snabbfliken **Motkonto** i fältet **Uppskrivning motkonto** anger du vilket redovisningskonto som du vill bokföra mottransaktioner för uppskrivning.

Mer information om hur du använder åtgärden **Infoga anl. motkonto** på journalrader för redovisningskonto för anläggningstillgångar, se t.ex. [Omvärdera anläggningstillgångar](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Så här ställer du in fördelningsnycklar för anläggningstillgångar
Du kan fördela transaktioner på olika avdelningar eller projekt utifrån användardefinierade fördelningsnycklar. Du kan till exempel skapa en fördelningsnyckel om du vill fördela avskrivningskostnader för bilar med 35 % på administrationsavdelningen och 65 % på försäljningsavdelningen. Mer information finns i [Fördela kostnader och intäkter](year-allocate-costs-income.md).

Fördelningsnycklar används för fördelningar av anläggningstillgångar, inte för individuella tillgångar.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. bokföringsmallar** och välj sedan relaterad länk.  
2. På sidan **Anl. bokföringsmallar** väljer du åtgärden **Fördelningar** och sedan en bokföringstyp.
3. På sidan **Anl. fördelningar** fyller du i fälten efter behov.
4. Upprepa steg 2 och 3 för varje bokföringstyp som du vill ange fördelningsnycklar för.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Så här skapar du journalmallar för anläggningstillgångar
En mall är en fördefinierad layout för en journal. Mallen innehåller information om spårkoder, rapporter och nummerserier. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] skapar automatiskt en journalmall för anläggningstillgångar första gången du öppnar sidan **Journalmall för anläggningstillgångar** men du kan skapa ytterligare journalmallar.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. journalmallar** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Så här ställer du in journaler för anläggningstillgångar
Du kan skapa flera journaler, d.v.s. enskilda journaler för varje journalmall. Personalen kan till exempel ha egna journaler som har den anställdes initialer som journalnamn. Mer information finns i [Arbeta medSkapa redovisningsjournaler](ui-work-general-journals.md).  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. journalmallar** och välj sedan relaterad länk.  
2. Välj relevant försäkringsjournalmall och välj sedan åtgärden **Journaler**.
3. På sidan **Anl.journaler** fyller du i fälten efter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Så här ställer du in grupperingsmallar för anläggningstillgångar
Du kan använda dedikerade grupperingsjournalen när du vill överföra, dela upp och slå ihop anläggningstillgångar. [!INCLUDE[d365fin](includes/d365fin_md.md)] skapar automatiskt en grupperingsjournalmall för anläggningstillgångar första gången som du öppnar sidan **Anl. grupperingsjournal** men du kan skapa ytterligare grupperingsjournalmallar för anläggningstillgångar. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. grupperingsjournalmallar** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Så här skapar du grupperingsjournaler för anläggningstillgångar
Du kan skapa flera journaler, d.v.s. enskilda journaler för varje grupperingsjournalmall. Personalen kan till exempel ha egna grupperingsjournaler som använder den anställdes inititaler som journalnamn. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. grupperingsjournalmallar** och välj sedan relaterad länk.  
2. Välj relevant försäkringsjournalmall och välj sedan åtgärden **Journaler**.
3. På sidan **Anl. grupper.journaler** fyller du i fälten efter behov.

## <a name="to-set-up-fixed-asset-class-codes"></a>Så här skapar du indelningskoder för anläggningstillgångar:
Indelningskoder för anläggningstillgångar kan användas för att gruppera anläggningstillgångar, t.ex. materiella och immateriella tillgångar.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. indelningar** och välj sedan relaterad länk.
2. Ange koder och namn för de indelningar som du vill skapa.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Så här skapar du underindelningskoder för anläggningstillgångar:
Du kan använda underindelningskoden för anläggningstillgångar om du vill gruppera dina tillgångar i kategorier, som exempelvis byggnader, fordon, möbler och maskiner.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. underindelningar** och välj sedan relaterad länk.
2. Ange koder och namn för de indelningar som du vill skapa.

## <a name="to-set-up-fixed-asset-location-codes"></a>Så här skapar du lagerställekoder för anläggningstillgångar
Du kan använda lagerställekoder för anläggningstillgångar om du vill registrera var en anläggningstillgång är placerad, till exempel försäljningsavdelning, reception, administration, fabrik och lager. Den här informationen är användbar för försäkrings- och lagerändamål.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. placeringar** och välj sedan relaterad länk.
2. Ange koder och namn för anläggningstillgångens lagerställe som du vill skapa.

## <a name="to-register-opening-entries"></a>Så här registrerar du ingående transaktioner
Om det är första gången som du använder anläggningstillgångarna i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du först ange inställningar för redovisningsmodulen. Hur du genomför detta beror på om anläggningstillgångar är integrerad med redovisningen.  

 Du använder följande procedur om anläggningstillgångstransaktionerna ska bokföras i redovisningen.  

1. Kontrollera att du har avslutat den grundläggande inställningsprocessen för anläggningstillgångar.  
2. Skapa ett anläggningstillgångskort för de befintliga tillgångarna.  
3. Skapa en avskrivningsregel för anläggningstillgångar för respektive avskrivning (till exempel skatt och bokslut). För varje avskrivningsregel måste du definiera villkor, till exempel integrering med redovisningen.  

    Aktivera redovisningintegration, genom att följa stegen. Försäkra dig först om att redovisningsintegration är inaktiverad för alla avskrivningsregler. Bokför sedan ingående transaktioner och slå sedan på redovisningsintegrationen.  
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Avskrivningsregler** och välj sedan relaterad länk.  
5. Välj den relevanta avskrivningsregeln. Välj **Redigera** för att öppna sidan **Avskrivningsregelkort** på fliken **Start** i gruppen **Hantera**.
6. Kontrollera att alla fält är ofyllda (ta bort markeringar) på snabbfliken **Integration**. Om du har fler än en avskrivningsregel ska du stänga av redovisningsintegrationen för samtliga.  
7. Ange följande rader för respektive anläggningstillgång i anläggningsjournalen:
   * En rad med anskaffningskostnaden.
   * En rad med den ackumulerade avskrivningen till slutet på föregående räkenskapsår.
   * En rad med den ackumulerade avskrivningen från början av det innevarande räkenskapsåret till det datum då [!INCLUDE[d365fin](includes/d365fin_md.md)] anges för att starta beräkningen av avskrivningen.

    Om du har andra ingående saldon kan du även ange dessa nu, t.ex. nedskrivning, uppskrivning o.s.v.  
8. När du har angett och bokfört journalraderna för respektive anläggningstillgång aktiverar du redovisningsintegrationen i avskrivningsreglerna.

Om anläggningstillgångarna inte har integrerats med redovisningen hoppar du över steg 6 och 8.

## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
