---
title: Designdetaljer - Balansera efterfrågan och tillgång | Microsoft Docs
description: Detta ämne introducerar begreppet etfterfrågan, som är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f808865bd4fc2113dd5c04071f7ba2e8793fe3af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185570"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="6ebfe-103">Designdetaljer: Efterfrågan vid tomt lagerställe</span><span class="sxs-lookup"><span data-stu-id="6ebfe-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="6ebfe-104">När en användare skapar en begärandehändelse, till exempel en försäljningsorderrad, låter programmet användaren ibland ange en lagerställekod och andra gånger inte, det vill säga ett tomt lagerställe.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="6ebfe-105">För efterfrågan med eller utan lagerställekod fungerar planeringssystemet på ett okomplicerat sätt när:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="6ebfe-106">Behovsraderna har alltid lagerställekoder och systemet använder lagerställeenheter helt och hållet, inklusive den relevanta lagerställekonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="6ebfe-107">Behovsraderna har aldrig lagerställekoder och systemet använder inte lagerställeenheter eller någon lagerställekonfiguration (se det sista scenariet i följande avsnitt).</span><span class="sxs-lookup"><span data-stu-id="6ebfe-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="6ebfe-108">Om behovshändelser ibland har lagerställekoder och ibland inte, kommer planeringssystemet att följa vissa regler beroende på konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="6ebfe-109">Behov vid lagerställe</span><span class="sxs-lookup"><span data-stu-id="6ebfe-109">Demand at Location</span></span>
<span data-ttu-id="6ebfe-110">När planeringssystemet identifierar behov vid ett lagerställe reagerar det på olika sätt beroende på tre viktiga konfigurationsvärden.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="6ebfe-111">När planeringen körs kontrolleras de tre konfigurationsvärdena i tur och ordning och planeringen sker därefter.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="6ebfe-112">Är fältet **Lagerställe ska finnas** markerat?</span><span class="sxs-lookup"><span data-stu-id="6ebfe-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="6ebfe-113">Om ja, då:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-113">If yes, then:</span></span>

2. <span data-ttu-id="6ebfe-114">Finns det en lagerställeenhet för artikeln?</span><span class="sxs-lookup"><span data-stu-id="6ebfe-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="6ebfe-115">Om ja, då:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-115">If yes, then:</span></span>

    <span data-ttu-id="6ebfe-116">Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="6ebfe-117">Om nej, då:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-117">If no, then:</span></span>

3. <span data-ttu-id="6ebfe-118">Innehåller fältet Komp. vid lagerställe den efterfrågade lagerställekoden?</span><span class="sxs-lookup"><span data-stu-id="6ebfe-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="6ebfe-119">Om ja, då:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-119">If yes, then:</span></span>

  <span data-ttu-id="6ebfe-120">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="6ebfe-121">Om nej, då:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-121">If no, then:</span></span>

  <span data-ttu-id="6ebfe-122">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti, Ta med lager = Ja, alla andra planeringsparametrar = Tom, artiklar som använder partiformningsmetoden = Order fortsätter att använda Order tillsammans med andra inställningar.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="6ebfe-123">Den speciella planläggningen ställde som anges som den sista reaktionen i moment till 3 ovan kallas i det följande för ”minimialternativet”.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="6ebfe-124">Denna planeringsinställningen täcker bara det exakta behovet. Alla planeringsparametrar som har definierats ignoreras.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="6ebfe-125">Se scenarioavsnittet nedan för information om varianter av den här planeringslogiken.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="6ebfe-126">Efterfrågan vid tomt lagerställe</span><span class="sxs-lookup"><span data-stu-id="6ebfe-126">Demand at Blank Location</span></span>
<span data-ttu-id="6ebfe-127">Även om fältet **Lagerställe** ska finnas har markerats tillåter programmet att rader skapas utan lagerställekod, vilken också kallas för tomt lagerställe.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="6ebfe-128">Detta är en avvikelse för systemet eftersom det har olika konfigurationsvärden som har justerats till att hantera lagerställen (se ovan) och därför kommer planeringsmotorn inte att skapa någon planeringsrad för en behovsrad.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="6ebfe-129">Om fältet **Lagerställe** ska finnas inte har valts men någon av inställningsvärdena för lagerställe finns, betraktas det också som en avvikelse och planeringssystemet kommer att reagera med genom att använda "minimialternativet": Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="6ebfe-130">Scenarierna</span><span class="sxs-lookup"><span data-stu-id="6ebfe-130">Scenarios</span></span>
<span data-ttu-id="6ebfe-131">Följande scenarier beskriver varianter av efterfrågan vid tomt lagerställe och hur planeringssystemet återgår till ”minimialternativet”.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="6ebfe-132">Konfiguration 1:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-132">Setup 1:</span></span>
<span data-ttu-id="6ebfe-133">Lagerställe ska finnas = Ja</span><span class="sxs-lookup"><span data-stu-id="6ebfe-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="6ebfe-134">Lagerställeenheten är inställd på RÖD</span><span class="sxs-lookup"><span data-stu-id="6ebfe-134">SKU is set up for RED</span></span>

<span data-ttu-id="6ebfe-135">Komponenter vid lagerställe = BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="6ebfe-136">Fall 1.1: Behov finns vid lagerställe RÖD</span><span class="sxs-lookup"><span data-stu-id="6ebfe-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="6ebfe-137">Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="6ebfe-138">Fall 1.2: Behov finns vid lagerställe BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="6ebfe-139">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="6ebfe-140">Fall 1.3: Behov finns vid lagerställe GRÖN</span><span class="sxs-lookup"><span data-stu-id="6ebfe-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="6ebfe-141">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="6ebfe-142">Fall 1.4: Behov finns vid lagerställe TOM</span><span class="sxs-lookup"><span data-stu-id="6ebfe-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="6ebfe-143">Artikeln planeras inte eftersom inget lagerställe har definierats på behovsraden.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="6ebfe-144">Konfiguration 2:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-144">Setup 2:</span></span>
<span data-ttu-id="6ebfe-145">Lagerställe ska finnas = Ja</span><span class="sxs-lookup"><span data-stu-id="6ebfe-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="6ebfe-146">Ingen lagerställeenhet finns</span><span class="sxs-lookup"><span data-stu-id="6ebfe-146">No SKU exists</span></span>

<span data-ttu-id="6ebfe-147">Komponenter vid lagerställe = BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="6ebfe-148">Fall 2.1: Behov finns vid lagerställe RÖD</span><span class="sxs-lookup"><span data-stu-id="6ebfe-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="6ebfe-149">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="6ebfe-150">Fall 2.2: Behov finns vid lagerställe BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="6ebfe-151">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="6ebfe-152">Konfiguration 3:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-152">Setup 3:</span></span>
<span data-ttu-id="6ebfe-153">Lagerställe ska finnas = Ja</span><span class="sxs-lookup"><span data-stu-id="6ebfe-153">Location Mandatory = No</span></span>

<span data-ttu-id="6ebfe-154">Ingen lagerställeenhet finns</span><span class="sxs-lookup"><span data-stu-id="6ebfe-154">No SKU exists</span></span>

<span data-ttu-id="6ebfe-155">Komponenter vid lagerställe = BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="6ebfe-156">Fall 3.1: Behov finns vid lagerställe RÖD</span><span class="sxs-lookup"><span data-stu-id="6ebfe-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="6ebfe-157">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="6ebfe-158">Fall 3.2: Behov finns vid lagerställe BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="6ebfe-159">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="6ebfe-160">Fall 3.3: Behov finns vid lagerställe TOM</span><span class="sxs-lookup"><span data-stu-id="6ebfe-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="6ebfe-161">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="6ebfe-162">Konfiguration 4:</span><span class="sxs-lookup"><span data-stu-id="6ebfe-162">Setup 4:</span></span>
<span data-ttu-id="6ebfe-163">Lagerställe ska finnas = Ja</span><span class="sxs-lookup"><span data-stu-id="6ebfe-163">Location Mandatory = No</span></span>

<span data-ttu-id="6ebfe-164">Ingen lagerställeenhet finns</span><span class="sxs-lookup"><span data-stu-id="6ebfe-164">No SKU exists</span></span>

<span data-ttu-id="6ebfe-165">Komponenter vid lagerställe = TOM</span><span class="sxs-lookup"><span data-stu-id="6ebfe-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="6ebfe-166">Fall 4.1: Behov finns vid lagerställe BLÅ</span><span class="sxs-lookup"><span data-stu-id="6ebfe-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="6ebfe-167">Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="6ebfe-168">Fall 4.2: Behov finns vid lagerställe TOM</span><span class="sxs-lookup"><span data-stu-id="6ebfe-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="6ebfe-169">Artikeln planeras enligt planeringsparametrarna på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="6ebfe-170">Som visas i det sista scenariet är det enda sättet att få ett korrekt resultat från en behovsrad utan lagerställekod att inaktivera alla konfigurationsvärden för lagerställena.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="6ebfe-171">Det enda sättet att få stabila planeringsresultat för behov vid lagerställen är att använda lagerställeenheter.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="6ebfe-172">Om du företag ofta planerar för behov vid lagerställen rekommenderas det starkt att de använder underavdelningen Lagerställeenheter.</span><span class="sxs-lookup"><span data-stu-id="6ebfe-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ebfe-173">Se även</span><span class="sxs-lookup"><span data-stu-id="6ebfe-173">See Also</span></span>  
<span data-ttu-id="6ebfe-174">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="6ebfe-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="6ebfe-175">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="6ebfe-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="6ebfe-176">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="6ebfe-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
