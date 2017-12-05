---
title: Om planeringsfunktioner | Microsoft Docs
description: "I planeringssystemet beaktas alla efterfråge- och tillgångsdata, resultaten nettoberäknas och förslag på balansering av tillgång för att uppfylla efterfrågan skapas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a00f88aaf70464c8911d59b829b08dda900dc474
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="about-planning-functionality"></a>Om planeringsfunktioner
I planeringssystemet beaktas alla efterfråge- och tillgångsdata, resultaten nettoberäknas och förslag på balansering av tillgång för att uppfylla efterfrågan skapas.  

Mer information finns i [Designdetaljer: Leveransplanering](design-details-supply-planning.md)  

> [!NOTE]  
> Alla de fält som nämns i det här avsnittet hittar du i beskrivningen för att förstå deras funktion. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Tillgång och efterfrågan  
Planering innehåller två element: tillgång och efterfrågan. Dessa två element måste balanseras för att se till att efterfrågan uppfylls i tid och så kostnadseffektivt som möjligt.  

- Efterfrågan är den term som vanligtvis används för alla typer av bruttobehov, t.ex. försäljningsorder, serviceorder, komponentbehov från montering eller produktionsorder, utgående överföringar, avropsorder eller prognoser. Utöver dessa, tillåts även en del andra typer av efterfrågan - t.ex. negativa produktions- eller inköpsorder, negativt lager och inköpsreturer.  
- Tillgång är det ord som vanligtvis används för alla typer av återanskaffning, t.ex. lager, inköpsorder, monteringsorder, produktionsorder eller ankommande överföring. På motsvarande sätt kan det finnas negativa försäljnings- eller serviceorder, negativt komponentbehov eller försäljningsretur – vilka alla på ett sätt också representerar tillgång.  

Ett annat mål med planeringssystemet är att se till att lagret inte blir onödigt stort. Om det uppstår en minskad efterfrågan, får du i planeringssystemet ett förslag om att skjuta upp, minska antalet eller annullera befintliga återanskaffningsorder.  

## <a name="planning-calculation"></a>Planeringsberäkning  
Planeringssystemet drivs av förväntad och faktisk kundefterfrågan samt även parametrar för lagerbeställningar. Om du kör planeringsberäkningen får du i programmet ett förslag på särskilda åtgärder (åtgärdsmeddelanden) som du ska vidta för eventuell återanskaffning från leverantörer, överföringar mellan distributionslager eller produktion. Om det redan finns återanskaffningsorder kan de förslagna åtgärderna vara att du till exempel ska öka eller påskynda order som motsvarar förändringarna i efterfrågan.  

Grunden för planeringsrutinen är beräkningen av brutto till netto. Nettobehoven styr släppningen av planerade order, som planeras utifrån operationsföljdsinformation (tillverkade artiklar) eller ledtid på artikelkortet (inköpta artiklar). Utsläppningsantalet för planerade order baseras på planeringsberäkningen och påverkas av parametrarna som ställs in på de enskilda artikelkorten.  

## <a name="planning-with-manual-transfer-orders"></a>Planera med manuella överföringsorder
Som du ser i fältet **Återanskaffningssystem** på ett kort för lagerställeenhet, kan planeringssystemet konfigureras till att skapa överföringsorder som balanserar leverans och behov mellan lagerställen.  

Förutom sådana automatiska överföringsorder kanske du ibland behöver utföra en allmän flyttning av lagerkvantiteter till en annan plats, oavsett befintligt behov. För det här syftet kan du skapa en överföringsorder manuellt för det antal som ska flyttas. För att vara säker på att planeringssystemet inte försöker att manipulera denna manuella överföringsorder, måste du ange fältet **Planeringsflexibilitet** på raden eller raderna till Ingen.  

Om du å andra sidan vill att planeringssystemet ska justera överföringsorderantalet och ange fältet **Planeringsflexibilitet** till standardvärdet Obegränsad.

## <a name="planning-parameters"></a>Planeringsparametrar  
Planeringsparametrarna styr när och hur återskaffningen sker och hur mycket som ska återanskaffas beroende på de olika inställningarna på artikelkortet (eller lagerställeenheten) och produktionsinställningarna.  

Följande planeringsparametrar finns på artikeln eller kortet för lagerställeenheten:  

-   Max. utjämningsperiod  
-   Max. avvikelsekvantitet  
-   Partiformningsmetod  
-   Beställningspunkt
-   Beställningsgräns  
-   Överflödesnivå  
-   Tidsenhet  
-   Partiackumuleringsperiod  
-   Omplaneringsperiod  
-   Beställningsantal  
-   Säkerhetsledtid  
-   Säkerhetslager  
-   Monteringsmetod  
-   Produktionsprincip  

Följande beställningsprinciper finns på artikeln eller kortet för lagerställeenheten:  

-   Min. partistorlek  
-   Max. partistorlek  
-   Partistorleksmultipel  

Inställningsfälten för planering i fönstret **Produktionsinställningar** inkluderar:  

-   Dynamisk lägsta-nivå-kod  
-   Aktuell prod.prognos  
-   Prognos på lagerställen  
-   Standard säkerhetsledtid  
-   Tom överflödesnivå  
-   Prod.prog./nettobehov   
-   Komp. vid lagerställe  
-   Standard för max. utjämningsperiod  
-   Max. avvikelsekvantitet  

Mer information finns i [Designdetaljer: Planläggningsparametrar](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Andra viktiga planeringsfält
### <a name="planning-flexibility"></a>Planeringsflexibilitet
På de flesta leveransorder, till exempel produktionsorder, kan du välja **obegränsad** eller **ingen** i fältet **Planeringsflexibilitet** på raderna.

Anger om leveransen som representeras av produktionsorderraden tas i beaktande av planeringssystemet när ett åtgärdsmeddelande beräknas.
Om fältet innehåller alternativet **Obegränsad**, ingår raden när meddelandena beräknas. Om fältet innehåller alternativet **Ingen**, är raden fast (går inte att ändra) och ingår inte när åtgärdsmeddelandena beräknas.

### <a name="warning"></a>Varning
Informationsfältet **varning** i fönstret **planeringsförslag** informerar dig om att alla planeringsrader som skapats för en ovanlig situation med text där användaren kan välja att få mer information. Följande typer av varningar förekommer:

- Nödsituation
- Undantag
- Observera!
- Nödsituation

Varningen för nödsituation visas i två olika situationer:

- Lagret är negativt på startdatumet för planeringen.
- Det finns antedaterade försörjnings- eller behovshändelser.

Om lagernivån för en artikel är negativ på startdatumet för planeringen föreslår systemet en nödleveransorder för det negativa antalet med leverans på startdatumet för planeringen. I varningstexten anges startdatumet och antalet i nödordern.

Eventuella dokumentrader med förfallodatum före startdatumet för planeringen konsolideras i en nödleveransorder för artikeln med leverans på startdatumet för planeringen.

### <a name="exception"></a>Undantag
Undantagsvarningen visas om det planerade disponibla lagret sjunker under nivån för säkerhetslagret.

Planeringssystemet föreslår en leveransorder för att uppfylla behovet på förfallodatumet. I varningstexten framgår vilket antal som gäller för artikelns säkerhetslager och det datum då det understigs.

Att bryta säkerhetslagrets nivå betraktas som ett undantag eftersom det inte bör inträffa om beställningspunkten har ställts in korrekt.

> [!NOTE]
> Tillgången på planeringsrader med undantagsvarningar ändras normalt inte enligt planeringsparametrarna. I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet. Du kan dock ange att planeringskörningen ska följa vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar. Mer information finns i avsnittet om planeringsparametrar för undantagvarningar i Beräkna plan - planeringsförslag. .

### <a name="attention"></a>Observera!
Den här varningen visas i två olika situationer:

- Startdatumet för planeringen ligger tidigare än arbetsdatumet.
- Planeringsraden föreslår att en släppt inköps- eller produktionsorder ändras.

> [!NOTE]
> Vid planering av rader med varningar är fältet **Acceptera åtgärdsmeddelande** inte markerat, eftersom planeraren förväntas att undersöka dessa rader innan planen utförs.

## <a name="see-also"></a>Se även  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
[Planerad](production-planning.md)   
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

