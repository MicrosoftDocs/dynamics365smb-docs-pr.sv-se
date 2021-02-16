---
title: Skapa och justera resursanvändning och priser | Microsoft Docs
description: Beskriver hur du kan registrera resursförbrukning eller förbrukning för ett projekt för att hålla reda på och hantera kostnader, priser och arbetstyper.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c753e38566971c044da3337f0f35f1609bd489c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748874"
---
# <a name="use-resources-for-jobs"></a>Använda resurser för projekt
Du registrerar förbrukning av resurser i projektjournalen för att hålla reda på kostnader, priser och de specifika projekttyper som är kopplade till projekt. Mer information finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).

> [!NOTE]
> Du kan också köpa externa resurser om du t.ex. vill fakturera en leverantör för levererat arbete. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

Du kan även bokföra förbrukningen av en resurs i en resursjournal eller projektjournal. Transaktioner bokförda i resursjournaler påverkar inte redovisningen.

## <a name="to-assign-resources-to-jobs"></a>Så här tilldelar du resurser till projekt
Du tilldelar resurser till projekt genom att skapa planeringsrader för projektet. Mer information finns i [Skapa projekt](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Registrera resursförbrukning för ett projekt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Jobbjournaler** och välj sedan relaterad länk.
2. Öppna den relevanta projektjournalen och fyll sedan i fälten som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. När journalen är slutförd väljer du åtgärden **Bokföra**.

## <a name="to-adjust-resource-prices"></a>Justera resurspriser
Om du vill ändra kostnader eller priser för många resurser på en gång kan du använda ett batch-jobb .  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Justera resurskostnad/pris** och välj sedan tillhörande länk.
2. Fyll i fälten på en rad efter behov och välj sedan knappen **OK**.

> [!NOTE]  
>   Batch-jobbet varken skapar eller justerar alternativa kostnader eller priser för resurser. Detta ändrar bara innehållet i fältet på resurskortet för fältet **Justeringsfält** som du har valt i batch-jobbet. Justeringarna börjar gälla direkt för resurser så kontrollera justeringsfaktorerna innan du kör batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Så här får du förslag till resursprisändringar enligt befintliga alternativa priser:
Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Ändringar i resurspris** och välj sedan tillhörande länk.
2. Välj åtgärden **Föreslå res.prisändring (pris)** och fyll sedan i fälten efter behov.
3. Välj knappen **OK**.  
4. När batch-jobbet har avslutats visar sidan **Resursprisändringar** resultatet av batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Så här får du förslag till resursprisändringar enligt standardpriser
Om du vill skapa flera alternativa resurspriser baserat på standardpriserna på resurskorten kan du använda ett batch-jobb .  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Ändringar i resurspris** och välj sedan tillhörande länk.
2. Välj åtgärden **Föreslå res.prisändring (res)** och fyll sedan i fälten efter behov.  
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du sidan **Resursprisändringar** för att visa resultatet av batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Så här får du förslag till resursprisändringar baserat på alternativa priser
Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Föreslå res.prisändring (pris)** och välj sedan tillhörande länk.  
2. Fyll i fälten om det behövs.
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du sidan **Resursprisändringar** för att visa resultatet av batch-jobbet.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)     
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
