---
title: Inventera, justera och gruppera lager | Microsoft Docs
description: Beskriver hur du utför en fysisk inventering, göra negativa eller positiva justeringar och ändra information, till exempel plats eller partinumret i artikeltransaktionerna och distributionslagertransaktionerna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d2052d2d6cc5d06eb001d2b29eb6d5fc79d8b00c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785979"
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Inventera, justera och gruppera lager med hjälp av journaler
Minst en gång per räkenskapsår måste du utföra en inventering (d.v.s. räkna alla artiklar i lagret) för att se om det antal som är registrerat i databasen är samma som det antal som verkligen finns i lagret. När det faktiska antalet är känt, måste det bokföras i redovisningen som en del av lagervärderingen för periodslutet.

Även om du inventerar alla artiklarna i lagret minst en gång per år kan du ha bestämt dig för att inventera vissa artiklar oftare, kanske för att de är mer värdefulla eller för att de har en hög omsättningshastighet och utgör en stor del av verksamheten. Du kan tilldela särskilda inventeringsperioder till objekten för detta ändamål. Mer information finns i avsnittet [Så här utför du cyklisk inventering](inventory-how-count-adjust-reclassify.md#to-perform-cycle-counting).

Om du behöver justera det registrerade lagerantalet, kan du i samband med inventeringen använda en artikeljournal för att ändra inventeringstransaktionerna direkt utan att bokföra affärstransaktioner. Du kan också justera för en enskild artikel på artikelkortet.

Om du måste ändra attribut i artikeltransaktionsposter kan du använda artikelgrupperingsjournalen. Vanliga attribut när du omgrupperar är dimensioner och försäljningskampanjkoder, men du utför även ”systemöverföringar” genom att omgruppera lagerplats- och lagerställekoder. Särskilda åtgärder gäller när du vill omgruppera serie- eller partinummer och deras utgångsdatum. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).

> [!NOTE]
> I avancerad lagerkonfiguration registreras artiklar på lagerställen som lagertransaktioner, inte som artikeltransaktioner. Därför utför du inventering, justering och gruppera i särskilda distributionslagerjournaler som stöder lagerställen. Därefter kan använda du särskilda funktionerna för att synkronisera de nya eller ändrade lagertransaktionerna med de associerade artikeltransaktionerna och ändringarna i kvantiteter och värden. Detta beskrivs i nedanstående procedurer vid behov.

## <a name="to-perform-a-physical-inventory"></a>Så här utför du en inventering
Minst en gång per räkenskapsår, kanske oftare, måste du utföra en inventering (d.v.s. räkna alla faktiska artiklar för hand) för att se om det antal som är registrerat i programmet är samma som det antal som verkligen finns i lagret. Om det finns avvikelser måste du bokföra dem på artikelkontona innan du gör lagervärderingen.

> [!NOTE]
> Den här proceduren beskriver hur du utför en inventering med hjälp av en journal på sidan **inventeringsjournal**. Du kan också utföra uppgiften med dokument, sidorna **inventeringsorder** och **inventeringsregistrering** som ger mer kontroll och support och distribuerar inventeringen till flera medarbetare. För mer information, se [Beräkna lager med dokument](inventory-how-count-inventory-with-documents.md).<br /><br />
> Observera att den dokumentbaserade funktionen inte kan användas för att inventera artiklar på lagerställen, distributionslagertransaktioner.

Förutom den fysiska redovisningen innefattar hela processen även följande tre uppgifter:

- Beräkna förväntat lager.
- Skriv ut rapporten som ska användas, när du vill beräkna.
- Fyll i och bokför det verkliga inventerade lagret.

Du kan utföra inventeringsjournalen på något av följande sätt beroende på lagerstyrningsinställningar: Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

-   Om lagerstället inte använder dirigerad artikelinförsel och plockning (grundläggande distributionslagerkonfiguration), använder du sidan **Inventeringsjournal** på menyn **Lager**. Tillvägagångssättet är ungefär det samma som när du utför en vanlig inventering.  
-   Om lagerstället är inställt på dirigerad artikelinförsel och plockning (avancerad distributionslagerkonfiguration) använder du först sidan **Dist.lager inventeringsjournal** fönstret, och sedan använder du sidan **Artikeljournal** för att köra **Beräkna dist.lager justering**-funktionen.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Beräkna förväntat lager i grundläggande distributionslagerkonfiguration.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventeringsjournaler** och välj sedan relaterad länk.
2. Välj åtgärden **Beräkna lager**.
3. På sidan **Beräkna lagersaldo** anger du de villkor som ska användas för att skapa journalraderna, till exempel om du ska inkludera artiklar som har noll registrerade lagersaldon.
4. Ange filter om du endast vill beräkna lagret till vissa artiklar, lagerställen eller dimensioner.
5. Välj **OK**.

> [!NOTE]  
>   Artikeltransaktionerna behandlas enligt den information som du har angett, och rader skapas i inventeringsjournalen. Observera att fältet **Antal inventerat** fylls i automatiskt med samma antal som fältet **antal (beräknat)**. Med den här funktionen behöver du inte ange det inventerade faktiska lagersaldot för artiklar som är samma som det beräknade antalet. Om den inventerade kvantiteten skiljer sig från den som har angetts i fältet **antal. (Beräknat)**, måste du skriva över den med de beräknade faktiska kvantiteterna.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Skriv ut rapporten som ska användas, när du vill beräkna.
1. På sidan **Inventeringsjournal** som innehåller det beräknade förväntade lagret, väljer du åtgärden **Skriv ut**.
2. På sidan **Inventeringslista** anger du om rapporten ska visas i beräknade kvantiteter och om rapporten ska ange lagerartiklar per serie-/partinummer.
3. Ange filter om du endast vill skriva ut rapporten för vissa artiklar, lagerställen eller dimensioner.
4. Välj knappen **Skriv ut**.

Lagerpersonalen kan nu fortsätta med att beräkna lager och registrera eventuella avvikelser på den utskrivna rapporten.

> [!NOTE]
> Det kan ta flera dagar innan utskrivna rapporter kommer tillbaka för slutlig bearbetning och bokföring. När du anger och bokför det verkliga inventerade lagret, justeras lagret så att det återspeglar skillnaden mellan förväntat och faktiskt inventerat lager. Du måste behålla de ursprungliga beräknade journalraderna och inte omberäkna det förväntade lagret, eftersom det förväntade lagret kan ändras och leda till felaktiga lagernivåer. Om du behöver skicka flera rapporter, till exempel för olika lagerställen eller en grupp av artiklar, måste du skapa och ha separata journaler.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Om du vill ange och bokföra det verkliga inventerade lagret i grundläggande konfigurationer
1. På varje rad på sidan **Inventeringsjournal** där det faktiska lagersaldot enligt inventeringen skiljer sig från det beräknade antalet, anger du det faktiska lagersaldot i fältet **Antal inventerat**.

    Projektspecifika fält uppdateras därefter.

    > [!NOTE]  
    >   Om det faktiska lagersaldot avviker från det beräknade på grund av att artiklar har bokförts under fel lagerställekod, ska du inte ange skillnaden i inventeringsjournalen. Använda grupperingsjournalen eller en överföringsorder för att i stället dirigera om artiklarna till rätt lagerställe. Mer information finns i Artikelgrupperingsjournal eller Skapa överföringsorder.

2. Om du vill justera det beräknade antalet till det faktiska kvantiteterna väljer du åtgärden **Bokför**.

    Både artikeltransaktioner och inventeringstransaktioner skapas. Öppna artikelkortet för att visa de resulterande inventeringstransaktionerna.

3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.
4. Om du vill verifiera inventeringen öppnar du artikelkortet i fråga och väljer sedan åtgärden **Fysiska inventeringstransaktioner**.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Beräkna förväntat lager i avancerad distributionslagerkonfiguration.
Synkronisera artikeltransaktioner och distributionslager innan du utför lagerinventeringen, annars kommer de resultat du bokför i inventeringsjournalen och i artikeltransaktionerna under processens sista del att utgöra inventeringsresultaten kombinerade med andra distributionslagerjusteringar för de artiklar som räknats. Mer information finns i [Synkronisera antal i artikeltransaktioner och distributionslager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lagerinventeringsjournal** och välj sedan relaterad länk.  
2. Välj åtgärden **Beräkna lager**. Beställningssidan för batch-jobbet **Dist.lager beräkna lager** öppnas.  
3. Ställ in filtren för att begränsa de artiklar som ska räknas i journalen och klicka sedan på knappen **OK**.

    En rad skapas för varje lagerplats som uppfyller filterkraven. Du kan fortfarande ta bort vissa av raderna, men om du vill bokföra resultatet som en inventering måste du räkna artikeln på alla lagerställen där den finns.  

     Om du endast har tid att räkna artikeln på vissa lagerställen kan det uppstå avvikelser. Registrera dem och bokför dem senare i artikeljournalen med hjälp av **Beräkna dist.lagerjustering** funktionen.  


### <a name="to-print-the-report-to-be-used-when-counting"></a>Skriv ut rapporten som ska användas i samband med räkning
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventeringslista för distributionslager** och välj sedan tillhörande länk.  
2. Öppna sidan för rapportbegäran och skriv ut de listor som du vill att de anställda ska registrera de artikelantal på som de räknar på respektive lagerplats.  

Lagerpersonalen kan nu fortsätta med att beräkna lager och registrera eventuella avvikelser på den utskrivna rapporten.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Om du vill ange och bokföra det verkliga inventerade lagret i avancerade lagerkonfigurationer
1. När inventeringen är klar anger du kvantiteterna i fältet **Antal inventerat** i inventeringsjournalen.  

    > [!NOTE]  
    >  I inventeringsjournalen fylls fältet **Lagersaldo (beräknat)** automatiskt i baserat på lagerplatsposterna och dessa kvantiteter kopieras till fältet **Antal inventerat** på respektive rad. Om den inventerade kvantiteten skiljer sig från den som har angetts i fältet Lagersaldo (beräknat) måste du ange den kvantitet som har räknats manuellt.  

2. Välj **Registrera** när du har angett alla inventerade kvantiteter.  

    När du registrerar journalen skapas två distributionslagertransaktioner i distributionslagerregistret för varje rad som har räknats och registrerats:  

    -   Om de beräknade och de fysiska kvantiteterna skiljer sig åt registreras en positiv eller negativ kvantitet för lagerstället, och en balanserande kvantitet bokförs på lagerställets justeringslagerplats.  
    -   Om den beräknade kvantiteten stämmer med den fysiska kvantiteten registreras en nolltransaktion för både lagerstället och justeringslagerstället. Transaktionerna är det som visar att en inventering av lagret har utförts på registreringsdatumet och att det inte fanns några avvikelser för artikeln.  

När du registrerar inventeringen bokför du inte artikeltransaktioner, inventeringstransaktioner eller värdetransaktioner, utan posterna finns där för eventuell avstämning. Om du vill veta exakt vad som sker i distributionslagret, och du har inventerat alla lagerställen där artiklar finns registrerade, bör du i stället omedelbart bokföra resultatet som en inventering. Mer information finns i [Synkronisera antalet i artikeltransaktioner och distributionslager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).


## <a name="to-perform-cycle-counting"></a>Så här: Utför Cyklisk inventering
Även om du inventerar alla artiklarna i lagret minst en gång per år kan du ha bestämt dig för att inventera vissa artiklar oftare, kanske för att de är mer värdefulla eller för att de har en hög omsättningshastighet och utgör en stor del av verksamheten. Du kan tilldela särskilda inventeringsperioder till objekten för detta ändamål.

Du kan utföra cyklisk inventering på något av följande sätt beroende på lagerstyrningsinställningar: Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

-   Om lagerstället inte använder dirigerad artikelinförsel och plockning (grundläggande distributionslagerkonfiguration), använder du sidan **Inventeringsjournal** på menyn **Lager**. Tillvägagångssättet är ungefär det samma som när du utför en vanlig inventering.  
-   Om lagerstället är inställt på dirigerad artikelinförsel och plockning (avancerad distributionslagerkonfiguration) använder du först sidan **Dist.lager inventeringsjournal** fönstret, och sedan använder du sidan **Artikeljournal** för att köra **Beräkna dist.lager justering**-funktionen.  

### <a name="to-set-up-counting-periods"></a>Så här ställer du in cykliska inventeringsperioder
En inventering utförs vanligtvis regelbundet, t. ex. varje månad, kvartal eller år. Du kan välja vilken cykliska inventeringsperiod som är nödvändiga.

Du ställer in de cykliska inventeringsperioder som du vill använda och därefter fördelar du en till varje artikel. När du utför en inventering och använder **Beräkna cyklisk inventeringsperiod** i inventeringsjournalen, skapas rader för artiklarna automatiskt.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventering cykliska inv.perioder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Så här tilldelar du en cyklisk inventeringsperiod till en artikel  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2. Markera artikeln som du vill tilldela en cyklisk inventeringsperiod.  
3. I fältet **Inventering cyklisk inv.period kod** väljer du lämplig cyklisk inventeringsperiod.  
4. Välj **ja** för att ändra koden och för att beräkna den första cykliska inventeringsperioden för artikeln. Nästa gång som du väljer att beräkna cyklisk inventeringsperiod i inventeringsjournalen visas artikeln som en rad på sidan **Inventering artikelval**. Du kan nu börja räkna artikeln med regelbundna intervall.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Så här initialiserar du en inventering baserat på den cykliska inventeringsperioder i grundläggande konfigurationer
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventeringsjournal** och välj sedan relaterad länk.
2. Välj åtgärden **Beräkna cyklisk inventeringsperiod**.

    Sidan **Inventering artikelval** öppnas. Det visar de artiklar som du har fastställt cykliska inventeringsperioder för som ska inventeras enligt motsvarande cykliska inventeringsperioder.
3. Utför inventeringen. Mer information finns i [Så här utför du en inventering av lagret](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Så här initialiserar du en inventering baserat på den cykliska inventeringsperioder i avancerade konfigurationer
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lagerinventeringsjournal** och välj sedan relaterad länk.  
2. Välj åtgärden **Beräkna cyklisk inventeringsperiod**.

    Sidan **Inventering artikelval** öppnas. Det visar de artiklar som du har fastställt cykliska inventeringsperioder för som ska inventeras enligt motsvarande cykliska inventeringsperioder.
3. Utför inventeringen. Mer information finns i [Så här utför du en inventering av lagret](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).  

    > [!NOTE]  
    >  Du måste inventera artikeln på alla lagerställen som innehåller den aktuella artikeln. Om du tar bort vissa lagerplatsrader som har hämtats för inventering på sidan **Dist.lager inventeringslista**, kommer du inte att räkna alla artiklarna i lagret. Om sådana ofullständiga resultat senare bokförs i Inventeringsjournal, kommer beloppen som bokförs, är inkorrekta.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Justera lagret för en artikel
När du har skapat en fysisk inventering av en artikel i ditt lagerområde kan du använda funktionen **Justera lager** för att registrera den faktiska lagerkvantiteten.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan tillhörande länk.
2. Välj den artikel som du vill justera lagret för och välj sedan åtgärden **Justera lager**.
3. Ange lagerkvantiteten som du vill registrera för artikeln i fältet **Nytt lager**.
4. Välj **OK**.

Nu har artikelns lager justerats. Den nya kvantiteten visas i fältet **Lagersaldo** på sidan **Artikelkort**.

Du kan också använda funktionen **Justera lager** som ett enkelt sätt att placera inköpta artiklar i lagret om du inte använder inköpsfakturor eller order för att registrera dina inköp. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

> [!NOTE]  
>   När du har justerat lagret, måste du uppdatera det med det aktuella, beräknade värdet. Mer information finns i [Omvärdera lager](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Så här justerar du lagerkvantiteten på flera objekt i grundläggande konfigurationer
På sidan **Artikeljournal** kan du bokföra artikeltransaktionen direkt för att justera lager i anslutnig till inköp, försäljning och positiva och negativa lagerjusteringar utan att använda dokument.

Om du ofta använder artikeljournalen för att bokföra samma eller likartade journalrader, kan du till exempel i anslutning med materialförbrukning använda sidan **Standardartikeljournal** om du vill göra detta återkommande arbete enklare. Mer information finns i [Arbeta med standardjournaler](ui-work-general-journals.md#working-with-standard-journals).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager artikeljournaler** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj åtgärden **Bokför** för att justera lagret.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Så här justerar du lagerplatskvantiteter i avancerad distributionslagerkonfiguration  
Om ditt lagerställe använder dirigerad artikelinförsel och plockning använder du **Dist.lager artikeljournal** för att bokföra alla positiva och negativa justeringar av artikelkvantitet som du vet är verkliga tillskott, till exempel artiklar som tidigare har bokförts som saknade och som oväntat har dykt upp, eller verkliga förluster, till exempel då något har gått sönder.  

När du använder artikeljournalen för distributionslagret får du ytterligare en justeringsnivå, som bidrar till att göra kvantitetsposterna ännu mer exakta, till skillnad från när du bokför justeringar i lagerartikeljournalen Distributionslagret därmed har alltid en fullständig post för hur många artiklar som finns och var de lagras, men alla justeringsregistreringar bokförs inte automatiskt som artikeltransaktioner. I registrering processen, debet eller kredit sker på den verkliga lagerstället med kvantitetsjusteringen och en mottransaktion skapas i en justeringslagerplats, en virtuell lagerplats med inga verkliga artiklar. Den här lagerstället definieras i **Justering lagerställeskod** på lagerställekortet.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager artikeljournal** och välj sedan relaterad länk.  
2.  Fyll i informationen i huvudet.  
3.  Fyll i fältet **Artikelnr** på raden.  
4.  Ange den lagerplats där du placerar extra artiklar eller där du har upptäckt att artiklar har försvunnit.  
5.  Fyll i den kvantitet som du anser vara en avvikelse i fältet **Antal**. Om du har hittat extra artiklar anger du ett positivt tal. Om artiklar saknas anger du ett negativt tal.  
6.  Välj **Registrera**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Så här synkroniserar du justerade lagertransaktioner med tillhörande artikeltransaktioner
Enligt de intervall som har angetts i företagets principer måste du bokföra distributionslagrets justeringslagerplatsposter som artikeltransaktioner. Vissa företag bokför justeringar varje dag som artikeltransaktioner, medan andra anser att det räcker med att göra avstämningar mer sällan.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikeljournal** och välj sedan relaterad länk.  
2.  Fyll i fälten för varje journalrad.  
3.  Välj sidan **Beräkna dist.lager justering** och fyll i de filter som är lämpliga i fönstret för begäran om batch-jobb. Justeringar beräknas endast för de transaktioner på justeringslagerstället som uppfyller filterkraven.  
4.  På snabbfliken **Alternativ** fyller du fältet **Verifikationsnr** med ett nummer som du anger manuellt. Eftersom ingen nummerserie har lagts upp för batch-jobbet använder du det nummersystem som har lagts upp för distributionslagret, eller anger datumet följt av dina initialer.  
5.  Välj knappen **OK**. Positiva och negativa justeringarna summeras för varje artikel, och rader skapas i artikeljournalen för de artiklar där summan antingen är positiv eller negativ.  
6.  Bokför journalraderna för att ange kvantitetsavvikelserna i artikeltransaktionerna. Lagersaldot på lagerställena stämmer nu exakt med det som står i artikeltransaktionerna.  

## <a name="to-reclassify-an-items-lot-number"></a>Gruppera om en artikels partinummer
Om du måste ändra attribut i artikeltransaktionsposter kan du använda artikelgrupperingsjournalen. Vanliga attribut när du omgrupperar är dimensioner och försäljningskampanjkoder, men du utför även ”systemöverföringar” genom att omgruppera lagerplats- och lagerställekoder.

Särskilda åtgärder gäller när du vill omgruppera serie- eller partinummer och deras utgångsdatum. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).

Följande exempel baseras på en lagerställekod. Åtgärderna är liknande för andra typer av artikelattribut.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelgrupperingsjournaler** och välj sedan relaterad länk.
2. På sidan **Artikelgrupp.journal** fyller du i fälten efter behov.
3. I fältet **Lagerställekod** anger du artikelns aktuella lagerställekod.
4. I fältet **Ny lagerställekod** anger du artikelns nya lagerställekod.
5. Välj åtgärden **Bokföra**.

Information om överföring av artiklar med full kontroll över kvantiteter som levererats och tagits emot finns i [Överföra lager mellan lagerställen](inventory-how-transfer-between-locations.md).

## <a name="see-also"></a>Se även
[Beräkna lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md)  
[Lager](inventory-manage-inventory.md)
[Lagerstyrningssystem](warehouse-manage-warehouse.md)    
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]