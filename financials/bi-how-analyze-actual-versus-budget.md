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
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="37094-103">Så här: Analysera faktiska belopp kontra budgeterade belopp</span><span class="sxs-lookup"><span data-stu-id="37094-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="37094-104">Som en del av att samla in, analysera och dela dina företagsdata, kan du visa faktiska belopp och budgeterade belopp för alla konton och för flera perioder.</span><span class="sxs-lookup"><span data-stu-id="37094-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="37094-105">Om du vill analysera budgeterade belopp, måste du först skapa budgetar.</span><span class="sxs-lookup"><span data-stu-id="37094-105">To analyze budgeted amounts, you must first create budgets.</span></span> <span data-ttu-id="37094-106">(Mer information finns i [Så här skapar du budgetar](finance-how-create-budgets.md).)</span><span class="sxs-lookup"><span data-stu-id="37094-106">For more information, see [How to: Create Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="37094-107">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="37094-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="37094-108">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="37094-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-budget"></a><span data-ttu-id="37094-109">Så här visar du en budget</span><span class="sxs-lookup"><span data-stu-id="37094-109">To view a budget</span></span>
<span data-ttu-id="37094-110">Om du vill kan du filtrera transaktionerna i en budget med dimensioner och på så sätt visa vissa bestämda budgetar.</span><span class="sxs-lookup"><span data-stu-id="37094-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="37094-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="37094-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="37094-112">I fönstret **Redovisningsbudgetar** öppnar du budgeten du vill visa.</span><span class="sxs-lookup"><span data-stu-id="37094-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="37094-113">Högst upp i fönstret fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="37094-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="37094-114">Om du har valt **Period** i antingen **Visa som rader** eller **Visa som kolumner**  måste du fylla i fältet **Visa efter**.</span><span class="sxs-lookup"><span data-stu-id="37094-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="37094-115">Om du inte har valt **Period** i antingen **Visa som rader** eller i **Visa som kolumner** anger du önskad period i fältet **Datumfilter**.</span><span class="sxs-lookup"><span data-stu-id="37094-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="37094-116">Endast transaktioner från redovisningsbudgeten med de filterkoder som du anger på snabbfliken **Filter** tas med i beräkningen.</span><span class="sxs-lookup"><span data-stu-id="37094-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="37094-117">Budgettransaktioner med andra filterkoder eller utan filterkoder inkluderas inte.</span><span class="sxs-lookup"><span data-stu-id="37094-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="37094-118">Så länge filtret finns kvar i fönstret visas endast budgettransaktionerna med dessa filterkoder i budgeten.</span><span class="sxs-lookup"><span data-stu-id="37094-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="37094-119">Om du vill ändra budgeten kan du redigera budgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="37094-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="37094-120">Välj beloppet för att visa de underliggande redovisningsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="37094-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="37094-121">Så här visar du faktiska och budgeterade belopp för alla konton</span><span class="sxs-lookup"><span data-stu-id="37094-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="37094-122">Du kan visa redovisningsbudgetar och jämföra dem med faktiska belopp i flera olika moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="37094-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="37094-123">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="37094-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37094-124">I fönstret **kontoplan** kan du välja åtgärden **Redovisningssaldo/Budget**.</span><span class="sxs-lookup"><span data-stu-id="37094-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="37094-125">Högst upp i fönstret fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="37094-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="37094-126">Välj fältet om du vill visa en specifikation av ett visat belopp.</span><span class="sxs-lookup"><span data-stu-id="37094-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="37094-127">De filter som definieras i fönsterhuvudet används både på redovisningstransaktioner och budgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="37094-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="37094-128">Kolumnerna till vänster innehåller kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="37094-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="37094-129">Av de fem kolumnerna till höger innehåller de fyra första kolumnerna faktiska och budgeterade debet- och kreditbelopp för alla konton.</span><span class="sxs-lookup"><span data-stu-id="37094-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="37094-130">I den femte kolumnen visas det proportionella sambandet mellan de faktiska och de budgeterade beloppen på redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="37094-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="37094-131">Använd fältet **Visa efter** i fönstret **Redov.saldo/budget** om du vill välja ett tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="37094-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="37094-132">Använd fältet **Visa som** om du vill bestämma hur beloppen ska beräknas, **Nettoförändring** eller **Saldo t.o.m. datum**.</span><span class="sxs-lookup"><span data-stu-id="37094-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="37094-133">Välj åtgärden **Föregående period** eller **Nästa period** för att ändra perioden.</span><span class="sxs-lookup"><span data-stu-id="37094-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="37094-134">Så här visar du faktiska och budgeterade belopp för flera perioder</span><span class="sxs-lookup"><span data-stu-id="37094-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="37094-135">I stället för att visa de faktiska och budgeterade beloppen för alla konton under en enstaka period kan du visa ett antal perioder för ett enskilt konto.</span><span class="sxs-lookup"><span data-stu-id="37094-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="37094-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="37094-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37094-137">I fönstretden **kontoplan** markerar du relevant redovisningskonto, och välj sedan åtgärden **konto saldo/budget**.</span><span class="sxs-lookup"><span data-stu-id="37094-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="37094-138">Högst upp i fönstret fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="37094-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="37094-139">Välj fältet om du vill visa en specifikation av ett visat belopp.</span><span class="sxs-lookup"><span data-stu-id="37094-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="37094-140">Se även</span><span class="sxs-lookup"><span data-stu-id="37094-140">See Also</span></span>
<span data-ttu-id="37094-141">[Affärsstöd](bi.md)
[Så här: arbeta med kontouppställningar](bi-how-work-account-schedule.md)</span><span class="sxs-lookup"><span data-stu-id="37094-141">[Business Intelligence](bi.md)
[How to: Work with Account Schedules](bi-how-work-account-schedule.md)</span></span>  
[<span data-ttu-id="37094-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="37094-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="37094-143">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="37094-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="37094-144">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="37094-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="37094-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37094-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

