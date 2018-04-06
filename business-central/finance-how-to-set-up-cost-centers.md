---
title: "Så här skapar du kostnadsställen | Microsoft Docs"
description: "Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter. Planen för kostnadsställen liknar dimensionsinformationen för redovisningen."
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
ms.openlocfilehash: 92d3e28fc9d7dc5aa9b2c5e25df6a0c965ab725d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-centers"></a><span data-ttu-id="38270-104">Skapa kostnadsgrupper</span><span class="sxs-lookup"><span data-stu-id="38270-104">Set Up Cost Centers</span></span>
<span data-ttu-id="38270-105">Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter.</span><span class="sxs-lookup"><span data-stu-id="38270-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="38270-106">Planen för kostnadsställen liknar dimensionsinformationen för redovisningen.</span><span class="sxs-lookup"><span data-stu-id="38270-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="38270-107">Du kan definiera planen för kostnadsställen på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="38270-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="38270-108">Överför dimensionsvärden i redovisningen till företagets plan för kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="38270-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="38270-109">Du kan göra nödvändiga justeringar efter överföringen.</span><span class="sxs-lookup"><span data-stu-id="38270-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="38270-110">Skapa en ny plan för kostnadsstället som är oberoende av redovisningen, eller lägg till ett nytt kostnadsställe i en befintlig plan för kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="38270-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="38270-111">Du måste skapa varje kostnadsställe var för sig.</span><span class="sxs-lookup"><span data-stu-id="38270-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="38270-112">Överföra dimensionsvärden i redovisningen till planen för kostnadsställen</span><span class="sxs-lookup"><span data-stu-id="38270-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="38270-113">Skapa en dimension som ska vara kostnadsställesdimensionen i fönstret **Uppdatera kostnadsredovisningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="38270-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="38270-114">Endast värdena från dimensionen överförs.</span><span class="sxs-lookup"><span data-stu-id="38270-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="38270-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lista över kostnadsställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="38270-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="38270-116">Välj **Hämta kostnadsställen från dimension** för att överföra dimensionsvärden till planen för kostnadsställen på fliken **Åtgärder** i gruppen **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="38270-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="38270-117">Funktionen överför de dimensionsvärden som du har definierat i steg 1.</span><span class="sxs-lookup"><span data-stu-id="38270-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="38270-118">Du kan ställa in fältet **Justera dimension för kostnadsställe** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="38270-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="38270-119">Du kan inte definiera en synkronisering av diagrammet över kostnadsställen till dimensionsvärden från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="38270-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="38270-120">Diagrammet över kostnadsställen innehåller nu alla angivna dimensionsvärden från redovisningen inklusive titlar och delsummor.</span><span class="sxs-lookup"><span data-stu-id="38270-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="38270-121">Så här skapar du nya kostnadsställen i fönstret Lista över kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="38270-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="38270-122">Du kan lägga upp och underhålla kostnadsställen antingen i kortet **Kort för kostnadsställe** eller i fönstret **Lista över kostnadsställen**.</span><span class="sxs-lookup"><span data-stu-id="38270-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="38270-123">I den här proceduren skapar du kostnadsställen i fönstret **Lista över kostnadsställen**.</span><span class="sxs-lookup"><span data-stu-id="38270-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="38270-124">Öppna fönstret **Lista över kostnadsställen** i redigeringsläge.</span><span class="sxs-lookup"><span data-stu-id="38270-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="38270-125">Ange kostnadsställets kod i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="38270-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="38270-126">Alla kostnadsställen måste ha en kod.</span><span class="sxs-lookup"><span data-stu-id="38270-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="38270-127">Ange kostnadsställets namn i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="38270-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="38270-128">Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsstället.</span><span class="sxs-lookup"><span data-stu-id="38270-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="38270-129">För kostnadsställen av typen **Summa** måste du fylla fältet **Summering**.</span><span class="sxs-lookup"><span data-stu-id="38270-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="38270-130">Använd **eller** operatorn som är en vertikal rad (**&#124;**) för att ange intervall av kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="38270-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="38270-131">För kostnadsställen av radtypen **till-summa** fylls det här fältet i automatiskt när du använder indragsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="38270-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="38270-132">Fyll i fälten **Sorteringsordning** och **Kostnadssubtyp**.</span><span class="sxs-lookup"><span data-stu-id="38270-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="38270-133">Välj nästa tomma rad för att skapa ett nytt kostnadsställe, och upprepa sedan steg 2 till 5.</span><span class="sxs-lookup"><span data-stu-id="38270-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="38270-134">När du har skapat alla kostnadsställen, väljer du åtgärden **Indrag för kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="38270-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="38270-135">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="38270-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="38270-136">Om du har angett definitioner i fältet  **Summering** för **Till-summa**-kostnadsställen innan du kör indragsfunktionen måste du ange dessa igen.</span><span class="sxs-lookup"><span data-stu-id="38270-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="38270-137">Funktionen ersätter värdena i alla fält för **slutsummor**.</span><span class="sxs-lookup"><span data-stu-id="38270-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="38270-138">Se även</span><span class="sxs-lookup"><span data-stu-id="38270-138">See Also</span></span>  
[<span data-ttu-id="38270-139">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="38270-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="38270-140">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="38270-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="38270-141">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="38270-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="38270-142">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="38270-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="38270-143">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="38270-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

