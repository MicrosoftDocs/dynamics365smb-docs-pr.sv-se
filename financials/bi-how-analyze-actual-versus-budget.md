---
title: Analysera faktiska kontra budget | Microsoft Docs
description: Beskriver hur du analyserar faktiska belopp kontra budgeterade belopp
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 126c8da9b9ef80e954510fa8e5089906d7dd6f01
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a>Så här: Analysera faktiska belopp kontra budgeterade belopp
Som en del av att samla in, analysera och dela dina företagsdata, kan du visa faktiska belopp och budgeterade belopp för alla konton och för flera perioder.

Om du vill analysera budgeterade belopp, måste du först skapa budgetar. (Mer information finns i [Så här skapar du budgetar](finance-how-create-budgets.md).)

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-view-a-budget"></a>Så här visar du en budget
Om du vill kan du filtrera transaktionerna i en budget med dimensioner och på så sätt visa vissa bestämda budgetar.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.
2. I fönstret **Redovisningsbudgetar** öppnar du budgeten du vill visa.  
3. Högst upp i fönstret fyller du i fälten för att definiera vad som ska visas. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Om du har valt **Period** i antingen **Visa som rader** eller **Visa som kolumner**  måste du fylla i fältet **Visa efter**. Om du inte har valt **Period** i antingen **Visa som rader** eller i **Visa som kolumner** anger du önskad period i fältet **Datumfilter**.  

> [!NOTE]  
>   Endast transaktioner från redovisningsbudgeten med de filterkoder som du anger på snabbfliken **Filter** tas med i beräkningen. Budgettransaktioner med andra filterkoder eller utan filterkoder inkluderas inte. Så länge filtret finns kvar i fönstret visas endast budgettransaktionerna med dessa filterkoder i budgeten.  

> [!TIP]  
>   Om du vill ändra budgeten kan du redigera budgettransaktionerna. Välj beloppet för att visa de underliggande redovisningsbudgettransaktioner.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Så här visar du faktiska och budgeterade belopp för alla konton  
Du kan visa redovisningsbudgetar och jämföra dem med faktiska belopp i flera olika moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.  
2. I fönstret **kontoplan** kan du välja åtgärden **Redovisningssaldo/Budget**.
3. Högst upp i fönstret fyller du i fälten för att definiera vad som ska visas.  
4. Välj fältet om du vill visa en specifikation av ett visat belopp.  

> [!NOTE]  
>   De filter som definieras i fönsterhuvudet används både på redovisningstransaktioner och budgettransaktioner.

Kolumnerna till vänster innehåller kontoplanen. Av de fem kolumnerna till höger innehåller de fyra första kolumnerna faktiska och budgeterade debet- och kreditbelopp för alla konton. I den femte kolumnen visas det proportionella sambandet mellan de faktiska och de budgeterade beloppen på redovisningskontot.  

> [!TIP]  
>   Använd fältet **Visa efter** i fönstret **Redov.saldo/budget** om du vill välja ett tidsintervall. Använd fältet **Visa som** om du vill bestämma hur beloppen ska beräknas, **Nettoförändring** eller **Saldo t.o.m. datum**. Välj åtgärden **Föregående period** eller **Nästa period** för att ändra perioden.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Så här visar du faktiska och budgeterade belopp för flera perioder  
I stället för att visa de faktiska och budgeterade beloppen för alla konton under en enstaka period kan du visa ett antal perioder för ett enskilt konto.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.  
2. I fönstretden **kontoplan** markerar du relevant redovisningskonto, och välj sedan åtgärden **konto saldo/budget**.  
3. Högst upp i fönstret fyller du i fälten för att definiera vad som ska visas.   
4. Välj fältet om du vill visa en specifikation av ett visat belopp.  

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)
[Så här: arbeta med kontouppställningar](bi-how-work-account-schedule.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

