---
title: "Genomgång: Beräkna produkter i arbete för ett projekt | Microsoft Docs"
description: "Med Projekt kan du schemalägga förbrukningen av ditt företags resurser och hålla reda på de olika kostnader som är förknippade med förbrukningen av resurser i ett visst projekt. I projekt ingår förbrukningen av anställdas arbetstimmar, maskintimmar, lagerartiklar samt andra typer av förbrukning som du behöver hålla koll på i takt med att arbetet fortskrider."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2c043a33e02d197281877a8287df7008377d52e4
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-calculating-work-in-process-for-a-job"></a>Genomgång: Beräkna produkter i arbete för ett projekt
Med Projekt kan du schemalägga förbrukningen av ditt företags resurser och hålla reda på de olika kostnader som är förknippade med förbrukningen av resurser i ett visst projekt. I projekt ingår förbrukningen av anställdas arbetstimmar, maskintimmar, lagerartiklar samt andra typer av förbrukning som du behöver hålla koll på i takt med att arbetet fortskrider. Om ett projekt löper över en längre tid kan du behöva överföra de här kostnaderna till ett konto för produkter i arbete (PIA) på balansräkningen medan projektet färdigställs. Du kan sedan bokföra kostnaderna och försäljningsintäkterna i resultaträkningskonton när det är lämpligt.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
 I den här genomgången tas följande aktiviteter upp:  

-   Beräkna PIA.  
-   Välja beräkningsmetod för PIA.  
-   Undanta delar av ett projekt från PIA.  
-   Bokföra PIA i redovisningen.  
-   Återföra PIA.  

 Under varje steg i processen beräknas värdet på projekttransaktionerna som flyttas till redovisningen. Stegen för beräkning och bokföring är åtskilda för att du lättare ska kunna granska data och göra ändringar innan de bokförs i redovisningen. Du bör därför se till att all information är korrekt när du har kört batch-jobben för beräkning och innan du bokför.  

## <a name="roles"></a>Roller  
 I den här genomgången används projektteammedlemmen Tricia.  

## <a name="prerequisites"></a>Förutsättningar  
 Innan du kan utföra aktiviteterna i den här genomgången måste du installera [!INCLUDE[d365fin](includes/d365fin_md.md)] på datorn.  

## <a name="story"></a>Situation  
 Den här genomgången fokuserar på CRONUS AB, ett design- och konsultföretag som ritar och bygger till exempel konferenshallar och kontor, med möbler, utrustning och lagerutrymmen. De flesta som arbetar på CRONUS är projektorienterade och Tricia, en projektmedlem, använder projekt för att få en översikt över alla pågående projekt, som CRONUS har inlett, och även de projekt som avslutats. Vissa av projekten kan vara mycket för långa och löpa över månader. Tricia kan använda en PIA för att registrera produkter i arbete och spåra kostnader i hela projektet.  

## <a name="calculating-wip"></a>Beräkna PIA  
 CRONUS har vunnit ett långvarigt projekt som nu har förlängts över flera redovisningsperioder. Tricia, en projektmedlem, beräknar produkter i arbete (PIA) för att kontrollera att företagets finansiella rapporter är rätt.  

 I den här proceduren kommer Tricia att välja en särskild grupp med aktiviteter som ska inkluderas i PIA-beräkningen. I fönstret **Projektaktivitetsrader** kan hon ange dessa rader i kolumnen **PIA, totalt**.  

 De tre alternativen beskrivs i tabellen nedan.  

|Fält|Description|  
|-------------------------------------|---------------------------------------|  
|**<blank>**|Ska lämnas tom om projektaktiviteten utgör en del av en projektaktivitetsgrupp.|  
|**Summa**|Definierar intervallet eller gruppen av aktiviteter som ingår i PIA- och resultatbeloppsberäkningen. Inom gruppen ska **Typ av projektaktivitet** som angetts som **Bokföring** ingå i PIA-totalen om inte fältet **PIA-total** angetts som **Exklusive**.|  
|**Exklusive**|Gäller bara när **Typ av projektaktivitet** är **Bokföring**. Aktiviteten beaktas inte när PIA och resultatbelopp beräknas.|  

 I följande genomgången använder Tricia kostnadsvärdemetoden, företagets standard, för att beräkna PIA. Hon anger vilken del av projektet som ska inkluderas i PIA-beräkningen genom att tilldela PIA-slutsummorna till olika projektaktivitetsrader.  

### <a name="to-calculate-wip"></a>Så här beräknar du PIA  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.  
2.  I listan **Projekt** väljer du projektet **Hjortfält** och väljer sedan åtgärden **redigera**. Projektkortet öppnas i redigeringsläge.  

     PIA kan beräknas baserat på metoderna Kostnadsvärde, Förs.värde, Försäljningskostnader, Färdigställningsgrad eller Slutfört kontrakt. I det här exemplet använder CRONUS kostnadsvärdemetoden.  

3.  På snabbfliken **Bokföring**, väljer du fältet **PIA-metod** och sedan **Kostnadsvärde**.  
4.  Välj åtgärden **Projektaktivitetsrader** och ange följande värden i fältet **PIA - Summa**.  

     Värdena beskrivs i tabellen nedan.  

    |Projektaktivitetsnr|Fältet PIA, totalt|  
    |------------------|----------------------|  
    |1130|Exklusive|  
    |1190|Summa|  
    |1210|Exklusive|  
    |1310|Exklusive|  

5.  Välj åtgärden **PIA** och klicka på åtgärden **beräkna PIA**.  
6.  I fönstret **Projekt - Beräkna PIA** kan du välja det projekt som du vill beräkna PIA för. På snabbfliken **Projekt** väljer du **Hjortfält** i fältet **Nr**. .  
7.  I fältet **Bokföringsdatum** anger du ett datum som är senare än arbetsdatumet.
8.  I fältet **Verifikationsnr** anger du **1**. Detta skapar ett dokument som du kan gå tillbaka till senare för spårning.  
9. Klicka på **OK** för att köra batchjobbet. Ett meddelande visas. Klicka på knappen **OK** för att fortsätta. Stäng fönstret **Projektaktivitetsrader**.  

    > [!NOTE]  
    >  Meddelandet om att det finns varningar är kopplat till PIA-beräkningen. Du ska granska varningarna i nästa procedur.  

10. På **Projektkortet** expanderar du snabbfliken **PIA och bokföring** för att visa de beräknade värdena. Du kan också se **PIA-bokföringsdatum** och värden som har bokförts i redovisningen, om dessa finns.  

 Observera att värdet för **Bokfört kostnadsbelopp** är 215,60 i kolumnen **Till bokföra**. Detta visar den totala kostnaden för två av artiklarna i gruppen med projektaktiviteter 1110 – 1130. Den tredje artikeln har lagts **Exklusive**, och ingår därför inte i PIA-beräkningen.  

### <a name="to-review-wip-warnings"></a>Så här kan du granska PIA-varningar  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Cockpit för PIA för projekt**, och välj sedan relaterad länk.  
2.  Välj åtgärden **Hjortfält** och välj sedan åtgärden **Visa varningar**.  
3.  I fönstret **Projekt - PIA-varningar** granskar du varningen som är kopplad till projektet.  

 Efter bokföringsperiodens slut måste Tricia beräkna PIA på nytt så att även slutfört arbete fram till dagens datum kommer med.  

### <a name="to-recalculate-wip"></a>Så här beräknar du PIA på nytt  

1.  På kortet **Projekt** väljer du åtgärden **PIA-transaktioner** för att visa PIA-beräkningen.  

     I fönstret **PIA-transaktioner för projekt** visas PIA-transaktionerna från den senaste beräkningen av ett projekt, även om PIA ännu inte har bokförts i redovisningen.  

2.  Du kan följa stegen i processen som förklarar hur du beräknar PIA för att omberäkna PIA. Varje gång som PIA beräknas skapas en transaktion i fönstret **PIA-transaktioner för projekt**.  
3.  Stäng fönstret.  

> [!NOTE]  
>  Endast produkter i arbete och resultatbelopp beräknas. Detta bokförs inte i Redovisning. Om du vill bokföra värdet måste du köra batchjobbet **Bokför PIA i redovisning** när du har beräknat PIA och bokföring.

## <a name="posting-wip-to-general-ledger"></a>Bokföra PIA i reodvisningen  
 Nu när Tricia har beräknat PIA för det här projektet kan hon bokföra det i redovisningen.  

### <a name="to-post-wip-to-general-ledger"></a>Så här bokför du PIA i redovisningen  

1.  I listan **Projekt** markerar du projektet **Hjortfält**.  
2.  Välj åtgärden **PIA** och klicka på åtgärden **Bokför PIA i redovisning**.  
3.  I fönstret **Projekt - Bokför PIA i redovisning**, på snabbfliken **Projekt**, väljer du **Hjortfält** i fältet **Nr**. .  
4.  På snabbfliken **Alternativ**, i fältet **Dokumentnr för återföring**, anger du **1**.  
5.  Klicka på **OK** för att bokföra PIA i redovisningen.  
6.  Välj **OK** för att stänga bekräftelsefönstret.  

     När du har fyllt i fältet kan du visa information om bokföring i fönstret **Pia-redovisningstransaktioner**.  

7.  I listan **Projekt** väljer du projektet **Hjortfält** och väljer sedan åtgärden **PIA-redovisningstransaktioner**.  

     I fönstret **PIA-redov.transaktioner för projekt** kan du verifiera att PIA har bokförts i redovisningen.  

8.  Stäng fönstret.  
9. Öppna kortet **Projekt** för projektet **Hjortfält**.  
10. Lägg märke till att kolumnen **Bokförd**, fältet **Bokfört kostnadsbelopp i redov.** nu fylls i på snabbfliken **PIA och bokföring**, vilket anger att PIA har bokförts i redovisningen.  
11. Välj **OK** för att stänga kortet.  

## <a name="reversing-a-wip-posting"></a>Återföra en PIA-bokning  
 Tricia anser att projektaktiviteter som är exkluderade från beräkning av PIA borde vara inkluderade i PIA. Hon kan återföra de felaktiga transaktionerna utan att behöva bokföra nya PIA-transaktioner.  

### <a name="to-reverse-a-wip-posting"></a>Så här återför du en PIA-transaktioner  

1.  I listan **Projekt** markerar du projektet **Hjortfält**.  
2.  Välj åtgärden **PIA** och klicka på åtgärden **Bokför PIA i redovisning**.  
3.  I fönstret **Projekt - Bokför PIA i redovisning**, på snabbfliken **Projekt**, väljer du **Hjortfält** i fältet **Nr**. .  
4.  På snabbfliken **Alternativ**, i fältet **Dokumentnr för återföring**, anger du **1**.  
5.  Ange det ursprungliga bokföringsdatumet i fältet **Bokföringsdatum för återföring**. Detta bör vara samma datum som du använde för att beräkna PIA den första gången.  
6.  Markera kryssrutan **Endast återföring**. Detta återför tidigare bokförd PIA, men bokför ny PIA i redovisningen.  
7.  Välj **OK** för att köra batch-jobbet och välj sedan **OK** för att stänga bekräftelsefönstret.  
8.  Öppna kortet **Projekt** för **Hjortfält**.  
9. Kontrollera att det inte finns några bokförda PIA-transaktioner på snabbfliken **PIA och bokföring**.  
10. Stäng fönstret.  
11. I listan **Projekt** väljer du projektet **Hjortfält**, väljer åtgärden **PIA** och väljer åtgärden **PIA redovisningstransaktioner**. För PIA-transaktionerna är kryssrutan **Återförd** markerad.  
12. Stäng fönstret.  
13. Öppna **Projektaktivitetsrader** för projektet, inkludera de delar av projektet som bör ingå i PIA-beräkningen och därefter räkna om och bokföra det nya värdet i redovisningen.  

    > [!NOTE]  
    >  Anta att Tricia har beräknat och bokfört PIA för ett projekt med felaktiga datum. Genom att följa metoden som diskuterades tidigare kan hon återföra de felaktiga transaktionerna, korrigera datum och bokföra dessa på nytt i redovisningen.  

## <a name="next-steps"></a>Gå vidare  
 Den här genomgången har du lärt dig hur du beräknar PIA i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I större projekt kan det vara praktiskt att överföra kostnaderna till ett PIA-konto periodvis medan projektet färdigställs. Den här genomgången har visat hur man exkluderar aktivitetsrader från en beräkning. Detta visar också när du bör omberäkna. Slutligen, den här genomgången visar hur du bokför PIA i redovisningen. Ett exempel på hur du återför en PIA-bokföring till redovisningen inkluderas också.  

## <a name="see-also"></a>Se även  
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Genomgång: Hantera projekt med Projekt](walkthrough-managing-projects-with-jobs.md)   
 [Förstå PIA-metoder](projects-understanding-wip.md)   
 [Övervaka framsteg och resultat](projects-how-monitor-progress-performance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

