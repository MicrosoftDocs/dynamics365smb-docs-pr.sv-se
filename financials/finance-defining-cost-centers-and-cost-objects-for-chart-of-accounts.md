---
title: "Definiera kostnadsställen och kostnadsbärare för kontoplanen | Microsoft Docs"
description: "Du kan automatiskt överföra kostnads- och intäktstransaktioner från redovisningen till kostnadsredovisningen antingen för varje redovisningsbokföring eller med ett batch-jobb. När du gör överföringen överför systemet endast de transaktioner som redan är länkade till ett kostnadsställe eller en kostnadsbärare. Om du vill skapa en meningsfullt överföring måste du kontrollera att kostnadsställena och kostnadsbärarna definierats korrekt."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="57570-105">Definiera kostnadsställen och kostnadsbärare för kontoplanen</span><span class="sxs-lookup"><span data-stu-id="57570-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="57570-106">Du kan automatiskt överföra kostnads- och intäktstransaktioner från redovisningen till kostnadsredovisningen antingen för varje redovisningsbokföring eller med ett batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="57570-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="57570-107">När du gör överföringen överför, [!INCLUDE[d365fin](includes/d365fin_md.md)] endast de transaktioner som redan är länkade till ett kostnadsställe eller en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="57570-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="57570-108">Om du vill skapa en meningsfullt överföring måste du kontrollera att kostnadsställena och kostnadsbärarna definierats korrekt.</span><span class="sxs-lookup"><span data-stu-id="57570-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="57570-109">Ange standarddimensionsvärden för redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="57570-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="57570-110">För varje redovisningskonto kan du ange standarddimensionsvärden i tabellen **Standarddimension**.</span><span class="sxs-lookup"><span data-stu-id="57570-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="57570-111">Följande exempel visar hur du anger att det alltid ska finnas ett kostnadsställe för avdelningen, men aldrig är en kostnadsbärare för ett projekt när du bokför på ett redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="57570-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="57570-112">**Dimensionskod**</span><span class="sxs-lookup"><span data-stu-id="57570-112">**Dimension Code**</span></span>|<span data-ttu-id="57570-113">**Bokförs med**</span><span class="sxs-lookup"><span data-stu-id="57570-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="57570-114">Avdelning</span><span class="sxs-lookup"><span data-stu-id="57570-114">Department</span></span>|<span data-ttu-id="57570-115">Kod alltid</span><span class="sxs-lookup"><span data-stu-id="57570-115">Code Mandatory</span></span>|  
|<span data-ttu-id="57570-116">Objekt</span><span class="sxs-lookup"><span data-stu-id="57570-116">Project</span></span>|<span data-ttu-id="57570-117">Ingen kod</span><span class="sxs-lookup"><span data-stu-id="57570-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="57570-118">Definiera dimensionsvärden för omkostnader och direkta kostnader</span><span class="sxs-lookup"><span data-stu-id="57570-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="57570-119">Du kan överföra omkostnader till ett kostnadsställe och direkta kostnader till en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="57570-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="57570-120">Följande tabell visar den optimala kombinationen av installationsvärden för dimensioner.</span><span class="sxs-lookup"><span data-stu-id="57570-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="57570-121">Överför till</span><span class="sxs-lookup"><span data-stu-id="57570-121">Transfer To</span></span>|<span data-ttu-id="57570-122">Kostnadsställebokföring</span><span class="sxs-lookup"><span data-stu-id="57570-122">Cost Center Posting</span></span>|<span data-ttu-id="57570-123">Kostnadsbärarbokföring</span><span class="sxs-lookup"><span data-stu-id="57570-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="57570-124">Kostnadsställe</span><span class="sxs-lookup"><span data-stu-id="57570-124">Cost Center</span></span>|<span data-ttu-id="57570-125">Kod alltid</span><span class="sxs-lookup"><span data-stu-id="57570-125">Code Mandatory</span></span>|<span data-ttu-id="57570-126">Ingen kod</span><span class="sxs-lookup"><span data-stu-id="57570-126">No Code</span></span>|  
|<span data-ttu-id="57570-127">Kostnadsbärare</span><span class="sxs-lookup"><span data-stu-id="57570-127">Cost Object</span></span>|<span data-ttu-id="57570-128">Ingen kod</span><span class="sxs-lookup"><span data-stu-id="57570-128">No Code</span></span>|<span data-ttu-id="57570-129">Kod alltid</span><span class="sxs-lookup"><span data-stu-id="57570-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="57570-130">Markera kryssrutan **Kontrollera redovisningsbokföringar** för att se till att de fördefinierade kostnadsställena och kostnadsbärarna som du skapar i redovisningen automatiskt överförs till kostnadsredovisningen.</span><span class="sxs-lookup"><span data-stu-id="57570-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="57570-131">Se även</span><span class="sxs-lookup"><span data-stu-id="57570-131">See Also</span></span>  
[<span data-ttu-id="57570-132">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="57570-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="57570-133">[Så här: Skapa kostnadsställen](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="57570-133">[How to: Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="57570-134">Så här: Skapa kostnadsbärare</span><span class="sxs-lookup"><span data-stu-id="57570-134">How to: Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="57570-135">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57570-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

