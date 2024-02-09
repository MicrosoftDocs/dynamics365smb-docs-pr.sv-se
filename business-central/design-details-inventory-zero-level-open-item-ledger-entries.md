---
title: Lagervärdet noll öppna artikeltransaktioner
description: Denna artikel adresserar problem där lagernivån är noll fastän öppna artikeltransaktioner finns.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-known-item-application-issue"></a>Designdetaljer: Kända problem med artikelkopplingar
Denna artikel adresserar problem där lagernivån är noll fastän öppna artikeltransaktioner finns i [!INCLUDE[prod_short](includes/prod_short.md)].  

Artikeln börjar med att lista vanliga symptom på problemet, följt av grunderna för artikelkoppling för att ge stöd åt de beskrivna orsakerna till detta problem. I slutet av artikeln finns en problemlösning med syfte att adressera sådana öppna artikeltransaktioner.  

## <a name="symptoms-of-the-issue"></a>Symptom på problemet
 Vanliga symptom på problem med nollager även då öppna artikeltransaktioner finns är följande:  

-   Följande meddelande visas när du försöker stänga en lagerperiod: ”Lagret kan inte stängas eftersom lagersaldot är negativt för en eller flera artiklar.”  

-   En bokföringssituation för artikeltransaktioner där både en utgående artikeltransaktion och dess relaterade, inkommande artikeltransaktion är öppna.  

     Se följande exempel på en situation med en artikeltransaktion.  

     |Löpnr|Bokföringsdatum|Transaktionstyp|Dokumenttyp|Dokumentnummer|Artikelnummer|Platskod|Antal|Kost.belopp (aktuellt)|Fakturerat antal|Återstående antal|Öppna|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
     |334|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|1|10|1|1|Ja|  

## <a name="basics-of-item-application"></a>Grunderna för artikelkoppling
 En artikelkopplingstransaktion skapas för varje lagertransaktion avsedd att koppla kostnadsmottagaren till kostnadskällan så att kostnaden kan vidarebefordras enligt värderingsprincipen. Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md).  

-   Artikelkopplingstransaktionen skapas för en inkommande artikeltransaktionen när artikeltransaktionen skapas.  

-   För en artikelkopplingstransaktion skapas artikelkopplingstransaktionen när artikeltransaktionen bokförs, OM det finns en öppen inkommande artikeltransaktion med en disponibel kvantitet att tillgå. Om det inte finns några öppna inkommande artikeltransaktioner att tillgå förblir den utgående artikeltransaktionen öppen tills en inkommande artikeltransaktion att tillgå bokförs.  

 Det finns två typer av artikelkopplingar:  

-   Antalskoppling  

-   Kost.koppling  

### <a name="quantity-application"></a>Antalskoppling
 Antalstillämpningar görs för alla lagertransaktioner och skapas automatiskt eller manuellt i vissa processer. Vid manuell framställning skapas kopplingar till mängdtillämpningar som fast tillämpning.  

 I följande diagram visas hur mängdtillämpningar skapas.  

![Kostnadsjusteringsflöde från inköp till försäljning.](media/helene/TechArticleInventoryZero2.png "Kostnadsjusteringsflöde från inköp till försäljning")

 Observera att artikeltransaktion 1 ovan (inköp) är både artikelns leverantör och kostnadskälla för den kopplade artikeltransaktionen, Artikeltransaktion 2 (försäljning).  

> [!NOTE]  
>  Om den utgående artikeltransaktionen värderas via genomsnittskostnaden är tillämpad inkommande artikeltransaktion inte unik kostnadskälla. Den spelar bara en roll för beräkningen av genomsnittskostnaden för perioden.  

### <a name="cost-application"></a>Kost.koppling
Kostnadskopplingar skapas endast för inkommande transaktioner där fältet **Koppla från artikellöpnr** fylls i för att skapa en fast koppling. Detta inträffar vanligen i samband med en försäljningskreditnota eller ett annullerat utleveransscenario. Kostnadskopplingen innebär att artikeln återinträder i lagret till samma kostnad som när den levererades.  

I följande diagram visas hur kostnadstillämpningar skapas.  

|Löpnr|Bokföringsdatum|Transaktionstyp|Dokumenttyp|Dokumentnummer|Artikelnummer|Platskod|Antal|Kost.belopp (aktuellt)|Fakturerat antal|Återstående antal|Öppna|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
|334|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|1|10|1|1|Ja|  

 Observera ovan att den inkommande artikeltransaktionen 3 (försäljningsreturorder) är en kostnadsmottagare för den ursprungliga utgående artikeltransaktionen 2 (försäljning).  

## <a name="illustration-of-a-basic-cost-flow"></a>Bild av ett grundläggande kostnadsflöde
 Anta ett fullständigt kostnadsflöde där en artikel inlevereras, levereras och faktureras, returneras med exakt\-kostnadsåterföring, och sedan skickas igen.  

 I följande diagram illustreras kostnadsflödet.  

![Kostnadsjusteringsflöde från försäljning till försäljningsretur.](media/helene/TechArticleInventoryZero4.png "Kostnadsjusteringsflöde från försäljning till försäljningsretur")

 Observera ovan att kostnaden vidarebefordras till artikeltransaktion 2 (försäljning), därefter till artikeltransaktion 3 (försäljningsreturorder), och slutligen till artikeltransaktion 4 (försäljning 2).  

## <a name="reasons-for-the-issue"></a>Orsakerna till problemet
 Vanliga symptom på problem med nollager även då öppna artikeltransaktioner finns kan exempelvis vara följande:  

-   Scenario 1: En utleverans och en faktura bokförs även om artikeln inte är tillgänglig. Bokföringen kostnadsåterförs sedan exakt med en försäljningskreditnota.  

-   Scenario 2: En utleverans bokförs även om artikeln inte är tillgänglig. Bokföringen annulleras sedan bort med hjälp av funktionen Återställ utleverans.  

 I följande diagram illustreras hur artikeltillämpningar görs i respektive fall.  

![Kostnadsjusteringsflödet skickas i båda riktningarna.](media/helene/TechArticleInventoryZero6.png "Kostnadsjusteringsflödet skickas i båda riktningarna")  

 Observera ovan att en kostnadsansökan görs (representerat av de blå pilarna) så att artikeltransaktion 2 (försäljningsreturorder) tilldelas samma kostnader som den artikeltransaktion som den återför, artikeltransaktion 1 (försäljning 1). En antalskoppling (som representeras av röda pilar) görs emellertid inte.  

 Artikeltransaktion 2 (försäljningsreturorder) kan inte vara både en kostnadsmottagaren av den ursprungliga artikeltransaktionen och samtidigt vara en leverantör av artiklar och deras kostnadskälla. Därför förblir den ursprungliga artikeltransaktionen 1 (försäljning 1) öppen tills en giltig källa visas.  

## <a name="identifying-the-issue"></a>Identifierar problemet
 Om du vill ta reda på om de öppna artikeltransaktionerna skapas gör du så här för respektive scenario:  

 För scenario 1, identifiera problemet på följande sätt:  

-   På sidan **Bokförd försäljningskreditnota** eller **Bokförd returinlevns**, leta upp fältet **koppla\-från artikellöpnr** för att se om fältet är ifyllt, och om så är fallet, till vilken artikeltransaktionsom returkvittot kostnadstillämpas.  

 För scenario 2, identifiera problemet på något av följande sätt:  

-   Sök efter en öppen utgående artikeltransaktion och en inkommande artikeltransaktionen med samma nummer i fältet **Dokumentnr.**, och Ja i fältet **Korrigering**. Se följande exempel på en sådan situation med en artikeltransaktion.  

|Löpnr|Bokföringsdatum|Transaktionstyp|Dokumenttyp|Dokumentnummer|Artikelnummer|Platskod|Antal|Kost.belopp (aktuellt)|Fakturerat antal|Återstående antal|Öppna|Rättningstransaktion|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|Nr|  
|334|2018-01-28|Försäljning|Utleverans|102043|TEST|BLÅ|1|10|1|1|Ja|**Ja**|  

-   På sidan **Bokförd försäljningsleverans** letar du upp fältet **Koppla från artikellöpnr** för att se om fältet är ifyllt, och om så är fallet, till vilken artikeltransaktion som returkvittot kostnadstillämpas.  

> [!NOTE]  
>  Kostnadstillämpningar kan inte identifieras på sidan **Kopplade artikeltransaktioner** eftersom det endast visar antalsprogram.  

 I båda fallen bör du identifiera involverad kostnadstillämpning enligt följande:  

1.  Öppna tabellen **Artikelkopplingstransaktion**.  

2.  Filtrera fältet **Artikeltrans.löpnr** med hjälp av artikeltransaktionen Antalet försäljningsreturorder.  

3.  Analysera artikelkopplingstransaktionen, med hänsyn tagen till följande:  

     Om fältet **utgående artikeltrans.nr** fylls i för en inkommande artikeltransaktion (positiv kvantitet) innebär det att den inkommande artikeltransaktionen är kostnadsmottagare för den utgående artikeltransaktionen.  

     Se följande exempel på en situation med en artikeltillämpning.  

     |Löpnr|Artikeltrans.löpnr|inkommande artikeltrans.nr|utgående artikeltrans.nr|Antal|Bokföringsdatum|Kost.koppling|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|2018-01-28|Ja|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Observera ovan att inkommande artikeltransaktion 334 är kostnader som har kopplats till utgående artikeltransaktion 333.  

## <a name="workaround-for-the-issue"></a>Åtgärda problemet
 På sidan **Artikeljournal** bokför du följande rader för den aktuella artikeln:  

-   En positiv justering för att stänga en öppen, utgående artikeltransaktion.  

-   En negativ justering med samma kvantitet.  

     Den här justeringen balanserar lagerökningen som orsakas av den positiva justeringen och stänger den öppna inkommande artikeltransaktionen.  

 Resultatet blir att lagret är noll och alla artikeltransaktioner har avslutats.  

## <a name="see-also"></a>Se även
[Designdetaljer: artikelkoppling](design-details-item-application.md)   
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
