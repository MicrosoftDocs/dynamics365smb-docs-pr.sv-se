---
title: 'Inventera, justera och gruppera lager'
description: Lär dig hur du utför inventeringen och gör justeringar och omklassificeringar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# Inventera, justera och gruppera lager med hjälp av journaler

Inventera alla artiklar i lagret fysiskt för att säkerställa att antalet är korrekt. Vissa företag gör ett årlig inventering och andra gör inventering av alla eller bara vissa artiklar oftare. När du har inventerat artiklar använder du journaler för att bokföra de faktiska kvantiteterna i redovisningen. Till exempel när du värderar lagret i slutet av en period.

Om du vill inventera vissa artiklar oftare än andra, kanske på grund av deras värde, använder du cyklisk inventering. För cyklisk inventering tilldelar du särskilda inventeringsperioder till artiklarna. Läs mer på [Att utföra cyklisk inventering](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Om du vill justera antalet efter en fysisk inventering eller andra syften använder du en artikeljournal för att ändra lagertransaktioner utan att bokföra transaktioner. Du kan också justera antalet för en enskild artikel på ett artikelkort.

För att ändra attribut i artikeltransaktionsposter kan du använda artikelgrupperingsjournalen. Vanliga attribut för omklassificering inkluderar dimensioner och försäljningskampanjkoder. Journaler för omklassificering kan också användas för överföringar genom gruppering av lagerplatskoder och lagerställekoder. Särskilda åtgärder gäller när du vill omgruppera serie- eller partinummer och deras utgångsdatum. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).

> [!NOTE]
> I processer med flera steg registreras artiklar på lagerplatser som lagertransaktioner, inte som artikeltransaktioner. Därför utför du inventering, justering och gruppera i särskilda distributionslagerjournaler som stöder lagerställen. Därefter kan du synkronisera de nya eller ändrade lagertransaktionerna med de associerade artikeltransaktionerna och ändringarna i kvantiteter och värden.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## Att göra fysisk inventering

Utföra fysisk inventering, d.v.s. räkna alla faktiska artiklar för hand, för att se om det antal som är registrerat i programmet är samma som det antal som finns i lagret. Normalt görs inventeringar i slutet av ett räkenskapsår, men ibland görs de oftare. Om det finns skillnader bokför du de faktiska kvantiteterna på artikelkontona <!--accounts, or ledger?--> innan du gör lagervärderingen.

> [!NOTE]
> Den här proceduren beskriver hur du utför en inventering med hjälp av en journal på sidan **inventeringsjournal**. Du kan använda dokument på sidorna **Inventeringsorder** och **Inventeringsregistrering**. Dessa dokument ger större kontroll och support för att fördela inventeringsarbetet till flera anställda. Läs mer på [Beräkna och justera lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md).<br /><br />
> Observera att du inte kan använda den dokumentbaserade funktionen för att inventera artiklar på lagerställen eller distributionslagertransaktioner.

Inventeringsförfarandet omfattar även följande uppgifter:

- Beräkna förväntat lager.
- Skriv ut rapporten som ska användas vid inventering.
- Fyll i och bokför det verkliga antalet.

Beroende på din lagerinställning, inventera fysiskt på något av följande sätt. Mer information finns i [Ställa in Warehouse Management](warehouse-setup-warehouse.md).  

- Om lagerplatsen inte använder dirigerad artikelinförsel och plockning använder du sidan **Inventeringsjournal**. Proceduren liknar fysisk inventering utan cyklisk inventering.  
- Om lagerstället inte använder dirigerad artikelinförsel och plockning använder du sidan **Inventeringsjournal**. Använd sedan sidan **Artikeljournaler** för att köra åtgärden **Beräkna distributionslagerjustering**. <!--We should say what to do on each of these pages.-->

### Beräkna förväntat lager i grundläggande distributionslagerkonfiguration

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inventeringsjournaler** och väljer sedan relaterad länk.
2. Välj åtgärden **Beräkna lager**.
3. På sidan **Beräkna lagersaldo** anger du de villkor som ska användas för att skapa journalraderna, till exempel om du ska inkludera artiklar som har noll registrerade lagersaldon.
4. Ange filter om du endast vill beräkna lagret till vissa artiklar, lagerställen eller dimensioner.
5. Välj **OK**.

> [!NOTE]  
> Artikeltransaktionerna behandlas enligt den information som du har angett, och rader skapas i inventeringsjournalen. Observera att fältet **Antal inventerat** fylls i automatiskt med samma antal som fältet **antal (beräknat)**. Du behöver inte ange det räknade antalet för artiklar där dessa värden matchar. Om antalet som skiljer sig åt, anger du dock den kvantitet som har inventerats.

### Skriv ut rapporten som ska användas i samband med räkning

1. På sidan **Inventeringsjournal** som innehåller det beräknade förväntade lagret, väljer du åtgärden **Skriv ut**.
2. På sidan **Inventeringslista för distributionslager** anger du om rapporten ska visas i beräknade kvantiteter och om rapporten ska ange lagerartiklar per serie- och partinummer.
3. Ange filter om du endast vill skriva ut rapporten för vissa artiklar, lagerställen eller dimensioner.
4. Välj **Skriv ut**.

Lagerpersonalen kan nu fortsätta med att beräkna lager och registrera eventuella avvikelser på den utskrivna rapporten.

> [!NOTE]
> Det kan ta flera dagar innan utskrivna rapporter kommer tillbaka för slutlig bearbetning och bokföring. När du anger och bokför det verkliga inventerade lagret, justeras lagret så att det återspeglar skillnaden mellan förväntat och faktiskt inventerat lager. Du måste behålla de ursprungliga beräknade journalraderna och inte omberäkna det förväntade lagret, eftersom det förväntade lagret kan ändras och leda till felaktiga lagernivåer. Om du behöver skicka flera rapporter, till exempel för olika lagerställen eller en grupp av artiklar, måste du skapa och ha separata journaler.

### Om du vill ange och bokföra det verkliga inventerade lagret i grundläggande konfigurationer

1. På varje rad på sidan **Inventeringsjournal** där det faktiska lagersaldot enligt inventeringen skiljer sig från det beräknade antalet, anger du det faktiska lagersaldot i fältet **Antal inventerat**.
  
  > [!NOTE]  
  > Om det faktiska lagersaldot avviker från det beräknade på grund av att artiklar har bokförts under fel lagerställe, ska du inte ange skillnaden i inventeringsjournalen. Använda grupperingsjournalen eller en överföringsorder för att i stället dirigera om artiklarna till rätt lagerställe. 

2. Om du vill justera det beräknade antalet till det faktiska kvantiteterna väljer du åtgärden **Bokför**.

    Bokföring skapar artikeltransaktioner och inventeringstransaktioner. Öppna sidan Artikelkort för att hitta de resulterande inventeringstransaktionerna. <!--Where are they shown on an item?-->

3. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.
4. Om du vill verifiera inventeringen öppnar du sidan Artikelkort och väljer sedan åtgärden **Inventeringstransaktioner**. <!--I don't see this action -->

### Beräkna förväntat lager i avancerad distributionslagerkonfiguration.

Synkronisera artikeltransaktioner och distributionslager <!--warehouse what?--> innan du gör en fysisk inventering. Annars kommer du att bokföra till inventeringsjournalen och artikeltransaktionerna blir resultatet av inventeringen i kombination med andra distributionslager justeringar för artiklarna. Mer information finns i [Synkronisera antal i artikeltransaktioner och distributionslager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inventeringslista för distributionslager** och väljer sedan relaterad länk.  
2. Välj åtgärden **Beräkna lager** för att öppna sidan **Dist.lager beräkna lager**.  
3. Ställ in filtren för att ange de artiklar som ska räknas i journalen och välj **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] skapar en rad för varje lagerplats som uppfyller filterkraven. Du kan ta bort raderna, men om du vill bokföra resultatet som en inventering måste du räkna artikeln på alla lagerplatser där den finns.  

   Om du endast har tid att räkna artikeln på vissa lagerplatser kan det uppstå avvikelser. Bokför dem senare i artikeljournalen med hjälp av åtgärden**Beräkna dist.lagerjustering**. <!--I don't see this action-->  

### Om du vill ange och bokföra det verkliga inventerade lagret i avancerade lagerkonfigurationer

1. På sidan **Inventeringsjournal för distributionslager** anger de faktiska antalet i fältet **Antal inventerat**.  

    > [!NOTE]  
    >  Fältet **antal (beräknat)** fylls i baserat på lagerplatsposter. Detta antal kopieras till fältet **Antal inventerat** för varje rad. Om antalet i dessa fält inte matchar anger du det faktiska antalet.  

2. När du har angett alla faktiska kvantiteter väljer du åtgärden **Registrera**.  

    När du registrerar journalen skapar [!INCLUDE [prod_short](includes/prod_short.md)] två distributionslagertransaktioner i distributionslagerregistret för varje rad som har räknats och registrerats:  

    - Om de beräknade och de faktiska kvantiteterna skiljer sig åt registreras en positiv eller negativ kvantitet för lagerplatsen, och en balanserande kvantitet bokförs på lagerställets justeringslagerplats.  
    - Om den beräknade kvantiteten stämmer med den fysiska kvantiteten registrerar [!INCLUDE [prod_short](includes/prod_short.md)] **0** för både lagerplatsen och justeringslagerstället. 

När du registrerar fysiskt lager bokför du inte på artikel-, inventerings- eller värdetransaktionerna. Posterna är dock tillgängliga för avstämning när de behövs. Om du vill behålla antalet exakta kvantiteter efter att artiklar på alla lagerplatser har beräknats bokför du resultatet som en inventering av lagret <!--physical inventory journal-->. Mer information finns i [Synkronisera antal i artikeltransaktioner och distributionslager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## Utför cyklisk inventering

Du kan räkna artiklar så ofta du vill. Det kan till exempel vara mer värdefullt, eller för att de rör sig snabbt och utgör en stor del av verksamheten. Ange inventeringsfrekvensen genom att tilldela artiklarna särskilda cyklisk inventeringsperioder.

Du kan utföra cyklisk inventering på något av följande sätt beroende på lagerstyrningsinställningar: Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).  

- Om lagerplatsen inte använder dirigerad artikelinförsel och plockning använder du sidan **Inventeringsjournal**. Stegen liknar fysisk inventering utan cyklisk inventering.  
- Om lagerstället inte använder dirigerad artikelinförsel och plockning använder du sidan **Inventeringsjournal**. Använd sedan sidan **Artikeljournaler** för att köra åtgärden **Beräkna distributionslagerjustering**. <!--we should say what to do on each of these pages-->  

### Så här ställer du in cykliska inventeringsperioder

En inventering är vanligtvis en återkommande uppgift, t.ex. varje månad, kvartal eller år. Du ställer in de cykliska inventeringsperioder som du behöver tilldelar en till varje artikel. Sedan använder du åtgärden **Beräkna cyklisk inventeringsperiod** på sidan **Physical Inventory Journal** för att automatiskt skapa rader för artiklarna.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inventering cykliska inv.perioder** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Så här tilldelar du en cyklisk inventeringsperiod till en artikel

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Markera artikeln som du vill tilldela en cyklisk inventeringsperiod.  
3. I fältet **Inventering cyklisk inv.period kod** väljer du inventeringsperiod.  

> [!NOTE]
> Om du ändrar inventeringsperioden visas ett meddelande med information om resultatet av ändringen. Välj **ja** för att ändra koden och för att beräkna den första inventeringsperioden för artikeln. Nästa gång som du väljer att beräkna cyklisk inventeringsperiod i inventeringsjournalen visas artikeln som en rad på sidan **Inventering artikelval**. Du kan sedan räkna artiklar regelbundet.

### Så här börjar du en inventering baserat på den cykliska inventeringsperioder i grundläggande konfigurationer

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inventeringsjournal** och väljer sedan relaterad länk.
2. Välj åtgärden **Beräkna cyklisk inventeringsperiod**.

    Sidan **Inventering artikelval** öppnas visar de artiklar som ska inventeras enligt deras inventeringsperioder.
3. Göra fysisk inventering. Läs mer på [Att göra fysisk inventering](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### Så här börjar du en inventering baserat på den cykliska inventeringsperioder i avancerade konfigurationer

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inventeringslista för distributionslager** och väljer sedan relaterad länk.  
2. Välj åtgärden **Beräkna cyklisk inventeringsperiod**.

    Sidan **Inventering artikelval** visar de artiklar som ska inventeras enligt deras inventeringsperioder.
3. Göra fysisk inventering. Läs mer på [Att göra fysisk inventering](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Räkna artikeln på alla lagerplatser som innehåller den. Om du tar bort lagerplatsrader som har hämtats för inventering på sidan **Dist.lager inventeringslista** blir räkningen blir felaktig när du bokför den i en fysisk inventeringsjournal.  

## Justera antalet för en artikel

När du har skapat en fysisk inventering av en artikel använder du åtgärden **Justera lager** för att registrera den faktiska lagerkvantiteten.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Välj den artikel som du vill justera lagret för och välj sedan åtgärden **Justera lager**.
3. I fältet **Ny inventering** för lagerplatsen anger du resultatet av räkningen.
4. Välj **OK**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Du kan också använda åtgärden **Justera lager** som ett enkelt sätt att lägga till inköpta artiklar i lagret om du inte använder inköpsfakturor eller order för att registrera dina inköp. Lär dig mer i [registrera inköp](purchasing-how-record-purchases.md).

> [!NOTE]  
> När du har justerat lagret uppdaterar du det aktuella värdet. Mer information finns i [Omvärdera lager](inventory-how-revalue-inventory.md).

### Så här justerar du antalen på flera objekt i grundläggande konfigurationer

På sidan **Artikeljournal** kan du bokföra artikeltransaktionen direkt för att justera lager för inköp, försäljning och positiva och negativa lagerjusteringar utan att använda dokument.

Om du ofta använder artikeljournalen för att bokföra samma eller likartade journalrader, t.ex. för materialförbrukning kan sidan **Standardartikeljournal** göra detta återkommande arbete enklare. Mer information finns i [Arbeta med standardjournaler](ui-work-general-journals.md#work-with-standard-journals).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikeljournaler** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj åtgärden **Bokför** om du vill bokföra antalen.

### Så här justerar du lagerplatskvantiteter i avancerad distributionslagerkonfiguration

Om lagerstället använder dirigerad artikelinförsel och plockning använder du sidan **Artikeljournal för distributionslager** för att bokföra oplanerade positiva och negativa ändringar i lager. Till exempel för artiklar som har bokförts som saknade och som i vissa fall visas med anledning av brott eller förluster.  

Artikeljournaler för distributionslager ger dig fler justeringar för att göra dina kvantiteter mer exakta. Distributionslagret vet hur många artiklar som finns i lager och var de är lagrade, men varje justering bokförs inte i artikeltransaktionen. Kredit eller debet görs på den verkliga lagerplatsen med kvantitetsjusteringen. En mottransaktion görs på en justeringslagerplats. Justeringslagerplatsen är en virtuell lagerplats utan verkliga artiklar. Du anger den virtuella lagerplatsen i fältet **Justering lagerplatskod** på sidan **Lagerställekort**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikeljournal för distributionslager** och väljer sedan relaterad länk.  
2. Fyll i informationen i huvudet.  
3. I fältet **Artikelnr.** väljer du artikeln.  
4. Ange den lagerplats där du placerar extra artiklar eller där artiklar har försvunnit.  
5. I fältet **Kvantitet**, anger du en positiv kvantitet om du har hittat extra artiklar. Om artiklar saknas anger du ett negativt tal.  
6. Välj **Registrera**.

## Så här synkroniserar du justerade lagertransaktioner med tillhörande artikeltransaktioner

Bokför justeringslagerplatsposterna i artikeltransaktionerna för de perioder som du har definierat. I vissa företag bokförs dagliga justeringar av artikeltransaktioner, medan andra stämmer av mer sällan.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikeljournal** och väljer sedan relaterad länk.  
2. Fyll i fälten för varje journalrad.  
3. Välj åtgärden **Beräkna distributionslagerjustering** och lägg sedan till filter på sidan **Beräkna distributionslagerjustering**. Justeringar beräknas endast för de transaktioner på justeringslagerstället som uppfyller filterkraven.  
4. På snabbfliken **Alternativ** fyller du fältet **Verifikationsnr** med ett nummer som du anger manuellt. Eftersom ingen nummerserie har lagts upp för batchprojektet använder du det nummersystem som har lagts upp för distributionslagret, eller anger datumet följt av dina initialer.  
5. Välj **OK**. Positiva och negativa justeringarna summeras för varje artikel, och rader skapas i artikeljournalen.  
6. Bokför journalraderna för att ange kvantitetsavvikelserna i artikeltransaktionerna. Inventeringarna på lagerplatserna och artikeltransaktionerna är nu matchade.  

## Se även

[Beräkna lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md)  
[Lager](inventory-manage-inventory.md)  
[Översikt över hantering av distributionslager](design-details-warehouse-management.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
