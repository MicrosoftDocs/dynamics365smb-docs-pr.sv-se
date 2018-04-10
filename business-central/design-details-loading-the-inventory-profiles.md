---
title: "Designdetaljer - Läsa in lagerprofilerna | Microsoft Docs"
description: "För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler."
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
ms.openlocfilehash: 5b47a898b7e1d574abaf521e917f780fd105c4a8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-loading-the-inventory-profiles"></a><span data-ttu-id="614b4-103">Designdetaljer: Läsa in lagerprofilerna</span><span class="sxs-lookup"><span data-stu-id="614b4-103">Design Details: Loading the Inventory Profiles</span></span>
<span data-ttu-id="614b4-104">För att sortera ut de många källorna till efterfrågan och tillgång ordnar planeringssystemet dem på två tidslinjer som kallas lagerprofiler.</span><span class="sxs-lookup"><span data-stu-id="614b4-104">To sort out the many sources of demand and supply, the planning system organizes them on two timelines called inventory profiles.</span></span>  

 <span data-ttu-id="614b4-105">De normala typerna av efterfrågan och tillgång med förfallodatum på eller efter planeringsstartdatumet laddas i varje lagerprofil.</span><span class="sxs-lookup"><span data-stu-id="614b4-105">The normal types of demand and supply with due dates on or after the planning starting date are loaded into each inventory profile.</span></span> <span data-ttu-id="614b4-106">När de laddas sorteras de olika efterfrågan- och tillgångstyperna enligt allmänna prioriteringar, till exempel förfallodatum, lågnivåkoder, lagerställe och variant.</span><span class="sxs-lookup"><span data-stu-id="614b4-106">When loaded, the different demand and supply types are sorted according to overall priorities, such as due date, low-level codes, location, and variant.</span></span> <span data-ttu-id="614b4-107">Dessutom kopplas orderprioriteter till de olika typerna för att se till att den viktigaste efterfrågan uppfylls först.</span><span class="sxs-lookup"><span data-stu-id="614b4-107">In addition, order priorities are applied to the different types to ensure that the most important demand is fulfilled first.</span></span> <span data-ttu-id="614b4-108">Mer information finns i [Designdetaljer: prioritera order](design-details-prioritizing-orders.md)</span><span class="sxs-lookup"><span data-stu-id="614b4-108">For more information, see [Design Details: Prioritizing Orders](design-details-prioritizing-orders.md).</span></span>  

 <span data-ttu-id="614b4-109">Som nämndes tidigare kan efterfrågan kan även vara negativ.</span><span class="sxs-lookup"><span data-stu-id="614b4-109">As previously mentioned, demand could also be negative.</span></span> <span data-ttu-id="614b4-110">Det betyder att den ska hanteras som tillgång, men till skillnad från de vanliga typerna av tillgång anses negativ efterfrågan vara fast tillgång.</span><span class="sxs-lookup"><span data-stu-id="614b4-110">This means that it should be treated as supply; however, unlike the normal types of supply, negative demand is considered fixed supply.</span></span> <span data-ttu-id="614b4-111">Planeringssystemet tar hänsyn till det, men föreslår inga ändringar.</span><span class="sxs-lookup"><span data-stu-id="614b4-111">The planning system can take it into account, but will not suggest any changes to it.</span></span>  

 <span data-ttu-id="614b4-112">I allmänhet betraktar planeringssystemet alla leveransorder efter planeringsstartdatumet som möjliga att ändra för att uppfylla behov.</span><span class="sxs-lookup"><span data-stu-id="614b4-112">In general, the planning system considers all supply orders after the planning starting date as subject to change in order to fulfill demand.</span></span> <span data-ttu-id="614b4-113">Men så snart ett antal bokförs från en leveransorder kan den inte längre ändras av planeringssystemet.</span><span class="sxs-lookup"><span data-stu-id="614b4-113">However, as soon as a quantity is posted from a supply order, it can no longer be changed by the planning system.</span></span> <span data-ttu-id="614b4-114">Följande olika order kan inte planeras om:</span><span class="sxs-lookup"><span data-stu-id="614b4-114">Accordingly, the following different orders cannot be replanned:</span></span>  

-   <span data-ttu-id="614b4-115">Släppta produktionsorder där förbrukning eller utflöde har bokförts.</span><span class="sxs-lookup"><span data-stu-id="614b4-115">Released production orders where consumption or output has been posted.</span></span>  

-   <span data-ttu-id="614b4-116">Monteringsorder där förbrukning eller utflöde har bokförts.</span><span class="sxs-lookup"><span data-stu-id="614b4-116">Assembly orders where consumption or output has been posted.</span></span>  

-   <span data-ttu-id="614b4-117">Överföring order där utleveransen har bokförts.</span><span class="sxs-lookup"><span data-stu-id="614b4-117">Transfer orders where shipment has been posted.</span></span>  

-   <span data-ttu-id="614b4-118">Inköpsorder där inleverans har bokförts.</span><span class="sxs-lookup"><span data-stu-id="614b4-118">Purchase orders where receipt has been posted.</span></span>  

 <span data-ttu-id="614b4-119">Förutom att ladda tillgångs- och efterfråganstyper, laddas vissa typer med hänsyn till speciella regler och beroenden som beskrivs i här efter.</span><span class="sxs-lookup"><span data-stu-id="614b4-119">Apart from loading demand and supply types, certain types are loaded with attention to special rules and dependencies that are described in the following.</span></span>  

## <a name="item-dimensions-are-separated"></a><span data-ttu-id="614b4-120">Artikeldimensioner är separerade</span><span class="sxs-lookup"><span data-stu-id="614b4-120">Item Dimensions are Separated</span></span>  
 <span data-ttu-id="614b4-121">Leveransplanen måste beräknas per kombination av artikeldimensioner, till exempel variant och lagerställe.</span><span class="sxs-lookup"><span data-stu-id="614b4-121">The supply plan must be calculated per combination of the item dimensions, such as variant and location.</span></span> <span data-ttu-id="614b4-122">Men det finns ingen anledning att beräkna någon teoretisk kombination.</span><span class="sxs-lookup"><span data-stu-id="614b4-122">However, there is no reason to calculate any theoretical combination.</span></span> <span data-ttu-id="614b4-123">Endast de kombinationer med ett efterfrågans- och/eller tillgångsbehov måste beräknas.</span><span class="sxs-lookup"><span data-stu-id="614b4-123">Only those combinations that carry a demand and/or supply need to be calculated.</span></span>  

 <span data-ttu-id="614b4-124">Planeringssystemet styr detta genom att gå igenom lagerprofilen.</span><span class="sxs-lookup"><span data-stu-id="614b4-124">The planning system controls this by running through the inventory profile.</span></span> <span data-ttu-id="614b4-125">När en ny kombination hittas, skapas en internkontrollpost som innehåller den faktiska informationen om kombinationen.</span><span class="sxs-lookup"><span data-stu-id="614b4-125">When a new combination is found, the program creates an internal control record that holds the actual combination information.</span></span> <span data-ttu-id="614b4-126">Programmet infogar lagerställeenheten som kontrollposten eller yttre loop.</span><span class="sxs-lookup"><span data-stu-id="614b4-126">The program inserts the SKU as the control record, or outer loop.</span></span> <span data-ttu-id="614b4-127">Det medför att rätt planeringsparametrar anges enligt en kombination av variant och lagerställe, och programmet kan fortsätta till den interna loopen.</span><span class="sxs-lookup"><span data-stu-id="614b4-127">As a result, the proper planning parameters according to a combination of variant and location are set, and the program can proceed to the inner loop.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="614b4-128">Programmet kräver inte att användaren ska ange en lagerställeenhetspost när du anger efterfrågan och/eller tillgång för en viss kombination av variant och lagerställe.</span><span class="sxs-lookup"><span data-stu-id="614b4-128">The program does not require the user to enter a SKU record when entering demand and/or supply for a particular combination of variant and location.</span></span> <span data-ttu-id="614b4-129">Om en lagerställeenhet inte finns för en viss kombination skapar programmet därför sin egna tillfälliga lagerställeenhetspost som baseras på artikelkortdata.</span><span class="sxs-lookup"><span data-stu-id="614b4-129">Therefore, if a SKU does not exist for a given combination, the program creates its own temporary SKU record based on the item card data.</span></span> <span data-ttu-id="614b4-130">Om Lagerställe ska finnas har värdet Ja i fönstret Lagerinställningar måste antingen lagerställeenhet skapas eller Komponenter vid lagerställe anges till Ja.</span><span class="sxs-lookup"><span data-stu-id="614b4-130">If Location Mandatory is set to Yes in the Inventory Setup window, then either a SKU must be created or Components at Location must be set to Yes.</span></span> <span data-ttu-id="614b4-131">Mer information finns i [Designdetaljer: Efterfrågan vid tomt lagerställe](design-details-demand-at-blank-location.md).</span><span class="sxs-lookup"><span data-stu-id="614b4-131">For more information, see [Design Details: Demand at Blank Location](design-details-demand-at-blank-location.md).</span></span>  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a><span data-ttu-id="614b4-132">Serie-/partinummer läses in efter specifikationsnivå</span><span class="sxs-lookup"><span data-stu-id="614b4-132">Serial/Lot Numbers are Loaded by Specification Level</span></span>  
 <span data-ttu-id="614b4-133">Attribut i form av serie-/partinummer laddas in i lagerprofilerna tillsammans med efterfrågan och tillgång som de har kopplats till.</span><span class="sxs-lookup"><span data-stu-id="614b4-133">Attributes in the form of serial/lot numbers are loaded into the inventory profiles along with the demand and supply that they are assigned to.</span></span>  

 <span data-ttu-id="614b4-134">Tillgångs- och efterfrågansattribut ordnas i prioritetsordning samt efter specifikationsnivå.</span><span class="sxs-lookup"><span data-stu-id="614b4-134">Demand and supply attributes are arranged by order priority as well as by their level of specification.</span></span> <span data-ttu-id="614b4-135">Eftersom serie-/partinummermatchningar visar nivån av specifikation söker den mer specifika efterfrågan, till exempel ett partinummer som specifikt har valts för en försäljningsrad, efter en matchning före en mindre specifik efterfrågan, till exempel en försäljning från ett valfritt utvalt partinummer.</span><span class="sxs-lookup"><span data-stu-id="614b4-135">Because serial/lot number matches reflect the level of specification, the more specific demand, such as a lot number selected specifically for a sale line, will seek a match before less specific demand, such as a sale from any lot number selected.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="614b4-136">Det finns inga tilldelade prioriteringregler för serie-/partinumrerad tillgång och efterfrågan, annat än nivån av specifikation som definieras av deras kombinationer av serie- och partinummer och artikelspårningsinställningen för de inblandade artiklarna.</span><span class="sxs-lookup"><span data-stu-id="614b4-136">There are no dedicated prioritization rules for serial/lot-numbered demand and supply, other than the level of specification defined by their combinations of serial and lot numbers and the item tracking setup of the involved items.</span></span>  

 <span data-ttu-id="614b4-137">Under balanseringen ser planeringssystemet tillgång med serie-/partinummer som oböjligt och försöker inte öka eller ändra tidpunkten för sådana leveransorder (såvida de inte används i samband en relation på orderbasis).</span><span class="sxs-lookup"><span data-stu-id="614b4-137">During balancing, the planning system regards supply that carries serial/lot numbers as inflexible and will not try to increase or reschedule such supply orders (unless they are used in an order-to-order relation).</span></span> <span data-ttu-id="614b4-138">Se Order-till-order-länkar bryts aldrig).</span><span class="sxs-lookup"><span data-stu-id="614b4-138">See Order-to-Order Links are Never Broken).</span></span> <span data-ttu-id="614b4-139">Det skyddar tillgången från att ta emot flera, eventuellt motsägande, åtgärdsmeddelanden när en leverans har varierande attribut, till exempel en samling med av olika serienummer.</span><span class="sxs-lookup"><span data-stu-id="614b4-139">This protects the supply from receiving several, possibly conflicting, action messages when a supply carries varying attributes—such as a collection of different serial numbers.</span></span>  

 <span data-ttu-id="614b4-140">En annan anledning till att serie-/partinumrerad tillgång är inflexibel är att serie-/partinummer vanligtvis tilldelas så sent i processen att det skulle vara förvirrande om ändringar föreslås.</span><span class="sxs-lookup"><span data-stu-id="614b4-140">Another reason that serial/lot numbered supply is inflexible is that serial/lot numbers are generally assigned so late in the process that it would be confusing if changes are suggested.</span></span>  

 <span data-ttu-id="614b4-141">Motkonteringen av serienummer/partinummer respekterar inte [Fryst zon](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="614b4-141">The balancing of serial/lot numbers does not respect the [Frozen Zone](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span> <span data-ttu-id="614b4-142">Om att efterfrågan och tillgång är inte är synkroniserade föreslår planeringssystemet ändringar eller förslår nya order oberoende av startdatumet för planeringen.</span><span class="sxs-lookup"><span data-stu-id="614b4-142">If demand and supply is not synchronized, the planning system will suggest changes or suggest new orders, regardless of the planning starting date.</span></span>  

## <a name="order-to-order-links-are-never-broken"></a><span data-ttu-id="614b4-143">Order-till-order-länkar bryts aldrig</span><span class="sxs-lookup"><span data-stu-id="614b4-143">Order-to-Order Links are Never Broken</span></span>  
 <span data-ttu-id="614b4-144">När du planerar en order-till-order-artikel får den länkade tillgången inte användas för någon annan efterfrågan än vad den ursprungligen ämnades för.</span><span class="sxs-lookup"><span data-stu-id="614b4-144">When planning an order-to-order item, the linked supply must not be used for any demand other than what it was originally intended for.</span></span> <span data-ttu-id="614b4-145">Den länkade efterfrågan ska inte täckas av någon annan slumpmässig leverans, även om den för närvarande är tillgänglig vad gäller tid och antal.</span><span class="sxs-lookup"><span data-stu-id="614b4-145">The linked demand should not be covered by any other random supply, even if, in its present situation, it is available in time and quantity.</span></span> <span data-ttu-id="614b4-146">Exempelvis kan en monteringsorder som är kopplad till en försäljningsorder i ett scenario för montering mot kundorder inte användas för täcka annan efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-146">For example, an assembly order that is linked to a sales order in an assemble-to-order scenario cannot be used to cover other demand.</span></span>  

 <span data-ttu-id="614b4-147">Order-till-order-efterfrågan och -tillgång måste balanseras korrekt.</span><span class="sxs-lookup"><span data-stu-id="614b4-147">Order-to-order demand and supply must balance precisely.</span></span> <span data-ttu-id="614b4-148">Planeringssystemet säkerställer tillgången under alla omständigheter, utan att överväga storleksparametrar för ordern, modifierare och antal i lager (annat än antal som är knutna till länkade order).</span><span class="sxs-lookup"><span data-stu-id="614b4-148">The planning system will ensure the supply under all circumstances without regarding order sizing parameters, modifiers, and quantities in inventory (other than quantities relating to the linked orders).</span></span> <span data-ttu-id="614b4-149">Av samma anledning föreslår systemet en minskning överskjutande tillgångar om den länkade efterfrågan minskas.</span><span class="sxs-lookup"><span data-stu-id="614b4-149">For the same reason, the system will suggest decreasing excess supplies if the linked demand is decreased.</span></span>  

 <span data-ttu-id="614b4-150">Denna motkontering påverkar också tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="614b4-150">This balancing also affects the timing.</span></span> <span data-ttu-id="614b4-151">Den begränsade horisonten som anges som tidsenheten beaktas inte; tillgången omplaneras om tidsplaneringen för efterfrågan har ändrats.</span><span class="sxs-lookup"><span data-stu-id="614b4-151">The limited horizon that is given by the time bucket is not regarded; the supply will be rescheduled if the timing of the demand has changed.</span></span> <span data-ttu-id="614b4-152">Emellertid respekteras dämpartiden och förhindrar tillgång på orderbasis från att schemaläggas, förutom den interna tillgången i en flernivå-produktionsorder (projektorder).</span><span class="sxs-lookup"><span data-stu-id="614b4-152">However, dampener time will be respected and will prevent order-to-order supplies from being scheduled out, except for the internal supplies of a multi-level production order (project order).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="614b4-153">Serie-/partinummer kan också anges på order-till-order-efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-153">Serial/lot numbers can also be specified on order-to-order demand.</span></span> <span data-ttu-id="614b4-154">I så fall betraktas inte tillgången som inflexibel som standard, vilket vanligtvis är fallet för serienummer eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="614b4-154">In that case, the supply is not regarded inflexible by default, as is normally the case for serial/lot numbers.</span></span> <span data-ttu-id="614b4-155">I det här fallet ökar/minskar systemet enligt ändringarna i efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-155">In this case, the system will increase/decrease according to changes in demand.</span></span> <span data-ttu-id="614b4-156">Dessutom är det så att om en efterfrågan har varierande serie-/partinummer, till exempel mer än ett partinummer, föreslås en leveransorder per parti.</span><span class="sxs-lookup"><span data-stu-id="614b4-156">Furthermore, if one demand carries varying serial/lot numbers, such as more than one lot number, one supply order will be suggested per lot.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="614b4-157">Prognoser ska inte leda till att skapa leveransorder som är bundna av en order-till-order-länk.</span><span class="sxs-lookup"><span data-stu-id="614b4-157">Forecasts should not lead to creating supply orders that are bound by an order-to-order link.</span></span> <span data-ttu-id="614b4-158">Om prognosen används den bör endast användas som för att skapa av härledd efterfrågan i en produktionsmiljö.</span><span class="sxs-lookup"><span data-stu-id="614b4-158">If the forecast is used, it should only be used as a generator of dependent demand in a manufacturing environment.</span></span>  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a><span data-ttu-id="614b4-159">Komponentbehov läses in enligt produktionsorderändringar</span><span class="sxs-lookup"><span data-stu-id="614b4-159">Component Need is Loaded according to Production Order Changes</span></span>  
 <span data-ttu-id="614b4-160">När du arbetar med produktionsorder måste planeringssystemet övervaka de nödvändiga komponenterna innan du laddar dem i begäranprofilen.</span><span class="sxs-lookup"><span data-stu-id="614b4-160">When handling production orders, the planning system must monitor the needed components before loading them into the demand profile.</span></span> <span data-ttu-id="614b4-161">Komponentrader som skapas från en ändrad produktionsorder ersätter de från den ursprungliga beställningen.</span><span class="sxs-lookup"><span data-stu-id="614b4-161">Component lines that result from an amended production order will replace those of the original order.</span></span> <span data-ttu-id="614b4-162">Detta säkerställer att planeringssystemet etablerar att planeringsrader för komponentbehov aldrig kopieras.</span><span class="sxs-lookup"><span data-stu-id="614b4-162">This ensures that the planning system establishes that planning lines for component need are never duplicated.</span></span>  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> <span data-ttu-id="614b4-163">Säkerhetslager kan förbrukas</span><span class="sxs-lookup"><span data-stu-id="614b4-163">Safety Stock May Be Consumed</span></span>  
 <span data-ttu-id="614b4-164">Antalet i säkerhetslager är primärt en efterfråganstyp och laddas därför i lagerprofilen på planeringsstartdatumet.</span><span class="sxs-lookup"><span data-stu-id="614b4-164">The safety stock quantity is primarily a demand type and is therefore loaded into the inventory profile on the planning starting date.</span></span>  

 <span data-ttu-id="614b4-165">Säkerhetslager är en lagerkvantitet som läggs undan för att kompensera för osäkerheter i efterfrågan under påfyllningledtiden.</span><span class="sxs-lookup"><span data-stu-id="614b4-165">Safety stock is an inventory quantity set aside to compensate for uncertainties in demand during the replenishment lead time.</span></span> <span data-ttu-id="614b4-166">Den kan förbrukas om det är nödvändigt att ta från den för att uppfylla en efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-166">However, it may be consumed if it is necessary to take from it to fulfill a demand.</span></span> <span data-ttu-id="614b4-167">När detta sker kommer planeringssystemet att se till att säkerhetslagret snabbt ersätts genom att föreslå en leveransgsorder för att fylla på säkerhetslagret.</span><span class="sxs-lookup"><span data-stu-id="614b4-167">In that case, the planning system will ensure that the safety stock is quickly replaced by suggesting a supply order to replenish the safety stock quantity on the date it is consumed.</span></span> <span data-ttu-id="614b4-168">Den här planeringsraden visar en ikon för en undantagsvarning som indikerar att säkerhetslagret delvis eller helt förbrukats och måste fyllas på genom en undantagsorder för det saknade antalet.</span><span class="sxs-lookup"><span data-stu-id="614b4-168">This planning line will display an Exception warning icon explaining to the planner that the safety stock has been partly or fully consumed by means of an exception order for the missing quantity.</span></span>  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a><span data-ttu-id="614b4-169">Prognostiserad efterfrågan minskas av försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="614b4-169">Forecast Demand is Reduced by Sales Orders</span></span>  
 <span data-ttu-id="614b4-170">Produktionsprognosen uttrycker förutsedd framtida efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-170">The production forecast expresses anticipated future demand.</span></span> <span data-ttu-id="614b4-171">Medan den faktiska efterfrågan anges, vanligtvis som försäljningsorder för producerade artiklar, förbrukar den prognosen.</span><span class="sxs-lookup"><span data-stu-id="614b4-171">While actual demand is entered, typically as sales orders for produced items, it consumes the forecast.</span></span>  

 <span data-ttu-id="614b4-172">Själva prognosen minskas inte egentligen av försäljningsorder: den förblir densamma.</span><span class="sxs-lookup"><span data-stu-id="614b4-172">The forecast itself is not actually reduced by sales orders; it remains the same.</span></span> <span data-ttu-id="614b4-173">Dock minskas prognosantalet som används i planeringsberäkningen (efter försäljningsorderantalet) innan det återstående antalet, om det finns något, anges i lagerprofilen för efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-173">However, the forecast quantities used in the planning calculation are reduced (by the sales order quantities) before the remaining quantity, if any, enters the demand inventory profile.</span></span> <span data-ttu-id="614b4-174">När planeringssystemet undersöker faktiska försäljningar under en period, ingår både öppna försäljningsorder och artikeltransaktioner från levererade försäljningar, om de inte härrör från en avropsorder.</span><span class="sxs-lookup"><span data-stu-id="614b4-174">When the planning system examines actual sales during a period, both open sales orders and item ledger entries from shipped sales are included, unless they are derived from a blanket order.</span></span>  

 <span data-ttu-id="614b4-175">En användare måste definiera en giltig prognosperiod.</span><span class="sxs-lookup"><span data-stu-id="614b4-175">A user is required to define a valid forecast period.</span></span> <span data-ttu-id="614b4-176">Datumet på det prognostiserade antalet anger startdatum för perioden, och datumet på nästa prognos definierar sedan slutet av perioden.</span><span class="sxs-lookup"><span data-stu-id="614b4-176">The date on the forecasted quantity defines the start of the period, and the date on the next forecast defines the end of the period.</span></span>  

 <span data-ttu-id="614b4-177">Prognosen för perioder före planeringsperioden används inte, oavsett om den förbrukades eller inte.</span><span class="sxs-lookup"><span data-stu-id="614b4-177">The forecast for periods prior to the planning period is not used, regardless of whether it was consumed or not.</span></span> <span data-ttu-id="614b4-178">Den första prognossiffran av intresse är antingen datumet på eller det närmaste datumet före planeringsstartdatumet.</span><span class="sxs-lookup"><span data-stu-id="614b4-178">The first forecast figure of interest is either the date on or the closest date prior to the planning starting date.</span></span>  

 <span data-ttu-id="614b4-179">Prognosen kan användas för icke härledd efterfrågan, t.ex. försäljningsorder, eller härledd efterfrågan, t.ex. produktionsorderkomponenter (modul-prognos).</span><span class="sxs-lookup"><span data-stu-id="614b4-179">The forecast can be for independent demand, such as sales orders, or dependent demand, like production order components (module-forecast).</span></span> <span data-ttu-id="614b4-180">En artikel kan ha båda typerna av prognos.</span><span class="sxs-lookup"><span data-stu-id="614b4-180">An item can have both types of forecast.</span></span> <span data-ttu-id="614b4-181">Under planeringen sker förbrukningen separat, först för härledd efterfrågan och sedan för icke härledd efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-181">During planning, the consumption takes place separately, first for independent demand and then for dependent demand.</span></span>  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a><span data-ttu-id="614b4-182">Avropsorderbegäran minskas med försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="614b4-182">Blanket Order Demand is Reduced by Sales Orders</span></span>  
 <span data-ttu-id="614b4-183">Prognostisering kompletteras av avropsorder som ett sätt att ange framtida efterfrågan från en specifik kund.</span><span class="sxs-lookup"><span data-stu-id="614b4-183">Forecasting is supplemented by the blanket sales order as a means of specifying future demand from a specific customer.</span></span> <span data-ttu-id="614b4-184">Som med den (ospecificerade) prognosen bör de faktiska försäljningarna förbruka den förutsedda efterfrågan, och det återstående antalet ska ingå i lagerprofilen för efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="614b4-184">As with the (unspecified) forecast, actual sales should consume the anticipated demand, and the remaining quantity should enter the demand inventory profile.</span></span> <span data-ttu-id="614b4-185">Förbrukningen minskar inte avropsordern.</span><span class="sxs-lookup"><span data-stu-id="614b4-185">Again, the consumption does not actually reduce the blanket order.</span></span>  

 <span data-ttu-id="614b4-186">Planeringsberäkningen beaktar öppna försäljningsorder länkade till den specifika avropsorderraden, men den beaktar inte någon giltig tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="614b4-186">The planning calculation considers open sales orders linked to the specific blanket order line, but it does not consider any valid time period.</span></span> <span data-ttu-id="614b4-187">Det tar inte heller hänsyn till den bokförda order, eftersom bokföringsproceduren redan har reducerat det utestående avropsorderantalet.</span><span class="sxs-lookup"><span data-stu-id="614b4-187">Nor does it consider posted orders, since the posting procedure has already reduced the outstanding blanket order quantity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="614b4-188">Se även</span><span class="sxs-lookup"><span data-stu-id="614b4-188">See Also</span></span>  
 <span data-ttu-id="614b4-189">[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="614b4-189">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="614b4-190">[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="614b4-190">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 <span data-ttu-id="614b4-191">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="614b4-191">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="614b4-192">Designdetaljer: Planeringsparametrar</span><span class="sxs-lookup"><span data-stu-id="614b4-192">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)
