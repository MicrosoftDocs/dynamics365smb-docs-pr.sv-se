---
title: Designdetaljer – inkommande distributionslagerflöde
description: Det ankommande lagerflödet startar när artiklar anländer till företagets lagerställe och registreras och matchas till ankommande källdokument.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2022
ms.author: bholtorf
---
# <a name="design-details-inbound-warehouse-flow" />Designdetaljer: inkommande distributionslagerflöde

Det inkommande artikelflödet i ett distributionslager börjar när artiklarna inlevereras i distributionslagret på företagsplatsen, antingen som har tagits emot från externa källor eller från en annan företagplats. I princip består processen mottagning av ankommande order av två olika aktiviteter:

* Ta emot artiklar på lagermottagningsplatsen där du identifierar artiklarna, matchar dem i ett källdokument och registrerar den inlevererade kvantiteten. 
* Införa artiklar som finns i lager och registrera den plats där du placerat dem.

Källdokumenten för ankommande lagerställeflöde är:

* Inköpsordrar  
* Inkommande överföringsorder  
* Försäljningsreturorder  

> [!NOTE]
> Produktion och monteringsutflöde representerar också inkommande källdokument. Läs mer om hantering av produktions- och monteringsutflöde för interna processer på [Designdetaljer: Interna distributionslagerflöden](design-details-internal-warehouse-flows.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du ta emot objekt och lägga undan dem med någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|inkommande behandling|Begär inleverans|Begär artikelinförsel|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument||Aktiverat|Grundläggande: Order för order|  
|A|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument|Aktiverat||Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument|Aktiverat|Aktiverat|Avancerat|  

Att välja ett tillvägagångssätt beror på företagets metoder och nivån av deras organisationskomplexitet. Här följer några exempel som kan hjälpa dig att bestämma dig.

* I distributionslagermiljö som hanterar en order i taget, där merparten av lagerpersonalen arbetar direkt med orderdokument, kan du välja att använda metod A. 
* Ett distributionslager som hanterar en order i taget som har en mer komplicerad artikelinförselprocedur, eller där lagerpersonalen delar upp sina artikelinförselaktiviteter från orderdokumentet, kan du använda metod B.
* Företag som behöver planera hanteringen av flera order kan få det att använda dist. lager inleveransdokument, metoder C och D.  

I metoderna A, B och C kombineras inleverans och artikelinförsel i ett steg när du bokför motsvarande dokument som inlevererade. I metod D bokförs först inleveransen för att registrera ökningen av lager och att artiklar är disponibla för försäljning. Lagerarbetaren registrerar sedan artikelinförsel för att göra artiklarna tillgängliga för plockning för avgående order. 

> [!NOTE]
> Även om distributionslagerinförslar och lagerartikelinförslar låter liknande, är de olika dokument och används i olika processer.
> * Lagerartikelinförsel som används i metod B, tillsammans med registrering av artikelinförselinformation, bokför även inleveransen av källdokumentet.
> * Distributionslagerinförsel som används i metod D kan inte bokföras och endast registrera artikelinförsel. Registreringen gör artiklarna tillgängliga för vidare bearbetning men bokför inte inleveransen. I det ankommande flödet kräver distributionslagerinförsel en distributionslagerinleverans.

## <a name="no-dedicated-warehouse-activity" />Ingen tilldelad distributionslageraktivitet

I följande artiklar finns information om hur du behandlar inleveranser för källdokument om du inte har särskilda lageraktiviteter.

* [Registrera inköp](purchasing-how-record-purchases.md)
* [Överföringsorder](inventory-how-transfer-between-locations.md)
* [Behandlar säljreturordrar](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations" />Grundläggande distributionslagerkonfiguration

I en grundläggande lagerkonfiguration, slå på växlingsknappen **Begär artikelinförsel** men växlingsknappen **Begär inleverans** är inaktiverad på platskortsidan för lagerstället.

Följande diagram visar de inkommande distibutionslagerflödena efter dokumenttyp i grundläggande lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Grundläggande ankommande flöde i distributionslager.":::

### <a name="-release-a-source-document-to-create-a-request-for-an-inventory-put-away" />1. Släpp ett källdokument för att skapa en begäran om en lagerinförsel

När du tar emot artiklar släpper du källdokumentet, till exempel en inköpsorder eller en ankommande överföringsorder. Om du släpper dokumentet blir artiklarna tillgängliga för införsel. Du kan också skapa lagerinförseldokument för enskilda orderrader, med en pushmetod, baserat på angivna lagerställen och antal som ska hanteras.  

### <a name="-create-an-inventory-put-away" />2: Skapa lagerinförsel

På sidan **Lagerinförsel** kan du med pull-metod få de väntande källdokumentraderna som baseras på inkommande distributionslagerförfrågningar. Med en pushmetod kan du också skapa lagerartikelinförselraderna när du skapar källdokumentet.  

### <a name="-post-an-inventory-put-away" />3: Bokför en lagerinförsel

På varje rad för artiklar som har införts, delvis eller helt, fyller du i fältet **Antal** och bokför sedan lagerartikelinförseln. Källdokument som är relaterade till artikelinförsel i lager bokförs som inlevererade.  

* Positiva artikeltransaktioner upprättas
* Dist.lager transaktioner skapas för lagerställen som kräver en lagerplatskod på alla artikeltransaktioner.
* Artikelinförsel förfrågan tas bort om den hanteras i sin helhet. Till exempel uppdateras fältet **Inlevererat antal** på den inkommande källdokumentraden.
* Ett redan bokfört inleveransdokument skapas som återspeglar till exempel inköpsordern, och de inlevererade artiklarna.  

## <a name="advanced-warehouse-configurations" />Avancerad distributionslagerkonfiguration

I en avancerad distributionslagerkonfiguration aktiveras växlingsknappen **Begär inleverans** på sidan Lagerställekort för lagerstället. Växlingsknappen **Kräver artikelinförsel** är valfri.

Följande diagram visar de inkommande distibutionslagerflödet efter dokumenttyp. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Avancerat ankommande flöde i distributionslager":::

### <a name="-release-the-source-document" />1: Släpp källdokument

När du tar emot artiklar släpper du källdokumentet, till exempel en inköpsorder eller en ankommande överföringsorder. Om du släpper dokumentet blir artiklarna tillgängliga för införsel. Artikelinförsel innehåller referenser till källdokumenttypen och numret.

### <a name="-create-a-warehouse-receipt" />2: Skapa dist.lager inleverans

Sidan **Distributionslagerinleverans** hämta raderna för ankommande källdokument. Flera dokumentrader kan kombineras i ett inleveransdokument för distributionslager. Fyll i fältet **Ant. att hantera** och väljer inleveranszon och lagerplats, om det behövs.  

### <a name="-post-the-warehouse-receipt" />3: Bokför lagerinleveransen

Boka distributionslagerinleveransen för att skapa positiva artikelposter. Fältet **Inlevererat antal** på den ankommande källdokumentraden uppdateras.  

Om växlingsknappen **Begär artikelinförsel** inte är påslagen på lagerställekortet, det är här processen stannar. Annars kan du lägga upp det ankommande källdokumentet blir artiklarna tillgängliga för införsel. Artikelinförsel innehåller referenser till källdokumenttypen och numret.  

### <a name="-optional-generate-put-away-worksheet-lines" />4: (Valfritt) Generera rader med artikelinförselkalkylark

Hämta artikelinförselraderna i **Artikelinförsel kalkylark** baserat på bokförda lagerinleveranser eller åtgärder som producerar utdata. Välj raderna för artikelinförsel och ange följande information:

* De lagerplatser som artiklarna ska tas från.
* Lagerplatser för att föra in artiklarna.
* Hur många enheter som ska hanteras.

Lagerställena kan fördefinieras av inställningarna för distributionslagerstället eller resursen som utförde åtgärden.  

När alla artikelinförslar har planerats och tilldelats till lagerarbetare genererar användaren artikelinförseldokumenten. Fullständigt tilldelade artikelinförselrader tas bort från **Artikelinförsel kalkylark**.  

> [!NOTE]  
> Om sidan **Artikelinförsel kalkylark** inte har markerats på lagerställekortet skapas distributionslagerdokument för artikelinförsel direkt baserat på bokförda distributionslagerinleveranser. I så fall behövs inte detta steg.  

### <a name="-create-a-warehouse-put-away-document" />5. Skapa ett dokument för artikelinförsel i distributionslager

Skapa ett dokument för artikelinförsel med en pullmetod baserat på den bokförda distributionslagerinleveransen. Alternativt skapas distributionslagerinförseldokumentet och tilldelas till en lagerarbetare med en pushmetod.  

### <a name="-register-a-warehouse-put-away" />6: Registrera dist.lager artikelinförsel

På varje rad för artiklar som har införts, delvis eller helt, fyller du i fältet **Antal** på sidan **Dist.lager artikelinförsel** och registrerar sedan lagerartikelinförseln.  

* Dist.lager transaktioner skapas för lagerställen som kräver en lagerplatskod på alla artikeltransaktioner.
* Artikelinförselraderna tas bort om den hanteras i sin helhet.
* Dokumentet för distributionslagerartikelinförsel förblir öppet tills hela antalet på den relaterade bokförda distributionslagerinleveransen har registrerats.
* Fältet **Artikelinförsel antal** som bokförs på distributionslagerinleveransorderraderna uppdateras.

## <a name="related-tasks" />Närliggande uppgifter

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|  
|Registrera inleveransen av artiklar på lagerställen med en lagerinleverans. Vid halv- eller helautomatisk distributionslagerprocess på plats.|[Ta emot artiklar](warehouse-how-receive-items.md)|
|Införa artiklar order för order och bokföra inleveransen i en aktivitet, i en grundläggande lagerkonfiguration.|[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Införa artiklar som har inlevererats från flera inköp, returer, överföringsorder i en avancerad lagerkonfiguration.|[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  


## <a name="see-also" />Se även

[!INCLUDE[footer-include](includes/footer-banner.md)]
