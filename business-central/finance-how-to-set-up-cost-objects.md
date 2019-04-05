---
title: Så här skapar du kostnadsbärare | Microsoft Docs
description: Lär dig ställa in kostnadsbärare som motsvarar dimensionerna för redovisningen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 616fcbe937e556c17e8beb79f68bc961ea8bbe18
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808125"
---
# <a name="set-up-cost-objects"></a><span data-ttu-id="b55a8-103">Skapa kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="b55a8-103">Set Up Cost Objects</span></span>
<span data-ttu-id="b55a8-104">Kostnadsbärare är projekt, produkter eller tjänster i ett företag.</span><span class="sxs-lookup"><span data-stu-id="b55a8-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="b55a8-105">Planen för kostnadsbärare liknar dimensionsinformationen för redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b55a8-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="b55a8-106">Du kan definiera planen för kostnadsbärare på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="b55a8-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="b55a8-107">Överför dimensionsvärden i redovisningen till företagets plan för kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="b55a8-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="b55a8-108">Du kan göra nödvändiga justeringar efter överföringen.</span><span class="sxs-lookup"><span data-stu-id="b55a8-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="b55a8-109">Skapa en ny plan för kostnadsbäraren som är oberoende av redovisningen, eller lägg till en ny kostnadsbäraren i en befintlig plan för kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="b55a8-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="b55a8-110">Du måste skapa varje kostnadsbärare var för sig.</span><span class="sxs-lookup"><span data-stu-id="b55a8-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="b55a8-111">Så här överför du dimensionsvärden från redovisningen till kontoplanen för kostnadsbärare</span><span class="sxs-lookup"><span data-stu-id="b55a8-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="b55a8-112">Skapa en dimension som ska vara kostnadsbärardimensionen på sidan **Uppdatera CA-dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-112">Set a dimension to be the cost object dimension on the **Update CA Dimensions** page.</span></span> <span data-ttu-id="b55a8-113">Endast värdena från dimensionen överförs.</span><span class="sxs-lookup"><span data-stu-id="b55a8-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="b55a8-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lista över kostnadsbärare** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b55a8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="b55a8-115">Välj åtgärden **Hämta kostnadsbärare från dimension** för att överföra dimensionsvärden till planen för kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="b55a8-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="b55a8-116">Funktionen överför de dimensionsvärden som du har definierat i steg 1.</span><span class="sxs-lookup"><span data-stu-id="b55a8-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b55a8-117">Du kan ställa in fältet **Justera dimension för kostnadsbärare** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen.</span><span class="sxs-lookup"><span data-stu-id="b55a8-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="b55a8-118">Du kan inte definiera en synkronisering av diagrammet över kostnadsbärare till dimensionsvärden från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b55a8-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="b55a8-119">Diagrammet över kostnadsbärare innehåller nu alla angivna dimensionsvärden från redovisningen inklusive rubriker och delsummor.</span><span class="sxs-lookup"><span data-stu-id="b55a8-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a><span data-ttu-id="b55a8-120">Så här skapar du nya kostnadsbärare på sidan Lista över kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="b55a8-120">To create new cost objects in the Chart of Cost Objects page</span></span>  
<span data-ttu-id="b55a8-121">Du kan lägga upp och underhålla kostnadsbärare antingen i kortet **Kort för kostnadsbärare** eller på sidan **Lista över kostnadsbärare**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-121">You can set up and maintain cost objects in either the **Cost Object Card** card or on the **Chart of Cost Objects** page.</span></span> <span data-ttu-id="b55a8-122">I den här proceduren skapar du kostnadsbärare på sidan **Lista över kostnadsbärare**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-122">In this procedure, you set up cost objects on the **Chart of Cost Objects** page.</span></span>  

1.  <span data-ttu-id="b55a8-123">Öppna sidan **Lista över kostnadsbärare** i redigeringsläge.</span><span class="sxs-lookup"><span data-stu-id="b55a8-123">Open the **Chart of Cost Objects** page in edit mode.</span></span>  
2.  <span data-ttu-id="b55a8-124">Ange kostnadsbäraren kod i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="b55a8-125">Alla kostnadsbärare måste ha en kod.</span><span class="sxs-lookup"><span data-stu-id="b55a8-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="b55a8-126">Ange kostnadsbärarens namn i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="b55a8-127">Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsbäraren.</span><span class="sxs-lookup"><span data-stu-id="b55a8-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="b55a8-128">För kostnadsbärare av radtypen **Summa** fyller du i fältet **Summa från/till**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="b55a8-129">Använd operatorn **eller** som är ett vertikalt streck (**&#124;**), för att ange intervall av kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="b55a8-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="b55a8-130">För kostnadsbärare av radtypen **slutsumma** fylls det här fältet i automatiskt när du använder indragsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="b55a8-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="b55a8-131">Fyll i fältet **Bokföringsdatum**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="b55a8-132">Välj nästa tomma rad för att skapa en ny kostnadsbäraren och upprepa sedan steg 2 till 5.</span><span class="sxs-lookup"><span data-stu-id="b55a8-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="b55a8-133">När du har skapat alla kostnadsbärare, väljer du åtgärden **Indrag för kostnadsbärare**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="b55a8-134">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="b55a8-135">Om du har angett definitioner i fälten **Summa från/till** för **Till-summa** för kostnadsbärare innan du kör indragsfunktionen måste du ange dessa igen.</span><span class="sxs-lookup"><span data-stu-id="b55a8-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="b55a8-136">Funktionen ersätter värdena i alla fält för **slutsummor**.</span><span class="sxs-lookup"><span data-stu-id="b55a8-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b55a8-137">Se även</span><span class="sxs-lookup"><span data-stu-id="b55a8-137">See Also</span></span>  
[<span data-ttu-id="b55a8-138">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="b55a8-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="b55a8-139">[Definiera kostnadsställen och kostnadsbärare för kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="b55a8-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="b55a8-140">[Saldon mellan kostnadstyp, kostnadsställe och kostnadsbärare](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="b55a8-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="b55a8-141">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="b55a8-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="b55a8-142">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="b55a8-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="b55a8-143">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="b55a8-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="b55a8-144">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b55a8-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
