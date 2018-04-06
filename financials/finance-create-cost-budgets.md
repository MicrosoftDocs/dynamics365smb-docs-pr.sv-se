---
title: Skapa kostnadsbudgetar | Microsoft Docs
description: "Det här avsnittet innehåller en översikt över var du skapar och analyserar kostnadsbudgetar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25094427b1e87002de11afad487ecd09a8af2e30
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="creating-cost-budgets"></a><span data-ttu-id="a3bb2-103">Skapa kostnadsbudgetar</span><span class="sxs-lookup"><span data-stu-id="a3bb2-103">Creating Cost Budgets</span></span>
<span data-ttu-id="a3bb2-104">Budgetering för kostnadsredovisning liknar budgetering i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="a3bb2-105">En kostnadsbudget skapas baserat på kostnadstyper, precis som en budget för redovisningen skapas baserat på redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="a3bb2-106">En kostnadsbudget skapas för en viss tidsperiod, till exempel ett räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="a3bb2-107">Du kan skapa kostnadsbudgetar efter behov.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="a3bb2-108">Du kan skapa en ny kostnadsbudget manuellt eller genom att importera en kostnadsbudget eller genom att kopiera en befintlig kostnadsbudget som budgetbas.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="a3bb2-109">Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="a3bb2-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="a3bb2-110">Du kan använda följande fönster för att skapa och analysera kostnadsbudgetar.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-110">You use the following windows to create and analyze cost budgets.</span></span> <span data-ttu-id="a3bb2-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport") för att hitta ett fönster och sedan läsa knappbeskrivningen för varje.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon to find a window, and then read the tooltip for each.</span></span>

|<span data-ttu-id="a3bb2-112">Om du vill</span><span class="sxs-lookup"><span data-stu-id="a3bb2-112">To</span></span>|<span data-ttu-id="a3bb2-113">Gå till</span><span class="sxs-lookup"><span data-stu-id="a3bb2-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="a3bb2-114">Överföra budgetar från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="a3bb2-115">Batch-jobbet **Kopiera redovisningsbudget**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="a3bb2-116">Kopiera kostnadsbudgetar.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-116">Copy cost budgets.</span></span>|<span data-ttu-id="a3bb2-117">Batch-jobbet **Kopiera kostnadsbudget**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="a3bb2-118">Tilldela budgeterar.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-118">Allocate budgets.</span></span>|<span data-ttu-id="a3bb2-119">Sidan **Kostnadsfördelning**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="a3bb2-120">Visa kostnadsbudgetjournaler och kostnadsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="a3bb2-121">Sidan **Kostnadsbudgetregister**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="a3bb2-122">Skriv ut kostnadsbudgetjämförelser med hjälp av olika rapporter.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="a3bb2-123">Rapporten **Saldo/budget för kostnadsredovisning**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="a3bb2-124">Rapporten **Kostnadsredovisning, resultaträkning/budget**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="a3bb2-125">Rapporten **Kostnadsbudget per kostnadsställe**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="a3bb2-126">Rapporten **Kostnadsbudget per kostnadsbärare**</span><span class="sxs-lookup"><span data-stu-id="a3bb2-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="a3bb2-127">Se även</span><span class="sxs-lookup"><span data-stu-id="a3bb2-127">See Also</span></span>  
[<span data-ttu-id="a3bb2-128">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="a3bb2-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="a3bb2-129">Skapa redovisningsbudgetar</span><span class="sxs-lookup"><span data-stu-id="a3bb2-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="a3bb2-130">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a3bb2-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="a3bb2-131">Definiera och fördela kostnader</span><span class="sxs-lookup"><span data-stu-id="a3bb2-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="a3bb2-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3bb2-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

