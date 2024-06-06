---
title: Välj för intern verksamhet i avancerade konfigurationer för distributionslager
description: 'Om lagerstället använder plockning och leverans väljer du komponenter för produktions-, och monterings- och projektaktiviteter på sidan Distributionslagerplockning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Plocka för produktion, montering eller projekt i avancerade distributionslagerkonfigurationer

Hur du för in plockningskomponenter för produktions, projekt eller monteringsorder beror på hur distributionslagret har ställts in som lagerställe. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).

I en avancerad lagerkonfiguration för det utgående flödet (plocka), slå på **Begär plockning** och växlingsknappen **Kräver utleverans** på sidan **Lagerställekort** för lagerstället.

När Lagerställe är inställt på att begära plockningsbearbetning och utleveransbearbetning använder du plockningsdokumenten för att skapa och bearbeta plockningsinformationen innan du bokför användningen eller förbrukningen av komponenter.  

Du kan inte skapa de distributionslagerplockdokument från början. Plockning är en del av ett arbetsflöde där en person som bearbetar order skapar dem med en pushmetod, eller som skapar lagerpersonalen på en pullmetod:

- Med en push-metod, där du använder åtgärden **Skapa plockning** på sidan **Produktionsorder**, **Monteringsorder**, **Projektkort**. Välj raderna att plocka och förbered plockningar genom att till exempel ange vilka fack som ska tas från och placeras i, och hur många enheter som ska hanteras. Lagerplatser kan fördefinieras för distributionslagerstället eller resurs.
- Det sätt på vilket du släpper **produktionsorder**, **monteringsorder**, **projektkort** till lagerställe som gör artiklarna tillgängliga för plockning. På sidan **Plockningskalkylark** kan distributionslagerpersonal använda åtgärden **Hämta dist.lager dokument** för att hämta sina tilldelade plockningar.

Om du vill plocka eller flytta komponenter för källdokumenten med en pullmetod måste du släppa källdokumentet så att det är klart för plockning. Släppa källdokumenten för intern operation på följande sätt.  

|Källdokument|Släppningsmetod|  
|---------------------|--------------------|  
|Produktionsorder|Ändra order statusen till släppt eller skapa en utsläppt produktionsorder direkt.|  
|Monteringsorder|Ändra status till släppt.|
|Projekt | Ändra status för att öppna eller skapa projekt med statusen öppen direkt.|  

## <a name="production"></a>Produktion

Använd dokumentet **Dist.lager plockning** för att plocka produktionskomponenter i flödet till produktion.

För en lagerställe där lagerplatser används för att flytta artiklar till öppna produktionslagerplats kan du använda följande metoder:

* För en lagerställe som använder dirigerad artikelinförsel och plockning följer du stegen i artikeln [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).
* För andra lagerställen följer du stegen i [Flytta objekt internt i grundläggande lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) .

## <a name="assembly"></a>Montering

Använd dokument **Dist.lager plockning** för att flytta monteringskomponenter till monteringsområdet.

[!INCLUDE [prod_short](includes/prod_short.md)] stöder montering mot lager och montering mot kundorder typer för monteringsflöden. Om du vill lära dig mer om montering på beställning i det utgående lagerflödet, gå till [Hantering av artikel för montering mot kundorder i Distributionslagerutleverans](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Projekthantering

Använd dokumentet **Dist.lager plockning** för att plocka projektkomponenter i flödet till projekthantering.

> [!NOTE]
> Möjligheten att plocka komponenter för projektplaneringsrader har lagts till [!INCLUDE[d365fin](includes/d365fin_md.md)] i utgivningscykel 2 år 2022. Om du vill börja använda funktionen måste en administratör aktivera **Funktionsuppdatering: Aktivera lager- och distributionslagerplockning från Projekt** på sidan **Funktionshantering**.
>
> Projekt stöder inte avancerade konfigurationer där växlingsknappen **Dirigerad art.inf. och plock.** är aktiverad.

## <a name="check-whether-items-are-available-for-picking"></a>Kontrollera om artiklar är tillgängliga för plockning

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Så här skapar du plockningsdokumenten i bulk med plockningskalkylarket

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Plockningskalkylark** och väljer sedan relaterad länk.  

2. Välj åtgärden **Hämta dist.lager dokument**.  

    I listan visas den släppta produktionsorder, projekt, monteringsorder som har vidarebefordrats till plockningsfunktionen. Orderna innehåller de för vilka plockningsinstruktioner redan har skapats. Dokument med plockningsrader som är plockade och registrerade visas inte i den här listan.  
3. Välj de order som du vill förbereda en plockning för.

    > [!NOTE]  
    > Om du väljer ett dokument som redan har instruktioner för alla dess rader, [!INCLUDE [prod_short](includes/prod_short.md)] informerar dig om att det inte finns något att hantera. För att kombinera de redan skapade lagerplockningsinstruktionerna till en plockningsinstruktion, radera de enskilda lagerplockningarna först.

4. Fyll i fältet **Sorteringsmetod** för att sortera raderna som du vill ha dem.  

    > [!NOTE]  
    > Hur raderna sorteras i förslaget överförs inte automatiskt till plockningsinstruktionen. Däremot finns samma sorteringsverktyg tillgängliga, tillsammans med lagerplatsordning. Du kan enkelt återskapa ordningen på raderna du planerar i kalkylbladet när du skapar plockningsinstruktionerna eller genom att sortera i plockningsinstruktionerna.

5. Fyll i fältet **Ant. att hantera**. Välj åtgärden **Fyll i auto. ant. att hantera** eller fyll i fälten manuellt.  

    På sidan visas de tillgängliga kvantiteterna för lagerplatser för direktutleverans, vilket är användbart när du planerar arbetstilldelningar i direktutleveranser. [!INCLUDE[prod_short](includes/prod_short.md)] föreslår alltid en plockning från en lagerplats för direktutleverans först.

6. Du kan redigera raderna manuellt efter behov. Du kan också ta bort en del rader för att skapa en välja mer effektivt. Om det till exempel finns rader med artiklar på lagerställen för direktutleveranser kanske du vill skapa en plockning för alla rader. Artiklarna för direktutleverans plockas, tillsammans med övriga artiklar i källdokument, och lagerställena för direktutleveranser får därmed plats för fler inkommande artiklar.

    > [!NOTE]  
    >  Rader som tas bort tas endast bort från det här förslaget, inte från välj urvalslista.  

7. Välj åtgärden **Skapa plockning**. Sidan **Skapa plockning** öppnas, där du kan lägga till mer information till valet.  

    Ange hur plockrader ska kombineras i plockdokumentet genom att välja ett av följande alternativ.  

    |Alternativ|Beskrivning|
    |-|-|
    |Per dist.lagerdokument Dokument|Skapa separata plockningsdokument för kalkylarksraderna med samma distributionslagerkälldokumentet.|
    |Per Kund/Lev./Lagerst.|Skapa separata plockningsdokument för varje kund (projekt)|
    |Per artikel|Skapa separata plockningsdokument för varje artikel i plockningsförslaget.|
    |Per från zon|Skapa separata plockningsdokument för varje zon som du tar artiklarna från.|
    |Per lagerplats|Skapa separata plockningsdokument för varje lagerplats som du tar artiklarna från.|
    |Per förfallodatum|Skapa separata plockningsdokument för källdokument som har samma förfallodatum.|

    Ange hur du skapar plockningsdokument genom att välja bland följande alternativ.  

    |Alternativ|Beskrivning|
    |-|-|
    |Max. Nr. av plockningsrader|Skapar plockningsdokument som inte har fler än radnummer än som ställts in i varje dokument.|
    |Max. Nr. av plock.källdok.|Skapar plockningsdokument som inte täcker antalet källdokument som ställts in.|
    |Tilldelat användar-ID|Skapar plockningsdokument enbart för förslagsrader som tilldelats den valda lagerpersonalen.|
    |Sorteringsmetod för plock.rader|Välja bland de tillgängliga alternativen för att sortera rader i den nya plockningsdokumentet.|
    |Sätt brytenhetsfilter|Döljer mellanliggande plockningsrader för brytenheter när en större måttenhet konverteras till en mindre måttenhet och plockas.|
    |Fyll inte i ant. att hantera|Lämnar fältet **Ant. att hantera** tomt på de skapade plockningsraderna.|
    |Skriv ut plockning|Skriver ut plockningsdokumenten, när de skapas. Du kan även skriva ut från skapade plockningsdokumenten.|

8. Välj **OK**.  

## <a name="to-pick-items-for-a-productions-order-assembly-order-job"></a>Så här plockar du artiklar för en produktionorder, monteringsorder, projekt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **plockningar** och väljer sedan relaterad länk.  

    Om du vill arbeta med en viss plockning väljer du plockningen från listan eller filtrerar listan för att söka efter de plockningar som har tilldelats dig. Öppna plockningskortet.  
2. Om **Tilldelat användar-ID** är tomt, anger du ID för att identifiera själv om det behövs.  
3. Plocka artiklar.  

    Om distributionslagret har konfigurerats att använda lagerställen, då artikelns standardlagerställen används för att föreslå var du vill hämta artiklar från. Instruktionerna innehåller minst två separata rader för Ta och placera-åtgärder.  

    Operationsområden som t.ex. produktionsgolv kan ha en standardlagerplats för komponenterna som behövs. Om så är fallet läggs standardlagerplatskoden till i distributionslagerplockdokumentet för att ange var artiklarna ska placeras. Mer information finns i verktygstipsen för **Till prod.-lagerplats – kod**, **Till monteringsplats – kod**, **Lagerplatskod för projekt**.

    Om lagret är distributionslager för att använda riktad borttagning och plockning, används lagerplatsordning för att beräkna de bästa lagerplatserna att plocka från. Dessa lagerplatser föreslås på plockningsraderna. Instruktionerna innehåller minst två separata rader för Ta och placera-åtgärder.  

    * Den första raden, med **Ta** i fältet **Åtgärdstyp**, anger var artiklarna finns i inleveransområdet. Om du skickar ett stort antal artiklar på en utleveransraden, kanske du måste plocka artiklarna i flera lagerplatser, så det finns en Ta-rad för varje lagerplats.
    * Nästa rad, med fältet **Plats** i **Åtgärdstyp**, anger var du måste placera artiklarna i distributionslager. Du kan inte ändra zon- och lagerplatsfältet på den här raden.

    > [!NOTE]
    > Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om den utsedda lagerplatsen är full, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.

      Du kan sortera plockningsraderna efter flera villkor, till exempel efter artikel, hyllnummer eller förfallodatum. Sortering kan hjälpa till att optimera processen för artikelinförsel, till exempel:

    * Om raderna för Ta och Placera för varje leveransrad inte visas direkt efter varandra och det är så du vill att de ska visas, kan du sortera raderna genom att välja **Artikel** i fältet **Sorteringsmetod**.  
    * Om lagerplatsordning återspeglar lagrets fysiska layout, använd sorteringsmetoden **Lagerplatsordning** för att organisera arbetet efter lagerplatser.

  > [!NOTE]  
  > Raderna sorteras i stigande ordning efter det valda kriteriet. Om du sorterar efter dokument görs sorteringen först efter dokumenttyp baserat på fältet **Källdokument för distributionslageraktivitet**. Om du sorterar efter leverans görs sorteringen först efter destinationstyp baserat på fältet **Destinationstyp för distributionslager**.

4. När du har plockat och placerat artiklarna i produktions-, monterings- eller projektområdet eller behållaren väljer du åtgärden **Registrera plockning**.  

    Du kan nu ta med artiklarna till respektive område och bokföra användningen eller förbrukningen av de plockade komponenterna genom att bokföra förbrukningsjournal, monteringsorder eller projektjournal. Följande artiklar ger mer information:

    * [Så här registrerar du förbrukning och utflöde för en utsläppt produktionsorderrad](production-how-to-register-consumption-and-output.md)
    * [Montera artiklar](assembly-how-to-assemble-items.md)
    * [Registrera förbrukning eller användning för projekt](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Bokföring av produktionskomponenter i en avancerad distributionslagerkonfiguration

Bokföringsmetoder påverkar flödet av komponenter i produktionen. Läs mer i [Bokföra komponenter utifrån operationens utflöde](production-how-to-flush-components-according-to-operation-output.md). Beroende på vilken bokföringsmetod som valts kan du plocka komponenter för produktion på följande sätt:

* Använd ett dokument för **Distributionslagerplockning** för att registrera plockning för artiklar som använder **manuell** bokföringsmetod. Du måste registrera förbrukning separat. Läs mer på [Batch-bokföra produktionsförbrukning](production-how-to-post-consumption.md).
* Använd ett dokument för **Distributionslagerplockning** för att registrera plockning för artiklar som använder bokföringsmetoden **Plocka + framåt**, **Plocka + bakåt**. Förbrukningen av komponenterna sker automatiskt antingen när du ändrar produktionsorderns status eller startar eller avslutar en åtgärd. Alla nödvändiga komponenter måste vara tillgängliga. Annars stoppas bokförs förbrukning som stoppas för den komponenten.
* Använd ett dokument för **Dist.lager transport** utan en hänvisning till ett källdokument eller andra sätt att registrera rörelsen av komponenter som använder bokföringsmetoden **Framåt** eller **Bakåt**. Komponenterna förbrukas automatiskt antingen när du ändrar produktionsorderns status eller startar eller avslutar en åtgärd. Alla nödvändiga komponenter måste vara tillgängliga. Annars stoppas bokförd förbrukning för den komponenten. Läs mer på [Flytta artiklar](warehouse-move-items.md).

### <a name="example"></a>Exempel

Du har en produktionsorder för 15 STYCK av artikeln SP-SCM1004. En del av artiklarna i komponentlistan måste bokföras manuellt i en förbrukningsjournal. Andra artiklar kan plockas och bokföras automatiskt med hjälp av bokföringsmetoden **plocka + bakåt**.  

Följande steg beskriver de åtgärder som olika användare gör och det relaterade svaret:  

1. Produktionsledaren släpper produktionsordern. Artiklar med bokföringsmetoden **Framåt** och utan verksamhetsföljdlänk dras av från den öppna produktionslagerplatsen.  
2. Produktionsledare väljer åtgärden **Skapa dist.lagerplockning** på produktionsordern. Ett plockningdokument för dist.lager skapas för plockning av artiklar med bokföringsmetoderna **Manuell**, **Plocka + bakåt**och **Plocka + framåt**. Dessa artiklar placeras i Till produktion-lagerstället.  
3. Lagerchefen tilldelar plockningar till lagerarbetare.  
4. Lagerarbetaren plockar artiklarna från lämpliga lagerställen och placerar dem i Till produktion-lagerstället eller lagerstället som anges på distributionslagerplockningen. Lagerplatsen kan vara för produktionsgrupp eller maskingrupp.
5. Lagerarbetaren registrerar plockningen. Antalet överförs från plocklagerplatsen till förbrukningslagerplatsen. Fältet **Plockat antal** på komponentlistan för alla plockade artiklar uppdateras.

    > [!NOTE]  
    >  Endast det antal som plockas kan förbrukas.  
6. Maskinoperatorn informerar produktionschefen att slutartiklarna är klara.
7. Produktionsledaren använder förbrukningsjournalen eller produktionsjournalen för att bokföra förbrukningen av komponentartiklarna som använder bokföringsmetoden **Manuell**.
8. Produktionsledaren använder utflödesjournalen eller produktionsjournalen för att bokföra utflödet. Antalet komponent artiklar som använder bokföringsmetoden **Plocka + Framåt** eller **Plocka + Bakåt** med operationsföljdslänkar dras från till produktionslagerplatsen.
9. Produktionschefen ändrar status för produktionsorder till **Avslutad**. Antalet av komponentartiklarna som använder bokföringsmetoden **Bakåt** dras av från öppna produktionslagerplatsen och antalet av komponentartiklarna som använder bokföringsmetoden **Plocka + bakåt** och ingen operationsföljdslänk dras av från till produktion-lagerplatsen.  

Följande illustration visas när fältet **Lagerställeskod** på komponentlistan fylls enligt inställningen för lagerstället eller maskin-/produktionsgruppen.  

:::image type="content" source="media/binflow.png" alt-text="Översikt över när och hur fältet Lagerplatskod fylls i.":::

## <a name="make-to-order-mto-production-components-in-an-advanced-warehouse-configuration"></a>Produktionskomponenter för Tillverka-Mot-Order i en avancerad distributionslagerkonfiguration

I scenarier där en producerad vara består av råvaror och halvfärdiga artiklar med tillverkningspolicyn inställd på **Tillverka-mot-order** kommer distributionslagerplockning för dessa halvfärdiga komponenter läggas till i samma produktionsorder med fältet **Planeringsnivåkod** ifylld. Det förväntas att halvfärdiga artiklar är tillgängliga för konsumtion omedelbart och behöver inte plockas så att de inte ingår i distributionslagerplockdokumentet. De skapade distributionslagerplockningarna innehåller endast råmaterial för producerade artiklar och halvfärdiga artiklar.

Om det däremot finns halvfärdiga artiklar i lager föreslår planeringssystemet att du förbrukar dem i stället för att producera hela kvantiteten. En producerad artikel kräver till exempel fem halvfärdiga komponenter, men tre finns redan i lager. I det här fallet visas fem halvfärdiga artiklar i produktionsorderkomponenterna, men endast två produceras i samma produktionsorder som en separat produktionsorderrad.
En sådan inställning är inte kompatibel med lagerplockning och beroende på frekvensen måste du antingen ändra tillverkningsprincipen för sådana halvfärdiga artiklar till **Tillverka-mot-lager** eller manuellt dela upp produktionsorderkomponentraden när du behöver plocka de halvfärdiga artiklarna som producerats tidigare.


## <a name="see-also"></a>Se även

- [Hantera lager](inventory-manage-inventory.md)  
- [Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
- [Monteringshantering](assembly-assemble-items.md)  
- [Översikt över hantering av distributionslager](design-details-warehouse-management.md)
- [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
