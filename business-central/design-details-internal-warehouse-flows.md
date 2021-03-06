---
title: Designdetaljer – Interna distributionslagerflöden | Microsoft Docs
description: Flödet av artiklar mellan lagerställen på ett företags lagerställe centreras på plockning av komponenter och införsel av slutartiklar för monterings- eller produktionsorder och ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 7be0a3907b59a17e6f77e4ae8eb3a36fc62d8f7a
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215134"
---
# <a name="design-details-internal-warehouse-flows"></a>Designdetaljer: Interna distributionslagerflöden
Flödet av artiklar mellan lagerställen på ett företags lagerställe centreras på plockning av komponenter och införsel av slutartiklar för monterings- eller produktionsorder och ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument. Omfattningen och typen av de berörda aktiviteterna varierar mellan grundläggande och avancerad lagerstyrning.  

 Alla interna flöden överlappar vid inkommande eller utgående flöden. Viss av den här överlappningen visas som moment 4 och 5 i de grafiska diagrammen för avancerade inkommande och utgående arbetsflöden. Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Interna flöden i Grundläggande lagerstyrning  
 I grundläggande lagerkonfiguration centreras flödet av artiklar mellan lagerställen inom företag på att plocka komponenter och införsel av slutartiklar för produktion eller monteringsorder och ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument.  

### <a name="flows-to-and-from-production"></a>Flöden till och från produktion  
 Den huvudsakliga integreringen mellan produktionsorder och grundläggande distributionslageraktiviteter representeras av möjligheten att välja produktionskomponenter med sidan **Lagerplockning** eller sidan **Lagerförflyttning**.  

> [!NOTE]  
>  På sidan **Lagerplockning** fönstret bokförs komponentförbrukningen tillsammans med plockbokföringen. Med hjälp av sidan **Lagerförflyttning** registreras bara lagerplatsjusteringar, och ingen bokföring av artikeltransaktion inträffar.  

 Förutom komponenthantering representeras integreringen av möjligheten att införa producerade artiklar via sidan **Lagerinförsel**.  

 Fälten **Till prod.-lagerplats – kod**, **Från prod.lagerplats – kod** och **Öppen prod.lagerplats kod** på lagerställekortet eller maskin-/produktionsgruppkorten definierar standardflöden till och från produktionsområden.  

 Se avsnittet ”Bokföring av produktionskomponenter i distributionslagret” i det här avsnittet om du vill ha mer information om hur komponentförbrukning bokförs från Till-produktionslagerplats eller öppen produktionslagerplats.  

### <a name="flows-to-and-from-assembly"></a>Flöden till och från montering  
 Den huvudsakliga integreringen mellan monteringsorder och grundläggande distributionslageraktiviteter representeras av möjligheten att flytta monteringkomponenter på monteringsområdet.  

 Det finns ingen särskild distributionslagerfunktion för att införsel av monteringsartiklar, men lagerställeskoden på monteringsorderhuvudet kan ställas in till en standardlagerplats för artikelinförsel. Bokföra av monteringsordern fungerar då som att bokföra artikelinförsel. Distributionslageraktiviteten som flyttar monteringsartiklar till distributionslagret kan hanteras på sidan **Interntransport** utan relation till monteringsordern.  

 Följande monteringsflöden finns.  

|Arbetsflöde|Beskrivning|  
|----------|---------------------------------------|  
|Montering mot lager|Komponenterna är nödvändiga på en monteringsorder där utflödet lagras i distributionslagret.<br /><br /> Det här distributionslagerflödet hanteras på sidan **Lagertransport**. En ta-rad anger var att komponenter ska tas. En placeringsrad anger var att komponenter ska placeras.|  
|Montering mot kundorder|Komponenterna är nödvändiga på en monteringsorder som är kopplad till en försäljningsorder som ska levereras när den sålda artikeln har monterats.|  

> [!NOTE]  
>  Om artiklar monteras mot kundorder aktiverar lagerplockningen för den kopplade försäljningsordern en lagerförflyttning för alla berörda monteringskomponenter, inte bara för den sålda artikeln som när du levererar lagerartiklar.  

 Fälten **Till monteringsplats – kod**, **Från monteringsplats – kod** och **Lagerpl.kod för mont. mot lev.** på lagerställekortet definierar standardflöden till och från monteringsområden.  

> [!NOTE]  
>  Fältet **Lagerpl.kod för mont. mot lev.** fungerar som från-monteringslagerplats i scenarier med montering mot kundorder.  

### <a name="ad-hoc-movements"></a>Förflyttningar ad hoc  
 I grundläggande lagerhantering hanteras transport av artiklar från lagerplats till lagerplats utan relation till källdokument på sidan **Interntransport** som fungerar tillsammans med sidan **Lagertransport**.  

 Ett annat sätt att flytta artiklar ad hoc mellan lagerställen är att bokföra positiva transaktioner i fältet **Ny lagerställeskod** på sidan **Artikelgrupperingsjnl**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Interna flöden i Avancerad lagerstyrning  
 I avancerade distributionslagerkonfigurationer centreras flödet av artiklar mellan lagerställen inom företaget på att plocka komponenter och föra in slutartiklar för produktionsorder och plocka komponenter för monteringsorder. Dessutom uppstår interna flöden som ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument.  

### <a name="flows-to-and-from-production"></a>Flöden till och från produktion  
 Den huvudsakliga integreringen mellan produktionsorder och avancerade lageraktiviteter representeras av kan du välja ut produktionskomponenter, på sidan **Distributionslagerplockning** och sidan **Plockningskalkylark**, och möjligheten att införa producerade artiklar via sidan **Dist.lager intern art.införsel**.  

 En annan integreringspunkt i produktionen finns på sidan **Dist.lager transport** tillsammans med sidan Transportkalkylark som du kan använda för att placera komponenter och ta producerade artiklar för släppta produktionsorder.  

 Fälten **Till prod.-lagerplats – kod**, **Från prod.lagerplats – kod** och **Öppen prod.lagerplats kod** på lagerställekortet eller maskin-/produktionsgruppkorten definierar standardflöden till och från produktionsområden.  

 Se avsnittet ”Bokföring av produktionskomponenter i distributionslagret” i det här avsnittet om du vill ha mer information om hur komponentförbrukning bokförs från Till-produktionslagerplats eller öppen produktionslagerplats.  

### <a name="flows-to-and-from-assembly"></a>Flöden till och från montering  
 Den huvudsakliga integreringen mellan monteringsorder och avancerade lageraktiviteter representeras av att kan du välja monteringkomponenter, både med sidan **Distributionslagerplockning** och sidan **Plockningskalkylark**. Den här funktionen fungerar precis som när du plockar komponenter för produktionsorder.  

 Det finns ingen särskild distributionslagerfunktion för att införsel av monteringsartiklar, men lagerställeskoden på monteringsorderhuvudet kan ställas in till en standardlagerplats för artikelinförsel. Bokföra av monteringsordern fungerar då som att bokföra artikelinförsel. Distributionslageraktiviteten som flyttar monteringsartiklar till distributionslagret kan hanteras på sidan **Transportkalkylark** eller sidan **Dist.lager intern art.införsel** utan relation till monteringsordern.  

> [!NOTE]  
>  Om artiklar monteras mot kundorder aktiverar distributionslagerutleveransen för den kopplade försäljningsordern en distributionslagerplockning för alla berörda monteringskomponenter, inte bara för den sålda artikeln som när du levererar lagerartiklar.  

 Fältet **Till monteringsplats – kod** och **Från monteringsplats – kod** på lagerställekortet definierar standardflöden till och från monteringsområden.  

### <a name="ad-hoc-movements"></a>Förflyttningar ad hoc  
 I avancerad lagerhantering hanteras transport av artiklar från lagerplats till lagerplats utan relation till källdokument på sidan **Transportkalkylark** och registreras i fönstret Dist.lager transport.  

## <a name="flushing-production-components-in-the-warehouse"></a>Bokföring av produktionskomponenter i distributionslagret  
 Om komponenter finns angivna på artikelkortet bokförs komponenter som plockas med distributionslagerplockning som förbrukade av produktionsordern när distributionslagerplockningen registreras. Genom att använda metoden **Plocka + framåt** och bokföringsmetoden **Plocka + bakåt** aktiverar plockregistreringen den relaterade förbrukningsbokföringen när den första operationen startar, eller när det sista operationen är klar, kommer.  

 Tänk på följande scenario baserat på [!INCLUDE[prod_short](includes/prod_short.md)]-demosdatabasen.  

 En produktionsorder för 15 STYCK av artikeln LS-100 finns. Några av artiklarna på komponentlistan måste bokföras manuellt i en förbrukningsjournal, och andra artiklar på listan kan plockas och bokföras automatiskt med hjälp av bokföringsmetoden **Plocka + bakåt**.  

> [!NOTE]  
>  **Plocka + framåt** fungerar bara om den andra produktionsverksamhetsföljdsradens operation använder en routningslänkkod. När du släpper en planerad produktionsorder aktiverar bokföring framåt av komponenter som har värdet **Plocka + framåt**. Bokföringen kan inte göras förrän plockningen av komponenterna är registrerad,vilket endast kan göras när ordern släpps.  

 Följande moment beskriver de ingående åtgärderna från olika användare och det relaterade svaret:  

1.  Produktionsledaren släpper produktionsordern. Artiklar med bokföringsmetoden **Framåt** och utan verksamhetsföljdlänkkod dras av från den öppna fabrikslagerstället.  
2.  Produktionsledare väljer knappen **Skapa dist.lagerplockning** på produktionsordern. Ett plockningdokument för dist.lager skapas för plockning av artiklar med bokföringsmetoderna **Manuell**, **Plocka + bakåt** och **Plocka + framåt**. Dessa artiklar placeras i Till produktion-lagerstället.  
3.  Lagerchefen tilldelar plockningar till lagerarbetare.  
4.  Lagerarbetaren plockar artiklarna från lämpliga lagerställen och placerar dem i Till produktion-lagerstället eller lagerstället som anges på distributionslagerplockningen, som kan vara en produktionsgrupp eller maskingrupplagerplats.  
5.  Lagerarbetaren registrerar plockningen. Antalet subtraheras från plocklagerställena och läggs till i förbrukningslagerstället. Fältet **Plockat antal** på komponentlistan för alla plockade artiklar uppdateras.  

    > [!NOTE]  
    >  Endast det antal som plockas kan förbrukas.  

6.  Maskinoperatorn informerar produktionschefen att slutartiklarna är klara.  
7.  Produktionsledaren använder förbrukningsjournalen eller produktionsjournalen för att bokföra förbrukningen av komponentartiklarna som använder bokföringsmetoden **Manuell** eller **Framåt** eller **Plocka + framåt** tillsammans med koderna för verksamhetsföljdslänkar.  
8.  Produktionschefen bokför utflödet av produktionsorder och ändrar status till **Avslutad**. Antalet av komponentartiklarna som använder bokföringsmetoden **Bakåt** dras av från öppna fabrikslagerställen, och antalet av komponentartiklarna som använder bokföringsmetoden **Plocka + bakåt** dras av från till produktion-lagerstället.  

 Följande illustration visas när fältet **Lagerställeskod** på komponentlistan fylls enligt inställningen för lagerstället eller maskin-/produktionsgruppen.  

 ![Översikt över när/hur fältet Lagerställeskod fylls i](media/binflow.png "Översikt över när/hur fältet Lagerställeskod fylls i")  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]