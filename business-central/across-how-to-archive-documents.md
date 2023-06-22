---
title: Arkivera försäljnings- och inköpsdokument
description: 'Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och ramorder och återställa originalen om det behövs.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.date: 03/06/2022
ms.author: bholtorf
---
# <a name="archive-documents" />Arkivera dokument
Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och ramorder. Genom att arkivera dokument kan du återställa originalet om det behövs. Du kan arkivera ett försäljnings- eller inköpsdokument flera gånger och spara en annan arkiverad version varje gång.

För arkiverade försäljningsdokument där originalet finns och inte har bokförts, kan du använda åtgärd **återställa** för att skriva över det aktuella dokumentet med en arkiverad version. 

För arkiverade dokument där originalet tagits bort kan du endast återanvända innehållet genom att kopiera informationen, till exempel med åtgärd **Kopiera från dokument**.  

## <a name="to-set-up-automatic-document-archiving" />Så här ställer du in automatisk dokumentarkivering

Du kan ställa in automatisk arkivering av försäljnings- och inköpsorder, offerter, avropsorder och returorder. När automatisk arkivering är aktiverad skapas en ny version av det arkiverade dokumentet när någon gör något av följande:

* Ändrar eller tar bort ett dokument.
* Skriver ut, hämtar eller skickar ett dokument via e-post.
* Konverterar en offert till en order eller faktura.
* Bokför en order.

Nedan beskrivs hur du ställer in automatisk arkivering av försäljningsdokument. Momenten är liknande för en inköpsorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.
2. På snabbfliken **arkivering** anger du om du vill aktivera automatisk arkivering för de olika typerna av försäljningsdokument. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Följande tabell beskriver alternativen för fält **Arkivera offerter**.

|Alternativ|Description|
|------|-----------|
|**Aldrig**| Aldrig arkivera försäljningsofferter när de tas bort.|
|**Fråga**|Välj för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort.|
|**Alltid**|Välj om du vill arkivera försäljningsofferter automatiskt när de tas bort.|

## <a name="to-manually-archive-a-sales-order" />För att arkivera en försäljningsorder

Följande förfarande beskriver hur du arkiverar en försäljningsorder. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Öppna en försäljningsorder som du vill arkivera.  
3. Välj åtgärden **Arkivera dokument**.

Försäljningsordern arkiveras. Du kan visa den på sidan **Arkiverade försäljningsorder**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive" />Så här återställer du en icke-bokförd försäljningsorder från arkivet

Nedan beskrivs hur du ändrar innehållet återställa en arkiverad försäljningsorder till den ursprungliga försäljningsordern. Att återställa ett dokument är endast möjligt när originaldokumentet inte har bokförts. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arkiv för försäljningsorder** och väljer sedan relaterad länk.
2. Markera den arkiverade försäljningsordern eller versionen av den som du vill återskapa och välj sedan åtgärden **Återskapa**.  

Innehållet i den ursprungliga försäljningsordern ersätts med värdet för den valda arkiverade versionen.

## <a name="to-delete-archived-sales-orders" />Ta bort arkiverade förs.orderversioner

Följande förfarande beskriver hur du tar bort arkiverade försäljningsorder. Stegen är liknande för andra arkiverade försäljnings- och inköpsdokument.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arkiv för försäljningsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ta bort äldre versioner** och välj sedan lämpliga filter på sidan **Ta bort arkiverade försäljningsorderversioner**.  
3. Välj knappen **OK**.

## <a name="see-also" />Se även

[Spåra dokumentrader](across-how-to-track-document-lines.md)  
[Försäljning](sales-manage-sales.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
