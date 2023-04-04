---
title: Skapa ett lagerställekort och definiera överföringsflöden (innehåller video)
description: 'Om du köper, lagrar eller säljer artiklar på mer än ett ställe kan du ställa in varje plats som lagerställe.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 07/05/2022
ms.author: bholtorf
---
# Konfigurera platser

Lagerställen är platser som distributionslager där du köper, lagrar eller säljer artiklar. [!INCLUDE [prod_short](includes/prod_short.md)] använder lagerställen för att hålla ordning på lagret i både enklare och mer komplicerade lagerprocesser.

Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen. Mer information finns i [Administrera projekt](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## Lagerställekort

Du anger information om ett lagerställe, till exempel ett distributionslager eller distributionscenter på sidan **Lagerställekort**. Du tilldelar varje lagerställe ett namn och en kod som representerar lagerstället. Du kan sedan ange lagerställekoden i andra delar av programmet när du vill registrera transaktioner för ett visst lagerställe.  

Du kan ange information om lagerplatser och lagerprinciper för varje lagerställe. Baserat på lagerprinciper kan du använda alternativen på snabbfliken **Lagerplatser** för att ange vilka lagerplatser som ska användas som standard för transaktioner. Om du använder riktad artikelinförsel och artikelplockning kan du med alternativen på snabbfliken **Lagerplatsprinciper** definiera hur du vill använda avancerade lagerfunktioner.  

Vissa alternativfält beror på inställningar på sidan **Lagerställekort** för att begränsa konfigurationskombinationer som inte stöds.  

Välj åtgärden **Zoner** eller **Lagerplatser** om du vill visa information om zoner och lagerplatser som har definierats för lagerstället.

### Så här skapar du lagerställen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.

> [!NOTE]  
> Många fält på sidan Lagerställekort hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser. Dessa fält är inte relevanta för företag som inte behöver komplicerade distributionslagerfunktioner. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Du kan ändra konfigurationen för ett lagerställe så länge den inte har några artikeltransaktioner.  

Du kan definiera överföringsflöden mellan lagerställen, om du har flera lagerställen. Mer information finns i [Skapa överföringsflöde](inventory-how-setup-locations.md#to-create-a-transfer-route).

### Så här skapar du ett överföringsflöde

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **överföringsflöden** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
4. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu överföra lagerartiklar mellan två lagerställen. Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).    

## Lagerplatser

Lagerplatser representerar den grundläggande lagerstrukturen och kan föreslå var artiklar ska placeras. Dina lagerplatser kan ha innehåll eller vara flytande lagerplatser utan visst innehåll. 

Om du vill använda lagerplatsfunktionen på ett lagerställe går du till sidan **Lagerställekort** på snabbfliken **Distributionslager** och aktiverar reglaget **Lagerplats obligatorisk**. Du kan utforma artikelflödet på lagerstället genom att ange lagerplatskoder i fälten för lagerprocesserna på snabbflikarna **Lagerplatser** och **Lagerplatsprinciper**.

> [!NOTE]
> Innan du kan ange lagerplatskoder på ett lagerställe, måste du skapa lagerplatskoder. Mer information finns i [Skapa lagerställen](warehouse-how-to-create-individual-bins.md) och [Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md).  

## Zoner

Om du vill strukturera lagerplatser under zoner kan du göra det på sidan **Zoner**. När du tilldelar en zon till lagerplatser kopierar [!INCLUDE [prod_short](includes/prod_short.md)] informationen från zonen till lagerplatserna. Du kan också välja att ställa in en zon och använda lagerplatser separat för att organisera distributionslagret. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

## Standarddimensioner för platser

Du anger standardmått för en plats på sidan **Platskort** genom att välja **Dimensioner**. Därefter kopplas platsens standarddimensioner till dokument när du väljer lagerställe på en rad. Om det behövs kan du ta bort eller ändra dimensionen på raden. På fältet **värdebokföring** kan du kräva att personer anger dimensioner för platser innan de kan bokföra en transaktion. Om du vill att användarna endast ska kunna välja vissa dimensionsvärden kan du ange värdena i fältet **Tillåtna värdefilter**. Du kan också ta med dimensions värden för lagerställe på sidan **standard dimensionsprioriteringar** och **Dimensionskombinationer** för kombinationer av prioritet och dimensionsregler.

## Se relaterad utbildning på [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## Se även

[Hantera lager](inventory-manage-inventory.md)  
[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)  
[Skapa lagerställen](warehouse-how-to-create-individual-bins.md)  
[Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
