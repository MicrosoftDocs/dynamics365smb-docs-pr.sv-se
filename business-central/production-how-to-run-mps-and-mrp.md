---
title: Kör komplett planering, nettobehov eller produktionsplan
description: I planeringssystemet beräknas antingen produktionsprogrammet eller nettobehovet, eller så beräknas båda på samma gång.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000852, 99000860
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 561b069cb3136b50a76fe6c43276edc2fb0ab5ab
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131359"
---
# <a name="run-full-planning-mps-or-mrp"></a>Kör komplett planering, nettobehov eller produktionsplan

Begreppen "Skapa inköpsförslageringsförslag" eller "beräkna nettobehov" syftar på beräkningen av produktionsprogram och materialbehov baserat på faktiskt och prognostiserat behov. I planeringssystemet beräknas antingen produktionsprogrammet eller nettobehovet, eller så beräknas båda på samma gång.  

-   Nettobehov är beräkningen av en produktionsplan baserat på faktiskt behov och efterfrågeprognosen. Beräkningen av produktionsprogrammet används för slutartiklar som har en prognosrad eller en försäljningsorderrad. Dessa artiklar kallas för "nettobehovsartiklar" och identifieras dynamiskt när beräkningen startar.  
-   Produktionsplan är beräkningen av materialbehov baserat på faktiskt behov av komponenter och efterfrågeprognosen på komponentnivå. Produktionsplanen beräknas endast för artiklar som inte är nettobehovsartiklar. Det övergripande syftet med produktionsplanen är att tillhandahålla tidsfasade formella planer, utifrån artikel, för att leverera rätt artikel i rätt tid, på rätt plats och i rätt antal.  

De planeringsalgoritmer som används för både nettobehov och produktionsplanen är identiska. Planeringsalgoritmerna berör nettobehovsberäkning, återanvändning av befintliga återanskaffningsorder och åtgärdsmeddelanden. Planeringssystemprocessen används för att söka efter vad som behövs eller kommer att behövas (efterfrågan) och vad som finns i lager eller förväntas finnas i lager (tillgång). Åtgärdsmeddelanden skapas i [!INCLUDE[prod_short](includes/prod_short.md)] när dessa kvantiteter kvittas mot varandra. Åtgärdsmeddelanden innehåller förslag om att skapa en ny order, ändra en orderorder (antal eller datum) eller annullera en order som redan är lagd. Begreppet "order" inbegriper inköpsorder, monteringsorder, produktionsorder och överföringsorder.

Länkar som skapas med planeringsmotorn mellan ett behov och dess relaterade tillgång kan spåras på sidan **Orderspårning**. Mer information finns i [Spåra relationer mellan tillgång och efterfrågan](production-how-track-demand-supply.md).   

Inställningen av artikelkort, monteringsstrukturer, produktionsstrukturer och verksamhetsföljder påverkar i hög grad att planeringsresultaten blir rätt.  

## <a name="methods-for-generating-a-plan"></a>Metoder för att skapa en plan  

-   **Beräkna fullständig plan**: Med den här funktionen bearbetas eller förnyas materialplanen. Den här processen startar när du tar bort alla planerade leveransorder som för närvarande har laddats. Alla poster i databasen planeras på nytt.  
-   **Beräkna nettoförändringsplan**: Med den här funktionen bearbetas en nettoförändringsplan. Artiklar tas med i nettoförändringsplaneringen från två typer av förändringar:  
    - **Förändringar i tillgång/efterfrågan:** Dessa omfattar förändringar i kvantiteter i försäljningsorder, efterfrågeprognosen, monteringsorder, produktionsorder eller inköpsorder. En oplanerad förändring av lagernivån betraktas också som en kvantitetsförändring.  
    - **Förändringar av planeringsparameter:** Dessa omfattar förändringar i säkerhetslager, beställningspunkt, verksamhetsföljd, strukturlista och förändringar i beräkningen av tidsenhet eller ledtid.  
-   **Hämta åtgärdsmeddelanden:** Den här funktionen fungerar som ett verktyg för planering på kort sikt genom att utfärda åtgärdsmeddelanden för att uppmärksamma användaren om eventuella ändringar som har genomförts sedan den senaste fullständiga planen eller nettoförändringsplanen beräknades.  

Med varje planeringsmetod genererar [!INCLUDE[prod_short](includes/prod_short.md)] kalkylarkstransaktioner med förmodad oändlig kapacitet. Produkktionsgruppers och maskingruppers kapacitet beaktas inte när du utvecklar scheman.  

> [!IMPORTANT]  
>  Funktionen Beräkna fullständig plan är den vanligaste processen. Funktionerna Skapa inköpsförslag och Verkställandet av åtgärdsmeddelanden kan användas för att köra beräkningen av nettoförändringsplanen.  
>   
>  Planen för funktionen Hämta åtgärdsmeddelanden kan köras mellan körningarna av nettoförändringsplanen och den fullständiga planen för att hämta en ögonblicksbild av den påverkan som planförändringarna har. Den är däremot inte tänkt som en ersättning till nettoförändringsplanen eller den fullständiga planen.  

## <a name="to-calculate-the-planning-worksheet"></a>Så här beräknar du planeringsförslaget  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **planeringsförslag** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Beräkna fullständig plan** för att öppna sidan **Skapa inköpsförslag**.  
3.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Alternativ**.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Prod.program**|Välj att initialisera beräkningen av ett produktionsprogram. Artiklar med öppna försäljningsorder eller efterfrågeprognoser tas med i beräkningen.|  
    |**Nettobehov**|Välj att initialisera beräkningen av materialbehovsplaneringen. Artiklar med beroende behov tas med i den här beräkningen. Prod.program och Nettobehov körs normalt samtidigt. Om du vill köra produktionsplanen och nettobehovet samtidigt, måste du markera fältet **Prod.plan./nettobehov** på snabbfliken **Planering** på sidan **Produktionsinställningar**.|  
    |**Fr.o.m.-datum**|Orderdatumet används för att utvärdera lagerdispositionen. Om lagersaldot för en artikel är under beställningspunkten framåtplaneras en återanskaffningsorder automatiskt i systemet från det här datumet. Om saldot för en artikel är under värdet för säkerhetslager (per startdatumet) bakåtplaneras en återanskaffningsorder som förfaller på startdatumet för planeringen.|  
    |**T.o.m.-datum**|Det här är slutdatumet för planeringshorisonten. Varken tillgång eller efterfrågan beaktas efter det här datumet. Om beställningscykeln för en artikel sträcker sig efter slutdatumet, är den giltiga planeringshorisonten för artikeln lika med order datum + beställningscykel.<br /><br /> Planeringshorisonten är den tidsperiod som planen omfattar. Om horisonten är för kort, innebär det att artiklar med en längre ledtid inte beställs i tid. Om den är för lång, innebär det att för mycket tid läggs ned på att granska och bearbeta information som troligtvis förändras innan den behövs. Du kan ange en planeringshorisont för produktion och en längre horisont för inköp, även om detta inte är ett krav. Du bör ställa in en planeringshorisont för inköp och produktion så att den täcker den ackumulerade ledtiden för komponenter.|  
    |**Stoppa och visa första felet**|Markera om du vill att planeringskörningen ska avslutas så snart den stöter på ett fel. På samma gång visas ett meddelande med information om felet (det första). Om det finns ett fel, kommer endast de planeringsrader som utfördes innan felet påträffades att visas i planeringsförslaget. Om du inte markerar fältet, kommer batchjobbet **Skapa inköpsförslag** att fortsätta köras tills det har slutförts, och eventuella fel kommer inte att avbryta batchjobbet. Om ett eller flera fel inträffar visas ett meddelande när jobbet är klart om hur många artiklar som påverkas. Sidan **Logg över planeringsfel** öppnas därefter för att visa mer information om felet och länkar till de artikelkort som påverkas.|  
    |**Använd prognos**|Välj en prognos som ska inkluderas som efterfrågan när batch-jobbet körs. Standardprognosen ställer du in på snabbfliken **Planering** på sidan **Produktionsinställningar**.|  
    |**Undanta prognos före**|Definiera hur mycket av den valda prognosen som ska inkluderas i planeringskörningen. Detta gör du genom att ange ett datum före i vilket efterfrågan inte inkluderas, och som i sin tur innebär att gammal information inte tas med.|  
    |**Ta hänsyn till planeringsparametrar för undantagsvarningar**|Fältet väljs som standard.<br /><br /> Tillgången på planeringsrader med varningar ändras normalt inte enligt planeringsparametrarna. I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet. Du kan dock ange vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar.<br /><br />|  

4.  På snabbfliken **Artikel** kan du ange filter och köra planeringsrutinerna utifrån på artikel, artikelbeskrivning eller lagerställe.  
5.  Välj **OK**. Batch-jobbet körs och sedan fylls planeringsförslaget i med planeringsraderna.  

## <a name="to-perform-action-messages"></a>Så här kan du verkställa åtgärdsmeddelanden  
1.  På sidan **Planeringsförslag** väljer du åtgärden **Verkställ åtgärdsmeddelande**.  
2.  Ange hur du skapar leveranser på snabbfliken **Alternativ**. Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Produktionsorder**|Ange hur du vill skapa produktionsorder. Du kan göra detta direkt från planeringsradförslagen. Du kan skapa antingen planerade eller fast planerade produktionsorder.|  
    |**Monteringsorder**|Ange hur du vill skapa monteringsorder. Du kan göra detta direkt från planeringsradförslagen.|  
    |**Inköpsorder**|Ange hur du vill skapa inköpsorder. Du kan göra detta direkt från planeringsradförslagen.<br /><br /> Om du väljer att kopiera planeringsradförslagen för inköpsorder till inköpskalkylarket, väljer du mall- och kalkylarksnamn här.|  
    |**Överföringsorder**|Ange hur du vill skapa överföringsorder. Du kan göra detta direkt från planeringsradförslagen.<br /><br /> Om du väljer att kopiera planeringsradförslagen för överföringsorder till inköpskalkylarket, väljer du mall- och kalkylarksnamn här.|  
    |**Kombinera överföringsorder**|Markera om du vill kombinera överföringsorder.|  
    |**Stoppa och visa första felet**|Markera om du vill att batch-jobbet **Verkställ åtgärdsmeddelande åtgärd. – Plan.** ska avslutas så snart ett fel påträffas. På samma gång visas ett meddelande med information om felet (det första). Om det finns ett fel, kommer endast de planeringsrader som bearbetades innan felet påträffades att resultera i leveransorder.|  

3.  På snabbfliken **Planeringsrad** kan du ange filter för att begränsa antalet åtgärdsmeddelanden som ska verkställas.  
4.  Välj **OK**.  

Batch-jobbet tar bort raderna i planeringsförslaget när åtgärdsmeddelandena har verkställts. De övriga raderna finns kvar i planeringsförslaget tills de antingen accepteras vid ett senare tillfälle eller tas bort. Du kan även ta bort raderna manuellt.  

## <a name="action-messages"></a>Åtgärdsmeddelanden  
Åtgärdsmeddelanden skickas av orderspårningssystemet när det inte går att uppnå balans inom det befintliga ordernätverket. Åtgärdsmeddelanden kan ses som ett förslag på hur du kan bearbeta ändringar som återställer jämvikten mellan tillgång och efterfrågan.  

Genereringen av åtgärdsmeddelanden sker en nivå i taget, med hänsyn till varje artikels lägsta-nivå-kod. På så sätt säkerställs att alla artiklar som är kopplade till eller kommer att vara kopplade till förändringar i tillgång och efterfrågan tas i beaktande.  

Användare kan upprätta dämpare för att undvika att få åtgärdsmeddelanden som är små, överflödiga eller oviktiga. Dessa dämpare begränsar genereringen av åtgärdsmeddelanden till sådana meddelanden som innehåller information om förändringar som överskrider den definierade kvantiteten eller definierat antal dagar.  

När du har granskat åtgärdsmeddelandena och bestämt om du vill acceptera vissa eller alla föreslagna förändringar, markerar du fältet **Acceptera åtgärdsmeddelande** och sedan är du klar att uppdatera planerna i enlighet med dessa.  

> [!NOTE]  
>  Ett åtgärdsmeddelande är ett förslag om att skapa en ny order, annullera en order eller ändra kvantiteten i eller datumet för en order. Med order menas en inköpsorder, överföringsorder eller produktionsorder.  

Följande åtgärdsmeddelanden genereras som svar på obalans i tillgång/efterfrågan.  

|Åtgärdsmeddelande|Beskrivning|  
|--------------------|---------------------------------------|  
|**Ny**|Om en efterfrågan inte kan tillgodoses genom åtgärdsmeddelanden med förslag om att **Ändra antal**, **Omplanera** eller **Omplanera och ändra** i befintliga order, genereras åtgärdsmeddelandet **Ny**, vilket ger kalkylark om en ny order. Dessutom skickas åtgärdsmeddelandet **Ny** om det inte finns några befintliga leveransorder inom beställningscykeln för artikeln i fråga. Med den här parametern fastställs antalet perioder framåt och bakåt i tillgänglighetsprofilen vid sökning efter en order att omplanera.|  
|**Ändra antal**|När det inträffar en kvantitetsförändring för efterfrågan som spåras till en leveransorder, genereras åtgärdsmeddelandet **Ändra antal**, vilket anger att relaterad tillgång ska ändras så att det motsvarar förändringen i efterfrågan. Om det uppstår ny efterfrågan söker [!INCLUDE[prod_short](includes/prod_short.md)] efter närmast befintliga icke reserverade leveransorder inom beställningscykeln, och skickar ett åtgärdsmeddelande om ändring för ordern.|  
|**Omplanera**|När det inträffar en ändring av datum för en leverans- eller behovsorder som orsakar obalans i ordernätverket, skickas åtgärdsmeddelandet **Omplanera**. Om det finns ett ett-till-ett-samband mellan tillgång och efterfrågan, skickas ett åtgärdsmeddelande med förslag om att leveransordern ska flyttas i enlighet med detta. Om leveransordern täcker behovet från fler än en försäljningsorder, omplaneras leveransordern till datumet för det första behovet.|  
|**Omplanera och Ändra antal**|Om både datumen för och antalet på en order har ändrats, är det nödvändigt att ändra planer med hänsyn till båda dessa faktorer. Åtgärdsmeddelanden samlar båda dessa faktorer i ett enda meddelande, **Planera & ändra antal** för att säkerställa att balansen i ordernätverket återställs.|  
|**Annullera**|Om behov som har täckts på orderbasis tas bort, skickas ett åtgärdsmeddelande om att annullera kopplade leveransorder. Om behovet inte täcks på orderbasis, skapas ett åtgärdsmeddelande för att ändra i ordern för att på så sätt minska tillgången. Om en leveransorder inte efterfrågas när åtgärdsmeddelandena genereras av användaren, till exempel vid lagerjusteringar, skickar [!INCLUDE[prod_short](includes/prod_short.md)] åtgärdsmeddelandet **Annullera** i kalkylarket.|  

## <a name="see-also"></a>Se även  
[Planerad](production-planning.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]