---
title: Processer för avgående distributionslager – översikt
description: I den här artikeln beskrivs arbetsflödet avgående distributionslager.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes" />Processer för avgående distributionslager

Avgående processer i distributionslager startar när du släpper ett källdokument för att ta bort artiklar från ett lagerställe. Till exempel, antingen för att leverera artiklarna någonstans eller för att flytta dem till ett annat lagerställe i företaget. I princip består processen utleverans av avgående order av två olika aktiviteter:

* Plocka artiklar från hyllorna.
* Utleverans av artiklar från distributionslagret.

Källdokumenten för avgående lagerställeflöde är:  

* Försäljningsorder  
* utgående överföringsorder  
* Inköpsreturorder  
* Tjänsteorder  

> [!NOTE]
> Produktions- och monteringsorder med komponent representerar också avgående källdokument. Produktions- och monteringsorder är lite olika eftersom de vanligtvis är interna processer som inte involverar leverans. De används i stället för införsel av tillverkade artiklar eller flytta de komponenter som behövs för att montera en artikel till ett monteringsområde. Mer information om de här processerna finns i [Designdetaljer: interna distributionslagerflöden](design-details-internal-warehouse-flows.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du plocka och inleverera artiklar och använda någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|Utgående process|Begär plockning|Kräv utleverans|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument|Aktiverat||Grundläggande: Order för order|  
|A|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument||Aktiverat|Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument|Aktiverat|Aktiverat|Avancerat|  

Vilken metod som ska väljas beror på distributionslagrets metoder och hur komplexa de är. Här följer några exempel som kan hjälpa dig att bestämma dig.

* I en miljö som tillverkar en order i taget med rättframma processer och enkel lagerplatsstruktur lämpar sig metod A, plockning och utleverans från orderraden.
* Om artiklar för en orderrad kommer från fler än en lagerplats, eller om lagerarbetarna inte kan arbeta med orderdokument, är användningen av separata plockningsdokument lämplig, metod B.
* Om plocknings- och leveransprocesserna omfattar flera order och kräver större kontroll och översikt, kan du välja att använda ett distributionslagerutleveransdokument och ett distributionslagerplockdokument för att åtskilja plocknings- och leveransaktiviteterna, metoderna C och D.  

I metoderna A, B och C kombineras aktiviteterna för plockning och utleverans i ett steg när du bokför ett dokument som utlevererat. I metod D registrerar du förs plockningen och sedan bokförs utleveransen vid ett senare tillfälle från ett annat dokument.

> [!NOTE]
> Även om distributionslagerplockningar och lager plockningar låter liknande, är de olika dokument och används i olika processer.
> * Lagerplockningen som används i metod B, tillsammans med registrering av plockningsinformation, bokför även utleveransen av källdokumentet.
> * Distributionslagerplockningen som används i metod D kan inte bokföras och endast registrera plockning. Registreringen gör artiklarna tillgängliga för distributionslagerutleveranser men bokför inte utleveransen. I det utgående flödet kräver distributionslagerplockningen en distributionslagerutleverans.

## <a name="no-dedicated-warehouse-activity" />Ingen tilldelad distributionslageraktivitet

I följande artiklar finns information om hur du behandlar inleveranser för källdokument om du inte har särskilda lageraktiviteter.

* [Sälja produkter](sales-how-sell-products.md)
* [Överföringsorder](inventory-how-transfer-between-locations.md)
* [Behandla inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md)
* [Skapa tjänsteorder](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations" />Grundläggande distributionslagerkonfiguration

Följande diagram visar de utgående distibutionslagerprocesserna för olika typer av dokument i grundläggande lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Visar stegen i ett grundläggande utgående flöde i ett lagerställe.":::

### <a name="1-release-a-source-document" />1: Släpp källdokument

När du använder åtgärden **Frisläpp** i ett källdokument, t.ex. en försäljnings- eller överföringsorder, är artiklarna i dokumentet klara att hanteras i distributionslagret. Till exempel plockat och placera i den lagerplats som anges i dokumentet. Användaren kan skapa plockningsdokument för inventering för enskilda rader på order, med en pushmetod, baserat på angivna lagerställen och antal som ska hanteras.  

### <a name="2-create-an-inventory-pick" />2. Skapa lagerplockning

På sidan **lagerplockning** hämtas lagerarbetaren från källdokument raderna. Lagerplockningsraderna kan redan ha skapats, med en pushmetod, av användaren som är ansvarig för källdokumentet.  

### <a name="3-post-an-inventory-pick" />3. Bokföra lagerplockning

På varje rad för artiklar som har plockats delvis eller helt, fyller lagerarbetaren i fältet **Antal** och bokför sedan lagerplockningen. Källdokument som är relaterade till lagerplockningen bokförs som levererade eller förbrukade.  

För lagerplockningarna skapas negativa artikeltransaktioner, distributionslagertransaktioner skapas och plockförfrågan tas bort, om de hanteras fullständigt. Till exempel uppdateras fältet **Utlevererat antal** på den utkommande källdokumentraden. Ett redan bokfört leveransdokument skapas som återspeglar till exempel försäljningsordern, och de levererade artiklarna.  

## <a name="advanced-warehouse-configurations" />Avancerad distributionslagerkonfiguration

Följande diagram visar de utgående distibutionslagerprocesserna för olika typer av dokument i avancerade lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Visar stegen i ett grundläggande utgående distributionslagerflöde.":::

### <a name="1-release-a-source-document" />1: Släpp källdokument

Om du frigör ett källdokument i avancerade konfigurationer sker samma sak som för grundläggande konfigurationer. Artiklarna blir tillgängliga för hantering i distributionslagret. De kan till exempel ingå i en utleverans.  

### <a name="2-create-a-warehouse-shipment" />2. Skapa en distributionslagerutleverans

Sidan **Dist.lager utleverans** hämtar raderna från det släppta källdokumentet. Du kan kombinera rader från flera källdokument i en distributionslagerutleverans.  

### <a name="3-create-a-warehouse-pick" />3: Skapa distributionslagerplockning

På sidan **Distributionslagerutleverans**, skapa aktiviteter för distributionslagerplockning för utleveranser på ett av två sätt:

- Med push-metod där du använder åtgärden **Skapa plockning**. Välj raderna att plockas och förbered plockningar genom att till exempel ange vilka fack som ska tas från och placeras i, och hur många enheter som ska hanteras. Lagerplatser kan fördefinieras för distributionslagerstället eller resurs.
- Med pull-metod där du använder åtgärden **Frisläppa**. På sidan **Plockningskalkylark** kan distributionslagerpersonal använda åtgärden **Hämta dist.lager dokument** för att hämta sina tilldelade plockningar. När distributionslagerplockningar är fullständigt registrerade tas raderna i **Plockningskalkylark** bort.

### <a name="4-register-a-warehouse-pick" />4: Registrera dist.lagerplockning

På sidan **Dist.lager plockning** fyller lagerarbetaren i fältet **Antal** på varje rad för artiklar som har plockats, delvis eller helt och registrerar sedan plockningen.

Distributionslagertransaktioner skapas och plockningsraderna tas bort om hela antalet plockades. Plockningsdokument förblir öppet tills hela antalet på distributionslagerutleverans registreras. Fältet **Plockat antal** på distributionslagerutleveransraderna uppdateras.  

### <a name="5-post-the-warehouse-shipment" />5: Bokför dist.lager utleverans

När alla artiklar på distributionslagerutleveransdokument registrerats som plockade bokför distributionslagerarbetaren utleveransen. Bokföringen uppdaterar artikeltransaktionerna så att de återspeglar minskningen av lagret. Till exempel uppdateras fältet **Utlevererat antal** på den utkommande källdokumentraden.  

## <a name="see-also" />Se även

[Warehouse Management](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
