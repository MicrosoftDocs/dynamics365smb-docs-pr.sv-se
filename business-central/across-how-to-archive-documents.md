---
title: Hur du arkiverar försäljnings- och inköpsdokument | Microsoft Docs
description: Du kan arkivera försäljnings- och inköpsorder, offerter, försäljningsreturorder och avropsorder, och du kan använda arkiverade dokumentet för att återskapa dokumentet som det arkiverades från.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c7f7da76bdea02f640bdb0ffaf5f1b8da16494cf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754873"
---
# <a name="archive-documents"></a>Arkivera dokument
Du kan arkivera försäljnings- och inköpsorder, offerter, returorder och avropsorder, till exempel för att spara en kopia av dokumentet för senare användning. Du kan arkivera ett försäljnings- eller inköpsdokument flera gånger och spara en annan arkiverad version varje gång.

För arkiverade dokument där originalet finns och inte har bokförts, kan du använda funktionen **återställa** för att skriva över originalet med den arkiverade versionen av dokumentet. Detta är praktiskt om du behöver återställa innehållet i ett dokument till ett tidigare tillstånd.

För arkiverade dokument där originalet tagits bort kan du endast återanvända innehållet genom att kopiera informationen, till exempel med funktionen **Kopiera från dokument**.   

## <a name="to-set-up-automatic-document-archiving"></a>Så här ställer du in automatisk dokumentarkivering  
Du kan ställa in automatisk arkivering av försäljnings- och inköpsorder, offerter, avropsorder och returorder innan du tar bort dokument.

Nedan beskrivs hur du ställer in automatisk arkivering av försäljningsdokument. Momenten är liknande för en inköpsorder.
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsinställningar** och välj sedan relaterad länk.
2. På sidan **Försäljningsinställningar** fyller du i följande fält:

|Fält|Description|
|-----|-----------|
|**Arkivering av försäljningsofferter**|**Aldrig** om du aldrig vill arkivera försäljningsofferter när de tas bort. **Fråga** för att uppmana användaren att välja huruvida försäljningsofferter ska arkiveras när de tas bort. **Alltid** om du vill arkivera försäljningsofferter automatiskt när de tas bort.|
|**Arkivera avropsorder för försäljning**|Välj detta alternativ om du vill arkivera avropsorder automatiskt när de tas bort.|
|**Arkivera inköpsorder och inköpsreturorder**|Välj detta alternativ om du vill arkivera försäljningsorder automatiskt när de tas bort.|

## <a name="to-archive-a-sales-order"></a>För att arkivera en försäljningsorder
Följande förfarande beskriver hur du arkiverar en försäljningsorder. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Öppna en försäljningsorder som du vill arkivera.  
3.  Välj åtgärden **Arkivera dokument**.

Försäljningsordern arkiveras. Du kan visa den på sidan **Arkiverade försäljningsorder**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Så här återställer du en icke-bokförd försäljningsorder från arkivet
Nedan beskrivs hur du ändrar innehållet i en arkiverad försäljningsorder till den ursprungliga försäljningsordern. Detta är endast möjligt när det ursprungliga dokumentet inte ännu bokförts. Stegen är liknande för alla inköpsorder, avropsorder, returorder och offerter.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arkiverade försäljningsorder** och välj sedan relaterad länk.
2. Markera den arkiverade försäljningsordern eller versionen av den som du vill återskapa och välj sedan åtgärden **Återskapa**.  

Innehållet i den ursprungliga försäljningsordern ersätts med värdet för den valda arkiverade versionen.

## <a name="to-delete-archived-sales-orders"></a>Ta bort arkiverade förs.orderversioner
Följande förfarande beskriver hur du tar bort arkiverade försäljningsorder. Stegen är liknande för andra arkiverade försäljnings- och inköpsdokument.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ta bort arkiverade försäljningsorderversioner** och välj sedan relaterad länk.  
2.  På sidan **Ta bort arkiverade försäljningsorderversioner** väljer du lämpliga filter.  
3.  Välj knappen **OK**.

## <a name="see-also"></a>Se även
[Spåra dokumentrader](across-how-to-track-document-lines.md)  
[Försäljning](sales-manage-sales.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]