---
title: Inventera, justera och gruppera lager | Microsoft Docs
description: "Beskriver hur du utför en fysisk inventering, göra negativa eller positiva justeringar och ändra information, till exempel plats eller partinumret i artikeltransaktionerna och distributionslagertransaktionerna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Så här: Inventera, justera och gruppera lager
Minst en gång per räkenskapsår måste du utföra en inventering (d.v.s. räkna alla artiklar i lagret) för att se om det antal som är registrerat i databasen är samma som det antal som verkligen finns i lagret. När det faktiska antalet är känt, måste det bokföras i redovisningen som en del av lagervärderingen för periodslutet.

Även om du inventerar alla artiklarna i lagret minst en gång per år kan du ha bestämt dig för att inventera vissa artiklar oftare, kanske för att de är mer värdefulla eller för att de har en hög omsättningshastighet och utgör en stor del av verksamheten. Du kan tilldela särskilda inventeringsperioder till objekten för detta ändamål. Mer information finns i avsnittet ”Så här utför du cyklisk inventering”.

Om du behöver justera det registrerade lagerantalet, kan du i samband med inventeringen använda en artikeljournal för att ändra inventeringstransaktionerna direkt utan att bokföra affärstransaktioner. Du kan också justera för en enskild artikel på artikelkortet.

Om du behöver ändra attribut i artikeltransaktioner samt antalet, kan du använda artikelgrupperingsjournalen. Vanliga attribut när du grupperar är serie-/partinummer, utgångsdatum och dimensioner.

## <a name="to-perform-a-physical-inventory"></a>Så här utför du en inventering
Minst en gång per räkenskapsår, kanske oftare, måste du utföra en inventering (d.v.s. räkna alla faktiska artiklar för hand) för att se om det antal som är registrerat i programmet är samma som det antal som verkligen finns i lagret. Om det finns avvikelser måste du bokföra dem på artikelkontona innan du gör lagervärderingen.

Förutom den fysiska redovisningen innefattar hela processen även följande tre uppgifter:

- Beräkna förväntat lager.
- Skriv ut rapporten som ska användas, när du vill beräkna.
- Fyll i och bokför det verkliga inventerade lagret.

### <a name="to-calculate-the-expected-inventory"></a>För att beräkna förväntat lager
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inventeringsjournaler** och välj sedan relaterad länk.
2. Välj åtgärden **Beräkna lager**.
3. I fönstret **Beräkna lagersaldo** anger du de villkor som ska användas för att skapa journalraderna, till exempel om du ska inkludera artiklar som har noll registrerade lagersaldon.
4. Ange filter om du endast vill beräkna lagret till vissa artiklar, lagerplatser eller dimensioner.
5. Välj **OK**.

> [!NOTE]  
>   Artikeltransaktionerna behandlas enligt den information som du har angett, och rader skapas i inventeringsjournalen. Observera att fältet **Antal inventerat** fylls i automatiskt med samma antal som fältet **antal (beräknat)**. Med den här funktionen behöver du inte ange det inventerade faktiska lagersaldot för artiklar som är samma som det beräknade antalet. Om den inventerade kvantiteten skiljer sig från den som har angetts i fältet **antal. (Beräknat)**, måste du skriva över den med de beräknade faktiska kvantiteterna.

### <a name="to-print-the-report-used-when-counting"></a>För att skriva ut rapporten när du vill beräkna
1. I fönstret **Inventeringsjournal** som innehåller det beräknade förväntade lagret, väljer du åtgärden **Skriv ut**.
2. I fönstret **Inventeringslista** anger du om rapporten ska visas i beräknade kvantiteter och om rapporten ska ange lagerartiklar per serie-/partinummer.
3. Ange filter om du endast vill skriva ut rapporten för vissa artiklar, lagerplatser eller dimensioner.
4. Välj knappen **Skriv ut**.

Lagerpersonalen kan nu fortsätta med att beräkna lager och registrera eventuella avvikelser på den utskrivna rapporten.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Fylla i och bokföra det verkliga inventerade lagret
1. På varje rad i fönstret **Inventeringsjournal** där det faktiska lagersaldot enligt inventeringen skiljer sig från det beräknade antalet, anger du det faktiska lagersaldot i fältet **Antal inventerat**.

    Projektspecifika fält uppdateras därefter.

    > [!NOTE]  
>   Om det faktiska lagersaldot avviker från det beräknade på grund av att artiklar har bokförts under fel lagerställekod, ska du inte ange skillnaden i inventeringsjournalen. Använda grupperingsjournalen eller en överföringsorder för att i stället dirigera om artiklarna till rätt lagerställe. Mer information om hur du delar upp rader finns i Artikelgrupperingsjnl eller så här skapar du överföringsorder.

2. Om du vill justera det beräknade antalet till det faktiska kvantiteterna väljer du åtgärden **Bokför**.

    Både artikeltransaktioner och inventeringstransaktioner skapas. Öppna artikelkortet för att visa de resulterande inventeringstransaktionerna.

3. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.
4. Om du vill verifiera inventeringen öppnar du artikelkortet i fråga och väljer sedan åtgärden **Fysiska inventeringstransaktioner**.

# <a name="to-perform-cycle-counting"></a>Så här: Utför Cyklisk inventering
Även om du inventerar alla artiklarna i lagret minst en gång per år kan du ha bestämt dig för att inventera vissa artiklar oftare, kanske för att de är mer värdefulla eller för att de har en hög omsättningshastighet och utgör en stor del av verksamheten. Du kan tilldela särskilda inventeringsperioder till objekten för detta ändamål.

> [!NOTE]  
>   Om lagerstället är inställt på dirigerad artikelinförsel och plockning, använder du först fönstret **Dist.lager inventeringsjournal** och sedan använder du fönstret **Beräkna dist.lager justering** för att köra **Artikeljournal**.

## <a name="to-set-up-counting-periods"></a>Så här ställer du in cykliska inventeringsperioder
En inventering utförs vanligtvis regelbundet, t.ex. varje månad, kvartal eller år. Du kan välja vilken cykliska inventeringsperiod som är nödvändiga.

Du ställer in de cykliska inventeringsperioder som du vill använda och därefter fördelar du en till varje artikel. När du utför en inventering och använder **Beräkna cyklisk inventeringsperiod** i inventeringsjournalen, skapas rader för artiklarna automatiskt.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inventering cykliska inv.perioder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Så här tilldelar du en cyklisk inventeringsperiod till en artikel  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.  
2. Markera artikeln som du vill tilldela en cyklisk inventeringsperiod.  
3. I fältet **Inventering cyklisk inv.period kod** väljer du lämplig cyklisk inventeringsperiod.  
4. Välj **ja** för att ändra koden och för att beräkna den första cykliska inventeringsperioden för artikeln. Nästa gång som du väljer att beräkna cyklisk inventeringsperiod i inventeringsjournalen visas artikeln som en rad i fönstret **Inventering artikelval**. Du kan nu börja räkna artikeln med regelbundna intervall.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Så här initierar du en inventering baserat på cykliska inventeringsperioder
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inventeringsjournal** och välj sedan relaterad länk.
2. Välj åtgärden **Beräkna cyklisk inventeringsperiod**.

    Fönstret **Inventering artikelval** öppnas. Det visar de artiklar som du har fastställt cykliska inventeringsperioder för som ska inventeras enligt motsvarande cykliska inventeringsperioder.
3. Utför inventeringen. Mer information finns i avsnittet "Så här utför du en inventering av lagret".

## <a name="to-adjust-the-inventory-of-one-item"></a>Justera lagret för en artikel
När du har skapat en fysisk inventering av en artikel i ditt lagerområde kan du använda funktionen **Justera lager** för att registrera den faktiska lagerkvantiteten.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.
2. Välj den artikel som du vill justera lagret för och välj sedan åtgärden **Justera lager**.
3. Ange lagerkvantiteten som du vill registrera för artikeln i fältet **Nytt lager**.
4. Välj **OK**.

Nu har artikelns lager justerats. Den nya kvantiteten visas i fältet **Aktuellt lager** i fönstret **Justera lager** och i fältet **Lager** i fönstret **Artikelkort**.

Du kan också använda funktionen **Justera lager** som ett enkelt sätt att placera inköpta artiklar i lagret om du inte använder inköpsfakturor eller order för att registrera dina inköp. För mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).

> [!NOTE]  
>   När du har justerat lagret, måste du uppdatera det med det aktuella, beräknade värdet. Mer information finns i [Så här omvärderar du lager](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Så här justerar du lagerkvantiteten för ett eller flera objekt
I fönstret **Artikeljournal** kan du bokföra artikeltransaktionen direkt för att justera lager i anslutnig till inköp, försäljning och positiva och negativa lagerjusteringar utan att använda dokument.

Om du ofta använder artikeljournalen för att bokföra samma eller likartade journalrader, kan du till exempel i anslutning med materialförbrukning använda fönstret **Standardartikeljournal** om du vill göra detta återkommande arbete enklare. Mer information finns i avsnittet "standardjournaler" i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikeljournaler** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj åtgärden **Bokför** för att justera lagret.

> [!NOTE]  
>   När du har justerat lagret, måste du uppdatera det med det aktuella, beräknade värdet. Mer information finns i [Så här omvärderar du lager](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Gruppera om en artikels partinummer
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournaler** och välj sedan relaterad länk.
2. I fönstret **Artikelgrupp.journal** fyller du i fälten efter behov.
3. Till i fältet **Partinr** anger du artikelns aktuella partinummer.
4. I fältet **Nytt partinr** anger du artikelns aktuella partinummer.
5. Välj åtgärden **Bokföra**.

## <a name="see-also"></a>Se även
[Lagersaldo](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

