---
title: Designdetaljer – Bokföring av produktionsorder | Microsoft Docs
description: Precis som för monteringsorderbokföring konverteras de förbrukade komponenterna och den använda maskintiden och utflödas som producerad artikel när produktionsordern har färdigställts.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designdetaljer: Bokföring av produktionsorder
Precis som för monteringsorderbokföring konverteras de förbrukade komponenterna och den använda maskintiden och utflödas som producerad artikel när produktionsordern har färdigställts. Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md) Däremot är kostnadsflödet för monteringsorder mindre komplicerat, särskilt eftersom bokföring av monteringskostnad endast uppstår en gång och därför inte genererar lager för produkter i arbete.


Transaktioner som uppstår under produktionsprocessen kan spåras genom efterföljande etapper:  

1.  Inköp av material och andra produktionsinflöden.  
2.  Konvertering till produkter i arbete.  
3.  Konvertering till färdiga varor i lager.  
4.  Försäljning av färdigvaror.  

Förutom vanliga lagerkonton måste därför produktionsföretaget fastställa tre olika lagerkonton för att registrera transaktioner under olika stadier i produktionen.  

|Lagerkonto|Description|  
|-----------------------|---------------------------------------|  
|**Råmaterialkonto**|Innehåller kostnaden för råmaterial som köps men ännu inte har överförts till produktionen. Saldot i kontot Råmaterial anger kostnaden för råmaterial som finns i lager.<br /><br /> När råmaterial flyttas till produktionsavdelningen överförs kostnaden för råmaterial från råmaterialkontot till PIA-kontot.|  
|**PIA-konto Produkter i arbete**|Ackumuleras kostnaderna som uppstått under produktionen i bokföringsperioden. PIA-kontot debiteras för kostnaden för råmaterial som har överförts från råmateriallagret, kostnaden för utfört direkt arbete och produktionsomkostnaderna som uppstått.<br /><br /> PIA-kontot krediteras för den totala produktionskostnaden för enheter som slutförs i fabriken och överförs till distributionslagret för färdiga varor.|  
|**Färdigvaror – konto**|Det här kontot innehåller den totala tillverkningskostnaden för enheter som är färdiga men ännu inte har sålts. Vid tidpunkten för försäljningen överförs kostnaden för sålda enheter från kontot för färdiga varor till kontot för kostnaden för sålda varor.|  

Lagervärdet beräknas genom att spåra kostnaderna för alla ökningar och minskningar, uttryckt av följande ekvation.  

* lagervärde = startsaldo för lager + värde på alla ökningar – värde på alla minskningar  

Beroende på typen av lager representeras ökningar och minskningar av olika transaktioner.  

||Ökningar|Minskningar|  
|-|---------------|---------------|  
|**Råmateriallager**|-   Nettoinköp av material<br />-   Utflöde av delprodukter<br />-   Negativ förbrukning|Materialförbrukning|  
|**PIA-lager**|-   Materialförbrukning<br />-   Kapacitetsförbrukning<br />-   Produktionsomkostnader|Utflöde av slutobjekt (kostnaden för tillverkade varor)|  
|**Färdiga varor i lager**|Utflöde av slutobjekt (kostnaden för tillverkade varor)|-   Försäljning (kostnad för sålda varor)<br />-   Negativt utflöde|  
|**Råmateriallager**|-   Nettoinköp av material<br />-   Utflöde av delprodukter<br />-   Negativ förbrukning|Materialförbrukning|  

Värdena av ökningar och minskningar registreras i de olika typerna av tillverkat lager på samma sätt som för inköpt lager. Varje gång en transaktion för lagerökning eller lagerminskning sker, skapas en artikeltransaktion och en motsvarande redovisningstransaktion för beloppet. Mer information finns i [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)  

Även om värdet på av transaktioner som är kopplade till inköpta varor bokförs endast som artikeltransaktioner med relaterade värdetransaktioner, bokförs transaktioner som är kopplade till producerade artiklar som kapacitetstransaktioner med relaterade värdetransaktioner, utöver artikeltransaktionerna.  

## Bokföringsstruktur  
När du bokför produktionsorder till PIA-lagret avser utflöde, förbrukning och kapacitet.  

Följande diagram visar de berörda bokföringsrutinerna i kodenhet 22.  

![Bokföringsrutiner för produktionsorder.](media/design_details_inventory_costing_14_production_posting_1.png "Bokföringsrutiner för produktionsorder")  

Följande diagram visar anslutningarna mellan de resulterande transaktionerna och kostnadsbärarna.  

![Produktionstransaktionsflöde.](media/design_details_inventory_costing_14_production_posting_2.png "Produktionstransaktionsflöde")  

Kapacitetstransaktioner beskriver kapacitetsförbrukningen i termer av tidsenheter, medan den relaterade värdetransaktionen beskriver värdet för den aktuella kapacitetsförbrukningen.  

Artikeltransaktionen beskriver materialförbrukningen eller utflödet i termer av antal, medan den relaterade värdetransaktionen beskriver värdet för denna specifika materialförbrukning eller utflöde.  

En värdetransaktion som beskriver PIA-lagervärdet kan kopplas till en av följande kombinationer av kostnadsbärare:  

-   En produktionsorderrad, en produktions – eller maskingrupp och en kapacitetstransaktion.  
-   En produktionsorderrad, en artikel och en artikeltransaktion.  
-   Endast en en produktionsorderrad  

För mer information om hur kostnader från produktion och montering bokförs i redovisningen, se [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md).  

## Kapacitetsbokföring  
Bokföring av utflöde från den sista produktionsorderns verksamhetsföljdsrad resulterar i en kapacitetstransaktion för slutobjektet, förutom dess lagerökning.  

 Kapacitetstransaktionen är en post för den tid som spenderades för att producera artikeln. Den relaterade värdetransaktionen beskriver ökningen av PIA-lagervärdet, som är värdet för konverteringkostnaden. Mer information finns i ”från fönstret kapacitetstransaktioner” i [Designdetaljer: konton i redovisningen](design-details-accounts-in-the-general-ledger.md).  

## Kostnadskalkylering för tillverkningsorder  
 För att kontrollera lager- och produktionskostnader måste ett produktionsföretag mäta kostnaden för produktionsordern, eftersom den förutbestämda standardkostnaden för varje producerad artikel ska kapitaliseras i balansräkningen. Se [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md) för information om varför producerade artiklar använder värderingsprincipen.  

> [!NOTE]  
>  I miljöer som inte använder värderingsprincipen Standard, kapitaliseras den faktiska kostnaden istället för standardkostnaden för producerade artiklar i balansräkningen.  

Den faktiska kostnaden för en produktionsorder består av följande kostnadskomponenter:  

-   Naturlig materialkostnad  
-   Faktisk kapacitetskostnad eller underleverantörskostnad  
-   Produktionsomkostnader  

De här faktiska kostnaderna bokförs i produktionsordern och jämförs med standardkostnaden för att beräkna avvikelser. Varianser beräknas för varje artikelkostnadkomponent: råmaterial, kapacitet, underleverantör, kapacitetsomkostnad och omkostnad för produktion. Avvikelserna kan analyseras för att fastställa problem, till exempel överdrivet spill i bearbetningen.  

I standardkostnadmiljöer baseras värderingen av en produktionsorder på följande mekanism:  

1.  När den sista verksamhetsföljden har bokförts, bokförs produktionsorderkostnaden i artikeltransaktionen och anges till den förväntade kostnaden.  

    Kostnaden är lika med utflödesantalet som bokförs i utflödesjournalen multiplicerat med standardkostnaden som kopieras från artikelkortet. Kostnaden behandlas som förväntade kostnader tills produktionsordern är färdig. Mer information finns i [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md)  

    > [!NOTE]  
    >  Det skiljer sig från monteringsorderbokföring, som alltid bokför faktiska kostnader. Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  
2.  När produktionsorder ställs in till **Färdig**, d.v.s ordern faktureras genom att köra batchjobbet **Justera kost. – artikeltrans.**. Det medför att den totala kostnaden för ordern beräknas baserat på standardkostnaden för de förbrukade materialen och kapaciteten. Skillnaden mellan det beräknade standardkostnaderna och de faktiska produktionskostnaderna beräknas och bokförs.  

## Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md) [Finans](finance.md)  
 [Arbeta med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]