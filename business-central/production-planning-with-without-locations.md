---
title: Planera med och utan lagerställen | Microsoft Docs
description: Det är viktigt att förstå att planera med eller utan lagerställekoder på behovsrader.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2d9afd30c3b81912797ad95871256207d135b673
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783988"
---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="bb1ad-103">Planera med och utan lagerställen.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-103">Planning With or Without Locations</span></span>
<span data-ttu-id="bb1ad-104">Vid planering med eller utan lagerställekod på behovsrader, fungerar planeringssystemet på ett okomplicerat sätt när:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="bb1ad-105">behovsraderna alltid har lagerställekoder och systemet helt och hållet använder lagerställeenheter, inklusive den relevanta lagerställekonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="bb1ad-106">behovsraderna aldrig har lagerställekoder och systemet inte använder lagerställeenheter eller någon lagerställekonfiguration (se det sista scenariet nedan).</span><span class="sxs-lookup"><span data-stu-id="bb1ad-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="bb1ad-107">Om behovsraderna ibland har lagerställekoder och ibland inte, kommer planeringssystemet att följa vissa regler beroende på konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="bb1ad-108">Behov vid lagerställe</span><span class="sxs-lookup"><span data-stu-id="bb1ad-108">Demand at Location</span></span>  
<span data-ttu-id="bb1ad-109">När planeringssystemet identifierar behov vid ett lagerställe (en rad med en lagerställekod) reagerar det på olika sätt beroende på tre viktiga konfigurationsvärden.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="bb1ad-110">När planeringen körs kontrolleras de tre konfigurationsvärdena i tur och ordning och planeringen sker därefter:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="bb1ad-111">Är fältet **Lagerställe ska finnas** markerat?</span><span class="sxs-lookup"><span data-stu-id="bb1ad-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="bb1ad-112">Om ja, då:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-112">If yes, then:</span></span>  

2.  <span data-ttu-id="bb1ad-113">Finns det en lagerställeenhet för artikeln?</span><span class="sxs-lookup"><span data-stu-id="bb1ad-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="bb1ad-114">Om ja, då:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-114">If yes, then:</span></span>  

    <span data-ttu-id="bb1ad-115">Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="bb1ad-116">Om nej, då:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-116">If no, then:</span></span>  

3.  <span data-ttu-id="bb1ad-117">Innehåller fältet **Komp. vid lagerställe** den efterfrågade lagerställekoden?</span><span class="sxs-lookup"><span data-stu-id="bb1ad-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="bb1ad-118">Om ja, då:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-118">If yes, then:</span></span>  

    <span data-ttu-id="bb1ad-119">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="bb1ad-120">Om nej, då:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-120">If no, then:</span></span>  

    <span data-ttu-id="bb1ad-121">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti*, Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="bb1ad-122">(De artiklar som använder partiformningsmetoden  *Order* fortsätter att använda  *Order* samt andra inställningar.)</span><span class="sxs-lookup"><span data-stu-id="bb1ad-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bb1ad-123">Detta minimialternativ täcker bara det exakta behovet.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="bb1ad-124">Alla planeringsparametrar som har definierats ignoreras.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="bb1ad-125">Se variationerna i scenarierna nedan.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="bb1ad-126">Behov vid tomt lagerställe</span><span class="sxs-lookup"><span data-stu-id="bb1ad-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="bb1ad-127">Även om kryssrutan **Lagerställe** är markerat, tillåter systemet att rader skapas utan lagerställekod – vilka också kallas för *TOM*.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="bb1ad-128">Detta är en avvikelse för systemet eftersom det har olika konfigurationsvärden som har justerats till att hantera lagerställen (se ovan) och därför kommer planeringsmotorn inte att skapa någon planeringsrad för en behovsrad.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="bb1ad-129">Om fältet **Lagerställe ska finnas** inte är markerat men om något av de andra konfigurationsvärdena för lagerstället har angetts, betraktas även detta som en avvikelse och planeringssystemet reagerar genom att skicka ut "minimialternativet":</span><span class="sxs-lookup"><span data-stu-id="bb1ad-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="bb1ad-130">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir *Order)*, Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="bb1ad-131">Se variationerna i inställningsscenarierna nedan.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="bb1ad-132">Konfiguration 1:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-132">Setup 1:</span></span>  

-   <span data-ttu-id="bb1ad-133">Lagerställe ska finnas = *Ja*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="bb1ad-134">Lagerställeenheten är inställd på  *RÖD*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="bb1ad-135">Komp. vid lagerställe =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="bb1ad-136">Fall 1.1: Behov finns vid lagerställe *RÖD*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="bb1ad-137">Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten (inklusive möjlig överföring).</span><span class="sxs-lookup"><span data-stu-id="bb1ad-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="bb1ad-138">Fall 1.2: Behov finns vid lagerställe *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="bb1ad-139">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="bb1ad-140">Fall 1.3: Behov finns vid lagerställe  *GRÖN*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="bb1ad-141">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="bb1ad-142">Fall 1.4: Behov finns vid lagerställe *TOM*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="bb1ad-143">Artikeln planeras inte eftersom inget lagerställe har definierats på behovsraden.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="bb1ad-144">Konfiguration 2:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-144">Setup 2:</span></span>  

-   <span data-ttu-id="bb1ad-145">Lagerställe ska finnas = *Ja*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="bb1ad-146">Ingen lagerställeenhet finns</span><span class="sxs-lookup"><span data-stu-id="bb1ad-146">No SKU exists</span></span>  
-   <span data-ttu-id="bb1ad-147">Komp. vid lagerställe =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="bb1ad-148">Fall 2.1: Behov finns vid lagerställe  *RÖD*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="bb1ad-149">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="bb1ad-150">Fall 2.2: Behov finns vid lagerställe *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="bb1ad-151">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="bb1ad-152">Konfiguration 3:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-152">Setup 3:</span></span>  

-   <span data-ttu-id="bb1ad-153">Lagerställe ska finnas = *Ja*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="bb1ad-154">Ingen lagerställeenhet finns</span><span class="sxs-lookup"><span data-stu-id="bb1ad-154">No SKU exists</span></span>  
-   <span data-ttu-id="bb1ad-155">Komp. vid lagerställe =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="bb1ad-156">Fall 3.1: Behov finns vid lagerställe  *RÖD*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="bb1ad-157">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="bb1ad-158">Fall 3.2: Behov finns vid lagerställe *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="bb1ad-159">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="bb1ad-160">Fall 3.3: Behov finns vid lagerställe  *TOM*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="bb1ad-161">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="bb1ad-162">Konfiguration 4:</span><span class="sxs-lookup"><span data-stu-id="bb1ad-162">Setup 4:</span></span>  

-   <span data-ttu-id="bb1ad-163">Lagerställe ska finnas = *Ja*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="bb1ad-164">Ingen lagerställeenhet finns</span><span class="sxs-lookup"><span data-stu-id="bb1ad-164">No SKU exists</span></span>  
-   <span data-ttu-id="bb1ad-165">Komp. vid lagerställe =  *TOM*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="bb1ad-166">Fall 4.1: Behov finns vid lagerställe  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="bb1ad-167">Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="bb1ad-168">Fall 4.2: Behov finns vid lagerställe  *TOM*</span><span class="sxs-lookup"><span data-stu-id="bb1ad-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="bb1ad-169">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="bb1ad-170">Som du ser i det sista scenariet, går det bara att korrigera resultat från en behovsrad utan lagerställekod genom att inaktivera alla konfigurationsvärden för lagerställena.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="bb1ad-171">Det enda sättet att få stabila planeringsresultat för behov vid lagerställen är att använda lagerställeenheter.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="bb1ad-172">Om du ofta planerar för behov vid lagerställen rekommenderas det starkt att du använder funktionen Lagerställeenheter.</span><span class="sxs-lookup"><span data-stu-id="bb1ad-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb1ad-173">Se även</span><span class="sxs-lookup"><span data-stu-id="bb1ad-173">See Also</span></span>
<span data-ttu-id="bb1ad-174">[Planerad](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="bb1ad-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="bb1ad-175">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="bb1ad-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="bb1ad-176">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="bb1ad-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="bb1ad-177">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="bb1ad-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="bb1ad-178">Inköp</span><span class="sxs-lookup"><span data-stu-id="bb1ad-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bb1ad-179">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="bb1ad-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="bb1ad-180">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="bb1ad-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="bb1ad-181">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bb1ad-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
