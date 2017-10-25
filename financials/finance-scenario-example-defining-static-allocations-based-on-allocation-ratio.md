---
title: "Definiera fast distribution beräknad på fördelningskvot | Microsoft Docs"
description: "Statisk fördelning är baserad på ett visst värde, till exempel kvadratmeter eller en fastställd fördelningskvot, till exempel 5:2:4."
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
ms.openlocfilehash: b48d7f73b640b98d0cdab6e2e7e7486a3bdb39db
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="0ccb3-103">Scenarioexempel: Definiera fast distribution beräknad på fördelningskvot</span><span class="sxs-lookup"><span data-stu-id="0ccb3-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="0ccb3-104">Statisk fördelning är baserad på ett visst värde, till exempel kvadratmeter eller en fastställd fördelningskvot, till exempel 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="0ccb3-105">I det här avsnittet beskrivs hur du definierar tre nya kostnadsbärare som är fördelningsmål för fördelningskällan PROD-kostnadsstället med hjälp av den etablerade fördelningskvoten 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="0ccb3-106">De tre målkostnadsbärarna är ACCESSO, PAINT och FITTINGS.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0ccb3-107">Exemplet använder demonstrationsdata i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0ccb3-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="0ccb3-108">Så här definierar du fördelningskällan PROD-kostnadsstället på snabbfliken Allmänt</span><span class="sxs-lookup"><span data-stu-id="0ccb3-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="0ccb3-109">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kostnadsfördelning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0ccb3-110">I fönstret **Kostnadsfördelning** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="0ccb3-111">I fältet **ID**, tryck på Retur eller ange ett id.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="0ccb3-112">Ange **1** i fältet **Nivå**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="0ccb3-113">I fälten **Giltig från** och **Giltig till** anger du datum.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="0ccb3-114">Ange **PROD** i fältet **Kod för kostnadsställe**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="0ccb3-115">I fältet **Kreditera till kostnadstyp** anger du kostnadstyp **9903**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="0ccb3-116">Då här definierar du kostnadsbärarna som är fördelningsmål på snabbfliken Rader</span><span class="sxs-lookup"><span data-stu-id="0ccb3-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="0ccb3-117">Ange **9903** i fältet **Målkostnadstyp** på den första raden.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="0ccb3-118">Välj **ACCESSO** i fältet **Målkostnadsobjekt** på den första raden.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="0ccb3-119">På den första raden, i fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="0ccb3-120">På den första raden, i fältet **Bas**, markera **Fast** för att använda fast fördelning.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="0ccb3-121">På den första raden, i fältet **Del**, ange fördelningssatsen **5**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="0ccb3-122">Ange **9903** i fältet **Målkostnadstyp** på den andra raden.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="0ccb3-123">Välj **PAINT** i fältet **Målkostnadsobjekt** på den andra raden.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="0ccb3-124">På den andra raden, i fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="0ccb3-125">På den andra raden, i fältet **Bas**, markera **Fast** för att använda fast fördelning.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="0ccb3-126">På den andra raden, i fältet **Del**, ange fördelningssatsen **2**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="0ccb3-127">Ange **9903** i fältet **Målkostnadstyp** på den andra raden.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="0ccb3-128">Välj **FITTINGS** i fältet **Målkostnadsobjekt** på tredje raden.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="0ccb3-129">På tredje raden, i fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="0ccb3-130">På tredje raden, i fältet **Bas**, markera **Fast** för att använda fast fördelning.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="0ccb3-131">På tredje raden, i fältet **Del**, ange fördelningssatsen **4**.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0ccb3-132"> beräknar automatiskt fältet **Procent** med hjälp av ett procenttal som är beroende av alla tre fördelningskvoterna, som anges i fältet **Del** för alla tre rader.</span><span class="sxs-lookup"><span data-stu-id="0ccb3-132"> automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ccb3-133">Se även</span><span class="sxs-lookup"><span data-stu-id="0ccb3-133">See Also</span></span>  
<span data-ttu-id="0ccb3-134">[Så här: ställa in fördelningskälla och mål](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="0ccb3-134">[How to: Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="0ccb3-135">[Definiera och fördela kostnader](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="0ccb3-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="0ccb3-136">[Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="0ccb3-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="0ccb3-137">Definiera och fördela kostnader</span><span class="sxs-lookup"><span data-stu-id="0ccb3-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

