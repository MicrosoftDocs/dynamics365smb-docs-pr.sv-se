---
title: "Definiera kostnadsställen och kostnadsbärare för kontoplanen | Microsoft Docs"
description: "Du kan automatiskt överföra kostnads- och intäktstransaktioner från redovisningen till kostnadsredovisningen antingen för varje redovisningsbokföring eller med ett batch-jobb. När du gör överföringen överför systemet endast de transaktioner som redan är länkade till ett kostnadsställe eller en kostnadsbärare. Om du vill skapa en meningsfullt överföring måste du kontrollera att kostnadsställena och kostnadsbärarna definierats korrekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5da3967e99bf8a1d5628159a542885ffd1113a02
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="8c5af-105">Definiera kostnadsställen och kostnadsbärare för kontoplanen</span><span class="sxs-lookup"><span data-stu-id="8c5af-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="8c5af-106">Du kan automatiskt överföra kostnads- och intäktstransaktioner från redovisningen till kostnadsredovisningen antingen för varje redovisningsbokföring eller med ett batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="8c5af-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="8c5af-107">När du gör överföringen överför, [!INCLUDE[d365fin](includes/d365fin_md.md)] endast de transaktioner som redan är länkade till ett kostnadsställe eller en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="8c5af-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="8c5af-108">Om du vill skapa en meningsfullt överföring måste du kontrollera att kostnadsställena och kostnadsbärarna definierats korrekt.</span><span class="sxs-lookup"><span data-stu-id="8c5af-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="8c5af-109">Ange standarddimensionsvärden för redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="8c5af-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="8c5af-110">För varje redovisningskonto kan du ange standarddimensionsvärden i tabellen **Standarddimension**.</span><span class="sxs-lookup"><span data-stu-id="8c5af-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="8c5af-111">Följande exempel visar hur du anger att det alltid ska finnas ett kostnadsställe för avdelningen, men aldrig är en kostnadsbärare för ett projekt när du bokför på ett redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="8c5af-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="8c5af-112">**Dimensionskod**</span><span class="sxs-lookup"><span data-stu-id="8c5af-112">**Dimension Code**</span></span>|<span data-ttu-id="8c5af-113">**Bokförs med**</span><span class="sxs-lookup"><span data-stu-id="8c5af-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="8c5af-114">Avdelning</span><span class="sxs-lookup"><span data-stu-id="8c5af-114">Department</span></span>|<span data-ttu-id="8c5af-115">Kod alltid</span><span class="sxs-lookup"><span data-stu-id="8c5af-115">Code Mandatory</span></span>|  
|<span data-ttu-id="8c5af-116">Objekt</span><span class="sxs-lookup"><span data-stu-id="8c5af-116">Project</span></span>|<span data-ttu-id="8c5af-117">Ingen kod</span><span class="sxs-lookup"><span data-stu-id="8c5af-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="8c5af-118">Definiera dimensionsvärden för omkostnader och direkta kostnader</span><span class="sxs-lookup"><span data-stu-id="8c5af-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="8c5af-119">Du kan överföra omkostnader till ett kostnadsställe och direkta kostnader till en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="8c5af-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="8c5af-120">Följande tabell visar den optimala kombinationen av installationsvärden för dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8c5af-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="8c5af-121">Överför till</span><span class="sxs-lookup"><span data-stu-id="8c5af-121">Transfer To</span></span>|<span data-ttu-id="8c5af-122">Kostnadsställebokföring</span><span class="sxs-lookup"><span data-stu-id="8c5af-122">Cost Center Posting</span></span>|<span data-ttu-id="8c5af-123">Kostnadsbärarbokföring</span><span class="sxs-lookup"><span data-stu-id="8c5af-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="8c5af-124">Kostnadsställe</span><span class="sxs-lookup"><span data-stu-id="8c5af-124">Cost Center</span></span>|<span data-ttu-id="8c5af-125">Kod alltid</span><span class="sxs-lookup"><span data-stu-id="8c5af-125">Code Mandatory</span></span>|<span data-ttu-id="8c5af-126">Ingen kod</span><span class="sxs-lookup"><span data-stu-id="8c5af-126">No Code</span></span>|  
|<span data-ttu-id="8c5af-127">Kostnadsbärare</span><span class="sxs-lookup"><span data-stu-id="8c5af-127">Cost Object</span></span>|<span data-ttu-id="8c5af-128">Ingen kod</span><span class="sxs-lookup"><span data-stu-id="8c5af-128">No Code</span></span>|<span data-ttu-id="8c5af-129">Kod alltid</span><span class="sxs-lookup"><span data-stu-id="8c5af-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="8c5af-130">Markera kryssrutan **Kontrollera redovisningsbokföringar** för att se till att de fördefinierade kostnadsställena och kostnadsbärarna som du skapar i redovisningen automatiskt överförs till kostnadsredovisningen.</span><span class="sxs-lookup"><span data-stu-id="8c5af-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c5af-131">Se även</span><span class="sxs-lookup"><span data-stu-id="8c5af-131">See Also</span></span>  
[<span data-ttu-id="8c5af-132">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="8c5af-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="8c5af-133">[Skapa kostnadsgrupper](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="8c5af-133">[Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="8c5af-134">Skapa kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8c5af-134">Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="8c5af-135">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c5af-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

