---
title: Designdetaljer – inkommande distributionslagerflöde | Microsoft Docs
description: Det inkommande artikelflödet i ett distributionslager börjar när artiklarna inlevereras i distributionslagret på företagsplatsen, antingen som har tagits emot från externa källor eller från en annan företagplats. Den anställde registrerar artiklarna, vanligtvis genom att skanna en streckkod. Från inleveransstället utförs lageraktiviteter på olika komplexitetsnivåer för att få artiklarna till lagringsområdet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: c2a78d585f949922e9f05e42a6ab61dcd7adc521
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215184"
---
# <a name="design-details-inbound-warehouse-flow"></a>Designdetaljer: inkommande distributionslagerflöde
Det inkommande artikelflödet i ett distributionslager börjar när artiklarna inlevereras i distributionslagret på företagsplatsen, antingen som har tagits emot från externa källor eller från en annan företagplats. Den anställde registrerar artiklarna, vanligtvis genom att skanna en streckkod. Från inleveransstället utförs lageraktiviteter på olika komplexitetsnivåer för att få artiklarna till lagringsområdet.  

 Varje artikel identifieras och matchas till ett motsvarande inkommande källdokument. Följande inkommande källdokument finns:  

- Inköpsorder  
- inkommande överföringsorder  
- Försäljningreturorder  

Dessutom finns följande interna källdokument som fungerar som inkommande källor:  

- Produktionsorder med bokföring av utflöde  
- Monteringsorder med bokföring av utflöde  

De två sista motsvarar inkommande flöden till distributionslagret från interna verksamhetsområden. Se [Designdetaljer: Interna distributionslagerflöden](design-details-internal-warehouse-flows.md) för mer information om lagerhantering för interna inkommande och utgående processer.  

Processer och användargränssnittsdokument i inkommande distributionslagerflöden är olika för grundläggande och avancerad lagerkonfigurationer. Den huvudsakliga skillnaden är att aktiviteter utförs order-för-order i grundläggande distributionslagerkonfiguration, och att de konsolideras för flera order i avancerad distributionslagerkonfiguration. Mer information om olika lagerkomplexitetsnivåer finns i [Designdetaljer: översikt över lagret](design-details-warehouse-setup.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Inleveranser|Artikelinförslar|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|INTER|||2|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument|||X|3|  
|L|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument||X||6-4-5|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument||X|X|6-4-5|  

Att välja ett tillvägagångssätt beror på företagets accepterade metoder och nivån av deras organisationskomplexitet. I distributionslagermiljö som hanterar en order i taget, där de flesta i lagerpersonalen arbetar direkt med orderdokument, kan ett företag välja att använda metod A. Ett distributionslager som hanterar en order i taget och har en mer komplicerad artikelinförselprocess, eller när det finns den särskild lagerpersonal som utför olika lagerstyrningsfunktioner, kan välja att separera artikelinförselfunktioner från orderdokumentet, metod B. Dessutom kan företag som behöver planera hanteringen av flera order ha användning för inleveransdokument för distributionslager, metod C och D.  

I metoderna A, B och C kombineras inleverans och artikelinförsel i ett steg när du bokför motsvarande dokument som inlevererade. I metod D bokförs först inleveransen för att känna igen ökningen av lager och att artiklar är disponibla för försäljning. Lagerarbetaren registrerar sedan artikelinförsel för att göra artiklarna tillgängliga för plockning.  

## <a name="basic-warehouse-configurations"></a>Grundläggande distributionslagerkonfiguration  
Följande diagram visar de inkommande distibutionslagerflödena efter dokumenttyp i grundläggande lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

![Ingående flöde i grundläggande lagerkonfigurationer](media/design_details_warehouse_management_inbound_basic_flow.png "Ingående flöde i grundläggande lagerkonfigurationer")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Släpp källdokument / skapa lagerartikelinförsel  
När artiklarna tas emot i distributionslagret släpper användaren som är ansvarig inleverans källdokument, t. ex. en inköpsorder eller en inkommande överföringsorder, för att signalera till lagerarbetare att de inlevererade artiklarna kan föras in i lagret. Användaren kan också skapa lagerinförseldokument för enskilda orderrader, med en pushmetod, baserat på angivna lagerställen och antal som ska hanteras.  

### <a name="2-create-inbound-request"></a>2: Skapa inkommande rekvisition  
När det inkommande källdokumentet släpps skapas en inkommande distributionslagerförfrågan automatiskt. Den innehåller referenser till källdokumenttypen och numret och kan inte ses av användaren.  

### <a name="3-create-inventory-put-away"></a>3: Skapa lager, artikelinförsel  
På sidan **Lagerinförslar** hämtar lagerarbetaren, med en pull-metod, de väntande källdokumentraderna som baseras på inkommande distributionslagerförfrågningar. Lagerartikelinförselraderna kan redan ha skapats, med en pushmetod, av användaren som är ansvarig för källdokumentet.  

### <a name="4-post-inventory-put-away"></a>4: Bokför lager, artikelinförsel  
På varje rad för artiklar som har införts, delvis eller helt, fyller lagerarbetaren i fältet **Antal** och bokför sedan lagerartikelinförseln. Källdokument som är relaterade till artikelinförsel i lager bokförs som inlevererade.  

Positiva artikeltransaktioner skapas, distributionslagertransaktioner skapas och artikelinförselförfrågan tas bort, om de hanteras fullständigt. Till exempel uppdateras fältet **Inlevererat antal** på den inkommande källdokumentraden. Ett redan bokfört inleveransdokument skapas som återspeglar till exempel inköpsordern, och de inlevererade artiklarna.  

## <a name="advanced-warehouse-configurations"></a>Avancerad distributionslagerkonfiguration  
Följande diagram visar de inkommande distibutionslagerflödet efter dokumenttyp i avancerade lagerkonfigurationer. Numret i diagrammet överensstämmer med momenten i avsnitten efter diagrammet.  

![Ingående flöde i avancerade lagerkonfigurationer](media/design_details_warehouse_management_inbound_advanced_flow.png "Ingående flöde i avancerade lagerkonfigurationer")  

### <a name="1-release-source-document"></a>1: Släpp källdokument  
När artiklarna tas emot i distributionslagret släpper användaren som är ansvarig inleverans källdokument, t. ex. en inköpsorder eller en inkommande överföringsorder, för att signalera till lagerarbetare att de inlevererade artiklarna kan föras in i lagret.  

### <a name="2-create-inbound-request"></a>2: Skapa inkommande rekvisition  
När det inkommande källdokumentet släpps skapas en inkommande distributionslagerförfrågan automatiskt. Den innehåller referenser till källdokumenttypen och numret och kan inte ses av användaren.  

### <a name="3-create-warehouse-receipt"></a>3: Skapa dist.lager inleverans  
På sidan **Dist.lager inleveranser** hämtar användaren som är ansvarig för att ta emot artiklar de väntande källdokumentraderna som baseras på den inkommande distributionslagerförfrågan. Flera dokumentrader kan kombineras i ett inleveransdokument för distributionslager.  

Användaren fyller i fältet **Ant. att hantera** och väljer inleveranszon och lagerplats, om det behövs.  

### <a name="4-post-warehouse-receipt"></a>4: Bokför dist.lagerinleverans  
Användaren bokför distributionslagerinleveransen. Positiva artikeltransaktioner upprättas. Till exempel uppdateras fältet **Inlevererat antal** på den inkommande källdokumentraden.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Skapa dist.lager, intern artikelinförsel  
Användaren som är ansvarig för artikelinförsel från interna operationer skapar en lagerintern artikelinförsel för artiklar som ska föras in i distributionslagret, till exempel produktion eller monteringsutflöde. Användaren anger antal, zon och lagerplats som artiklarna ska införas från, eventuellt med funktionen **Hämta lagerställesinnehåll**. Användaren släpper den lagerinterna artikelinförsel, vilket skapar en inkommande lagerförfrågan så att uppgiften kan hämtas i artikelinförseldokument för distributionslager eller i artikelinförselkalkylarket.  

### <a name="6-create-put-away-request"></a>6: Skapa artikelinförselförfrågan  
När det inkommande källdokumentet bokförs skapas en förfrågan om lagerartikelinförsel automatiskt. Den innehåller referenser till källdokumenttypen och numret och kan inte ses av användaren. Beroende på inställningarna skapar utflöde från en produktionsorder också en förfrågan om artikelinförsel att föra in de färdiga produkterna i lagret.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Generera rader med artikelinförselkalkylark (valfritt)  
Användaren som är ansvarig för att koordinera artikelinförsel hämtar artikelinförselraderna för distributionslager i **Artikelinförsel kalkylark** baserat på bokförda distributionslagerinleveranser eller interna operationer med utförsel. Användaren väljer raderna som ska artikelinföras och förbereder artikelinförseln genom att ange vilka lagerställen att ta från, vilka lagerställen att placera i och hur många enheter som ska hanteras. Lagerställena kan fördefinieras av inställningarna för distributionslagerstället eller verksamhetsresursen.  

När alla artikelinförslar har planerats och tilldelats till lagerarbetare genererar användaren artikelinförseldokumenten. Fullständigt tilldelade artikelinförselrader  tas bort från **Artikelinförsel kalkylark**.  

> [!NOTE]  
>  Om fältet **Artikelinförsel kalkylark** inte har markerats på lagerställekortet skapas distributionslagerdokument för artikelinförsel direkt baserat på bokförda distributionslagerinleveranser. I så fall utelämnas moment 7.  

### <a name="8-create-warehouse-put-away-document"></a>8: Skapa artikelinförseldokument för dist.lager  
Lagerarbetaren som utför artikelinförsel skapar ett artikelinförseldokument för distributionslager, med en pull-metod, baserat på den bokförda distributionslagerinleveransen. Alternativt skapas distributionslagerinförseldokumentet och tilldelas till en lagerarbetare med en pushmetod.  

### <a name="9-register-warehouse-put-away"></a>9: Registrera dist.lager artikelinförsel  
På varje rad för artiklar som har införts, delvis eller helt, fyller lagerarbetaren i fältet **Antal** på sidan **Dist.lager artikelinförsel** och registrerar sedan lagerartikelinförseln.  

Distributionslagertransaktioner skapas och artikelinförselraderna tas bort om de är helt hanterade. Dokumentet för distributionslagerartikelinförsel förblir öppet tills hela antalet på den relaterade bokförda distributionslagerinleveransen har registrerats. Fältet **Artikelinförsel antal** på distributionslagerinleveransorderraderna uppdateras.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]