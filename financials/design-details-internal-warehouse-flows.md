---
title: "Designdetaljer - Interna distributionslagerflöden | Microsoft Docs"
description: "Flödet av artiklar mellan lagerplatser på ett företags lagerställe centreras på plockning av komponenter och införsel av slutartiklar för monterings- eller produktionsorder och ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9ba5203013af329f1d59432a5e5800fe486658cc
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-internal-warehouse-flows"></a>Designdetaljer: Interna distributionslagerflöden
Flödet av artiklar mellan lagerplatser på ett företags lagerställe centreras på plockning av komponenter och införsel av slutartiklar för monterings- eller produktionsorder och ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument. Omfattningen och typen av de berörda aktiviteterna varierar mellan grundläggande och avancerad lagerstyrning.  

 Alla interna flöden överlappar vid ankommande eller avgående flöden. Viss av den här överlappningen visas som moment 4 och 5 i de grafiska diagrammen för avancerade ankommande och avgående arbetsflöden. Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Interna flöden i Grundläggande lagerstyrning  
 I grundläggande lagerkonfiguration centreras flödet av artiklar mellan lagerplatser inom företag på att plocka komponenter och införsel av slutartiklar för produktion eller monteringsorder och ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument.  

### <a name="flows-to-and-from-production"></a>Flöden till och från produktion  
 Den huvudsakliga integreringen mellan produktionsorder och grundläggande distributionslageraktiviteter representeras av möjligheten att välja produktionskomponenter med fönstret **Lagerplockning** eller fönstret **Lagerförflyttning**.  

> [!NOTE]  
>  I fönstret **Lagerplockning** fönstret bokförs komponentförbrukningen tillsammans med plockbokföringen. Med hjälp av fönstret **Lagerförflyttning** registreras bara lagerplatsjusteringar, och ingen bokföring av artikeltransaktion inträffar.  

 Förutom komponenthantering representeras integreringen av möjligheten att införa producerade artiklar via fönstret **Lagerinförsel**.  

 Fälten **Till prod.-lagerplats - kod**, **Från prod.lagerplats - kod** och **Öppen prod.lagerplats kod** på lagerställekortet eller maskin-/produktionsgruppkorten definierar standardflöden till och från produktionsområden.  

 Se avsnittet ”Bokföring av produktionskomponenter i distributionslagret” i det här avsnittet om du vill ha mer information om hur komponentförbrukning bokförs från Till-produktionslagerplats eller öppen produktionslagerplats.  

### <a name="flows-to-and-from-assembly"></a>Flöden till och från montering  
 Den huvudsakliga integreringen mellan monteringsorder och grundläggande distributionslageraktiviteter representeras av möjligheten att flytta monteringkomponenter på monteringsområdet.  

 Det finns ingen särskild distributionslagerfunktion för att införsel av monteringsartiklar, men lagerplatskoden på monteringsorderhuvudet kan ställas in till en standardlagerplats för artikelinförsel. Bokföra av monteringsordern fungerar då som att bokföra artikelinförsel. Distributionslageraktiviteten som flyttar monteringsartiklar till distributionslagret kan hanteras i fönstret **Interntransport** utan relation till monteringsordern.  

 Följande monteringsflöden finns.  

|Arbetsflöde|Description|  
|----------|---------------------------------------|  
|Montering mot lager|Komponenterna är nödvändiga på en monteringsorder där utflödet lagras i distributionslagret.<br /><br /> Det här distributionslagerflödet hanteras i fönstret **Lagertransport**. En ta-rad anger var att komponenter ska tas. En placeringsrad anger var att komponenter ska placeras.|  
|Montering mot kundorder|Komponenterna är nödvändiga på en monteringsorder som är kopplad till en försäljningsorder som ska levereras när den sålda artikeln har monterats.|  

> [!NOTE]  
>  Om artiklar monteras mot kundorder aktiverar lagerplockningen för den kopplade försäljningsordern en lagerförflyttning för alla berörda monteringskomponenter, inte bara för den sålda artikeln som när du levererar lagerartiklar.  

 Fälten **Till monteringsplats - kod**, **Från monteringsplats - kod** och **Lagerpl.kod för mont. mot lev.** på lagerställekortet definierar standardflöden till och från monteringsområden.  

> [!NOTE]  
>  Fältet **Lagerpl.kod för mont. mot lev.** fungerar som från-monteringslagerplats i scenarier med montering mot kundorder.  

### <a name="ad-hoc-movements"></a>Förflyttningar ad hoc  
 I grundläggande lagerhantering hanteras transport av artiklar från lagerplats till lagerplats utan relation till källdokument i fönstret **Interntransport** som fungerar tillsammans med fönstret **Lagertransport**.  

 Ett annat sätt att flytta artiklar ad hoc mellan lagerplatser är att bokföra positiva transaktioner i fältet **Ny lagerplatskod** i fönstret **Artikelgrupperingsjnl**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Interna flöden i Avancerad lagerstyrning  
 I avancerade distributionslagerkonfigurationer centreras flödet av artiklar mellan lagerplatser inom företaget på att plocka komponenter och föra in slutartiklar för produktionsorder och plocka komponenter för monteringsorder. Dessutom uppstår interna flöden som ad hoc-transporter, till exempel lagerplatspåfyllningar, utan relation till källdokument.  

### <a name="flows-to-and-from-production"></a>Flöden till och från produktion  
 Den huvudsakliga integreringen mellan produktionsorder och avancerade lageraktiviteter representeras av kan du välja ut produktionskomponenter, i fönstret **Distributionslagerplockning** och fönstret **Plockningsförslag**, och möjligheten att införa producerade artiklar via fönstret **Dist.lager intern art.införsel**.  

 En annan integrationspunkt i produktionen finns i fönstret **Dist.lager transport** tillsammans med fönstret Transportförslag som du kan använda för att placera komponenter och ta producerade artiklar för släppta produktionsorder.  

 Fälten **Till prod.-lagerplats - kod**, **Från prod.lagerplats - kod** och **Öppen prod.lagerplats kod** på lagerställekortet eller maskin-/produktionsgruppkorten definierar standardflöden till och från produktionsområden.  

 Se avsnittet ”Bokföring av produktionskomponenter i distributionslagret” i det här avsnittet om du vill ha mer information om hur komponentförbrukning bokförs från Till-produktionslagerplats eller öppen produktionslagerplats.  

### <a name="flows-to-and-from-assembly"></a>Flöden till och från montering  
 Den huvudsakliga integreringen mellan monteringsorder och avancerade lageraktiviteter representeras av att kan du välja monteringkomponenter, både med fönstret **Distributionslagerplockning** och fönstret **Plockningsförslag**. Den här funktionen fungerar precis som när du plockar komponenter för produktionsorder.  

 Det finns ingen särskild distributionslagerfunktion för att införsel av monteringsartiklar, men lagerplatskoden på monteringsorderhuvudet kan ställas in till en standardlagerplats för artikelinförsel. Bokföra av monteringsordern fungerar då som att bokföra artikelinförsel. Distributionslageraktiviteten som flyttar monteringsartiklar till distributionslagret kan hanteras i fönstret **Transportförslag** eller fönstret **Dist.lager intern art.införsel** utan relation till monteringsordern.  

> [!NOTE]  
>  Om artiklar monteras mot kundorder aktiverar distributionslagerutleveransen för den kopplade försäljningsordern en distributionslagerplockning för alla berörda monteringskomponenter, inte bara för den sålda artikeln som när du levererar lagerartiklar.  

 Fältet **Till monteringsplats - kod** och **Från monteringsplats - kod** på lagerställekortet definierar standardflöden till och från monteringsområden.  

### <a name="ad-hoc-movements"></a>Förflyttningar ad hoc  
 I avancerad lagerhantering hanteras transport av artiklar från lagerplats till lagerplats utan relation till källdokument i fönstret **Transportförslag** och registreras i fönstret Dist.lager transport.  

## <a name="flushing-production-components-in-the-warehouse"></a>Bokföring av produktionskomponenter i distributionslagret  
 Om komponenter finns angivna på artikelkortet bokförs komponenter som plockas med distributionslagerplockning som förbrukade av produktionsordern när distributionslagerplockningen registreras. Genom att använda metoden **Plocka + framåt** och bokföringsmetoden **Plocka + bakåt** aktiverar plockregistreringen den relaterade förbrukningsbokföringen när den första operationen startar, eller när det sista operationen är klar, kommer.  

 Tänk på följande scenario baserat på [!INCLUDE[d365fin](includes/d365fin_md.md)] demodatabas, lagerställe VIT.  

 En produktionsorder för 15 STYCK av artikeln LS-100 finns. Några av artiklarna på komponentlistan måste bokföras manuellt i en förbrukningsjournal, och andra artiklar på listan kan plockas och bokföras automatiskt med hjälp av bokföringsmetoden **Plocka + bakåt**.  

> [!NOTE]  
>  **Plocka + framåt** fungerar bara om den andra produktionsoperationsföljdsradens operation använder en routningslänkkod. När du släpper en planerad produktionsorder aktiverar bokföring framåt av komponenter som har värdet **Plocka + framåt**. Bokföringen kan inte göras förrän plockningen av komponenterna är registrerad,vilket endast kan göras när ordern släpps.  

 Följande moment beskriver de ingående åtgärderna från olika användare och det relaterade svaret:  

1.  Produktionsledaren släpper produktionsordern. Artiklar med bokföringsmetoden **Framåt** och utan operationsföljdlänkkod dras av från den öppna fabrikslagerplatsen.  
2.  Produktionsledare väljer knappen **Skapa dist.lagerplockning** på produktionsordern. Ett plockningdokument för dist.lager skapas för plockning av artiklar med bokföringsmetoderna **Manuell**, **Plocka + bakåt**och **Plocka + framåt**. Dessa artiklar placeras i Till produktion-lagerplatsen.  
3.  Lagerchefen tilldelar plockningar till lagerarbetare.  
4.  Lagerarbetaren plockar artiklarna från lämpliga lagerplatser och placerar dem i Till produktion-lagerplatsen eller lagerplatsen som anges på distributionslagerplockningen, som kan vara en produktionsgrupp eller maskingrupplagerplats.  
5.  Lagerarbetaren registrerar plockningen. Antalet subtraheras från plocklagerplatserna och läggs till i förbrukningslagerplatsen. Fältet **Plockat antal** på komponentlistan för alla plockade artiklar uppdateras.  

    > [!NOTE]  
    >  Endast det antal som plockas kan förbrukas.  

6.  Maskinoperatorn informerar produktionschefen att slutartiklarna är klara.  
7.  Produktionsledaren använder förbrukningsjournalen eller produktionsjournalen för att bokföra förbrukningen av komponentartiklarna som använder bokföringsmetoden **Manuell** eller **Framåt** eller **Plocka + framåt** tillsammans med koderna för operationsföljdslänkar.  
8.  Produktionschefen bokför utflödet av produktionsorder och ändrar status till **Avslutad**. Antalet av komponentartiklarna som använder bokföringsmetoden **Bakåt** dras av från öppna fabrikslagerplatser, och antalet av komponentartiklarna som använder bokföringsmetoden **Plocka + bakåt** dras av från till produktion-lagerplatsen.  

 Följande illustration visas när fältet **Lagerplatskod** på komponentlistan fylls enligt inställningen för lagerstället eller maskin-/produktionsgruppen.  

 ![Flödesschema för lagerplats](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)

