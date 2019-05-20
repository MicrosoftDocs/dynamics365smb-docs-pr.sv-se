---
title: Skapa kostnadsbudgetar | Microsoft Docs
description: Det här avsnittet innehåller en översikt över var du skapar och analyserar kostnadsbudgetar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5b1fdcfb61d9836676a69c9912fd624bd078b950
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239780"
---
# <a name="creating-cost-budgets"></a><span data-ttu-id="e2f32-103">Skapa kostnadsbudgetar</span><span class="sxs-lookup"><span data-stu-id="e2f32-103">Creating Cost Budgets</span></span>
<span data-ttu-id="e2f32-104">Budgetering för kostnadsredovisning liknar budgetering i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e2f32-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="e2f32-105">En kostnadsbudget skapas baserat på kostnadstyper, precis som en budget för redovisningen skapas baserat på redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="e2f32-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="e2f32-106">En kostnadsbudget skapas för en viss tidsperiod, till exempel ett räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="e2f32-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="e2f32-107">Du kan skapa kostnadsbudgetar efter behov.</span><span class="sxs-lookup"><span data-stu-id="e2f32-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="e2f32-108">Du kan skapa en ny kostnadsbudget manuellt eller genom att importera en kostnadsbudget eller genom att kopiera en befintlig kostnadsbudget som budgetbas.</span><span class="sxs-lookup"><span data-stu-id="e2f32-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="e2f32-109">Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="e2f32-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="e2f32-110">Du kan använda följande sidor för att skapa och analysera kostnadsbudgetar.</span><span class="sxs-lookup"><span data-stu-id="e2f32-110">You use the following pages to create and analyze cost budgets.</span></span> <span data-ttu-id="e2f32-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") för att hitta en sida och läs sedan knappbeskrivningen för varje länk.</span><span class="sxs-lookup"><span data-stu-id="e2f32-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a page, and then read the tooltip for each.</span></span>

|<span data-ttu-id="e2f32-112">Till</span><span class="sxs-lookup"><span data-stu-id="e2f32-112">To</span></span>|<span data-ttu-id="e2f32-113">Gå till</span><span class="sxs-lookup"><span data-stu-id="e2f32-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="e2f32-114">Överföra budgetar från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e2f32-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="e2f32-115">Batch-jobbet **Kopiera redovisningsbudget**</span><span class="sxs-lookup"><span data-stu-id="e2f32-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="e2f32-116">Kopiera kostnadsbudgetar.</span><span class="sxs-lookup"><span data-stu-id="e2f32-116">Copy cost budgets.</span></span>|<span data-ttu-id="e2f32-117">Batch-jobbet **Kopiera kostnadsbudget**</span><span class="sxs-lookup"><span data-stu-id="e2f32-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="e2f32-118">Tilldela budgeterar.</span><span class="sxs-lookup"><span data-stu-id="e2f32-118">Allocate budgets.</span></span>|<span data-ttu-id="e2f32-119">Sidan **Kostnadsfördelning**</span><span class="sxs-lookup"><span data-stu-id="e2f32-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="e2f32-120">Visa kostnadsbudgetjournaler och kostnadsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e2f32-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="e2f32-121">Sidan **Kostnadsbudgetregister**</span><span class="sxs-lookup"><span data-stu-id="e2f32-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="e2f32-122">Skriv ut kostnadsbudgetjämförelser med hjälp av olika rapporter.</span><span class="sxs-lookup"><span data-stu-id="e2f32-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="e2f32-123">Rapporten **Saldo/budget för kostnadsredovisning**</span><span class="sxs-lookup"><span data-stu-id="e2f32-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="e2f32-124">Rapporten **Kostnadsredovisning, resultaträkning/budget**</span><span class="sxs-lookup"><span data-stu-id="e2f32-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="e2f32-125">Rapporten **Kostnadsbudget per kostnadsställe**</span><span class="sxs-lookup"><span data-stu-id="e2f32-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="e2f32-126">Rapporten **Kostnadsbudget per kostnadsbärare**</span><span class="sxs-lookup"><span data-stu-id="e2f32-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="e2f32-127">Se även</span><span class="sxs-lookup"><span data-stu-id="e2f32-127">See Also</span></span>  
[<span data-ttu-id="e2f32-128">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="e2f32-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="e2f32-129">Skapa redovisningsbudgetar</span><span class="sxs-lookup"><span data-stu-id="e2f32-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="e2f32-130">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="e2f32-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="e2f32-131">Definiera och fördela kostnader</span><span class="sxs-lookup"><span data-stu-id="e2f32-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="e2f32-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2f32-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
