---
title: "Definiera prissättning och kostnader för service | Microsoft Docs"
description: "Så här: registrera prissättning och alternativa kostnader för service"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d0f0fcdff4a67df7542c5acb6d44f804997d1a2c
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-pricing-and-additional-costs-for-services"></a><span data-ttu-id="9a770-103">Så här: registrera prissättning och alternativa kostnader för service</span><span class="sxs-lookup"><span data-stu-id="9a770-103">How to: Set Up Pricing and Additional Costs for Services</span></span>
<span data-ttu-id="9a770-104">Med prissättningsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du göra inställningar i och anpassa programmet så att du tillämpar och justerar priser för serviceartiklar, reparationer och order.</span><span class="sxs-lookup"><span data-stu-id="9a770-104">You can use the [!INCLUDE[d365fin](includes/d365fin_md.md)] pricing features to set up and customize your application so that you apply and adjust pricing on service items, repairs, and orders.</span></span> <span data-ttu-id="9a770-105">Dessa beslut om prissättning överförs sedan till faktureringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="9a770-105">These pricing decisions are then easily transmitted to the invoicing process.</span></span>  
  
<span data-ttu-id="9a770-106">Om det behövs kan du skapa prisgrupper och mappa dem till specifika tidsperioder, kunder eller valutor.</span><span class="sxs-lookup"><span data-stu-id="9a770-106">As your implementation requires, you can set up pricing groups and map them to specific time periods, customers, or currency.</span></span> <span data-ttu-id="9a770-107">Du kan lägga upp fast, minsta eller högsta pris beroende på servicekontrakten som du har med kunderna.</span><span class="sxs-lookup"><span data-stu-id="9a770-107">You can set up fixed, minimum, or maximum pricing, depending on the service contracts that you have with customers.</span></span> <span data-ttu-id="9a770-108">När du har justerat priserna kan du visa och godkänna ändringarna innan du sparar dem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="9a770-108">Finally, as you adjust your prices, you can view and approve the changes before committing them to the ledger.</span></span>  

## <a name="to-set-up-a-service-price-group"></a><span data-ttu-id="9a770-109">Så här skapar du en serviceprisgrupp</span><span class="sxs-lookup"><span data-stu-id="9a770-109">To set up a service price group</span></span>
<span data-ttu-id="9a770-110">Du kan lägga upp grupper med serviceartiklar om du vill ha samma speciella serviceprissättning.</span><span class="sxs-lookup"><span data-stu-id="9a770-110">You can set up groups containing service items that you want to receive the same special service pricing.</span></span> <span data-ttu-id="9a770-111">Du tilldelar serviceprisgrupper till serviceartiklar på serviceartikelrader.</span><span class="sxs-lookup"><span data-stu-id="9a770-111">You assign service price groups to service items on service item lines.</span></span> <span data-ttu-id="9a770-112">Du kan även tilldela serviceprisgrupper till serviceartikelgrupper.</span><span class="sxs-lookup"><span data-stu-id="9a770-112">You can also assign service price groups to service item groups.</span></span>  

1. <span data-ttu-id="9a770-113">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceprisgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9a770-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Price Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a770-114">Skapa en ny serviceprisgrupp.</span><span class="sxs-lookup"><span data-stu-id="9a770-114">Create a new service price group.</span></span>  
3. <span data-ttu-id="9a770-115">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="9a770-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="9a770-116">Välj åtgärden **Installation**.</span><span class="sxs-lookup"><span data-stu-id="9a770-116">Choose the **Setup** action.</span></span>  
2. <span data-ttu-id="9a770-117">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="9a770-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > <span data-ttu-id="9a770-118">Fälten **Justeringstyp** och **Belopp** samarbetar för att ange om denna justering gäller ett fast belopp, eller bara gäller när det totala servicepriset överskrider eller är lägre än det belopp som anges i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="9a770-118">The **Adjustment Type** and **Amount** fields work together to specify whether an adjustment concerns a fixed amount, or applies only when the total service price exceeds or is lower than the amount in the **Amount** field.</span></span>  

## <a name="to-set-up-a-service-price-adjustment-group"></a><span data-ttu-id="9a770-119">Så här skapar du serviceprisjusteringsgrupper</span><span class="sxs-lookup"><span data-stu-id="9a770-119">To set up a service price adjustment group</span></span>  
<span data-ttu-id="9a770-120">Du kan ställa in prisjusteringsgrupper för att justera servicepriset för serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="9a770-120">You can set up price adjustment groups to adjust service pricing of service items.</span></span> <span data-ttu-id="9a770-121">skapa en prisjusteringsgrupp som justerar priset för frakt eller reservdelar.</span><span class="sxs-lookup"><span data-stu-id="9a770-121">For example, you can set up price adjustment groups that adjust price of freight or spare parts.</span></span>  
  
1. <span data-ttu-id="9a770-122">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceprisgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9a770-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Price Adjustment Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a770-123">Skapa en ny serviceprisjusteringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="9a770-123">Create a new service price adjustment group.</span></span>  
3. <span data-ttu-id="9a770-124">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="9a770-124">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="9a770-125">I fältet **Typ** anger du den transaktionstyp som du vill justera.</span><span class="sxs-lookup"><span data-stu-id="9a770-125">In the **Type** field, enter the type of the entry that you want to adjust.</span></span>  
  
    * <span data-ttu-id="9a770-126">Om du vill justera endast en specifik post, anger du numret på transaktionen i fältet **nr.**</span><span class="sxs-lookup"><span data-stu-id="9a770-126">To adjust only one specific entry, enter the number of this entry in the **No.**</span></span> <span data-ttu-id="9a770-127">.</span><span class="sxs-lookup"><span data-stu-id="9a770-127">field.</span></span> <span data-ttu-id="9a770-128">Om du låter det här fältet vara tomt justerar justeringsgruppen ALLA poster av den typ som definierats i fältet **Radtyp**.</span><span class="sxs-lookup"><span data-stu-id="9a770-128">When you leave this field blank, your adjustment group will adjust all entries of the type defined in the **Type** field.</span></span>  
    * <span data-ttu-id="9a770-129">Om du vill justera servicepriser som bara gäller en specifik service, fyller du i fältet **arbetstyp**.</span><span class="sxs-lookup"><span data-stu-id="9a770-129">To adjust service prices related to only one specific service, fill in the **Work Type** field.</span></span> <span data-ttu-id="9a770-130">Om du låter det här fältet vara tomt ignoreras det.</span><span class="sxs-lookup"><span data-stu-id="9a770-130">When you leave this field blank, it will just be ignored.</span></span>  
  
5. <span data-ttu-id="9a770-131">Du kan ge en kort beskrivning av serviceprisjusteringen i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="9a770-131">In the **Description** field, enter a short description of the service price adjustment.</span></span>  
6. <span data-ttu-id="9a770-132">Om du vill justera servicepriser relaterade till bara en specifik produktbokföringsmall, fyller du i fältet **Produktbokföringsmall**.</span><span class="sxs-lookup"><span data-stu-id="9a770-132">To adjust service prices related to only one specific general product posting group, fill in the **Gen. Prod. Posting Group** field.</span></span>

> [!Tip]
> <span data-ttu-id="9a770-133">Du kan välja **uppgifter** för att lägga till ytterligare information om justeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="9a770-133">You can choose **Details** to add additional information about the adjustment group.</span></span> <span data-ttu-id="9a770-134">Du kan till exempel ange vilken artikel som tillhör serviceprisjusteringsgruppen och om det är en artikel, en resurs, en resursgrupp eller en serviceavgift.</span><span class="sxs-lookup"><span data-stu-id="9a770-134">For example, you can specify which item belongs to the service price adjustment group, and whether this is an item, a resource, a resource group, or a service charge.</span></span>  

## <a name="to-set-up-additional-costs-for-services"></a><span data-ttu-id="9a770-135">Så här: registrera alternativa kostnader för tjänster</span><span class="sxs-lookup"><span data-stu-id="9a770-135">To set up additional costs for services</span></span>
<span data-ttu-id="9a770-136">När du arbetar med serviceartiklar och serviceorder kanske du behöver registrera ytterligare kostnader, till exempel resekostnader för vissa service zoner eller uppstartskostnader.</span><span class="sxs-lookup"><span data-stu-id="9a770-136">When you work with service items and service orders, you may need to register additional costs, such as travel costs to particular service zones or starting fees.</span></span> <span data-ttu-id="9a770-137">När du skapar en serviceorder kan du infoga kostnaderna och en rad med typen **kostnad** läggs till i ordern.</span><span class="sxs-lookup"><span data-stu-id="9a770-137">When you create a service order, you can insert these costs and a line with the type **Cost** will be added to the order.</span></span> <span data-ttu-id="9a770-138">Om du vill koppla kostnader till alla serviceorder kan du ställa in standardkostnaden.</span><span class="sxs-lookup"><span data-stu-id="9a770-138">Alternatively, if you want to apply the cost to all service orders, you can set up a default cost.</span></span> <span data-ttu-id="9a770-139">Till exempel om du alltid vill använda en uppstartskostnad.</span><span class="sxs-lookup"><span data-stu-id="9a770-139">For example, if you always want to apply a starting fee.</span></span>
  
### <a name="to-set-up-service-costs"></a><span data-ttu-id="9a770-140">Så här skapar du servicekostnader:</span><span class="sxs-lookup"><span data-stu-id="9a770-140">To set up service costs</span></span>
1. <span data-ttu-id="9a770-141">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Servicekostnader** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9a770-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Costs**, and then choose the related link.</span></span> 
2. <span data-ttu-id="9a770-142">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="9a770-142">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a><span data-ttu-id="9a770-143">Ange standardkostnaden för serviceorder</span><span class="sxs-lookup"><span data-stu-id="9a770-143">To specify a default cost for service orders</span></span>
1. <span data-ttu-id="9a770-144">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **serviceinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9a770-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="9a770-145">I fältet **Serviceorder uppstartskostnad**, välj lämplig servicekostnad.</span><span class="sxs-lookup"><span data-stu-id="9a770-145">In the **Service Order Starting Fee** field, choose the appropriate service cost.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a770-146">Se även</span><span class="sxs-lookup"><span data-stu-id="9a770-146">See Also</span></span>
[<span data-ttu-id="9a770-147">Ställa in servicehantering</span><span class="sxs-lookup"><span data-stu-id="9a770-147">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="9a770-148">Servicehantering</span><span class="sxs-lookup"><span data-stu-id="9a770-148">Service Management</span></span>](service-service.md)  

