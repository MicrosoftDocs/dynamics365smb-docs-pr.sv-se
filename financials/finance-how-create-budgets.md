---
title: Skapa budgetar | Microsoft Docs
description: "Beskriver hur du skapar budgetar för att förutse olika ekonomiska aktiviteter och koppla dimensionerna för affärssystemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7dfd3cc7efe00b48a39982bb220ccc21b7409da4
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create--budgets"></a><span data-ttu-id="43370-103">Så här skapar du budgetar</span><span class="sxs-lookup"><span data-stu-id="43370-103">How to: Create  Budgets</span></span>
<span data-ttu-id="43370-104">Om du vill kan du använda flera olika budgetar för samma tidsperioder genom att skapa budgetar med separata namn.</span><span class="sxs-lookup"><span data-stu-id="43370-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="43370-105">Först definierar du budgetnamnet och matar in budgetsiffrorna.</span><span class="sxs-lookup"><span data-stu-id="43370-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="43370-106">Budgetnamnet infogas sedan i alla budgettransaktioner du skapar.</span><span class="sxs-lookup"><span data-stu-id="43370-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="43370-107">När du skapar en budget kan du definiera fyra dimensioner för varje budget.</span><span class="sxs-lookup"><span data-stu-id="43370-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="43370-108">Dessa budget\-specifika dimensionerna kallas för budgetdimensioner.</span><span class="sxs-lookup"><span data-stu-id="43370-108">These budget\-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="43370-109">Du kan välja budgetdimensionerna bland de dimensioner som redan finns upplagda.</span><span class="sxs-lookup"><span data-stu-id="43370-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="43370-110">Budgetdimensioner kan användas för att skapa filter för en budget och lägga till dimensionsinformation till budgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="43370-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="43370-111">Mer information finns i [Arbeta med](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="43370-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="43370-112">Budgetar spelar en viktig roll i business intelligence, exempelvis i bokslut som baseras på kontoscheman som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i diagrammet över konton.</span><span class="sxs-lookup"><span data-stu-id="43370-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="43370-113">Mer information finns i [Affärsstöd](bi.md).</span><span class="sxs-lookup"><span data-stu-id="43370-113">For more information, see [Business Intelligence](bi.md).</span></span>   

 > [!NOTE]  
>   <span data-ttu-id="43370-114">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="43370-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="43370-115">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="43370-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="43370-116">Så här skapar du en ny budget:</span><span class="sxs-lookup"><span data-stu-id="43370-116">To create a new budget</span></span>  

1. <span data-ttu-id="43370-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="43370-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="43370-118">Välj åtgärden **Redigera lista** och fyll sedan i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="43370-118">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="43370-119">Välj åtgärden **Redigera budget**.</span><span class="sxs-lookup"><span data-stu-id="43370-119">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="43370-120">Högst upp i fönstret **Budget** fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="43370-120">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="43370-121">Endast transaktioner som innehåller budgetnamnet som du angav i fältet **Budgetnamn** visas.</span><span class="sxs-lookup"><span data-stu-id="43370-121">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="43370-122">Fönstret är för närvarande tomt eftersom budgetnamnet just har skapats och det därför inte finns några transaktioner som matchar filtret.</span><span class="sxs-lookup"><span data-stu-id="43370-122">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="43370-123">Därför är fönstret tomt.</span><span class="sxs-lookup"><span data-stu-id="43370-123">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="43370-124">Om du vill ange ett belopp väljer du relevant cell i matrisen.</span><span class="sxs-lookup"><span data-stu-id="43370-124">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="43370-125">Fönstret **Redov.budgettransaktioner** öppnas.</span><span class="sxs-lookup"><span data-stu-id="43370-125">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="43370-126">Skapa en ny rad och fyll i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="43370-126">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="43370-127">Stäng fönstret **Redov.budgettransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="43370-127">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="43370-128">Upprepa steg 5–6 tills du har angett alla budgetbeloppen.</span><span class="sxs-lookup"><span data-stu-id="43370-128">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="43370-129">På snabbfliken **Filter** kan du filtrera budgetinformationen beroende på hur många budgetdimensioner som definierats under budgetnamnet.</span><span class="sxs-lookup"><span data-stu-id="43370-129">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="43370-130">Se även</span><span class="sxs-lookup"><span data-stu-id="43370-130">See Also</span></span>
[<span data-ttu-id="43370-131">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="43370-131">Finance</span></span>](finance.md)  
[<span data-ttu-id="43370-132">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="43370-132">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="43370-133">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="43370-133">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="43370-134">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="43370-134">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="43370-135">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43370-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

