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
ms.date: 03/25/2023
ms.author: bholtorf
---
# <a name="set-up-locations"></a>Konfigurera platser

Lagerställen är platser som distributionslager där du köper, lagrar eller säljer artiklar. [!INCLUDE [prod_short](includes/prod_short.md)] använder lagerställen för att hålla ordning på lagret i både enklare och mer komplicerade lagerprocesser.

Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen. Mer information finns i [Hantera lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lagerställekort

Du anger information om ett lagerställe, till exempel ett distributionslager eller distributionscenter på sidan **Lagerställekort**. Du tilldelar varje lagerställe ett namn och en kod som representerar lagerstället. Du kan sedan ange lagerställekoden i andra delar av programmet när du vill registrera transaktioner för ett visst lagerställe.  

Du kan ange information om lagerplatser och lagerprinciper för varje lagerställe. Baserat på lagerprinciper kan du använda alternativen på snabbfliken **Lagerplatser** för att ange vilka lagerplatser som ska användas som standard för transaktioner. Om du använder riktad artikelinförsel och artikelplockning kan du med alternativen på snabbfliken **Lagerplatsprinciper** definiera hur du vill använda avancerade lagerfunktioner.  

Vissa alternativfält beror på inställningar på sidan **Lagerställekort** för att begränsa konfigurationskombinationer som inte stöds.  

Välj åtgärden **Zoner** eller **Lagerplatser** om du vill visa information om zoner och lagerplatser som har definierats för lagerstället.

### <a name="to-set-up-a-location"></a>Så här skapar du lagerställen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.

> [!NOTE]  
> Många fält på sidan Lagerställekort hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser. Dessa fält är inte relevanta för företag som inte behöver komplicerade distributionslagerfunktioner. Läs mer på [Ställa in Warehouse Management](warehouse-setup-warehouse.md).

Du kan ändra konfigurationen för ett lagerställe så länge den inte har några artikeltransaktioner.  

Du kan definiera överföringsflöden mellan lagerställen, om du har flera lagerställen. Om du vill veta mer om överföringsflöden går du till [Skapa ett överföringsflöde](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Så här skapar du ett överföringsflöde

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **överföringsflöden** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
4. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu överföra lagerartiklar mellan två lagerställen. Om du vill veta mer om överföringar går du vidare till [överför lager mellan lagerställen](inventory-how-transfer-between-locations.md).

## <a name="bins"></a>Lagerställen

Lagerplatser representerar den grundläggande lagerstrukturen och kan föreslå var artiklar ska placeras. Dina lagerplatser kan ha innehåll eller vara flytande lagerplatser utan visst innehåll.

Om du vill använda lagerplatsfunktionen på ett lagerställe går du till sidan **Lagerställekort** på snabbfliken **Distributionslager** och aktiverar reglaget **Lagerplats obligatorisk**. Du kan utforma artikelflödet på lagerstället genom att ange lagerplatskoder i fälten för lagerprocesserna på snabbflikarna **Lagerplatser** och **Lagerplatsprinciper**.

> [!NOTE]
> Innan du kan ange lagerplatskoder på ett lagerställe, måste du skapa lagerplatskoder. Om du vill lära dig mer om lager platser går du till [skapa lagerplatser](warehouse-how-to-create-individual-bins.md) och [skapar lagerplatstyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zoner

Om du vill strukturera lagerplatser under zoner kan du göra det på sidan **Zoner**. När du tilldelar en zon till lagerplatser kopierar [!INCLUDE [prod_short](includes/prod_short.md)] informationen från zonen till lagerplatserna. Du kan också välja att ställa in en zon och använda lagerplatser separat för att organisera distributionslagret. Läs mer om zoner på [Ställa in Warehouse Management](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standarddimensioner för platser

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem med olika rapporteringsverktyg. Till exempel kan dimensioner indikera avdelningen eller projektet en post kom från. Med standarddimensioner kan användare undvika misstag och behöva ange dimensioner manuellt på transaktionsnivån om alla varor kommer från en enda plats och avdelning.

Du anger standardmått för en plats på sidan **Platskort** genom att välja **Dimensioner**. Därefter kopplas platsens standarddimensioner till dokument när du väljer lagerställe på en rad.

* Överföringsorder
* Inventeringsorder
* Lagerutleveranser
* Lagerinleveranser
* Artikeljournaler

Om det behövs kan du ta bort eller ändra dimensionen på raden. På fältet **värdebokföring** kan du kräva att personer anger dimensioner för platser innan de kan bokföra en transaktion. Om du vill att användarna endast ska kunna välja vissa dimensionsvärden kan du ange värdena i fältet **Tillåtna värdefilter**. Du kan också ta med dimensions värden för lagerställe på sidan **standard dimensionsprioriteringar** och **Dimensionskombinationer** för kombinationer av prioritet och dimensionsregler.

Eftersom överföringsorder dokument och grupperingsjournalen innehåller mer än en plats, är order som används för att ange data viktig. Standarddimensioner kopieras från fältet senaste plats (transitlagerstället ignoreras).

### <a name="example-of-default-dimensions-on-locations"></a>Exempel på standardmått på lagerställen

Följande exempel visar hur standarddimensionen används.

Du har följande dimensionsinställningar:

* Lagerställe ÖST. Avdelningsdimension är ADM
* Lagerställe VÄST. Avdelningsdimension är PROD

Du anger lagerstället i en överföringsorder så här:

1. Från lagerställe = ÖST
2. Till lagerställe = VÄST

Dimensionen PROD kommer att kopieras från lagerställe VÄST.

Du fyller i fälten i motsatt ordning, enligt följande:

1. Till lagerställe = VÄST
2. Från lagerställe = ÖST

Dimensionen ADM kommer att kopieras från lagerställe ÖST.

## <a name="see-also"></a>Se även

[Hantera lager](inventory-manage-inventory.md)  
[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)  
[Skapa lagerställen](warehouse-how-to-create-individual-bins.md)  
[Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
