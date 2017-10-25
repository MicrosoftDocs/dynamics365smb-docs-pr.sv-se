---
title: "Så här skapar du Lagerplatser | Microsoft Docs"
description: "Det effektivaste sättet att skapa lagerplatserna i distributionslagret på är att generera grupper med liknande lagerplatser i lagerplatsuppläggningsförslaget, men du kan även skapa en lagerplats i taget genom att följa anvisningarna nedan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 37a79ad08113b16bf0240d4c92eac6464015db07
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-bins"></a><span data-ttu-id="c802b-103">Så här: Skapa lagerplatser</span><span class="sxs-lookup"><span data-stu-id="c802b-103">How to: Create Bins</span></span>
<span data-ttu-id="c802b-104">Det effektivaste sättet att skapa lagerplatserna i distributionslagret på är att generera grupper med liknande lagerplatser i lagerplatsuppläggningsförslaget, men du kan även skapa en lagerplats i taget från lagerställekortet.</span><span class="sxs-lookup"><span data-stu-id="c802b-104">The most effective way to create the bins of your warehouse is to generate groups of similar bins in the bin creation worksheet, but you can also create your bins individually from the location card.</span></span> <span data-ttu-id="c802b-105">Du kan också använda en funktion i fönstret **Lagerplatsuppläggning förslag** för att skapa lagerplatserna automatiskt.</span><span class="sxs-lookup"><span data-stu-id="c802b-105">You can also use a function in the **Bin Creation Worksheet** window to create bins automatically.</span></span>  

## <a name="to-create-a-bin-from-the-location-card"></a><span data-ttu-id="c802b-106">Så här skapar du en lagerplats från lagerställekortet:</span><span class="sxs-lookup"><span data-stu-id="c802b-106">To create a bin from the location card</span></span>  
1.  <span data-ttu-id="c802b-107">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c802b-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and choose the related link.</span></span>  
2.  <span data-ttu-id="c802b-108">Markera lagerstället som du vill skapa en lagerplats från och välj åtgärden **Lagerplatser**</span><span class="sxs-lookup"><span data-stu-id="c802b-108">Select the location that you want to create a bin from, and then choose the **Bins** action.</span></span>  
3. <span data-ttu-id="c802b-109">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c802b-109">Choose the **New** action.</span></span>
4. <span data-ttu-id="c802b-110">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="c802b-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a><span data-ttu-id="c802b-111">Så här skapar du enstaka lagerplatser i Lagerplatsuppläggning förslag:</span><span class="sxs-lookup"><span data-stu-id="c802b-111">To create bins individually in the bin creation worksheet</span></span>  
1.  <span data-ttu-id="c802b-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerplatsuppläggning förslag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c802b-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="c802b-113">På varje rad fyller du i de fält som är nödvändiga för att namnge och ange egenskaper för de lagerplatser som du skapar.</span><span class="sxs-lookup"><span data-stu-id="c802b-113">Fill in on each line the fields that are necessary to name and characterize the bins you are creating.</span></span>  
3.  <span data-ttu-id="c802b-114">Välj åtgärden **Skapa lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="c802b-114">Choose the **Create Bins** action.</span></span>  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a><span data-ttu-id="c802b-115">Så här skapar du lagerplatser automatiskt i lagerplatsuppläggningsförslaget:</span><span class="sxs-lookup"><span data-stu-id="c802b-115">To make bins automatically in the bin creation worksheet</span></span>  
<span data-ttu-id="c802b-116">Innan du börjar skapa lagerplatser automatiskt i förslaget bör du bestämma vilken typ av lagerplatser som är viktiga för driften samt vilket artikelflöde som är mest praktiskt i den fysiska strukturen i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="c802b-116">Before you start creating bins automatically, you should determine the kind of bins that are essential for your operations, as well as the most practical flow of items through the physical structure of your warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c802b-117">När du använder en lagerplats inte kan du ta bort den om den inte är tom.</span><span class="sxs-lookup"><span data-stu-id="c802b-117">As soon as you use a bin, you cannot delete it unless it is empty.</span></span> <span data-ttu-id="c802b-118">Om du vill använda ett annat namngivningssystem för lagerplatser kan du dock använda grupperingsjournalen för att flytta artiklarna till ett nytt lagerplatssystem.</span><span class="sxs-lookup"><span data-stu-id="c802b-118">But if you want to use another bin-naming system, you can use the reclassification journal to in effect move your items to a new bin system.</span></span> <span data-ttu-id="c802b-119">Det här måste göras manuellt och är tidskrävande, så det är bättre att skapa lagerplatserna rätt från början.</span><span class="sxs-lookup"><span data-stu-id="c802b-119">This process is manual and takes time, however, so it is best to set up your bins correctly from the start.</span></span>  

<span data-ttu-id="c802b-120">Om du vill arbeta i fönstret **Lagerplatsuppläggning förslag** måste du ställas in som en lageranställd på det lagerställe där lagerplatserna finns.</span><span class="sxs-lookup"><span data-stu-id="c802b-120">To work with the **Bin Creation Worksheet** window, you must be set up as a warehouse employee at the location where the bins exist.</span></span> <span data-ttu-id="c802b-121">Mer information finns i [Så här skapar du Dist.lager personal](warehouse-how-to-set-up-warehouse-employees.md).</span><span class="sxs-lookup"><span data-stu-id="c802b-121">For more information, see [How to: Set Up Warehouse Employees](warehouse-how-to-set-up-warehouse-employees.md).</span></span>    

1.  <span data-ttu-id="c802b-122">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerplatsuppläggning förslag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c802b-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Creation Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c802b-123">Välj åtgärden **Beräkna lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="c802b-123">Choose the **Calculate Bins** action.</span></span>
3. <span data-ttu-id="c802b-124">Klicka på **Beräkna lagerplatser** i fältet **Lagerplatsmall kod** och välj den lagerplatsmall som du vill använda som modell när du skapar lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="c802b-124">In the **Calculate Bins** window, in the **Bin Template Code** field, select the bin template that you want to use as the model for the bins you are creating.</span></span>
4.  <span data-ttu-id="c802b-125">Fyll i en beskrivning av de lagerplatser som du håller på att skapa.</span><span class="sxs-lookup"><span data-stu-id="c802b-125">Fill in a description for the bins you are in the process of creating.</span></span>  
5.  <span data-ttu-id="c802b-126">Om du vill skapa lagerplatskoderna, fyller du i **från nr**</span><span class="sxs-lookup"><span data-stu-id="c802b-126">To create the bin codes, fill in the **From No.**</span></span> <span data-ttu-id="c802b-127">och **Till nr.**</span><span class="sxs-lookup"><span data-stu-id="c802b-127">and **To No.**</span></span> <span data-ttu-id="c802b-128">I de tre kategorierna som visas i fönstret: **ställning**, **sektion**, och **nivå.**</span><span class="sxs-lookup"><span data-stu-id="c802b-128">fields in the three categories shown in the window: **Rack**, **Section,**, and **Level.**</span></span> <span data-ttu-id="c802b-129">Lagerplatskoden kan bestå av högst 20 tecken.</span><span class="sxs-lookup"><span data-stu-id="c802b-129">The bin code can contain up to 20 characters.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c802b-130">Det antal tecken som du har angett i de tre kategorierna för något av fälten (t.ex. de tecken som du har angett i de tre fälten **Från nr**)</span><span class="sxs-lookup"><span data-stu-id="c802b-130">The number of characters that you have entered in the three categories for either field, for example, the characters you have entered in the three **From No.**</span></span> <span data-ttu-id="c802b-131">plus eventuella fältavgränsare, får högst vara 20.</span><span class="sxs-lookup"><span data-stu-id="c802b-131">fields, plus the field separators, if any, must be 20 or less.</span></span>  

     <span data-ttu-id="c802b-132">Du kan använda bokstäver i koden som en kombination för identifiering, men den bokstav som du använder måste vara samma i fältet **Från nr.**</span><span class="sxs-lookup"><span data-stu-id="c802b-132">You can use letters in the code as an identifying combination, but the letter you use must be the same in the **From No.**</span></span> <span data-ttu-id="c802b-133">och **Till nr.**</span><span class="sxs-lookup"><span data-stu-id="c802b-133">and **To No.**</span></span> <span data-ttu-id="c802b-134">.</span><span class="sxs-lookup"><span data-stu-id="c802b-134">fields.</span></span> <span data-ttu-id="c802b-135">Till exempel kanske du anger ställningsdelen av koden som **Från nr. A01** och **Till nr. A10**.</span><span class="sxs-lookup"><span data-stu-id="c802b-135">For example, you might define the Rack part of the code as **From No. A01** and **To No. A10**.</span></span> <span data-ttu-id="c802b-136">Programmet genererar inte koder i bokstavsordning, till exempel från A01 till F05.</span><span class="sxs-lookup"><span data-stu-id="c802b-136">The program is not set up to generate codes with letter sequences, for example, from A01 to F05.</span></span>  

6.  <span data-ttu-id="c802b-137">Om du vill att ett tecken, t.ex. ett bindestreck, ska avgränsa de kategorifält som du har definierat som en del av lagerplatskoden, fyller du i fältet **Fältseparator** med det tecknet.</span><span class="sxs-lookup"><span data-stu-id="c802b-137">If you want a character, such as a hyphen, to separate the category fields you have defined as part of the bin code, fill in the **Field Separator** field with this character.</span></span>  
7.  <span data-ttu-id="c802b-138">Om du inte vill att en rad ska skapas för en lagerplats om den redan finns, markerar du fältet **Kontrollera existerande lagerplats**.</span><span class="sxs-lookup"><span data-stu-id="c802b-138">If you want the program not to create a line for a bin if it exists already, select the **Check on Existing Bin** field.</span></span>  
8. <span data-ttu-id="c802b-139">När du är klar med att fylla i fälten klickar du på knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c802b-139">When you have finished filling in the fields, choose the **OK** Button.</span></span>

    <span data-ttu-id="c802b-140">En rad skapas för respektive lagerplats i förslaget.</span><span class="sxs-lookup"><span data-stu-id="c802b-140">The program creates a line for each bin in the worksheet.</span></span> <span data-ttu-id="c802b-141">Nu kan du ta bort några av lagerplatserna, till exempel om du har en ställning med en gång genom de två första nivåerna i ett par sektioner.</span><span class="sxs-lookup"><span data-stu-id="c802b-141">You can now delete some of the bins, for example, if you have a rack with a passageway through the first two levels of a couple of sections.</span></span>  

9. <span data-ttu-id="c802b-142">När du har tagit bort alla onödiga lagerplatser väljer du åtgärden **Skapa lagerplatser** så skapas lagerplatser för varje rad i förslaget.</span><span class="sxs-lookup"><span data-stu-id="c802b-142">When you have deleted all unnecessary bins, choose the **Create Bins** action, and the program will create bins for each line in the worksheet.</span></span>  

<span data-ttu-id="c802b-143">Upprepa processen för ytterligare en uppsättning lagerplatser tills du har skapat alla de lagerplatser som du ska ha i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="c802b-143">Repeat the process for another set of bins until you have created all the bins in your warehouse.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c802b-144">Se även</span><span class="sxs-lookup"><span data-stu-id="c802b-144">See Also</span></span>  
[<span data-ttu-id="c802b-145">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="c802b-145">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c802b-146">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="c802b-146">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c802b-147">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="c802b-147">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="c802b-148">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c802b-148">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c802b-149">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="c802b-149">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c802b-150">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c802b-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
