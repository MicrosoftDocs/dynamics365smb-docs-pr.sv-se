---
title: Bokföra komponenter utifrån verksamhetens utflöde
description: För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till Färdig.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d1448b9105426103d70abfb820bd38b6adb41db8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779259"
---
# <a name="flush-components-according-to-operation-output"></a>Bokföra komponenter utifrån verksamhetens utflöde
Du kan definiera olika bokföringsstrategier för att automatisera registrering av förbrukning av komponenter. 

Om t. ex. en produktionsorder för att kunna producera 800 meter kräver 8 kg av en komponent så, när du bokför 200 meter som utflöde, bokförs 2 kg automatiskt som förbrukning. 

Den här funktionen är användbar för följande:  

- **Lagervärdering**

    Värdetransaktioner för förbrukning och utflöde har skapats parallellt, i takt med att produktionsordern fortskrider. Utan verksamhetsföljdslänkkoder minskar lagervärdet när utflödet bokförs och ökar sedan vid en senare tidpunkt, när värdet för komponentförbrukning bokförs tillsammans med färdig produktionsorder.  
- **Lagerdisposition**

    Med tidsfasad förbrukningsbokföring, är tillgängligheten till komponentartiklarna mer uppdaterad, vilket är viktigt för att underhålla det interna saldot mellan tillgång och efterfrågan. Utan verksamhetsföljdslänkkoder kan andra behov av komponenten tro att den är tillgänglig så länge det finns en väntande försenad förbrukningsbokföring.  
- **Just-in-Time**

    Med möjligheten att anpassa produkter till pågående kundförfrågningar kan du reducera kassation genom att se till att arbets- och systemändringar endast görs när det behövs.  

Du kan uppnå det genom att kombinera metoden för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen. För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**. Om du definierar verksamhetsföljdslänkkoder också utförs beräkning och bokföring när varje operation har slutförts, och antal, som faktiskt förbrukades i operationen, bokförs. Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Bokföra komponenter utifrån operationens utflöde

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan tillhörande länk.  
2.  Välj åtgärden **Redigera**.  
3.  På snabbfliken **Återanskaffning**, i fältet **Bokföringsmetod**, markera **Bakåt**.  

    > [!NOTE]  
    >  Välj **Plocka + bakåt** om komponenten ska användas på ett lagerställe som har skapats för dirigerad artikelinförsel och plockning.  

4.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **verksamhetsföljder** och välj sedan relaterad länk.  
5.  Definiera verksamhetsföljdslänkkoder för varje operation som förbrukar komponenten. Mer information finns i [Skapa verksamhetsföljder ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Använd inte samma routningslänk för olika operationer i operationsföljden, eftersom det leder till registrering av förbrukning av komponent för varje länkad operation.  
6.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Prod.struktur** och välj sedan relaterad länk.  
7.  Definiera verksamhetsföljdslänkkoder från varje instans av komponenten till operationen där den förbrukas.

Förbrukningen bokförs automatiskt när du registrerar utdata. Mer information finns i [Batch-bokför utflöde och körtider](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Bokföringsmetoder

I följande tabell beskrivs de tillgängliga bokföringsmetodalternativen som du kan ange korten **Artikel** och korten **Lagerställeenhet**.

|Alternativ|Beskrivning|
|------------|-------------|  
|Manuell|Kräver att du anger och bokför förbrukningen manuellt i förbrukningsjournalen.|
|Framåt|Bokför förbrukningen automatiskt enligt produktionsorderkomponentraderna. <br><br>Som standard sker bokföringen av komponentförbrukning när du ändrar statusen för en produktionsorder till **Släppt**. Om du använder kodfälten **Operationsföljdslänk** på produktionsorderkomponentrader, kommer bokföringen ske per operation när operationen startas. För mer information, se [Så här skapar du en operationsföljdslänk](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Obs**<br>För bokföring framåt baseras operation-specifik bokföring som du erhåller med operationsföljdslänkkoder på förväntade kvantiteter som har definierats på komponentraden. Visa beskrivning av **Bakåt** i det här avsnittet för information om operation-specifik bokföring som baseras på faktiskt utflöde.<br><br>Om lagerstället eller resurserna där den här komponenten förbrukas har upprättats med en standardlagerplatsstruktur, förbrukas **Öppen prod.lagerplats kod**. Mer information finns i [så här: ställa in grundläggande dist.lager med operationsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Viktigt!** <br>Bokföring framåt uppstår också när du klickar på **Uppdatera** på en släppt nyskapad produktionsorder. I dessa direkt skapade utsläppta produktionsorder, kan du inte ändra informationen om lagerplats, eftersom produktionsorderkomponentraderna skapas när du uppdaterar ordern och komponenterna samtidigt bokförs framåt. Därför, om du vill ändra information om lagerplatsen i produktionsorderkomponentrader före bokföring framåt uppstår, måste order skapas med *planerade* eller *fast planerad* status.|
|Bakåt|Beräknar och bokför förbrukningen automatiskt enligt produktionsorderkomponentraderna.<br><br> Som standard sker beräkningen och bokföringen av komponentförbrukning när du ändrar statusen för en utsläppt produktionsorder till **Släppt**. Om du använder **Operationsföljdslänkkod** på produktionsorderkomponentrader, kommer beräkningen och bokföringen ske när operationen startas.<br><br> **Obs** <br>Kopplingskoder för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen. Mer information finns i [så här: bokföra komponenter enligt operationens utflöde](#to-flush-components-according-to-operation-output).<br><br> Om platsen och maskingrupp där den här komponenten förbrukas har upprättats med en standardlagerplatsstruktur, förbrukas **Öppen prod.lagerplats kod**.|
|Plocka + framåt|Samma som för bokföringsmetoden Framåt, fast den fungerar bara för lagerställen som använder dirigerad artikelinförsel och plockning.<br><br> Förbrukning beräknas och bokförs från lagerplatsen som definieras i **Till prod.-lagerplats - kod** på lagerstället eller maskingruppen, när komponenten har plockats från distributionslagret.<br><br> **Obs** <br>Om en komponent har upprättats med plocka + metoden bokföringsmetoden Framåt, kan den inte ha en operationsföljdkopplingskod till en operation som har upprättats med förrensning leveransvillkor. Komponenten skulle då bokföras automatiskt framåt när operationen startas, vilket gör det omöjligt att begära aktiviteten plocka.|
|Plocka + bakåt|Samma som för bokföringsmetoden Bakåt, fast den fungerar bara för lagerställen som använder dirigerad artikelinförsel och plockning.<br><br> Förbrukning beräknas och bokförs från lagerplatsen som definieras i **Till prod.-lagerplats - kod** på lagerstället eller maskingruppen, när komponenten har plockats från distributionslagret.|

## <a name="see-also"></a>Se även

[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
