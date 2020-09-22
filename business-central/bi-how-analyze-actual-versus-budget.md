---
title: Analysera faktiska kontra budget | Microsoft Docs
description: Beskriver hur du analyserar faktiska belopp kontra budgeterade belopp
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: cc0497b4e0add53ce983883cd58c10475c9d9a6e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783487"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="3319f-103">Analysera faktiska belopp kontra budgeterade belopp</span><span class="sxs-lookup"><span data-stu-id="3319f-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="3319f-104">Som en del av att samla in, analysera och dela dina företagsdata, kan du visa faktiska belopp och budgeterade belopp för alla konton och för flera perioder.</span><span class="sxs-lookup"><span data-stu-id="3319f-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="3319f-105">Om du vill analysera budgeterade belopp måste du först skapa redovisningsbudgetar.</span><span class="sxs-lookup"><span data-stu-id="3319f-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="3319f-106">Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="3319f-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="3319f-107">Så här visar du en redovisningsbudget</span><span class="sxs-lookup"><span data-stu-id="3319f-107">To view a G/L budget</span></span>
<span data-ttu-id="3319f-108">Om du vill kan du filtrera transaktionerna i en budget med dimensioner och på så sätt visa vissa bestämda budgetar.</span><span class="sxs-lookup"><span data-stu-id="3319f-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="3319f-109">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsbudgetar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3319f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="3319f-110">På sidan **Redovisningsbudgetar** öppnar du budgeten du vill visa.</span><span class="sxs-lookup"><span data-stu-id="3319f-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="3319f-111">Högst upp på sidan fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3319f-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="3319f-112">Om du har valt **Period** i antingen **Visa som rader** eller **Visa som kolumner** måste du fylla i fältet **Visa efter**.</span><span class="sxs-lookup"><span data-stu-id="3319f-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="3319f-113">Om du inte har valt **Period** i antingen **Visa som rader** eller i **Visa som kolumner** anger du önskad period i fältet **Datumfilter**.</span><span class="sxs-lookup"><span data-stu-id="3319f-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3319f-114">Endast transaktioner från redovisningsbudgeten med de filterkoder som du anger på snabbfliken **Filter** tas med i beräkningen.</span><span class="sxs-lookup"><span data-stu-id="3319f-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="3319f-115">Budgettransaktioner med andra filterkoder eller utan filterkoder inkluderas inte.</span><span class="sxs-lookup"><span data-stu-id="3319f-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="3319f-116">Så länge filtret finns kvar på sidan visas endast budgettransaktionerna med dessa filterkoder i budgeten.</span><span class="sxs-lookup"><span data-stu-id="3319f-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="3319f-117">Om du vill ändra budgeten kan du redigera budgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="3319f-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="3319f-118">Välj beloppet för att visa de underliggande redovisningsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="3319f-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="3319f-119">Så här visar du faktiska och budgeterade belopp för alla konton</span><span class="sxs-lookup"><span data-stu-id="3319f-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="3319f-120">Du kan visa redovisningsbudgetar och jämföra dem med faktiska belopp i flera olika moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3319f-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="3319f-121">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontolista**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3319f-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3319f-122">På sidan **kontoplan** kan du välja åtgärden **Redovisningssaldo/Budget**.</span><span class="sxs-lookup"><span data-stu-id="3319f-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="3319f-123">Högst upp på sidan fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3319f-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="3319f-124">Välj fältet om du vill visa en specifikation av ett visat belopp.</span><span class="sxs-lookup"><span data-stu-id="3319f-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3319f-125">De filter som definieras på sidhuvudet används både på redovisningstransaktioner och budgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="3319f-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="3319f-126">Kolumnerna till vänster innehåller kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="3319f-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="3319f-127">Av de fem kolumnerna till höger innehåller de fyra första kolumnerna faktiska och budgeterade debet- och kreditbelopp för alla konton.</span><span class="sxs-lookup"><span data-stu-id="3319f-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="3319f-128">I den femte kolumnen visas det proportionella sambandet mellan de faktiska och de budgeterade beloppen på redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="3319f-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="3319f-129">Använd fältet **Visa efter** på sidan **Redov.saldo/budget** om du vill välja ett tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="3319f-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="3319f-130">Använd fältet **Visa som** om du vill bestämma hur beloppen ska beräknas, **Nettoförändring** eller **Saldo t.o.m. datum**.</span><span class="sxs-lookup"><span data-stu-id="3319f-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="3319f-131">Välj åtgärden **Föregående period** eller **Nästa period** för att ändra perioden.</span><span class="sxs-lookup"><span data-stu-id="3319f-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="3319f-132">Så här visar du faktiska och budgeterade belopp för flera perioder</span><span class="sxs-lookup"><span data-stu-id="3319f-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="3319f-133">I stället för att visa de faktiska och budgeterade beloppen för alla konton under en enstaka period kan du visa ett antal perioder för ett enskilt konto.</span><span class="sxs-lookup"><span data-stu-id="3319f-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="3319f-134">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3319f-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3319f-135">På sidan **kontoplan** markerar du relevant redovisningskonto, och välj sedan åtgärden **konto saldo/budget**.</span><span class="sxs-lookup"><span data-stu-id="3319f-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="3319f-136">Högst upp på sidan fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3319f-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="3319f-137">Välj fältet om du vill visa en specifikation av ett visat belopp.</span><span class="sxs-lookup"><span data-stu-id="3319f-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3319f-138">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="3319f-138">See Related Training at [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="3319f-139">Se även</span><span class="sxs-lookup"><span data-stu-id="3319f-139">See Also</span></span>
[<span data-ttu-id="3319f-140">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="3319f-140">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="3319f-141">Arbeta med kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="3319f-141">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="3319f-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="3319f-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="3319f-143">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="3319f-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="3319f-144">Huvudbok och kontolista</span><span class="sxs-lookup"><span data-stu-id="3319f-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="3319f-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3319f-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
