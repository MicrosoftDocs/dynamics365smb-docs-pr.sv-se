---
title: "öppna artikeltransaktioner"
description: "Lär dig varför lagernivån är noll fastän öppna artikeltransaktioner finns."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e25721b0c79a87f4201314a0f3556f969a110e18
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-known-item-application-issue"></a>Designdetaljer: Kända problem med artikelkopplingar
Denna artikel adresserar problem där lagernivån är noll fastän öppna artikeltransaktioner finns i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Artikeln börjar med att lista vanliga symptom på problemet, följt av grunderna för artikelkoppling för att ge stöd åt de beskrivna orsakerna till detta problem. I slutet av artikeln finns en problemlösning med syfte att adressera sådana öppna artikeltransaktioner.  

## <a name="symptoms-of-the-issue"></a>Symptom på problemet  
 Vanliga symptom på problem med nollager även då öppna artikeltransaktioner finns är följande:  

-   Följande meddelande visas när du försöker stänga en lagerperiod: ”Lagret kan inte stängas eftersom lagersaldot är negativt för en eller flera artiklar.”  

-   En bokföringssituation för artikeltransaktioner där både en avgående artikeltransaktion och dess relaterade, ankommande artikeltransaktion är öppna.  

     Se följande exempel på en situation med en artikeltransaktion.  

     |Löpnr|Bokföringsdatum|Transaktionstyp|Dokumenttyp|Dokumentnummer|Artikelnummer|Platskod|Antal|Kost.belopp (aktuellt)|Fakturerat antal|Återstående antal|Öppna|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
     |334|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|1|10|1|1|Ja|  

<!--![Why is inventory zero 1](media/helene/TechArticleInventoryZero1.png "Whyisinventoryzero\_1")-->

## <a name="basics-of-item-application"></a>Grunderna för artikelkoppling  
 En artikelkopplingstransaktion skapas för varje lagertransaktion avsedd att koppla kostnadsmottagaren till kostnadskällan så att kostnaden kan vidarebefordras enligt värderingsprincipen. Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md).  

-   Artikelkopplingstransaktionen skapas för en ankommande artikeltransaktionen när artikeltransaktionen skapas.  

-   För en artikelkopplingstransaktion skapas artikelkopplingstransaktionen när artikeltransaktionen bokförs, OM det finns en öppen ankommande artikeltransaktion med en disponibel kvantitet att tillgå. Om det inte finns några öppna ankommande artikeltransaktioner att tillgå förblir den avgående artikeltransaktionen öppen tills en ankommande artikeltransaktion att tillgå bokförs.  

 Det finns två typer av artikelkopplingar:  

-   Antalskoppling  

-   Kost.koppling  

### <a name="quantity-application"></a>Antalskoppling  
 Antalstillämpningar görs för alla lagertransaktioner och skapas automatiskt eller manuellt i vissa processer. Vid manuell framställning skapas kopplingar till mängdtillämpningar som fast tillämpning.  

 I följande diagram visas hur mängdtillämpningar skapas.  

![Varför är lagervärdet noll 2](media/helene/TechArticleInventoryZero2.png "Whyisinventoryzero\_2")

 Observera att artikeltransaktion 1 ovan (inköp) är både artikelns leverantör och kostnadskälla för den kopplade artikeltransaktionen, Artikeltransaktion 2 (försäljning).  

> [!NOTE]  
>  Om den avgående artikeltransaktionen värderas via genomsnittskostnaden är tillämpad ankommande artikeltransaktion inte unik kostnadskälla. Den spelar bara en roll för beräkningen av genomsnittskostnaden för perioden.  

### <a name="cost-application"></a>Kost.koppling  
Kostnadskopplingar skapas endast för ankommande transaktioner där fältet **Koppla från artikellöpnr** fylls i för att skapa en fast koppling. Detta inträffar vanligen i samband med en försäljningskreditnota eller ett annullerat utleveransscenario. Kostnadskopplingen innebär att artikeln återinträder i lagret till samma kostnad som när den levererades.  

I följande diagram visas hur kostnadstillämpningar skapas.  

|Löpnr|Bokföringsdatum|Transaktionstyp|Dokumenttyp|Dokumentnummer|Artikelnummer|Platskod|Antal|Kost.belopp (aktuellt)|Fakturerat antal|Återstående antal|Öppna|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
|334|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|1|10|1|1|Ja|  
<!--![Why is inventory zero 3](media/helene/TechArticleInventoryZero3.png "Whyisinventoryzero\_3")-->

 Observera ovan att den ankommande artikeltransaktionen 3 (försäljningsreturorder) är en kostnadsmottagare för den ursprungliga avgående artikeltransaktionen 2 (försäljning).  

## <a name="illustration-of-a-basic-cost-flow"></a>Bild av ett grundläggande kostnadsflöde  
 Anta ett fullständigt kostnadsflöde där en artikel inlevereras, levereras och faktureras, returneras med exakt\-kostnadsåterföring, och sedan skickas igen.  

 I följande diagram illustreras kostnadsflödet.  

![Varför är lagervärdet noll 4](media/helene/TechArticleInventoryZero4.png "Whyisinventoryzero\_4")

 Observera ovan att kostnaden vidarebefordras till artikeltransaktion 2 (försäljning), därefter till artikeltransaktion 3 (försäljningsreturorder), och slutligen till artikeltransaktion 4 (försäljning 2).  

## <a name="reasons-for-the-issue"></a>Orsakerna till problemet  
 Vanliga symptom på problem med nollager även då öppna artikeltransaktioner finns kan exempelvis vara följande:  

-   Scenario 1: En utleverans och en faktura bokförs även om artikeln inte är tillgänglig. Bokföringen kostnadsåterförs sedan exakt med en försäljningskreditnota.  

-   Scenario 2: En utleverans bokförs även om artikeln inte är tillgänglig. Bokföringen annulleras sedan bort med hjälp av funktionen Återställ utleverans.  

 I följande diagram illustreras hur artikeltillämpningar görs i respektive fall.  

![Varför är lagervärdet noll 6](media/helene/TechArticleInventoryZero6.png "Whyisinventoryzero\_6")  

 Observera ovan att en kostnadsansökan görs (representerat av de blå pilarna) så att artikeltransaktion 2 (försäljningsreturorder) tilldelas samma kostnader som den artikeltransaktion som den återför, artikeltransaktion 1 (försäljning 1). En antalskoppling (som representeras av röda pilar) görs emellertid inte.  

 Artikeltransaktion 2 (försäljningsreturorder) kan inte vara både en kostnadsmottagaren av den ursprungliga artikeltransaktionen och samtidigt vara en leverantör av artiklar och deras kostnadskälla. Därför förblir den ursprungliga artikeltransaktionen 1 (försäljning 1) öppen tills en giltig källa visas.  

## <a name="identifying-the-issue"></a>Identifierar problemet  
 Om du vill ta reda på om de öppna artikeltransaktionerna skapas gör du så här för respektive scenario:  

 För scenario 1, identifiera problemet på följande sätt:  

-   I fönstret **Bokförd försäljningskreditnota** eller **Bokförd returinlevns**, leta upp fältet **koppla\-från artikellöpnr** för att se om fältet är ifyllt, och om så är fallet, till vilken artikeltransaktionsom returkvittot kostnadstillämpas.  

 För scenario 2, identifiera problemet på något av följande sätt:  

-   Sök efter en öppen utgående artikeltransaktion och en ankommande artikeltransaktionen med samma nummer i fältet **Dokumentnr.**, och Ja i fältet **Korrigering**. Se följande exempel på en sådan situation med en artikeltransaktion.  

|Löpnr|Bokföringsdatum|Transaktionstyp|Dokumenttyp|Dokumentnummer|Artikelnummer|Platskod|Antal|Kost.belopp (aktuellt)|Fakturerat antal|Återstående antal|Öppna|Rättningstransaktion|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|Nr|  
|334|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|1|10|1|1|Ja|**Ja**|  
<!--![Why is inventory zero 7](media/helene/TechArticleInventoryZero7.png "Whyisinventoryzero\_7")-->

-   I fönstret **Bokförd försäljningsleverans** letar du upp fältet **Koppla från artikellöpnr** för att se om fältet är ifyllt, och om så är fallet, till vilken artikeltransaktion som returkvittot kostnadstillämpas.  

> [!NOTE]  
>  Kostnadstillämpningar kan inte identifieras i fönstret **Kopplade artikeltransaktioner** eftersom det endast visar antalsprogram.  

 I båda fallen bör du identifiera involverad kostnadstillämpning enligt följande:  

1.  Öppna tabellen **Artikelkopplingstransaktion**.  

2.  Filtrera fältet **Artikeltrans.löpnr** med hjälp av artikeltransaktionen Antalet försäljningsreturorder.  

3.  Analysera artikelkopplingstransaktionen, med hänsyn tagen till följande:  

     Om fältet **Avgående artikeltrans.nr** fylls i för en ankommande artikeltransaktion (positiv kvantitet) innebär det att den ankommande artikeltransaktionen är kostnadsmottagare för den avgående artikeltransaktionen.  

     Se följande exempel på en situation med en artikeltillämpning.  

     |Löpnr|Artikeltrans.löpnr|Ankommande artikeltrans.nr|Avgående artikeltrans.nr|Antal|Bokföringsdatum|Kost.koppling|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|2018-01-28|Ja|  
<!--![Why is inventory zero 8](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Observera ovan att ankommande artikeltransaktion 334 är kostnader som har kopplats till avgående artikeltransaktion 333.  

## <a name="workaround-for-the-issue"></a>Åtgärda problemet  
 I fönstret **Artikeljournal** bokför du följande rader för den aktuella artikeln:  

-   En positiv justering för att stänga en öppen, utgående artikeltransaktion.  

-   En negativ justering med samma kvantitet.  

     Den här justeringen balanserar lagerökningen som orsakas av den positiva justeringen och stänger den öppna ankommande artikeltransaktionen.  

 Resultatet blir att lagret är noll och alla artikeltransaktioner har avslutats.  

## <a name="see-also"></a>Se även  
[Designdetaljer: artikelkoppling](design-details-item-application.md)   
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  

