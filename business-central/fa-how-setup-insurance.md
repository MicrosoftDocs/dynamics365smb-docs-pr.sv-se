---
title: Skapa försäkring för anläggningstillgångar | Microsoft Docs
description: Om du vill hantera täckning av försäkring för anläggningstillgångar måste du ange ett försäkringskort och allmän försäkringsinformation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ebb62a4ef9ea84ec5bfddc099dfb6120a4e6405
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774047"
---
# <a name="set-up-fixed-asset-insurance"></a>Skapa försäkring för anläggningstillgångar
Om du vill hantera täckning av försäkring för anläggningstillgångar måste du först ange en viss allmän försäkringsinformation och ett försäkringskort per brev.

## <a name="to-set-up-general-insurance-information"></a>Så här anger du allmän försäkringsinformation
Om du vill använda den här funktionen i [!INCLUDE[prod_short](includes/prod_short.md)], måste du ange viss allmän information.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Inställningar i anl.** och välj sedan tillhörande länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Så här skapar du försäkringstyper
Du kan gruppera dina försäkringsbrev i kategorier, t. ex. stöldförsäkring och brandförsäkring. Försäkringstyperna används på försäkringskortet.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Försäkringstyper** och välj sedan tillhörande länk.  
2. Fyll i fälten om det behövs.

## <a name="to-set-up-insurance-cards"></a>Så här skapar du försäkringskort
Du kan lagra information om varje försäkringsbrev på försäkringskortet.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkring** och välj sedan tillhörande länk.  
2. På sidan **Försäkring** väljer du åtgärden **Ny** åtgärder för att skapa ett nytt försäkringskort.  
3. Fyll i fälten om det behövs.

## <a name="to-set-up-insurance-journal-templates"></a>Så här skapar du journalmallar för försäkringar
[!INCLUDE[prod_short](includes/prod_short.md)] skapar automatiskt en försäkringsjournalmall första gången du öppnar sidan **Försäkringsjournal**. Du kan dessutom skapa ytterligare mallar. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkringsjournalmallar** och välj sedan tillhörande länk.  
2. Fyll i fälten om det behövs.

## <a name="to-set-up-insurance-journal-batches"></a>Så här skapar du försäkringsjournaler
Du kan skapa journaler i en försäkringsjournalmall. Värdena i journalen används som standardvärden om du inte fyller i fälten på journalraderna. Mer information finns i [Arbeta medSkapa redovisningsjournaler](ui-work-general-journals.md)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkringsjournalmallar** och välj sedan tillhörande länk.  
2. Välj en försäkringsjournalmall och välj sedan åtgärden **Journaler**.
3. På sidan **Försäkringsjournaler** fyller du i fälten efter behov.

> [!NOTE]  
>   Siffror fyller en särskild funktion i journalnamnen. Om ett journalmallsnamn eller ett journalnamn innehåller ett nummer, får namnet efterföljande nummer automatiskt när journalen bokförs. Om till exempel HH1 anges i fältet **Namn** ändras journalnamnet till HH2 när journalen som heter HH1 har bokförts.

## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]