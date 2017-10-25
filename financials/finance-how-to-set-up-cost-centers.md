---
title: "Så här skapar du kostnadsställen | Microsoft Docs"
description: "Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter. Planen för kostnadsställen liknar dimensionsinformationen för redovisningen."
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
ms.openlocfilehash: 433526fbd2a13f32e64be94cc1936151445c19f5
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cost-centers"></a><span data-ttu-id="15589-104">Så här: Skapa kostnadsställen</span><span class="sxs-lookup"><span data-stu-id="15589-104">How to: Set Up Cost Centers</span></span>
<span data-ttu-id="15589-105">Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter.</span><span class="sxs-lookup"><span data-stu-id="15589-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="15589-106">Planen för kostnadsställen liknar dimensionsinformationen för redovisningen.</span><span class="sxs-lookup"><span data-stu-id="15589-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="15589-107">Du kan definiera planen för kostnadsställen på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="15589-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="15589-108">Överför dimensionsvärden i redovisningen till företagets plan för kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="15589-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="15589-109">Du kan göra nödvändiga justeringar efter överföringen.</span><span class="sxs-lookup"><span data-stu-id="15589-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="15589-110">Skapa en ny plan för kostnadsstället som är oberoende av redovisningen, eller lägg till ett nytt kostnadsställe i en befintlig plan för kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="15589-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="15589-111">Du måste skapa varje kostnadsställe var för sig.</span><span class="sxs-lookup"><span data-stu-id="15589-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="15589-112">Överföra dimensionsvärden i redovisningen till planen för kostnadsställen</span><span class="sxs-lookup"><span data-stu-id="15589-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="15589-113">Skapa en dimension som ska vara kostnadsställesdimensionen i fönstret **Uppdatera kostnadsredovisningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="15589-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="15589-114">Endast värdena från dimensionen överförs.</span><span class="sxs-lookup"><span data-stu-id="15589-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="15589-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lista över kostnadsställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="15589-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="15589-116">Välj **Hämta kostnadsställen från dimension** för att överföra dimensionsvärden till planen för kostnadsställen på fliken **Åtgärder** i gruppen **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="15589-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="15589-117">Funktionen överför de dimensionsvärden som du har definierat i steg 1.</span><span class="sxs-lookup"><span data-stu-id="15589-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="15589-118">Du kan ställa in fältet **Justera dimension för kostnadsställe** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="15589-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="15589-119">Du kan inte definiera en synkronisering av diagrammet över kostnadsställen till dimensionsvärden från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="15589-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="15589-120">Diagrammet över kostnadsställen innehåller nu alla angivna dimensionsvärden från redovisningen inklusive titlar och delsummor.</span><span class="sxs-lookup"><span data-stu-id="15589-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="15589-121">Så här skapar du nya kostnadsställen i fönstret Lista över kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="15589-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="15589-122">Du kan lägga upp och underhålla kostnadsställen antingen i kortet **Kort för kostnadsställe** eller i fönstret **Lista över kostnadsställen**.</span><span class="sxs-lookup"><span data-stu-id="15589-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="15589-123">I den här proceduren skapar du kostnadsställen i fönstret **Lista över kostnadsställen**.</span><span class="sxs-lookup"><span data-stu-id="15589-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="15589-124">Öppna fönstret **Lista över kostnadsställen** i redigeringsläge.</span><span class="sxs-lookup"><span data-stu-id="15589-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="15589-125">Ange kostnadsställets kod i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="15589-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="15589-126">Alla kostnadsställen måste ha en kod.</span><span class="sxs-lookup"><span data-stu-id="15589-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="15589-127">Ange kostnadsställets namn i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="15589-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="15589-128">Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsstället.</span><span class="sxs-lookup"><span data-stu-id="15589-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="15589-129">För kostnadsställen av typen **Summa** måste du fylla fältet **Summering**.</span><span class="sxs-lookup"><span data-stu-id="15589-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="15589-130">Använd **eller** operatorn som är en vertikal rad (**&#124;**) för att ange intervall av kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="15589-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="15589-131">För kostnadsställen av radtypen **till-summa** fylls det här fältet i automatiskt när du använder indragsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="15589-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="15589-132">Fyll i fälten **Sorteringsordning** och **Kostnadssubtyp**.</span><span class="sxs-lookup"><span data-stu-id="15589-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="15589-133">Välj nästa tomma rad för att skapa ett nytt kostnadsställe, och upprepa sedan steg 2 till 5.</span><span class="sxs-lookup"><span data-stu-id="15589-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="15589-134">När du har skapat alla kostnadsställen, väljer du åtgärden **Indrag för kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="15589-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="15589-135">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="15589-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="15589-136">Om du har angett definitioner i fältet  **Summering** för **Till-summa**-kostnadsställen innan du kör indragsfunktionen måste du ange dessa igen.</span><span class="sxs-lookup"><span data-stu-id="15589-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="15589-137">Funktionen ersätter värdena i alla fält för **slutsummor**.</span><span class="sxs-lookup"><span data-stu-id="15589-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="15589-138">Se även</span><span class="sxs-lookup"><span data-stu-id="15589-138">See Also</span></span>  
[<span data-ttu-id="15589-139">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="15589-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="15589-140">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="15589-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="15589-141">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="15589-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="15589-142">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="15589-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="15589-143">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="15589-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

