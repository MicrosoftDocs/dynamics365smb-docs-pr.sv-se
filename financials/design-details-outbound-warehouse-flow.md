---
title: "Designdetaljer - Avgående distributionslagerflöde | Microsoft Docs"
description: "Det avgående artikelflödet i distributionslagret inleds med en förfrågan från utsläppta källdokument att ta artiklarna ut från distributionslagerplatsen, antingen för att levereras till en extern part eller till en annan företagplats. Från lagringsområdet utförs lageraktiviteter på olika komplexitetsnivåer för att få ut artiklarna till utleveransställena."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 54489c23a34e409ccb22faff77da41acdaf065b3
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-outbound-warehouse-flow"></a>Designdetaljer: Avgående distributionslagerflöde
Det avgående artikelflödet i distributionslagret inleds med en förfrågan från utsläppta källdokument att ta artiklarna ut från distributionslagerplatsen, antingen för att levereras till en extern part eller till en annan företagplats. Från lagringsområdet utförs lageraktiviteter på olika komplexitetsnivåer för att få ut artiklarna till utleveransställena.  

 Varje artikel identifieras och matchas till ett motsvarande ankommande källdokument. Följande avgående källdokument finns:  

- Försäljningsorder  
- Avgående överföringsorder  
- Inköpsreturorder  
- Tjänsteorder  

Dessutom finns följande interna källdokument som fungerar som avgående källor:  

- Produktionsorder med komponentbehov  
- Monteringsorder med komponentbehov  

 De två sista dokumenten motsvarar utgående flöden från distributionslagret till interna verksamhetsområden. Se [Designdetaljer: Interna distributionslagerflöden](design-details-internal-warehouse-flows.md) för mer information om lagerhantering för interna ankommande och utgående processer.  

 Processer och användargränssnittsdokument i avgående distributionslagerflöden är olika för grundläggande och avancerad lagerkonfigurationer. Den huvudsakliga skillnaden är att aktiviteter utförs order-för-order i grundläggande distributionslagerkonfiguration, och att de konsolideras för flera order i avancerad distributionslagerkonfiguration. Mer information om olika lagerkomplexitetsnivåer finns i [Designdetaljer: översikt över lagret](design-details-warehouse-setup.md).  

 I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|Ankommande behandling|Lagerplatser|Plockningar|Utleveranser|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|INTER|||2|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument||X||3|  
|L|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument|||X|6-4-5|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument||INTER|INTER|6-4-5|  

 Mer information finns i [Designdetaljer: Avgående distributionslagerflöde]().  

 Att välja ett tillvägagångssätt beror på företagets accepterade metoder och nivån av deras organisationskomplexitet. I en miljö som tillverkar en order i taget med rättframma processer och enkel lagerplatsstruktur lämpar sig metod A, plockning och utleverans från orderraden. I andra order-för-order-företag, där artiklar för en orderrad kan komma från fler än en lagerplats eller där lagerarbetare inte kan arbeta med orderdokument, är användning av separata plockdokument lämplig, metod B. Ett företag där plockning- och leveransprocesser innehåller hantering av flera order och därför kräver större kontroll och översikt, kan företaget välja att använda ett distributionslagerutleveransdokument och distributionslagerplockningdokument för att skilja plockning- och utleveransuppgifterna, metod C och D.  

 I metoderna A, B och C kombineras åtgärderna plockning och utleverans i ett steg när du bokför motsvarande dokument som utlevererade. I metod D registreras plockningen först, och sedan bokförs utleveransen vid ett senare tillfälle från ett annat dokument.  

## <a name="basic-warehouse-configurations"></a>Grundläggande distributionslagerkonfiguration  
 Följande diagram visar de avgående distibutionslagerflödena efter dokumenttyp i grundläggande lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

 ![Utkommande flöde i grundläggande lagerkonfigurationer](media/design_details_warehouse_management_outbound_basic_flow.png "design_details_warehouse_management_outbound_basic_flow")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Släpp källdokumentet/skapa lagerplockning eller transport  
 När en användare som är ansvarig för källdokument, t.ex. en försäljningsorderhandläggare eller en produktionsplanerare, är redo för den utgående lageraktiviteten släpper han eller hon källdokumentet för att signalera till lagerpersonalen att sålda artiklar eller komponenter kan plockas och placeras i de angivna lagerplatserna. Användaren kan också skapa lagerplocknings- eller transportdokument för de individuella orderraderna, med en push-metod, baserat på vissa lagerplatser och antal att hantera.  

> [!NOTE]  
>  Lagerförflyttningar används för att flytta artiklar till interna verksamhetsområden i grundläggande lagerkonfigurationer, baserat på källdokument eller på ad hoc-bas.  

### <a name="2-create-outbound-request"></a>2: Skapa avgående rekvisition  
 När det avgående källdokumentet släpps skapas en avgående distributionslagerförfrågan automatiskt. Den innehåller referenser till källdokumenttypen och numret och kan inte ses av användaren.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Skapa lagerplockning eller transport  
 I fönstret **Lagerplockning** eller **Lagerrörelse** hämtar lagerarbetaren, med en pull-metod, de väntande källdokumentraderna som baseras på avgående distributionslagerförfrågningar. Lagerplockningsraderna kan redan ha skapats, med en pushmetod, av användaren som är ansvarig för källdokumentet.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Bokför lagerplockning eller registrera lagertransport  
 På varje rad för artiklar som har plockats eller transporterats, delvis eller helt, fyller lagerarbetaren i fältet **Antal** och bokför sedan lagerplockningen eller registrerar lagertransporten. Källdokument som är relaterade till lagerplockningen bokförs som levererade eller förbrukade. Källdokument som är relaterade till lagerförflyttningar bokförs inte.  

 För lagerplockningarna skapas negativa artikeltransaktioner, distributionslagertransaktioner skapas och plockförfrågan tas bort, om de hanteras fullständigt. Till exempel uppdateras fältet **Utlevererat antal** på den utkommande källdokumentraden. Ett redan bokfört leveransdokument skapas som återspeglar till exempel försäljningsordern, och de levererade artiklarna.  

## <a name="advanced-warehouse-configurations"></a>avancerad distributionslagerkonfiguration  
 Följande diagram visar de avgående distibutionslagerflödet efter dokumenttyp i avancerade lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

 ![Utkommande flöde i avancerade lagerkonfigurationer](media/design_details_warehouse_management_outbound_advanced_flow.png "design_details_warehouse_management_outbound_advanced_flow")  

### <a name="1-release-source-document"></a>1: Släpp källdokument  
 När en användare som är ansvarig för källdokument, t.ex. en försäljningsorderhandläggare eller en produktionsplanerare, är redo för den utgående lageraktiviteten släpper han eller hon källdokumentet för att signalera till lagerpersonalen att sålda artiklar eller komponenter kan plockas och placeras i de angivna lagerplatserna.  

### <a name="2-create-outbound-request"></a>2: Skapa avgående rekvisition  
 När det ankommande källdokumentet släpps skapas en avgående distributionslagerförfrågan automatiskt. Den innehåller referenser till källdokumenttypen och numret och kan inte ses av användaren.  

### <a name="3-create-warehouse-shipment"></a>3: Skapa distributionslagerutleverans  
 I fönstret **Dist.lager utleverans** hämtar den utleveransarbetare som är ansvarig de väntande källdokumentraderna som baseras på den avgående distributionslagerförfrågan. Flera dokumentrader kan kombineras i ett utleveransdokument för distributionslager.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Släpp leveransen/skapa dist.lagerplockning  
 Utleveransarbetaren som är ansvarig frigör distributionslagerutleveransen, så att lagerarbetare kan skapa eller koordinera distributionslagerplockning för utleveransen i fråga.  

 Användaren kan också skapa lagerplockningsdokument för enskilda utleveransrader, med en pushmetod, baserat på angivna lagerplatser och antal som ska hanteras.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Släpp intern operation/ Skapa dist.lagerplockning  
 Användaren som är ansvarig för interna operationer släpper ett internt källdokument, t.ex en produktions- och monteringsorder, så att lagerarbetare kan skapa eller koordinera distributionslagerplockning för den interna operationen i fråga.  

 Användaren kan också skapa lagerplockningsdokument för den enskilda produktions- eller monteringsordern, med en pushmetod, baserat på angivna lagerplatser och antal som ska hanteras.  

### <a name="6-create-pick-request"></a>6: Skapa plockförfrågan  
 När det avgående källdokumentet släpps skapas en lagerplockförfrågan automatiskt. Den innehåller referenser till källdokumenttypen och numret och kan inte ses av användaren. Beroende på inställningarna skapar förbrukning från en produktions- och monteringsorder även en plockförfrågan att plocka de nödvändiga komponenterna från lagret.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Generera plockningskalkylarksrader  
 Användaren som är ansvarig för att koordinera plockningar hämtar den lagerplockningsraderna i **Plockningskalkylark** baserat på plockförfrågningar från utleveranser från distributionslager eller interna operationer med komponentförbrukning. Användaren väljer raderna som ska plockas och förbereder plockningarna genom att ange vilka lagerplatser som de ska tas från, vilka lagerplatser att placera i och hur många enheter som ska hanteras. Lagerplatserna kan fördefinieras av inställningarna för distributionslagerstället eller verksamhetsresursen.  

 Användaren anger plockningsmetoder för optimerad lagerhantering och använder sedan en funktion för att skapa motsvarande den distributionslagerplockningsdokument, som tilldelats olika lagerarbetare som utför distributionslagerplockningarna. När distributionslagerplockningar är fullständigt tilldelade tas **Plockningskalkylark** bort.  

### <a name="8-create-warehouse-pick-documents"></a>8: Skapa plockningdokument för dist.lager  
 Lagerarbetaren som utför plockning skapar ett plockningsdokument för distributionslager, med en pull-metod, baserat på det utsläppta källdokumentet. Alternativt skapas lagerplockningdokumentet och tilldelas till en lagerarbetare med en pushmetod.  

### <a name="9-register-warehouse-pick"></a>9: Registrera dist.lagerplockning  
 På varje rad för artiklar som har plockats, delvis eller helt, fyller lagerarbetaren i fältet **Antal** i fönstret **Dist.lager plockning Pick** och registrerar sedan lagerplockningen.  

 Distributionslagertransaktioner skapas och plockningsraderna tas bort om de är helt hanterade. Plockningsdokument förblir öppet tills hela antalet på den relaterade distributionslagerutleverans registreras. Fältet **Plockat antal** på distributionslagerutleveransraderna uppdateras.  

### <a name="10-post-warehouse-shipment"></a>10: Bokför dist.lager utleverans  
 När alla artiklar på distributionslagerutleveransdokument registrerats som plockade till de angivna utleveranslagerplatserna, bokför leveransarbetaren som är ansvarig utleveransen. Negativa artikeltransaktioner upprättas. Till exempel uppdateras fältet **Utlevererat antal** på den utkommande källdokumentraden.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)

