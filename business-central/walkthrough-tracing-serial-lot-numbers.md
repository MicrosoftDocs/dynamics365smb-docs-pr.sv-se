---
title: 'Genomgång: Spåra serienummer/partinummer'
description: 'I det här avsnittet beskrivs de åtgärder som behövs för att förhindra att en defekt artikel säljs, och hur du spårar och återkallar artiklar vid behov.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Genomgång: Spåra serienummer/partinummer

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

När produktfel inträffar måste felen identifieras och de artiklar som påverkas måste hindras från att lämna företaget. Ifall defekta produkter redan har skickats måste du spåra vem som tagit emot dem och, vid behov, att återkalla dessa artiklar.  

Den första uppgiften vid felhantering är att ta reda på var de defekta artiklarna kommer ifrån och var de har använts. Den här undersökningen baseras på historiska data och underlättas av en sökning bland artikelspårningsposterna på sidan **Artikelspårning**.  

Nästa uppgift vid felhantering är att fastställa om de spårade artiklarna har planerats i öppna dokument, t. ex. icke-bokförda försäljningsorder eller förbrukningsjournaler. Detta arbete utförs på sidan **Hitta transaktioner**. Du kan använda funktionen Hitta transaktioner för att söka igenom alla typer av databasposter.  

## Om den här genomgången

Den här genomgången visar hur du identifierar de artiklar som är defekta, vilken leverantör som levererat dem samt var de har använts, så att de order som berörs kan stoppas eller återkallas.  

I den här genomgången tas följande aktiviteter upp:  

- Spåra förbrukning till ursprung.  
- Spåra ursprung till förbrukning.  
- Söka efter alla aktuella poster som innehåller det spårade serienumret/partinumret.  

## Roller

Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

- Kvalitetskontrollant  
- Dist.lagerchef  
- Orderhandläggare  
- Inköpsagent  

## Förutsättningar

För att kunna utföra den här genomgången behöver du:  

- Företaget [!INCLUDE[prod_short](includes/prod_short.md)].  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## Situation

Kvalitetskontrollanten Rickard utreder en försäljningsretur av artikel 1002, Racercykel. Kunden, Selangorian AB, har klagat på att svetsfogarna i ramen har spruckit. Teknikerna på kvalitetskontrollen har bekräftat att den returnerade cykelns racingram är defekt. Nu måste kvalitetskontrollen fastställa följande:  

- Vilket parti med racercykelramar som var defekt.  
- Vilken inköpsorder det defekta partiet togs emot för.  

Från försäljningsavdelningen får kvalitetskontrollanten veta att den returnerade racercykeln, artikel 1002, hade serienumret SN1. Med denna grundläggande information måste de fastställa var den färdiga racercykeln senast användes och sedan måste de spåra baklänges till tidigaste möjliga ursprung för att fastställa vilket partinummer den trasiga komponenten, d.v.s. cykelramen, kommer från.  

Resultatet av den här första artikelspårningsuppgiften identifierar vilka racerramar som var defekta och vilken leverantör som levererat dessa. Sedan, men genom samma övergripande spårningsprocess, måste kvalitetskontrollanten leta upp alla de racercyklar med racerramar från det defekta partiet som sålts, så att dessa order kan stoppas eller återkallas. Slutligen måste kvalitetskontrollanten hitta eventuella öppna dokument där det defekta partiet används så att inga ytterligare transaktioner skapas med det.  

De första två defekthanteringsuppgifterna utförs på sidan **Artikelspårning**. Den sista uppgiften utförs på sidan **Hitta transaktioner** tillsammans med sidan **Artikelspårning**.  

## Förbereda exempeldata

Du måste skapa följande nya artiklar:  

- 2000, Racercykelram: partispecifik spårning, komponent i 1002  
- 1002, Racercykel: serienummerspecifik spårning  

Du måste sedan skapa olika inköps-, produktions- och försäljningstransaktioner med dessa två artiklar.  

### Så här skapar du serviceartiklar  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Nr.** ange **2000** och fyll sedan i följande fält.  

    |Beskrivning|Basenhet|Redovisnings- Produktbokföringsmall|Moms produktbokföringsmall|Lagerbokföringsmall|Artikelspårningskod|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Racercykelram|STYCK|RÅMAT|MOMS25|RÅMAT|PARTIALLA|  

    > [!NOTE]  
    >  Välj knappen **Ny** och välj sedan **PSC** på sidan **Artikelenheter** om du vill ange basenheten.  

4. Alla övriga fält innehåller acceptabla standarddata eller behöver inte fyllas i.  
5. Klicka på **OK** för att skapa det första nya artikelkortet, 2000.  
6. Välj **Ny**.  
7. I fältet **Nr.** ange **1002** och fyll sedan i följande fält.  

    |Beskrivning|Basenhet|Redovisnings- Produktbokföringsmall|Moms produktbokföringsmall|Lagerbokföringsmall|Återanskaffningssystem|Artikelspårningskod|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Racercykel|STYCK|DETALJ|MOMS25|FÄRDIG|Prod.order|SNALLA|  

    > [!NOTE]  
    >  Välj knappen **Ny** och välj sedan **PSC** på sidan **Artikelenheter** om du vill ange basenheten.  

    Fortsätt genom att definiera artikelns produktionsinställningar.

8. På snabbfliken **Återanskaffning** i fältet **Operationsföljdsnr.** anger du **1000**.  
9. Välj fältet **Prod.strukturnr** och välj sedan **Avancerat**.  
10. På sidan **Prod. strukturlista** väljer du första raden **1000**, och sedan **Redigera**.  
11. På sidan **Prod.struktur** ändrar du värdet i fältet **Status** till **Under utveckling**.  
12. Gå till en tom rad, ange **2000** i fältet **nr.** och skriv sedan **1** i den **antal Per** fält.  
13. Ändra tillbaka värdet i fältet **Status** till **Certifierat**.  
14. Välj knappen **OK** om du vill infoga produktionsstrukturen på artikelkortet och stänga sidan **Prod.struktur**.  

    Nu köper du racercykelramar från Metallprofilexperten AB.  

### Så här kan du köpa komponenter

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Skapa en inköpsorder för leverantören, som är Metallprofilexperten AB, genom att fylla i följande radfält.  

    |Artikel|Antal|Partinr|  
    |----|--------|-------|  
    |2000|10|PARTI1|  

4. Om du vill ange partinumret, väljer du åtgärden **Artikelspårningsrader**.  
5. På sidan **Artikelspårningsrader** klickar du på listrutan i fältet **Partinr.** och **Antal (bas)** och stänger sedan sidan.  
6. Fyll i fältet **Leverantörens fakturanr** med något värde.  
7. Välj åtgärden **bokför**, välj alternativet **inleverera och fakturera**, och välj sedan **OK**-knappen.  

    Sedan köper du in racercykelramar från Teknologibyrån AB.  
8. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
9. Välj åtgärden **Ny**.
10. Skapa en inköpsorder för leverantören, som är Teknologibyrån AB, genom att fylla i följande radfält.  

    |Artikel|Antal|Partinr|  
    |----------|--------------|-------------|  
    |2000|11|PARTI2|  

11. Om du vill ange partinumret går du till snabbfliken **Rader**, gruppen **Rad**, och väljer **Artikelspårningsrader**.  
12. På sidan **Artikelspårningsrader** klickar du på listrutan i fältet **Partinr.** och **Antal (bas)** och stänger sedan sidan.  
13. Fyll i fältet **Leverantörens fakturanr** med något värde.  
14. Välj åtgärden **bokför**, välj alternativet **inleverera och fakturera**, och välj sedan **OK**-knappen.  

    Sedan producerar du racercyklar, SN1 och SN2.  

### Så här kan du producera slutartiklar

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **utsläppta produktionsorder** och väljer sedan relaterad länk.  
2. Välj gruppen **Ny**.  
3. Skapa en ny släppt produktionsorder genom att fylla i följande fält.  

    |Ursprungsnr|Antal|Serienr|  
    |----------|--------|----------|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4. Välj åtgärden **Uppdatera produktionsorder** och klicka på **OK** för att fylla i raden.  
5. Om du vill ange serienummer väljer du åtgärden **Artikelspårningsrader**.  
6. På sidan **Artikelspårningsrader** klickar du på listrutan i fältet **Serienummer** och **Antal (bas)** och stänger sedan sidan.  

    Nu bokför du förbrukningen av racercykelramar från PARTI1.  
7. På sidan **släppt produktionsorder** kan du välja åtgärden **produktionsjournal**.  
8. På sidan **Produktionsjournal** markerar du förbrukningsraden för artikeln 2000, väljer åtgärden **Artikelspårningsrader**.
9. På sidan **Artikelspårningsrader** klickar du på listrutan i fältet **Partinr.** markerar **LOT1**, och sedan knappen **OK**.  
10. Lämna alla övriga standardvärden på sidan **produktionsjournalen** och välj sedan **bokför**.  

    Sedan producerar du två racercyklar till, SN3 och SN4.  

11. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **utsläppta produktionsorder** och väljer sedan relaterad länk.  
12. Välj åtgärden **Ny**.  
13. Skapa en ny släppt produktionsorder genom att fylla i följande fält i huvudet.  

    |Ursprungsnr|Antal|Serienr|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Välj åtgärden **Uppdatera produktionsorder** för att fylla i raden.  
15. Om du vill ange serienummer går du till åtgärden **Artikelspårningsrader** och sedan numren på två rader i fältet **Serienr.** på sidan **Artikelspårningsrader**.  

    Nu bokför du ytterligare förbrukning av racercykelramar från PARTI1.  
16. På sidan **släppt produktionsorder** kan du välja åtgärden **produktionsjournal**.  
17. På sidan **Produktionsjournal** markerar du förbrukningsraden för artikeln 2000, väljer åtgärden **Artikelspårningsrader**.
18. På sidan **Artikelspårningsrader** klickar du på listrutan i fältet **Partinr.** markerar **LOT1**, och sedan knappen **OK**.  
19. Lämna alla övriga standardvärden på sidan **produktionsjournalen** och välj sedan **bokför**.  

    Du har producerat fyra racercyklar, SN1 till SN4, och förbrukat fyra av de tio racercykelramarna från PARTI1 med två ramar i varje produktionsorder.  

20. Stäng produktionsjournalen och produktionsordrarna.  

    Sedan ska racercyklarna säljas. Sälj först racercykeln med SN1 till Service AB.  

### Sälja slutartiklarna

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Ny** och skapa en försäljningsorder genom att fylla i följande fält.  

    |Kund|Artikel|Ant.|Serienr|  
    |--------------|----------|----------|----------------|  
    |Service AB|1002|1|SN1|  

3.  Om du vill ange serienummer går du till åtgärden **Artikelspårningsrader** och sedan numren på två rader i fältet **Serienr.** på sidan **Artikelspårningsrader**.  
4.  Välj åtgärden **bokför**, välj alternativet **Leverera och fakturera**, och välj sedan **OK**-knappen.  

    Sedan säljs racercykeln med SN2 till Fotograferna AB.  

5.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
6.  Välj åtgärden **Ny** och skapa en försäljningsorder genom att fylla i följande fält.  

    |Kund|Artikel|Ant.|Serienr|  
    |--------------|----------|----------|----------------|  
    |Fotograferna AB.|1002|1|SN2|  

7.  Om du vill ange serienummer går du till åtgärden **Artikelspårningsrader** och sedan numren på två rader i fältet **Serienr.** på sidan **Artikelspårningsrader**.  
8.  Välj åtgärden **bokför**, välj alternativet **Leverera och fakturera**, och välj sedan **OK**-knappen.  

    Slutligen, sälj en del racercykelramar separat. Cannon Group PLC. beställer även fyra separata racercykelramar till deras egen monteringslinje.  

9. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
10. Välj åtgärden **Ny** och skapa en försäljningsorder genom att fylla i följande fält.  

    |Kund|Artikel|Ant.|Serienr|  
    |--------------|----------|----------|----------------|  
    |Fotograferna AB.|2000|5|PARTI1|  

11. Om du vill ange serienummer, på snabbdliken **Rader** i gruppen **Rad** väljer du åtgärden **Artikelspårningsrader** och sedan numren på två rader i fältet **Serenr.** på sidan **Artikelspårningsrader**.  

    > [!NOTE]  
    >  Bokför inte den sista försäljningsordern för fem racercykelramar.  

    Nu är du klar med förberedandet av data för att visa upp funktionerna Artikelspårning och Hitta transaktioner.  

## Spåra från förbrukning till ursprung

 Från försäljningsavdelningen får kvalitetskontrollanten veta att den returnerade racercykeln, artikel 1002, har serienumret SN1. Genom att använda den grundläggande informationen kan de fastställa var den färdiga racercykeln senast användes, i det här fallet för försäljningsutleveransen till Service AB. Sedan måste kvalitetskontrollanten spåra baklänges till tidigaste möjliga ursprung för att fastställa vilket partinummer den trasiga in ramen kommer ifrån och vilken leverantör som levererat den.  

### Så här fastställer du vilket parti den defekta ramen förekom i och vem som levererade den

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **artikelspårning** och väljer sedan relaterad länk.  
2.  På sidan **Artikelspårning**, ange **SN1** i fältet **Serienrfilter** och anger sedan **1002** i fältet **Artikelfilter**.  
3.  Behåll standardinställningen för **Artikel-Endast spårade** i fältet **Visa komponenter** och behåll standardspårningsmetoden **Förbrukning – Ursprung** i **Spårningsmetod**.  
4.  Välj åtgärden **Spåra**.  

    Lägg märke till hur ett utleveranshuvud matchar sökvillkorna. Innan du fortsätter med spårningen ska du verifiera att utleveransen är den som innehöll den defekta cykeln till Service AB.  

5.  Markera spårningsraden och välj sedan åtgärden **visa dokument**.  

    Fortsätt nu att spåra ursprunget för försäljningsutleveransen som innehåller racercykeln med numret SN1.  
6.  Välj +-ikonen på spårningsraderna för att efterhand expandera och spåra bakåt i transaktionskedjan som försäljningsutleveransen har sitt ursprung i.  

    Du kan spåra följande transaktionshistorik:  

    - Första bokförda dokument bakåt i transaktionskedjan är utflödesbokföringen av SN1 från den första släppta produktionsordern.  
    - Nästa bokförda dokument bakåt i kedjan är förbrukningsbokföringen från den första släppta produktionsordern. Här kan kvalitetskontrollanten se att en racercykelram från PARTI1 har använts.  
    - Det bokförda dokument som ligger längst ned i kedjan är den bokförda inleveransen då racercykelramar i PARTI1 fördes in i lagret.  

    Kvalitetskontrollanten har nu fastställt vilket parti med racercykelramar som var defekt och kan söka efter den sista spårningsraden för att se vilken leverantör som levererade dessa, nämligen Metallprofilexperten AB.  

    > [!NOTE]  
    >  Gör inga ytterligare ändringar i spårningsresultaten eftersom du kommer att använda dem i nästa avsnitt.  

     Nu är du klar med den första defekthanteringsuppgiften med hjälp av sidan **Artikelspårning**. Kvalitetskontrollanten måste nu fastställa om andra bokförda dokument innehåller racercykelramar från PARTI1.  

## Spåra från ursprung till förbrukning

 Kvalitetskontrollanten har fastställt att de defekta racercykelramarna kommer från PARTI1. Nu måste de leta reda på eventuella andra racercyklar som innehåller ramar från det defekta partiet så att dessa cyklar kan stoppas eller återkallas.  

 Ett sätt att förbereda den här spårningsuppgiften på sidan **Artikelspårning** är att manuellt ange LOT1 i fältet **Partinrfilter** och 2000 i fälte **Artikelfilter**. I den här genomgången använder vi emellertid funktionen **Spåra motsatt – från rad**.  

### Så här hittar du all förbrukning som använder det defekta partiet  

1.  På sidan **Artikelspårning** markerar du inleveransraden (den sista spårningsraden), klickar på **Spåra motsatt – från rad**.  

    Spårningsresultatet kommer nu att baseras på filtren på spårningsraden för inleveransen, PARTI1 och artikel 2000, och resultatet kommer att baseras på spårningsmetoden **Ursprung – Förbrukning**.  

    Fortsätt och expandera alla spårningsrader om du vill visa en översikt över all förbrukning av artikeln 2000 med PARTI1.  

2.  Välj åtgärden **Expandera alla**.  

    De första fyra spårningsraderna refererar till försäljningsutleveransen till Service AB, som redan har lösts. Den sista raden indikerar att ytterligare en racercykel, SN2, har producerats i samma släppta produktionsorder och har sedan sålts och levererats vid en annan försäljningsutleverans.  

    Kvalitetskontrollanten informerar genast försäljningsavdelningen så att de kan sätta igång och återkalla den defekta racercykeln från kunden, Fotograferna AB.  

    Samtidigt kan de av de sista tre spårningsraderna utläsa att ytterligare två artiklar, SN3 och SN4, har producerats baserat på racercykelramar från PARTI1. Kvalitetskontrollanten vidtar en åtgärd för att spärra dessa två slutprodukter i lagret.  

    Nu är du klar med den andra defekthanteringsuppgiften med hjälp av sidan **Artikelspårning** för defekthantering. Eftersom sidan **Artikelspårning** endast bygger på bokförda poster måste kvalitetskontrollanten fortsätta till sidan **Hitta transaktioner** för att säkerställa att PARTI1 inte förekommer i icke-bokförda dokument.  

## Hitta alla poster som innehåller ett serienummer/partinummer

 Med sidan **Artikelspårning** fick kvalitetskontrollanten veta att de defekta racercykelramarna kom från PARTI1, vilken leverantör som levererat dem samt i vilka bokförda transaktioner de förekommit. Kvalitetskontrollanten måste nu fastställa om PARTI1 förekommer i något öppet dokument genom att integrera från spårningsresultatet till sidan **Hitta transaktioner**, där han/hon kan utföra en sökning i alla databasposter.  

### Så här hittar du alla förekomster av PARTI1 i icke-bokförda poster, t. ex. öppna order  

1.  På sidan **Artikelspårning** markerar du pekaren på den första spårningsraden, som är inleveransen för PARTI1.  
2.  Välj åtgärden **Hitta transaktioner**.  

    På sidan **Hitta transaktioner** finns förinställda sökfilter som bygger på spårningsresultatet för PARTI1. Kvalitetskontrollanten ser att de flesta av posterna hör till dokument som redan har identifierats på sidan **Artikelspårning**. Exempelvis refererar den sista raden på Hitta transaktioner av typen Produktionsorder till de två släppta produktionsordrarna som förbrukade racercykelramar från PARTI1.  

    Den andra raden på Hitta transaktioner av typen **Försäljningsrad** hör dock till en icke-bokförd dokumentrad, varför kvalitetskontrollanten fortsätter med att undersöka den.  

3.  Du kan öppna försäljningsradposten genom att markera den andra raden på Hitta transaktioner och välja åtgärden **Visa**. Alternativt kan du välja värdet i fältet **Antal poster**.  

    Nu ser kvalitetskontrollanten en öppen försäljningsrad för de defekta racercykelramarna. Kvalitetskontrollanten ger försäljningsavdelningen genast förslaget att annullera den här ordern och att skapa en ny produktionsorder, baserat på godkända racercykelramar.  

 Nu är du klar med genomgången av hur du använder sidan **Hitta transaktioner** för defekthantering tillsammans med sidan **Artikelspårning**.  

## Se relaterad [Microsoft utbildning](/training/paths/use-serial-lot-numbers/)

## Se även

[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  
[Hitta transaktioner](ui-find-entries.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
