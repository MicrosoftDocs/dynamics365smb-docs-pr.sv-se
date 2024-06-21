---
title: Bokföra komponenter utifrån operationens utflöde
description: I den här artikeln beskrivs hur man spolar komponenter enligt verksamhetens utflöde och andra involverade bokföringsmetoder.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="flush-components-according-to-operation-output"></a>Bokföra komponenter utifrån operationens utflöde
Du kan definiera olika bokföringsstrategier för att automatisera registrering av förbrukning av komponenter. 

Den här funktionen är användbar för följande:  

- **Lagervärdering**

    Värdetransaktioner för förbrukning och utflöde har skapats parallellt, i takt med att produktionsordern fortskrider. Utan verksamhetsföljdslänkkoder minskar lagervärdet när utflödet bokförs och ökar sedan vid en senare tidpunkt, när värdet för komponentförbrukning bokförs tillsammans med färdig produktionsorder.  
- **Lagerdisposition**

    Med tidsfasad förbrukningsbokföring, är tillgängligheten till komponentartiklarna mer uppdaterad, vilket är viktigt för att underhålla det interna saldot mellan tillgång och efterfrågan. Utan verksamhetsföljdslänkkoder kan andra behov av komponenten tro att den är tillgänglig så länge det finns en väntande försenad förbrukningsbokföring.  
- **Just-in-Time**

    Med möjligheten att anpassa produkter till pågående kundförfrågningar kan du reducera kassation genom att se till att arbets- och systemändringar endast görs när det behövs.  

- **Minimera datainmatning**

    Med möjligheten att automatiskt bokföra en operation kan hela registreringsprocessen för förbrukning och utflöde automatiseras. Nackdelen med att använda automatisk bokföring är att du kanske inte på ett korrekt sätt registrerar, eller ens är medveten om, kassation.

## <a name="automatic-consumption-posting-flushing-methods"></a>Metoder för automatisk bokföring av förbrukning

- Bokföra hela ordern framåt  
- Bokföring framåt efter operation  
- Bokföring bakåt efter operation  
- Bokföra hela ordern bakåt  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatisk rapportering – Bokför hela ordern framåt
Om du bokför hela produktionen framåt när arbetet börjar, är beteendet hos programmet liknande det vid manuell förbrukning. Den största skillnaden är att förbrukningen sker automatiskt.  

- Hela innehållet i produktionsstrukturen förbrukas och dras ifrån lagret när den släppta produktionsordern uppdateras.  
- Förbrukningskvantiteten är den kvantitet per montering som anges i produktionsstrukturen multiplicerat med antalet överordnade artiklar som du tillverkar.  
- Du behöver inte registrera någon information i förbrukningsjournalen om alla artiklar ska bokföras.  
- När artiklar förbrukas från lagret, spelar det inte någon roll när utflödesjournaltransaktionerna genomförs eftersom utflödesjournalen inte påverkar den här typen av förbrukningsbokföring.  
- Inga operationsföljdslänkkoder kan anges.  

Bokföra en hel order framåt kan användas i produktionsmiljöer med:  

-   Ett lågt antal fel  
-   Ett lågt antal operationer  
-   Hög komponentförbrukning i tidiga operationer  

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatisk rapportering – Bokföring framåt efter operation
Med bokföring efter operation, kan du dra av lager under en särskild operation i operationsföljden för den överordnade artikeln. Material kopplas till operationsföljden med hjälp av operationsföljdslänkkoder, som motsvarar de operationsföljdslänkkoder som tillämpas på komponenter i produktionsstrukturen.  

Bokföring sker när operationen som har samma kod till verksamhetsföljdlänken startas. Startad betyder att någon aktivitet registreras i utflödesjournalen för operationen. Och den aktiviteten kanske är att omställningstiden anges.  

Det belopp som bokförs gäller för det antal per montering som har angetts i produktionsstrukturen multiplicerat med antalet överordnade artiklar som tillverkas (förväntat antal).  

Den här metoden är lämpligast när det finns många operationer och vissa komponenter inte behövs förrän sent i monteringssekvensen. Om du använder JIT (Just-in-Time – precis i tid) kanske inte ens artiklarna finns i lager när produktionen påbörjas.  

Material kan förbrukas under operationer genom att använda operationsföljdslänkkoder. Vissa komponenter kanske inte används förrän i de sista monteringsoperationerna och ska inte tas ut ur lagret förrän det är dags.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatisk rapportering – Bokföring bakåt efter operation
När du använder metoden Bokföring bakåt efter operation, registreras förbrukning när operationen har bokförts i utflödesjournalen.  

Fördelen med den här metoden är att antalet överordnade delar som slutförts i operationen är känt.  

Material i produktionsstrukturen kopplas till operationsföljdsposterna med hjälp av operationsföljdslänkkoder. Bokföring bakåt utförs när en operation med en särskild operationsföljdslänkkod bokförs med ett färdigställt antal.  

Bokföringsbeloppet gäller för det antal per montering som har angetts i produktionsstrukturen multiplicerat med antalet överordnade artiklar som bokfördes som utflödeantal i operationen. Detta antal kanske inte stämmer överens med det förväntade antalet.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatisk rapportering – Bokför hela ordern bakåt
Operationsföljdslänkkoder används inte för den här rapporteringsmetoden.  

Inga komponenter plockas förrän statusen för den släppta produktionsordern ändras till *Färdig*. Bokföringsbeloppet är det antal per montering som anges i produktionsstrukturen multiplicerat med antalet överordnade artiklar som slutfördes och överfördes till lagret.  

Vid bokföring bakåt måste hela produktionsordern ha samma inställning som vid bokföring framåt: Rapporteringsmetoden måste anges till bakåt på varje artikelkort för alla artiklar inom den överordnade strukturen som ska rapporteras. Dessutom måste alla verksamhetsföljdslänkkoder tas bort från produktionsstrukturen. 



Om t. ex. en produktionsorder för att kunna producera 800 meter kräver 8 kg av en komponent så, när du bokför 200 meter som utflöde, bokförs 2 kg automatiskt som förbrukning. Du kan uppnå det genom att kombinera metoden för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen. För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**. Om du definierar verksamhetsföljdslänkkoder också utförs beräkning och bokföring när varje operation har slutförts, och antal, som faktiskt förbrukades i operationen, bokförs. Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Bokföra komponenter utifrån operationens utflöde

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Redigera**.  
3.  På snabbfliken **Återanskaffning**, i fältet **Bokföringsmetod**, markera **Bakåt**.  

    > [!NOTE]  
    >  Välj **Plocka + bakåt** om komponenten ska användas på ett lagerställe som har skapats för dirigerad artikelinförsel och plockning.  

4.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Operationsföljder** och väljer sedan relaterad länk.  
5.  Definiera verksamhetsföljdslänkkoder för varje operation som förbrukar komponenten. Mer information finns i [Skapa verksamhetsföljder ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Använd inte samma routningslänk för olika operationer i operationsföljden, eftersom det leder till registrering av förbrukning av komponent för varje länkad operation.  
6.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Prod.struktur** och väljer sedan relaterad länk.  
7.  Definiera verksamhetsföljdslänkkoder från varje instans av komponenten till operationen där den förbrukas.

Förbrukningen bokförs automatiskt när du registrerar utdata. Mer information finns i [Batch-bokför utflöde och körtider](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Bokföringsmetoder

I följande tabell beskrivs de tillgängliga bokföringsmetodalternativen som du kan ange korten **Artikel** och korten **Lagerställeenhet**.

|Alternativ|Beskrivning|
|------------|-------------|  
|Manuell|Kräver att du anger och bokför förbrukningen manuellt i förbrukningsjournalen.|
|Framåt|Bokför förbrukningen automatiskt enligt produktionsorderkomponentraderna. <br><br>Som standard sker bokföringen av komponentförbrukning när du ändrar statusen för en produktionsorder till **Släppt**. Om du använder kodfälten **Operationsföljdslänk** på produktionsorderkomponentrader, kommer bokföringen ske per operation när operationen startas. För mer information, se [Så här skapar du en operationsföljdslänk](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Obs**<br>För bokföring framåt baseras operation-specifik bokföring som du erhåller med operationsföljdslänkkoder på förväntade kvantiteter som har definierats på komponentraden. Visa beskrivning av **Bakåt** i den här artikeln för information om operation-specifik bokföring som baseras på faktiskt utflöde.<br><br>Om lagerstället eller resurserna där den här komponenten förbrukas har upprättats med en standardlagerplatsstruktur, förbrukas **Öppen prod.lagerplats kod**. Mer information finns i [så här: ställa in grundläggande dist.lager med operationsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Viktigt!** <br>Bokföring framåt uppstår också när du klickar på **Uppdatera** på en släppt nyskapad produktionsorder. I dessa direkt skapade utsläppta produktionsorder, kan du inte ändra informationen om lagerplats, eftersom produktionsorderkomponentraderna skapas när du uppdaterar ordern och komponenterna samtidigt bokförs framåt. Därför, om du vill ändra information om lagerplatsen i produktionsorderkomponentrader före bokföring framåt uppstår, måste order skapas med *planerade* eller *fast planerad* status.|
|Bakåt|Beräknar och bokför förbrukningen automatiskt enligt produktionsorderkomponentraderna.<br><br> Som standard sker beräkningen och bokföringen av komponentförbrukning när du ändrar statusen för en utsläppt produktionsorder till **Släppt**. Om du använder **Operationsföljdslänkkod** på produktionsorderkomponentrader, kommer beräkningen och bokföringen ske när operationen startas.<br><br> **Obs** <br>Kopplingskoder för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen. Mer information finns i [så här: bokföra komponenter enligt operationens utflöde](#to-flush-components-according-to-operation-output).<br><br> Om platsen och maskingrupp där den här komponenten förbrukas har upprättats med en standardlagerplatsstruktur, förbrukas **Öppen prod.lagerplats kod**.|
|Plocka + framåt|Samma som för bokföringsmetoden framåt, förutom att den bara fungerar för lagerställen som använder antingen avancerad lagerkonfiguration eller grundläggande lagerkonfiguration med obligatoriska lager.<br><br> Förbrukning beräknas och bokförs från lagerplatsen som definieras i **Till prod.-lagerplats – kod** på lagerstället eller maskingruppen, när komponenten har plockats från distributionslagret.<br><br> **Obs** <br>Om en komponent har upprättats med plocka + metoden bokföringsmetoden Framåt, kan den inte ha en operationsföljdkopplingskod till en operation som har upprättats med bokförs framåt leveransvillkor. Komponenten skulle då bokföras automatiskt framåt när operationen startas, vilket gör det omöjligt att begära aktiviteten plocka.|
|Plocka + bakåt|Samma som för bokföringsmetoden bakåt, förutom att den bara fungerar för lagerställen som använder antingen avancerad lagerkonfiguration eller grundläggande lagerkonfiguration med obligatoriska lager.<br><br> Förbrukning beräknas och bokförs från lagerplatsen som definieras i **Till prod.-lagerplats – kod** på lagerstället eller maskingruppen, när komponenten har plockats från distributionslagret.|

## <a name="see-also"></a>Se även

[Skapa produktionsstrukturlistor](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
