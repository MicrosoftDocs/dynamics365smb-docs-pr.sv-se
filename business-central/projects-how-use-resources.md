---
title: Skapa och justera resursanvändning och priser
description: 'Beskriver hur du kan registrera resursförbrukning eller förbrukning för ett projekt för att hålla reda på och hantera kostnader, priser och arbetstyper.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '201,206, 207, 271, 493'
ms.date: 04/01/2021
ms.author: edupont
---
# Använda resurser för projekt

Du registrerar förbrukning av resurser i projektjournalen för att hålla reda på kostnader, priser och de specifika projekttyper som är kopplade till projekt. Mer information finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).

> [!NOTE]
> Du kan också köpa externa resurser om du t. ex. vill fakturera en leverantör för levererat arbete. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

Du kan även bokföra förbrukningen av en resurs i en resursjournal eller projektjournal. Transaktioner bokförda i resursjournaler påverkar inte redovisningen.

## Så här tilldelar du resurser till projekt

Du tilldelar resurser till projekt genom att skapa planeringsrader för projektet. Mer information finns i [Skapa projekt](projects-how-create-jobs.md).

## Registrera resursförbrukning för ett projekt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.
2. Öppna den relevanta projektjournalen och fyll sedan i fälten som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. När journalen är slutförd väljer du åtgärden **Bokföra**.

## Justera resurspriser

Om du vill ändra kostnader eller priser för många resurser på en gång kan du använda ett batch-jobb .  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Justera resurskostnad/pris** och väljer sedan relaterad länk.
2. Fyll i fälten på en rad efter behov och välj sedan knappen **OK**.

> [!NOTE]  
> Batch-jobbet varken skapar eller justerar alternativa kostnader eller priser för resurser. Detta ändrar bara innehållet i fältet på resurskortet för fältet **Justeringsfält** som du har valt i batch-jobbet. Justeringarna börjar gälla direkt för resurser så kontrollera justeringsfaktorerna innan du kör batch-jobbet.

## Så här får du förslag till resursprisändringar enligt befintliga alternativa priser:

Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Resursprisändringar** och väljer sedan relaterad länk.
2. Välj åtgärden **Föreslå res.prisändring (pris)** och fyll sedan i fälten efter behov.
3. Välj knappen **OK**.  
4. När batch-jobbet har avslutats visar sidan **Resursprisändringar** resultatet av batch-jobbet.

## Så här får du förslag till resursprisändringar enligt standardpriser

Om du vill skapa flera alternativa resurspriser baserat på standardpriserna på resurskorten kan du använda ett batch-jobb .  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resursprisändringar** och väljer sedan relaterad länk.
2. Välj åtgärden **Föreslå res.prisändring (res)** och fyll sedan i fälten efter behov.  
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du sidan **Resursprisändringar** för att visa resultatet av batch-jobbet.

## Så här får du förslag till resursprisändringar baserat på alternativa priser

Om du redan har skapat alternativa priser för några resurser kan du använda batch-jobbet för att skapa flera alternativa resurspriser.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Föreslå res.prisändring (pris)** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.
3. Välj **OK**.  
4. När batch-jobbet har avslutats öppnar du sidan **Resursprisändringar** för att visa resultatet av batch-jobbet.

## Se även

[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)     
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]