---
title: "Scenarioexempel - Definiera dynamisk distribution beräknad på sålda artiklar | Microsoft Docs"
description: "I det här avsnittet innehåller exempel på hur du definierar fördelningar med dynamisk fördelning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3103583c9781c283479c5f66e90f0e875faf46cc
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="a9e2e-103">Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar</span><span class="sxs-lookup"><span data-stu-id="a9e2e-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="a9e2e-104">I det här avsnittet innehåller exempel på hur du definierar fördelningar med dynamisk fördelning.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="a9e2e-105">I exemplet ändrar du dynamisk fördelning av kostnaderna för de SALES-kostnadsstället för att det ska fungera med den nya kostnadsbäraren IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="a9e2e-106">IT EQUIPMENT-paketet har artikelnummer i intervallet 8904-W till 8924-W.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="a9e2e-107">Du kan använda föregående års försäljningssiffror för att beräkna antalet andelen.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="a9e2e-108">Fördelningen bokförs på hjälpkostnadstypen 9903.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a9e2e-109">Exemplet använder demonstrationsdata i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a9e2e-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="a9e2e-110">Så här definierar du dynamisk fördelning beräknad på sålda artiklar under föregående år</span><span class="sxs-lookup"><span data-stu-id="a9e2e-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="a9e2e-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kostnadsfördelningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a9e2e-112">På sidan **Kostnadsfördelning** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-112">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="a9e2e-113">I fältet **ID**, tryck på Retur eller ange ett id.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="a9e2e-114">Ange **1** i fältet **Nivå**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="a9e2e-115">I fälten **Giltig från** och **Giltig till** anger du datum.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="a9e2e-116">Ange **FÖRS** i fältet **Kod för kostnadsställe**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="a9e2e-117">I fältet **Kreditera till kostnadstyp** anger du kostnadstyp **9903**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="a9e2e-118">I fältet **Målkostnadstyp** anger du kostnadstyp **9903**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="a9e2e-119">I fältet **Målkostnadsobjekt** välj **Ny** för att skapa den nya kostnadsbäraren IT EQUIPMENT och fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="a9e2e-120">Välj **IT EQUIPMENT**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="a9e2e-121">Låt fältet **Målkostnadsställe** vara tomt.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="a9e2e-122">I fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="a9e2e-123">I fältet **Bas** välj fördelningsbasen **Sålda artikler (belopp)**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="a9e2e-124">I fältet **Nummerfilter** anger du **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="a9e2e-125">I fältet **Kod för datumfilter** anger du **Föregående år**.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="a9e2e-126">Välj åtgärden **Beräkna fördelningsnyckel** för att beräkna andelen.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a9e2e-127">använder föregående år försäljningssiffror för att beräkna en andel för 1596,50 BVA till 100 procent för IT EQUIPMENT-paketet.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="a9e2e-128">Det innebär att alla sålda artiklar föregående år är fördelade på kostnadsbäraren IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="a9e2e-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a9e2e-129">Se även</span><span class="sxs-lookup"><span data-stu-id="a9e2e-129">See Also</span></span>  
[<span data-ttu-id="a9e2e-130">Definiera och fördela kostnader</span><span class="sxs-lookup"><span data-stu-id="a9e2e-130">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="a9e2e-131">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a9e2e-131">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="a9e2e-132">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="a9e2e-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

