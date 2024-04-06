---
title: Arkivera försäljnings- och inköpsdokument
description: 'Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och ramorder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/18/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# <a name="archive-documents"></a>Arkivera dokument

Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och ramorder. Du kan arkivera ett försäljnings- eller inköpsdokument flera gånger och spara en annan arkiverad version varje gång.

För arkiverade försäljningsdokument där originalet finns och inte har bokförts, kan du använda åtgärd **återställa** för att skriva över det aktuella dokumentet med en arkiverad version. Åtgärden fungerar bara för försäljningsdokument.

För arkiverade dokument där originalet tagits bort kan du endast återanvända innehållet genom att kopiera informationen, till exempel med åtgärd **Kopiera från dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Så här ställer du in automatisk dokumentarkivering

Du kan ställa in automatisk arkivering av försäljnings- och inköpsorder, offerter, avropsorder och returorder. När automatisk arkivering är aktiverad skapas en ny version av det arkiverade dokumentet när någon gör något av följande:

* Ändrar eller tar bort ett dokument.
* Skriver ut, hämtar eller skickar ett dokument via e-post.
* Konverterar en offert till en order eller faktura.
* Bokför en order.

Nedan beskrivs hur du ställer in automatisk arkivering av försäljningsdokument. Momenten är liknande för en inköpsorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.
2. På snabbfliken **arkivering** anger du om du vill aktivera automatisk arkivering för de olika typerna av försäljningsdokument. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Följande tabell beskriver alternativen för fält **Arkivera offerter**.

|Alternativ|Description|
|------|-----------|
|**Aldrig**| Aldrig arkivera försäljningsofferter när de tas bort.|
|**Fråga**|Välj för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort.|
|**Alltid**|Välj om du vill arkivera försäljningsofferter automatiskt när de tas bort.|

## <a name="to-manually-archive-a-sales-order"></a>För att manuellt arkivera en försäljningsorder

Följande förfarande beskriver hur du manuellt arkiverar en försäljningsorder. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Öppna en försäljningsorder som du vill arkivera.  
3. Välj åtgärden **Arkivera dokument**.

Försäljningsordern arkiveras. Du kan visa den på sidan **Arkiverade försäljningsorder**.

## <a name="to-restore-a-non-posted-sales-document-or-a-project-from-the-archive"></a>Så här återställer du en icke-bokförd försäljningsorder från arkivet

Nedan beskrivs hur du ändrar innehållet återställa en arkiverad försäljningsorder till den ursprungliga försäljningsordern. Att återställa ett dokument är endast möjligt när originaldokumentet inte har bokförts. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arkiv för försäljningsorder** och väljer sedan relaterad länk.
2. Markera den arkiverade försäljningsordern eller versionen av den som du vill återskapa och välj sedan åtgärden **Återskapa**.  

Innehållet i den ursprungliga försäljningsordern ersätts med värdet för den valda arkiverade versionen.

## <a name="to-delete-archived-versions"></a>Ta bort arkiverade förs.orderversioner

Använd en kvarhållningsprincip för att rensa arkiverade dokument som inte längre behövs. Med hjälp av kvarhållningsprinciper kan administratörer definiera hur länge de vill lagra data. De kan t.ex. skapa en princip som tar bort data efter förfallodatum. Mer information finns i [Definiera bevarandeprinciper](admin-data-retention-policies.md).

Det finns några saker du bör notera om att skapa kvarhållningsprinciper för arkiverade dokument:

* *Om det ursprungliga dokumentet inte har tagits bort tar Business Central inte bort de arkiverade versionerna. Arkiverade versioner upphör inte att gälla så länge som den ursprungliga finns.
* När du anger kvarhållningsprincip kan du ange att du vill att principen ska ta bort alla arkiverade versioner av ett dokument utom det senaste. Du kan till exempel ha 10 versioner av ett dokument och ha kvar en kopia av det senaste. 
* Business Central beräknar utgångsdatumet för dokument som baseras på datumet för den senaste arkiverade versionen.

## <a name="see-also"></a>Se även

[Spåra dokumentrader](across-how-to-track-document-lines.md)  
[Försäljning](sales-manage-sales.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
