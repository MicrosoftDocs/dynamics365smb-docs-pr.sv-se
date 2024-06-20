---
title: Designdetaljer – inkommande distributionslagerflöde
description: Lär dig hur du tar emot artiklar i distributionslagret och registrerar och matchar dem med ankommande källdokument.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: warehouse
ms.date: 09/18/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designdetaljer: ankommande distributionslagerflöde

Det inkommande artikelflödet i ett distributionslager börjar när artiklarna inlevereras i distributionslagret på företagsplatsen, antingen som har tagits emot från externa källor eller från en annan företagplats. Du kan ta emot fysiska artiklar och artiklar som inte finns i lager. Om du vill veta mer om hur du tar emot artiklar som inte finns i lager går du till [Bokför artiklar som inte finns i lager](#post-non-inventory-items).

I princip består processen mottagning av ankommande order av två olika aktiviteter:

* Ta emot artiklar på lagermottagningsplatsen där du identifierar dem, matchar dem mot ett källdokument och registrerar den inlevererade kvantiteten.
* Placera artiklar i lager, och registrera den plats där du placerat dem.

Källdokumenten för ankommande lagerställeflöde är:

* Inköpsorder  
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

## Ingen tilldelad distributionslageraktivitet

I följande artiklar finns information om hur du behandlar inleveranser för källdokument om du inte har särskilda lageraktiviteter.

* [Registrera inköp](purchasing-how-record-purchases.md)
* [Överföringsorder](inventory-how-transfer-between-locations.md)
* [Behandlar säljreturorder](sales-how-process-sales-returns-orders.md)

## Grundläggande distributionslagerkonfiguration  

I en grundläggande lagerkonfiguration slås växlingsknappen **Begär artikelinförsel** på, men växlingsknappen **Begär inleverans** är inaktiverad på sidan **Platskort** för lagerstället.

Följande diagram visar de inkommande distibutionslagerflödena efter dokumenttyp i grundläggande lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Grundläggande ankommande flöde i distributionslager.":::

### 1. Släpp ett källdokument för att skapa en begäran om en lagerinförsel  

När du tar emot artiklar släpper du källdokumentet, till exempel en inköpsorder eller en ankommande överföringsorder. Om du släpper dokumentet blir artiklarna tillgängliga för införsel. Du kan också skapa lagerinförseldokument för enskilda orderrader med en pushmetod baserat på angivna lagerställen och antalet som ska hanteras.  

### 2: Skapa lagerinförsel  

På sidan **Lagerinförsel** kan du med pull-metod få de väntande källdokumentraderna som baseras på inkommande distributionslagerförfrågningar. Med en pushmetod kan du också skapa lagerartikelinförselraderna när du skapar källdokumentet.  

### 3: Bokför en lagerinförsel  

På varje rad för artiklar som har införts, delvis eller helt, fyller du i fältet **Antal** och bokför sedan lagerartikelinförseln. Källdokument som är relaterade till artikelinförsel i lager bokförs som inlevererade.  

* Positiva artikeltransaktioner upprättas.
* Dist.lager transaktioner skapas för lagerställen som kräver en lagerplatskod på alla artikeltransaktioner.
* Artikelinförsel förfrågan tas bort om den hanteras i sin helhet. Till exempel uppdateras fältet **Inlevererat antal** på den inkommande källdokumentraden.
* Ett redan bokfört inleveransdokument skapas som återspeglar till exempel inköpsordern, och de inlevererade artiklarna.  

## Avancerad distributionslagerkonfiguration  

För att kunna använda en avancerad distributionslagerkonfiguration aktiverar du växlingsknappen **Begär inleverans** på sidan Lagerställekort för lagerstället. Växlingsknappen **Kräver artikelinförsel** är valfri.

Följande diagram visar de inkommande distibutionslagerflödet efter dokumenttyp. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Avancerat ankommande flöde i distributionslager":::

### 1: Släpp källdokument  

När du tar emot artiklar släpper du källdokumentet, till exempel en inköpsorder eller en ankommande överföringsorder. Om du släpper dokumentet blir artiklarna tillgängliga för införsel. Artikelinförsel innehåller referenser till källdokumenttypen och numret.

### 2: Skapa dist.lager inleverans  

Sidan **Distributionslagerinleverans** hämta raderna för ankommande källdokument. Flera dokumentrader kan kombineras i ett inleveransdokument för distributionslager. Fyll i fältet **Ant. att hantera** och välj inleveranszon och lagerplats, vid behov.  

### 3: Bokför lagerinleveransen  

Boka distributionslagerinleveransen för att skapa positiva artikelposter. Fältet **Inlevererat antal** på den ankommande källdokumentraden uppdateras.  

Om växlingsknappen **Begär artikelinförsel** inte är påslagen på lagerställekortet, det är här processen stannar. Annars kan du lägga upp det ankommande källdokumentet blir artiklarna tillgängliga för införsel. Artikelinförsel innehåller referenser till källdokumenttypen och numret.  

### 4: (Valfritt) Generera rader med artikelinförselkalkylark

Hämta artikelinförselraderna i **Artikelinförsel kalkylark** baserat på bokförda lagerinleveranser eller åtgärder som producerar utdata. På raderna för artikelinförsel anger du följande information:

* De lagerplatser som artiklarna ska tas från.
* Lagerplatser för att föra in artiklarna.
* Hur många enheter som ska hanteras.

Lagerställena kan fördefinieras av inställningarna för distributionslagerstället eller resursen som utförde åtgärden.  

När alla artikelinförslar har planerats och tilldelats till lagerarbetare genererar användaren artikelinförseldokumenten. Fullständigt tilldelade artikelinförselrader tas bort från **Förslag för artikelinförsel**.  

> [!NOTE]  
> Om sidan **Artikelinförsel kalkylark** inte har markerats på lagerställekortet skapas distributionslagerdokument för artikelinförsel direkt baserat på bokförda distributionslagerinleveranser. I så fall behövs inte detta steg.  

### 5. Skapa ett dokument för artikelinförsel i distributionslager

Skapa ett dokument för artikelinförsel med en pullmetod baserat på den bokförda distributionslagerinleveransen. Alternativt skapas distributionslagerinförseldokumentet och tilldelas till en lagerarbetare med en pushmetod.  

### 6: Registrera dist.lager artikelinförsel

På varje rad för artiklar som har införts, delvis eller helt, fyller du i fältet **Antal** på sidan **Dist.lager artikelinförsel** och registrerar sedan lagerartikelinförseln.  

* Dist.lager transaktioner skapas för lagerställen som kräver en lagerplatskod på alla artikeltransaktioner.
* Artikelinförselraderna för dstributionslager tas bort om de hanteras i sin helhet.
* Dokumentet för artikelinförsel för distributionslager förblir öppet tills du registrerar hela antalet på den relaterade bokförda distributionslagerinleveransen.
* Fältet **Artikelinförsel antal** som bokförs på distributionslagerinleveransorderraderna uppdateras.

## Närliggande uppgifter

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|**För att**|**Gå till**|  
|------------|-------------|  
|Ta emot artiklar på lagerställen med en distributionslagerinleverans för helt eller delvis automatiserad distributionslagerbehandling.|[Inleverera artiklar](warehouse-how-receive-items.md)|
|Artikelinförselariklar på order-för-order-bas och bokför inleveransen i en enda aktivitet, i grundläggande distributionslagerkonfigurationer.|[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Införa artiklar som har inlevererats från flera inköp, returer, överföringsorder i en avancerad lagerkonfiguration.|[Föra in artiklar med Distributionslager, artikelinförslar](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  

## Bokföra artiklar som inte finns i lager

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## Se även

[!INCLUDE[footer-include](includes/footer-banner.md)]
