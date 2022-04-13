---
title: Analysera faktiska belopp kontra budgeterade belopp
description: I det här avsnittet beskrivs hur du analyserar faktiska belopp mot budgeterade belopp som ett sätt att samla in, analysera och dela ut dina företagsdata.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 120, 121, 422
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: e21454f52564d4c679cd20171189b0dc14bfe49f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523043"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analysera faktiska belopp kontra budgeterade belopp
Som en del av att samla in, analysera och dela dina företagsdata, kan du visa faktiska belopp och budgeterade belopp för alla konton och för flera perioder.

Om du vill analysera budgeterade belopp måste du först skapa redovisningsbudgetar. Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)

## <a name="to-view-a-gl-budget"></a>Så här visar du en redovisningsbudget
Om du vill kan du filtrera transaktionerna i en budget med dimensioner och på så sätt visa vissa bestämda budgetar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsbudgetar** och väljer sedan relaterad länk.
2. På sidan **Redovisningsbudgetar** öppnar du budgeten du vill visa.  
3. Högst upp på sidan fyller du i fälten för att definiera vad som ska visas. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Om du har valt **Period** i antingen **Visa som rader** eller **Visa som kolumner** måste du fylla i fältet **Visa efter**. Om du inte har valt **Period** i antingen **Visa som rader** eller i **Visa som kolumner** anger du önskad period i fältet **Datumfilter**.  

> [!NOTE]  
>   Endast transaktioner från redovisningsbudgeten med de filterkoder som du anger på snabbfliken **Filter** tas med i beräkningen. Budgettransaktioner med andra filterkoder eller utan filterkoder inkluderas inte. Så länge filtret finns kvar på sidan visas endast budgettransaktionerna med dessa filterkoder i budgeten.  

> [!TIP]  
>   Om du vill ändra budgeten kan du redigera budgettransaktionerna. Välj beloppet för att visa de underliggande redovisningsbudgettransaktioner.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Så här visar du faktiska och budgeterade belopp för alla konton  
Du kan visa redovisningsbudgetar och jämföra dem med faktiska belopp i flera olika moduler i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. På sidan **kontoplan** kan du välja åtgärden **Redovisningssaldo/Budget**.
3. Högst upp på sidan fyller du i fälten för att definiera vad som ska visas.  
4. Välj fältet om du vill visa en specifikation av ett visat belopp.  

> [!NOTE]  
>   De filter som definieras på sidhuvudet används både på redovisningstransaktioner och budgettransaktioner.

Kolumnerna till vänster innehåller kontoplanen. Av de fem kolumnerna till höger innehåller de fyra första kolumnerna faktiska och budgeterade debet- och kreditbelopp för alla konton. I den femte kolumnen visas det proportionella sambandet mellan de faktiska och de budgeterade beloppen på redovisningskontot.  

> [!TIP]  
>   Använd fältet **Visa efter** på sidan **Redov.saldo/budget** om du vill välja ett tidsintervall. Använd fältet **Visa som** om du vill bestämma hur beloppen ska beräknas, **Nettoförändring** eller **Saldo t.o.m. datum**. Välj åtgärden **Föregående period** eller **Nästa period** för att ändra perioden.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Så här visar du faktiska och budgeterade belopp för flera perioder  
I stället för att visa de faktiska och budgeterade beloppen för alla konton under en enstaka period kan du visa ett antal perioder för ett enskilt konto.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. På sidan **kontoplan** markerar du relevant redovisningskonto, och välj sedan åtgärden **konto saldo/budget**.  
3. Högst upp på sidan fyller du i fälten för att definiera vad som ska visas.   
4. Välj fältet om du vill visa en specifikation av ett visat belopp.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Arbeta med kontouppställningar](bi-how-work-account-schedule.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]