---
title: Om planeringsfunktioner
description: Lär dig hur planering använder efterfråge- och tillgångsdata för att föreslå hur du balanserar utbudet för att möta efterfrågan.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '5430,'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="about-planning-functionality"></a>Om planeringsfunktioner

I planeringssystemet beaktas alla efterfråge- och tillgångsdata, resultaten nettoberäknas och förslag på balansering av tillgång för att uppfylla efterfrågan skapas.  

Mer information finns i [Designdetaljer: Leveransplanering](design-details-supply-planning.md)  

> [!NOTE]  
> Alla de fält som nämns i det här avsnittet hittar du i beskrivningen för att förstå deras funktion. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="supply-and-demand"></a>Tillgång och efterfrågan

Planering innehåller två element: tillgång och efterfrågan. Dessa måste balanseras för att säkerställa att efterfrågan tillgodoses.  

- Efterfrågan är det ord som vanligtvis används för alla typer av bruttobehov, t.ex. försäljningsorder, serviceorder eller komponentbehov för monterings- eller produktionsorder, utgående överföring, avropsorder eller prognos. Därutöver finns även andra typer av efterfrågan, t. ex. negativa produktions- eller inköpsorder, negativt lager och inköpsreturer.  
- Tillgång avser alla typer av återanskaffning, t.ex. lager, inköpsorder, monteringsorder, produktionsorder eller inkommande överföring. På motsvarande sätt kan det finnas negativa försäljnings- eller serviceorder, negativt komponentbehov eller försäljningsretur som också representerar tillgång.  

Ett annat mål med planeringssystemet är att se till att lagret inte blir onödigt stort. Om det uppstår en minskad efterfrågan, får du i planeringssystemet ett förslag om att skjuta upp, minska antalet eller annullera befintliga återanskaffningsorder.  

## <a name="planning-calculation"></a>Planeringsberäkning

Planeringssystemet drivs av förväntad och faktisk kundefterfrågan samt även parametrar för lagerbeställningar. Om du kör planeringsberäkningen får du i programmet ett förslag på särskilda åtgärder ([åtgärdsmeddelanden](production-how-to-run-mps-and-mrp.md#action-messages)) som du ska vidta för eventuell återanskaffning från leverantörer, överföringar mellan distributionslager eller produktion. Om det redan finns återanskaffningsorder kan de förslagna åtgärderna vara att du till exempel ska öka eller påskynda order som motsvarar förändringarna i efterfrågan.  

Grunden för planeringsrutinen är beräkningen av brutto till netto. Nettobehoven styr släppningen av planerade order, som planeras utifrån operationsföljdsinformation (tillverkade artiklar) eller ledtid på artikelkortet (inköpta artiklar). Utsläppningsantalet för planerade order baseras på planeringsberäkningen och påverkas av parametrarna som ställs in på de enskilda artikelkorten.  

> [!TIP]
> Planeringssystemet är beroende av hur organisationen använder lagerställen. Mer information finns i [Planera med eller utan lagerställen](production-planning-with-without-locations.md).

## <a name="planning-with-manual-transfer-orders"></a>Planera med manuella överföringsorder

I fältet **Återanskaffningssystem** på ett kort för lagerställeenhet kan du konfigurera planeringssystemet i syfte att skapa överföringsorder som balanserar tillgång och efterfrågan mellan olika lagerställen.  

Förutom sådana automatiska överföringsorder kanske du ibland behöver utföra en allmän flyttning av lagerkvantiteter till en annan plats, oavsett befintligt behov. För det här syftet kan du skapa en överföringsorder manuellt för det antal som ska flyttas. För att vara säker på att planeringssystemet inte försöker att manipulera denna manuella överföringsorder, måste du ange fältet **Planeringsflexibilitet** på raden eller raderna till Ingen.  

Om du å andra sidan vill att planeringssystemet ska justera överföringsorderantalet och ange fältet **Planeringsflexibilitet** till standardvärdet Obegränsad.

## <a name="planning-parameters"></a>Planeringsparametrar

Planeringsparametrarna styr när och hur återskaffningen sker och hur mycket som ska återanskaffas beroende på de olika inställningarna på artikelkortet (eller lagerställeenheten) och produktionsinställningarna.  

Följande planeringsparametrar finns på artikeln eller kortet för lagerställeenheten:  

- Max. utjämningsperiod  
- Max. avvikelsekvantitet  
- Partiformningsmetod  
- Beställningspunkt
- Beställningsgräns  
- Överflödesnivå  
- Tidsenhet  
- Partiackumuleringsperiod  
- Omplaneringsperiod  
- Beställningsantal  
- Säkerhetsledtid  
- Säkerhetslager  
- Monteringsmetod  
- Produktionsprincip  

Följande beställningsprinciper finns på artikeln eller kortet för lagerställeenheten:  

- Min. partistorlek  
- Max. partistorlek  
- Partistorleksmultipel  

Inställningsfälten för planering på sidan **Produktionsinställningar** inkluderar:  

- Dynamisk lägsta-nivå-kod  
- Aktuell efterfrågeprognos  
- Prognos på lagerställen  
- Standard säkerhetsledtid  
- Tom överflödesnivå  
- Prod.prog./nettobehov
- Komp. vid lagerställe  
- Standard för max. utjämningsperiod  
- Standardtid för dämpare  

Mer information finns i [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Andra viktiga planeringsfält

### <a name="planning-flexibility"></a>Planeringsflexibilitet

På de flesta leveransorder, till exempel produktionsorder, kan du välja **obegränsad** eller **ingen** i fältet **Planeringsflexibilitet** på raderna.

Anger om leveransen som representeras av produktionsorderraden tas i beaktande av planeringssystemet när ett åtgärdsmeddelande beräknas.
Om fältet innehåller alternativet **Obegränsad**, ingår raden när meddelandena beräknas. Om fältet innehåller alternativet **Ingen**, är raden fast (går inte att ändra) och ingår inte när åtgärdsmeddelandena beräknas.

### <a name="warning"></a>Varning

Informationsfältet **varning** på sidan **planeringsförslag** informerar dig om att alla planeringsrader som skapats för en ovanlig situation med text där användaren kan välja att få mer information. Följande typer av varningar förekommer:

- Nödsituation
- Undantag
- Observera!

### <a name="emergency"></a>Nödsituation

Varningen för nödsituation visas i två olika situationer:

- Lagret är negativt på startdatumet för planeringen.
- Det finns antedaterade försörjnings- eller behovshändelser.

Om lagernivån för en artikel är negativ på startdatumet för planeringen föreslår planeringssystemet en nödleveransorder för det negativa antalet med leverans på startdatumet för planeringen. I varningstexten anges startdatumet och antalet i nödordern.

Eventuella dokumentrader med förfallodatum före startdatumet för planeringen konsolideras i en nödleveransorder för artikeln med leverans på startdatumet för planeringen.

### <a name="exception"></a>Undantag

Undantagsvarningen visas om det planerade tillgängliga lagret sjunker under nivån för säkerhetslagret.

Planeringssystemet föreslår en leveransorder för att uppfylla behovet på förfallodatumet. I varningstexten framgår vilket antal som gäller för artikelns säkerhetslager och det datum då det understigs.

Att bryta mot säkerhetslagrets nivå betraktas som ett undantag eftersom det inte bör inträffa om återbeställningspunkten har ställts in korrekt.

> [!NOTE]
> Tillgången på planeringsrader med undantagsvarningar ändras normalt inte enligt planeringsparametrarna. I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet. Du kan dock ange att planeringskörningen ska följa vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar. Mer information finns i beskrivningen av fältet **Respektera planeringsparametrar för undantagsvarningar** i artikeln [Kör hela planeringen, MPS eller MRP](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Observera!

Varningen visas i två olika situationer:

- Startdatumet för planeringen ligger tidigare än arbetsdatumet.
- Planeringsraden föreslår att en släppt inköps- eller produktionsorder ändras.

> [!NOTE]
> Vid planering av rader med varningar är fältet **Acceptera åtgärdsmeddelande** inte markerat, eftersom planeraren förväntas att undersöka dessa rader innan planen utförs.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Planeringsförslag och inköpskalkylark

På det sätt som beskrivs i [Planera](production-planning.md) kan du välja mellan två kalkylblad för de flesta planeringsaktiviteter, planeringsförslaget och inköpskalkylarket. De flesta processer beskrivs utifrån planeringsförslaget, men det finns ett par scenarier där inköpskalkylarket är prioriterat.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

### <a name="requisition-worksheet"></a>Inköpskalkylark

På sidan **Inköpskalkylark** visas en lista över artiklar som behöver beställas. Du kan ange artiklar i kalkylarket på följande sätt:

- Ange artiklarna manuellt i förslaget och fyll i aktuella fält.

- Använd batchprojektet **Skapa inköpsförslag**. Genom detta beräknas en påfyllningsplan för artiklar och enheter som har skapats med påfyllningssystemet **Inköp** eller **Överföring**. När du använder detta batchprojekt fylls fältet **Åtgärdsmeddelande** automatiskt i med ett förslag på en åtgärd för att fylla på artikeln. Detta kan till exempel innebära att artikelantalet i en befintlig order ökas eller att en ny order skapas.

- Om du har använt batchprojektet **Skapa inköpsförslag** från sidan **Planeringsförslag** för att beräkna en återanskaffningsplan kan du använda batchprojektet **Verkställ åtgärdsmeddelande** för att kopiera inköps- och överföringsorderförslag från planeringsförslaget till inköpskalkylarket. Detta är praktiskt om olika användare är ansvariga för hantering av produktionsorder och inköps-/överföringsorder.

- Du kan använda åtgärden **Direktleverans** för att fylla i raderna i inköpskalkylarket. För den här åtgärden används batchprojektet **Hämta förs.order** så att du kan bestämma vilka försäljningsorderrader du vill ange för en direktleverans.

- Du kan använda åtgärden **Specialorder** för att fylla i raderna i inköpskalkylarket. För den här åtgärden används batchprojektet **Hämta förs.order** så att du kan bestämma vilka försäljningsorderrader du vill ange för en specialorder.

Inköpsförslagsraderna innehåller detaljerad information om de artiklar som måste beställas. Du kan redigera och ta bort raderna så att påfyllningsplanen justeras, och du kan bearbeta raderna ytterligare med hjälp av batchprojektet **Verkställ åtgärdsmeddelande**. 

Information om hur du planerar lagerställen och överföringar finns i [Planera med eller utan lagerställen](production-planning-with-without-locations.md).

> [!TIP]
> När du arbetar på sidorna **Inköpsförslag** eller **Planeringsförslag** kan du ordna raderna genom att sortera efter ett kolumnnamn. Detta är särskilt användbart på sidan Paneringsförslag eftersom de kan användas för produktionsorder på flera nivåer. Som standard sorteras rader efter fältet **Artikelnr**. Om du vill gruppera rader för en order med flera nivåer sorterar du efter **Ref.ordernr** . Också fälten **MPS-order** och **Planeringsnivå** kan hjälpa dig att visa hierarkin av rader.

## <a name="see-also"></a>Se även

[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
[Planerad](production-planning.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
