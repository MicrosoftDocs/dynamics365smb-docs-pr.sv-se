---
title: "Så här ställer du in resursfördelningar | Microsoft Docs"
description: "Lär dig hur systemet kan hjälpa dig tilldela någon som har de kvalifikationer som krävs för att tillhandahålla tjänster."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6dc4a059cb3bca46910a4a4be43a5940a5652c8f
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-resource-allocation"></a><span data-ttu-id="caf8c-103">Så här skapar du resursfördelningar</span><span class="sxs-lookup"><span data-stu-id="caf8c-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="caf8c-104">För att säkerställa att en serviceuppgift utförs är det viktigt att hitta en resurs som är kvalificerad att göra arbetet.</span><span class="sxs-lookup"><span data-stu-id="caf8c-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="caf8c-105">Du kan ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)] så att det är enkelt att allokera någon som har rätt kunskaper för projektet.</span><span class="sxs-lookup"><span data-stu-id="caf8c-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="caf8c-106">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kallas detta _resursfördelning_.</span><span class="sxs-lookup"><span data-stu-id="caf8c-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="caf8c-107">Du kan fördela resurser utifrån deras kunskaper, tillgänglighet, eller om de finns i samma servicezon som kunden.</span><span class="sxs-lookup"><span data-stu-id="caf8c-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="caf8c-108">Om du vill använda resursfördelning, måste du ställa in:</span><span class="sxs-lookup"><span data-stu-id="caf8c-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="caf8c-109">De kunskaper som krävs för att reparera och underhålla serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="caf8c-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="caf8c-110">Du tilldelar dem till serviceartiklar och resurser.</span><span class="sxs-lookup"><span data-stu-id="caf8c-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="caf8c-111">Geografiska områden, kallade zoner som anges för din marknad.</span><span class="sxs-lookup"><span data-stu-id="caf8c-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="caf8c-112">Det kan t.ex. vara öst, väst, mittregion o.s.v.</span><span class="sxs-lookup"><span data-stu-id="caf8c-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="caf8c-113">Du tilldelar dessa till kunder och resurser.</span><span class="sxs-lookup"><span data-stu-id="caf8c-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="caf8c-114">Om du vill visa resursernas kunskaper och zoner och om du vill visa en varning om någon väljer icke-kvalificerade resurser eller resurser som inte finns i kundzonen.</span><span class="sxs-lookup"><span data-stu-id="caf8c-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="caf8c-115">Så här ställer du in kvalifikationer</span><span class="sxs-lookup"><span data-stu-id="caf8c-115">To set up skills</span></span>
1. <span data-ttu-id="caf8c-116">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **kvalifikationer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="caf8c-117">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="caf8c-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="caf8c-118">Du tilldelar kvalifikationer till serviceartiklar och resurser.</span><span class="sxs-lookup"><span data-stu-id="caf8c-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="caf8c-119">Välj den ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") ikon, ange **Serviceartiklar** eller **Resurser**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="caf8c-120">Öppna kortet för den serviceartikel eller resurs och välj något av följande:</span><span class="sxs-lookup"><span data-stu-id="caf8c-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="caf8c-121">För serviceartiklar, välj **Resurskvalifikationer**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="caf8c-122">För resurser, välj **kvalifikationer**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="caf8c-123">Så här skapar du zoner:</span><span class="sxs-lookup"><span data-stu-id="caf8c-123">To set up zones</span></span>
1. <span data-ttu-id="caf8c-124">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **kvalifikationer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="caf8c-125">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="caf8c-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="caf8c-126">Så här tilldelar du zoner till kunder och resurser</span><span class="sxs-lookup"><span data-stu-id="caf8c-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="caf8c-127">Välj den ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") ikon, ange **Kunder** eller **Resurser**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="caf8c-128">Öppna kortet för den serviceartikel eller resurs och välj något av följande:</span><span class="sxs-lookup"><span data-stu-id="caf8c-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="caf8c-129">För kunder, väljer du en zon i fältet **Servicezonskod**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="caf8c-130">För resurser, väljer du åtgärden **servicezoner**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="caf8c-131">Om du vill ange vad som ska visas när en resurs har valts</span><span class="sxs-lookup"><span data-stu-id="caf8c-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="caf8c-132">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **serviceinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="caf8c-133">I fältet **Resurskvalifikationsförbr**, välj ett av alternativen som beskrivs i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="caf8c-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="caf8c-134">**Alternativ**</span><span class="sxs-lookup"><span data-stu-id="caf8c-134">**Option**</span></span>|<span data-ttu-id="caf8c-135">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="caf8c-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="caf8c-136">Visad kod</span><span class="sxs-lookup"><span data-stu-id="caf8c-136">Code Shown</span></span> | <span data-ttu-id="caf8c-137">Visar endast koden.</span><span class="sxs-lookup"><span data-stu-id="caf8c-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="caf8c-138">Visad varning</span><span class="sxs-lookup"><span data-stu-id="caf8c-138">Warning Displayed</span></span> | <span data-ttu-id="caf8c-139">Informationen visas och en varning visas om du väljer en resurs som inte är kvalificerade.</span><span class="sxs-lookup"><span data-stu-id="caf8c-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="caf8c-140">Inte använd</span><span class="sxs-lookup"><span data-stu-id="caf8c-140">Not Used</span></span> | <span data-ttu-id="caf8c-141">Den här informationen visas inte.</span><span class="sxs-lookup"><span data-stu-id="caf8c-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="caf8c-142">Så här uppdaterar du resurskapacitet:</span><span class="sxs-lookup"><span data-stu-id="caf8c-142">To update resource capacity</span></span>  
<span data-ttu-id="caf8c-143">Du kan behöva ändra kapaciteten för resurser.</span><span class="sxs-lookup"><span data-stu-id="caf8c-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="caf8c-144">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **resurskapacitet**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="caf8c-145">Välj resursen och välj sedan åtgärd **Ange kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="caf8c-146">Gör önskade ändringar och klicka på **uppdatera kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="caf8c-147">Uppdatera kunskaper för artiklar, serviceartiklar eller serviceartikelgrupper</span><span class="sxs-lookup"><span data-stu-id="caf8c-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="caf8c-148">Om du vill ändra de kvalifikationskoder som har tilldelats till artiklar, till exempel från **PC** till **PCS**, gör du det för en artikel, serviceartikel eller för alla artiklar i en serviceartikelgrupp.</span><span class="sxs-lookup"><span data-stu-id="caf8c-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="caf8c-149">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artiklar**, **Serviceartikel**, eller **Serviceartikelgrupp** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="caf8c-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="caf8c-150">Välj enheten som ska uppdateras och välj sedan åtgärd **Resurskvalifikationer**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="caf8c-151">På den rad där den kod som ska ändras finns, väljer du önskad kvalifikationskod i fältet **Kvalifikationskod**.</span><span class="sxs-lookup"><span data-stu-id="caf8c-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="caf8c-152">Om artikeln har associerade serviceartiklar öppnas en dialogruta med två alternativ:</span><span class="sxs-lookup"><span data-stu-id="caf8c-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="caf8c-153">Ändra kvalifikationskoderna till det valda värdet: Välj det här alternativet om du vill ersätta den gamla kvalifikationskoden med den nya för alla relaterade serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="caf8c-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="caf8c-154">Ta bort kvalifikationskoderna eller uppdatera relationen: Välj det här alternativet om du vill ändra endast den här artikelns kvalifikationskod.</span><span class="sxs-lookup"><span data-stu-id="caf8c-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="caf8c-155">Kvalifikationskoden för de relaterade serviceartiklarna kommer att omfördelas, vilket innebär att fältet **Tilldelad från** kommer att uppdateras.</span><span class="sxs-lookup"><span data-stu-id="caf8c-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="caf8c-156">Se även</span><span class="sxs-lookup"><span data-stu-id="caf8c-156">See Also</span></span>
[<span data-ttu-id="caf8c-157">Så här tilldelar du resurser</span><span class="sxs-lookup"><span data-stu-id="caf8c-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="caf8c-158">Ställa in arbetstimmar och tjänstetider</span><span class="sxs-lookup"><span data-stu-id="caf8c-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="caf8c-159">Konfigurera felrapportering</span><span class="sxs-lookup"><span data-stu-id="caf8c-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="caf8c-160">Skapa koder för standardtjänst</span><span class="sxs-lookup"><span data-stu-id="caf8c-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 

