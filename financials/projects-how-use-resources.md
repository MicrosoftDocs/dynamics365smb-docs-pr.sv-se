---
title: "Så här använder du resurser för projekt | Microsoft Docs"
description: "Beskriver hur du använder tidrapporter för projekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34d8b133a11324e1821780e3988158bb0989349b
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-resources-for-jobs"></a>Så här använder du resurser för projekt
Du registrerar förbrukning av resurser i projektjournalen för att hålla reda på kostnader, priser och de specifika projekttyper som är kopplade till projekt. Mer information finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).

Du kan även bokföra förbrukningen av en resurs i en resursjournal eller projektjournal. Transaktioner bokförda i resursjournaler påverkar inte redovisningen.

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-assign-resources-to-jobs"></a>Så här tilldelar du resurser till projekt
Du tilldelar resurser till projekt genom att skapa planeringsrader för projektet. (Mer information finns i [Så här skapar du Projekt](projects-how-create-jobs.md).)

## <a name="to-record-resource-usage-for-a-job"></a>Registrera resursförbrukning för ett projekt
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Projektredovisningsjournaler**, och välj sedan relaterad länk.
2. Öppna den relevanta projektjournalen och fyll sedan i fälten som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. När journalen är slutförd väljer du åtgärden **Bokföra**.

## <a name="to-adjust-resource-prices"></a>Justera resurspriser
Om du vill ändra kostnader eller priser för många resurser på en gång kan du använda ett batch-jobb .  

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Justera kostnader/priser** och väljer sedan relaterad länk.
2. Fyll i fälten på en rad efter behov och välj sedan knappen **OK**.

**Obs**! Batch-jobbet varken skapar eller justerar alternativa kostnader eller priser för resurser. Detta ändrar bara innehållet i fältet på resurskortet för fältet **Justeringsfält** som du har valt i batch-jobbet. Justeringarna börjar gälla direkt för resurser så kontrollera justeringsfaktorerna innan du kör batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Så här får du förslag till resursprisändringar enligt befintliga alternativa priser:
Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Resursprisändringar** och väljer sedan relaterad länk.
2. Välj åtgärden **Föreslå res.prisändring (pris)** och fyll sedan i fälten efter behov.
3. Välj **OK**.  
4. När batch-jobbet har avslutats visar fönstret **Resursprisändringar** resultatet av batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Så här får du förslag till resursprisändringar enligt standardpriser
Om du vill skapa flera alternativa resurspriser baserat på standardpriserna på resurskorten kan du använda ett batch-jobb .  

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Resursprisändringar** och väljer sedan relaterad länk.
2. Välj åtgärden **Föreslå res.prisändring (res)** och fyll sedan i fälten efter behov.  
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du fönstret **Resursprisändringar** för att visa resultatet av batch-jobbet.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Så här får du förslag till resursprisändringar baserat på alternativa priser
Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. I rutan **Sök** anger du **Föreslå res.prisändring (pris)** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du fönstret **Resursprisändringar** för att visa resultatet av batch-jobbet.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)     
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

