---
title: Skapa redovisningsbudgetar| Microsoft Docs
description: "Beskriver hur du skapar redovisningsbudgetar för att förutse olika ekonomiska aktiviteter och koppla dimensioner för affärssystemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1311d566a8166a8a8720bb09789f42c65a1b6e7
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="a9d5a-103">Skapa redovisningsbudgetar</span><span class="sxs-lookup"><span data-stu-id="a9d5a-103">Create G/L Budgets</span></span>
<span data-ttu-id="a9d5a-104">Om du vill kan du använda flera olika budgetar för samma tidsperioder genom att skapa budgetar med separata namn.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="a9d5a-105">Först definierar du budgetnamnet och matar in budgetsiffrorna.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="a9d5a-106">Budgetnamnet infogas sedan i alla budgettransaktioner du skapar.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="a9d5a-107">När du skapar en budget kan du definiera fyra dimensioner för varje budget.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="a9d5a-108">De här budgetspecifika dimensionerna kallas för budgetdimensioner.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="a9d5a-109">Du kan välja budgetdimensionerna bland de dimensioner som redan finns upplagda.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="a9d5a-110">Budgetdimensioner kan användas för att skapa filter för en budget och lägga till dimensionsinformation till budgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="a9d5a-111">Mer information finns i [Arbeta med](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="a9d5a-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="a9d5a-112">Budgetar spelar en viktig roll i business intelligence, exempelvis i bokslut som baseras på kontoscheman som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i diagrammet över konton.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="a9d5a-113">Mer information finns i [Affärsstöd](bi.md).</span><span class="sxs-lookup"><span data-stu-id="a9d5a-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="a9d5a-114">Budgetar spelar en viktig roll i business intelligence, exempelvis i bokslut som baseras på kontoscheman som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i diagrammet över konton.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="a9d5a-115">Mer information finns i [Affärsstöd](bi.md).</span><span class="sxs-lookup"><span data-stu-id="a9d5a-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="a9d5a-116">I kostnadsredovisning arbetar du med kostnadsbudgetar på liknande sätt.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="a9d5a-117">(Mer information finns i [Skapa kostnadsbudgetar](finance-create-cost-budgets.md).)</span><span class="sxs-lookup"><span data-stu-id="a9d5a-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="a9d5a-118">Så här skapar du en ny redovisningsbudget</span><span class="sxs-lookup"><span data-stu-id="a9d5a-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="a9d5a-119">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Redovisningsbudgetar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a9d5a-120">Välj åtgärden **Redigera lista** och fyll sedan i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="a9d5a-121">Välj åtgärden **Redigera budget**.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="a9d5a-122">Högst upp i fönstret **Budget** fyller du i fälten för att definiera vad som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="a9d5a-123">Endast transaktioner som innehåller budgetnamnet som du angav i fältet **Budgetnamn** visas.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="a9d5a-124">Fönstret är för närvarande tomt eftersom budgetnamnet just har skapats och det därför inte finns några transaktioner som matchar filtret.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="a9d5a-125">Därför är fönstret tomt.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="a9d5a-126">Om du vill ange ett belopp väljer du relevant cell i matrisen.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="a9d5a-127">Fönstret **Redov.budgettransaktioner** öppnas.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="a9d5a-128">Skapa en ny rad och fyll i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="a9d5a-129">Stäng fönstret **Redov.budgettransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="a9d5a-130">Upprepa steg 5–6 tills du har angett alla budgetbeloppen.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a9d5a-131">På snabbfliken **Filter** kan du filtrera budgetinformationen beroende på hur många budgetdimensioner som definierats under budgetnamnet.</span><span class="sxs-lookup"><span data-stu-id="a9d5a-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="a9d5a-132">Se även</span><span class="sxs-lookup"><span data-stu-id="a9d5a-132">See Also</span></span>
[<span data-ttu-id="a9d5a-133">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="a9d5a-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="a9d5a-134">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="a9d5a-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="a9d5a-135">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="a9d5a-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="a9d5a-136">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="a9d5a-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="a9d5a-137">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9d5a-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

