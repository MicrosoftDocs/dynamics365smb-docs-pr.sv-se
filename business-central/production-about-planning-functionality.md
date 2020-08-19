---
title: Om planeringsfunktioner | Microsoft Docs
description: I planeringssystemet beaktas alla efterfråge- och tillgångsdata, resultaten nettoberäknas och förslag på balansering av tillgång för att uppfylla efterfrågan skapas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: sgroespe
ms.openlocfilehash: 2b803e52038d39375aa13dce36f81d429261f985
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577337"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="491b4-103">Om planeringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="491b4-103">About Planning Functionality</span></span>

<span data-ttu-id="491b4-104">I planeringssystemet beaktas alla efterfråge- och tillgångsdata, resultaten nettoberäknas och förslag på balansering av tillgång för att uppfylla efterfrågan skapas.</span><span class="sxs-lookup"><span data-stu-id="491b4-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="491b4-105">Mer information finns i [Designdetaljer: Leveransplanering](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="491b4-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="491b4-106">Alla de fält som nämns i det här avsnittet hittar du i beskrivningen för att förstå deras funktion.</span><span class="sxs-lookup"><span data-stu-id="491b4-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="491b4-107">Tillgång och efterfrågan</span><span class="sxs-lookup"><span data-stu-id="491b4-107">Demand and Supply</span></span>

<span data-ttu-id="491b4-108">Planering innehåller två element: tillgång och efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="491b4-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="491b4-109">Dessa två element måste balanseras för att se till att efterfrågan uppfylls i tid och så kostnadseffektivt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="491b4-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="491b4-110">Efterfrågan är den term som vanligtvis används för alla typer av bruttobehov, t.ex. försäljningsorder, serviceorder, komponentbehov från montering eller produktionsorder, utgående överföringar, avropsorder eller prognoser.</span><span class="sxs-lookup"><span data-stu-id="491b4-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="491b4-111">Utöver dessa, tillåts även en del andra typer av efterfrågan - t.ex. negativa produktions- eller inköpsorder, negativt lager och inköpsreturer.</span><span class="sxs-lookup"><span data-stu-id="491b4-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="491b4-112">Tillgång är det ord som vanligtvis används för alla typer av återanskaffning, t.ex. lager, inköpsorder, monteringsorder, produktionsorder eller ankommande överföring.</span><span class="sxs-lookup"><span data-stu-id="491b4-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="491b4-113">På motsvarande sätt kan det finnas negativa försäljnings- eller serviceorder, negativt komponentbehov eller försäljningsretur – vilka alla på ett sätt också representerar tillgång.</span><span class="sxs-lookup"><span data-stu-id="491b4-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="491b4-114">Ett annat mål med planeringssystemet är att se till att lagret inte blir onödigt stort.</span><span class="sxs-lookup"><span data-stu-id="491b4-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="491b4-115">Om det uppstår en minskad efterfrågan, får du i planeringssystemet ett förslag om att skjuta upp, minska antalet eller annullera befintliga återanskaffningsorder.</span><span class="sxs-lookup"><span data-stu-id="491b4-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="491b4-116">Planeringsberäkning</span><span class="sxs-lookup"><span data-stu-id="491b4-116">Planning Calculation</span></span>

<span data-ttu-id="491b4-117">Planeringssystemet drivs av förväntad och faktisk kundefterfrågan samt även parametrar för lagerbeställningar.</span><span class="sxs-lookup"><span data-stu-id="491b4-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="491b4-118">Om du kör planeringsberäkningen får du i programmet ett förslag på särskilda åtgärder (åtgärdsmeddelanden) som du ska vidta för eventuell återanskaffning från leverantörer, överföringar mellan distributionslager eller produktion.</span><span class="sxs-lookup"><span data-stu-id="491b4-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="491b4-119">Om det redan finns återanskaffningsorder kan de förslagna åtgärderna vara att du till exempel ska öka eller påskynda order som motsvarar förändringarna i efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="491b4-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="491b4-120">Grunden för planeringsrutinen är beräkningen av brutto till netto.</span><span class="sxs-lookup"><span data-stu-id="491b4-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="491b4-121">Nettobehoven styr släppningen av planerade order, som planeras utifrån operationsföljdsinformation (tillverkade artiklar) eller ledtid på artikelkortet (inköpta artiklar).</span><span class="sxs-lookup"><span data-stu-id="491b4-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="491b4-122">Utsläppningsantalet för planerade order baseras på planeringsberäkningen och påverkas av parametrarna som ställs in på de enskilda artikelkorten.</span><span class="sxs-lookup"><span data-stu-id="491b4-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="491b4-123">Planera med manuella överföringsorder</span><span class="sxs-lookup"><span data-stu-id="491b4-123">Planning with Manual Transfer Orders</span></span>

<span data-ttu-id="491b4-124">Som du ser i fältet **Återanskaffningssystem** på ett kort för lagerställeenhet, kan planeringssystemet konfigureras till att skapa överföringsorder som balanserar leverans och behov mellan lagerställen.</span><span class="sxs-lookup"><span data-stu-id="491b4-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="491b4-125">Förutom sådana automatiska överföringsorder kanske du ibland behöver utföra en allmän flyttning av lagerkvantiteter till en annan plats, oavsett befintligt behov.</span><span class="sxs-lookup"><span data-stu-id="491b4-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="491b4-126">För det här syftet kan du skapa en överföringsorder manuellt för det antal som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="491b4-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="491b4-127">För att vara säker på att planeringssystemet inte försöker att manipulera denna manuella överföringsorder, måste du ange fältet **Planeringsflexibilitet** på raden eller raderna till Ingen.</span><span class="sxs-lookup"><span data-stu-id="491b4-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="491b4-128">Om du å andra sidan vill att planeringssystemet ska justera överföringsorderantalet och ange fältet **Planeringsflexibilitet** till standardvärdet Obegränsad.</span><span class="sxs-lookup"><span data-stu-id="491b4-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="491b4-129">Planeringsparametrar</span><span class="sxs-lookup"><span data-stu-id="491b4-129">Planning Parameters</span></span>

<span data-ttu-id="491b4-130">Planeringsparametrarna styr när och hur återskaffningen sker och hur mycket som ska återanskaffas beroende på de olika inställningarna på artikelkortet (eller lagerställeenheten) och produktionsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="491b4-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="491b4-131">Följande planeringsparametrar finns på artikeln eller kortet för lagerställeenheten:</span><span class="sxs-lookup"><span data-stu-id="491b4-131">The following planning parameters exist on the item or SKU card:</span></span>  

- <span data-ttu-id="491b4-132">Max. utjämningsperiod</span><span class="sxs-lookup"><span data-stu-id="491b4-132">Dampener Period</span></span>  
- <span data-ttu-id="491b4-133">Max. avvikelsekvantitet</span><span class="sxs-lookup"><span data-stu-id="491b4-133">Dampener Quantity</span></span>  
- <span data-ttu-id="491b4-134">Partiformningsmetod</span><span class="sxs-lookup"><span data-stu-id="491b4-134">Reordering Policy</span></span>  
- <span data-ttu-id="491b4-135">Beställningspunkt</span><span class="sxs-lookup"><span data-stu-id="491b4-135">Reorder Point</span></span>
- <span data-ttu-id="491b4-136">Beställningsgräns</span><span class="sxs-lookup"><span data-stu-id="491b4-136">Maximum Inventory</span></span>  
- <span data-ttu-id="491b4-137">Överflödesnivå</span><span class="sxs-lookup"><span data-stu-id="491b4-137">Overflow Level</span></span>  
- <span data-ttu-id="491b4-138">Tidsenhet</span><span class="sxs-lookup"><span data-stu-id="491b4-138">Time Bucket</span></span>  
- <span data-ttu-id="491b4-139">Partiackumuleringsperiod</span><span class="sxs-lookup"><span data-stu-id="491b4-139">Lot Accumulation Period</span></span>  
- <span data-ttu-id="491b4-140">Omplaneringsperiod</span><span class="sxs-lookup"><span data-stu-id="491b4-140">Rescheduling Period</span></span>  
- <span data-ttu-id="491b4-141">Beställningsantal</span><span class="sxs-lookup"><span data-stu-id="491b4-141">Reorder Quantity</span></span>  
- <span data-ttu-id="491b4-142">Säkerhetsledtid</span><span class="sxs-lookup"><span data-stu-id="491b4-142">Safety Lead Time</span></span>  
- <span data-ttu-id="491b4-143">Säkerhetslager</span><span class="sxs-lookup"><span data-stu-id="491b4-143">Safety Stock Quantity</span></span>  
- <span data-ttu-id="491b4-144">Monteringsmetod</span><span class="sxs-lookup"><span data-stu-id="491b4-144">Assembly Policy</span></span>  
- <span data-ttu-id="491b4-145">Produktionsprincip</span><span class="sxs-lookup"><span data-stu-id="491b4-145">Manufacturing Policy</span></span>  

<span data-ttu-id="491b4-146">Följande beställningsprinciper finns på artikeln eller kortet för lagerställeenheten:</span><span class="sxs-lookup"><span data-stu-id="491b4-146">The following order modifiers exist on the item or SKU card:</span></span>  

- <span data-ttu-id="491b4-147">Min. partistorlek</span><span class="sxs-lookup"><span data-stu-id="491b4-147">Minimum Order Quantity</span></span>  
- <span data-ttu-id="491b4-148">Max. partistorlek</span><span class="sxs-lookup"><span data-stu-id="491b4-148">Maximum Order Quantity</span></span>  
- <span data-ttu-id="491b4-149">Partistorleksmultipel</span><span class="sxs-lookup"><span data-stu-id="491b4-149">Order Multiple</span></span>  

<span data-ttu-id="491b4-150">Inställningsfälten för planering på sidan **Produktionsinställningar** inkluderar:</span><span class="sxs-lookup"><span data-stu-id="491b4-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

- <span data-ttu-id="491b4-151">Dynamisk lägsta-nivå-kod</span><span class="sxs-lookup"><span data-stu-id="491b4-151">Dynamic Low-Level Code</span></span>  
- <span data-ttu-id="491b4-152">Aktuell efterfrågeprognos</span><span class="sxs-lookup"><span data-stu-id="491b4-152">Current Demand Forecast</span></span>  
- <span data-ttu-id="491b4-153">Prognos på lagerställen</span><span class="sxs-lookup"><span data-stu-id="491b4-153">Use Forecast on Locations</span></span>  
- <span data-ttu-id="491b4-154">Standard säkerhetsledtid</span><span class="sxs-lookup"><span data-stu-id="491b4-154">Default Safety Lead Time</span></span>  
- <span data-ttu-id="491b4-155">Tom överflödesnivå</span><span class="sxs-lookup"><span data-stu-id="491b4-155">Blank Overflow Level</span></span>  
- <span data-ttu-id="491b4-156">Prod.prog./nettobehov</span><span class="sxs-lookup"><span data-stu-id="491b4-156">Combined MPS/MRP Calculation</span></span>
- <span data-ttu-id="491b4-157">Komp. vid lagerställe</span><span class="sxs-lookup"><span data-stu-id="491b4-157">Components at Location</span></span>  
- <span data-ttu-id="491b4-158">Standard för max. utjämningsperiod</span><span class="sxs-lookup"><span data-stu-id="491b4-158">Default Dampener Period</span></span>  
- <span data-ttu-id="491b4-159">Max. avvikelsekvantitet</span><span class="sxs-lookup"><span data-stu-id="491b4-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="491b4-160">Mer information finns i [Designdetaljer: Planläggningsparametrar](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="491b4-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="491b4-161">Andra viktiga planeringsfält</span><span class="sxs-lookup"><span data-stu-id="491b4-161">Other Important Planning Fields</span></span>

### <a name="planning-flexibility"></a><span data-ttu-id="491b4-162">Planeringsflexibilitet</span><span class="sxs-lookup"><span data-stu-id="491b4-162">Planning Flexibility</span></span>

<span data-ttu-id="491b4-163">På de flesta leveransorder, till exempel produktionsorder, kan du välja **obegränsad** eller **ingen** i fältet **Planeringsflexibilitet** på raderna.</span><span class="sxs-lookup"><span data-stu-id="491b4-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="491b4-164">Anger om leveransen som representeras av produktionsorderraden tas i beaktande av planeringssystemet när ett åtgärdsmeddelande beräknas.</span><span class="sxs-lookup"><span data-stu-id="491b4-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="491b4-165">Om fältet innehåller alternativet **Obegränsad**, ingår raden när meddelandena beräknas.</span><span class="sxs-lookup"><span data-stu-id="491b4-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="491b4-166">Om fältet innehåller alternativet **Ingen**, är raden fast (går inte att ändra) och ingår inte när åtgärdsmeddelandena beräknas.</span><span class="sxs-lookup"><span data-stu-id="491b4-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="491b4-167">Varning</span><span class="sxs-lookup"><span data-stu-id="491b4-167">Warning</span></span>

<span data-ttu-id="491b4-168">Informationsfältet **varning** på sidan **planeringsförslag** informerar dig om att alla planeringsrader som skapats för en ovanlig situation med text där användaren kan välja att få mer information.</span><span class="sxs-lookup"><span data-stu-id="491b4-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="491b4-169">Följande typer av varningar förekommer:</span><span class="sxs-lookup"><span data-stu-id="491b4-169">The following warning types exist:</span></span>

- <span data-ttu-id="491b4-170">Nödsituation</span><span class="sxs-lookup"><span data-stu-id="491b4-170">Emergency</span></span>
- <span data-ttu-id="491b4-171">Undantag</span><span class="sxs-lookup"><span data-stu-id="491b4-171">Exception</span></span>
- <span data-ttu-id="491b4-172">Observera!</span><span class="sxs-lookup"><span data-stu-id="491b4-172">Attention</span></span>
- <span data-ttu-id="491b4-173">Nödsituation</span><span class="sxs-lookup"><span data-stu-id="491b4-173">Emergency</span></span>

<span data-ttu-id="491b4-174">Varningen för nödsituation visas i två olika situationer:</span><span class="sxs-lookup"><span data-stu-id="491b4-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="491b4-175">Lagret är negativt på startdatumet för planeringen.</span><span class="sxs-lookup"><span data-stu-id="491b4-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="491b4-176">Det finns antedaterade försörjnings- eller behovshändelser.</span><span class="sxs-lookup"><span data-stu-id="491b4-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="491b4-177">Om lagernivån för en artikel är negativ på startdatumet för planeringen föreslår planeringssystemet en nödleveransorder för det negativa antalet med leverans på startdatumet för planeringen.</span><span class="sxs-lookup"><span data-stu-id="491b4-177">If an item's inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="491b4-178">I varningstexten anges startdatumet och antalet i nödordern.</span><span class="sxs-lookup"><span data-stu-id="491b4-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="491b4-179">Eventuella dokumentrader med förfallodatum före startdatumet för planeringen konsolideras i en nödleveransorder för artikeln med leverans på startdatumet för planeringen.</span><span class="sxs-lookup"><span data-stu-id="491b4-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="491b4-180">Undantag</span><span class="sxs-lookup"><span data-stu-id="491b4-180">Exception</span></span>

<span data-ttu-id="491b4-181">Undantagsvarningen visas om det planerade disponibla lagret sjunker under nivån för säkerhetslagret.</span><span class="sxs-lookup"><span data-stu-id="491b4-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="491b4-182">Planeringssystemet föreslår en leveransorder för att uppfylla behovet på förfallodatumet.</span><span class="sxs-lookup"><span data-stu-id="491b4-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="491b4-183">I varningstexten framgår vilket antal som gäller för artikelns säkerhetslager och det datum då det understigs.</span><span class="sxs-lookup"><span data-stu-id="491b4-183">The warning text states the item's safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="491b4-184">Att bryta säkerhetslagrets nivå betraktas som ett undantag eftersom det inte bör inträffa om beställningspunkten har ställts in korrekt.</span><span class="sxs-lookup"><span data-stu-id="491b4-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="491b4-185">Tillgången på planeringsrader med undantagsvarningar ändras normalt inte enligt planeringsparametrarna.</span><span class="sxs-lookup"><span data-stu-id="491b4-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="491b4-186">I stället föreslår planeringssystemet endast en försörjning för att täcka det exakta efterfrågade antalet.</span><span class="sxs-lookup"><span data-stu-id="491b4-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="491b4-187">Du kan dock ange att planeringskörningen ska följa vissa planeringsparametrar för planeringsrader som ska kopplas till vissa varningar.</span><span class="sxs-lookup"><span data-stu-id="491b4-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="491b4-188">Mer information finns i beskrivningen av fältet **Respektera planeringsparametrar för undantagsvarningar** i artikeln [Kör hela planeringen, MPS eller MRP](production-how-to-run-mps-and-mrp.md).</span><span class="sxs-lookup"><span data-stu-id="491b4-188">For more information, see the description for the **Respect Planning Parameters for Exception Warnings** field in the [Run Full Planning, MPS or MRP](production-how-to-run-mps-and-mrp.md) article.</span></span>

### <a name="attention"></a><span data-ttu-id="491b4-189">Observera!</span><span class="sxs-lookup"><span data-stu-id="491b4-189">Attention</span></span>

<span data-ttu-id="491b4-190">Den här varningen visas i två olika situationer:</span><span class="sxs-lookup"><span data-stu-id="491b4-190">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="491b4-191">Startdatumet för planeringen ligger tidigare än arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="491b4-191">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="491b4-192">Planeringsraden föreslår att en släppt inköps- eller produktionsorder ändras.</span><span class="sxs-lookup"><span data-stu-id="491b4-192">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="491b4-193">Vid planering av rader med varningar är fältet **Acceptera åtgärdsmeddelande** inte markerat, eftersom planeraren förväntas att undersöka dessa rader innan planen utförs.</span><span class="sxs-lookup"><span data-stu-id="491b4-193">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="planning-worksheets-and-requisition-worksheets"></a><span data-ttu-id="491b4-194">Planeringsförslag och inköpskalkylark</span><span class="sxs-lookup"><span data-stu-id="491b4-194">Planning worksheets and requisition worksheets</span></span>

<span data-ttu-id="491b4-195">På det sätt som beskrivs i [Planera](production-planning.md) kan du välja mellan två kalkylblad för de flesta planeringsaktiviteter, planeringsförslaget och inköpskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="491b4-195">As described in [Planning](production-planning.md), you can choose between two worksheets for most planning activities, the planning worksheet and the requisition worksheet.</span></span> <span data-ttu-id="491b4-196">De flesta processer beskrivs utifrån planeringsförslaget, men det finns ett par scenarier där inköpskalkylarket är prioriterat.</span><span class="sxs-lookup"><span data-stu-id="491b4-196">Most processes are described based on the planning worksheet, but there are a couple of scenarios where the requisition worksheet is preferred.</span></span>

### <a name="requisition-worksheet"></a><span data-ttu-id="491b4-197">Inköpskalkylark</span><span class="sxs-lookup"><span data-stu-id="491b4-197">Requisition worksheet</span></span>

<span data-ttu-id="491b4-198">På sidan **Inköpskalkylark** visas en lista över artiklar som behöver beställas.</span><span class="sxs-lookup"><span data-stu-id="491b4-198">The **Requisition Worksheet** page lists items that you want to order.</span></span> <span data-ttu-id="491b4-199">Du kan ange artiklar i kalkylarket på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="491b4-199">You can enter items in the worksheet in the following ways:</span></span>

- <span data-ttu-id="491b4-200">Ange artiklarna manuellt i kalkylarket och fyll i aktuella fält.</span><span class="sxs-lookup"><span data-stu-id="491b4-200">Enter the items manually in the worksheet and fill in the relevant fields.</span></span>

- <span data-ttu-id="491b4-201">Använd batch-jobbet **Skapa plan**.</span><span class="sxs-lookup"><span data-stu-id="491b4-201">Use the **Calculate Plan** batch job.</span></span> <span data-ttu-id="491b4-202">Genom detta beräknas en återanskaffningsplan för artiklar och lagerställesenheter som har skapats med återanskaffningssystemet **Inköp** eller **Överföring**.</span><span class="sxs-lookup"><span data-stu-id="491b4-202">This calculates a replenishment plan for items and stockkeeping units that have been set up with a replenishment system of **Purchase** or **Transfer**.</span></span> <span data-ttu-id="491b4-203">När du använder detta batch-jobb fylls fältet **Åtgärdsmeddelande** automatiskt i med ett förslag på en åtgärd för att fylla på artikeln.</span><span class="sxs-lookup"><span data-stu-id="491b4-203">When you use this batch job, the program automatically fills in the **Action Message** field with a suggestion for an action you can take to replenish the item.</span></span> <span data-ttu-id="491b4-204">Detta kan till exempel innebära att artikelantalet i en befintlig order ökas eller att en ny order skapas.</span><span class="sxs-lookup"><span data-stu-id="491b4-204">This could be increasing the item quantity on an existing order or creating a new order, for example.</span></span>

- <span data-ttu-id="491b4-205">Om du har använt batch-jobbet **Skapa inköpsförslag** från sidan **Planeringsförslag** för att beräkna en återanskaffningsplan kan du använda batch-jobbet **Verkställ åtgärdsmeddelande** för att kopiera inköps- och överföringsorderförslag från planeringsförslaget till inköpskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="491b4-205">If you have used the **Calculate Plan** batch job from the **Planning Worksheet** page to calculate a replenishment plan, you can use the **Carry Out Action Message** batch job to copy purchase and transfer order proposals from the planning worksheet to the requisition worksheet.</span></span> <span data-ttu-id="491b4-206">Detta är praktiskt om olika användare är ansvariga för hantering av produktionsorder och inköps-/överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="491b4-206">This is practical if separate users are responsible for handling production orders and purchase/transfer orders.</span></span>

- <span data-ttu-id="491b4-207">Du kan använda åtgärden **Direktleverans** för att fylla i raderna i inköpskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="491b4-207">You can use the **Drop Shipment** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="491b4-208">För den här åtgärden används batch-jobbet **Hämta förs.order** så att du kan bestämma vilka försäljningsorderrader du vill ange för en direktleverans.</span><span class="sxs-lookup"><span data-stu-id="491b4-208">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a drop shipment.</span></span>

- <span data-ttu-id="491b4-209">Du kan använda åtgärden **Specialorder** för att fylla i raderna i inköpskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="491b4-209">You can use the **Special Order** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="491b4-210">För den här åtgärden används batch-jobbet **Hämta förs.order** så att du kan bestämma vilka försäljningsorderrader du vill ange för en specialorder.</span><span class="sxs-lookup"><span data-stu-id="491b4-210">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a special order.</span></span>

<span data-ttu-id="491b4-211">Raderna i inköpskalkylarket innehåller detaljerad information om de artiklar som måste beställas på nytt.</span><span class="sxs-lookup"><span data-stu-id="491b4-211">Requisition worksheet lines contain detailed information about the items that need to be reordered.</span></span> <span data-ttu-id="491b4-212">Du kan redigera och ta bort raderna så att återanskaffningsplanen justeras, och du kan bearbeta raderna ytterligare med hjälp av batch-jobbet **Verkställ åtgärdsmeddelande**.</span><span class="sxs-lookup"><span data-stu-id="491b4-212">You can edit and delete the lines to adjust your replenishment plan, and you can further process the lines by using the **Carry Out Action Message** batch job.</span></span>

<span data-ttu-id="491b4-213">Information om hur du planerar lagerställen och överföringar finns i [Planera med eller utan lagerställen](production-planning-with-without-locations.md).</span><span class="sxs-lookup"><span data-stu-id="491b4-213">For details about planning with locations and transfers, see [Planning With or Without Locations](production-planning-with-without-locations.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="491b4-214">Se även</span><span class="sxs-lookup"><span data-stu-id="491b4-214">See Also</span></span>

[<span data-ttu-id="491b4-215">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="491b4-215">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
[<span data-ttu-id="491b4-216">Planerad</span><span class="sxs-lookup"><span data-stu-id="491b4-216">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="491b4-217">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="491b4-217">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="491b4-218">Produktion</span><span class="sxs-lookup"><span data-stu-id="491b4-218">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="491b4-219">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="491b4-219">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="491b4-220">Inköp</span><span class="sxs-lookup"><span data-stu-id="491b4-220">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="491b4-221">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="491b4-221">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="491b4-222">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="491b4-222">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
