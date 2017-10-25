---
title: "Så här arbetar du med Lagerperioder | Microsoft Docs"
description: "Du kan styra den tidsperiod som användare kan bokföra ändringar i lagret genom att definiera lagerperioder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8f9c289f4fef06ef0b684dd7176630d29b2fc5d3
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-inventory-periods"></a><span data-ttu-id="b922d-103">Så här kan du arbeta med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="b922d-103">How to: Work with Inventory Periods</span></span>
<span data-ttu-id="b922d-104">Under en lagerperiod går det att bokföra ändringar i lagret.</span><span class="sxs-lookup"><span data-stu-id="b922d-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="b922d-105">Lagerperioden definieras utifrån slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="b922d-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="b922d-106">När en lagerperiod stängs kan inga ändringar bokföras i lagret, oavsett om de är förväntade eller rör faktureringen, före det här slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="b922d-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="b922d-107">Det går inte heller att bokföra nya värden i lagret före slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="b922d-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="b922d-108">Om det finns öppna artikeltransaktioner i den stängda perioden, d.v.s. positiva antal som ännu inte har kopplats till avgående transaktioner, går det fortfarande att koppla avgående antal till de här transaktionerna även om perioden är stängd.</span><span class="sxs-lookup"><span data-stu-id="b922d-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="b922d-109">I följande avsnitt finns beskrivningar om att:</span><span class="sxs-lookup"><span data-stu-id="b922d-109">The following sections describe how to:</span></span>  

* <span data-ttu-id="b922d-110">Skapa lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="b922d-110">Create inventory periods.</span></span>  
* <span data-ttu-id="b922d-111">Stänga lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="b922d-111">Close inventory periods.</span></span>  
* <span data-ttu-id="b922d-112">Öppna lagerperioder igen.</span><span class="sxs-lookup"><span data-stu-id="b922d-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="b922d-113">Skapa en lagerperiod</span><span class="sxs-lookup"><span data-stu-id="b922d-113">To create an inventory period</span></span>  
1. <span data-ttu-id="b922d-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerperioder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b922d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b922d-115">Skapa en ny rad.</span><span class="sxs-lookup"><span data-stu-id="b922d-115">Create a new line.</span></span>  
3. <span data-ttu-id="b922d-116">Ange det sista datumet för lagerperioden som definieras i fältet **Slutdatum**.</span><span class="sxs-lookup"><span data-stu-id="b922d-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="b922d-117">När perioden har stängts går det inte längre att bokföra lagerändringar före det här datumet.</span><span class="sxs-lookup"><span data-stu-id="b922d-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="b922d-118">Ange ett beskrivande namn i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="b922d-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="b922d-119">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="b922d-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="b922d-120">Stänga lagerperioder</span><span class="sxs-lookup"><span data-stu-id="b922d-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="b922d-121">I fältet **Stängd** anges om lagerperioden är stängd för lagervärdeändringar.</span><span class="sxs-lookup"><span data-stu-id="b922d-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="b922d-122">Fältet kan inte redigeras.</span><span class="sxs-lookup"><span data-stu-id="b922d-122">You cannot edit this field.</span></span>  

<span data-ttu-id="b922d-123">Det går att stänga vilken lagerperiod som helst, förutsatt att följande villkor är uppfyllda:</span><span class="sxs-lookup"><span data-stu-id="b922d-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="b922d-124">Det får inte finnas några öppna externa artikeltransaktioner, d.v.s. inget negativt lager, i den perioden.</span><span class="sxs-lookup"><span data-stu-id="b922d-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="b922d-125">Kostnaden för alla artiklar har justerats med batch-jobbet **Justera kost. - artikeltrans.**.</span><span class="sxs-lookup"><span data-stu-id="b922d-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="b922d-126">Detta innebär att alla avgående transaktionsantal (till exempel antalen från försäljningsorder, avgående överföringar, fakturor, inköpsreturer eller inköpskreditnotor) måste kopplas till ett befintligt antal i lagret.</span><span class="sxs-lookup"><span data-stu-id="b922d-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="b922d-127">Stänga en lagerperiod</span><span class="sxs-lookup"><span data-stu-id="b922d-127">To close an inventory period</span></span>  
1. <span data-ttu-id="b922d-128">Kör batch-jobbet **Justera kost. - artikeltrans.** innan en lagerperiod stängs för att säkerställa att alla kostnadsjusteringar har bokförts.</span><span class="sxs-lookup"><span data-stu-id="b922d-128">Before closing an inventory period, run the **Adjust Cost – Item Entries** batch job to ensure that all cost adjustments are posted.</span></span> <span data-ttu-id="b922d-129">På fliken **Åtgärder** i gruppen **Funktioner** väljer du **Justera kost. - artikeltrans.**.</span><span class="sxs-lookup"><span data-stu-id="b922d-129">On the **Actions** tab, in the **Functions** group, choose **Adjust Cost – Item Entries**.</span></span>  

     <span data-ttu-id="b922d-130">Kör rapporten **Stäng lagerperiod - test** för att avgöra om det finns öppna externa artikeltransaktioner i lagerperioden eller om det finns artiklar som saknar justerad kostnad.</span><span class="sxs-lookup"><span data-stu-id="b922d-130">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="b922d-131">Välj åtgärden **Stäng lagerperiod - Test**.</span><span class="sxs-lookup"><span data-stu-id="b922d-131">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="b922d-132">Kör batch-jobbet **Bokför lagerkostnad i redov.** för att säkerställa att alla kostnader har bokförts i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b922d-132">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="b922d-133">Välj åtgärden **Bokför lager i redov.**.</span><span class="sxs-lookup"><span data-stu-id="b922d-133">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="b922d-134">I fönstret **Lagerperioder** väljer du den lagerperiod du vill stänga.</span><span class="sxs-lookup"><span data-stu-id="b922d-134">In the **Inventory Periods** window, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="b922d-135">Välj åtgärden **Stäng period**.</span><span class="sxs-lookup"><span data-stu-id="b922d-135">Choose the **Close Period** action.</span></span> <span data-ttu-id="b922d-136">När lagerperioden har stängts kan inga lagerändringar bokföras före slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="b922d-136">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="b922d-137">Kostnaden för alla artiklar måste justeras med batch-jobbet **Justera kost. - artikeltrans.** innan lagerperioden kan stängas.</span><span class="sxs-lookup"><span data-stu-id="b922d-137">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="b922d-138">Klicka på **Ja** för att bekräfta stängningen av perioden eller klicka på **Nej** för att avbryta stängningen.</span><span class="sxs-lookup"><span data-stu-id="b922d-138">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="b922d-139">Lagerperioden stängs och en bekräftelse visas när stängningen är klar.</span><span class="sxs-lookup"><span data-stu-id="b922d-139">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="b922d-140">Öppna lagerperioder igen</span><span class="sxs-lookup"><span data-stu-id="b922d-140">Reopening Inventory Periods</span></span>  
<span data-ttu-id="b922d-141">När lagerperioden har stängts en gång går det inte längre att ta bort den.</span><span class="sxs-lookup"><span data-stu-id="b922d-141">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="b922d-142">Det går däremot att öppna lagerperioden igen om bokföring före lagerperiodens slutdatum ska tillåtas.</span><span class="sxs-lookup"><span data-stu-id="b922d-142">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="b922d-143">Om en period öppnas igen, öppnas även de lagerperioder som innehåller slutdatum som infaller efter slutdatumet för perioden som öppnas igen.</span><span class="sxs-lookup"><span data-stu-id="b922d-143">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="b922d-144">Öppna en lagerperiod igen</span><span class="sxs-lookup"><span data-stu-id="b922d-144">To reopen an inventory period</span></span>  
1. <span data-ttu-id="b922d-145">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerperioder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b922d-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b922d-146">Välj den lagerperiod som du vill öppna igen.</span><span class="sxs-lookup"><span data-stu-id="b922d-146">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="b922d-147">Välj åtgärdenden **Öppna period igen**.</span><span class="sxs-lookup"><span data-stu-id="b922d-147">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="b922d-148">Bekräfta att du vill öppna perioden igen.</span><span class="sxs-lookup"><span data-stu-id="b922d-148">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="b922d-149">Alla lagerperioder med slutdatum efter perioden som du har valt öppnas igen.</span><span class="sxs-lookup"><span data-stu-id="b922d-149">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b922d-150">Se även</span><span class="sxs-lookup"><span data-stu-id="b922d-150">See Also</span></span>  
[<span data-ttu-id="b922d-151">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="b922d-151">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="b922d-152">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="b922d-152">Finance</span></span>](finance.md)  
[<span data-ttu-id="b922d-153">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="b922d-153">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b922d-154">Arbeta med Financials</span><span class="sxs-lookup"><span data-stu-id="b922d-154">Working with Financials</span></span>](ui-work-product.md)

