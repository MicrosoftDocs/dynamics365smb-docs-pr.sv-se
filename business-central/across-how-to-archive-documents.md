---
title: Arkivera försäljnings- och inköpsdokument
description: 'Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och ramorder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# <a name="archive-documents"></a>Arkivera dokument

Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och ramorder. Om du använder projekthanteringsfunktioner kan du också arkivera dina projekt. Du kan arkivera ett dokument och projekt flera gånger, vilket sparar en annan arkiverad version varje gång.

För försäljningsdokument där originalet finns och inte har bokförts, kan du använda åtgärd **återställa** för att skriva över det med en arkiverad version. 

> [!NOTE]
> Du kan bara återställa försäljningsdokument och projekt. Åtgärden är inte tillgänglig för arkiverade inköpsdokument.

För arkiverade dokument där originalet tagits bort kan du återanvända innehållet genom att kopiera informationen, till exempel med åtgärd **Kopiera från dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Så här ställer du in automatisk dokumentarkivering

Du kan automatisera arkivering för att skapa en ny version av det arkiverade dokumentet när någon gör något av följande:

* Ändrar eller tar bort ett dokument eller projekt.
* Skriver ut, hämtar eller skickar ett dokument via e-post.
* Konverterar en offert till en order eller faktura.
* Bokför en order.

Följande steg beskriver hur du ställer in automatisk arkivering av försäljningsdokument från sidan **Försäljningsinställningar**. Stegen är liknande för inköpsdokument och projekt. För inköpsdokument använder du sidan **Inköpsinställningar**. För projekt använder du sidan **Projektinställningar**.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.
2. På snabbfliken **arkivering** anger du om du vill aktivera automatisk arkivering för de olika typerna av försäljningsdokument. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Följande tabell beskriver alternativen för fält **Arkivera offerter**.

|Alternativ|Description|
|------|-----------|
|**Aldrig**| Aldrig arkivera försäljningsofferter när de tas bort.|
|**Fråga**|Välj för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort.|
|**Alltid**|Välj om du vill arkivera försäljningsofferter automatiskt när de tas bort.|

## <a name="to-manually-archive-a-sales-order"></a>För att manuellt arkivera en försäljningsorder

Följande förfarande beskriver hur du manuellt arkiverar en försäljningsorder. Stegen är liknande för alla dokument och projekt som du kan arkivera.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Öppna en försäljningsorder som du vill arkivera.  
3. Välj åtgärden **Arkivera dokument**.

Försäljningsordern arkiveras. Du kan visa den på sidan **Arkiverade försäljningsorder**.

## <a name="to-restore-a-non-posted-sales-document-or-a-project-from-the-archive"></a>Så här återställer du ett icke-bokfört försäljningsdokument eller ett projekt från arkivet

Nedan beskrivs hur du ändrar innehållet återställa en arkiverad försäljningsorder till den ursprungliga försäljningsordern. Att återställa ett dokument är endast möjligt när originaldokumentet inte har bokförts. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter och även för projekt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arkiv för försäljningsorder** och väljer sedan relaterad länk.
2. Markera den arkiverade försäljningsordern eller versionen av den som du vill återskapa och välj sedan åtgärden **Återskapa**.  

Innehållet i den ursprungliga försäljningsordern eller projekt ersätts med värdet för den valda arkiverade versionen.

## <a name="to-delete-archived-versions"></a>För att ta bort arkiverade versioner

Använd en kvarhållningsprincip för att rensa arkiverade versioner som inte längre behövs. Med hjälp av kvarhållningsprinciper kan administratörer definiera hur länge de vill lagra data. De kan t.ex. skapa en princip som tar bort data efter förfallodatum. Mer information finns i [Definiera kvarhållningsprincip](admin-data-retention-policies.md).

Det finns några saker du bör notera om att skapa kvarhållningsprinciper för arkiverade dokument och projekt:

* Om det ursprungliga dokumentet inte har tagits bort tar [!INCLUDE [prod_short](includes/prod_short.md)] inte bort de arkiverade versionerna. Arkiverade versioner upphör inte att gälla så länge som den ursprungliga finns.
* När du anger kvarhållningsprincip kan du ange att du vill att principen ska ta bort alla arkiverade versioner utom det senaste. Du kan till exempel ha 10 versioner och ha kvar en kopia av det senaste. 
* [!INCLUDE [prod_short](includes/prod_short.md)] beräknar utgångsdatumet för dokument som baseras på datumet för den senaste arkiverade versionen.

## <a name="see-also"></a>Se även

[Spåra dokumentrader](across-how-to-track-document-lines.md)  
[Försäljning](sales-manage-sales.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
